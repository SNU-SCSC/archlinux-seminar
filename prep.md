# 아치리눅스 세미나

## 목표

Arch Linux를 설치하고 세팅하면서 리눅스에 대해 이해하고 경험을 쌓기

## 장소

미정 (참가 인원에 따라서)

## 시간

오후 2시부터 5시정도 (상황에 따라 더 일찍 끝날 수도 있고 눚게 끝날 수도….)

## 준비물:

- 노트북

노트북이 반드시 필요합니다. (성능은 상관이 없고, 10GB정도의 디스크 공간이 남아 있는 것을 추천합니다.) 만약에 동방에서 진행한다면 동방 컴퓨터를 사용할 수 있지만, 만약에 인원이 너무 많으면 학교의 다른 곳을 빌려야 할 것 같습니다.

저희 집에 안 쓰는 오래된 맥북 (2010년)이 하나 있긴 합니다. 저에게 톡을 해주지면 선착순으로 단 한 명에게 빌려드리도록 하겠습니다…

- 검은 화면과 하얀 글씨의 콘솔창에 겁먹지 않을 용기

## 사전 준비:

- 한 공간에서 모두가 다운로드를 하면 다운로드 속도가 느릴 수 있으니 Arch Linux ISO를 미리 다운받는 것을 추천합니다.
    - 링크: http://ftp.kaist.ac.kr/ArchLinux/iso/2018.01.01/archlinux-2018.01.01-x86_64.iso
- VirtualBox를 미리 설치해 오세요.
    - 링크: https://www.virtualbox.org/wiki/Downloads

## 미리 공부하고 싶은 분들을 위해:

### Vim 익히기

Arch Linux를 설치하면서 Vim이라는 콘솔 전용 텍스트 편집기를 사용할 것입니다. 중간중간에 설정 파일을 편집해야 하는 상황이 많이 발생하는데, 설치 과정에서는 콘솔창 밖에 없기 때문에 메모장/Sublime Text/Atom과 같은 GUI 프로그램을 쓸 수 없습니다. Vim은 콘솔에서 쓸 수 있고 제대로 익히면 매우 강력하다는 장점이 있지만, 그만큼 높은 진입장벽을 가지기로도 유명합니다. 첫 세미나에서 Vim의 사용법에 대해서 다루긴 하겠지만, 미리 익숙해지고 싶으신 분은 Vim을 설치해서 사용해보는 것을 권장합니다.

Vim은 모든 플랫폼에서 설치할 수 있습니다:
https://vim.sourceforge.io/download.php

