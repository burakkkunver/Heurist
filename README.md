# Heurist

Gerekliyse;
```bash
apt install sudo
  ```
Güncellemeler klasiks
```bash
sudo apt-get update && sudo apt-get upgrade
sudo apt install curl git wget htop screen tmux build-essential jq make lz4 gcc unzip gcc clang cmake build-essential -y


sudo apt update && sudo apt install python3.10-venv python3-venv python3-pip
sudo apt-get update && sudo apt-get upgrade
sudo apt install -y build-essential gcc git curl wget python3-pip python3-venv

pip install torch torchvision --index-url https://download.pytorch.org/whl/cu118
```

Anaconda kuralıms

```bash
wget https://repo.anaconda.com/archive/Anaconda3-2023.07-1-Linux-x86_64.sh

bash Anaconda3-2023.07-1-Linux-x86_64.sh

source ~/.bashrc

```

Screen açıp dosyaları çekelim;

```bash
screen -S heurist
```

```bash
conda create --name heurist-miner python=3.11 -y
conda activate heurist-miner

git clone https://github.com/heurist-network/miner-release.git
cd miner-release

pip install -r requirements.txt

```
PyTorch ve CUDA'yı Kuralım ( en son true çıkıyorsa başaralı)

```bash
conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
```

```bash
python -c "import torch; print(torch.cuda.is_available())"

```

Miner kimliği ve ödüller için biz cüzdan belirleyelim public key yazıcaz

```bash
nano .env
```

Bir env dosyası oluşturduk aşağıdaki kısmı  0x ile başlayan cüzdan adresi yazıp env dosyasına yapıştıralım kaydedip çıkalım

```bash
MINER_ID_0=0xYourWalletAddressHere

```

Bir id wallet oluşturucaz ( sadece güvenlik için, kesinlikle kelimeleri ve adresi komple kaydedelim. Sonrasında import için yine bu kod kullanılacak)

```bash
python3 ./auth/generator.py

```

Her şey tamam çalıştıralım ve kazalım (:


```bash

python sd-miner.py

```

Eğer daha büyük dosyalarla çalışılmak isteniyorsa (daha fazla puan vermedi ama verebilir dcden hangi model ile çalışılmak isteniyorsa seçilmeli)



```bash
./llm-miner-starter.sh <model_id>

```

Örnek model ID: dolphin-2.9-llama3-8b















