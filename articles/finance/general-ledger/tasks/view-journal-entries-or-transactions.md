---
title: 仕訳入力またはトランザクションの表示
description: この手順では、仕訳入力やトランザクションを検索するための伝票トランザクションの照会の使用方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f463b7764288918609cba364acf342eed28ad929
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144654"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="2605a-103">仕訳入力またはトランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="2605a-103">View journal entries or transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2605a-104">この手順では、仕訳入力やトランザクションを検索するための伝票トランザクションの照会の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2605a-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="2605a-105">**ナビゲーション ウィンドウ > モジュール > 総勘定元帳 > 照会およびレポート > 伝票トランザクション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2605a-105">Go to **Navigation pane > Modules > General ledger > Inquiries and reports > Voucher transactions**.</span></span>
2. <span data-ttu-id="2605a-106">フィルター基準を定義するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="2605a-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="2605a-107">選択したフィールドのフィルター基準を入力します。</span><span class="sxs-lookup"><span data-stu-id="2605a-107">Enter your filter critieria for the selected field.</span></span> <span data-ttu-id="2605a-108">1 つの値または範囲をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="2605a-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="2605a-109">範囲を定義するときに、正しい構文が使用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2605a-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="2605a-110">値は 2 つのピリオド (..) で区切られている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2605a-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="2605a-111">**結合**タブをクリックして、フィルター処理する追加のテーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="2605a-111">Click the **Joins** tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="2605a-112">ツリーで、**テーブルの一般仕訳入力**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2605a-112">In the tree, select **Tables/General journal entry**.</span></span>
6. <span data-ttu-id="2605a-113">**テーブル結合の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2605a-113">Click **Add table join**.</span></span>
7. <span data-ttu-id="2605a-114">追加のテーブルを追加しないことにした場合は、**キャンセル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2605a-114">Click **Cancel** if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="2605a-115">**範囲**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2605a-115">Click the **Range** tab.</span></span>
9. <span data-ttu-id="2605a-116">**OK** をクリックして、クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="2605a-116">Click **OK** to run the query.</span></span>
10. <span data-ttu-id="2605a-117">アクション ウィンドウで、**トランザクション発生元**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2605a-117">On the Action pane, click **Transaction origin**.</span></span> <span data-ttu-id="2605a-118">グリッドに関するさまざまなボタンは、伝票の選択されたレコードに関する追加情報の調査に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2605a-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="2605a-119">一部のボタンは、トランザクションのタイプと特性によって使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2605a-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>
11. <span data-ttu-id="2605a-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2605a-120">Close the page.</span></span>
12. <span data-ttu-id="2605a-121">アクション ウィンドウで、**元の文書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2605a-121">On the Action pane, Click **Original document**.</span></span>
13. <span data-ttu-id="2605a-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2605a-122">Close the page.</span></span>

