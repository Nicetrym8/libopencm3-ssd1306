# libopencm3-ssd1306
Simple ssd1306 monochrome display library for libopencm3. 

Based on https://github.com/SL-RU/stm32libs/tree/master/stm32f10x/ssd1306

**CURRENTLY SUPPORTS ONLY I2C VERSION!!!**

## Supported platforms
| Platform | Tested |
|----------|:------:|
| STM32F1  | :heavy_check_mark: |
| STM32F2  | :x:    |
## Usage
Link to your project (via cmake or whatever you are using). Define platform specific if not defined.
```c
#include <libopencm3-ssd1306/ssd1306.h>
//... some periphery inits
int main() {
 // ...
  ssd1306_init();
  ssd1306_fill(SSD1306_COLOR_BLACK);
  ssd1306_puts("Test", &Font_11x18, SSD1306_COLOR_WHITE);
  ssd1306_update_screen();
 // ...
}

```
## Compiler Defines
| Name | Default value | Description |
| ---- | ------------- | ----------- |
| STM32F1 | undefined  | Platform specific definition |
| STM32F2 | undefined  | Platform specific definition |
| SSD1306_NOSTDLIB | defined(in CMakeLists.txt) | If defined replaces all stdlib calls with its own |
| SSD1306_I2C | I2C2 | LCD I2C port |
| SSD1306_I2C_ADDR | 60 | LCD I2C slave address |
| SSD1306_I2C_TIMEOUT | 1000 | Countdown before timeout |
| SSD1306_WIDTH | 128 | LCD width in pixels |
| SSD1306_HEIGHT | 64 | LCD height in pixels |



## Contributing

1. Create an issue and describe your idea
2. Fork it
3. Create your feature branch (`git checkout -b my-new-feature`)
4. Commit your changes (`git commit -am 'Add some feature'`)
5. Publish the branch (`git push origin my-new-feature`)
6. Create a new pull request
