# Implementação de Técnicas de Pré-Processamento de Imagens

Este repositório contém as implementações das quatro tarefas solicitadas no trabalho de Processamento Digital de Imagens.  
O projeto foi desenvolvido em Python e organizado em um único notebook executável (Google Colab), contendo código, explicações e relatório.

---

## 📌 Funcionalidades Implementadas

### **1) Clusterização de Tons de Cinza**
Converte uma imagem colorida para tons de cinza e reduz a quantidade de níveis agrupando os valores em blocos (ex.: agrupar a cada 4 → 64 tons finais).

Função:  
`grayscale_cluster(img, group_size=4)`

### **2) Subtração de Imagens + Detecção do Corpo**
Processo:
1. Tirar uma foto do fundo (background)
2. Tirar uma foto com o corpo na mesma posição de câmera
3. Converter ambas para tons de cinza
4. Subtrair as imagens
5. Binarizar com limiar manual
6. Encontrar regiões com contorno
7. Marcar com retângulo vermelho

Função:  
`detectar_corpo(bg, person, thresh=30, min_area=500)`

### **3) Filtro High-Boost + Comparação com Filtro Passa-Alta**
Filtros implementados manualmente:
- High-Boost: realce de detalhes baseado na máscara da diferença
- Passa-alta: kernel Laplaciano clássico

Funções:  
`high_boost(img, A=1.5)`  
`high_pass(img)`

### **4) Comparação de Convolução Direta vs FFT**
Demonstra o ganho computacional do Teorema da Convolução:

- Convolução direta → `cv2.filter2D`
- Convolução no domínio da frequência → FFT 2D

Funções:  
`conv_time(img, kernel)`  
`fft_time(img, kernel)`

---

## Como Executar

### No Google Colab
1. Fazer upload do notebook  
2. Instalar dependências se necessário  
3. Executar as células em sequência  
4. Fazer upload das imagens quando solicitado  

### Localmente (Jupyter / VSCode)
Criar ambiente virtual:

## 📝 Relatório
O relatório está incluído no final do notebook e traz:
- Objetivo de cada tarefa  
- Imagens de entrada e saída  
- Comparações entre técnicas  
- Avaliação dos tempos (convolução × FFT)  
- Conclusões finais  

##  Autores 
**Adalberto Santos**  
Ciência da Computação

**Diogo Azevedo Batagini**  
Ciência da Computação

