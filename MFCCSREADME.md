# Análise Exploratória de Áudio com Librosa 🔊

Projeto prático de processamento de sinais de áudio usando **Python** e a biblioteca **Librosa** no Google Colab.

Transformei um áudio bruto em visualizações e features numéricas compactas, mostrando o poder da redução de dimensionalidade no audio processing.

## Visualizações Geradas

### 1. Waveform (Forma de Onda)
Mostra a amplitude do sinal ao longo do tempo.

![Waveform](waveform.png)

### 2. Espectrograma Mel
Representação frequencial na escala Mel (como o ouvido humano percebe o som).

![Espectrograma Mel](melspectrogram.png)

### 3. MFCCs (Mel-Frequency Cepstral Coefficients)
Extraí os 13 coeficientes MFCC clássicos – o pipeline completo (windowing → FFT → Mel filterbank → log → DCT) está implementado.

- Matriz resultante: 13 coeficientes × número de frames temporais
- Visualização do heatmap dos MFCCs está no notebook (próximo passo: salvar como imagem)

## Redução de Dimensionalidade Incrível
- Áudio bruto → milhões de amostras de amplitude
- Após processamento → **apenas 13 números** que resumem a "alma" do som (timbre essencial)

**Coeficientes MFCC médios calculados neste áudio**:
