---
title: 売上税グループと品目売上税グループの設定
description: このタスクの記録では、売上税および品目売上税のグループ設定について説明します。
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 126e1de2d59d33fd7a5df1e011aa8c1aff63dfc6
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454671"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="c4736-103">売上税グループと品目売上税グループの設定</span><span class="sxs-lookup"><span data-stu-id="c4736-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4736-104">このタスクの記録では、売上税および品目売上税のグループ設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="c4736-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="c4736-105">売上税グループは、顧客と仕入先に関連付けられた売上税コードのグループです。</span><span class="sxs-lookup"><span data-stu-id="c4736-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="c4736-106">また、特定の仕入先や顧客には転記されないトランザクションの勘定科目にも関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c4736-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="c4736-107">品目売上税グループは、製品などのリソースに関連付けられた売上税コードのグループです。</span><span class="sxs-lookup"><span data-stu-id="c4736-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="c4736-108">特定のトランザクションに適用される売上税は、トランザクションの売上税グループと品目売上税グループの両方に含まれる売上税コードによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="c4736-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="c4736-109">売上税の計算が可能なのは、売上税の計算または記録が必要な各トランザクションに対して、売上税グループと品目売上税グループが選択されている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="c4736-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="c4736-110">**ナビゲーション ウィンドウ > モジュール > 税 > 間接税 > 売上税 > 売上税グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c4736-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="c4736-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4736-111">Click **New**.</span></span>
3. <span data-ttu-id="c4736-112">**売上税グループ** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4736-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="c4736-113">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4736-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c4736-114">**設定**セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="c4736-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="c4736-115">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4736-115">Click **Add**.</span></span>
7. <span data-ttu-id="c4736-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c4736-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c4736-117">**売上税コード** フィールドで、ドロップダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c4736-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c4736-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4736-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c4736-119">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4736-119">Click **Save**.</span></span>
11. <span data-ttu-id="c4736-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c4736-120">Close the page.</span></span>
12. <span data-ttu-id="c4736-121">**税 > 間接税 > 売上税 > 品目売上税グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c4736-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="c4736-122">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4736-122">Click **New**.</span></span>
14. <span data-ttu-id="c4736-123">**品目売上税グループ** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4736-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="c4736-124">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4736-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="c4736-125">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4736-125">Click **Add**.</span></span>
17. <span data-ttu-id="c4736-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c4736-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="c4736-127">**売上税コード** フィールドで、ドロップダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c4736-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="c4736-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4736-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="c4736-129">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4736-129">Click **Save**.</span></span>

