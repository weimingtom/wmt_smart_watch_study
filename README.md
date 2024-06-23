# wmt_smart_watch_study
My smart watch study

## (TODO) lvgl-watch  
* https://github.com/diylxy/lvgl-watch  

## (TODO) NWatch  
* https://gitee.com/weidongshan/NWatch-DShanMCU-F103  
* https://www.bilibili.com/video/BV1Rw411r7kb  
* https://blog.zakkemble.net/diy-digital-wristwatch  
* https://github.com/ZakKemble/NWatch  

## (TODO) zhuhai-and/LV8AndroidWatch, fbiego/esp32-c3-mini   
* https://www.bilibili.com/video/BV1iJ4m1u7FF    
* https://github.com/fbiego/esp32-c3-mini   
* https://github.com/zhuhai-and/LV8AndroidWatch   
* https://github.com/zhuhai-and/LV8AndroidWatch/releases  

## (TODO) OV-Watch, NUCLEO-F411RE + Waveshare 1.69inch Touch LCD Module    
* https://www.waveshare.net/wiki/1.69inch_Touch_LCD_Module  
* connection
```
right border<->left,1,2,right,1,2
VCC<->VCC<->left 2 top 8
GND<->GND<->left 2 top 10
LCD_DIN<->PB5(x)PA7<->right 1 bottom 5(x)right 1 top 8
LCD_CLK<->PB3(x)PA5<->right 1 bottom 4(x)right 1 top 6
LCD_CS<->PB8<->right 1 top 2
LCD_DC<->PB9<->right 1 top 3
LCD_RST<->PB7<->left 1 bottom 9
LCD_BL<->PB0(x)PC0<->left 2 bottom 3(x)left 2 bottom 1
TP_SDA<->PB4<->right 1 bottom 6
TP_SCL<->PB6(x!!!)PA8<->right 1 bottom 11(x)right 1 bottom 8
TP_RST<->PA15<->left 1 bottom 11
TP_IRQ<->PB1<->right 2 bottom 8
```
* https://github.com/No-Chicken/OV-Watch  
https://item.taobao.com/item.htm?id=791307182743  
https://gitee.com/kingham/OV-Watch  
https://github.com/No-Chicken/FryPi  
https://gitee.com/kingham/FryPi  
* ov-watch + NUCLEO-F411RE   
OV_Watch_V2.4_v13_will_crash_close_backlight.7z  
* sim
```
在xubuntu20下编译运行OV-Watch的模拟器代码成功，效果如下，左边是我自己的工程模板，
右边是定制过的模拟器代码（带鼠标图标，修改过）。原版是用Windows编译（可能是cmake），
我这里是用make编译，所以要改动。我猜测可能是用squareline或者类似的工具生成ui代码。
至于硬件手表版，还没开始研究
```
* OV-Watch-main_xubuntu_v1_sim_success.tar.gz

## OneWatch, STM32F411, port to NUCLEO F411RE + 1.28inch round screen    
* (not good) OneWatch_Soft_f411re_final_work.7z  
* 学了3天的littleVGL做了一个手表, OneWatch, STM32F411    
* https://www.bilibili.com/video/av757399659  
* search baidupan, OneWatch.rar  
* nucleo f411re: OneWatch_Soft_f411re_v1.rar  
* (IMP) f411ceu6: OneWatch_Soft_v1_success_缺面包板接线图.rar  
* Nucleo F411RE<--->1.28寸圆形屏    
```
Nucleo F411RE<--->1.28寸圆形屏  
GND（左3列7行）<--->GND  
3V3（左3列4行）<--->VCC  
PA5（右1列5行）<--->SCL(SPI1)  
PA7（右1列7行）<--->SDA(SPI1)  
PA6（右1列6行）<--->RES  
PA4（左3列11行）<--->DC  
CS接地 <--->GND
BLK<->NC  
PA9（右1列10行）<--->上按键（向上翻）
PA10（右1列16行）<--->下按键（向下翻）
PA11（右3列7行）<--->右按键（确定）
PA12（右3列6行）<--->左按键（取消）
```

