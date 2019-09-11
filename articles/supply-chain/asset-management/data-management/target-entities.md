---
title: ターゲット エンティティ
description: このトピックでは、資産管理におけるターゲット エンティティの概要の取得方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/26/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0db7b3dac22380d90b745fd6b2041054d922d72b
ms.sourcegitcommit: e7834191b6eb14f525823075efcc1b1ab2c68463
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2019
ms.locfileid: "1920498"
---
# <a name="target-entities"></a><span data-ttu-id="2d85d-103">ターゲット エンティティ</span><span class="sxs-lookup"><span data-stu-id="2d85d-103">Target entities</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="2d85d-104">**Dynamics 365 for Finance and Operations** > **データ管理**ワークスペースでは、 ターゲット エンティティ、関連するエンティティ タイプ、**資産管理**モジュールに関連するステージング テーブルの概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="2d85d-104">In **Dynamics 365 for Finance and Operations** > **Data management** workspace, you can get an overview of target entities, related entity types and staging tables related to the **Asset management** module.</span></span> 

1. <span data-ttu-id="2d85d-105">画面の左上隅にある **Finance and Operations** ボタンをクリックし、**データ管理**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d85d-105">Click the **Finance and Operations** button in the upper-left corner of the screen, and click **Data management**.</span></span>

2. <span data-ttu-id="2d85d-106">**インポート/エクスポート** セクションで、**データ エンティティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d85d-106">In the **Import / Export** section, click **Data entities**.</span></span> 

![図 1](media/01-data-management.png)

3. <span data-ttu-id="2d85d-108">**ターゲット エンティティ** ページで、フィルターで「資産管理」を検索し、Enter キーを押して、資産管理に関連するエンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="2d85d-108">On the **Target entities** page, search for "asset management" in the filter, and press Enter to see a list of the entities related to Asset management.</span></span>

<span data-ttu-id="2d85d-109">次の図は、資産管理エンティティの一部を示しています。</span><span class="sxs-lookup"><span data-stu-id="2d85d-109">The figure below shows some of the Asset management entities.</span></span>

![図 2](media/02-data-management.png)

4. <span data-ttu-id="2d85d-111">エンティティを選択し、**ターゲット マッピングの変更**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d85d-111">Select an entity and click **Modify target mapping**.</span></span>

5. <span data-ttu-id="2d85d-112">**ステージングをターゲットにマップ** ページに、選択したエンティティに関連するステージング フィールドの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d85d-112">On the **Map staging to target** page, you see a list of the staging fields related to the selected entity.</span></span> <span data-ttu-id="2d85d-113">**マッピングの視覚化**をクリックして、ステージング データとターゲット データがどのように関連しているかの概要をグラフィック表示します。</span><span class="sxs-lookup"><span data-stu-id="2d85d-113">Click **Mapping visualization** to see a graphic overview of how staging data and target data are related.</span></span> 

<span data-ttu-id="2d85d-114">次の図では、資産タイプ エンティティに関連するフィールドの視覚化が示されています。</span><span class="sxs-lookup"><span data-stu-id="2d85d-114">In the figure below, a visualization of the fields related to the asset types entity is shown.</span></span>

![図 3](media/03-data-management.png)

