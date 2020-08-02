# widora_AIR-R3_Computer Vision
## File
+ kendryte_dvp2lcd-standalone1.14.zip 

  Factory firmware
  
+ kendryte_face-detect-standalone_airvR3.rar

  Modify according to original firmware
+ kendryte_20-classify-detect-standalone_airvR3.rar
  
## Modify Contents
+ GPIO mapping
  use flash editor according to below code in kendryte_dvp2lcd-standalone1.14.zip 
  
  ~~~
   /* Init DVP IO map and function settings */
  fpioa_set_function(42, FUNC_CMOS_RST);
  fpioa_set_function(13, FUNC_CMOS_PWDN);
  fpioa_set_function(46, FUNC_CMOS_XCLK);
  fpioa_set_function(43, FUNC_CMOS_VSYNC);
  fpioa_set_function(45, FUNC_CMOS_HREF);
  fpioa_set_function(47, FUNC_CMOS_PCLK);
  fpioa_set_function(41, FUNC_SCCB_SCLK);
  fpioa_set_function(40, FUNC_SCCB_SDA);

  /* Init SPI IO map and function settings */
  fpioa_set_function(38, FUNC_GPIOHS0 + DCX_GPIONUM);
  fpioa_set_function(37, FUNC_SPI0_SS3);
  fpioa_set_function(39, FUNC_SPI0_SCLK);
  ~~~
+ LCD driver

  copy lcd.h and .c from standalone1.14
  
+ Camera driver
  copy camera.h and .c from standalone1.14
  
## Notes
+ model init error

  Model Setting and Action:  ![avatar](https://github.com/bluejazzCHN/widora_AIR-R3_face-detect/blob/master/kmodel_config.jpg)
  
+ PIN Config

  Camera Pin Setting:  ![avatar](https://github.com/bluejazzCHN/widora_AIR-R3_face-detect/blob/master/DVP_pin_config.jpg)
  
  SPI Pin Setting:  ![avatar](https://github.com/bluejazzCHN/widora_AIR-R3_face-detect/blob/master/SPI_pin_config.jpg)
  
  HSIO Pin Setting:  ![avatar](https://github.com/bluejazzCHN/widora_AIR-R3_face-detect/blob/master/GPIO_pin_config.jpg)

