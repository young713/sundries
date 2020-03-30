## macOS 에서 zsh로 terminal 적용하기

### iTerm2 [다운로드](https://www.iterm2.com/downloads.html)

### HomeBrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### zsh, OhMyZsh
```
brew install zsh
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### iTerm 색 테마(참고)
- https://github.com/mhartington/oceanic-next-iterm/archive/master.zip
- iTerm2 -> Preferences ... -> Profiles -> Color Presets ... -> 적용하고자 하는 테마 선택

### zsh Agnoster 테마 적용
`vi ~/.zshrc`
`ZSH_THEME="agnoster"` 로 변경

### 폰트 변경
- https://beomi.github.io/others/Ubuntu_Mono_derivative_Powerline.ttf, 더블 클릭하여 테마 설치 후 터미널 재시작.
- iTerm2 -> Preferences ... -> Profiles -> Text -> Font -> 적용하고자 하는 폰트 선택

### zsh-syntax-highlighting plugin
다운받을 원하는 경로로 이동 후
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
```
