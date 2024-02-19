# tnth

1. 라즈베리 파이 키트 환경 세팅

   - 온습도 센서 관련 세팅
     ###파이썬으로 세팅할 경우, Adafruit_DHT 라이브러리 필요 >> 라이브러리부터 설치해줌
     (라이브러리 설치 과정)
     1) 깃허브에서 Adafruit_python_DHT 검색해서 clone해옴
     2) 우선 다음과 같은 과정을 수행한다

        sudo apt-get update 
        sudo apt-get upgrade ...(패키지 목록 최신화 및 업그레이드)

        sudo apt-get install python3-dev python3-pip
        (파이썬3를 통해 C/C++등의 확장 모듈 설치 시 필요한 개발 라이브러리 및 헤더 설치 & 파이썬3용 패키지관리자(pip)설치)

        sudo python3 -m pip install --upgrade pip setuptools wheel
        (파이썬 패키지 설치용 툴(pip, setuptools, wheel) 모두 최신화)
        
        sudo pip install Adafruit_DHT
        (pip 패키지 매니저로 Adafruit_DHT 라이브러리 설치 >> 여기서 에러뜨긴 했었음)
        만약 이 방법으로 라이브러리 설치가 안된다면 아래 과정을 진행하자
           터미널에서 현재 디렉터리를 Adafruit_Python_DHT로 변경
           sudo python3 setup.py install
           (또는, 비글본 블랙과 라베리파이를 지정하라고 할 경우, install 뒤에 --force-pi 옵션을 추가로 입력해준다)
        

    3) 이 후엔 온습도 측정하는 코드 찾아서 실행시키기만 하면 된다.

      테스트 코드를 만들어볼 때, 터미널에서 vim 편집기를 통해서 만들었다 (sudo vim testss.py)
      편집기를 동작시켰을 때 원하는대로 동작하지 않는것을 방지할 수 있지않을까 싶어서 편집기 업데이트까지 같이 해주었다 (sudo apt-get upgrade vim)

   * 파일에 권한이 없어서 실행이 안될 경우
  
   chmod 777 파일이름  >> 뭐가 뭔지 모르니 그냥 user, group, other user에 모든 권한 냅다 떄려박아버린다.

   ####C언어로 세팅하게되는 경우까지 가는건 진짜 최후의 보루이니 여까지 가는일이 없도록 기도해야함 ㅎㅎ
   ###C언어로 작성할 경우, wiringPi.h라는 헤더파일을 포함시켜야 함 >> 마찬가지로 깃허브에서 라이브러리 찾아서 설치

   


