# 系统架构说明

## 整体结构

```text
Sensor / Actuator
       |
     STM32
       |
Serial / CAN / TCP
       |
     RK3568
       |
 Local Service / AI / Gateway
       |
  Cloud Server / Database
       |
   Web Dashboard
```

## 模块职责

### STM32

- 采集传感器数据
- 执行电机、继电器、蜂鸣器等控制任务
- 将采集结果按照约定协议上传

### RK3568

- 接收多路下位机数据
- 进行本地缓存、边缘处理与图像识别
- 负责与本地服务器或云端进行数据交互

### Server

- 接收设备上报
- 存储运行状态、任务记录与告警数据
- 向 Web 端提供查询与控制接口

### Web

- 展示设备在线状态
- 展示巡检记录与异常结果
- 提供任务配置、远程控制与信息看板
