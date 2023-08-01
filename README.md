# CardGame
짝 맞추기 Card Game입니다.

## 프로젝트 설명
javascript를 처음 배우고 짠 Card Game입니다.
DB 설계, spring, react에 대해 배우기 전
스스로 MVC 패턴, 의존성 주입, React Componet 개념을 생각해내고, 도입했습니다.
또한 렌더링 최적화가 무엇인지 모른 채 렌더링을 최적화하는 방안을 생각해 코드를 짰습니다.

1. DB 설계  
   코딩에 들어가기 전 미리 필요한 영역을 설계했습니다. 전체를 board로 보고, 하위 영역을 button, table, console, buffer로 나눴습니다.
   필요한 속성을 Class로 만들었습니다. Board, Card, Deck 객체를 만들고, getter와 setter를 이용해 값을 줬습니다. 훗날 이것이 DTO 개념과 유사함을 알았습니다.

2. 의존성 주입  
   Print 객체를 만들어 1에서 만든 객체를 변수로 넘겨주었습니다. 객체 멤버변수 값이 바뀌어도 Print함수를 통해 알맞은 html을 생성할 수 있었습니다. 훗날 이것이 의존성 주입임을 알았습니다.

3. MVC 패턴  
   미리 만들어 놓은 객체에 상황에 맞게 setter로 값을 바꿨습니다. 그리고 바뀐 값 또는 객체를 handler나 짝이 맞았는지 계산하는 checkNum 함수, print 함수에 보냈습니다.
   변수를 담는 객체와, 계산과 로직을 처리하는 객체, print를 해주는 객체를 따로 나누는 것이 MVC 패턴임을 추후 스프링에 대해 배우며 알았습니다.

4. React Component  
   event handler가 event가 생길 때마다 event 발생한 곳을 for문을 돌아 찾는 방법이 비효율적이라 생각했습니다. 그래서 이벤트가 발생하는 곳에 상위 태그를 만들어 주고, 상위 태그에서 이벤트 발생시 target만 추적하게 코드를 짰습니다.
   훗날 React를 공부하며 이것이 Component 개념임을 알았습니다. 또한 if 문으로 하위 태그 별로 로직을 달리 짰습니다. 이것이 useEffect와 비슷함을 추후에 알았습니다.

5. 렌더링 최적화  
   Shuffle 기능 구현 때 이미 렌더링한 img 태그들을 다시 렌더링하면 비효율적이라 판단했습니다. 그래서 console.dir로 javascript 문법을 찾고, outerHTNL이 있음을 알았습니다.
   outerHTML로 이미 업로드된 이미지를 다시 업로드하지 않고, 태그 간 순서만 바꿀 수 있었습니다. 이것이 렌더링을 최적화하는 방법인지 추후에 알았습니다.

### 사용한 기술들

1. javascript  
  javascript에 대한 문법을 모른 채 console.log와 console.dir을 찍어가며 문법을 익혔습니다.

2. html  
   html 안에서 javascript를 실행시켰습니다. 
   
3. css  
  기본적인 색을 넣는 용도로만 활용했습니다.  

## 프로젝트 설치 및 실행 방법

1. git clone으로 프로젝트를 다운 받습니다.

```
  git clone https://github.com/dancingKim/CardGame.git
```

2. Visual Studio Code로 프로젝트를 엽니다.

3. index.html을 엽니다.

4. 우클릭 후 Open with Live Server를 클릭합니다.

## 프로젝트 사용 방법

## 팀원 및 참고 자료
### 팀 소개
김정호

### 참고 자료
없음.

## 라이센스
“This project is licensed under the terms of the MIT license.”
