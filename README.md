# Liunx Navicat 15 premium破解笔记

# 一、相关工具

- navicat15-premium-cs.AppImage：Navicat 15 premium 官方简体中文试用版
- navicat-patcher：补丁
- navicat-keygen ：注册机
- appimagetool-x86_64.AppImage：Linux 独立运行软件打包工具

# 二、系统环境配置

### 安装 capstone



```csharp
sudo apt-get install libcapstone-dev
```

### 安装 keystone



```bash
sudo apt-get install cmake
git clone https://github.com/keystone-engine/keystone.git
cd keystone
mkdir build
cd build
../make-share.sh
sudo make install
sudo ldconfig
```

### 安装 rapidjson



```csharp
sudo apt-get install rapidjson-dev
```

# 三、操作步骤

### 1、赋予执行权限



```css
chmod +x appimagetool-x86_64.AppImage
chmod +x navicat-patcher
chmod +x navicat-keygen
```

### 2、解包官方软件



```css
mkdir navicat15
mount -o loop navicat15-premium-cs.AppImage navicat15
cp -r navicat15 navicat15-patched
sudo chmod -R 777 navicat15-patched/
```

### 3、运行补丁



```shell
./navicat-patcher navicat15-patched/navicat15
```

生成RegPrivateKey.pem文件



```kotlin
**********************************************************
*       Navicat Patcher (Linux) by @DoubleLabyrinth      *
*                  Version: 1.0                          *
**********************************************************
[*] New RSA-2048 private key has been saved to
    ./RegPrivateKey.pem
*******************************************************
*           PATCH HAS BEEN DONE SUCCESSFULLY!         *
*                  HAVE FUN AND ENJOY~                *
*******************************************************
```

### 4、打包成独立运行软件



```shell
./appimagetool-x86_64.AppImage navicat15-patched/navicat15 navicat15-premium-cs-pathed.AppImage

```

### 5、运行补丁后软件包



```shell
chmod +x navicat15-premium-cs-pathed.AppImage
./navicat15-premium-cs-pathed.AppImage
```

### 6、运行注册机



```undefined
./navicat-keygen --text ./RegPrivateKey.pem 
```

选择产品类型： 1 Premium



```kotlin
**********************************************************
*       Navicat Keygen (Linux) by @DoubleLabyrinth       *
*                   Version: 1.0                         *
**********************************************************
[*] Select Navicat product:
 0. DataModeler
 1. Premium
 2. MySQL
 3. PostgreSQL
 4. Oracle
 5. SQLServer
 6. SQLite
 7. MariaDB
 8. MongoDB
 9. ReportViewer
```

选择语言： 1 Simplified Chinese



```csharp
[*] Select product language:
 0. English
 1. Simplified Chinese
 2. Traditional Chinese
 3. Japanese
 4. Polish
 5. Spanish
 6. French
 7. German
 8. Korean
 9. Russian
 10. Portuguese
```

选择版本： 15



```csharp
[*] Input major version number:
(range: 0 ~ 15, default: 12)> 15
```

生成序列号： 填写至软件注册页面，并在断网后选择手工激活



```csharp
[*] Serial number:
NAVE-TOBD-ZLE4-EGEY

```

填写个人信息：



```csharp
[*] Your name: maolei
[*] Your organization: maolei.space

```

输入注册码： 复制软件激活页面注册码并粘贴此处



```csharp
[*] Input request code in Base64: (Double press ENTER to end)
pGdEATZjeOWtGuDh7rX4waf0AA8XN1scuhGa+5bjpwTpAxrV5lxf00J+kulC9OwAVF04zI0k+GoczVxiv95AJERC/ffLq1SThp+QJV0Y0xLxLvTQmTe6RJF6ADvLXAuXL3s8vi7ZqO/Pgc6CstHrnWaI2dNf5D4F/O0dIl3DZuiGbad0A0Mdy6KO9ouxC622F1nDF3tmlV1tlEFdLxhLca9JC5kPzZR12ZWWRGjtfm9+qAZY9VEn8i7CixIlzUPu/Mch1/h4QKGEWHzZ8+zVVqELo6PuH6sTf5RLuy7F3pVFKtlzYy61IVwuA83gJ6AaOHMd1w6kBK5bYLwB1QBSgA==

```

生成激活码： 复制Activation Code内容粘贴至软件激活页面



```csharp
[*] Request Info:
{"K":"NAVETOBDZLE4EGEY", "DI":"2AB5E5F0B9E5907E2CF5", "P":"linux"}

[*] Response Info:
{"K":"NAVETOBDZLE4EGEY","DI":"2AB5E5F0B9E5907E2CF5","N":"maolei","O":"maolei.space","T":1630375125}

[*] Activation Code:
rtQyDtJUl55AWhcgQBm0qw/7diQcxhjVQbEGBml3TpXMqaTAhnbDm8742J3zi0zwJx15rNMSMMC6etXQUZGxj6Jaxbh0rc59X2jmBHsX11ifKP6VwJIszegzFVyDMH553mETOEChLYyoUWY1gi2PIJdjm2iG9vhzA+yYCYVJ5EyUHHJVeUVeF1oUB5DO15NrvYfAKKxOssmLbloUHnpCyJQYD2jTjDdXlTLaJMfsLZmecapzp0n0MD0Zt+YL5qnmPigitQhWf/HslXykhj+T9rZQrYCmCJvpRqXC0FiyfRGoNU9I9SpFY9blPMgj3V1URxiPWNIICct/p/TfW99b2A==

```