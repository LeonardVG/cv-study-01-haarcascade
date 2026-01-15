# Estudo 01: Haar Cascade

Este repositório contém um estudo prático sobre Visão Computacional, focando na implementação do algoritmo clássico **Haar Cascade** utilizando Python e OpenCV.

O código foi desenvolvido e testado no **Google Colab**.

## ⚠️ Importante: Como carregar as imagens

Neste notebook, utilizei imagens armazenadas no meu **Google Drive** para facilitar a persistência dos dados. Se você for executar este código, precisará ajustar o carregamento da imagem de uma das duas formas abaixo:

### Opção 1: Usando o Google Drive (Como está no código)
O código atual monta o drive (`drive.mount`) e busca as imagens em um caminho específico (ex: `/content/drive/MyDrive/...`).
* **Vantagem:** As imagens não somem quando você fecha o navegador.
* **Como usar:** Você precisará alterar o caminho no código para coincidir com a pasta onde **você** salvou suas imagens no seu Drive.

### Opção 2: Upload Manual (Temporário)
Se não quiser conectar seu Drive, você pode apenas arrastar a imagem para a aba de arquivos do Colab (ícone de pasta na esquerda).
* **Como usar:**
    1. Faça upload da imagem (ex: `teste.jpg`).
    2. No código, altere o caminho de leitura:
       ```python
       # De:
       img = cv2.imread('/content/drive/MyDrive/Pasta/imagem.jpg')
       # Para:
       img = cv2.imread('teste.jpg')
       ```
* **❗ Atenção:** O Google Colab apaga os arquivos locais sempre que o **Ambiente de Execução (Runtime)** é reiniciado. Se a sessão cair, você terá que fazer o upload da imagem novamente.

---

## 🧠 Sobre o Algoritmo Haar Cascade

Este notebook explora o método proposto por Viola e Jones (2001). É um algoritmo de detecção de objetos baseado em aprendizado de máquina, muito popular por sua velocidade e eficiência em detectar rostos frontais.

**O funcionamento baseia-se em:**
1.  **Haar Features:** Cálculo de diferenças de contraste (luz vs sombra) em regiões retangulares.
2.  **Imagens Integrais:** Uma técnica matemática para calcular essas diferenças de forma extremamente rápida.
3.  **Cascata de Classificadores:** O algoritmo descarta regiões de "não-rosto" rapidamente em vários estágios, focando o processamento apenas onde há alta probabilidade de haver um rosto.

> 📝 **Nota:** A explicação detalhada, incluindo a intuição sobre os parâmetros `scaleFactor` e `minNeighbors`, encontra-se escrita nas **células de texto dentro do próprio notebook**.

## 🛠️ Tecnologias
* Python
* OpenCV (`cv2`)
* Google Colab
