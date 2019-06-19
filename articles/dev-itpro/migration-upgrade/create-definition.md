---
title: AX 2009 の移行 － 移行グループの作成
description: このトピックでは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations にアップグレードするために移行グループを作成する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 09/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 7d75f46e996314d30f1c5a450cfcbc86fd8ba79e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557996"
---
# <a name="ax-2009-migration--create-migration-groups"></a><span data-ttu-id="5b9a1-103">AX 2009 の移行 – 移行グループの作成</span><span class="sxs-lookup"><span data-stu-id="5b9a1-103">AX 2009 migration – Create migration groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b9a1-104">移行の定義を作成するときは、パッケージ化してまとめてエクスポートするエンティティを決定し、すべてのエンティティを移行グループにまとめて配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-104">When you create a definition for migration, you determine which entities should be packaged and exported together, and then put all the entities together in a migration group.</span></span> <span data-ttu-id="5b9a1-105">移行グループは、順番に処理する必要があるか、論理的にグループ化できる一連のエンティティです。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-105">A migration group is a set of entities that must be processed in a sequence, or that can logically be grouped together.</span></span> <span data-ttu-id="5b9a1-106">移行グループのエンティティは、ソースからステージングまたはファイル パッケージに直接まとめてエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-106">The entities in a migration group are exported together, either from the source to staging or directly to a file package.</span></span> <span data-ttu-id="5b9a1-107">移行グループでは、法人を関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-107">In a migration group, you also associate legal entities.</span></span> <span data-ttu-id="5b9a1-108">エクスポート プロセスを開始する前に、移行グループを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-108">Migration groups must be set up before you begin the export process.</span></span>

<span data-ttu-id="5b9a1-109">移行グループを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-109">Follow these steps to create a migration group.</span></span>

1. <span data-ttu-id="5b9a1-110">Microsoft Dynamics AX 2009 のナビゲーション ウィンドウで、**データ移行** \> **共通フォーム** \> **移行グループの作成** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-110">In Microsoft Dynamics AX 2009, in the navigation pane, click **Data Migration** \> **Common forms** \> **Create migration group**.</span></span>
2. <span data-ttu-id="5b9a1-111">**移行グループ** フォームで、CTRL+N を押すか **新規** をクリックして、新しい移行グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-111">In the **Migration group** form, press CTRL+N or click **New** to create a new migration group.</span></span>
3. <span data-ttu-id="5b9a1-112">移行グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-112">Enter a name for the migration group.</span></span> <span data-ttu-id="5b9a1-113">その後に、Tab キーを押して **会社** フィールドに移動し、**会社の選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-113">Then press Tab to move to the **Company** field, and click **Select company**.</span></span>
4. <span data-ttu-id="5b9a1-114">**会社コードの選択** フォームで、移行グループに追加する 1 つまたは複数の会社を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-114">In the **Select company accounts** form, select one or more companies to add to the migration group, and then click **OK**.</span></span>
5. <span data-ttu-id="5b9a1-115">**移行グループ** フォームで、**エンティティ** をクリックし、移行に含める行を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-115">In the **Migration group** form, click **Entity**, and select the lines to include in the migration.</span></span>
6. <span data-ttu-id="5b9a1-116">必要に応じて、フィールド マッピングの空白を埋めます。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-116">Fill in any gaps in the field mapping, as required.</span></span>
7. <span data-ttu-id="5b9a1-117">**順序の適用** をクリックしてフォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b9a1-117">Click **Apply sequence**, and then close the form.</span></span>
