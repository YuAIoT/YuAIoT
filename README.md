
**YuAIoT**
YuAIoT is an integrated and open source solution for the rapid construction of AI IoT applications.

We live in a world of extensive internet. Not only people commuting in internet, but more and more things we know or don't know well are becoming in internet, de isolated, easier to be perceived and become more intelligent, more and more interactions between things and people happens, the world is becoming more and more interesting. How to realize connecting, intelligence, isolation, perception and interaction more quickly is the original intention of founding the YuAIoT project on New Year's Day 2021(this day is so cold!  ^_^).

YuAIoT platform is composed of server, web client, iOS client, Android client, device end device system. YuAIoT platform will provide an integrated and open source solution for the rapid construction of AI IoT applications. We hope that the components of YuAIoT platform are common, and the components of the platform are optional. Developers can choose the components they need or customize them based on their own needs.

**Components of YuAIoT platform**
As a technology controller, I hope to ensure using mainstream or cutting-edge technology in building the YuAIoT platform, in order to make the open source IoT platform YuAIoT is excellent and more acceptable. The components of YuAIoT platform are as follows.

| Component  | Function  | Tech stack  |
| ------------ | ------------ | ------------ |
| YuAIoT Server  | server  | SrpingCloud、Netty、MySql、Redis  |
| YuAIoT Web  | Web client and admin client  | Vue.js、Node.js  |
| YuAIoT iOS  | iOS client app  | iOS SDK  | 
| YuAIoT Android  | Android client app  | Android SDK  |
| YuAIoT Device  | Device, will using AI chip Kendryte K510 as its SoC  | Kendryte K510  |
| YuAIX  | Python environment runs on YuAIoT Device  | base on MicroPython  |

**YuAIoT Server**
YuAIoT Server is an open source, distributed IoT server software. It will be built on the Spring Cloud framework. It is mainly responsible for device connection, device management, device data parsing, data analysis and data processing. It also provide the corresponding API for clients of web client, iOS client, Android client, etc.
The differences between different kinds of things are often great. When making things connect to the Internet, the models we use in building a system for certain kinds of things are also different. The differences exist objectively and cannot be eliminated. In order to ensure YuAIoT Server can provide connection of all kinds of devices that need to be connected, we use the concept of object model. Platform users can directly establish the corresponding physical model for the devices that need be connected to internet in a visual way according to various needs. After devices are connected to the YuAIot server. The YuAIoT server collects and analyzes the data reported by the device. The analysis rules are specified according to the user's needs. With the parsed data, we need to make use of these data. Therefore, YuAIoT server will also integrate a flexible rule engine, which can easily customize the implementation of device alarm, message push, data forwarding, linkage operation, etc.

**YuAIoT Web **
YuAIoT Web is web client and admin client in YuAIoT plaform. It will base on Node.js and Vue.js. YuAIoT Web provides user login, device data presentation, device control, device management, object model management, rule engine management, user management and other functions

**YuAIoT iOS **
YuAIoT iOS is the iOS client app, which provides user login, device data presentation, device control, user management and other functions.

**YuAIoT Android **
YuAIoT Android is the Android client app, which provides user login, device data presentation, device control, user management and other functions.

**YuAIoT Device**
YuAIoT Device is an IoT hardware device supporting AI function in YuAIoT platform. We plan to make it into a development board to facilitate development. It will use AI chip Kendryte K510. Why K510 chip? Kendryte K210 is an AI chip with good performance price ratio that launched in 2019. We also see that there are many development boards or devices based on this chip on the market. K210 has many advantages, such as low power consumption, open source, good computing power and relatively high cost performance. However, Kendryte K210 is an experimental AI chip product of Canaan-Creative, which has some obvious shortcomings (such as weak computing power and small RAM). K210 is called No.0 (instead of No.1) AI chip in Canaan-Creative, which shows that K210 is a transitional AI chip product. We are more looking forward to the second generation AI chip K510 to be released by Canaan-Creative. It is understood that the computing power of K510 can reach 3TOPS, and it can be equipped with multi channel HD cameras. The technical specifications will be fully compatible with tensorflow and support all operators in tensorflow file format. It is understood that K510 chip will be released in the first quarter of 2021.

**YuAIX**
As time goes on, the performance of MCU chips is getting higher and higher, and the resources on MCU chips are increasing. Compared with a few years ago, the price may not increase much or even be cheaper. I think it is a trend to run Python software on medium performance chips. After all, sometimes we want to use less time to develop software that can do more things or more complex things. Compared with C language or C++ development, Python is much more convenient (although Python software runs slower than C/C++ software, it often runs fast enough to let us ignore this disadvantage). We plan to run Python environment directly in YuAIoT device, so that developers can use Python directly to quickly make more interesting and meaningful application. The performance and resources of MCU in AI chip K510 used by YuAIoT device are enough to run Python environment. The Python environment of YuAIoT device we plan to develop will base on MicroPython, which is suitable run in embed system.
