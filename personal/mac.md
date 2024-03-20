## [Done] 软件同步

> brew cask 有可能存在安全问题，建议在 官网 or AppStore(优先) 下载 这些常用的 gui 软件

1. Chrome

   1. 网上下载

2. 搜狗输入法

   1. ```Bash
      brew install --cask sogouinput
      ```

3. 微信

   1. 字体调整
   2. 默认浏览器打开
   3. 快捷键设置
   4. 从 App Store 下载

4. 飞书

   1. 更新版本

5. VSCode

   1. Copilot
   2. 登录 CodeEnter Github Sync 配置
   3. Install shell path

6. PasteNow

   1. 系统启用
   2. 粘贴 快捷键 CS V
   3. ![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=ZTI4YmU1Mzk4YTY4NWYwNmRkMGI1OWQ5NzAzNTY4MzVfUVR4cnl0UEFYMmdIMGJNb2FXN2g5RmswdDZ3d0dIYWpfVG9rZW46VUZRbmJGVlR3b2lLWXN4b2xFYWN4cDRXbmhiXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=MDA3MjczOGMyODY1YTRiZjBhM2Q5OWI4MDVjZDk5MTFfSTZHQmxZcFpFNGd4TnlVbVJzakpYSWdJSHlnRm5nTFZfVG9rZW46TzRHNGIxeU12bzl6Zjh4RVdFSGNUc3hvbjJkXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)
   4. 

7. AltTab

侧边栏

1. Snipaste
   1. 侧边栏文档
2. Flux

- 10 点起床
- 基于 location 设置

1. 设置黑色壁纸

1. BetterAndBetter
   1. 侧边栏文档

1. Fork

1. Raycast
2. Postman
   1. VSCode 插件

配置好系统工具之后再进行配置：

1. Kitty

1. iBar，在外：
   1. 输入法
   2. 电联
   3. 微信
   4. 飞书
   5. Flux

可选：

1. WPS
2. Typora  
   1. 主题[optional]
3. Shottr
4. QQ
5. XCode
6. Charles
7. JetBrains Toolbox
8. 网易云音乐
   1. 关闭全局快捷键
   2. 启用 VIP 音质

1. Telegram

1. **Warp**
2. Manico

![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=YjRkM2U2ZmVjOGFmNTRjMWQzNTZhNGUwZGFmZDk2YmZfdWE3cmNSWmhmZVVvUFBwVVBJSUZZNXA2cHlKNkRXOUZfVG9rZW46RlpYY2JxbTVtb290Ykt4N2RBdWNkcm5tbnBoXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NWZhMTFlZjJkZjgxMzk1NDdmN2U4ZTc5ZjZiMDE5ZDBfVnpGQnlockhzZFY4RVZpYWdUMU14WUxER29XN1QyQW9fVG9rZW46UmpyYmJhTjZab2dxTll4aXJVWmN3Z2dNblJjXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=ZmZjMWY0OTkzZmFlNzBlNjdmMjI5ZmI3ZGZjNzAxODFfaXVHZWN0cWdBcElCT2JzMnJoakZSWm80c1dpMG9CclBfVG9rZW46RG4yaGJMM04yb2Rta054SHRYeGNZNTRsbjVjXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)

1. 自动切换输入法? / **Input Source Pro**
   1. 提示触发规则禁用掉
   2. 登录启动
   3. ![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NTgyMWFkNmZlNGZiN2I5ZGNkNzljOTJjY2U4MDQxOWRfdFFPbkFWUUNPMmFjMFFjemlmeFNRN2NieVZuZlR6TUlfVG9rZW46TFYwdWJVZ1VDb0xMbnZ4b2dBcWNZckp1bjhmXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)
2. Keycastr
   1.  brew install --cask keycastr

## [Done] 程序同步

### [Done] 开发工具

1. [Done] Node.js

   1. [Done] FNM

   2. ```Bash
      brew install fnm
      
      # add the following to zshrc
      eval "$(fnm env --use-on-cd)"
      
      fnm install --lts
      
      fnm use {lts}
      
      fnm default {lts}
      ```

   3. yarn/pnpm

   4. @antfu/ni

   5. serve

   6. kill-port

   7. fkill

   8. eslint

   9. prettier

   10. typescript

   11. gacp

```Bash
npm install -g pnpm
pnpm install pnpm -g
pnpm install -g yarn @antfu/ni serve kill-port fkill-cli eslint prettier typescript gacp esno

; ~/.nirc
; fallback when no lock found
defaultAgent=pnpm # default "prompt"
; for global installs
globalAgent=pnpm
```

1. [Done] Git

