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

  <div align="center">
    1.라떼판다 SBC (Single Board Computer) 보드와 함께 동봉된 12V 전력 서플라이를 통해 라떼판다에 전원을 공급한다.
    <br>
    2.라떼판다는 USB-C type을 통해 편리하게 전원 공급이 가능하다.
    <br>
    3.부팅


    <br>
    <img src="https://user-images.githubusercontent.com/92789013/194212696-ee46ec76-b849-4f47-b7b2-71e19553a77b.jpg"><br>
  
    ( 전원을 연결하고 hdmi 포트를 통해 화면을 연결해도 아무런 반응이 없다. )<br>
    ( SBC 의 측면에 위치한 power 버튼을 약 1초간 눌러주면 파란불이 점등되며 부팅이 시작된다 )
    <br>
    <br>
    <br>  

    4.별다른 조작이 없다면 기본적인 eMMC에 설치되어 있는 Windows 10이 실행된다.
    <br>
    5.Windows 10 으로 부팅이 되었다면 전원을 OFF하거나 다시시작하기를 눌러 전원을 리셋한다.
    <br>
    6.라떼판다 로고가 등장하기 전 DEL (delet) 키보드를 연타하여 라떼판타 SBC의 Bios에 진입한다.
    <br>
    <img src="https://user-images.githubusercontent.com/92789013/194212688-1f76d30a-bc33-46fd-af6f-301de59d0896.jpg">
      <br>
      <br>
      <br>

     (앞으로의 작업은 board 버전에 따라 설정할 수 있다. 때문에 있는 안건만 수정해 주면 된다.)
    7.Advanced - CPU Configuration - VT-d ==> (Disabled) { 없을 가능성이 높다 }
      <img src="https://user-images.githubusercontent.com/92789013/194211727-d5094a4a-1ae6-4b8d-8ba4-518a56aa0a2d.png">
      <br>
      <br>
      <br>
      
    8.Chipset - USB Configuration - XHCI Hand-off ==> (Enabled)
      <img src="https://user-images.githubusercontent.com/92789013/194211730-1fd302b3-243a-4786-9a17-68ac2f601d2f.png">
      <img src="https://user-images.githubusercontent.com/92789013/194211737-11edfa8c-487c-4e96-83a0-25b18b026584.png">
      <br>
      <br>
      <br>
      
    9.Chipset - Graphics Configuration - 그림과 같이 수정
      <img src="https://user-images.githubusercontent.com/92789013/194211733-798fdf6c-f396-4abb-993d-147e51a72954.png">
      <br>
      <br>
      <br>
      
    10.f4를 눌러 Bios 설정 내용 저장 후 나가기
      <br>
      <br>
      <br>
      
 </div>
      
      
## 4.2 클로버 부트로더가 설치되어 있는 USB 부팅하기
- 이전 단계를 오류 없이 수행했다면 USB 플래시 드라이브는 현재 부팅 디스크로써의 역할을 수행할 수 있다.
- 만약 이후 작업에 에러가 발생하거나 어려움이 생긴다면 이전 작업을 다시 시도해보는 것이 좋을 것이다.
- ( 예상 문제 )
  - 클로버 부트로더를 설치했는데도 EFI 폴더가 생성되지 않음
    - 해결 : 저장장치의 포맷을 GUID 파티션과 APFS로 설정하지 않아서


