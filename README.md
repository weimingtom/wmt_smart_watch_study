# wmt_smart_watch_study
My smart watch study

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

## (TODO) nrf52840 讯联开发板, with j-link, port to ili9341  
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
