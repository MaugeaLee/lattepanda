# lattepanda
personal lattepanda used

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
  
  
  
</div>
