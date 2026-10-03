1. 파일 다운로드 및 옮기기 (USB / 망연계 시스템 활용):
    GitHub 저장소에서 코드 내려받기 (requirements.txt 포함)
    Release 페이지에서 openwebui_offline_pkgs.zip 다운로드하여 압축 해제

2. 폐쇄망 PC에서 설치 (CMD 실행):

# 1. 파이썬 3.11/3.12 가상환경 생성 및 활성화
python -m venv venv
venv\Scripts\activate

# 2. 인터넷 연결 없이 오프라인 패키지 폴더 지정 설치
pip install --no-index --find-links=./openwebui_offline_pkgs -r requirements.txt

# 3. Open WebUI 서버 실행
open-webui serve


3. 접속: 브라우저에서 http://localhost:8080 접속하면 끝납니다!


GitHub 저장소에서 다운로드:소스 코드 (requirements.txt 포함)   

Releases 페이지에서 openwebui_offline_pkgs.zip 파일 다운로드   

폐쇄망 PC에서 설치 실행:openwebui_offline_pkgs.zip 압축 해제

Python 3.11 가상환경 생성 및 활성화:DOSpython -m venv venv

venv\Scripts\activate

오프라인 옵션으로 pip 설치:

DOS
pip install --no-index --find-links=./openwebui_offline_pkgs -r requirements.txt

서버 구동:DOS

open-webui serve
Release 업로드까지 마무리해 두시면 완전히 복구 및 설치 가능한 오프라인 배포본 준비가 완성됩니다.

set PORT=8088
open-webui serve
