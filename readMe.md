1.将Openssl安装的bin路径添加到环境变量中
    C:\Program Files\OpenSSL-Win64\bin
    CMD运行:set C:\Program Files\OpenSSL-Win64\bin\openssl.cfg
    重启电脑
2.安装iPhone 配置实用工具导出描述文件[描述:请点击右上角的“安装”按钮，输入密码后完成安装。本APP已经过苹果官方安全认证，请放心安装！]
3.下载SSL证书server.crt保存.pem文件第一组,ca.crt保存.pem文件第二组,server.key保存.key文件
4.将证书和描述文件[4]搞到一个文件夹中运行下面代码
openssl smime -sign -in Baidu.mobileconfig -out app.mobileconfig -signer server.crt -inkey server.key -certfile ca.crt -outform der -nodetach