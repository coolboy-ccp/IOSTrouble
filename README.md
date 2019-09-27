# IOSTroubles
一些奇奇怪怪的编译、崩溃问题的解决办法

### xcode升级后编译报错Failed to find or create execution context for description...
1. 关闭Xcode ;
2. 在终端中输入以下命令，并回车：
sudo killall -9 com.apple.CoreSimulator.CoreSimulatorService
3. 重启Xcode ;

### 安装cocoapods
1. 暗转rvm
* curl -L get.rvm.io | bash -s stable 
* source ~/.bashrc
* source ~/.bash_profile
2. 安装homebrew if need
* /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
3. 升级ruby
* rvm list known
* rvm install 2.5.1
* rvm use 2.5.1 --default
4. 升级gem
* sudo gem update --system
5. 替换源
* gem sources --remove https://rubygems.org/
* gem sources --add https://gems.ruby-china.com/
* gem sources -l
6. 安装cocoapods
* sudo gem install -n /usr/local/bin cocoapods
* sudo xcode-select -switch /Applications/Xcode.app/Contents/Developer如果安装了多个版本的xcode时，使用此命令选择xcode版本
* pod setup

### 升级cocoapods
1. 更新gem：sudo gem update --system
2. 删除gem源：gem sources --remove https://ruby.taobao.org/  if need
3. 修改gem源：gem sources -a https://gems.ruby-china.org if need
4. 查看gem源是否是最新的：gem sources -l
5. 升级cocoapods：sudo gem install -n /usr/local/bin cocoapods
6. 查看升级后的cocoapods版本：pod --version

