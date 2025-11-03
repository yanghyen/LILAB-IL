# 251029
## ✅TO-DO
- ✅Word2Vec 스트리밍 코드 수정 -> 학습 가능하도록 
- Word2Vec 실험 목록 정리
    - 논문 읽고 실험 정리
    - config 파일 만들어두기
    - ver2의 결과물 경로 파악
- Word2Vec paper 작성

## 📌Today I Learned
### <UNK>

## 💡 회고 / 인사이트

## 💥 트러블슈팅
### 문제상황: 6.9B 데이터셋 학습했는데 loss가 증가했다.
- lr이 너무 커서 그럴지도?
- <UNK> 토큰이 vocab_data.pkl에 포함되지 않았다.
### 해결방법: lr = 0.0025 -> lr = 0.001로 변경 
- 아직 해결된 건 아님 

## 🍩내일 할 일 
- Word2Vec 실험 목록 정리
    - 논문 읽고 실험 정리
    - config 파일 만들어두기
    - ver2의 결과물 경로 파악
- Word2Vec paper 작성