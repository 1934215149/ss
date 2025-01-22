# PsPal
## 初衷

解决“被打赏人”在收到打赏后无法立刻回应或者回馈“打赏人”问题，同时分享一个除使用主流数据库的数据处理方案。

GitHub 演示：[https://maddog888.github.io/Ps_Pal/](https://maddog888.github.io/Ps_Pal/) 

> 当前支持：VX打赏
> 
> MadDogQQ交流群：591668872

## 前言

  + 哥哥姐姐们，项目是全开源的，连各个模块都全部开源，该项目仅供学习和个人使用，重点是不可以用于商用更不能非法使用！！！感谢！！！

## 打赏端：

> 技术思路(使用Web方式展示接收打赏的信息，由HTML和原生JS以及EMQ的MQTT库实现！)：
> 
1、index.html 为展示创建打赏的过程，由变量（打赏唯一识别号、打赏数额、同步地址、异步地址、通信秘钥）生成打赏内容信息，并通过sha256使用通信秘钥生成唯一签名，避免恶意提交。

2、PsPal.html 通过得到的内容生成打赏内容信息并通过WebSocket协议对MQTT协议服务器发送打赏数据，由服务端验证并在对应的Topic返回识别信息和打赏成功信息。

## 服务端：

> 技术思路(使用中文编程易语言写的应用程序实现)：
> 
1、使用Windows的窗体控件交互访问指定窗口上的内容，并通过MQTT协议实现与打赏端的通信，均已使用sha256签名验证数据真伪。

2、使用服务端即数据库本身的思路开发，并且使用当代物理网MQTT协议的加持通信，使得该方案优于使用主流数据库方案！

## 版权

请遵循[LICENSE](https://github.com/maddog888/ps_pal/blob/main/LICENSE)。

## 其他

因使用sha256加密，采用的是openssl的动态链接库，libeay32.dll文件来自https://www.opendll.com/index.php?file-download=libeay32-1.0.0-msvcrt.dll&arch=32bit&version=&dsc=#

MD5：905a08c595f950e9152635fd3b84d659

请注意甄别！


