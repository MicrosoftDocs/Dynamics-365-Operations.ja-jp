---
title: オンプレミス環境でのプロキシのコンフィギュレーション
description: このトピックでは、プロキシ環境下のオンプレミス環境で Dynamics 365 for Finance and Operations を保護する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: 6f238a45c6e00521adc8748ced47d11133d51afc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537025"
---
# <a name="configure-proxies-for-on-premises-environments"></a>オンプレミス環境でのプロキシのコンフィギュレーション

[!include [banner](../includes/banner.md)]

プロキシ環境下のオンプレミス環境では Dynamics 365 for Finance and Operations を保護することを推奨します。 プロキシとは、クライアントとのデータ通信を行う際に、実際に使っているサーバーを相手側に非表示化するサーバーです。 プロキシ サーバーは、Finance and Operations 環境の代わりにクライアントからの要求を受理し、そのトラフィックを転送します。 クライアントは、Finance and Operations 環境を構成する実際のサーバーを認識していません。 これにより、別のセキュリティ対策が追加され、負荷分散が可能になります。 

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
