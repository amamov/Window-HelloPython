# Window Python Setting

1. MS Store에서 Python 최신 버전 다운로드

2. VSCode Extension에서 Python, Black-Formatter 설치

3. VSCode json 설정에서 아래 코드 추가

   - json 설정 : ctrl + shift + p > settings.json (Preferences: Open User Settings)

```json
{
    "[python]": {
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "ms-python.black-formatter"
    },
    "[markdown]": {
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "explorer.confirmDragAndDrop": false,
    "explorer.confirmDelete": false
}

```

4. 가상환경 사용

- 가상환경 생성 : `python -m venv 가상환경이름`

- 가상환경 활성화
    - MAC : `source 가상환경이름/Scripts/activate`
    - Window : `.\venv\Scripts\activate`
        - 권한 에러 발생 시
            1. Windows PowerShell 관리자로 실행
            2. `Set-ExecutionPolicy RemoteSigned` 입력후 Y 입력

- 가상환경 비활성화 : `deactivate`

- 설치된 패키지 리스트 txt 파일로 변환 : `pip freeze > requirements.txt`

- 변환된 txt 파일로 패키지 설치 : `pip install -r 파일이름.txt`
