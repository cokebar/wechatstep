### 准备工作

- 启用微信运动，打开排行榜，为避免出现问题，建议授予微信运动传感器权限；
- 下载安装Zepp Life（原小米运动），为避免出问题，建议绑定前打开存储、运动传感器权限；
- 使用国内手机号注册并登录Zepp Life，并在第三方数据来源中绑定微信（支付宝等其他app同理）;
- 可以先杀掉微信，然后在Zepp Life中手摇一些步数出来，然后打开微信后看能否同步过去

### 修改配置

- 配置文件(config.json)参数说明：
- ScheduleTime：定时器，每天哪个时间运行，格式"HH:MM"。如果仅运行一次，则留空；
- Tag：为该账户起一个好识别的名称，无实际作用；
- PhoneNum：Zepp Life登录手机号；
- PassWord：Zepp Life密码；
- StepNum：需要刷的步数，格式"XXXXX-YYYYY"，则会在XXXXX-YYYYY之间随机一个数字；格式"XXXXX"，则会固定步数"XXXXX"；
- DeviceId：设备唯一码，程序自动按账户随机生成，无需自行填写。

### 本地运行

- 准备一个python3运行环境，并安装有pip
- 拷贝本程序到任意目录，如/usr/src/app
- 安装依赖：pip install -r requirements.txt
- 执行：python wechatstep.py

### Docker

- 暂时仅为简单说明
- 生成镜像：docker build -t cokebar/wechatstep .
- 复制config.json到宿主机按需编辑，并将其挂载到容器/usr/src/app/config.json

**参考：**
https://blog.csdn.net/Jaeger_Java/article/details/109631118
