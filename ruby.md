mac os上安装ruby

step1:安装homebrew
打开终端并执行以下命令
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

进行中需要管理员密码

>尝试在命令行中运行brew -v来验证是否安装成功。如果安装成功，它应该显示安装的Homebrew版本信息。
>显示zsh: command not found: brew，这意味着你的终端无法识别brew命令。这可能是由于Homebrew的路径尚未添加到你的系统路径中。
>
>(echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/chengsuki/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
>
>这将会将Homebrew添加到你的.zprofile文件中，并且将其配置添加到你的当前终端会话中。然后，你可以尝试重新打开一个新的终端窗口，或者运行source ~/.zprofile来使更改生效。
>
>可以使用brew -v命令来检查Homebrew的版本信息
