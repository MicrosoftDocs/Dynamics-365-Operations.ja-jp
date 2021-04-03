---
title: 勘定と分析コードの組み合わせの入力 (セグメント化されたエントリのコントロール)
description: この記事は、勘定と分析コードの組み合わせまたは勘定科目を入力する方法について説明します。 入力経験は、多くの場合、セグメント化されたエントリのコントロールと呼ばれます。
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bed6a13a721269550fa72c495e7ecfddadf9d8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260784"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="c86a4-104">勘定と分析コードの組み合わせの入力 (セグメント化されたエントリのコントロール)</span><span class="sxs-lookup"><span data-stu-id="c86a4-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c86a4-105">この記事は、勘定と分析コードの組み合わせまたは勘定科目を入力する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="c86a4-106">入力経験は、多くの場合、セグメント化されたエントリのコントロールと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c86a4-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="c86a4-107">ユーザーは、一般仕訳帳、予算作成、および転記の定義などのさまざまなページで、勘定と分析コードの組み合わせを入力します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="c86a4-108">有効な勘定と分析コードの組み合わせは、元帳に割り当てられた勘定構造と勘定構造に割り当てられた詳細ルールによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c86a4-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="c86a4-109">組み合わせを入力するときに、手動で値を入力するか、または豊富なルックアップ エクスペリエンスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c86a4-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="c86a4-110">フィールドを入力するときに、入力し始めると、値と説明を検索できます。</span><span class="sxs-lookup"><span data-stu-id="c86a4-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="c86a4-111">たとえば、「180」と入力すると、その番号の組み合わせで始まるすべての値を検索します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="c86a4-112">または、「Cash」と入力すれば、「Cash」で始まるすべての説明を持つ値を検索します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="c86a4-113">\*Cash や \*180 などのワイルドカードを使用すると、値や説明に検索基準が含まれているかどうか検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="c86a4-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="c86a4-114">次の表に、ルックアップが閉じているときに使用できるキーボード ショートカットを示します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c86a4-115">キーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="c86a4-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="c86a4-116">アクション</span><span class="sxs-lookup"><span data-stu-id="c86a4-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c86a4-117">Alt + 下方向キー</span><span class="sxs-lookup"><span data-stu-id="c86a4-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="c86a4-118">ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c86a4-118">Open the lookup.</span></span> <span data-ttu-id="c86a4-119">2 回目に Alt + 下方向キーを押した場合、フォーカスがポップアップのセグメントに移動します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="c86a4-120">Enter キーおよび Shift + Enter キー</span><span class="sxs-lookup"><span data-stu-id="c86a4-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="c86a4-121">勘定科目表の区切り記号</span><span class="sxs-lookup"><span data-stu-id="c86a4-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="c86a4-122">右方向キーおよび左方向キー</span><span class="sxs-lookup"><span data-stu-id="c86a4-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="c86a4-123">前後のセグメントへ移動します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c86a4-124">タブ</span><span class="sxs-lookup"><span data-stu-id="c86a4-124">Tab</span></span></td>
<td><span data-ttu-id="c86a4-125">グリッド内で次のフィールドに移動します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c86a4-126">次の表に、ルックアップが開いているときに使用できるキーボード ショートカットを示します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c86a4-127">キーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="c86a4-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="c86a4-128">アクション</span><span class="sxs-lookup"><span data-stu-id="c86a4-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c86a4-129">Esc キー</span><span class="sxs-lookup"><span data-stu-id="c86a4-129">Esc</span></span></td>
<td><span data-ttu-id="c86a4-130">ルックアップを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c86a4-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="c86a4-131">上方向キーおよび下方向キー</span><span class="sxs-lookup"><span data-stu-id="c86a4-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="c86a4-132">Page Up キーおよび Page Down キー</span><span class="sxs-lookup"><span data-stu-id="c86a4-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="c86a4-133">Home キーおよび End キー</span><span class="sxs-lookup"><span data-stu-id="c86a4-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="c86a4-134">一覧での前後の値、値の前後のグループ、またはルックアップの最初または最後の要素に移動します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c86a4-135">勘定科目表の区切り記号</span><span class="sxs-lookup"><span data-stu-id="c86a4-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="c86a4-136">右方向キーおよび左方向キー</span><span class="sxs-lookup"><span data-stu-id="c86a4-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="c86a4-137">前後のセグメントへ移動します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c86a4-138">タブ</span><span class="sxs-lookup"><span data-stu-id="c86a4-138">Tab</span></span></td>
<td><span data-ttu-id="c86a4-139">グリッド内で次のフィールドに移動します。</span><span class="sxs-lookup"><span data-stu-id="c86a4-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c86a4-140">Alt + W キー</span><span class="sxs-lookup"><span data-stu-id="c86a4-140">Alt+W</span></span></td>
<td><span data-ttu-id="c86a4-141"><strong>すべて表示l</strong> と <strong>有効なものを表示</strong> を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="c86a4-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]