```Bash
git config --global user.name "SimonAKing"
git config --global user.email "simon@tomotoes.com"

git config --global user.name "马进"
git config --global user.email "majin.dev@bytedance.com"

git config --global --add push.default current
git config --global --add push.autoSetupRemote true
# 追加

[color]
  ui = auto
  diff = auto
  status = auto
  branch = auto
  interactive = true
[core]
  excludesfile = ~/.gitignore
  editor = vim
[icdiff]
  options = --highlight --line-numbers
[alias]
  fpush = push --force-with-lease
  info = log --oneline --decorate --all --graph
  amend = commit --amend --reuse-message=HEAD
  changelog = log origin..HEAD --format='* %s%n%w(,4,4)%+b'
  workon = "!f(){ git fetch && git checkout -b \"$1\" $(git symbolic-ref refs/remotes/origin/HEAD | sed \"s@^refs/remotes/@@\"); };f"
  refresh = "!f(){ git fetch && git stash && git rebase $(git symbolic-ref refs/remotes/origin/HEAD | sed \"s@^refs/remotes/@@\") && git stash pop; };f"
[url "git@github.com:"]
  insteadOf = https://github.com/
# Folder view configuration files
.DS_Store
Desktop.ini

# Thumbnail cache files
._*
Thumbs.db

# Files that might appear on external disks
.Spotlight-V100
.Trashes

# Compiled Python files
*.pyc

# Compiled C++ files
*.out

# Application specific files
venv
node_modules
.sass-cache
```

1. [Done] gh(Github shell)

```Bash
mkdir ~/.ssh
# file name 用 github，passphrase 随意
ssh-keygen -t ed25519 -C "github"
# 编辑配置，内容如下
touch ~/.ssh/config

Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/github
# 添加到系统 keychain
sudo ssh-add --apple-use-keychain ~/.ssh/github
# 添加 public key 到 github

brew install gh

gh auth login
gh auth refresh -h github.com -s admin:public_key
gh ssh-key add ~/.ssh/github.pub -t github
```

1. [Done] vim/**nvim**/**lazyvim**

```Bash
# 「optional」
brew install vim

brew install neovim

# lazyvim:https://www.lazyvim.org/installation

git clone https://github.com/LazyVim/starter ~/.config/nvim
rm -rf ~/.config/nvim/.git

nvim
```

- [Done] vimrc

```Bash
" ==================================================
" 配置篇
" ==================================================

" 语法高亮
syntax on

" 关闭自动折行
set nowrap

" 横向滚动一次 40 个字符,
set sidescroll=40
" 垂直滚动时，光标距离顶部/底部的位置（单位：行）
set scrolloff=5
" 水平滚动时，光标距离行首或行尾的位置（单位：字符）。该配置在不折行时比较有用
set sidescrolloff=15

" 搜索时，高亮显示匹配结果
" set hlsearch
" 输入搜索模式时，每输入一个字符，就自动跳到第一个匹配的结果
set incsearch
" 搜索时忽略大小写
set ignorecase
" 如果同时打开了ignorecase，那么对于只有一个大写字母的搜索词，将大小写敏感
" 其他情况都是大小写不敏感。比如，搜索Test时，将不匹配test；搜索test时，将匹配Test
set smartcase

" 不与 Vi 兼容（采用 Vim 自己的操作命令）
set nocompatible

" 在状态栏显示光标的当前位置（位于哪一行哪一列）
set ruler
" 显示光标所在的当前行的行号，其他行都为相对于该行的相对行号
set relativenumber
" 显示行号
set number
" 光标所在的当前行高亮
set cursorline
" 是否显示状态栏。0 表示不显示，1 表示只在多窗口时显示，2 表示显示
set laststatus=2
" 命令模式下，在底部显示，当前键入的指令
set showcmd
" 光标遇到圆括号、方括号、大括号时，自动高亮对应的另一个圆括号、方括号和大括号
set showmatch
" 在底部显示，当前处于命令模式还是插入模式
set showmode

" Vim 需要记住多少次历史操作
set history=1000
" 与系统共用剪切板
set clipboard+=unnamed

" 打开文件监视。如果在编辑过程中文件发生外部改变（比如被别的编辑器编辑了），就会发出提示
set autoread

" 正常使用鼠标
set mouse=

" Tab 转为多少个空格
set softtabstop=2
" 按下回车键后，下一行的缩进会自动跟上一行的缩进保持一致
set autoindent

" 出错时，不要发出响声
set noerrorbells

" 允许退格键在以下场景下正常执行
set backspace=indent,eol,start

" ==================================================
" 映射篇
" ==================================================

" 禁用 esc 键
" inoremap <esc> <nop>

" 禁用方向键
"noremap <up> <nop>
"noremap <down> <nop>
"noremap <left> <nop>
"noremap <right> <nop>

" j k 映射成 gj gk
nnoremap k gk
nnoremap j gj
```

1. [Done] Xcode

   1. ```Bash
      xcode-select --install
      ```

