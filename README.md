# lattepanda
personal lattepanda used

# 0. 준비물
## 0.1 하드웨어
- Lattepanda alpha (delta는 각종 오류 가능성 있음)
- M2 NVMe SSD (SATA 안됨) 혹은 USB형 외장 SSD or HDD
- 플래쉬 USB 디스크 (최소 30GB 이상)
- 유선 키보드
- 유선 마우스

## 0.2 소프트웨어
- VMware (가상 윈도우 머신)
- VMware MacOS 10.14 Mojave IOS
- Clover Bootloader

# 1. Lattepanda MacOS Mojave Install
- 라떼 판다의 사양은 17년도 intel Macbook 과 사양이 매우 흡사하여 하드웨어의 별다른 부담 없이 mac os를 인스톨하여 사용할 수 있다. <br>
|성능|Lattepanda alpha|Macbbok(17")|
|---|:---:|:---:|
|CPU| i7 core M3-7Y30 | i7 core M3-7Y32 |
|GPU| X | intel HD Graphics 615 900MHz GPU |
|RAM| LPDDR3 RAM 8GB | 8/16GB LPDDR3 SDRAM |
|저장장치| eMMC 5.0 64GB | 256/512 GB SSD |
| offical OS| Windows 10 or Linux | macOS 10.13 (High Sierra / Mojave update)|
- 그 중에서 17년 intel Macbook과 가장 호환성이 좋은 Mojave 버전을 별다른 OS Config 없이 아주 쉽게 install 할 수 있다.
- 하지만 offical OS 가 아니기 때문에 하드웨어의 기술적 손상이 생길 수 있다.
- Wi-Fi 랜카드 Bluetoos의 사용이 불가능해진다. (USB 랜카드와 Bluetoos 동글로 해결한다.)

## 1.1 Hackintosh (해킨토시)
- macOS를 탑재한 Apple사 PC를 Macintosh(매킨토시)라고 통칭한다. 
- 이때 타사 PC에 macOS를 install하여 Unoffical OS 구성을 빌드하는 경우 이를 Macintosh에 빗대어 Hackintosh 혹은 Custom Mac 이라고 부른다.
- Hackintosh를 빌드하기 위해선 Windows install과 마찬가지로 부팅 USB가 필요하며 이때 macOS의 app 파일이 필요하다.
- macOS의 install.app 파일을 다운받기 위해선 mac 환경이 필요하며 이를 위해 VMware가상 머신을 통해 파일을 다운받는다.

## 1.2 Clover Bootloader
- Apple 사의 전용 메인보드와 부트로더를 사용할 수 없기 때문에 Custom Bootloader를 사용하게 된다.
- GUID 파티션맵의 APFS으로 포맷된 저장장치를 EFL과 USB-BOOT 파티션으로 나누어 Lattepanda 보드으 메모리가 아닌 플래시 USB 자체를 부트로더 역할을 수행가능하도록 설정하는 프로그램이다.
