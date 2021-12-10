# Tkinter로 구현해 본 벽돌 깨기 게임

## 프로그래밍 순서

1. tkinter 라이브러리를 사용하기 위해 메인 창인 'tk 객체의 인스턴스'를 생성
2. GUI component(위젯) 생성 후 메인 창에 배치
3. 메인 루프 실행 -> GUI화면 완성
4. 생성한 창에서 버튼을 누르는 등의 사용자 조작은 Event로 다루어지고, 각종 이벤트가 발생하면 미리 등록된 처리가 실행

## tkinter 사용하기

1. tkinter 모듈 import
2. Tk 클래스 객체(root) 생성
3. 이 객체의 mainloop() method 호출
4. 빈 다이얼로그 표시

## 전반적인 실행 코드 분석
### GUI 구현  

from tkinter import*: tkinter 라이브러리 import   

root = Tk(): 상위 레벨 윈도우 창 생성  

 윈도우이름(root): 다른이름 가능  
 
root.mainloop(): 윈도우 창을 윈도우가 종료될 때까지 실행  

title("제목"): 윈도우 창의 제목  
  
geometry("너비 x 높이 + x좌표 + y좌표")  

resizeable(상하, 좌우)  

 - 윈도우 창의 창 크기 조절 가능 여부  
 - True인 경우: 윈도우 창의 크기 조절가능  
 - True(1), False(0) 사용 가능  
 
wm_attributes("-topmost", 1): 최상위 창 설정하기  

Canvas: 선, 다각형, 원 등을 그리기 위한 캔버스 생성   

Label(윈도우창, parameter1, parameter2, parameter3,..): 라벨의 속성 설정  
  
  
### Class 생성

1. 공(Ball) Class  

2. 사용자가 움직일 패들(paddle) Class  

3. 깰 블럭(Bricks) Class  

## 코드 구성 순서

1. 프레임 생성  
2. 공(Ball)class 생성  
3. 공 움직이게 만들기
4. 지속적으로 공이 반사되게 만들기
5. 패들(Paddle) class 생성
6. 패들 움직이기
7. 벽돌(Brick) class 생성  
8. 게임의 구조 형성  
  8-1. Score 구현  
  8-2. Brick 14개 * 5줄 = 95개 모두 깨면 **"성공!!"** 출력  
  8-3. 중간에 Ball을 떨어뜨리면 **"실패ㅠ"** 출력  
  8-4. 일시정지 구현 
9. 실행
