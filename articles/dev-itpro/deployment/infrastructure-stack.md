---
title: セルフサービス配置
description: このトピックでは、Finance and Operations のセルフ サービス配置の概要を示します。
author: sarvanisathish
manager: AnnBe
ms.date: 12/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: a2399573be036faefe70f9b00754e41d854c7661
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537064"
---
# <a name="self-service-deployment"></a><span data-ttu-id="67026-103">セルフサービス配置</span><span class="sxs-lookup"><span data-stu-id="67026-103">Self-service deployment</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="67026-104">Dynamics 365 for Finance and Operationsクラウド環境では、セルフサービス配置が可能です。</span><span class="sxs-lookup"><span data-stu-id="67026-104">Self-service deployment is available for Dynamics 365 for Finance and Operations cloud environments.</span></span> <span data-ttu-id="67026-105">セルフ サービス配置により、簡単な配置が可能になり配置時間が大幅に減少します。</span><span class="sxs-lookup"><span data-stu-id="67026-105">Self-service deployment enables easier deployment and significantly reduced deployment times.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67026-106">この機能は、Microsoft Azure の国/地域に基づいて段階的にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="67026-106">The functionality for this feature will be released incrementally, based on your Microsoft Azure country/region.</span></span> <span data-ttu-id="67026-107">ただし、この機能は現在、Finance and Operations のサインアップ過程にいる**新しい顧客**のみ利用可能です。</span><span class="sxs-lookup"><span data-stu-id="67026-107">However, this functionality is currently available only for **new customers** who are in the process of signing up for Finance and Operations.</span></span> <span data-ttu-id="67026-108">現在の顧客の既存の環境に変更はありません。</span><span class="sxs-lookup"><span data-stu-id="67026-108">There is no change in existing environments for current customers.</span></span>
>
> <span data-ttu-id="67026-109">すべての新しい顧客にこの機能が表示されるわけではない点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="67026-109">Note that not all new customers will see this functionality.</span></span> <span data-ttu-id="67026-110">ただし、アクセス権を持つ新しい顧客の数は、徐々に増加します。</span><span class="sxs-lookup"><span data-stu-id="67026-110">However, the number of new customers who have access to it will gradually increase.</span></span> 

## <a name="whats-new-or-changed"></a><span data-ttu-id="67026-111">新規または変更</span><span class="sxs-lookup"><span data-stu-id="67026-111">What’s new or changed</span></span>

<span data-ttu-id="67026-112">セルフ サービス機能を使用する顧客は、LCS エクスペリエンスにおいて次の変更が見られます。</span><span class="sxs-lookup"><span data-stu-id="67026-112">Customers using the self-service capabilities will see the following changes in their LCS experience.</span></span> 

- <span data-ttu-id="67026-113">配置はセルフ サービスであり、平均 30 分以内に完了することができます。</span><span class="sxs-lookup"><span data-stu-id="67026-113">Deployment is self-service and can be completed within an average time of 30 minutes.</span></span> <span data-ttu-id="67026-114">配置のリード タイムや待機時間はなくなります。</span><span class="sxs-lookup"><span data-stu-id="67026-114">There are no longer lead times and wait times for deployment.</span></span> <span data-ttu-id="67026-115">いつ配置するかを制御し、環境が展開されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="67026-115">You can control when you deploy, and verify that the environment is deployed.</span></span> <span data-ttu-id="67026-116">このエクスペリエンスは、現在のエクスペリエンスと同じです。</span><span class="sxs-lookup"><span data-stu-id="67026-116">This experience is the same as the current experience.</span></span> <span data-ttu-id="67026-117">詳細については、[配置に関するよく寄せられる質問](deploymentFAQ.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67026-117">For more information, see [Deployment FAQ](deploymentFAQ.md).</span></span>

   ![配置設定](media/deployment-settings.png)

- <span data-ttu-id="67026-119">レベル 2 以上のサンドボックス環境へのリモート デスクトップ アクセスがなくなります。</span><span class="sxs-lookup"><span data-stu-id="67026-119">You will no longer have remote desktop access to the Tier 2+ sandbox environments.</span></span> <span data-ttu-id="67026-120">リモート デスクトップ アクセスが必要なすべての操作は、セルフ サービス アクションとして使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="67026-120">All operations that need remote desktop access are now available as self-service actions.</span></span> <span data-ttu-id="67026-121">次の図に、環境の **メンテナンス** \> **データベース メニュー オプションの移動** における操作の一部を示します。</span><span class="sxs-lookup"><span data-stu-id="67026-121">The following image shows some of the operations in the environment’s **Maintain** \> **Move database menu option**.</span></span> <span data-ttu-id="67026-122">詳細については、[配置のメンテナンス操作](maintenanceoperationsguide-newinfrastructure.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67026-122">For more information, see [Maintenance operations for deployments](maintenanceoperationsguide-newinfrastructure.md).</span></span>

> <span data-ttu-id="67026-123">[重要] リモート デスクトップ アクセスは、セルフ サービス展開を使用して配置された環境にのみ制限されます。</span><span class="sxs-lookup"><span data-stu-id="67026-123">[IMPORTANT] Remote desktop access will be restricted only to environments deployed using the self-service deployment.</span></span> <span data-ttu-id="67026-124">既存の環境または既存の顧客に変更はありません。</span><span class="sxs-lookup"><span data-stu-id="67026-124">There is no change to existing environments or existing customers.</span></span> 

   ![セルフ サービス アクション](media/Self-service-actions.png)

- <span data-ttu-id="67026-126">診断機能は、同じままです。リモート デスクトップ アクセスなしでトラブルシューティングが可能になります。</span><span class="sxs-lookup"><span data-stu-id="67026-126">The diagnostics capabilities will remain the same, which enables troubleshooting without remote desktop access.</span></span> <span data-ttu-id="67026-127">詳細については、[セルフサービス配置で配置された環境のトラブルシューティング](troubleshoot-newinfrastructure.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67026-127">For more information, see [Troubleshoot environments deployed through self-service deployment](troubleshoot-newinfrastructure.md).</span></span> 

   ![環境の監視](media/environment-monitoring.png)

- <span data-ttu-id="67026-129">レベル 2 以上では SQL Server アクセスはありません。</span><span class="sxs-lookup"><span data-stu-id="67026-129">You will not have SQL Server access on Tier 2+.</span></span> <span data-ttu-id="67026-130">Just-In-Time アクセスを使用して SQL データベース アクセスすることは引き続きできます。</span><span class="sxs-lookup"><span data-stu-id="67026-130">You will continue to have SQL database access using just-in-time access.</span></span>

- <span data-ttu-id="67026-131">カスタマイズのための結合された配置可能パッケージを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67026-131">You will need to provide a combined deployable package for customizations.</span></span> <span data-ttu-id="67026-132">つまり、ISV パッケージを含む、すべてのカスタム拡張機能パッケージは、1 つのソフトウェア配置可能パッケージとして配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67026-132">That is, all custom extension packages, including ISV packages, must be deployed as a single software deployable package.</span></span> <span data-ttu-id="67026-133">一度に 1 つのモジュールを配置することはできません。</span><span class="sxs-lookup"><span data-stu-id="67026-133">You will not be able to deploy one module at a time.</span></span> <span data-ttu-id="67026-134">これは常に推奨されるベスト プラクティスであり、適用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="67026-134">This was always a recommended best practice and is now enforced.</span></span>
