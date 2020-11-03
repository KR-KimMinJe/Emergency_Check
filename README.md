# Ⅰ. **개요**
*   개발 기간 : 2020.04.08 ~ 2020.04.21
*   개발 목적 : 기존 방범 시스템에 행동을 인식하는 소프트웨어를 탑재하여 <br>
                   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;범죄의 사각지대를 좁히는 목표
*   융합정보논문지 10(6), 140-146
  
# Ⅱ. **동작 구성도**
![noname01](https://user-images.githubusercontent.com/73852272/98032860-f9fc9480-1e57-11eb-9db9-c09d4f574555.png)
# Ⅲ. **개발환경**
*    Languege &nbsp;&nbsp;: Python
*    FrameWork :&nbsp; Pytorch
*    Model&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:&nbsp; Yolo
*    Application &nbsp;:&nbsp; AndroidStudio
# Ⅳ. **주요기능**
*    위험요소로 판단 되는 무기류와 피해자로 판단되는 요소가 있을 시 위험상황으로 판단.
*    위험 상황의 현장 정보를 UDP 통신을 통해 전송하여 어플리케이션에서 확인.

# Ⅴ. 위험 상황 예시
&nbsp;&nbsp;&nbsp;
<img src="https://user-images.githubusercontent.com/73852272/98035812-6b3e4680-1e5c-11eb-8fde-15cfb3a62e11.jpg" width="100" hieght="100">
<img src="https://user-images.githubusercontent.com/48273803/98036748-e5bb9600-1e5d-11eb-8125-4f513905ea8c.png" width="150" hieght="150">
   <br>&nbsp;&nbsp;&nbsp;&nbsp;1.&nbsp;Danger &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.&nbsp;Not Danger <br><br>

*    피해자로 판단되는 양 손을 올린 제스처의 사람 객체 필요
*    '사람' 객체의 전체 Height 범위중 2/3위치에 '손' 객체가 두 개 이상 검출될 시<br>피해자로 구분
*    기존의 신고 방식보다 제스처를 통한 신속한 위급 상황 전파 가능

# Ⅵ. 위험 상황의 객체 감지 결과
<img src="https://user-images.githubusercontent.com/48273803/98038589-b6f2ef00-1e60-11eb-8384-3520a1c4224c.png" width="300" hieght="300">

# Ⅶ. Application
*    위험 상황 시 UI<br>
<img src="https://user-images.githubusercontent.com/48273803/98037969-bb6ad800-1e5f-11eb-8a25-6f87d2955fb9.png" width="150" hieght="150">

*    안전 취지에 맞게 신속성과 정확성이 요구
*    모델의 정확성을 고려하여 Yolo모델 선택, 
     통신의 신속성을 위하여 TCP가 아닌 UDP로 개발
