# 260102
## 🔥Challenge💧
- 💧일찍 출근: 11:00
- 🔥1일1논문: Accelerating Scientific Discovery with Autonomous Goal-evolving Agents 마무리
- 1일1논문: TAID: Temporally Adaptive Interpolated Distillation for Efficient Knowledge Transfer in Language Models (ICLR 2025 Spotlight)
- 1일1구현: cross-lingual RAG (https://arxiv.org/abs/2505.10089)
  - https://github.com/amazon-science/XRAG?utm_source=chatgpt.com 

## ✅TO-DO🎠
- ✅ELMo) 디렉토리 정리 후 커밋
- ✅ELMo) 전처리 확인 -> 다시 진행 중 
- ✅ELMo) 트러블 슈팅 작성 -> 데이터 전처리 시 UNK 토큰 개수 2000개 대 
- Transformers) wikidocs 3, 4
- ✅Transformers) ref code 찾기 https://ysg2997.tistory.com/11 https://nlp.seas.harvard.edu/2018/04/03/attention.html 
- 디동) “Think Twice”: Perspective-Taking Improves LLMs’ Theory-of-Mind Capabilities – ACL 2024 읽기 

## 📌Today I Learned
### 모델 별 특성 찾아보기


## 💡 회고 / 인사이트

## 💥 트러블슈팅
### biLM Collapse 버그
1. 학습과 평가 시 다른 Projection 사용
- 학습할 땐 forward_projection, backward_projection으로 각각 학습
- 평가할 때 get_representations 메서드를 통해 projection 가져오는데, 이때 lstm_projection 가져왔음

2. tied_weight 무분별 사용
- tied_weight란 입력 임베딩 가중치와 출력 가중치를 동일하게 쓰는 기법
- 차원을 맞추려고 임시 해결책으로 적용했을 것

3. 잘못된 dropout 위치
- projection 이후

4. ⭐학습 시 대부분 토큰이 UNK (85%)
```bash
forward_target unique labels: (
    tensor([1, 6, 9, 10, 6793, 20688, ...], device='cuda:0'),  # ← 고유 label 값들
    tensor([2635, 4, 4, 8, 1, 1, 1, ...], device='cuda:0')     # ← 각 label의 개수
)
```
- Label 1 (UNK)가 2635개(전체 토큰 3072개)
- `word2idx = limited_word2idx`가 문제됨
    - 대체 왜 인덱싱 과정에서 100k로 제한한 걸 덮어씌운 걸까요
    - ⭐⭐⭐인덱싱 과정에선 원본 데이터 써야 함
    - corpus → 3.5M(원본) vocab으로 인덱싱 → 원본 인덱스(0~3.5M) → 재매핑: 빈도 기준(낮은 빈도 → UNK)
    - 이전에는 코퍼스 단어들을 100K vocab으로 인덱싱 했음 ⇒ 대부분의 단어가 UNK가 됨


## 🍩내일 할 일 
- Transformers) wikidocs 3, 4
- 디동) “Think Twice”: Perspective-Taking Improves LLMs’ Theory-of-Mind Capabilities – ACL 2024 읽기 
- ELMo) epoch 1 eval (16시 예상)
- Transformers) 블로그 읽기 https://ysg2997.tistory.com/11 https://nlp.seas.harvard.edu/2018/04/03/attention.html 
- CS224N) 1강 수강 