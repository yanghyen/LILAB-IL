# 251203
## ✅TO-DO🎠
- ✅ELMo 개념 학습
    - ✅논문 읽기(5.3~)
- ELMo 레퍼런스 코드 실행해보기
- 10월 MIL 작성
- 11월 MIL 작성 
- 심리학 연구 논문1 읽기 

## 📌Today I Learned
### ELMo 사전학습
1. Character embedding (char lookup)
2. Character-level CNN (char-CNN)
3. Highway networks (2-layer)
4. Projection (to LSTM input, 512d)
5. 2-layer bidirectional LSTM (biLM)
6. Softmax LM heads (forward & backward)
```
raw text -> tokenized words -> each word -> chars -> char embeddings
  -> char-CNN convs -> concat -> highway -> projection(512)  # layer0 (512)
  -> biLSTM layer1 -> proj -> h^1 (1024)                     # layer1
  -> biLSTM layer2 -> proj -> h^2 (1024)                     # layer2
  -> LM heads -> forward/backward softmax (compute LM loss)
```

## 💡 회고 / 인사이트

## 💥 트러블슈팅

## 🍩내일 할 일 