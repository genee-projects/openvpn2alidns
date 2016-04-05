# OpenVPN 客户配置转换到阿里云解析DNS记录

## 如何安装
1. 运行 `pip install openvpn2alidns` 安装软件
2. 配置 config.ini

    ```ini
      [alidns]
      accessKey=
      accessSecret=
      regionId=cn-hangzhou
      productName=Alidns
      serviceAddr=alidns.aliyuncs.com
      domainName=genee.cn
      rrSuffix=server
    ```
3. 如果希望使用最新的AliDNS Python SDK, 可从[这里](https://help.aliyun.com/document_detail/dns/sdk/sdk.html)查看下载安装

## 如何使用
1. 运行 `openvpn2alidns -c path/to/config.ini path/to/openvpn/client.d`