2. [Done] Rust

   1. cargo

```Bash
brew install rustup

rustup-init

source "$HOME/.cargo/env"

rustc -V
```

1. **[Skip] pyenv**

   1. ```Bash
      # 方案1 使用 pyenv，ARM 芯片不兼容
      brew install pyenv
      
      echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
      echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
      echo 'eval "$(pyenv init -)"' >> ~/.zshrc
      
      pyenv install 2.7.9
      pyenv install 3.10
      
      # 方案2 直接安装
      bi python@3.11
      ```

   2. Python2

   3. Python3

2. Bun

```Bash
brew tap oven-sh/bun # for macOS and Linux
brew install bun
```

1. [Done] AndroidSDK

```Bash
brew install android-platform-tools

adb
```

1. **[Done] gvm**
   1. Go

```Bash
# 方案1 使用 gvm，ARM 芯片不兼容

bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)

source ~/.gvm/scripts/gvm

gvm listall
gvm install go1.20.4
gvm use go1.20.4 --default

# 方案2 直接安装 golang
bi go

go version
```

1. [Done] Java

```Bash
curl -s "https://get.sdkman.io" | bash
source "~/.sdkman/bin/sdkman-init.sh"
 
sdk install java
```

1. [Done] ffmpeg

```Shell
brew install ffmpeg

# optional
# bi icu4c
```

1. [Done] docker
   1. lazyDocker

```Bash
brew install lazydocker

https://docs.docker.com/desktop/install/mac-install/
```

1. [Done] lua

```Bash
brew install lua
```

1. [Done] nginx

```Bash
brew install nginx
```

1. [Done] redis

```Bash
brew install redis

# redis-cli
```

1. mongodb
2. MySQL
3. [Done] mycli

```Bash
brew update && brew install mycli  # Only on macOS
```

1. [Done] sqlite

```Bash
brew install sqlite
```

### [Done] 系统工具

1. [Done] Homebrew

   1. ```Bash
      /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
      ```

