---
title: "非製造環境での標準原価を更新"
description: "この記事は、非製造環境での標準原価の更新についてのガイダンスを提供します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4fa545aa6903bd6f789dda20ab5755ffe9a12b88
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="924e7-103">非製造環境での標準原価を更新</span><span class="sxs-lookup"><span data-stu-id="924e7-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="924e7-104">この記事は、非製造環境での標準原価の更新についてのガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="924e7-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="924e7-105">次のガイドラインでは、標準原価の更新に 2 バージョンによるアプローチを使用することを想定しています。</span><span class="sxs-lookup"><span data-stu-id="924e7-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="924e7-106">この方法では、1 番目の原価バージョンには凍結期間の最初に定義された標準原価が含まれ、2 番目の原価バージョンには差分の更新が含まれます。</span><span class="sxs-lookup"><span data-stu-id="924e7-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="924e7-107">各更新は 2 番目の原価バージョンに収容される原価レコードとして入力され、最終的に各更新が有効になります。</span><span class="sxs-lookup"><span data-stu-id="924e7-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="924e7-108">代わりの 1 バージョンによるアプローチでは、最初に定義された標準原価セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="924e7-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="924e7-109">2 バージョン方式では第 2 の原価バージョンを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="924e7-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="924e7-110">原価バージョンの定義に関するガイドラインは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="924e7-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="924e7-111">**標準原価**の原価タイプを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="924e7-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="924e7-112">**2016-UPDATES** など、原価バージョンの内容を示す意味のある識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="924e7-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="924e7-113">内容には必ず原価レコードが含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="924e7-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="924e7-114">すべてのサイトの原価レコードの入力を許可します。</span><span class="sxs-lookup"><span data-stu-id="924e7-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="924e7-115">サイトを指定すると、原価レコードはそのサイトに対してのみ入力できます。</span><span class="sxs-lookup"><span data-stu-id="924e7-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="924e7-116">[**なし**] の予備原則を指定します。</span><span class="sxs-lookup"><span data-stu-id="924e7-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="924e7-117">予備原則は、製造品目の原価計算にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="924e7-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="924e7-118">新しい品目の標準原価を訂正、調整、または更新するには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="924e7-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="924e7-119">2 番目の原価バージョンに入力する原価データを有効にするには [**原価バージョン** **設定**] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="924e7-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="924e7-120">オプションで、保留中の原価が完全かつ正確に定義された後で許可されるよう、保留中の原価の有効化を禁止できます。</span><span class="sxs-lookup"><span data-stu-id="924e7-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="924e7-121">必要に応じて、[**開始日**] フィールドに日付を入力できます。</span><span class="sxs-lookup"><span data-stu-id="924e7-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="924e7-122">一般的なガイドラインとして、差分更新を有効化する予定の日付を使用します。</span><span class="sxs-lookup"><span data-stu-id="924e7-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="924e7-123">または、原価バージョンの [**開始日**] フィールドを空にしたまま、各原価レコードの [**開始日**] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="924e7-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="924e7-124">[**品目価格**] ページを使用して、2 番目の原価バージョンに収納される品目原価レコードとして、更新を入力します。</span><span class="sxs-lookup"><span data-stu-id="924e7-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="924e7-125">[**品目価格**] レポートを使用して、2 番目の原価バージョンに収納される品目原価レコードに間違いがないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="924e7-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="924e7-126">[**原価バージョンの保守**] ページを使用して、2 番目の原価バージョンに収納される保留中の原価レコードを有効化できるように、ブロック フラグを変更します。</span><span class="sxs-lookup"><span data-stu-id="924e7-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="924e7-127">[**価格の有効化**] ページ ([**原価バージョンの保守**] ページから開く) を使用して、2 番目の原価バージョンに収納されるすべての品目の保留中の原価レコードを有効化できます。</span><span class="sxs-lookup"><span data-stu-id="924e7-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="924e7-128">[**品目価格**] ページの [**保留中の価格の有効化**] ボタンをクリックすることにより、個々の品目の保留中の原価レコードを有効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="924e7-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="924e7-129">追加のデータ管理を禁止するには、[**原価バージョン設定**] ページを使用して、2 番目の原価バージョンに収納されるブロック フラグを変更します。</span><span class="sxs-lookup"><span data-stu-id="924e7-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="924e7-130">ブロック ポリシーは、新しい保留中の原価の入力と有効化を禁止します。</span><span class="sxs-lookup"><span data-stu-id="924e7-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





