# Arch Linux 세미나 #2
SCSC 장필식

---

# Bash 심화: Wildcards

---

# Bash 심화: Filters

---

# Bash 심화: Pipes

---

# Arch Linux... 뭔가 허전하다

https://wiki.archlinux.org/index.php/General_recommendations

---

# Disclaimer

여기서부터는 알아서 위키를 찾아가면서 해결해야하는 구간들이 있습니다.

---

# Users and groups

https://wiki.archlinux.org/index.php/Users_and_groups#User_management

```
useradd -m -G wheel -s /bin/bash <username>
```

---

# Sudo

https://wiki.archlinux.org/index.php/Sudo

---

# Service management

https://wiki.archlinux.org/index.php/Systemd#Basic_systemctl_usage

Arch Linux에서는 ``systemd``라는 녀석이 시스템 거의 전체를 관리한다.

실습: Arch Linux를 셸에서 재부팅해보자.

---

# Pacman

Arch Linux의 **패키지 매니져**.

---

# Arch Build System

Arch Linux의 패키지들을 빌드하는 시스템.

---

# Arch User Repository

더 많은 패키지들을 찾고 싶으면 여기를 가면 된다.
문제는 여기의 패키지들은 공식으로 등록되어 있지 않기 때문에 ``pacman -S``로 설치할 수 없다.
이를 해결하기 위해 AUR Helper라는 것을 설치해야 한다.

https://github.com/trizen/trizen

---

# 드디어... GUI

---

# Xorg (Display Server)

---

# Wayland?

- Xorg는 90년대에 나왔기 때문에 꽤나 낡았음
- 요즘의 그래픽 요구 상황에 안 맞다는 말이 많아짐
- 그래서 리눅스 전반적으로 물갈이를 시작
- ...하지만 아직 VirtualBox에서는 지원을 하지 않기 때문에 스킵.
- 아직 일부 그래픽 카드에서 지원이 불안정할 수 있다.

---

# Desktop Environment

유저에게 통합된 GUI 환경을 제공해 줌.
이것을 하나 깔면 이젠 일반 사용자들도 쉽게 쓸 수 있는 OS가 된다.

대표적인 예:
- Gnome (현재 가장 많이 씀)
- KDE (좋은 2번재 후보)
- Xfce (가벼워서 좋음)
- LXDE / LXQt (더욱 가벼움)
- Pantheon (예쁨)
- MATE
- Plasma

---

# Desktop Environment

https://wiki.archlinux.org/index.php/Desktop_environment

스크린샷을 몇 개 보고 취향에 맞는 걸 선택해 설치해보자.

덤으로 원한다면 테마도 한번 깔아보자.

---

# Window Manager

하드코어를 달리고 싶다면 추천.

창 관리 말고 거의 아무것도 제공해 주지 않는다.
즉 다른 요소들은 유저가 직접 해결해야 함.

대표적인 예:
- i3 (필자가 쓰고 있음)
- Openbox
- bspwm (Binary Tree로 스크린을 관리함)

---

# Display Manager

https://wiki.archlinux.org/index.php/Display_manager

자동으로 그래픽 환경을 시작해 주고 유저 로그인을 관리한다.

없어도 전혀 문제 없다! 셸에 로그온 한 뒤 ``startx``를 치면 된다.

---

# VirtualBox Guest Additions

VirtualBox와의 연계를 좀 더 부드럽게 해 준다.

https://wiki.archlinux.org/index.php/VirtualBox#Install_the_Guest_Additions

---

# 이외 잡다한 것들

폰트: https://wiki.archlinux.org/index.php/fonts (pacman으로 원하는 걸 설치하면 된다.)

한글 입력: https://wiki.archlinux.org/index.php/IBus

프린트: https://wiki.archlinux.org/index.php/CUPS

---

# 실제 데스크탑/노트북에 설치하고 싶다면 (Dual boot)

터질 수 있는 문제들

- 일단 컴퓨터의 펌웨어가 BIOS계통인지 UEFI계통인지 확인하고, 이것에 따라 bootloader를 설치해 주어야 한다.
    - 요즘 노트북은 거의 다 UEFI일 것이다. 그래도 끝까지 확인해보라!
- 그래픽 카드 문제
    - Intel이면 아무 문제가 생기지 않을 것이다.
    - NVIDIA라면 https://wiki.archlinux.org/index.php/NVIDIA 참고. 
    - ATI라면 https://wiki.archlinux.org/index.php/ATI 참고.
    - 노트북에서 Intel 내장 그래픽과 외장 그래픽을 같이 쓰고 싶다면 (NVIDIA Optimus처럼), Bumblebee라는 것을 깔아야한다. 필자는 성공했지만... 모두가 성공한다는 보장을 못 한다

---

# 끄으읕
