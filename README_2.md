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

## 2.2 Virtual Machine Start
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
  
  <p> 10. VMware에서 작성한 가상 머신 실행</p>
  <img src="https://user-images.githubusercontent.com/92789013/192195790-29e977ec-81bc-4dfa-b3aa-9bc447b068e7.png">
  <br>
  <br>
  <br>
  
</div>

## 2.3 VMware MacOS Mojave Install

- MacOS Catalina 버전으로 스크린샷이 찍혔지만 <b>반드시</b> macOS Mojave 버전으로 진행해야 한다.
- Catalina 버전은 진행 결과 해킨토시에 실패 했음을 알림

<div align="center">
  <p> 1. 진행 언어 설정 (한국어) </p>
  <img src="https://user-images.githubusercontent.com/92789013/192195793-54f8619d-c5fb-4565-8449-a51f0458d0c5.png">
  <br>
  <br>
  <br>
  
  <p> 2. 디스크 포맷 진행 </p>
  <p> VMware Virtual SATA Hard Drive Media를 포맷</p>
  <p> 이름은 반드시 영문으로 작성한다</p>
  <p> 포맷은 APFS, 설계는 GUID 파티션 맵으로 설정한다</p>
  <img src="https://user-images.githubusercontent.com/92789013/192206929-603d6800-516b-435e-aa58-fe61fef46e6e.png">
  <img src="https://user-images.githubusercontent.com/92789013/192206937-09b3d360-a137-486c-8b94-d1deeb2bb995.png">
  <img src="https://user-images.githubusercontent.com/92789013/192206939-05a3c00a-95e2-4f0e-b0aa-6fede55a7f5b.png">
  <br>
  <br>
  <br>
  
  
  <p> 3. macOS 설치 시작</p>
  <img src="https://user-images.githubusercontent.com/92789013/192206941-726fadbd-1720-4ffc-83f5-aa80e6108469.png">
  <br>
  <p> 3.1 설치 파일이 손상되었다는 오류가 발생한다면 아래와 같이 조치한다.</p>
  
- 1. PC의 인터넷을 차단한다 (랜뽑 / Wi-Fi Off)
- 2. 유틸리티 -> 터미널
- 3. date 0930093017
- 4. macOS 설치 재시도
- 5. 긴 시간 어떠한 응답도 없다면 다시 인터넷을 연결하고 오류가 다시 발생한다며 1부터 재시도
OS Installer에서 해킨토시 차단을 위해 ISO를 손상된 파일로 인식하지만 해당 차단 알고리즘을 시행하지 않는 17년도 날짜로 변경하면 ISO를 손상되지 않은 파일로 인지한다.
  
  <br>
  <br>
  <br>
  
  <p> 4. 설치 진행 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192195805-2b8d5f04-ebb5-47c8-9450-b7b7dc9d77ac.png">
  <br>
  <br>
  <br>
  
  <p> 5. 설치 디스크 선택 (15~30분 소요)</p>
  <img src="https://user-images.githubusercontent.com/92789013/192195807-9e3a30c1-4b48-4fe5-a942-e3418c424a15.png">
  <img src="https://user-images.githubusercontent.com/92789013/192195809-990f7b7f-dc7e-4874-b131-b353c3ac9900.png">
  <br>
  <br>
  <br>
  
  <p> 6. 국가 선택 (대한민국) </p>
  <img src="https://user-images.githubusercontent.com/92789013/192195812-6e846ed2-8aab-452a-917f-14ac28cb4c42.png">
  <br>
  <br>
  <br>
  
  <p> 7. 인터네 설정 DHCP 서버가 자동으로 검색되지 않으면 그냥 Pass</p>
  <img src="https://user-images.githubusercontent.com/92789013/192195814-d1555e49-d2cd-40bc-bb49-6ee83a3a172a.png">
  <img src="https://user-images.githubusercontent.com/92789013/192195816-f5908011-38c4-48ed-938f-0a0fd4d28fcc.png">
  <br>
  <br>
  <br>
      
  <p> 8. 정보 전송을 하지 않음</p>
  <img src="https://user-images.githubusercontent.com/92789013/192195820-a3ead9e8-ece8-4395-a654-b2270896cd01.png">
  <br>
  <br>
  <br>
  
  <b> 이 뒤로는 계정 생성 이외에 모두 다음을 누른다.</b>
  </div>

  # 3. 부팅 USB 만들기
  - USB 플래시 드라이브를 통해 부트로더를 설치한 macOS 부팅 드라이브를 작성한다.

  ## 3.1 Install macOS Mojave.app 다운 
  
