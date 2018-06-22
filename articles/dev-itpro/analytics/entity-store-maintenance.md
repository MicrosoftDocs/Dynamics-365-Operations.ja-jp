---
title: "エンティティ格納のメンテナンス"
description: "このトピックでは、エンティティ ストアのメンテナンス後に完了する必要のある手順について説明します。"
author: sarvanisathish
manager: AnnBe
ms.date: 04/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region:
- Global for most topics. Set Country/Region name for localizations
ms.author: sarvanis
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 008435994a75ff17628a470347bc1ad73e58ff2d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="entity-store-maintenance"></a><span data-ttu-id="918ed-103">エンティティ格納のメンテナンス</span><span class="sxs-lookup"><span data-stu-id="918ed-103">Entity store maintenance</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="918ed-104">エンティティ格納に対してメンテナンスが実行されるとき、それは次のコンポーネントに影響します。</span><span class="sxs-lookup"><span data-stu-id="918ed-104">When maintenance is performed on the entity store, it impacts the following components:</span></span> 

-   <span data-ttu-id="918ed-105">Dynamics 365 for Finance and Operations 7.2 またはそれ以上で、埋め込み分析レポートの分析ワークスペースを構成している場合は、アプリケーション分析ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="918ed-105">Application analytical workspaces, if you are on Dynamics 365 for Finance and Operations 7.2 or higher and have configured analytical workspaces for embedded analytical reports.</span></span>

-   <span data-ttu-id="918ed-106">PowerBI.com に配備されたエンティティ格納ベースのレポート。</span><span class="sxs-lookup"><span data-stu-id="918ed-106">Entity store-based reports that have been deployed to PowerBI.com.</span></span>

<span data-ttu-id="918ed-107">これらのコンポーネントで問題を解決するには、このトピックの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="918ed-107">To resolve issues with these components, complete the procedures in this topic.</span></span>

> [!Note]
> <span data-ttu-id="918ed-108">Dynamics 365 for Finance and Operations instance の通常の操作には**影響はありません**。</span><span class="sxs-lookup"><span data-stu-id="918ed-108">There will be **no impact** to the normal operation of your Dynamics 365 for Finance and Operations instance.</span></span>

## <a name="if-you-are-using-application-analytical-workspaces"></a><span data-ttu-id="918ed-109">アプリケーション分析ワークスペースを使用している場合</span><span class="sxs-lookup"><span data-stu-id="918ed-109">If you are using application analytical workspaces</span></span>

<span data-ttu-id="918ed-110">アプリケーション分析ワークスペースおよびレポートは、特定の保守操作が完了した後データを表示しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="918ed-110">Application analytical workspaces and reports may not render data after certain maintenance operations are completed.</span></span> <span data-ttu-id="918ed-111">次のスクリーン ショットはその例です。</span><span class="sxs-lookup"><span data-stu-id="918ed-111">The following screenshot shows an example of this.</span></span>

![分析レポートは空白](media/blank-powerbi.png)

<span data-ttu-id="918ed-113">この問題を解決するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="918ed-113">To resolve this issue:</span></span>

1. <span data-ttu-id="918ed-114">Dynamics 365 for Finance and Operations にサインインします。</span><span class="sxs-lookup"><span data-stu-id="918ed-114">Sign in to Dynamics 365 for Finance and Operations.</span></span>

2. <span data-ttu-id="918ed-115">**バッチ ジョブ** ページ (**システム管理 > 照会 > バッチ ジョブ**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="918ed-115">Go to the **Batch jobs** page (**System administration > Inquiries > Batch jobs**).</span></span> 
    
3. <span data-ttu-id="918ed-116">エンティティ格納に関連付けられているすべての保留中のバッチ ジョブを削除します。</span><span class="sxs-lookup"><span data-stu-id="918ed-116">Delete all pending batch jobs associated with the entity store.</span></span> <span data-ttu-id="918ed-117">これらのバッチ ジョブには次がふくまれます。</span><span class="sxs-lookup"><span data-stu-id="918ed-117">These batch jobs:</span></span>

- <span data-ttu-id="918ed-118">**待機中** の状態になります。</span><span class="sxs-lookup"><span data-stu-id="918ed-118">Will have a status of **Waiting**.</span></span>
- <span data-ttu-id="918ed-119">通常は **測定の配置** の説明があります。</span><span class="sxs-lookup"><span data-stu-id="918ed-119">Will typically have a description of **Deploy measurement**.</span></span>
    
    > [!Note]
    > <span data-ttu-id="918ed-120">既定の説明は、**測定の配置** です。</span><span class="sxs-lookup"><span data-stu-id="918ed-120">The default description is **Deploy measurement**.</span></span> <span data-ttu-id="918ed-121">説明がカスタマイズされている場合は、クラス名を参照して、バッチ ジョブがエンティティの店舗に関連付けられているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="918ed-121">If the description has been customized, you can verify whether a batch job is associated with the entity store by looking at the class name.</span></span> <span data-ttu-id="918ed-122">エンティティ格納に関連付けられているバッチ ジョブのクラス名は **BIMeasurementDeployManagementEntityBatchJob** になります。</span><span class="sxs-lookup"><span data-stu-id="918ed-122">Batch jobs associated with the entity store will have a class name of **BIMeasurementDeployManagementEntityBatchJob**.</span></span>

4.  <span data-ttu-id="918ed-123">**エンティティ格納**ページ (**システム管理** \> **設定** \> **エンティティ格納**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="918ed-123">Go to the **Entity store** page (**System Administration** \> **Setup** \> **Entity Store**).</span></span>

5.  <span data-ttu-id="918ed-124">更新する必要があるすべてのエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="918ed-124">Select all entities that need to be refreshed.</span></span>

6.  <span data-ttu-id="918ed-125">**更新**をクリックし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="918ed-125">Click **Refresh**, and then click **OK**.</span></span>

<span data-ttu-id="918ed-126">リフレッシュが完了すると、アプリケーション分析ワークスペースおよびレポートはデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="918ed-126">After the refresh completes, the application analytical workspaces and reports will render data.</span></span>

## <a name="if-you-have-deployed-entity-store-based-reports-to-powerbicom-and-are-using-the-reports-within-powerbicom"></a><span data-ttu-id="918ed-127">エンティティ格納ベースのレポートを PowerBI.com に展開し、PowerBI.com 内のレポートを使用している場合</span><span class="sxs-lookup"><span data-stu-id="918ed-127">If you have deployed entity store-based reports to PowerBI.com and are using the reports within PowerBI.com</span></span>

<span data-ttu-id="918ed-128">エンティティ格納 (前述) を更新した後、Finance and Operations の **Power BI レポート ファイルの配置**ぺージを使用してレポートを再配置します (**システム管理** \> **設定** \> **Power BI ファイルの配置**)。</span><span class="sxs-lookup"><span data-stu-id="918ed-128">After refreshing the entity store (as described above), redeploy the reports using the **Deploy Power BI report files** page in Finance and Operations (**System Administration** \> **Setup** \> **Deploy Power BI files**).</span></span>

> [!Note]
> <span data-ttu-id="918ed-129">以前に PowerBI.com に展開されたレポートは、エラーを発生させることがあります。</span><span class="sxs-lookup"><span data-stu-id="918ed-129">Reports that were previously deployed to PowerBI.com may produce errors.</span></span> <span data-ttu-id="918ed-130">これが発生した場合、保守活動が終了したあとにレポートを削除し再配置する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="918ed-130">If this occurs, you may need to delete and redeploy the report after the maintenance activity is completed.</span></span>
