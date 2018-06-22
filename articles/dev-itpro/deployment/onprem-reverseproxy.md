---
title: "オンプレミス環境のリバース プロキシのコンフィギュレーション"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: bd6ba94cf116ad1bdeb8cc35c4e3bfb9ce13b13f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="configure-reverse-proxy-for-your-on-premises-environment"></a><span data-ttu-id="34d95-103">オンプレミス環境のリバース プロキシのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="34d95-103">Configure reverse proxy for your on-premises environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34d95-104">リバース プロキシの背後にあるオンプレミス環境で Dynamics 365 for Finance and Operations を保護することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="34d95-104">You may want to secure the Dynamics 365 for Finance and Operations on-premises environment behind a reverse proxy.</span></span> <span data-ttu-id="34d95-105">リバース プロキシは、クライアントからトラフィックを生成する実際のサーバーを非表示にするサーバーです。</span><span class="sxs-lookup"><span data-stu-id="34d95-105">Reverse proxy is a server that hides the actual servers serving traffic from the clients.</span></span> <span data-ttu-id="34d95-106">プロキシ サーバーは、Finance and Operations 環境の代わりにクライアントからの要求を受理し、そのトラフィックを転送します。</span><span class="sxs-lookup"><span data-stu-id="34d95-106">The proxy server accepts requests from the clients on behalf of the Finance and Operations environment and forwards the traffic to it.</span></span> <span data-ttu-id="34d95-107">クライアントは、Finance and Operations 環境を構成する実際のサーバーを認識していません。</span><span class="sxs-lookup"><span data-stu-id="34d95-107">The clients are not aware of the actual servers that compose the Finance and Operations environment.</span></span> <span data-ttu-id="34d95-108">これにより、別のセキュリティ対策が追加され、負荷分散が可能になります。</span><span class="sxs-lookup"><span data-stu-id="34d95-108">This adds another measure of security and enables load balancing.</span></span> 

## <a name="configure-the-reverse-proxy"></a><span data-ttu-id="34d95-109">リバース プロキシのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="34d95-109">Configure the reverse proxy</span></span>

<span data-ttu-id="34d95-110">Microsoft Azure Service Fabric クラスターの **OrchestratorType** タイプの**各**ノードで、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34d95-110">Perform the following steps in **each** node of type **OrchestratorType** in the Microsoft Azure Service Fabric cluster.</span></span>

1. <span data-ttu-id="34d95-111">リモート アクセスを使用して、オーケストレーター仮想マシン (VM) に接続します。</span><span class="sxs-lookup"><span data-stu-id="34d95-111">Use remote access to connect to the Orchestrator virtual machine (VM).</span></span>
2. <span data-ttu-id="34d95-112">```machine.config``` ファイルのパスを取得するには、次の PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="34d95-112">Execute the following PowerShell script to retrieve the path of the ```machine.config``` file.</span></span>

    ```Powershell
    [System.Runtime.InteropServices.RuntimeEnvironment]::SystemConfigurationFile
    ```

3. <span data-ttu-id="34d95-113">```machine.config``` ファイルを編集し、次のコード例を追加します。</span><span class="sxs-lookup"><span data-stu-id="34d95-113">Edit the ```machine.config``` file to add the following code example.</span></span>

    ```XML
        <system.net>
            <defaultProxy enabled="true" >
                <proxy <<<SET YOUR PROXY SETTINGS>> />
            </defaultProxy>
        </system.net>
    ```

4. <span data-ttu-id="34d95-114">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="34d95-114">Save the file.</span></span>
5. <span data-ttu-id="34d95-115">仮想マシンを再起動します。</span><span class="sxs-lookup"><span data-stu-id="34d95-115">Restart the virtual machine.</span></span>

<span data-ttu-id="34d95-116">上記の手順は、すべてのオーケストレータ ノード VM に対して実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34d95-116">The above procedure must be performed for all Orchestrator node VMs.</span></span> 

