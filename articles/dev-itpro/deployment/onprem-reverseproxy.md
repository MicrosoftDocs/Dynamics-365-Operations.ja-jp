---
title: オンプレミス環境のリバース プロキシのコンフィギュレーション
description: このトピックでは、リバース プロキシの背後にあるオンプレミス環境で Dynamics 365 for Finance and Operations を保護する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 02/06/2018
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
ms.openlocfilehash: 4bf3291cdfcf7274b1564a6872221994f228c39e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369484"
---
# <a name="configure-reverse-proxies-for-on-premises-environments"></a>オンプレミス環境のリバース プロキシのコンフィギュレーション

[!include [banner](../includes/banner.md)]

リバース プロキシの背後にあるオンプレミス環境で Dynamics 365 for Finance and Operations を保護することができます。 リバース プロキシは、クライアントからトラフィックを生成する実際のサーバーを非表示にするサーバーです。 プロキシ サーバーは、Finance and Operations 環境の代わりにクライアントからの要求を受理し、そのトラフィックを転送します。 クライアントは、Finance and Operations 環境を構成する実際のサーバーを認識していません。 これにより、別のセキュリティ対策が追加され、負荷分散が可能になります。 

## <a name="configure-the-reverse-proxy"></a>リバース プロキシのコンフィギュレーション

Microsoft Azure Service Fabric Cluster の **OrchestratorType** タイプの **各** ノードで、以下の手順を実行します。

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
