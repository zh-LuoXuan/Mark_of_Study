# FreeRTOS

## 编码规则

- $\color{#F00}变量名$
  - 对于`stdint.h`中定义的各种标准类型整数
    - 前缀`c`表示`char`类型变量；
    - 前缀`s`表示`int16_t`(`short`)类型变量；
    - 前缀`l`表示`int32_t`类型变量；
    - 前缀`uc`表示`uint_8`类型变量；
    - 前缀`us`表示`uint16_t`类型变量；
    - 前缀`ul`表示`uint32_t`类型变量；
    - ……
  - `BaseType_t`和所有其他的非标准类型的变量名，如结构体变量、任务句柄、队列句柄等都用前缀`x`。
  - `UBaseType_t`类型的变量使用前缀`ux`。
  - 指针类型变量在前面再增加一个`p`，如`pc`表示`char*`类型。
- $\color{#F00}函数名$
  - 函数名的前缀由返回值类型和函数所在文件组成
    - `xTaskCreate()`，返回值为`BaseType_t`类型，在文件`task.h`中定义；
    - `vQueueDelete()`，返回值为`void`类型，在文件`queue.h`中定义；
    - `pcTimerGetName()`，返回值为`char*`类型，在文件`timer.h`中定义；
    - `pvPortMalloc()`，返回值为`void*`类型，在文件`portable.h`中定义；
    - ……
  - `CMSIS RTOS`相关文件中定义的函数前缀都是`os`，不包括返回值类型和所在文件的前缀。例如，`cmsis os2.h`中的函数`osThreadNew()`。