# 智能数据采集系统

本项目是一个基于ESP8266的智能数据采集系统，能够通过串口接收数据，并通过WebSocket和HTTP接口实时展示和传输数据。

## 功能特性

- 通过串口接收数据包
- 实时计算并记录最大值、最小值和运行次数
- 提供WebSocket接口用于实时数据传输
- 内置Web服务器，提供数据展示页面
- 支持OTA（Over-The-Air）无线更新
- 数据可通过HTTP POST发送到远程服务器

## 硬件要求

- ESP8266开发板（如NodeMCU）
- 串口数据源设备

## 软件依赖

- ESPAsyncWebServer
- AsyncElegantOTA
- ESPAsyncTCP

## 使用说明

1. 修改`main.cpp`中的WiFi配置：
   ```cpp
   const char* ssid = "YOUR_WIFI_SSID";
   const char* password = "YOUR_WIFI_PASSWORD";
   ```
2. 连接ESP8266开发板和串口数据源设备。
3. 编译并上传代码到ESP8266开发板。
4. 打开浏览器，访问ESP8266的IP地址，即可查看数据展示页面。
5. 实时数据将通过WebSocket和HTTP接口传输。
## 注意事项
- 确保ESP8266开发板和串口数据源设备之间的连接正常。
- 确保ESP8266开发板的IP地址正确配置。
- 确保远程服务器的地址和端口正确配置。
- 请根据实际情况修改代码中的WiFi配置和远程服务器地址。   
const char* servername = "http://YOUR_SERVER_IP/data/";

## 项目结构
```IntelligentDataCollection/
├── include/          # 头文件目录
├── lib/              # 私有库目录
├── src/              # 源代码目录
│   └── main.cpp      # 主程序文件
├── test/             # 测试代码目录
└── platformio.ini    # PlatformIO配置文件
```
## 贡献
欢迎贡献代码和改进建议。请在GitHub上提交问题和拉取请求。
## 许可证
本项目使用MIT许可证。请参阅[LICENSE](LICENSE)文件了解更多信息。
