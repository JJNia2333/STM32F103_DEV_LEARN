# STM32F103_DEV_LEARN
F103ZET6_USART&FLASH_INPUT/SAVE/OUTPUT.zip：
踩坑：中断只能接收到一个字符
原因：函数printf()为阻塞函数，不能在中断中使用
总结：硬件无法像软件开发一样，用一步步打印说明的方法调试。之后可以通过指示灯的闪烁来当做标志

