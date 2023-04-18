# Ansible

## Infrastructure As Code, IaC

- 시스템, 하드웨어 또느 인터페이스의 구성정보를 파일을 통해 관리 및 프로비저닝
- 물리 및 가상 머신과 관련된 구성 리소스를 관리
- 버전 관리를 통한 리소스 관리

## Ansible

- 여러개의 서버를 효율적으로 관리할 수 있게 해주는 환경 구성 자동화 도구
  - Configuration Management, Deployment & Orchestration tool
  - It infrastructure 자동화
- Push 기반 서비스
- 에이전트 불필요

### 가능한 작업

- 설치
  - apt-get, yum, homebrew
- 파일 및 스크립트 배포
  - copy
- 다운로드
  - get_url, git
- 실행
  - shell, task

### 실행 옵션

- `-i`
  - `--inventory-file` 
  - 적용 될 호스트들에 대한 파일 정보
  - `/etc/ansible/hosts`
- `-m`
  - `--module-name` 
  - 모듈 선택
- `-k`
  - `--ask-pass`
  - 관리자 암호 요청
- `-K`
  - `--ask-become-pass`
  - 관리자 권한 상승
- `--list-hosts`
  - 적용되는 호스트 목록
- 멱등성
  - 같은 설정을 여러번 적용하더라도 결과가 달라지지 않음
  - copy 가 여러번 하더라도 같은 내용이라면 한번만 적용된다

### Playbook

- 사용자가 원하는 내용을 미리 작성해 놓은 파일
  - 설치, 파일 전송, 서비스 재시작 등
  - 여러 서버에 반복 작업을 처리해야하는 경우