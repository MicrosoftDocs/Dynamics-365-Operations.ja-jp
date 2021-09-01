---
title: オンプレミス環境でのプロキシのコンフィギュレーション
description: このトピックでは、プロキシ環境下にあるオンプレミス環境を保護する方法について説明します。
author: faix
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: fc0febb59368096d8fdf7561f2a501189ca7edc953bdd13dc2c240d0a237e3ef
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712554"
---
# <a name="configure-proxies-for-on-premises-environments"></a>オンプレミス環境でのプロキシのコンフィギュレーション

[!include [banner](../includes/banner.md)]

プロキシの背後にある Dynamics 365 Finance + Operations (オンプレミス) 環境を保護することができます。 プロキシは、クライアントからのトラフィックを処理している実際のサーバーを隠すサーバーです。 プロキシ サーバーは、環境に代わってクライアントからの要求を受理し、そのトラフィックを転送します。 クライアントは、環境を構成する実際のサーバーを認識していません。 これにより、別のセキュリティ対策が追加され、負荷分散が可能になります。 

## <a name="configure-the-proxy"></a>プロキシの設定

Microsoft Azure Service Fabric cluster の **OrchestratorType** の **各** ノードで、以下の手順を実行します。

1. リモート アクセスを使用して、オーケストレーター仮想マシン (VM) に接続します。
2. ```machine.config``` ファイルのパスを取得するには、次の PowerShell スクリプトを実行します。

    ```powershell
    [System.Runtime.InteropServices.RuntimeEnvironment]::SystemConfigurationFile
    ```

3. ```machine.config``` ファイルを編集し、次のコード例を追加します。

    ```xml
    <system.net>
        <defaultProxy enabled="true" >
            <proxy <<<SET YOUR PROXY SETTINGS>> />
        </defaultProxy>
    </system.net>
    ```

4. ファイル保存します。
5. 仮想マシンを再起動します。

上記の手順は、すべてのオーケストレータ ノード VM に対して実行する必要があります。

## <a name="safe-list-urls"></a>セーフ リストの URL

LocalAgent は Azure リソースと通信する必要があります。 結果として、次の URL は プロキシやファイアウォールでセーフ リスト化される必要があます。そうすることで全ての **OrchestratorType** ノードがアクセスすることができます。

```Text
- lcsapi.lcs.dynamics.com
- login.windows.net
- uswelcs1lcm.queue.core.windows.net
- www.office.com
- login.microsoftonline.com
- dc.services.visualstudio.com
- uswelcs1lcm.blob.core.windows.net
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]