<div align="center">
  1.Lattepanda 보드에 부팅 USB + m.2 SSD (or USB 외장 HDD) + 키보드&마우스를 연결한다.
  (USB 외장 하드를 사용하는 경우 USB 포트가 부족해서 상당히 불편하게 된다. 키보드 & 마우스를 교차하며 사용하던가 USB 확장 허브를 사용해야한다)
  <img src="https://user-images.githubusercontent.com/92789013/194230956-5d2817bf-814d-45d4-8cde-fc1f15c93433.jpg">
  <br>
  <br>
  <br>
  
  2.Lattepanda를 부팅하고 f5를 연타하여 부팅 선택 화면으로 이동한다.<br>
  해당 화면에서 포맷할때 사용한 이름 (혹은 USB 제작회사 이름)으로된 USB 부팅 디스크를 선택한다
  <img src="https://user-images.githubusercontent.com/92789013/194211738-07952597-649d-4c8b-9ac3-765341c4aa30.png">
  <br>
  <br>
  <br>
  
  3.클로버 부트로더를 통해 OS Select를 진행한다.<br>
  Boot macOS Install from Install macOs Mojave 를 선택한다 (선택은 키보드로 진행한다)
  <img src="https://user-images.githubusercontent.com/92789013/194211739-c273ac91-1df8-4fc4-9385-3dfed4bc531f.png">
  <br>
  <br>
  <br>
  
  4.Installer 의 부팅을 기다린다 (5~10분 정도 소요된다. 혹여 지나치게 오랜시간이 소요된다면 무한사과라는 에러이니 부팅 USB 설치부터 다시 진행해야 한다)
  <img src="https://user-images.githubusercontent.com/92789013/194211741-85d5f0a4-1c42-4fbe-b7f8-74a3b37305ca.png">
  <br>
  <br>
  <br>
  
  5.이전 VMware 가상머신을 설치했을 때는 참고하여 macOS를 설치할 SSD or HDD을 포맷한다
  <img src="https://user-images.githubusercontent.com/92789013/194212653-69093097-c4b5-4473-9fe0-20da9e87a448.jpg">
  <img src="https://user-images.githubusercontent.com/92789013/194212655-7ad71ea6-890a-472d-87fc-6a8032ec4e63.jpg">
  <img src="https://user-images.githubusercontent.com/92789013/194212660-6faa4986-8ce1-42b4-8da8-67fc3ea1bcd1.jpg">
  ( 필자는 한 HDD의 파티션을 macOS 용과 Linux 용으로 나눌 예정이기 때문에 파티션을 나누어 포맷했다. )
  <br>
  <br>
  <br>
  
  6.이전 VMware 가상머신을 설치했을 때를 참고하여 macOS 설치를 진행한다.
  
  <img src="https://user-images.githubusercontent.com/92789013/194212657-60d51e7b-b4d8-4b5e-822f-67d4e5770ae2.jpg">
  <img src="https://user-images.githubusercontent.com/92789013/194212666-1d7a922e-df6e-46d9-81bc-509e9f9326ee.jpg">
  <img src="https://user-images.githubusercontent.com/92789013/194212659-b36b6d9b-072f-4bae-971d-44ca28de7348.jpg">
  <br>
  <br>
  <br>
  
  7.설치에 30~60분 가량이 소요된다. 이 때 너무 오랜시간 아무런 동작도 없다면 자동으로 전원이 절전모드로 전환되기 때문에 가끔씩 키보드나 마우스를 조작해줘야 한다.<br>
  절전모드가 되면 OS 설치가 중간에 끊겨 손상되기 때문에 OS설치를 처음부터 다시 시작해주어야 한다!!!
  <br>
  <br>
  <br>
 </div>
  
## 4.3 Mojave 설치하기
  <div align="center">
  1.클로버 부트로더에서 Boot macOS from macOS (혹은 Boot macOS from [포맷할 때 지은 HDD 이름])으로 된 부팅 디스크를 선택한다.
  <img src="https://user-images.githubusercontent.com/92789013/194211795-a192ad82-fa49-46b6-8343-7ac4bfd76392.png">
  <br>
  <br>
  <br>
  
  2. 이후로는 VMware 가상머시에서 했던 것을 참고하여 OS 설치를 진행한다.
  
  <img src="https://user-images.githubusercontent.com/92789013/194212669-82e865fc-ebc6-4877-8596-66a395b667fa.jpg">
  <img src="https://user-images.githubusercontent.com/92789013/194212671-fbfa3ab0-ba18-4335-8e2d-35c0367f0878.jpg">
  <img src="https://user-images.githubusercontent.com/92789013/194212675-e8bac38f-00b5-4d0c-8807-1df72354a4b0.jpg">
  <img src="https://user-images.githubusercontent.com/92789013/194212676-0992a14a-9ea2-4bc7-99bd-7b8cf46fc453.jpg">
  <img src="https://user-images.githubusercontent.com/92789013/194212680-c7cb59a5-c706-4e76-b213-db39c48bc66d.jpg">
  (정상적으로 부팅된다.)
  
  
  
  
