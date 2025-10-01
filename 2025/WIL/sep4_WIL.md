# 2509 넷째주
## ✅TO-DO
- ✅CBOW 직접 구현
- Skip-gram 직접 구현
- 밑바닥부터 시작하는 딥러닝 5, 6 학습
- Word2Vec 프로젝트 정리 및 paper 작성

## 📌This Week I Learned
### 학습을 GPU로 돌리려면 device 설정 필수 
- ``device = torch.device("cuda" if torch.cuda.is_available() else "cpu")```

### Hierarchical softmax
- 단어를 허프만 이진 트리의 잎 노드로 배치하고, 중심 단어에서 타겟 단어까지 리프로 가는 경로의 확률만 계산

### AVSR
- MMS LLaMA 논문을 공부하며 알게된 것들이다.
- AVSR: 노이즈가 있는 환경에선 음성파일이 손상돼있을 확률이 크다. 그래서 Visual data를 Audio data와 함께 넣어서 음성을 텍스트로 변환한다.

### random seed 고정
- 초기 가중치, shuffling, random samplingㅇ이 원래는 랜덤하게 진행되지만, 정확한 실험을 위해서 seed를 고정해주면 고정된 값이 추출된다.
- ```train.py```에 설정하면 된다.

### configs/*.yaml으로 실행하기
- ``python train.py --config configs/brown.yaml``` 이런 명령어로 실행할 수 있다.
- python에서 제공하는 ```argparse```를 사용한다.
```py
parser = argparse.ArgumentParser()
parser.add_argument("--config", type=str, default="configs/brown.yaml")
args = parser.parse_args()

with open(args.config, "r") as f:
    config = yaml.safe_load(f)
```

## 💡 회고 / 인사이트
### 방향성만 잘 잡으면 해보면서 깊어진다.
- 논문 발표 준비도 그렇고 모델 구현 모두 초반에 방향성을 잡기 위해 이해하는 초기 단계가 중요하다. 하지만 여기서 시간을 과도하게 끌면 조금 곤란하다. 나중에 엄청 촉박해진다.
- 처음부터 100% 이해하고 시작하려 하지 말고 어느정도 플로우가 이해됐다면 피피티 제작이나 코드 구현에 도입하는 게 좋은 것 같다.

## 💥 트러블슈팅

## 🍩Next Week Goals
- Skip-gram 재구현
- Word2Vec paper 작성
- 