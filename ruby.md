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



step2: 安装rbenv
终端输入
brew install rbenv
安装完成后初始化

 rbenv 已经成功安装了。你可以通过以下命令来验证安装是否成功：

 rbenv --version

 
rbenv init 
命令用于在当前 shell 中初始化 rbenv。它将修改你的 shell 环境以便正确地管理不同的 Ruby 版本。通常你只需要运行这个命令一次，然后它会自动在每次打开 shell 时加载。
chengsuki@ChengdeMacBook-Pro ~ % rbenv init

# Load rbenv automatically by appending
# the following to ~/.zshrc:

eval "$(rbenv init - zsh)"

chengsuki@ChengdeMacBook-Pro ~ % 


step3:安装 Ruby 可以通过 rbenv 来完成。你可以使用以下命令来查看可用的 Ruby 版本：
rbenv install -l
这将列出所有可用的 Ruby 版本。选择你想要安装的特定版本，然后使用以下命令安装它：
rbenv install 3.0.6
安装完成后，你可以使用以下命令将全局 Ruby 版本设置为新安装的版本：
rbenv global 3.0.6
