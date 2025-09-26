# 250925
## ✅TO-DO
- 언어에이전트 발표1 준비
    - 논문 정리
    - 발표 개요 잡기
- CBOW 재구현 디렉토리 구성 
    - ✅src(eval.py)
    - scripts
    - ✅runs
    - README.md 작성

## 📌Today I Learned
### ssh환경에서 github 연결
1. ssh에 git 설치 ```sudo apt install git```
2. 키 생성: ```ssh-keygen -t ed25519 -C "your_email@example.com"``` 
3. GitHub 키 등록: ```~/.ssh/id_ed25519.pub``` 출력값 -> GitHub -> Settings -> SSH and GPG keys 등록
4. 키 추가: ```eval "$(ssh-agent -s)"  
ssh-add ~/.ssh/id_ed25519```
    - 키 등록 확인: ```ssh-add -l```
5. 원격 저장소 설정: ```git remote set-url origin git@github.com:yanghyen/Word2Vec-CBOW-PyTorch.git```
6. git push!

## 💡 회고 / 인사이트

## 💥 트러블슈팅

## 🍩내일 할 일 
- 언어에이전트 발표1 준비
    - 논문 정리
    - 발표 개요 잡기
- CBOW 재구현 디렉토리 구성 
    - scripts
    - README.md 작성
- CBOW 재구현 결과 분석
- Skip-gram 재구현 디렉토리 구성
    - src
    - configs
    - data
    - scripts
    - runs
    - README.md 작성