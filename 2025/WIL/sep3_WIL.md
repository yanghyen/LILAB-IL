# 2509 셋째주
## ✅TO-DO
- 위키독스 09-08~09-14 실습 진행
- ✅밑딥시 Ch3
- ✅밑딥시 Ch4
- 밑딥시 Ch5
- 밑딥시 Ch6
- PyTorch 강의 수강 
- ✅CBOW 코드 재현
- ✅Skip-gram 코드 재현
- MMS-LLaMA: Efficient LLM-based Audio-Visual Speech Recognition with Minimal Multimodal Speech Tokens 발표 준비(9/30)
- 언어에이전트 논문 리뷰 과제

## 📌This Week I Learned
### 학습된 모델 torch.save로 저장하기
### device 설정으로 gpu로 연산하기

## 💡 회고 / 인사이트
- 해야할 일이 무엇인지, 무엇을 위해 하는 일인지를 판단해서 위키독스 학습을 멈췄다. 모델을 코드로 구현하기 위해선 어떤 과정을 거쳐야 하는지 잘 모르겠어서 헤매고 있다. 

## 💥 트러블슈팅
### MNIST Load -> Keras MNIST
- 밑시딥 교재에서는 mnist load로 mnist를 불러왔지만, url이 잘 안돼서 keras에서 제공하는 mnist를 불러와서 사용했다. 
- keras는 데이터 로드랑 모델 정의를 분리해둬서 flatte, normalize, one_hot_lable 등의 기능을 제공하지 않아서 직접 구현해야 한다.

### ssh 외부 접속 불가 -> Tailscale
- ssh를 외부망에서 접속할 수 없어서 Tailscale을 활용해서 우회해서 접속했다.

### 연산이 지나치게 오래 걸린다 -> GPU 사용하고 있는지 체크
- 연산이 굉장히 오래 걸리길래 확인했더니 CPU로 연산하고 있었다^_^...
- ```device = torch.device("cuda" if torch.cuda.is_available() else "cpu")```로 설정하면 된다.

## 🍩Next Week Goals
- CBOW 직접 구현
- Skip-gram 직접 구현
- 밑바닥부터 시작하는 딥러닝 5, 6 학습
- Word2Vec 프로젝트 정리 및 paper 작성