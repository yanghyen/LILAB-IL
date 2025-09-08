# 2509 첫째주
## ✅TO-DO
- ✅Word2Vec1 논문 읽기
- PyTorch 강의 수강
- ✅데이콘 체크
- ✅서버 세팅

## 📌This Week I Learned
### CBOW
- CBOW는 input에 과거 4개, 미래 4개의 단어를 사용해서 중간에 들어갈 단어 예측

### Skip-gram
- Skip-gram은 단어 하나를 두고, 그 주변 단어 예측 
- Skip-gram은 단어 예측에 집중해서 문법이나 구조에 약함 -> RNN과 결합하면 정확도 베리굿

### Word2Vec1 논문 결론
- 간단한 아키텍처로 기존 모델(feedforwarding NNLM, LSA,...)보다 높은 퀄리티 학습 가능. 계산 복잡도가 낮아서 **더 큰 데이터셋에서 더 큰 차원으로 학습이 가능**했기 때문.

### cond 가상환경
- conda: GPU 관련 라이브러리(PyTorch, TensorFlow)나 큰 과학/수치 계산 패키지 설치
- pip: 순수 Python 패키지 설치

## 💡 회고 / 인사이트
- 한 주를 계획하고 돌아보는 행위를 굉장히 오랜만에 하는 것 같다. 기록하는 것도 중요하지만 회고도 굉장히 중요하다. 아직 WIL에 무엇을 기록해야할지 기준이 모호하지만 하다보면 감이 올 것이다. 
- 생각보다 자유로운 시간에 길게 집중하기 어렵다. 어떤 시간대와 루틴이 내게 잘 맞는지 탐색해보자. 다음 주는 약속이 꽤 있어서 할 수 있을 때 부지런히 할 일을 해놔야 한다.ㄴ

## 💥 트러블슈팅
### 결국 conda 가상환경으로 진행
- systemd가 지원되지 않아서 docker 데몬 실행이 불가했다. docker 경험을 위해 사용해보려 했지만 conda로 진행했다. conda는 venv처럼 간단했다.

## 🍩Next Week Goals
- 밑딥시 Ch3-6
- PyTorch 강의 수강 
- Word2Vec2 논문 읽기
- CBOW 코드 재현
- Skip-gram 코드 재현