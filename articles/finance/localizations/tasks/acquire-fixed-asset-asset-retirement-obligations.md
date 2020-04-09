---
title: 資産除去責務がある固定資産の取得
description: 日本では、資産除去責務 (ARO) は現在の値に割引され、固定資産の取得原価に追加されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8830a73831be239beedb0b2687900bb84cfabe53
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143500"
---
# <a name="acquire-a-fixed-asset-with-asset-retirement-obligations"></a><span data-ttu-id="b6671-103">資産除去責務がある固定資産の取得</span><span class="sxs-lookup"><span data-stu-id="b6671-103">Acquire a fixed asset with asset retirement obligations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6671-104">日本では、資産除去責務 (ARO) は現在の値に割引され、固定資産の取得原価に追加されます。</span><span class="sxs-lookup"><span data-stu-id="b6671-104">For Japan, the asset retirement obligation (ARO) is discounted to present value, and added to the acquisition cost of the fixed asset.</span></span> 



<span data-ttu-id="b6671-105">このタスクでは、ARO を持つ固定資産の取得方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b6671-105">Use this task to learn how to acquire a fixed asset with ARO.</span></span> 



<span data-ttu-id="b6671-106">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6671-106">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="b6671-107">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="b6671-107">This task uses the JPMF demo company data.</span></span>

1. <span data-ttu-id="b6671-108">[固定資産] > [資産除去責務] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6671-108">Go to Fixed assets > Asset retirement obligations > Fixed assets journal.</span></span>
2. <span data-ttu-id="b6671-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6671-109">Click New.</span></span>
3. <span data-ttu-id="b6671-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6671-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b6671-111">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6671-111">Click Save.</span></span>
5. <span data-ttu-id="b6671-112">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6671-112">Click Lines.</span></span>
6. <span data-ttu-id="b6671-113">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6671-113">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="b6671-114">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6671-114">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="b6671-115">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6671-115">In the Book field, type a value.</span></span>
9. <span data-ttu-id="b6671-116">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6671-116">In the Debit field, enter a number.</span></span>
10. <span data-ttu-id="b6671-117">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6671-117">Click Functions.</span></span>
11. <span data-ttu-id="b6671-118">[資産除去責務トランザクションの生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6671-118">Click Generate asset retirement obligation transactions.</span></span>
    * <span data-ttu-id="b6671-119">[機能] > [資産除去責務トランザクションの生成] のメニューは、固定資産が同じ仕訳帳にある場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="b6671-119">The menu at Functions > Generate asset retirement obligation transactions is used when the fixed asset is in the same journal.</span></span>     <span data-ttu-id="b6671-120">また、すでに取得済の固定資産については、[提案] > [除去費用の資産計上] のメニューも使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b6671-120">You can also use the menu at Proposals > Capitalized asset retirement obligation for already acquired fixed assets.</span></span>  
    * <span data-ttu-id="b6671-121">[ドキュメント タイプ] が [資産除去責務] である新しいレコードが作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b6671-121">Confirm that a new record with Document type of Asset retirement obligation is created.</span></span>  
12. <span data-ttu-id="b6671-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b6671-122">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b6671-123">提案金額は現在の値に割引されます。</span><span class="sxs-lookup"><span data-stu-id="b6671-123">The proposed amount is discounted to present value.</span></span>  
13. <span data-ttu-id="b6671-124">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6671-124">Click Post.</span></span>

