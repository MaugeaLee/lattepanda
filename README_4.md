# lattepanda
personal lattepanda used

# 4. Lattepanda Bios Setting
- macOS가 정상적으로 작동할 수 있도록 간단한 바이오스 셋팅을 진행해줘야 한다.
- Bios 설정을 위해 라떼판다 USB포트에 키보드를 연결할 수 있어야 한다.

## 4.1 Lattepanda Booting 
- 라떼판다의 bios는 일반 PC의 메인보드와 마찬가지로 키보드로 조작한다.
- (간단한 사용법)
  - 가로 화살표 : 상단 탭 변경
  - 세로 화살표 : 현재 탭의 메뉴 변경
  - 엔터 : 선택
  - esc : 현재 선택한 configuration에서 나가기
  - f4 : 저장후 나가기 
<br>

  <div align="center">
    1. 라떼판다 SBC (Single Board Computer) 보드와 함께 동봉된 12V 전력 서플라이를 통해 라떼판다에 전원을 공급한다.
    <br>
    2. 라떼판다는 USB-C type을 통해 편리하게 전원 공급이 가능하다.
    <br>
    3. 부팅
    <br>
    <img src="https://user-images.githubusercontent.com/92789013/194212696-ee46ec76-b849-4f47-b7b2-71e19553a77b.jpg">
    ( 전원을 연결하고 hdmi 포트를 통해 화면을 연결해도 아무런 반응이 없다. )<br>
    ( SBC 의 측면에 위치한 power 버튼을 약 1초간 눌러주면 파란불이 점등되며 부팅이 시작된다 )
    <br>
    <br>
    <br>  

    4. 별다른 조작이 없다면 기본적인 eMMC에 설치되어 있는 Windows 10이 실행된다.
    <br>
    5. Windows 10 으로 부팅이 되었다면 전원을 OFF하거나 다시시작하기를 눌러 전원을 리셋한다.
    <br>
    6. 라떼판다 로고가 등장하기 전 DEL (delet) 키보드를 연타하여 라떼판타 SBC의 Bios에 진입한다.
    <br>
    <img src="https://user-images.githubusercontent.com/92789013/194212688-1f76d30a-bc33-46fd-af6f-301de59d0896.jpg">
      <br>
      <br>
      <br>

     (앞으로의 작업은 board 버전에 따라 설정할 수 있다. 때문에 있는 안건만 수정해 주면 된다.)
    7. Advanced - CPU Configuration - VT-d ==> (Disabled) { 없을 가능성이 높다 }
      <img src="https://user-images.githubusercontent.com/92789013/194211727-d5094a4a-1ae6-4b8d-8ba4-518a56aa0a2d.png">
      <br>
      <br>
      <br>
      
    8. Chipset - USB Configuration - XHCI Hand-off ==> (Enabled)
      <img src="https://user-images.githubusercontent.com/92789013/194211730-1fd302b3-243a-4786-9a17-68ac2f601d2f.png">
      <img src="https://user-images.githubusercontent.com/92789013/194211737-11edfa8c-487c-4e96-83a0-25b18b026584.png">
      <br>
      <br>
      <br>
      
    9. Chipset - Graphics Configuration - 그림과 같이 수정
      <img src="https://user-images.githubusercontent.com/92789013/194211733-798fdf6c-f396-4abb-993d-147e51a72954.png">
      <br>
      <br>
      <br>
      
    10. f4를 눌러 Bios 설정 내용 저장 후 나가기
      <br>
      <br>
      <br>
      
 </div>
      
      
## 4.2 클로버 부트로더가 설치되어 있는 USB 부팅하기
- 이전 단계를 오류 없이 수행했다면 USB 플래시 드라이브는 현재 부팅 디스크로써의 역할을 수행할 수 있다.
- 만약 이후 작업에 에러가 발생하거나 어려움이 생긴다면 이전 작업을 다시 시도해보는 것이 좋을 것이다.
- (예상 문제 )
  
  
