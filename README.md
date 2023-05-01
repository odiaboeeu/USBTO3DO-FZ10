# USBTO3DO-FZ10
这是Francois CARON的SATATO3DO项目https://github.com/FCare/SataTo3DO 的拓展，使用了集成电路来缩小体积，具体使用方法请参考其方案
https://github.com/tzmwx/USBTO3DO-FZ10/blob/53a964b5ae9940e723ff627eb59a6fed1fb0ab20/FZ10TEST.jpg


BOM:

最小系统：

U1 RP2040 PICO模块(兼容引脚功能看2040pico.jpg）

U2/U3 TXS0108 TSSOP-20

U4 74LVC4245 TSSOP-24




如果你要在模块上建立一个换盘功能：

你需要增加一个6X6mm的按钮开关和一个R2 4.7K


如果你要在模块上建立一个CD盖子开关换盘功能：

你需要增加R2 4.7K，R3 107K，Q1 9014(或其他NPN三极管）


如果你要在模块上建立一个读盘灯（同主机面板绿色读盘灯）：

你需要增加： R1：470欧姆 LED：3MM



预留了电容的位置，可以不需要安装， C1/C2：220uf-470uf/10V C3/C4/C5/C6/C7：0.1uf

预留了X1,有源晶振OSC SMD7050 33.86Mhz,只有当你不对IC640进行挑脚而是拆除IC640时才需要安装，然后将CLK连接至主板L643

READ读盘灯接口，按图连接至Q410

COVER光驱盖板感应接口，按图连接至SW721，需要增加R2 4.7K，R3 107K，Q1 9014(或其他NPN三极管）,用开关CD舱盖来实现换盘功能

DISC接口是换盘键并联，如不喜欢CD舱盖模式，可飞线一个按钮开关

(+5V,D-,D+,GND)接口可以延长USB，而不使用C延长线，注意此接口要提前在底部与2040模块要焊接好
