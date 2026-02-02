# 🚗 Don’t Sleep (Detector de Sonolência)

Sistema inteligente de **alerta de sonolência para motoristas**, utilizando visão computacional para detectar quando o condutor fecha os olhos por alguns segundos e emitir um alerta imediato.  

> ⚠️ **Atenção**: este projeto **não substitui** práticas seguras de direção. É apenas um **assistente adicional**.  
> Se estiver com sono, **pare o veículo com segurança e descanse**.

---

## 🧠 Visão Geral

O **Don’t Sleep** é um sistema voltado para **prevenção de acidentes causados por fadiga**.  
Ele utiliza a webcam do computador (ou câmera embutida) para identificar **fechamento ocular prolongado**, característico de sonolência, e aciona um **alerta sonoro/visual**.

### 🔍 Recursos principais
- 👁️ Detecção de olhos e cálculo do **EAR (Eye Aspect Ratio)**  
- ⏱️ Monitoramento contínuo para detectar **fechamento prolongado dos olhos**  
- 🔊 Emissão de alerta sonoro quando detectada sonolência  
- 🖥️ Compatível com **webcam** e **vídeos gravados**  
- ⚙️ Parâmetros ajustáveis (limiar de detecção, tempo de alerta, sensibilidade)

---

## 🧰 Tecnologias Utilizadas

- **Python 3.10+**
- **OpenCV** – processamento de vídeo e imagem  
- **MediaPipe** ou **Dlib** – detecção facial e landmarks  
- **NumPy** – cálculos matemáticos  
- **Playsound** ou **Winsound** – emissão de som  

> 🔧 Ajuste conforme as bibliotecas que você realmente usa.

---

## 🚀 Como Executar o Projeto

### 1️⃣ Pré-requisitos

- Python 3.10 ou superior  
- Pip atualizado
 
- python -m pip install --upgrade pip
  
### 2️⃣ Clonar o repositório
- git clone https://github.com/lucasm9140/prova_tarde.git
- cd prova_tarde


- 🔧 Caso altere o nome do repositório, atualize o link acima.

### 3️⃣ Criar ambiente virtual (recomendado)
- Windows
- python -m venv .venv
- .venv\Scripts\activate

- Linux/Mac
- python -m venv .venv
- source .venv/bin/activate

### 4️⃣ Instalar dependências
- pip install -r requirements.txt


- 🔧 Se ainda não tiver o arquivo requirements.txt, crie um contendo:

- opencv-python
- mediapipe
- numpy
- playsound

### 🧪 Como Testar o Sistema

- Você pode realizar os testes usando sua webcam ou um vídeo gravado.

- ▶️ Teste com Webcam (tempo real)

- Conecte uma webcam ao computador (ou use a embutida no notebook).

- No terminal, execute:

- python main.py


- O sistema abrirá uma janela mostrando sua imagem.

- Pisque normalmente — piscadas curtas não devem gerar alerta.

- Feche os olhos por 2–3 segundos para testar o alerta sonoro/visual.

- Caso o alerta esteja sensível demais, ajuste os parâmetros (veja abaixo).

### 🎥 Teste com Vídeo Gravado (opcional)

- Adicione um vídeo de alguém piscando e depois fechando os olhos por alguns segundos em uma pasta tests.

- Execute:

- python main.py --video ./tests/sonolencia.mp4


- O sistema analisará o vídeo e emitirá alertas quando detectar fechamento ocular prolongado.

### ⚙️ Parâmetros (exemplo)
- python main.py --ear-threshold 0.25 --frames-closed 15 --cooldown 2

- Parâmetro	Descrição
--ear-threshold	Limite para considerar olho fechado (padrão: 0.25)
--frames-closed	Número de frames consecutivos antes de disparar alerta
--cooldown	Tempo mínimo entre alertas
### 🗂️ Estrutura do Projeto
prova_tarde/
├── main.py                # Arquivo principal
├── detector/              # Lógica de detecção
│   ├── eyes_detector.py
│   ├── alerts.py
│   └── utils.py
├── tests/                 # Vídeos de teste
│   └── sonolencia.mp4
├── requirements.txt
└── README.md


- 🔧 Ajuste conforme a estrutura real do seu repositório.

- 🔉 Alertas

- Visual: mensagem “⚠️ SONOLÊNCIA DETECTADA” sobre o vídeo

- Sonoro: toque curto e alto

- Logs (opcional): registros de eventos de alerta com data/hora

### ⚠️ Limitações

- Ambientes com baixa iluminação reduzem precisão

- Óculos escuros ou ângulo desfavorável da câmera podem impedir detecção

- Pode ser necessário ajustar o threshold conforme o rosto e a câmera usada

### 📈 Próximas Etapas (Roadmap)

 - Detecção de bocejo

 - Reconhecimento de inclinação da cabeça

 - Interface gráfica (Dashboard de eventos)

 - Versão mobile / integração IoT

 - Dashboard de monitoramento remoto

### 🔐 Privacidade e Ética

- O processamento é totalmente local, sem envio de dados ou vídeo para servidores.

- Nenhuma imagem é salva sem consentimento.

- O projeto tem caráter educacional e experimental.

### 🤝 Contribuição

- Faça um fork do projeto

- Crie uma nova branch:

- git checkout -b feature/nova-funcionalidade


- Envie suas alterações:

- git commit -m "Adiciona nova funcionalidade X"
- git push origin feature/nova-funcionalidade


- Abra um Pull Request descrevendo suas alterações

### 🧾 Licença

- Este projeto está sob a licença MIT — veja o arquivo LICENSE
 para mais detalhes.

### 👨🏽‍💻 Autor

- Lucas Matheus Rodrigues de Jesus (AxionTechI9) feito em sala de aula.

✉️ lucas14fdk@gmail.com
