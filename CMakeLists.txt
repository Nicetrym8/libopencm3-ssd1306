cmake_minimum_required(VERSION 3.0)


add_definitions(-DSSD1306_NOSTDLIB)
add_library(ssd1306
  ssd1306.c
  ssd1306.h
  ssd1306_i2c.c
  ssd1306_i2c.c
  fonts.c
  fonts.h
)







