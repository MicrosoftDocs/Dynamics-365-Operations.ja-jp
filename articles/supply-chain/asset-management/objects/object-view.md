---
title: 資産表示
description: このトピックでは、資産管理の資産表示について説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0256cc86dc306c8addb37d2c8f335470b19177a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019407"
---
# <a name="asset-view"></a><span data-ttu-id="9da0c-103">資産表示</span><span class="sxs-lookup"><span data-stu-id="9da0c-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9da0c-104">このトピックでは、資産管理の資産表示について説明します。</span><span class="sxs-lookup"><span data-stu-id="9da0c-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="9da0c-105">**資産表示** ページには、ツリー ビューに有効な資産と機能的な場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9da0c-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="9da0c-106">したがって、機能的な場所への資産関係の概要を簡単に取得できます。</span><span class="sxs-lookup"><span data-stu-id="9da0c-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="9da0c-107">さらに、機能的な場所、資産、および関連する部品表 (BOMs) に関する詳細情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="9da0c-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="9da0c-108">また、資産に関連する有効なメンテナンス要求とワーク オーダーの概要をすばやく取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="9da0c-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="9da0c-109">**資産管理** \> **共通** \> **資産** \> **資産表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9da0c-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="9da0c-110">ページに表示されるビューを変更するには、**表示** フィールドで新しい値を選択します。</span><span class="sxs-lookup"><span data-stu-id="9da0c-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9da0c-111">**資産表示** ページを開いたときに表示される既定のビューは、**資産管理パラメーター** ページの **資産** タブの **表示** フィールドで選択した値によって異なります。 (**資産管理** \> **設定** \> **資産管理パラメーター**)。</span><span class="sxs-lookup"><span data-stu-id="9da0c-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="9da0c-112">ページの右側に、クイック タブは選択したビューの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="9da0c-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="9da0c-113">ツリー ビューの上に表示される階層リンク軌跡には、ツリー ビューで現在選択されているものが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9da0c-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="9da0c-114">この階層リンク証跡は、次の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="9da0c-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="9da0c-115">機能的な場所 ID / 機能的な場所 ID (複数の機能的な場所がある場合) \> 資産 ID / 資産 ID (複数の資産がある場合) - 品目番号。</span><span class="sxs-lookup"><span data-stu-id="9da0c-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="9da0c-116">ツリー ビューで資産を選択した場合は、**有効な要求** または **有効なワーク オーダー** を選択して、資産に関連するメンテンナンス要求またはワーク オーダーを表示できます。</span><span class="sxs-lookup"><span data-stu-id="9da0c-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="9da0c-117">**開く** \> **機能的な場所**、**資産**、または **資産 BOM** を選択して、関連ビューを開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="9da0c-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="9da0c-118">**表示** フィールドで選択できる **資産の機能的な場所** オプションは、資産を選択できる任意の資産ルックアップでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="9da0c-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="9da0c-119">たとえば、[資産の作成](../objects/create-an-object.md)、メンテナンス要求の作成、ワーク オーダーの作成など、ツリー ビューが **資産表示** タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9da0c-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
