# MLX90614 Library for STM HAL

A MLX90614 library that works for STM32 microcontrollers with HAL library.


## Demonstration

To utilize the library its necessary run its initilize funcion:

```ruby
initMLX90614(&hi2c1, MLX90614_DEFAULT_SA);
```

You can Read and Write from the RAM, EEPROM and other addresses with the functions:

```ruby
uint8_t status1 = MLX90614_WriteReg(MLX90614_PWMCTRL, 0x00FA);
uint16_t read;
uint8_t status2 = MLX90614_WriteReg(MLX90614_PWMCTRL,&read);
```

That is also a function to read temperature as a float:

```ruby
float temp;
uint8_t status = MLX90614_ReadTemp(MLX90614_TOBJ1, &temp);
```