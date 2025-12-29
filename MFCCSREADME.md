# Análise Exploratória de Áudio com Librosa 🔊

Projeto prático de processamento de sinais de áudio usando **Python** e a biblioteca **Librosa** no Google Colab.

Transformei um áudio bruto em visualizações e features numéricas compactas, mostrando o poder da redução de dimensionalidade no audio processing.

## Visualizações Geradas

### 1. Waveform (Forma de Onda)
Mostra a amplitude do sinal ao longo do tempo.

![Waveform](analise%20audio.png)

### 2. Espectrograma Mel
Representação frequencial na escala Mel (como o ouvido humano percebe o som).

![Espectrograma Mel](audioMel.png)

### 3. MFCCs (Mel-Frequency Cepstral Coefficients)
Extraí os 13 coeficientes MFCC clássicos – o pipeline completo (windowing → FFT → Mel filterbank → log → DCT) está implementado.

- Matriz resultante: 13 coeficientes × número de frames temporais
- Visualização do heatmap dos MFCCs está no notebook (próximo passo: salvar como imagem)

## Redução de Dimensionalidade Incrível
- Áudio bruto → milhões de amostras de amplitude
- Após processamento → **apenas 13 números** que resumem a "alma" do som (timbre essencial)

**Coeficientes MFCC médios calculados neste áudio**:
MFCC 1:  -123.83
MFCC 2:  +168.10
MFCC 3:   -58.69
MFCC 4:   +50.19
MFCC 5:    -2.98
MFCC 6:   +26.44
MFCC 7:    +1.37
MFCC 8:    -6.63
MFCC 9:    +0.92
MFCC 10:   -4.81
MFCC 11:   +3.66
MFCC 12:   -5.84
MFCC 13:   +1.80


Análise preliminar: perfil muito próximo de **música pop/rock** – alta energia em frequências médias-altas e distribuição harmônica rica.

## Como Executar
Abra o notebook diretamente no Google Colab e faça upload do seu próprio áudio:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bgambaroni/analisedeaudio/blob/main/MFCCS.ipynb)

## Tecnologias Utilizadas
- Python
- Librosa
- Matplotlib
- Google Colab

## Próximos Passos
- Salvar o heatmap dos MFCCs como imagem e adicionar aqui
- Calcular delta e delta-delta (total de 39 features)
- Comparar múltiplos áudios via distância cosseno
- Classificação simples (fala × música × ambiente)
- Clustering automático de vários arquivos

#Python #AudioProcessing #Librosa #DataScience #MachineLearning #SignalProcessing
