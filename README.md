# STM32F103_DEV_LEARN32  

STM32例程学习、代码修改  
轮子搜集、使用、说明  
踩坑总结、经验分享  


F103ZET6_USART&FLASH_INPUT_SAVE_OUTPUT.7z：  
描述：红灯闪烁等待输入；输入后开始计时，间隔1秒输出数据，绿灯闪烁；  
踩坑：中断只能接收到一个字符  
原因：函数printf()为阻塞函数，不能在中断中使用  
总结：硬件无法像软件开发一样，用一步步打印说明的方法调试。之后可以通过指示灯的闪烁来当做标志  


F103c8t6_0807_1024byteTRX_ModbusCRC16.zip：  
描述：每秒持续输入1024字节带有CRC16校验的数据，接收，并通过串口打印回来  
踩坑：无法返回、不受控制无限返回、无响应、数据丢失等等  
原因：大数据及其考研硬件速度，CRC需要查表不能用计算，其他地方严禁使用printf函数  
总结：需要一定代码复杂度分析  

