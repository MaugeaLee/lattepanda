# lattepanda
personal lattepanda used

<h2> 이하 내용은 어느 정도 macOS의 Finder 사용법 정도는 알고 있어야 수행하기 수월하다. 간단하게 

# 5. Booting Disk install
- 현재 라떼판다의 부팅은 오롯이 USB 플래시 디스크에서 수행하고 있다.
- USB를 제거한다면 부팅이 되지 않는다
- 따라서 USB 부팅 디스크의 부팅 수행 능력을 SSD or HDD로 옮기고 이를 수행하도록 설정해주어야 한다.
- 이미지 캡쳐에 실수하여 캡쳐 화면이 잘 안보일 수 있으나 이미지를 클릭하면 크게 확인 할 수 있다.

## 5.1 부팅 디스크의 프로그램을 Main Disk로 복사하기
<div align="center">
  1.터미널을 open 하여 현재 디스크 리스트를 확인하기

```bash
diskutil list
```

  <img src="https://user-images.githubusercontent.com/92789013/194243393-fba98518-9be3-463c-9dff-bd6191edaf4b.png">
  (이 때 확인해주어야 하는 것은 Install macOS Mojave 파일이 위치한 디스크 { 필자는 /dev/disk0 })<br>
  (그리고 main Disk가 위치한 디스크이다 { 필자는 /dev/disk1 } <- 필자는 main HDD의 용량이 500GB 인 것으로 확인 할 수 있었다.)
  <br>
  <br>
  <br>
  
  2.USB 디스크의 내용을 main Disk로 복사 이동시킨다.
  ```bash
  sudo dd if=/dev/disk0s1 of=/dev/disk1s1
  ```
  
  if(input) 디스크는 USB 디스크이며 <br>
  of(output) 디스크는 main Disk 이다 
  
  <img src="https://user-images.githubusercontent.com/92789013/194243408-9acb915d-caa7-40ab-acf9-75f9c617e094.png">
  <br>
  <br>
  <br>
  
  3.EFI 설정 내역을 하드에 복사하기 
    <a href="https://github.com/novaspirit/macpanda/releases/download/master/lattepanda.clover.zip">
      (하지만 EFI는 USB 디스크가 부팅디스크 역할을 수행하며 자동으로 휘발되었기 때문에 기존 설정되어 있는 로그 파일을 다운받아 수행할 수 있다.)<br>
       클로버 부트로더 다운 </a> <br>
    (라떼판다의 랜포트에 유선랜을 삽입하여 인터넷 통신을 통해 클로버 부트로더를 다운받는다)
  <img src="https://user-images.githubusercontent.com/92789013/194243431-305ad1d9-5f3f-42dc-a69f-dacc061befb1.png">
  <br>
  <br>
  <br>
  
  4.Clover Bootloader 폴더 안의 path-edid.rb 파일을 Downloads(다운로드) 폴더로 이동시킨다.
  <img src="https://user-images.githubusercontent.com/92789013/194243446-caa3ce27-5fb9-4131-bcce-593c66d09853.png">
  <br>
  <br>
  <br>
  
  5.터미널에서 path-edid.rb 스크립트를 수행하는 코드를 진행한다.
  
  ```bash
  cd Downloads/        # 다운로드 폴더로 이동
  ls -al               # 폴더내의 리스트 확인 (patch-edid.rb 파일 확인)
  ruby patch-edid.rb   # patch-edid.rb 파일 실행
  ```
    
  <img src="https://user-images.githubusercontent.com/92789013/194243455-de5de97f-1f8f-44e4-8a09-958ec55151b9.png">
  <br>
  <br>
  <br>
  
  6.patch-edid.rb 스크립트를 실행하면 자동으로 Display... 파일이 생성된다 해당 파일을 복사한다.
  <img src="https://user-images.githubusercontent.com/92789013/194243460-8f659ac2-0fa0-4704-a436-ff66b1bd28b9.png">
  <br>
  <br>
  <br>
  
  7.새로운 Finder를 생성하고 root 폴더로 이동<br>
  <img src="https://user-images.githubusercontent.com/92789013/194243468-0b6c8906-4b8d-442b-baae-dc05ac01c8d5.png">
  <br>
  <br>
  <br>
  
  8.root - System - Library - Display - Resources - Override 폴더에 위에서 복사한 폴더 붙여넣기
  <img src="https://user-images.githubusercontent.com/92789013/194243473-baf0501f-2e6b-493a-b082-766d81a4ef1b.png">
  <img src="https://user-images.githubusercontent.com/92789013/194243480-7858b784-17b3-43b3-9d4d-4e79c1ed3960.png">
  <img src="https://user-images.githubusercontent.com/92789013/194243484-b9885e30-7f84-4a49-9e13-3249ef78e812.png">
  <img src="https://user-images.githubusercontent.com/92789013/194243489-30165eba-02f0-4c93-a9de-082d48225427.png">
  <br>  
  (root 폴더이기 때문에 비밀번호 입력 경고창이 등장한다)
  <br>
  <img src="https://user-images.githubusercontent.com/92789013/194243493-f88fb6c7-f2ed-4b3c-b81c-6b50040b7227.png">
  
  9.재부팅을 수행한다.
  <img src="https://user-images.githubusercontent.com/92789013/194243495-b63f4f8e-fde9-4377-a9a4-b9438eccfa84.png">
  <br>
  <br>
  <br>
  
  
  
  
</div>