2. [Done] ZSH

   1. [Done] oh-my-zsh

   2. ```Bash
      sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
      ```

   3. [Done] zsh 插件

   4. ```Bash
      zsh-autosuggestions
      # git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
      fast-syntax-highlighting
      # git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git   ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting
      command-not-found (builtin)
      you-should-use
      # git clone https://github.com/MichaelAquilina/zsh-you-should-use.git $ZSH_CUSTOM/plugins/you-should-use
      git-open
      # git clone https://github.com/paulirish/git-open.git $ZSH_CUSTOM/plugins/git-open
      vi-mode（builtin）
      zsh-vi-mode
      # git clone https://github.com/jeffreytse/zsh-vi-mode  $ZSH/custom/plugins/zsh-vi-mode
      autoupdate
      # git clone https://github.com/TamCore/autoupdate-oh-my-zsh-plugins $ZSH_CUSTOM/plugins/autoupdate
      sudo (builtin)
      zsh-completions
      # git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions
      # autoload -U compinit && compinit
      
      history-substring-search
      # git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
      fzf-tab
      # git clone https://github.com/Aloxaf/fzf-tab ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/fzf-tab
      ```

   5. [Done] zsh 配置

   6. ```Bash
      DEFAULT_USER=majin
      export USER=majin
      
      export ZSH="$HOME/.oh-my-zsh"
      export LANGUAGE=en_US.UTF-8
      export EDITOR='code'
      
      HIST_STAMPS="yyyy-mm-dd"
      HISTFILE=~/.zsh_history
      SAVEHIST=10000000
      
      export PATH=/usr/bin:$PATH
      export PNPM_HOME="$HOME/Library/pnpm"
      export PATH="$PNPM_HOME:$PATH"
      
      # export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
      
      setopt no_beep
      setopt LOCAL_OPTIONS # allow functions to have local options
      setopt LOCAL_TRAPS # allow functions to have local traps
      setopt no_flow_control
      setopt transient_rprompt
      setopt HIST_REDUCE_BLANKS
      
      setopt EXTENDED_HISTORY          # Write the history file in the ':start:elapsed;command' format.
      setopt INC_APPEND_HISTORY        # Write to the history file immediately, not when the shell exits.
      setopt SHARE_HISTORY             # Share history between all sessions.
      setopt HIST_EXPIRE_DUPS_FIRST    # Expire a duplicate event first when trimming history.
      setopt HIST_IGNORE_DUPS          # Do not record an event that was just recorded again.
      setopt HIST_IGNORE_ALL_DUPS      # Delete an old recorded event if a new event is a duplicate.
      setopt HIST_FIND_NO_DUPS         # Do not display a previously found event.
      setopt HIST_IGNORE_SPACE         # Do not record an event starting with a space.
      setopt HIST_SAVE_NO_DUPS         # Do not write a duplicate event to the history file.
      setopt HIST_VERIFY               # Do not execute immediately upon history expansion.
      setopt APPEND_HISTORY            # append to history file
      setopt HIST_NO_STORE             # Don't store history commands
      setopt prompt_subst
      setopt CORRECT
      setopt complete_in_word
      setopt IGNORE_EOF
      
      plugins=(
        zsh-autosuggestions
        fast-syntax-highlighting
        command-not-found
        you-should-use
        git-open
        vi-mode
        zsh-vi-mode
        autoupdate
        sudo
        zsh-completions
        history-substring-search
        fzf-tab
      )
      
      ZSH_THEME="robbyrussell"
      
      ZVM_VI_INSERT_ESCAPE_BINDKEY=jj
      
      zle -N history-substring-search-up
      zle -N history-substring-search-down
      bindkey "^[[A" history-substring-search-up
      bindkey "^[[B" history-substring-search-down
      bindkey '\e[A' history-substring-search-up
      bindkey '\e[B' history-substring-search-down
      bindkey '\eOA' history-substring-search-up # or ^[OA
      bindkey '\eOB' history-substring-search-down # or ^[OB
      
      export FZF_PREVIEW_COMMAND="([[ -f {} ]] && (bat --style=numbers --color=always {} || cat {})) || ([[ -d {} ]] && (tree -C {} | less)) || echo {} 2> /dev/null | head -200"
      # ! export FZF_DEFAULT_OPTS="--multi --cycle --inline-info --ansi --border --layout=default --height 80% --no-reverse --preview-window=:hidden --bind '?:toggle-preview' --preview '($FZF_PREVIEW_COMMAND)'"
      export FZF_DEFAULT_OPTS="--multi --cycle --inline-info --ansi --border --layout=default --height 80% --no-reverse --preview-window=:hidden --bind '?:toggle-preview'"
      export FZF_DEFAULT_COMMAND="ag --ignore-dir .git --ignore-dir .idea --ignore-dir .vscode --ignore-dir node_modules --ignore-dir pkg --ignore-dir bin --ignore-dir github.com --ignore-dir dist  -g ''"
      export FZF_CTRL_T_COMMAND="$FZF_DEFAULT_OPTS"
      export FZF_CTRL_R_OPTS="$FZF_DEFAULT_OPTS"
      
      zstyle ':fzf-tab:complete:kill:argument-rest' fzf-flags '--preview-window=down:3:wrap'
      zstyle ':fzf-tab:complete:kill:argument-rest' fzf-preview 'ps --pid=$word -o cmd --no-headers -w -w'
      zstyle ':fzf-tab:complete:kill:*' popup-pad 0 3
      zstyle ':fzf-tab:complete:cd:*' fzf-preview 'exa -1 --color=always $realpath'
      zstyle ':fzf-tab:complete:cd:*' popup-pad 30 0
      
      zstyle ":fzf-tab:*" fzf-flags --color=bg+:23
      zstyle ':fzf-tab:*' fzf-command ftb-tmux-popup
      zstyle ':fzf-tab:*' switch-group ',' '.'
      zstyle ':fzf-tab:*' fzf-preview '([[ -f  $realpath ]] && (bat --style=numbers --color=always  $realpath || cat  $realpath)) || ([[ -d  $realpath ]] && (tree -C  $realpath | less)) || echo $realpath 2> /dev/null | head -200'
      
      zstyle ':completion:*' list-colors ${(s.:.)LS_COLORS}
      zstyle ":completion:*:git-checkout:*" sort false
      zstyle ':completion:*' file-sort modification
      zstyle ':completion:files' sort false
      zstyle ':completion:*:exa' sort false
      
      autoload -Uz compinit
      compinit
      
      source $ZSH/oh-my-zsh.sh
      
      alias cat='bat --paging=never'
      alias du='dust'
      alias vim='nvim'
      alias ls="exa"
      
      alias mkdir='mkdir -pv'
      alias cp='cp -i'
      alias rm='rm -i'
      alias mv='mv -i'
      alias cls='clear'
      alias extract='ouch'
      alias ss="br"
      alias diff="difft"
      
      alias bi="brew install"
      alias bs="brew search"
      
      function copy() {
        pbcopy < $1
      }
      
      alias gs='git status'
      alias gc='git checkout'
      alias log="git log --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative --graph --decorate"
      alias ..='cd ..'
      alias ...='cd ../..'
      alias ....='cd ../../..'
      alias .....='cd ../../../..'
      alias ~="cd ~" # `cd` is probably faster to type though
      alias -- -="cd -"
      
      alias config='code ~/.zshrc'
      alias reload='source ~/.zshrc'
      
      alias nc='rm -rf node_modules && rm -rf {package-lock.json,yarn.lock,pnpm-lock.yaml}'
      
      alias kp="kill-port"
      
      # source ~/powerlevel10k/powerlevel10k.zsh-theme
      
      # To customize prompt, run `p10k configure` or edit ~/.p10k.zsh.
      # [[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
      
      # neofetch
      
      eval "$(zoxide init zsh --cmd cd)"
      source $HOME/.config/broot/launcher/bash/br
      
      eval "$(fnm env --use-on-cd)"
      
      export PYENV_ROOT="$HOME/.pyenv"
      command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
      eval "$(pyenv init -)"
      
      #THIS MUST BE AT THE END OF THE FILE FOR SDKMAN TO WORK!!!
      # # export SDKMAN_DIR="$HOME/.sdkman"
      # [[ -s "$HOME/.sdkman/bin/sdkman-init.sh" ]] && source "$HOME/.sdkman/bin/sdkman-init.sh"
      ```

