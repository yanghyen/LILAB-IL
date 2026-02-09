# 260209
## 🔥Challenge💧
- 💧일찍 출근: 11:30
- 1일1논문: TAID 발표 준비
- 1일1구현: cross-lingual RAG (https://arxiv.org/abs/2505.10089)
  - https://github.com/amazon-science/XRAG?utm_source=chatgpt.com 

## ✅TO-DO🎠
- 진행사안 탭 관리
- 🎠TFM) 학습 가능한 코드 구현 
  - ✅vocab은 bpe 잘 적용돼서 생성됐는지 확인
  - ✅dataloader.py 
  - token embedding, positional encoding (sin/cos or learned) -> 여기까지 하고 발표 준비 
  - scaled dot-product attention
  - multi-head attention
  - add & layerNorm
  - FFN
  - encoder block
  - decoder block
  - 전체 모델 테스트 
- 세미나) TAID 논문 읽기 
  - ✅지금까지 읽은 내용 복기
  - ✅3.1 읽기
  - 3.2, 4, 5 읽기 

## 📌Today I Learned
### 모델 별 특성 찾아보기


## 💡 회고 / 인사이트
### 교수님 면담
- 모델 구현할 때 구현 다 마치고 eval로 판단하지 말고
- 단계 별로 모델 구현이 잘 됐는지 하나하나 내 눈으로 체크를 한 뒤에 나아가기

## 💥 트러블슈팅
### vocab.pkl에 영어와 독일어가 아닌 다른 언어가 포함돼있었다
- preprocess.py에서 생성한 vocab.pkl 파일을 확인해봤다. tail을 살펴봤더니 한자, 가타카나, 한글이 출력됐다.
- 이래서 데이터나 output을 직접 확인해봐야 되는구나

## 🍩내일 할 일 
- 진행사안 탭 관리
- 🎠TFM) 학습 가능한 코드 구현 
  - token embedding, positional encoding (sin/cos or learned) 
  - scaled dot-product attention
  - multi-head attention
  - add & layerNorm
  - FFN
  - encoder block
  - decoder block
  - 전체 모델 테스트 
- 세미나) TAID 논문 읽기 
  - 3.2, 4, 5 읽기 