---
title: メンテナンス要求レポート
description: このトピックでは、資産管理でメンテナンス要求レポートを作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0734416eccf149330b390cce897d2c254f6c698b
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571625"
---
# <a name="maintenance-request-reports"></a><span data-ttu-id="6231c-103">メンテナンス要求レポート</span><span class="sxs-lookup"><span data-stu-id="6231c-103">Maintenance request reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6231c-104">資産管理では、メンテナンス要求に関連する 2 つのレポートを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="6231c-104">In Asset Management, you can generate two reports that are related to maintenance requests.</span></span> <span data-ttu-id="6231c-105">1 つのレポートには詳細が表示され、もう 1 つのレポートには計画とフォローアップに使用できるリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6231c-105">One report shows details, and the other report provides a list that can be used for planning and follow-up.</span></span>

## <a name="create-a-maintenance-request-details-report"></a><span data-ttu-id="6231c-106">メンテナンス要求の詳細レポートの作成</span><span class="sxs-lookup"><span data-stu-id="6231c-106">Create a Maintenance request details report</span></span>

<span data-ttu-id="6231c-107">**メンテナンス要求の詳細**レポートには、メンテナンス要求に関連するさまざまな情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6231c-107">The **Maintenance request details** report shows various information that is related to maintenance requests.</span></span>

1. <span data-ttu-id="6231c-108">**資産管理**\>**レポート**\>**メンテナンス要求**\>**メンテナンス要求の詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6231c-108">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request details**.</span></span>
2. <span data-ttu-id="6231c-109">**対象に含めるレコード** クイック タブで、レポートに含める特定のメンテナンス要求を選択できます。</span><span class="sxs-lookup"><span data-stu-id="6231c-109">On the **Records to include** FastTab, you can select specific maintenance requests to include on the report.</span></span>
3. <span data-ttu-id="6231c-110">**バックグラウンドで実行**クイック タブでは、必要に応してレポート生成をバッチ ジョブとして設定できます。</span><span class="sxs-lookup"><span data-stu-id="6231c-110">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="6231c-111">**OK** を選択してレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="6231c-111">Select **OK** to generate the report.</span></span>

<span data-ttu-id="6231c-112">次の図は、**メンテナンス要求の詳細**レポートの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6231c-112">The following illustration shows an example of the **Maintenance request details** report.</span></span>

![メンテナンス要求の詳細レポート](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a><span data-ttu-id="6231c-114">メンテナンス要求リストのレポートの作成</span><span class="sxs-lookup"><span data-stu-id="6231c-114">Create a Maintenance request list report</span></span>

<span data-ttu-id="6231c-115">**メンテナンス要求リスト** レポートには、同じ要求タイプのすべてのメンテナンス要求のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6231c-115">The **Maintenance request list** report shows a list of all maintenance requests of the same request type.</span></span>

1. <span data-ttu-id="6231c-116">**資産管理**\>**レポート**\>**メンテナンス要求**\>**メンテナンス要求のリスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6231c-116">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request list**.</span></span>
2. <span data-ttu-id="6231c-117">**対象に含めるレコード** クイック タブで、どのメンテナンス要求をレポートに含めるかを定義するための選択を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6231c-117">On the **Records to include** FastTab, you can make selections to define which maintenance requests are included on the report.</span></span>
3. <span data-ttu-id="6231c-118">**バックグラウンドで実行**クイック タブでは、必要に応してレポート生成をバッチ ジョブとして設定できます。</span><span class="sxs-lookup"><span data-stu-id="6231c-118">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="6231c-119">**OK** を選択してレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="6231c-119">Select **OK** to generate the report.</span></span>

<span data-ttu-id="6231c-120">次の図は、すべての有効なメンテナンス要求に関する**メンテナンス要求リスト** レポートの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6231c-120">The following illustration shows an example of the **Maintenance request list** report for all active maintenance requests.</span></span>

![メンテナンス要求リスト レポート](media/10-manage-maintenance-requests.png)