3. [Done] autojump/**zoxide**

```Bash
bi zoxide

# add the following to zshrc
eval "$(zoxide init zsh --cmd cd)"

# optional
zoxide import --from=autojump "/path/to/autojump/db"
```

1. [Done] find -> fd

```Bash
bi fd
```

1. [Done] fzf

```Bash
bi fzf

# To install useful key bindings and fuzzy completion:
$(brew --prefix)/opt/fzf/install
```

1. [Done] cat -> bat

```Bash
bi bat
```

1. [Done] du -> dust

```Bash
bi dust
```

1. [Done] sd

```Bash
bi sd
```

1. [Done] ls -> exa

```Bash
bi exa
```

1. [Done] top -> bottom

```Bash
bi bottom

# 用法 btm
```

1. [Done] tree

```Bash
bi tree
```

1. **[Done] br** / llama

```Bash
bi broot

broot
```

1. [Done] jq

```Bash
bi jq
```

1. [Done] fx

```Shell
bi fx
```

1. [Done] wget

```Bash
bi wget
```

1. [Done] httpie

```Bash
bi httpie
```

1. tmux
2. [Done] the_silver_searcher

配合 fzf 一起使用

```Bash
bi the_silver_searcher
```

1. [Done] neofetch

```Bash
bi neofetch
```

1. 因为使用 warp，以下 prompt 不再使用

   1. p10k

   2. ```Bash
      bi romkatv/powerlevel10k/powerlevel10k
      echo 'source $(brew --prefix powerlevel10k)/powerlevel10k.zsh-theme' >>! ~/.zshrc
      
      reload
      
      p10k configure
      ```

   3.  ···

2. [Done] tokei

```Bash
brew install tokei
```

1. Wrap 内置了 history 查询
   1. atuin
2. [Done] tldr

```Bash
brew install tldr
```

1. [Done] cheat

```Bash
brew install cheat

cheat
```

1. [Done] ouch

```Bash
brew install ouch
```

1. [Done] diff

   1. [difftastic](https://github.com/Wilfred/difftastic)

   2. ```Bash
      brew install difftastic
      
      git config --global diff.external difft
      ```

   3. git-delta

   4. diff-so-fancy

   5. git-split-diffs

## [Done] 配置

### [Done] 设置同步

1. 软件更新
2. 通用 修改设备名称
3. 外观
   1. 在滚动条中点按 跳到点按位置
4. 控制中心 调整图表
5. 关闭定位服务
6. 显示器调整缩放率
7. 更换墙纸
8. 调整锁定屏幕

![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=YjlkZTFmMzc4ZjE3YmRmYTRhZjU5OTdkZmZlMzYzODZfeFdpbDJzZm5KMFhmNk44UDV1NHpyeVpydm5DS1lRUTlfVG9rZW46R2RxU2J6cTF4b3ZDenh4MnlDTGNZcURsbk1iXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=YzIzYWY2MDI4NjYzZWE5MTRkNjRlMmI1NTFkMjM5ZGZfZGxJNzJvTGN0WVpOazRYcmF6aHZmZFoyU3daTjl2cXlfVG9rZW46TkppVGJjTTdDb09Qc3Z4R2Y4dWNpNHJNbmJ4XzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=MGUxMWIzMmFhMGIyN2I2MDQxYTA2YjM2ZTFmY2MwYzdfZmJvUEZ4aUkzTzVXMmUyMFpzUUV6VWFPWVIxQkJic3lfVG9rZW46T0NKbmJyOXlVb0RNOGR4eTFPNGNhaWxSbmRkXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NTI4NGI4ZTBiMmQzNDhhZWZmYzdmYjRjNTQzZjBmOTNfeEJtcW5aU1lob0R5R3VTQXNiU2M3amFFRjRCdUJCMURfVG9rZW46VTdUa2IxVTBRb2ROODl4WW9ydmNiZUdlbmRlXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=Njk3NzcwMDczMjkxNjhiYTkyNWFjMjI3MGM0ZTMwNjVfMnFmYUJyWUtaR25pa0FGUGR3aUh4REdobjBmUk1OZWdfVG9rZW46RHNCVGI3aWdHb1JSSFh4bnFIV2NsRE1QbnViXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=ZjJkZGM1MmExMzRlMTExNWVhMTYwMjA1NTUzYWY3OThfVkFxU04zZFpyd1l6RGx4anpKMTNHckJOZ1U2SnZxZG5fVG9rZW46UnBmcWJiYVFzb291Nll4dHk3dmMxRFlvbjFkXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=ODVlYWVkZDQ1N2Q4NzI5MzcwZGFjM2NkOWNmNjQ5MjFfb0VnSjlsd1UwaE9tNDhJUTVyUExOVFp3a3RHejJ1bmtfVG9rZW46TnJreGJuV01Sb1E0bWx4Nm9URGM3QWFkbkRkXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NGY5NTQ2MWNkYzBhZWY2NTczYTY3ZGJjOTM0MTc3ODVfZlllT0Q5eUwzTERObTN0dk14MHRnVE4zQVpoRGtaYkVfVG9rZW46VWhESmJRU1dqb3FPTjB4TVg1amN1eE9BbmFnXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)

### [Done] 改键配置

![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=MDhmZmU0NjU0NDk5YjYwNThlZWZiMDNlMDhiNjg5ZmVfenl3Z25xUmZSMXFhdENjY2hXSWpKbjZMZzJ1ZE9FS0dfVG9rZW46TUNHWWJuY3FrbzFjU094cXlUTGM0YlJpbm9iXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NDY0OWZiZDI5MTNiYjFhYmUyMTllM2M4OWFjMGNiMGJfOWVmbDExNGFQSlh6V1J2TVpTQUlpQmpQNVYzU0RReGVfVG9rZW46RzR1emJKanVGb1o4WVB4TndVemM4b0xYbmhoXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=YjNiZTE5MjEzYTk5NjNjODc1ZWVkYzBmZjQ0ODM1NDJfQUJzZ2pjUndvdnhxTVUxb2pOaVhMZ3pHaVBTTjdUUWNfVG9rZW46QktQVWJCSzJXb3h0Um14MFJSS2M5SGptbmpnXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=YTM2YTBhZThlMWViMWU1M2YwZjBjNTNhZTZjMjRhMDhfc3dzNkNtMkxGd1pmU012VmVpc0ZlbzZFUHhmd0xMNHdfVG9rZW46Q2pYZ2JrdUZVb2ltTDZ4RnlLVGNNeGxCbnFEXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NTY4OTEwMmFjMGNkYWQ5NjU2YWI3Yjc2ZjkwMWFkZTFfdjNpNUl1ZXV2V0ZJeFpFRVgwSDNLWmVTVnN1VXVGMU5fVG9rZW46WnZFNmI0b0F6b3hjbVN4ZElVTGN4NkZHbmtlXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)

1. 其余全部取消勾选
2. 将 Capslock 配置成 F15

```Bash
hidutil property --set '{"UserKeyMapping":[{"HIDKeyboardModifierMappingSrc":0x700000039,"HIDKeyboardModifierMappingDst":0x70000006A}]}'
```

1. 永久保存配置 - `~/Library/LaunchAgents/com.tomotoes.CapslockF15.plist`

```Bash
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<!-- Place in ~/Library/LaunchAgents/ -->
<plist version="1.0">
  <dict>
    <key>Label</key>
    <string>com.tomotoes.CapslockF15</string>
    <key>ProgramArguments</key>
    <array>
      <string>/usr/bin/hidutil</string>
      <string>property</string>
      <string>--set</string>
      <string>{"UserKeyMapping":[{"HIDKeyboardModifierMappingSrc":0x700000039,"HIDKeyboardModifierMappingDst":0x70000006A}]}</string>
    </array>
    <key>RunAtLoad</key>
    <true/>
  </dict>
</plist>
```

### [Done] 字体配置

```Bash
brew tap homebrew/cask-fonts
```

1. Roboto

```Bash
brew install font-roboto
```

1. FairCode

```Bash
brew install font-fira-code
```

1. JetBrainsMono

```Bash
brew install font-jetbrains-mono
```

1. source-code-pro

```Bash
brew install font-source-code-pro
```

1. 霞鹜文楷
2. NerdFont

```Bash
brew install font-jetbrains-mono-nerd-font font-fira-code-nerd-font
```

### [Done] 系统配置

1. [Done] 管理员权限
2. [Done] Sudo 免输入密码

```TypeScript
sudo vim /etc/sudoers

 %admin          ALL = (ALL) ALL
=>
 %admin          ALL = (ALL) NOPASSWD: ALL
```

1. [Done] 程序分组配置

#### [Done] 访达设置

![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=ZjdlYzYzNTIyNzQ2MjBkNmNmYzkxMjBlMWZjOWFlNGNfdmF3ZG5NS2lOWDVTT0NHUHR4T3FISTdZbEtsem9QOEpfVG9rZW46UVEyOWJjSnNxb1k4aUN4RDRGbGNhczF4bjVmXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=ZTgwMzEwZjQ0ZjcwOGJiOGIxMjQwOGNhMWE4MDMxNDNfQmp2NnBZU1lkbTF2MGxMRVhLT05lNkxDdEN3UkpOTndfVG9rZW46UEx4WmJzekZUbzRGVE94T0V5dGM2S1FrbkhjXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NWQ0ZTY3YmZmMDRkMDc4YzU1ZWNmNTY3ZjM2ZDQ4N2FfN3UwWWdsVXkxelZlT1B3SGUxSE1NODh0Y0ZXNk53dHhfVG9rZW46Q2FQTmJYTnFYb3NxMHJ4cTIwRWM2Z0l4bldlXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=MDY4ZTk4YzI3M2YxZjdjMGFhYmU3NDIwMzFmYzFlNTVfdEF4Tm5XSEpqdHhpbnh3TVJCRHVrN1pRMFBUb0NaMHJfVG9rZW46UThQVGJyWnpBb2N1SkJ4ajdqQ2NsSExDbmNlXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=Yjk3M2NjNTg3ZGFlMjFiMmNlNGJjOGY5ZTZmMjA2ZWFfak10Wk9Jb0JINFJGcUROOHNBeXpmcFRjUHFFVlJsaFNfVG9rZW46WHN1OGJ0UUJCb0REY0x4TDk5ZmNnUFl4bnJnXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=MWI0NDMzOTIwNjQ1ZjAyYjk1MDdiNGZhMmEyYzAxNzVfeDdQem1IcHF5QkFDakZLekE0MUdISEtyS1B5WU9CaEVfVG9rZW46SzRCVmI4ZUJvb29PdXh4eFY5Z2NnUmhKbndnXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)

### [Done] 调优配置

```Bash
# Save to disk, rather than iCloud
defaults write NSGlobalDomain NSDocumentSaveNewDocumentsToCloud -bool false

defaults write com.apple.Finder AppleShowAllFiles -bool true
defaults write com.apple.finder AppleShowAllFiles TRUE

echo "Expanding the save panel by default"
defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode -bool true
defaults write NSGlobalDomain PMPrintingExpandedStateForPrint -bool true
defaults write NSGlobalDomain PMPrintingExpandedStateForPrint2 -bool true

echo "Displaying ASCII control characters using caret notation in standard text views"
defaults write NSGlobalDomain NSTextShowsControlCharacters -bool true

echo "Removing duplicates in the 'Open With' menu"
/System/Library/Frameworks/CoreServices.framework/Frameworks/LaunchServices.framework/Support/lsregister -kill -r -domain local -domain system -domain user

echo "Disable Photos.app from starting everytime a device is plugged in"
defaults -currentHost write com.apple.ImageCapture disableHotPlug -bool true
```

- 在「Privacy & Security > Developer Tools」里把 Terminal 等开发者工具加上，绕开系统的安全策略，据说可以让请求和编译更快。

### [Done] 网络配置

相关文章：https://hifool.cn/posts/f42b65b0/

#### [Done] VPN Client

ClashX - Pro

https://install.appcenter.ms/users/clashx/apps/clashx-pro/distribution_groups/public

#### [Done] VPN 配置

1. https://sockboom.tv/user/ 一键导入配置
2. https://github.com/Loyalsoldier/clash-rules 增加规则到 配置文件中

1. 在 vpn 配置中手动配置 `clash-rules` 规则
2. 其中`rules` 中的 `PROXY` 需换成 `手动选择`（Proxy 的名称）
3. 出站模式选择 `规则判断`
4. 重启 clash 或者 重载配置
5. 使用 yacd 的日志功能进行测试
6. 进行 shell 的网络代理

![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=ZjgzMmI5OGU0NmUwNGIxM2RjOTkzZTNhYTQ5YjU3MzJfckNLeWRiMFB6d2QwQm5sdktabUVCMFdiOWJjeTc4UmFfVG9rZW46VUZqeGI5cXVwb0NGT2p4WVp5aWM3N1RBblNoXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NWRmMDBhNzU4NjUxMzEyMGUwYTY4NmJmODMwZTUxMmRfN0p0dUZFeW52WVlmamljaWpmcHhvWUtqc1hzODd6RXFfVG9rZW46UWxSc2J1Z1Ezb0wxdjF4UFg4QWNna0l1bktlXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)

#### [Done] 网络代理

```Plaintext
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

### [Done] 浏览器配置

1. Bitwarden 登录，并配置验证方式
   1. 取消超时
   2. 配置 pin 码（不勾选主密码验证）
2. Git Master、GitHub Hovercard 生成 并 配置 token
3. 油猴
4. 简悦
5. 掘金 Tab

### [Done] 输入法配置

1. 只保留 ABC 与 搜狗输入法
2. 登录搜狗输入法并同步
3. 模糊音全部开启

![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NmY4YzVlMjhmYTQwNmJlZGMzNWU2OTVmZGI4YmE4NjdfaFZaUU5YNlI5ZW1pU2E4Z1lndU1NQUVxZXhyN2ZDdnBfVG9rZW46WGFzcmJwV2ZIb0YwVmx4R0pjRGN6NnJ2bmtlXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=NmIwMjQzZGM0MGFkNGUzYTI0MjBkZWNkMjcwNjAxZjJfVk9KSWdoNzROclZURVNyMFA3cjdpSTVIS1BzWlc4TExfVG9rZW46UXBRVmJGR1FMb3gzQUp4Z0lZeGNYcGtibkRnXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=YjRhM2YyYzg1NjIwMmQ4NWEyN2YxZTM0NzA2M2MyMDRfQXh4U3V2Z3NhSEY0SXgwTmZITGlveEhYMDNrT3pQQXFfVG9rZW46TEl0dGJIRko4b09vUWp4ZGp5VWNqZzZtbk5nXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=Nzg5MTBmODAwM2Q0NzQyMzA3ZDNhNzk5NmJmMjQyMjhfZHdlaEFmS1QyZjJLWUl4S09PcDBRUnVSVGNUQlNZUFRfVG9rZW46VzlIVGJJNjhvb3FmSUR4dW9FT2NJU1pnblpmXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=MTFkZDllMzMzZGY0YzFhMDhlMTcyZTI3YTY0NmM1MTdfeWlwbjU0VjVQV2Y0Zklid29ZN2NxcEQ4OXI4RTZPVTBfVG9rZW46SFdzSGJSd01Ub0xvQkR4eXBTVWNxVkJzbklmXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)

1. 下载 Boundary 搜狗主题 https://github.com/xiaochunjimmy/Sogou-Input-Skin/blob/master/Boundary.mssf
2. F15 配置成 切换上一个输入法
3. ABC 输入法配置

![img](https://fm130w9hwf.feishu.cn/space/api/box/stream/download/asynccode/?code=MmUyYTBmYjRmZGZmNDZmOWViZTNjNGU5MTA0MTMzM2ZfNlp5cjQ5czcxY1ZKMWFFQ1FVQ2wyT0M1RFlDWHpVRjhfVG9rZW46WVZsQmI4aUV0bzJJV2F4cVlBT2N4S2Y2bm1jXzE3MDk2Mjc4MDk6MTcwOTYzMTQwOV9WNA)

## 项目同步

- [Done] Tomotoes
- [Done] Materials
  - [Done] 毕设
- [Done] Media
- [Done] Notes
  - [Done] Softs

- [Done] OpenRepos
  - 最近看的一些开源库
  - https://github.com/Ricbet/panel-magic
  - https://github.com/woai3c/visual-drag-demo
  - https://github.com/nashaofu/node-screenshots
- PersonalRepos
  - Tomotoes
    - About
    - Blog
    - CDN
    - Gallery
    - Home
    - React-Terminal
    - Thinking
    - Version
    - Weibo
  - GE

## 问题

### [Resolved] Option + 数字键 会打开程序坞的软件

### [Resolved] Option D 无法 toggle VSCode

将 VSC 放到了应用程序中

### [Resolved] 去掉警报声音

将声音调低

### [Resolved] Warp Cmd+Enter 已经被 AI 提示使用

### [Resolved] VSCode 切换主题快捷键与截图快捷键冲突

修改成 A+4

### 「Resolved」Google 双栏有时候无法点击

换成分页模式时，stylus 样式会失效

### Warp 功能缺陷

- 无法使用 vim mode

Broot 打开时没有默认 preview 状态

## 相关资源

- https://mp.weixin.qq.com/s/sdBZTSOzm94Zopgr_OijOg
- https://www.robinwieruch.de/mac-setup-web-development/
- https://www.swyx.io/new-mac-setup-2021
- https://github.com/dubuqingfeng/dotfiles
- https://github.com/nicolashery/mac-dev-setup
- https://www.taniarascia.com/setting-up-a-brand-new-mac-for-development/?ck_subscriber_id=591519942
- https://github.com/mathiasbynens/dotfiles
- https://gist.github.com/brandonb927/3195465
- https://github.com/TaKO8Ki/awesome-alternatives-in-rust