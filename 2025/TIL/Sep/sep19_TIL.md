# 250919
## ✅TO-DO
- 밑딥시 Ch4
- ✅CBOW 클론 코딩 50 epoch & gensim 구현 money~finance 유사도 값 비교
- ✅Skip-gram 클론 코딩 50 epoch & gensim 구현 money~finance 유사도 값 비교
- 클론 코딩 코드 분석 
- 언어에이전트 발표1 논문 훑기 

## 📌Today I Learned
### 학습을 GPU로 돌리려면 device 설정 필수 
- 어쩐지 CBOW랑 Skip-gram 학습이 오래 걸렸다. 내가 device 설정을 안 해서 cpu로 연산을 하고 있던 것이다^_^....
- ```watch -n 1 nvidia-smi```로 확인하면 된다.
- ```device = torch.device("cuda" if torch.cuda.is_available() else "cpu")```로 설정하면 된다.

### 모델 설계할 때 초기 값 차원수 잘 맞추기
- 행렬곱은 차원수가 잘 맞아야 계산 가능하니까여 

## 💡 회고 / 인사이트

## 💥 트러블슈팅

## 🍩주말 할 일 
- 클론 코딩 코드 분석 
- 언어에이전트 발표1 논문 훑기 