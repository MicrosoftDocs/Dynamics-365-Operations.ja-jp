---
title: 複数レベル資産
description: このトピックでは、複数レベル資産の作成および削除する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7609a85f0315ee5cb5fae62d151b271ef5febe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432099"
---
# <a name="multi-level-assets"></a><span data-ttu-id="a5623-103">複数レベル資産</span><span class="sxs-lookup"><span data-stu-id="a5623-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a5623-104">このトピックでは、複数レベル資産の作成および削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a5623-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="a5623-105">階層ツリー構造内で資産および関連する下位資産を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a5623-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="a5623-106">この方法で、資産間の依存関係を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a5623-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="a5623-107">メンテナンス ジョブは、ツリー構造のすべてのレベルに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="a5623-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="a5623-108">統計は、個々のレベルまたはすべての下位資産レベルの合計として作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="a5623-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="a5623-109">**全資産** リストページの (**資産管理** \> **共通** \> **資産** \> **全資産**) で、**資産** 列に階層順に資産が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5623-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="a5623-110">**親** 列には、関連する親が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5623-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="a5623-111">さらに、資産と下位資産が既に作成されている場合は、**関連情報** ウィンドウの **資産ツリー** セクションにツリー構造内の資産が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5623-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="a5623-112">資産の作成方法については、[資産作成](../objects/create-an-object.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5623-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="a5623-113">下位資産を作成するには、**全般** クイック タブにある **親** フィールド内の親資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="a5623-114">資産または資産構造のコピー</span><span class="sxs-lookup"><span data-stu-id="a5623-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="a5623-115">会社に複数の類似した資産構造がある場合は、資産管理のコピー機能を使用してすばやく作成できます。</span><span class="sxs-lookup"><span data-stu-id="a5623-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="a5623-116">**資産管理** \> **共通** \> **資産** \> **全資産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="a5623-117">**全資産** リスト ページで、コピーする資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="a5623-118">たとえば、下位資産を含む資産構造全体をコピーする場合は、親資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="a5623-119">**資産コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-119">Select **Copy asset**.</span></span> <span data-ttu-id="a5623-120">**コピー元** セクションの、**資産** フィールドがリスト ページで選択した資産に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a5623-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="a5623-121">**コピー先** セクションの **資産** フィールドに、新しい資産の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5623-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="a5623-122">作成する資産が既存の資産構造の一部であるべきならば、**親資産** セクションの **資産** フィールドで親 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="a5623-123">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-123">Select **OK**.</span></span> <span data-ttu-id="a5623-124">新しい資産構造は、**全資産** リスト ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5623-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="a5623-125">コピーした資産に関連するすべての資産属性、メンテナンス計画、およびメンテナンス ラウンドは、新しい資産または資産構造に転送されます。</span><span class="sxs-lookup"><span data-stu-id="a5623-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="a5623-126">資産構造をコピーすると、新しい構造内の下位資産の名前は、コピーした下位資産のものと同じになります。</span><span class="sxs-lookup"><span data-stu-id="a5623-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="a5623-127">コピー手順の完了後、資産の名前やその他の設定を簡単に変更できます。</span><span class="sxs-lookup"><span data-stu-id="a5623-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="a5623-128">**全資産** リスト ページで資産を選択し、**編集** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="a5623-129">資産または資産構造をコピーすると、新しい資産のライフサイクル状態は資産の初期ライフサイクル状態として定義した状態にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="a5623-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="a5623-130">機能場所は、既定の機能場所にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="a5623-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="a5623-131">資産または資産構造の削除</span><span class="sxs-lookup"><span data-stu-id="a5623-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="a5623-132">資産に関連する下位資産がある場合は、いずれかの資産にメンテナンス要求、ワーク オーダー ジョブ、エラー登録、または条件評価が登録されていない場合にのみ削除できます。</span><span class="sxs-lookup"><span data-stu-id="a5623-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="a5623-133">**全資産** リスト ページで、削除する資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="a5623-134">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5623-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="a5623-135">この手順を使用して資産を削除できない場合は、削除を処理するもう 1 つの方法として、この目的のために資産ライフサイクル状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="a5623-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="a5623-136">たとえば、**資産ライフサイクル状態** ページの **仕損済** または **削除** でライフサイクル状態を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a5623-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
