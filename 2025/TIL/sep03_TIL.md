# 250903
## ✅TO-DO
- ✅Word2Vec 논문 읽기 (2. Model Architectures까지)
- ✅서버 세팅
    - ~~docker 이미지 생성 후 Python, PyTorch, CUDA 설치 및 버전 관리~~
    - ✅conda 가상환경으로 Word2Vec 환경 세팅 

## 📌Today I Learned
### conda 가상환경 생성
```
# 가상환경 생성
conda create -n word2vec python=3.10 -y

# 가상환경 활성화
conda activate word2vec

# PyTorch + CUDA 12.8 설치
conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia -y
```
- conda: GPU 관련 라이브러리(PyTorch, TensorFlow)나 큰 과학/수치 계산 패키지 설치
- pip: 순수 Python 패키지 설치

## 💡 회고 / 인사이트

## 💥 트러블슈팅
### 결국 conda 가상환경으로 진행
- 내 서버는 systemd가 지원되지 않았다. 그래서 Docker 데몬을 실행할 수 없어서 Docker는 포기했다. 
- ```ps -p 1 -o comm=```로 확인해보니 PID 1이 sshd로 되어 있다. 
- systemd는 리눅스에서 프로세스와 서비스를 관리하는 init 시스템이다. init 시스템은 부팅 후 가장 먼저 실행되는 프로세스로, 시스템을 초기화하고 서비스(데몬)를 실행하는 역할을 담당한다.
- 요즘 서버는 주로 PID 1이 systemd라는데, 왜 내 서버는 PID 1이 sshd일까?.. gpt는 "SSH 접속만 가능하고 일반적인 system 섭시ㅡ 관리가 없는 환경"으로 컨테이너, 제한된 가상 환경, HPC 계열 서버에서 발생한다고 한다.
- 관리자가 불필요한 데몬을 최소화하기 위해 SSH 접속만 가능하게 설정한 것 같다. -> 여쭤보장 
- conda 가상환경으로 진행하니 간단하게 서버 세팅을 마쳤다. 

## 🍩내일 할 일
- PyTorch 강의 수강 (파이토치 한번에 끝내기)
- Word2Vec 논문 읽기 (끝까지 ^_ㅠ)