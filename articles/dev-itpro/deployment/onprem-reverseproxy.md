---
title: "オンプレミス環境のリバース プロキシの構成"
description: "このトピックでは、リバース プロキシの背後にあるオンプレミス環境で Dynamics 365 for Finance and Operations を保護する方法について説明します。"
author: sarvanisathish
manager: AnnBe
ms.date: 02/06/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 4bf3291cdfcf7274b1564a6872221994f228c39e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="configure-reverse-proxies-for-on-premises-environments"></a><span data-ttu-id="a3b7b-103">オンプレミス環境のリバース プロキシの構成</span><span class="sxs-lookup"><span data-stu-id="a3b7b-103">Configure reverse proxies for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3b7b-104">リバース プロキシの背後にあるオンプレミス環境で Dynamics 365 for Finance and Operations を保護することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-104">You may want to secure the Dynamics 365 for Finance and Operations on-premises environment behind a reverse proxy.</span></span> <span data-ttu-id="a3b7b-105">リバース プロキシは、クライアントからトラフィックを生成する実際のサーバーを非表示にするサーバーです。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-105">Reverse proxy is a server that hides the actual servers serving traffic from the clients.</span></span> <span data-ttu-id="a3b7b-106">プロキシ サーバーは、Finance and Operations 環境の代わりにクライアントからの要求を受理し、そのトラフィックを転送します。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-106">The proxy server accepts requests from the clients on behalf of the Finance and Operations environment and forwards the traffic to it.</span></span> <span data-ttu-id="a3b7b-107">クライアントは、Finance and Operations 環境を構成する実際のサーバーを認識していません。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-107">The clients are not aware of the actual servers that compose the Finance and Operations environment.</span></span> <span data-ttu-id="a3b7b-108">これにより、別のセキュリティ対策が追加され、負荷分散が可能になります。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-108">This adds another measure of security and enables load balancing.</span></span> 

## <a name="configure-the-reverse-proxy"></a><span data-ttu-id="a3b7b-109">リバース プロキシのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a3b7b-109">Configure the reverse proxy</span></span>

<span data-ttu-id="a3b7b-110">Microsoft Azure Service Fabric クラスターの **OrchestratorType** タイプの**各**ノードで、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-110">Perform the following steps in **each** node of type **OrchestratorType** in the Microsoft Azure Service Fabric cluster.</span></span>

1. <span data-ttu-id="a3b7b-111">リモート アクセスを使用して、オーケストレーター仮想マシン (VM) に接続します。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-111">Use remote access to connect to the Orchestrator virtual machine (VM).</span></span>
2. <span data-ttu-id="a3b7b-112">```machine.config``` ファイルのパスを取得するには、次の PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-112">Execute the following PowerShell script to retrieve the path of the ```machine.config``` file.</span></span>

    ```Powershell
    [System.Runtime.InteropServices.RuntimeEnvironment]::SystemConfigurationFile
    ```

3. <span data-ttu-id="a3b7b-113">```machine.config``` ファイルを編集し、次のコード例を追加します。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-113">Edit the ```machine.config``` file to add the following code example.</span></span>

    ```XML
        <system.net>
            <defaultProxy enabled="true" >
                <proxy <<<SET YOUR PROXY SETTINGS>> />
            </defaultProxy>
        </system.net>
    ```

4. <span data-ttu-id="a3b7b-114">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-114">Save the file.</span></span>
5. <span data-ttu-id="a3b7b-115">仮想マシンを再起動します。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-115">Restart the virtual machine.</span></span>

<span data-ttu-id="a3b7b-116">上記の手順は、すべてのオーケストレータ ノード VM に対して実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3b7b-116">The above procedure must be performed for all Orchestrator node VMs.</span></span> 

