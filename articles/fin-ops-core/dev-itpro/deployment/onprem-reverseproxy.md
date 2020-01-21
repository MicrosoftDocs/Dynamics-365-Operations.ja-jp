---
title: オンプレミス環境でのプロキシのコンフィギュレーション
description: このトピックでは、プロキシ環境下にあるオンプレミス環境を保護する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 12/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 6d45339f2e0ceca8e7805e70a4a371e1be583335
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914807"
---
# <a name="configure-proxies-for-on-premises-environments"></a>オンプレミス環境でのプロキシのコンフィギュレーション

[!include [banner](../includes/banner.md)]

プロキシの背後にある Dynamics 365 Finance + Operations (オンプレミス) 環境を保護することができます。 プロキシは、クライアントからのトラフィックを処理している実際のサーバーを隠すサーバーです。 プロキシ サーバーは、環境に代わってクライアントからの要求を受理し、そのトラフィックを転送します。 クライアントは、環境を構成する実際のサーバーを認識していません。 これにより、別のセキュリティ対策が追加され、負荷分散が可能になります。 

## <a name="configure-the-proxy"></a>プロキシの設定

Microsoft Azure Service Fabric cluster の **OrchestratorType** の **各** ノードで、以下の手順を実行します。

1. リモート アクセスを使用して、オーケストレーター仮想マシン (VM) に接続します。
2. ```machine.config``` ファイルのパスを取得するには、次の PowerShell スクリプトを実行します。

    ```Powershell
    [System.Runtime.InteropServices.RuntimeEnvironment]::SystemConfigurationFile
    ```

3. ```machine.config``` ファイルを編集し、次のコード例を追加します。

    ```XML
        <system.net>
            <defaultProxy enabled="true" >
                <proxy <<<SET YOUR PROXY SETTINGS>> />
            </defaultProxy>
        </system.net>
    ```

4. ファイル保存します。
5. 仮想マシンを再起動します。

上記の手順は、すべてのオーケストレータ ノード VM に対して実行する必要があります。

## <a name="whitelist-urls"></a>ホワイトリスト URLs

LocalAgent は Azure リソースと通信する必要があります。 結果として、次の URL は プロキシやファイアウォールでホワイトリスト化される必要があり、そうすることで全ての **OrchestratorType** ノードがアクセスすることができます:
```
- lcsapi.lcs.dynamics.com
- login.windows.net
- uswelcs1lcm.queue.core.windows.net
- www.office.com
- login.microsoftonline.com
- dc.services.visualstudio.com
- uswelcs1lcm.blob.core.windows.net
```
