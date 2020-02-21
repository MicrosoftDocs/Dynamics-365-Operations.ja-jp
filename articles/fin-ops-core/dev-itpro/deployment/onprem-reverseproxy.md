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
ms.openlocfilehash: 1979eac8805dff49934025fcd6b2fccdd67c013a
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029425"
---
# <a name="configure-proxies-for-on-premises-environments"></a><span data-ttu-id="f81b1-103">オンプレミス環境でのプロキシのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f81b1-103">Configure proxies for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f81b1-104">プロキシの背後にある Dynamics 365 Finance + Operations (オンプレミス) 環境を保護することができます。</span><span class="sxs-lookup"><span data-stu-id="f81b1-104">You may want to secure the Dynamics 365 Finance + Operations (on-premises) environment behind a proxy.</span></span> <span data-ttu-id="f81b1-105">プロキシは、クライアントからのトラフィックを処理している実際のサーバーを隠すサーバーです。</span><span class="sxs-lookup"><span data-stu-id="f81b1-105">Proxy is a server that hides the actual servers that are serving traffic from the clients.</span></span> <span data-ttu-id="f81b1-106">プロキシ サーバーは、環境に代わってクライアントからの要求を受理し、そのトラフィックを転送します。</span><span class="sxs-lookup"><span data-stu-id="f81b1-106">The proxy server accepts requests from the clients on behalf of the environment and forwards the traffic to it.</span></span> <span data-ttu-id="f81b1-107">クライアントは、環境を構成する実際のサーバーを認識していません。</span><span class="sxs-lookup"><span data-stu-id="f81b1-107">The clients are not aware of the actual servers that compose the environment.</span></span> <span data-ttu-id="f81b1-108">これにより、別のセキュリティ対策が追加され、負荷分散が可能になります。</span><span class="sxs-lookup"><span data-stu-id="f81b1-108">This adds another measure of security and enables load balancing.</span></span> 

## <a name="configure-the-proxy"></a><span data-ttu-id="f81b1-109">プロキシの設定</span><span class="sxs-lookup"><span data-stu-id="f81b1-109">Configure the proxy</span></span>

<span data-ttu-id="f81b1-110">Microsoft Azure Service Fabric cluster の **OrchestratorType** の **各** ノードで、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f81b1-110">Perform the following steps in **each** node of type **OrchestratorType** in the Microsoft Azure Service Fabric cluster.</span></span>

1. <span data-ttu-id="f81b1-111">リモート アクセスを使用して、オーケストレーター仮想マシン (VM) に接続します。</span><span class="sxs-lookup"><span data-stu-id="f81b1-111">Use remote access to connect to the Orchestrator virtual machine (VM).</span></span>
2. <span data-ttu-id="f81b1-112">```machine.config``` ファイルのパスを取得するには、次の PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="f81b1-112">Execute the following PowerShell script to retrieve the path of the ```machine.config``` file.</span></span>

    ```powershell
    [System.Runtime.InteropServices.RuntimeEnvironment]::SystemConfigurationFile
    ```

3. <span data-ttu-id="f81b1-113">```machine.config``` ファイルを編集し、次のコード例を追加します。</span><span class="sxs-lookup"><span data-stu-id="f81b1-113">Edit the ```machine.config``` file to add the following code example.</span></span>

    ```xml
    <system.net>
        <defaultProxy enabled="true" >
            <proxy <<<SET YOUR PROXY SETTINGS>> />
        </defaultProxy>
    </system.net>
    ```

4. <span data-ttu-id="f81b1-114">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="f81b1-114">Save the file.</span></span>
5. <span data-ttu-id="f81b1-115">仮想マシンを再起動します。</span><span class="sxs-lookup"><span data-stu-id="f81b1-115">Restart the virtual machine.</span></span>

<span data-ttu-id="f81b1-116">上記の手順は、すべてのオーケストレータ ノード VM に対して実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f81b1-116">The above procedure must be performed for all Orchestrator node VMs.</span></span>

## <a name="whitelist-urls"></a><span data-ttu-id="f81b1-117">ホワイトリスト URLs</span><span class="sxs-lookup"><span data-stu-id="f81b1-117">Whitelist URLs</span></span>

<span data-ttu-id="f81b1-118">LocalAgent は Azure リソースと通信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f81b1-118">The LocalAgent needs to communicate with Azure resources.</span></span> <span data-ttu-id="f81b1-119">結果として、次の URL は プロキシやファイアウォールでホワイトリスト化される必要があり、そうすることで全ての **OrchestratorType** ノードがアクセスすることができます:</span><span class="sxs-lookup"><span data-stu-id="f81b1-119">As a result, the following URLs should be whitelisted on the proxy or firewalls so that all **OrchestratorType** nodes can access them:</span></span>

```Text
- lcsapi.lcs.dynamics.com
- login.windows.net
- uswelcs1lcm.queue.core.windows.net
- www.office.com
- login.microsoftonline.com
- dc.services.visualstudio.com
- uswelcs1lcm.blob.core.windows.net
```
