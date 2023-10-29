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
