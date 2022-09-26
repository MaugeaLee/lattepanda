# lattepanda
personal lattepanda used

# 2. VMware install

## 2.1 VMware Apple Mac OS Unlocker install
- 기존 VMware에서는 MAC OS의 가상 OS 설치를 지원하지 않지만 user update를 통해 MAC OS를 설치 할 수 있다.

<div align="center">
  <img src="https://user-images.githubusercontent.com/92789013/192200879-22c6deae-92a8-4be3-9401-d3903123ec2b.png">
  <p> 이전 README_1.md 에서 업로드한 VMware Unlocker를 다운받고 해당 파일의 win-install.cmd를 관리자 권한으로 실행하며 자동 설치 됨 </a>
  <p><b> 주의!! </b> 현재 프로세스에 VMware가 실행되고 있다며 작업관리자를 통해 VMware 관련 프로세스를 모두 종료하거나 PC를 재부팅하고 진행해야 한다</p>
</div>

## 2.2 VMware MacOS Mojave install
- 가상 머신 VMware를 설치하여 macOS install USB를 만들기 위한 가상 Mojave 환경을 구축한다.

<div align="center">
  <p> 1. Create a New Virtual Machine 클릭</p>
  <img src="https://user-images.githubusercontent.com/92789013/192198998-67953494-b618-4ef7-a37c-26cdf4c3bcaa.png"><br>
  <br>
  <br>
  <br>
  
  <p> 2. Installer disc image file (iso) -> Browse 클릭으로 로컬 디스크의 ISO 파일 열기</p>
  <img src="https://user-images.githubusercontent.com/92789013/192199009-1c92afb1-70a0-45ac-a09b-15475f83f5fb.png"><br>
  <img src="https://user-images.githubusercontent.com/92789013/192199030-4c491659-37a6-4755-bba6-444400a88ebb.png">
  <br>
  <br>
  <br>
  
  <p> 3. 아까 설치해둔 macOS unlocker로 해제된 Apple Mac OS X 체크 -> Mojave 버전인 macOS 10.14 선택 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192199033-e3ea7563-a5a6-4a0f-bd1a-b7dc698f27a1.png">
  <br>
  <br>
  <br>
  
  <p> 4. 가상머신 이름과 머신이 설치될 위치 설정 (Default 면 내 문서(Documents)->Virtual Machines) </p>
  <img src="https://user-images.githubusercontent.com/92789013/192199034-4fa8fba4-34bc-4602-8856-ce278fa46f01.png">
  <br>
  <br>
  <br>
  
  <p> 5. Store virtual disk as a single file로 설정</p>
  <p> 혹시 PC 하드 용량이 부족하다면 Maximum disk size 르 20GB 정도로 수정</p>
  <img src="https://user-images.githubusercontent.com/92789013/192199035-d8b1fac2-e23c-4559-8050-0e6154dbc8f3.png"><br>
  <br>
  <br>
  <br>
  
  <p> 6. Customize Hardware... 클릭</p>
  <img src="https://user-images.githubusercontent.com/92789013/192199039-56d2554e-4c6a-4fa5-bebd-ff961d7d9336.png"><br>
  <br>
  <br>
  <br>
  
  <p> 7. 가상머신 할당 메모리를 4~8GB, processor cores수를 4로 수정</p>
  <img src="https://user-images.githubusercontent.com/92789013/192199041-e6fdeca8-e230-4397-ba65-d0917e55943b.png">
  <img src="https://user-images.githubusercontent.com/92789013/192199044-59e30f64-4e94-46ac-8894-7a9c58274635.png">
  <br>
  <br>
  <br>
   
  <p> 8. '7단계'에서 설정한 위치로 이동하여 .vmx 파일을 메모장으로 open</p>
  <img src="https://user-images.githubusercontent.com/92789013/192195784-228f24b0-531e-492b-894e-fab36cb52fed.png">
  <br>
  <br>
  <br>
  
  <p> 9. open한 .vmx 파일의 최하단부에 smc.version = "0" 입력</p>
  <img src="https://user-images.githubusercontent.com/92789013/192195786-a75d59e0-7f4f-4b66-8f6a-1c9d6a7fb96d.png">
  <br>
  <br>
  <br>
  
  <p> 10. VMware에서 작성한 가사 머신 실행</p>
  <img src="https://user-images.githubusercontent.com/92789013/192195790-29e977ec-81bc-4dfa-b3aa-9bc447b068e7.png">
  <br>
  <br>
  <br>
  
</div>
