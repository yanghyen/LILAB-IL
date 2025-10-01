# 250924
## ✅TO-DO
- 언어에이전트 발표1 논문 정리
- CBOW 재구현 디렉토리 구성 
    - src
    - ✅configs
    - ✅data
    - scripts
    - runs
    - README.md 작성

## 📌Today I Learned
### src/train.py에 랜덤시드 고정하기
- 초기 가중치, shuffling, random sampling이 원래는 랜덤하게 진행되지만, 정확한 실험 결과를 위해서 seed를 고정해주면 고정된 값이 할당됨
- gpu(cuda)로 돌릴 때도 연산 결과 일정하도록 설정
    - ```torch.backends.cudnn.deterministic = True```
    - ```torch.backends.cudnn.benchmark = False```

### configs/*.yaml 불러와서 학습 실행하기
- ```python train.py --config configs/brown.yaml``` 이렇게 yaml파일로 실행할 수 있다.
- python에서 제공하는 ```argparse```를 사용한다.
```py
parser = argparse.ArgumentParser()
parser.add_argument("--config", type=str, default="configs/brown.yaml")
args = parser.parse_args()

with open(args.config, "r") as f:
    config = yaml.safe_load(f)
```
- 이렇게 config를 정의하면 나중에 config["embedding_dim"]으로 불러오면 된다.

## 💡 회고 / 인사이트
### 코드 재구현과 실험에 더 시간을 분배하자
- 9월엔 첫 달이라 적응하고 어떻게 해나갈지 방향을 잡는데 시간이 좀 걸렸다. 여러 학습 방법을 시도하느라 모델 재구현을 시작하는 시기가 늦어졌다.
- 앞으로는 intern instruction에 맞춰 데이터셋 별 + 최소 실험 + 분석 요구사항 작성 등에 시간을 더 분배하자.

## 💥 트러블슈팅

## 🍩내일 할 일 
- 언어에이전트 발표1 준비
    - 논문 정리
    - 발표 개요 잡기
- CBOW 재구현 디렉토리 구성 
    - src(eval.py)
    - scripts
    - runs
    - README.md 작성