- 윈도우 환경인 분들은 위의 링크로 가서 인스톨러를 다운받으면 됩니다.
- 이미 리눅스 환경인 분들은 해당 패키지 매니져에서 쉽게 설치할 수 있습니다.
- 맥 사용지들은 아마 Terminal에서 “vim”을 치면 이미 설치되어 있음을 확인할 수 있습니다. Terminal 말고 별개로 열 수 있는 프로그램을 원한다면 MacVim (http://macvim-dev.github.io/macvim/ )을 설치하시면 됩니다.

물론 Emacs를 쓰신다면 강요하진 않겠습니다.

### Bash 익히기

Arch Linux의 기본 Shell인 Bash를 익히는 것도 중요합니다. 세미나에서 기본적인 것들은 다루기는 하겠지만, 더욱 심도있게 다루고 싶으신 분은 다음 링크들을 참고하면 좋을 것 같습니다.

- 리눅스 / 셸 입문: http://linuxcommand.org/index.php
- Bash 스크립팅 (한글): https://wiki.kldp.org/HOWTO/html/Adv-Bash-Scr-HOWTO/index.html

Bash를 설치하는 방법은 다음과 같습니다.

- 맥/리눅스 사용자: 터미널 앱을 키면 Bash Shell이 기본적으로 설치되어 있을 것을 알 수 있습니다.

- 윈도우 사용자: 아쉽게도 Windows는 Bash가 기본으로 깔려있지 않으며, 매우 구식이고 낙후된 cmd라는 셸을 대신 사용합니다. 몰론 최근에 들어서 Powershell이라는게 새로 나왔지만... 하여튼 설치 방법은 다음과 같이 두 가지 입니다.
    - WSL (Windows Subsystem for Linux): 공식적으로 윈도우 10 상에서 우분투를 가상머신 없이 돌릴 수 있습니다! 방법은:
        1. 설정 앱에서 업데이트 및 복구 -> 개발자용 -> 개발자 모드 옵션을 체크한다.
        2. 설정 앱에서 "Windows 기능"을 검색해서 연 다음에 "Linux용 Windows 하위 시스템 (베타)" 옵션을 킨다.
        3. 재부팅 후 cmd를 관리자 권한으로 연다.
        4. ``lxrun /install``를 치고 설치가 끝나면 안내사항대로 UNIX 사용자 계정을 만들면 된다.
        5. 이젠 bash 프로그램을 cmd에서 치거나 검색해서 실행하면 될 것이다.
    - MSYS: Linux의 일부 개발자 툴들 (bash, gcc, pacman)등을 윈도우로 포팅한 것. http://www.msys2.org/ 에서 다운받아 설치하면 된다. Linux 셸과 유사한 환경을 제공하긴 하지만, 순수 Linux를 돌리는 것과는 차이가 많긴 하다.

### Arch Linux 세팅의 번거로움 없이 한 번 사용해보고 싶은 경우

Arch Linux 베이스를 기반으로 한 OS가 몇 개 있는데, 간편한 인스톨러가 제공된다.

- Manjaro: https://manjaro.github.io/
- Antergos: https://antergos.com/

## 세미나 계획

### 1회차

매뉴얼을 차근차근 따라하면서 Arch Linux의 베이스 시스템을 설치하는 것을 첫 세미나의 목표로 합니다.

자료: https://wiki.archlinux.org/index.php/installation_guide (첫 세미나에서 사용하게 될 매뉴얼)

다룰 것들:
- Linux란?
- Arch Linux 소개
    - DIY, KISS, RTFM
- Arch Linux 설치 (Installation Guide 참고)
    - 인터넷 연결 확인하기
        - bash 기본 사용
        - Wiki 읽기
    - 시간 업데이트하기
    - 디스크 파티션/포맷하기
        - 파티션이란? 파티션 테이블이란? Swap File?
    - 파일 시스템 마운트하기
    - Pacman 미러 서버 세팅하기
        - vim 과 함께하는 텍스트 편집
    - Base package 설치하기
        - pacman이란?
    - fstab 파일 만들기
        - bash와 vim 심화 사용
    - chroot하기
    - 타임존 세팅하기
        - symlink란?
    - Locale 세팅
    - Hostname 세팅
    - 네트워크 세팅
    - 패스워드 설정하기
    - 부트로더 설정하기 
    - Reboot! Profit???
- Vim / Bash 연습

### 2회차

완성된 Arch Linux 베이스 시스템을 키면 아직 콘솔창밖에 없습니다. 이젠 입맛에 맞게 나만의 Linux 시스템을 구축해 봅시다.

자료: https://wiki.archlinux.org/index.php/General_recommendations 

다를 것들:
- System Administration
    - Users and groups
    - sudo
    - systemd
- Package Management
    - pacman
    - makepkg
    - Arch User Repository (AUR)
- Intel microcode updates
- Graphical User Interface
    - Xorg display server
    - Desktop environments (GNOME, KDE, XFCE, ...)
    - Display(login) manager
- Miscellaneous (ALSA (sound), Fonts, Alternative shells, ...)

### 3회차 (아직 미정!!)

혹시 도중에 해결을 못한게 있거나 문제가 발생한 분들을 위해 3번째 세미나를 열 수도 있습니다. 2회차까지 성공한 분들은 오시지 않아도 괜찮습니다. (몰론, 와서 다른 사람들을 도와주신다면 매우 고마워용)

그리고 만약 열린다면 이 때 노트북에 직접 Partition을 만들어서 설치하고 싶으신 분들을 위해서도 시간을 가지려고 합니다. 노트북 기종에 따라서 세팅해야 하는 것들이 달라질 수 있으니...
