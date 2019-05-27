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
# <a name="configure-proxies-for-on-premises-environments"></a><span data-ttu-id="02022-103">オンプレミス環境でのプロキシのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="02022-103">Configure proxies for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02022-104">プロキシ環境下のオンプレミス環境では Dynamics 365 for Finance and Operations を保護することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="02022-104">You may want to secure the Dynamics 365 for Finance and Operations on-premises environment behind a proxy.</span></span> <span data-ttu-id="02022-105">プロキシとは、クライアントとのデータ通信を行う際に、実際に使っているサーバーを相手側に非表示化するサーバーです。</span><span class="sxs-lookup"><span data-stu-id="02022-105">Proxy is a server that hides the actual servers serving traffic from the clients.</span></span> <span data-ttu-id="02022-106">プロキシ サーバーは、Finance and Operations 環境の代わりにクライアントからの要求を受理し、そのトラフィックを転送します。</span><span class="sxs-lookup"><span data-stu-id="02022-106">The proxy server accepts requests from the clients on behalf of the Finance and Operations environment and forwards the traffic to it.</span></span> <span data-ttu-id="02022-107">クライアントは、Finance and Operations 環境を構成する実際のサーバーを認識していません。</span><span class="sxs-lookup"><span data-stu-id="02022-107">The clients are not aware of the actual servers that compose the Finance and Operations environment.</span></span> <span data-ttu-id="02022-108">これにより、別のセキュリティ対策が追加され、負荷分散が可能になります。</span><span class="sxs-lookup"><span data-stu-id="02022-108">This adds another measure of security and enables load balancing.</span></span> 

## <a name="configure-the-proxy"></a><span data-ttu-id="02022-109">プロキシの設定</span><span class="sxs-lookup"><span data-stu-id="02022-109">Configure the proxy</span></span>

<span data-ttu-id="02022-110">Microsoft Azure Service Fabric cluster の **OrchestratorType** の **各** ノードで、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="02022-110">Perform the following steps in **each** node of type **OrchestratorType** in the Microsoft Azure Service Fabric cluster.</span></span>

1. <span data-ttu-id="02022-111">リモート アクセスを使用して、オーケストレーター仮想マシン (VM) に接続します。</span><span class="sxs-lookup"><span data-stu-id="02022-111">Use remote access to connect to the Orchestrator virtual machine (VM).</span></span>
2. <span data-ttu-id="02022-112">```machine.config``` ファイルのパスを取得するには、次の PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="02022-112">Execute the following PowerShell script to retrieve the path of the ```machine.config``` file.</span></span>

    ```Powershell
    [System.Runtime.InteropServices.RuntimeEnvironment]::SystemConfigurationFile
    ```

3. <span data-ttu-id="02022-113">```machine.config``` ファイルを編集し、次のコード例を追加します。</span><span class="sxs-lookup"><span data-stu-id="02022-113">Edit the ```machine.config``` file to add the following code example.</span></span>

    ```XML
        <system.net>
            <defaultProxy enabled="true" >
                <proxy <<<SET YOUR PROXY SETTINGS>> />
            </defaultProxy>
        </system.net>
    ```

4. <span data-ttu-id="02022-114">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="02022-114">Save the file.</span></span>
5. <span data-ttu-id="02022-115">仮想マシンを再起動します。</span><span class="sxs-lookup"><span data-stu-id="02022-115">Restart the virtual machine.</span></span>

<span data-ttu-id="02022-116">上記の手順は、すべてのオーケストレータ ノード VM に対して実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02022-116">The above procedure must be performed for all Orchestrator node VMs.</span></span> 
