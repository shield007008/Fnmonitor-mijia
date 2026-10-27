在作者：**Misite齊** · 贡献者：**[iqiuzixuan](https://github.com/iqiuzixuan)**（新界面、虚拟机、安全加固、回归测试）基础上添加直接读取米家插座功率回报支持
在 server.py 新增统一读取函数`_xiaomi_read_power()` ， 两种协议自动兼容 ：
1. 先走老协议`get_prop` （chuangmi.plug / powerstrip 等老设备直接命中）
2. 失败则回退 miot`get_properties` （按 siid/piid 定位：功率 11/2、开关 2/1、温度 12/2）
