# wmt_smart_watch_study
My smart watch study

## open-watch, port to STM32F103RCT6    
* https://github.com/SMotlaq/open-watch    
* https://github.com/SMotlaq/open-watch/blob/master/open-watch-firmware/my_watch_software/Src/main.c  
* openwatch_v5_run_success.rar  
* jlink报错，需要找SWD针脚是否被占用  
https://zhuanlan.zhihu.com/p/70099066  
* RCC设置晶振  
https://blog.csdn.net/Qxiaofei_/article/details/119006893   
* 定时器开NVIC中断（或update中断）  
* STM32F103RCT6<->OLED12864  
```
STM32F103RCT6<->OLED12864
3.3V(left 2 bottom 1)<->VCC  
GND(left 2 bottom 2)<->GND  
PB6(left 2 bottom 5)<->SCL  
PB7(left 1 bottom 4)<->SDA  
```
