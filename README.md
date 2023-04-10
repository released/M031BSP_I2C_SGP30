# M031BSP_I2C_SGP30
 M031BSP_I2C_SGP30

update @ 2023/04/10

1. use I2C0 initial SGP30 (PC1 : SCL , PC0 : SDA) , with I2C interrupt and polling flow (SGP30 is 16bit REGISTER)

check #define ENABLE_I2C_POLLING_DISCRETE , #define ENABLE_I2C_IRQ

2. base on sample code behavior

https://github.com/Sensirion/embedded-sgp/tree/master/sgp30

3. below is sgp30_probe LA capture with REG : 0x202F , 

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/01_sgp30_probe_LA.jpg)	

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/01_sgp30_probe_code.jpg)	

4. below is sgp30_probe LA capture with REG : 0x2003 , 

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/02_sgp30_probe_LA.jpg)	

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/02_sgp30_probe_code.jpg)	

5. below is get_serial_id LA capture with REG : 0x3682 , 

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/03_get_serial_id_LA.jpg)	

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/03_get_serial_id_code.jpg)	

6. below is measure_raw LA capture with REG : 0x2050 , 

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/04_measure_raw_LA.jpg)	

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/04_measure_raw_code.jpg)	

7. below is measure_iaq (regulor polling) LA capture with REG : 0x2008 , 

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/05_measure_iaq_LA.jpg)	

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/05_measure_iaq_code.jpg)	

8. below is log message capture ,

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/log.jpg)	

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/log_regular_polling.jpg)	

9. notice about implement interrupt TX , according to datasheet : Table 10 Measurement commands.  

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/tx.jpg)	

10. notice about implement interrupt RX , according to datasheet : Table 10 Measurement commands.  

![image](https://github.com/released/M031BSP_I2C_SGP30/blob/main/rx.jpg)	

