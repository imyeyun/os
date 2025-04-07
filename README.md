# Gamatch - Game Agent Match Program

## 📌 과제 개요
- 충북대학교 운영체제 수업 과제 2
- 두 개의 게임 에이전트 프로그램이 4-in-a-row (Connect 4) 게임을 진행하도록 중계하는 프로그램입니다.
- 시스템 호출 (fork, exec, pipe, signal 등) 을 사용하여 프로세스를 관리합니다.

## 📂 파일 구성
- gamatch.c : 메인 소스 코드
- Makefile : 빌드 스크립트
- README.md : 프로그램 설명

## ⚙️ 빌드 방법
1. 프로젝트 폴더로 이동합니다.
2. 터미널에서 다음 명령어를 입력합니다.
3. <pre>c<br>make<br></pre>


3. 실행 파일 gamatch 가 생성됩니다.

## 🚀 실행 방법
기본 실행 예제:
<pre>c<br>./gamatch -X /opt/os/hw2/rand_agent -Y /opt/os/hw2/greedy_agent<br></pre>

명령어 형식:
<pre>c<br>./gamatch -X <agent_X_path> -Y <agent_Y_path><br></pre>


- `<agent_X_path>` : Player 1 (X) agent 프로그램 경로
- `<agent_Y_path>` : Player 2 (Y) agent 프로그램 경로

**주의:** 반드시 lab 서버 (sdevlab.cbnu.ac.kr) 에서 실행해야 정상 작동합니다.

## ✅ 프로그램 주요 기능
- agent 에게 stdin 으로 게임판 전달, stdout 으로 선택된 열 받기
- 3초 시간 제한, 시간 초과 시 상대 플레이어 승
- 잘못된 입력 (잘못된 열, 가득 찬 열 등) 시 상대 플레이어 승
- 게임 종료 후 자식 프로세스 정리
- Ctrl+C 시 프로그램 즉시 종료 및 자식 프로세스 종료

## 🧩 예제 Agent
학교 서버에서 제공하는 agent 들을 사용할 수 있습니다.
<pre>c<br>/opt/os/hw2/rand_agent /opt/os/hw2/greedy_agent /opt/os/hw2/agent_blue /opt/os/hw2/agent_red<br></pre>
