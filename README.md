***
- BUG漫天飞
- MAIKA永相随
***
## 使用方法：
- 使用方法
    - 在docker内执行`apk add python3`
    - 如需扫码获取cookie及获取图片 需执行`apk add zlib-dev gcc jpeg-dev python3-dev musl-dev freetype-dev`
    - 由于需要安装多个依赖包，建议将清华源设置为默认源`pip3 config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple`
    - 执行`pip3 install telethon python-socks[asyncio] pillow qrcode requests prettytable`
    - 或者下载requirements.txt `pip3 install -r requirements.txt`
    - 下载jbot文件夹 放在、/jd或/ql目录下，下载config/bot.json放在config下，在jd或ql目录下运行 `nohup python3 -m jbot >/dev/null 2>&1 &`
***
## 主要实现功能：
- 主要功能
    - /a 使用你的自定义快捷按钮
    - /start 开始使用本程序
    - /help 获取命令，可直接发送至botfather
    - /bash 执行bash程序，如git_pull、diy及可执行自定义.sh，例如/bash /jd/config/abcd.sh
    - /node 执行js脚本文件，目前仅支持/scirpts、/config目录下js，直接输入/node jd_bean_change 即可进行执行。该命令会等待脚本执行完，期间不能使用机器人，建议使用snode命令。
    - /cmd 执行cmd命令,例如/cmd python3 /python/bot.py 则将执行python目录下的bot.py
    - /snode 命令可以选择脚本执行，只能选择/jd/scripts目录下的脚本，选择完后直接后台运行，不影响机器人响应其他命令
    - /log 选择查看执行日志
    - /getfile 获取/jd目录下文件
    - /setshort 设置自定义按钮，每次设置会覆盖原设置
    - /getcookie 扫码获取cookie
    - 此外直接发送文件，会让你选择保存到哪个文件夹，如果选择运行，将保存至scripts或者own目录下，并立即运行脚本crontab.list文件会自动更新时间
