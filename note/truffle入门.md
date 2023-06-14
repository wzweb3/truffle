# TRUFFLE

**Truffle是一个世界级的开发环境，测试框架，以太坊的资源管理通道，致力于让以太坊上的开发变得简单**

### 环境搭建

安装truffle

```shell
npm install -g truffle
```



安装solidity编辑器

```shell
npm install -g solc
```



安装web3.js

```shell
npm install -g web3@1.10.0
```



安装webpack

```shell
npm install -g webpack@4.46.0
```



### truffle项目入门

创建项目

```
truffle unbox webpack
```



提示连接失败，修改系统hosts文件，把失败提示的ip加入到hosts文件。参考：https://blog.csdn.net/qq_40452317/article/details/90315213

提示 EPERM: operation not permitted ，使用vscode执行命令



成功之后项目文件已创建，但是缺少package.json



初始化

```
npm init -f
```

初始化成功后自动生成package.json文件



修改package.json内容

```json
{
  "name": "truffle-project",
  "version": "1.0.0",
  "description": "test project",
  "main": "truffle-config.js",
  "directories": {
    "test": "test"
  },
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "private": true,
  "dependencies": {
    "formidable": "^1.2.2"
  }
}
```





### 启动truffle项目



安装依赖

```shell
npm install
```



运行开发模式

```shell
truffle develop
```

```
Truffle Develop started at http://127.0.0.1:8545/

Accounts:
(0) 0xff820a71d35552775a66cc13638520224006b16e
(1) 0xdd06c28a7f742cd78501550e30b0b73e1a791bd7
(2) 0x4ae17682046d4cb4dd98a1bc58d43b21078a09a6
(3) 0x05818e936c810effcd3b947e85b38ed6af5b7036
(4) 0x0756ec21951fe443823b7d8b3f498f2c04946b2a
(5) 0x554cb34f7bb7c44a4b030929782da23e392974da
(6) 0xc0f7e58c9114e4005b8a4933b4121940b06074a7
(7) 0x9567e0bc64a6bd2167643e0b1d1ae3867e9f6d1f
(8) 0x6d7dc39d65fb16f68faf2911cb69444f74a065f2
(9) 0xce97e0dfe3f608beb6455e3d543cdbd44e71c497

Private Keys:
(0) 321c5a8df4d59b1851501f6023889d18c958095e29a0728b864d0e7020f752eb
(1) b4d6a2eb482e72c85bd602265868e57c61a17fd0d7f9c1ebbb785ca87e45d25a
(2) 283d781abda64e992d018dab6dbd24ecdc72f379609878511741d25f0961aed6
(3) f149a73830c28d67c8a046b6ffca3e533d05d1f0d20d4e88300327276d91d1a3
(4) 669008df0044c0111473d91be3bebd734dd65a6aae74e3b591715e8ea492d4f3
(5) 4ba4027c73f84e4a2c6595f03f76bfa594b5e23f1412f9e222a08991182cf0f8
(6) 8e03f23a9b4ecab788b0f04f2d12f00afd65afc20e4aa51c50105df26183428b
(7) 063be7dbfde8ae876b67f99837006f089b8fe82e78202b8b3b50a66d79fefe36
(8) bb55de09be47ac1e6e29f530702d284cc491548e002d90d2d7013ffe460196de
(9) 7a0b4b3b90af904f6bab473f7ca8ea6921b4a7c8e416698e9aca8f6141c22384

Mnemonic: pulse dice labor view gate panther daring security captain issue flip tail

⚠️  Important ⚠️  : This mnemonic was created for you by Truffle. It is not secure.
Ensure you do not use it on production blockchains, or else you risk losing funds.
```

此时已创建了10个账号，并进入开发模式



编译项目

```shell
truffle(develop)> compile
```



部署项目

```shell
truffle(develop)> migrate
```



### 启动web项目

进入truffle项目中的app目录下

启动项目

```shell
npm install

npm run dev
```

启动成功后进入web页面http://localhost:8080/



### 测试

进入页面，会自动加载前面生成的第一个账号，可看到这个账号余额

You have **8800** META



测试转账：1、输入转账数量	2、输入地址（从10个账号中选择，选第一为转给自己）

点击send，提示Transaction complete!

此时上方余额发生改变，转账成功





