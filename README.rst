====
OpenVPN Clients Config to Aliyun DNS Records
====

----
How to install
----
1. 因为AliDNS Python SDK 似乎没有正式发布, 没办法用pip安装, 可从[这里](https://help.aliyun.com/document_detail/dns/sdk/sdk.html)下载
2. 运行 `python setup.py install` 安装SDK
3. 运行 `pip install openvpn2alidns` 安装软件
4. 配置 config.ini

    .. code::
      [alidns]
      accessKey=
      accessSecret=
      regionId=cn-hangzhou
      productName=Alidns
      serviceAddr=alidns.aliyuncs.com
      domainName=genee.cn
      rrSuffix=server

5. 运行 `openvpn2alidns -c path/to/config.ini path/to/openvpn/client.d`
