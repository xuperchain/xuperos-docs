
.. _dev:

合约开发说明
------------

智能合约的开发流程如下：

1. 下载 `源代码 <https://github.com/xuperchain/xuperunion>`_，搭建基础开发环境, 目前开放网络使用`v3.4.0`版本，请下载对应的版本源代码并按照XuperUnion开发文档进行编译。

2. 开发合约

    |    1) 创建合约：请参考 `简易开发教程 <https://xuperchain.readthedocs.io/zh/latest/advanced_usage/create_contracts.html>`_
    |    2) 样例
    |        - 样例1： `电子存证合约 <https://xuperchain.readthedocs.io/zh/latest/developing_apps/eleccert.html>`_
    |        - 样例2： `数字资产交易 <https://xuperchain.readthedocs.io/zh/latest/developing_apps/erc721.html>`_

3. 编译合约（部署合约），请参考 `部署wasm合约 <https://xuperchain.readthedocs.io/zh/latest/advanced_usage/create_contracts.html#wasm>`_

4. 最后编译成功的文件上传平台即可

.. _sdk:

SDK使用说明
-----------

为方便GO开发者调试和快速接入百度超级链，将向您介绍Xuper-SDK，并通过简单的示例帮助您快速熟悉Xuper-SDK的使用方法，并构建自己的应用。

1. 开放网络配置
>>>>>>>>>
Go SDK中的开放网络配置位于**conf/sdk.yaml**文件中，具体内容如下：

::

    # EndorseService Info
    # XuperOS addrs
    endorseServiceHost: "39.156.69.83:37100"   
    complianceCheck:
      complianceCheckEndorseServiceFee: 100
      complianceCheckEndorseServiceFeeAddr: aB2hpHnTBDxko3UoP2BpBZRujwhdcAFoT
      complianceCheckEndorseServiceAddr: jknGxa6eyum1JrATWvSJKW3thJ9GKHA9n


其中：

#. **endorseServiceHost** 是开放网络对外暴露的GRPC接口，所有的背书和链上请求都可以通过此接口调用开放网络。
#. **complianceCheck** 是链上数据合规检查的相关配置，其中complianceCheckEndorseServiceFee是指黄反检测所需要的手续费，目前统一为100链上资源，折合0.001余额；complianceCheckEndorseServiceFeeAddr是指黄反检测所需要的手续费接收地址；complianceCheckEndorseServiceAddr是指背书签名的签发地址。

2. 详细使用说明
>>>>>>>>>

更详细的接口文档，请前往 `SDK使用说明与下载地址 <https://github.com/xuperchain/xuper-sdk-go/wiki/xuper-sdk-go-%E4%B8%AD%E6%96%87%E7%89%88>`_ 。




