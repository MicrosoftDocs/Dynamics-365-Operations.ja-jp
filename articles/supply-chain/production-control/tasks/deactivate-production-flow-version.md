--- 
title: "生産フロー バージョンの無効化"
description: "有効な生産フロー バージョンが不要になった場合、無効化することができます。"
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 04ed71ab3501be7c9670748d4c7001843ed96c81
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="d8c98-103">生産フロー バージョンの無効化</span><span class="sxs-lookup"><span data-stu-id="d8c98-103">Deactivate a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8c98-104">有効な生産フロー バージョンが不要になった場合、無効化することができます。</span><span class="sxs-lookup"><span data-stu-id="d8c98-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="d8c98-105">すべてのかんばんルールと活動が終了し、今後有効化しない場合にのみ、このオプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8c98-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="d8c98-106">この生産フロー バージョンに関連付けられたすべてのかんばんルールの有効期限は現在の日時に更新されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d8c98-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="d8c98-107">有効な生産フロー バージョンを変更するには、有効なバージョンの有効期限を設定することを検討し、新しいバージョンを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8c98-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="d8c98-108">これにより、新しいバージョンおよび関連するかんばんルールを作成している間、生産の工程を続けることができます。</span><span class="sxs-lookup"><span data-stu-id="d8c98-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="d8c98-109">有効な生産フロー バージョンを期限切れにするには、有効期限を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8c98-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="d8c98-110">その意味で、無効化は、ルールというより、例外というようなものです。</span><span class="sxs-lookup"><span data-stu-id="d8c98-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="d8c98-111">この手順では、無効化することができるバージョンの生産フローが必要です。</span><span class="sxs-lookup"><span data-stu-id="d8c98-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="d8c98-112">バージョンが完全に廃止されていることを 100% 確信しない限り、生産環境にはこれを試みません。</span><span class="sxs-lookup"><span data-stu-id="d8c98-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="d8c98-113">生産フロー バージョンの無効化</span><span class="sxs-lookup"><span data-stu-id="d8c98-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="d8c98-114">[生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8c98-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d8c98-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d8c98-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d8c98-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8c98-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d8c98-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d8c98-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d8c98-118">[無効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8c98-118">Click Deactivate.</span></span>
    * <span data-ttu-id="d8c98-119">この生産フロー バージョンが廃止であると 100% 確信していない限り次の手順に進まないでください。</span><span class="sxs-lookup"><span data-stu-id="d8c98-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="d8c98-120">[OK] をクリックすると、すべての有効なかんばんルールの期限が切れ、この生産フロー バージョンにおけるすべての生産と補充の活動に即時停止が設定されます。</span><span class="sxs-lookup"><span data-stu-id="d8c98-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="d8c98-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8c98-121">Click OK.</span></span>


