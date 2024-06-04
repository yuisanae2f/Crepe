# 개요
> 파이썬으로 작성한 스크립트를 컴파일한 executable 파일의 코드를 분석하고 싶어요.

이걸 읽어 보시면 당신은 5000P를 아낄 수 있습니다.

# 디컴파일링
파이썬은 굉장히 활성화가 잘 된 시장입니다.  
어느 정도로 활성화가 잘 되어 있냐면 이미 빌드된 exe마저 파이썬으로 만들어졌다면 뚫어 버릴 수 있을 수준이죠.

파이썬으로 빌드된 exe는 두 가지 단계로 디컴파일링이 가능합니다.
1. exe를 pyc 묶음으로 쪼개 버린다.
2. pyc를 py로 디컴파일링한다.
3. 즐긴다.

# exe 쪼개기
https://github.com/extremecoders-re/pyinstxtractor  

이 리포지토리는 파이썬으로 빌드된 executable 파일에서 pyc를 추출할 수 있는 라이브러리입니다.  
사용법 또한 굉장히 쉽습니다. master 브랜치에 보면 `pyinstxtractor.py`라는 이름의 파일이 있을 텐데,  

이걸 이용하면 알아서 쪼개 줍니다.

```bash
python ./pyinstxtractor.py whatever.exe
```

이제 같은 디렉토리에 딱 봐도 추출된 것처럼 보이는 디렉토리가 생길 것입니다.  
안에 .pyc 파일이 보이면 성공한 거에요.

# pyc 디컴파일하기
https://github.com/zrax/pycdc

이 리포지토리는 pyc 파일을 디컴파일하여 원본 스크립트를 최대한 복구해 줄 수 있는 프로그램입니다.  
빌드는... 직접 하셔서 pyc 파일을 py로 복사할 수 있습니다.  
어디에 복사할지도 정할 수 있다고요!

```bash
pycdc wherever.pyc > decompiled.py
```

# 즐기기
```py
import requests
from bs4 import BeautifulSoup
import tkinter as tk
import pyperclip
```
추출한 코드에서 확인한 라이브러리 포함 부분입니다.  
requests, BeautifulSoup, tkinter, pyperclip이 있군요.  
각각 뭘 하는지나 한 번 봅시다.

- requests: http 요청 날리는 거. 검색용 프로그램에서 naver.com에 검색 결과 달라고 부탁할 때 사용한 것으로 추정.  
- BeautifulSoup: html 파싱 쉽게 해 주는 거  
- tkinter: 위젯 만들려고 쓰는 거. 프로그램 창 띄워서 이쁘게 만들고 싶으셨나 보다.
- pyperclip: 클립보드 조종할 수 있는 거. `클립보드에 복사하기` 버튼 같은 거 만들고 싶으셨나 보다.

이로써 안전하다는 결론을 내고 5000P를 받았습니다.  
이것으로 당신의 돈을 아끼셨다면 입소문이라도 좀 내 주십쇼.  
감사합니다.