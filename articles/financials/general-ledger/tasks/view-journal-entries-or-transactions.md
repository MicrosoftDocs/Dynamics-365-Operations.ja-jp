---
title: 仕訳入力またはトランザクションの表示
description: この手順では、仕訳入力やトランザクションを検索するための伝票トランザクションの照会の使用方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: c93b581e22665b27c1b99503cc91c20ead14ac81
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834687"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="53bf3-103">仕訳入力またはトランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="53bf3-103">View journal entries or transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53bf3-104">この手順では、仕訳入力やトランザクションを検索するための伝票トランザクションの照会の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="53bf3-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="53bf3-105">[総勘定元帳] > [照会およびレポート] > [伝票トランザクション] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="53bf3-105">Go to General ledger > Inquiries and reports > Voucher transactions.</span></span>
2. <span data-ttu-id="53bf3-106">フィルター基準を定義するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="53bf3-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="53bf3-107">選択したフィールドのフィルター基準を入力します。</span><span class="sxs-lookup"><span data-stu-id="53bf3-107">Enter your filter critieria for the selected field.</span></span>
    * <span data-ttu-id="53bf3-108">1 つの値または範囲をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="53bf3-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="53bf3-109">範囲を定義するときに、正しい構文が使用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="53bf3-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="53bf3-110">値は 2 つのピリオド (..) で区切られている必要があります。</span><span class="sxs-lookup"><span data-stu-id="53bf3-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="53bf3-111">[結合] タブをクリックして、フィルター処理する追加のテーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="53bf3-111">Click the Joins tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="53bf3-112">ツリーで、[テーブル] の [一般仕訳入力] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53bf3-112">In the tree, select 'Tables\General journal entry'.</span></span>
6. <span data-ttu-id="53bf3-113">[テーブル結合の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53bf3-113">Click Add table join.</span></span>
7. <span data-ttu-id="53bf3-114">追加のテーブルを追加しないことにした場合は、[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53bf3-114">Click Cancel if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="53bf3-115">[範囲] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53bf3-115">Click the Range tab.</span></span>
9. <span data-ttu-id="53bf3-116">[OK] をクリックして、クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="53bf3-116">Click OK to run the query.</span></span>
10. <span data-ttu-id="53bf3-117">[トランザクション発生元] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53bf3-117">Click Transaction origin.</span></span>
    * <span data-ttu-id="53bf3-118">グリッドに関するさまざまなボタンは、伝票の選択されたレコードに関する追加情報の調査に使用できます。</span><span class="sxs-lookup"><span data-stu-id="53bf3-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="53bf3-119">一部のボタンは、トランザクションのタイプと特性によって使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="53bf3-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>  
11. <span data-ttu-id="53bf3-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53bf3-120">Close the page.</span></span>
12. <span data-ttu-id="53bf3-121">[元の文書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53bf3-121">Click Original document.</span></span>
13. <span data-ttu-id="53bf3-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53bf3-122">Close the page.</span></span>

