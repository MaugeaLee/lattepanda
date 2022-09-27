# lattepanda
personal lattepanda used

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
  <img src="https://user-images.githubusercontent.com/92789013/192327941-d9d275a0-db60-41be-9404-4a877a37f2c4.PNG">
  <br>
  <br>
  <br>
  
  <p> 3. 부팅 디스크 제작이 완료됨을 확인 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327957-0ff6fd6f-1829-4b8d-9de1-77e358d62213.PNG">
  <br>
  <br>
  <br>
</div>
  
  ## 3.4 부팅 USB에 Clover Bootloader 설치 
<div align="center">
  <p> 1. README_1.md 에서 다운받은 CloverBootloader 압축 해제 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327963-02f71d3f-7c2b-48f5-a5f1-49c70683c934.PNG">
  <br>
  (업로드 된 파일은 사진 보다 파일 하나가 더 많다)
  <img src="https://user-images.githubusercontent.com/92789013/192445184-95a72412-e77c-4c6e-9dad-31c9fe9bceb4.png">
  <br>
  <br>
  <br>
  
  <p> 2. Clover.pkg 파일 오픈 (더블 클릭하면 열리지 않을 수 있음) </p>
  <img src="https://user-images.githubusercontent.com/92789013/192327968-488dff6e-3787-4646-aef1-3a06e89cdec9.PNG">
  <img src="https://user-images.githubusercontent.com/92789013/192327970-e630b25c-21e2-45e9-9f69-a2d34955a734.PNG">
  <br>
  <br>
  <br>
  
  <p> 3. 클로버 부트로더 설치 진행</p>
  <img src="https://user-images.githubusercontent.com/92789013/192327981-a10b88cf-8842-4d12-b544-33e1fdaedfb0.PNG">
  <img src="https://user-images.githubusercontent.com/92789013/192327998-6fdaf961-d6d8-4fe2-bf40-c2174102f665.png">
  <br>
  <br>
  <br>
  
  <p> 4. 3.3.2를 통해 자동으로 Install macOS Mojave로 이름이 변경된 디스크를 선택 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192328011-e995e6b1-005d-4adc-96ef-be5ad382a4ba.PNG">
  <br>
  <br>
  <br>
  
  
  <p> 5. 사용자 설정 설치 체크 (위에서 두 체크박스만 체크하면 됨)</p>
  <img src="https://user-images.githubusercontent.com/92789013/192328007-1b46598b-9e9e-4691-832c-3b51b0127d93.png">
  <img src="https://user-images.githubusercontent.com/92789013/192328023-ce3946ee-5ac4-4c26-bb99-c709982f2f4b.PNG">
  <img src="https://user-images.githubusercontent.com/92789013/192328032-d0096f1e-1b21-4041-bd89-9cfb2c266d25.PNG">
  <br>
  <br>
  <br>
  
  <p> 6. 클로버 부트로더 설치 완료 </p>
  <img src="https://user-images.githubusercontent.com/92789013/192328063-2b0e4cd4-fc1e-4f0f-b354-37281596984a.PNG">
  <br>
  <br>
  <br>
  
  