<div align="center">
  <p> 1. 사파리 오픈 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327793-0640c057-f559-4d7e-9678-7bb8d71b9f64.PNG">
  <br>
  <br>
  <br>
  
  <p> 2. Apple 정식 macOS Mojave 클릭 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327799-f977d4af-22eb-4964-a438-a1dee5de5d96.PNG">
  <br>
  <br>
  <br>
  
  <p> 3. 페이지 하단의 macOS Mojave 링크 클릭 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327807-54c43011-f92d-42a1-9cfb-684428647a7b.PNG">
  <br>
  <br>
  <br>
  
  <p> 4. 자동으로 연결된 AppStore 에서 Mojave 어플리케이션 다운</p>
  <img src="https://user-images.githubusercontent.com/92789013/192327815-b7ce9cc9-5824-41e0-a119-1a9243caca32.PNG">
  <br>
  <br>
  <br>
  
  <p> 5. Finder(파일 탐색기)의 Application(응용 프로그램) 폴더의 Install macOS Mojave.app 파일 다운 여부 확인</p>
  <img src="https://user-images.githubusercontent.com/92789013/192327831-d6f364a3-d465-4738-9cfd-5b3698697013.PNG">
  <br>
  <br>
  <br>
 </div>
   
  ## 3.2 USB 플래시 디스크 포맷 
<div align="center">
  <p> 1. PC에 USB 삽입 후 USB 인식으로 가상머신으로 설정 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327905-6436867f-fb21-46df-9b27-e8eb22eebd5c.PNG">
  <img src="https://user-images.githubusercontent.com/92789013/192327919-db7f1cb1-c54d-4bea-a083-95875d767e34.PNG">
  <br>
  <br>
  <br>
  
  <p> 2. 우측 상단의 돋보기 클릭 후, 디스크 유틸리티 오픈 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327928-3bd1b5f8-47f5-45fe-9ce4-7e79108bc05f.PNG">
  <br>
  <br>
  <br>
  
  <p> 3. 디스크 유틸리티의 보기 탭 클릭 (스샷이 유실되어 다른 버전에서 진행한 스샷을 첨부) </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327935-4dc6ba15-dc99-4a63-9aaa-dd4a12c8e0de.PNG">
  <img src="https://user-images.githubusercontent.com/92789013/192327834-6d50e4bc-585f-4d4b-8c7a-5a973e53d6b9.png">
  <br>
  <br>
  <br>
  
  <p> 4. 인식된 USB 외장 물리적 저장공간을 포맷</p>
  <p> 포맷 : APFS / 설계 : GUID 파티션 맵 / 이름 : 영문 이름 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327837-6e5a0f15-288b-4eaa-b7e2-b22e21ac59b5.png">
  <img src="https://user-images.githubusercontent.com/92789013/192327842-a52db897-228d-4e0c-b0ec-9072e823af35.png">
  <br>
  <br>
  <br>
  
</div>
  
  ## 3.3 부팅 USB 제작
  
<div align="center">
  <p> 1. 3.2.2와 같이 돋보기를 클릭하여 terminal 입력 후 터미널 오픈 </p>
  <br>
  <br>
  <br>
  
  <p> 2. 터미널에 Install macOS mojave.app 을 사용한 부팅 디스크 제작 코드 작성 </p>
  
  <pre>
    <code>
      sudo /Applications/Install\ macOS\ mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/disk
    </code>
  </pre>
  
  <img src="https://user-images.githubusercontent.com/92789013/192327938-0abc1bf1-4bd4-4230-8708-0d6e1e232775.PNG">
  <br>
  <br>
  <br>
  
  
  
    
  
  
