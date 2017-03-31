### Atom+Nuclide环境搭建
- #### 安装Atom.

- #### 进入Atom->File->Settings->Install,查找Nuclide插件，并进行install.

  #### ![](https://github.com/Alford087/react-native/blob/master/react-native-doc/image/323837ece550a19cc052acdd8920f5be.jpg?raw=true)

- ##### 安装完毕后，进入Packages->Settings View->Manage Packets寻找Nuclide，选择勾选Install recommended packets on startup，此时退出Atom，再次打开后，会自动安装依赖包. 

  ##### ![](https://raw.githubusercontent.com/Alford087/react-native/master/react-native-doc/image/27651778d8ac43e4ac957de1e5232414.jpg) 

  ![](https://raw.githubusercontent.com/Alford087/react-native/master/react-native-doc/image/802ad51ea96687ea05c779f2758fbcd1.jpg?raw=true)

### 新建工程
- #### 进入cmd，进入项目文件夹。这里举官网例子。 

  ```
  react-native init Demo --verbose
  ```

- #### 打开Atom，点击Add project folder 

  #### ![]() 

- #### sdfsdfs 

### 运行工程 

- 首先需要部署，在IDE中，点击 command + shift + p打开command palette（打开终端选项），然后输入

  ```
  react native start
  ```

  选择**Nuclide React Native :Start packager**。

  如果，出现错误：

  ```
  /Users/huangwenchen/Desktop/Demo/node_modules/react-native/local-cli/cli.js:123
  class CreateSuppressingTerminalAdapter extends TerminalAdapter {
  ^^^^^
  SyntaxError: Unexpected reserved word
      at exports.runInThisContext (vm.js:73:16)
      at Module._compile (module.js:443:25)
      at Object.Module._extensions..js (module.js:478:10)
      at Module.load (module.js:355:32)
      at Function.Module._load (module.js:310:12)
      at Function.Module.runMain (module.js:501:10)
      at startup (node.js:129:16)
      at node.js:814:3
  ```

  这需要更新node.js。更新方式如下

  ```
  sudo npm cache clean -f
  sudo npm install -g n
  sudo n stable
  ```

- 然后通过编译，运行在终端上。运行需要在通过终端命令进入当前文件夹下，并执行

  ```
  react-native run-ios//ios
  react-native run-android//android
  ```

- 调试模式。command + shift + p打开command palette（打开终端选项），输入react native debug，接着，点击模拟器，Command+D，选择Enable Remote JS debugging 。这时候，你会看到，Nuclide中，加载了debug窗口 