## ZSWatch v1, nRF52833-DK + 中景园GC9A01圆屏    
* https://github.com/jakkra/ZSWatch  
* (nrf52833 dk, ncs 2.2.0) ZSWatch_v1_v2_run_success.rar     
* (zephyr display demo, nrf52833 dk, ncs 2.2.0, with or without LVGL)  
gc9a01a_zephyr_driver_app_v7_lvgl.rar  
* nrf52833 pins to GC9A01, SPI1    
```
//MISO P1.08
//MOSI P0.30
//SCK P0.31
//CS0 P0.16	
---
//GND: GND
//VCC: VDD
//SCL: P0.31
//SDA: P0.30
//RES: P0.03
//DC:  P1.00
//CS: P0.16 -> P1.03
//BLK: P0.26
```
* https://docs.zephyrproject.org/latest/boards/arm/ubx_evkninab4_nrf52833/doc/index.html  
* https://docs.zephyrproject.org/latest/boards/arm/nrf52833dk_nrf52833/doc/index.html  

## ZSWatch v2, nRF5340-DK + 微雪GC9A01圆屏带触摸      
* (nrf5340 dk, ncs 2.3.0) ZSWatch_v2_v5_succss_no_sleep_touch.7z  
* (nrf5340 dk, ncs 2.3.0) ZSWatch_v2b_v1_success.7z  
* (zephyr display demo, nrf5340 dk, ncs 2.3.0)  
gc9a01a_zephyr_driver_app230_run_success.rar  
* nrf5340 pins to GC9A01, SPI4    
```
//MISO P1.14
//MOSI P1.13
//SCK P1.15
//CS0 P0.06
---
//GND: GND
//VCC: VDD
//SCL: P1.15
//SDA: P1.13
//RES: P0.25
//DC:  P0.07
//CS:  P0.06 -> P1.03
//BLK: P1.06->VCC (waveshare version touch round screen is high)
```
* https://docs.zephyrproject.org/latest/boards/arm/nrf5340dk_nrf5340/doc/index.html  

## open-watch, STM32F030C8T6, but port to STM32F103RCT6 + OLED12864      
* https://github.com/SMotlaq/open-watch    
* https://github.com/SMotlaq/open-watch/blob/master/open-watch-firmware/my_watch_software/Src/main.c  
* openwatch_v5_run_success.rar  
* jlink报错，需要找SWD针脚是否被占用  
https://zhuanlan.zhihu.com/p/70099066  
* RCC设置晶振  
https://blog.csdn.net/Qxiaofei_/article/details/119006893   
* 定时器开NVIC中断（或update中断）  
* (IMP) STM32F103RCT6<->OLED12864  
```
STM32F103RCT6<->OLED12864
3.3V(left 2 bottom 1)<->VCC  
GND(left 2 bottom 2)<->GND  
PB6(left 2 bottom 5)<->SCL  
PB7(left 1 bottom 4)<->SDA  
```

## (TODO, TODO) OM6621, 昂瑞微, HS6621, 汉天下    
* 6621PG手表开发板资料.rar  
* sdk_smartwatch_6621p_gxevb_v01.zip  

## (TODO) FR8000  
* fr8000_lvgl_watch_240x280-master_v1_run_success.rar
* FR8008XP开发板

## (TODO) 优感手表, nrf52840 讯联开发板, with j-link, port to ili9341  
* (TODO) 优感手表, nrf52840, 魔改成ili9341显示（原版不是），注释掉大部分传感器代码  
smart-watch_top_v4_ili9341.7z  
待补充原来的gitee网址  
https://gitee.com/in_drama/smart-watch  
smart-watch_top_v1_build_success.7z
* with nRF5SDK1500a53641a, nRF5 SDK 15.0.0  
* D:\work_nrf52840  
* smart-watch_top_v5_ili9341_watch.7z  
```
sck 47=1.15
miso 46=1.14
mosi 45=1.13
ss 44=1.12
dc 43=1.11
reset 42=1.10
-32
vcc
gnd
cs
reset
dc
sdi
sck
led
sdo
```
* 接线
```
sck 47=1.15
miso 46=1.14
mosi 45=1.13
ss 44=1.12
dc 43=1.11

reset 42=1.10

-32

vcc<->jlink Vout
gnd<->jlink GND
cs<->1.12
reset<->1.10
dc<->1.11
sdi<->1.13
sck<->1.15
led<->jlink Vout
sdo<->NC
```

## csdn TODO:  
* (TODO) 基于STM32的OLED多级菜单项目（简化版智能手表）
* (TODO) 基于STM32的可穿戴手环设计  
