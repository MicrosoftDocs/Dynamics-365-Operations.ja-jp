---
title: オンプレミス環境のプロキシの構成
description: この記事では、プロキシ環境下にあるオンプレミス環境を保護する方法について説明します。
author: faix
ms.date: 04/05/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: b3d9366febacad10854479a294e2faef7aecbe12
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739828"
---
# <a name="configure-proxies-for-on-premises-environments"></a>オンプレミス環境のプロキシの構成

[!include [banner](../includes/banner.md)]

組織によっては、追跡またはパケットの検査のために、すべてのサーバー トラフィックがプロキシ サーバーを経由する必要があります。 このセクションでは、これらのケースで推奨される環境を構成する方法について説明します。

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
        <defaultProxy>
            <proxy usesystemdefault="true" proxyaddress="http://<PROXYADDRESS>:<PROXYPORT>" bypassonlocal="true" />
        </defaultProxy>
    </system.net>
    ```

4. ファイル保存します。
5. 仮想マシンを再起動します。

上記の手順は、すべてのオーケストレータ ノード VM に対して実行する必要があります。

## <a name="safe-list-urls"></a>セーフ リストの URL

LocalAgent は Azure リソースおよび Microsoft Dynamics Lifecyle Services (LCS) と通信する必要があります。 その結果、一部の URL をプロキシやファイアウォールでセーフ リストに追加して、全ての **OrchestratorType** ノードがアクセスできるようにする必要があります。 URL は、配置する環境の LCS 地域によって異なります。

### <a name="lcs-global"></a>LCS グローバル

```Text
- lcsapi.lcs.dynamics.com
- login.windows.net
- uswelcs1lcm.queue.core.windows.net
- www.office.com
- login.microsoftonline.com
- dc.services.visualstudio.com
- uswelcs1lcm.blob.core.windows.net
```

### <a name="lcs-eu"></a>LCS ヨーロッパ

```Text
- lcsapi.eu.lcs.dynamics.com
- login.windows.net
- euweprodlcm.queue.core.windows.net
- www.office.com
- login.microsoftonline.com
- dc.services.visualstudio.com
- euweprodlcm.blob.core.windows.net
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
