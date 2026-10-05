0. 파이썬 설치 (폐쇄망 PC에 파이썬 3.11/3.12가 없는 경우)
   - Release에서 python-3.11.x-amd64.exe 다운로드 후 설치
   - ⚠️ 설치 시 반드시 맨 아래 [Add python.exe to PATH] 체크박스 선택
   - 

1. 파일 다운로드 및 옮기기 (USB / 망연계 시스템 활용):
    GitHub 저장소에서 코드 내려받기 (requirements.txt 포함)
    Release 페이지에서 openwebui_offline_pkgs.zip 다운로드하여 압축 해제

2. 폐쇄망 PC에서 설치 (CMD 실행):

### 1. 파이썬 3.11/3.12 가상환경 생성 및 활성화

> **참고**: PC에 여러 파이썬 버전이 설치된 경우, 버전을 명확히 지정하여 가상환경을 생성합니다.

# 방법 A (권장): 윈도우 파이썬 런처(py)로 특정 버전 지정 생성
py -3.11 -m venv venv

# (만약 3.12 버전을 설치해둔 경우)
py -3.12 -m venv venv

# 방법 B: 설치된 특정 파이썬 전체 경로를 직접 지정하는 경우
"C:\Program Files\Python311\python.exe" -m venv venv

---

# 가상환경 활성화 (CMD 기준)
venv\Scripts\activate

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
