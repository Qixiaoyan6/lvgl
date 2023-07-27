# 如何驱动WT32-KXB-1.54

该实例基于esp-iot-solution中的lvgl_example修改而来，其中的软件配置已经完全适配该屏，只需要下载编译即可


### 如何使用该示例

软件需求：该示例是在esp-idf_v4.4的基础上修改而来，所以您需要安装esp-idf_v4.4环境。


硬件需求：您需要一个串口烧录板，推荐ESP_T02串口烧录板，该串口烧录板也是基于该屏适
配，通过烧录板供电下载，如下图示例：
![image-20230727100222069](C:\Users\34088\AppData\Roaming\Typora\typora-user-images\image-20230727100222069.png)

### 编译和下载

编译工程并将其下载开发板，然后运行串口监视工具来查看串口输出：

运行 **idf.py -p PORT flash monitor** 以编译、下载和监视项目。
（需要退出串口监视器，请输入**ctrl+]**）

### 示例输出

如果示例下载成功，则串口监视器输出：

```c
I (26) boot: ESP-IDF v4.4.5-104-g8b94183c9c-dirty 2nd stage bootloader
I (26) boot: compile time 10:07:12
I (27) boot: chip revision: v1.0
I (31) boot.esp32: SPI Speed      : 40MHz
I (36) boot.esp32: SPI Mode       : DIO
I (41) boot.esp32: SPI Flash Size : 4MB
I (45) boot: Enabling RNG early entropy source...
I (50) boot: Partition Table:
I (54) boot: ## Label            Usage          Type ST Offset   Length
I (61) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (69) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (76) boot:  2 factory          factory app      00 00 00010000 00200000
I (84) boot: End of partition table
I (88) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=24690h (149136) map
I (150) esp_image: segment 1: paddr=000346b8 vaddr=3ffb0000 size=01c48h (  7240) load
I (154) esp_image: segment 2: paddr=00036308 vaddr=40080000 size=09d10h ( 40208) load
I (173) esp_image: segment 3: paddr=00040020 vaddr=400d0020 size=3e4a0h (255136) map
I (265) esp_image: segment 4: paddr=0007e4c8 vaddr=40089d10 size=03d9ch ( 15772) load
I (279) boot: Loaded app from partition at offset 0x10000
I (279) boot: Disabling RNG early entropy source...
I (290) cpu_start: Pro cpu up.
I (290) cpu_start: Single core mode
I (299) cpu_start: Pro cpu start user code
I (299) cpu_start: cpu freq: 160000000
I (299) cpu_start: Application information:
I (303) cpu_start: Project name:     lvgl_example
I (309) cpu_start: App version:      1
I (313) cpu_start: Compile time:     Jul 27 2023 10:06:43
I (319) cpu_start: ELF file SHA256:  41519662e2bdd3f1...
I (325) cpu_start: ESP-IDF:          v4.4.5-104-g8b94183c9c-dirty
I (332) cpu_start: Min chip rev:     v0.0
I (337) cpu_start: Max chip rev:     v3.99
I (341) cpu_start: Chip rev:         v1.0
I (346) heap_init: Initializing. RAM available for dynamic allocation:
I (354) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (359) heap_init: At 3FFB2B70 len 0002D490 (181 KiB): DRAM
I (366) heap_init: At 3FF
```

