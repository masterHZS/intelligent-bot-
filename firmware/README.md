# Firmware 模块

本目录用于存放 `STM32` 下位机程序。

## 建议内容

- `stm32_core/`：主控逻辑、任务调度、状态机
- `drivers/`：GPIO、USART、TIM、PWM、ADC 等基础驱动
- `sensors/`：具体传感器驱动与数据处理
- `communication/`：串口、CAN、RS485、协议封装与解析

## 当前目标

- 建立基础工程
- 打通传感器采集链路
- 完成与 RK3568 的数据通信
