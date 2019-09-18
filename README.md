# IOSTroubles
一些奇奇怪怪的编译、崩溃问题的解决办法

### xcode升级后编译报错Failed to find or create execution context for description...
1. 关闭Xcode ;
2. 在终端中输入以下命令，并回车：
sudo killall -9 com.apple.CoreSimulator.CoreSimulatorService
3. 重启Xcode ;
