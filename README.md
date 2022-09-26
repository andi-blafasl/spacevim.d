# Installation of SpaceVim

1. https://spacevim.org/quick-start-guide/
  - Windows https://spacevim.org/install.cmd
  - Linux `curl -sLf https://spacevim.org/install.sh | bash -s -- --install vim`
2. Fonts https://www.nerdfonts.com/font-downloads
  - SourceCodePro (Sauce Code Pro)
    - https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/SourceCodePro.zip
  - CascadiaCode (Caskaydia Cove)
    - https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip
  - Sauce Code ist used in VIM, Caskaydia Cove is perfect replacement for Windows Terminal
3. Clone this Repo to your $HOME
  - `git clone https://github.com/andi-blafasl/spacevim.d.git .SpaceVim.d`

## use oh-my-posh prompt

1. install oh-my-posh
  - `winget install JanDeDobbeleer.OhMyPosh`
2. add cmder config
  - `cmderr`
  - `cd config`
  - `echo load(io.popen('oh-my-posh init cmd --config %USERPROFILE%/.SpaceVim.d/.mytheme.omp.json'):read("*a"))()>oh-my-posh.lua`
3. add git-bash config
  - `cd ~`
  - `echo eval "$(oh-my-posh init bash --config ~/.SpaceVim.d/.mytheme.omp.json)">>.bashrc`
4. add powershell profile
  - `Add-Content -path $profile -value "`r`noh-my-posh init pwsh --config `"`$env:USERPROFILE\.SpaceVim.d\.mytheme.omp.json`" | Invoke-Expression"`
