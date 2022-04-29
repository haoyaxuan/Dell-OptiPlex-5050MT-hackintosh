# Dell-OptiPlex-5050
## 电脑配置

| 规格     | 详细信息              |
| -------- |-------------------|
| 电脑型号 | DELL-OptiPlex-5050 |
| 处理器   | 英特尔 酷睿 i5-7500 处理器 |
| 内存     | DDR4 16GB         |
| 硬盘     | 256GB SSD         |
| 集成显卡 | 英特尔图形卡 HD630（无独显） |
| 声卡     | 瑞昱 ALC255         |
| 网卡     | Intel i219V       |

## 正常功能
* 核显正常
* dp输出
* 有线网卡正常
* usb，前面板和主板均正常
* 音频正常


## 说明
* 引导中使用`SSDT-S3-BLOCK.aml`补丁解决睡眠问题，这也意味着电脑在MacOS下只会进入S2睡眠，不会进入S3深度睡眠，S2只会对CPU进行低功耗。
* `hackintool`文件夹包含使用到的工具及acpi的源文件。
* 使用之前补齐`三码`


## BIOS设置
* General → Advanced Boot Options：***取消勾选***
* System Configuration → SATA Operation: ***AHCI***
* System Configuration → Serial Port: ***Disabled***
* Secure Boot → Secure Boot Enable: ***Disabled***
* Power Management → Block Sleep → Block Sleep (S3 state) ***勾选***
* Virtualization Support → VT for Direct I/O: ***取消勾选***


## BIOS设置 For 隐项
* 将EFI-shell文件夹复制到U盘，改名为EFI，然后从U盘启动
* 设置 Pre-Allocated DVMT 为 64M:
  ***setup_var 0x795 0x02***
* 禁用 CFG lock:
  ***setup_var 0x4ed 0x00***

## 镜像下载
- 黑果小兵部落阁 [MacOS Catalina 10.15.6](https://blog.daliansky.net/macOS-Catalina-10.15.6-19G73-Release-version-with-Clover-5119-original-image-Double-EFI-Version-UEFI-and-MBR.html)，感谢 @黑果小兵

## 联系方式
QQ：3129598