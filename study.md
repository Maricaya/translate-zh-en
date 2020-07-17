ts + node 做命令行翻译工具，发布npm上

1. 加密方式
2. 命令行使用
3. 发布 npm

# node 类型文件
yarn add --dev @types/node

# cli 工具
commander.js
yarn add commander

# 不可知验证法
生成方法：
Step1. 将请求参数中的 APPID(appid)， 翻译query(q, 注意为UTF-8编码), 随机数(salt), 以及平台分配的密钥(可在管理控制台查看) 按照 appid+q+salt+密钥 的顺序拼接得到字符串1。
Step2. 对字符串1做md5，得到32位小写的sign。
注：
1. 待翻译文本（q）需为UTF-8编码
2. 在生成签名拼接 appid+q+salt+密钥 字符串时，q不需要做URL encode，在生成签名之后，发送HTTP请求之前才需要对要发送的待翻译文本字段q做URL encode

     q=apple
     from=en
     to=zh
     appid=2015063000000001（请替换为您的appid）
     salt=1435660288（随机码）
     平台分配的密钥: 12345678

# 发布
