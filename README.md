# 👁️ Sistema de Segmentação e Reconhecimento de Íris

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

**Status do Projeto: ✔️ Concluído**

## 📖 Descrição

Este projeto acadêmico implementa um sistema completo de biometria baseado em reconhecimento de íris. O objetivo é aplicar técnicas de processamento de imagem para segmentar a região da íris em uma imagem de um olho, extrair suas características únicas e, por fim, compará-las com uma base de dados para identificar um indivíduo.

A metodologia é amplamente baseada nos algoritmos propostos por John Daugman, uma referência na área de biometria por íris.

## ✨ Funcionalidades

O pipeline do projeto segue as seguintes etapas:

1.  **Pré-processamento:** Tratamento inicial da imagem para remoção de ruídos e reflexos, utilizando técnicas como a aplicação do filtro Gaussiano.
2.  **Segmentação da Íris:** Isola a região da íris (a área entre a pupila e a esclera) utilizando o **Operador Integrodiferencial de Daugman** para encontrar as bordas circulares internas e externas.
3.  **Normalização:** Transforma a imagem da íris segmentada de coordenadas cartesianas para um sistema de coordenadas polares. Esse processo, conhecido como "modelo rubber sheet", cria uma representação retangular com dimensões padronizadas, que é invariante a variações de tamanho da pupila e rotação do olho.
4.  **Extração de Características e Reconhecimento:**
    * Gera um "código da íris" (IrisCode), um template binário que representa a textura única da íris.
    * Utiliza a **Distância de Hamming** para medir a dissimilaridade entre dois códigos de íris. Quanto menor a distância, mais similares são as íris, permitindo a identificação do indivíduo na base de dados.

## 🛠️ Tecnologias Utilizadas

- **Python:** Linguagem principal do projeto.
- **OpenCV (`cv2`):** Para tarefas de processamento de imagem, como leitura, filtros e detecção de círculos.
- **NumPy:** Para manipulação eficiente de arrays e cálculos matemáticos complexos.
- **Pandas:** Para carregar e manipular os dados dos "códigos de íris" armazenados.
- **Matplotlib:** Para visualização dos resultados e das etapas do processamento.
- **SciPy:** Utilizada para cálculos específicos, como a Distância de Hamming.
- **Google Colab:** Ambiente de desenvolvimento utilizado para executar o notebook.

## 📊 Dataset

O projeto utiliza o banco de dados **CASIA-Iris-Thousand**, que contém imagens de íris de alta qualidade, amplamente utilizado para pesquisa e desenvolvimento de sistemas de reconhecimento.

- **Link para o dataset:** [Kaggle: CASIA-IRIS-THOUSAND](https://www.kaggle.com/datasets/sondosaabed/casia-iris-thousand/data)

## 🚀 Como Executar o Projeto

Este projeto foi desenvolvido para ser executado no ambiente Google Colab. Siga os passos abaixo:

1.  **Baixe o Dataset:** Acesse o link acima, baixe as imagens e descompacte-as em seu computador.
2.  **Prepare o Ambiente no Colab:**
    * Abra o notebook `SegmentacaoReconhecimentoIris.ipynb` no Google Colab.
    * No painel lateral esquerdo, clique na aba **"Arquivos"** (ícone de pasta).
    * Crie uma nova pasta chamada `img`.
3.  **Faça o Upload das Imagens:** Arraste as imagens do dataset da sua máquina para dentro da pasta `img` recém-criada no Colab.
4.  **Execute as Células:** Com as imagens no local correto, execute todas as células do notebook em ordem.

## 👨‍💻 Autores

Este projeto foi desenvolvido por:

- **Pietro Bernardo Dutra Scaglione**
- **Samuel Gerga Martins**
