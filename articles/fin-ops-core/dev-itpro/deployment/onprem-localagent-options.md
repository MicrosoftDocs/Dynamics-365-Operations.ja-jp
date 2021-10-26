---
title: ローカル エージェントの配置コンフィギュレーション
description: このトピックでは、ローカル エージェントを配置する際に、環境に関連する特別なコンフィギュレーションを示すために指定できる配置コンフィギュレーションについて説明します。
author: faix
ms.date: 10/06/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-08-03
ms.openlocfilehash: 847c6d093e43a5cc9fac0b17e07270957b9f418a
ms.sourcegitcommit: 132c3dbdd66bceb7596d329c34b2256c581a20fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/07/2021
ms.locfileid: "7612352"
---
# <a name="deployment-configurations-for-the-local-agent"></a>ローカル エージェントの配置コンフィギュレーション

このトピックでは、ローカル エージェントを配置する際に、環境に関連する特別なコンフィギュレーションを示すために指定できる配置コンフィギュレーションについて説明します。

deploymentOptions のラベルがついた localagent-config.json ファイルにセクションがあります。 これは、ローカル エージェントをインストールする前に変更できます。

```json
    ...
    "deploymentOptions": {
                "office365AdfsCompatibility": {
                    "value": "false"
                },
                "sqlServerVersion": {
                    "value": "2016"
                },
                "isMultiSubnetFailoverEnabled": {
                    "value": "false"
                },
                "skipCRLCheck" : {
                    "value": "false"
                }
            },
    ...
```

## <a name="specify-the-version-of-microsoft-sql-server"></a>Microsoft SQL Server のバージョンの指定

環境のさまざまなコンポーネント全体に Microsoft SQL Server 2019 がインストールされている場合は、**sqlServerVersion** を規定値の 2016 から 2019 に変更します。

互換性のある SQL Server のバージョンの一覧については、[Microsoft Dynamics 365 Finance + Operations (オンプレミス) でサポートされているソフトウェア](./onprem-compatibility.md)を参照してください。

## <a name="specify-that-ad-fs-is-deployed-with-microsoft-365-compatibility"></a>AD FS に Microsoft 365 と互換性のある配置を指定する

Microsoft 365 と互換性のある Active Directory フェデレーション サービス (AD FS) の配置を指定するには、**office365AdfsCompatibility** を **false** から **true** に変更します。

詳細については、[AD FS Microsoft 365 の互換性](./onprem-adfscompatibility.md) を参照してください。

## <a name="specify-that-the-sql-server-cluster-is-deployed-in-multiple-subnets"></a>SQL Server クラスターを複数のサブネットに配置するように指定する

SQL Server クラスターを複数のサブネットに配置するように指定するには、**isMultiSubnetFailoverEnabled** を **false** から **true** に変更します。

この SQL Server コンフィギュレーションの詳細については、[SQL Server の複数のサブネットへのクラスタリング](/sql/sql-server/failover-clusters/windows/sql-server-multi-subnet-clustering-sql-server)を参照してください。

この機能のサポートは、リリース 10.0.19 で導入されました。

## <a name="specify-that-checking-the-certificate-revocation-list-of-a-certificate-should-be-skipped"></a>証明書の証明書失効リストのチェックをスキップするように指定する

クライアントとサーバー間の信頼できる接続を確立する一環として、実行されるチェックの 1 つは、サーバーによって提供された証明書が発行機関によって取り消されていないことをチェックすることです。

これには、FinancialReporting サービスなどのクライアントが証明書失効リストを取得する必要があります。 証明書が公的証明機関によって発行された場合、クライアントは、証明書が取り消されていないことを確認するためにインターネットにアクセスする必要があります。

一部のオンプレミス環境はインターネットへの接続を許可されません。 そのため、このチェックを実行できない場合があります。 **skipCRLCheck** を **false** から **true** に更新することで、このチェックを無効にすることができます。

このオプションのサポートは、バージョン 10.0.21 で導入されました。 また、このオプションを使用するには、少なくともローカル エージェント 2.7.1 が必要です。

> [!IMPORTANT]
> 証明書の失効リストを無効にすると、セキュリティ チェックは実行されません。 このドキュメントを無効にするリスクは、すべてユーザーが負うものとします。 このチェックを無効にすることによるセキュリティへの影響を十分に認識している場合にのみ、この配置オプションを有効にする必要があります。

