# 250918
## ✅TO-DO
- ✅맥북 jump host로 ssh 접속 문제 해결
- 밑딥시 Ch4.3까지
- CBOW 클론 코딩 50 epoch & gensim 구현 money~finance 유사도 값 비교
- Skip-gram 클론 코딩 50 epoch & gensim 구현 money~finance 유사도 값 비교
- 클론 코딩 코드 분석 
- 언어에이전트 발표1 논문 훑기 

## 📌Today I Learned

## 💡 회고 / 인사이트

## 💥 트러블슈팅
### SSH 외부 접속 환경 구축
### 상황
- 학교 규정상 연구실 PC는 외부망에서 직접 SSH 접속 불가
- 원래는 GUI 기반 VPN/ZeroTier로 접속하려고 했지만, 기존 설치된 GUI가 실행되지 않음
### 해결과정
1. Tailscale 설치
- ZeroTier 대신 Tailscale 사용
- Tailscale은 WireGuard 기반의 VPN 서비스로, 별도의 포트 포워딩 없이도 기기 간 안전하게 사설 네트워크를 구축할 수 있음
2. SSH 계정 문제
- 연구시 PC 계정의 비밀번호 확인 불가 -> SSH 로그인 불가
- Microsoft 계정 비밀번호 또는 PIN은 SSH 인증용 비밀번호로 사용할 수 없음
3. 로컬 계정 생성
- PowerShell에서 로컬 계정 sshuser 생성 및 비밀번호 설정
### 결과 
- 맥북 → Tailscale VPN → 연구실 PC(sshuser) → 최종 서버(lilab) SSH 연결 성공
- SSH 외부 접속 환경이 안전하게 구축됨
### 배운 점 
- 외부망 제한 환경에서 SSH 접속을 우회하려면 사설 VPN + 로컬 계정 조합이 유용함
- Tailscale은 GUI가 안 되거나 포트 포워딩이 어려운 환경에서도 빠르고 안전하게 네트워크 연결을 제공함

## 🍩내일 할 일