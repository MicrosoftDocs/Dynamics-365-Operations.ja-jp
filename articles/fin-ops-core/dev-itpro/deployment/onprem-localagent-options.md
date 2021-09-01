---
title: ローカル エージェントの配置コンフィギュレーション
description: このトピックでは、ローカル エージェントを配置する際に、環境に関連する特別なコンフィギュレーションを示すために指定できる配置コンフィギュレーションについて説明します。
author: faix
ms.date: 08/03/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-08-03
ms.openlocfilehash: 6753f8955681de6d9d0d12b6d729acf06e535a3f35c49665cd08809b60fc8e17
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719331"
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
                "sqlServerVersion" : {
                    "value": "2016"
                },
                ...
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
