---
title: 仕訳帳の詳細なルールの作成
description: この手順は、仕訳帳の詳細なルールの作成について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553110"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="85da7-103">仕訳帳の詳細なルールの作成</span><span class="sxs-lookup"><span data-stu-id="85da7-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85da7-104">この手順は、仕訳帳の詳細なルールの作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="85da7-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="85da7-105">これには、仕訳帳のコントロールおよびユーザーの転記制限の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="85da7-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="85da7-106">この手順では、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="85da7-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="85da7-107">仕訳帳コントロールの設定</span><span class="sxs-lookup"><span data-stu-id="85da7-107">Set up journal control</span></span>
1. <span data-ttu-id="85da7-108">[総勘定元帳] > [仕訳帳の設定] > [仕訳帳名] に移動します。</span><span class="sxs-lookup"><span data-stu-id="85da7-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="85da7-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="85da7-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="85da7-110">[仕訳帳コントロール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-110">Click Journal control.</span></span>
4. <span data-ttu-id="85da7-111">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-111">Click Add.</span></span>
5. <span data-ttu-id="85da7-112">[会社コード] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="85da7-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="85da7-113">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="85da7-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="85da7-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="85da7-115">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-115">Click Add.</span></span>
9. <span data-ttu-id="85da7-116">[勘定構造] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="85da7-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="85da7-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="85da7-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="85da7-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="85da7-119">[区分] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="85da7-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="85da7-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="85da7-121">[開始値] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="85da7-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="85da7-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="85da7-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="85da7-123">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="85da7-124">[終了値] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="85da7-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="85da7-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="85da7-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="85da7-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="85da7-127">転記制限の設定</span><span class="sxs-lookup"><span data-stu-id="85da7-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="85da7-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="85da7-128">Close the page.</span></span>
2. <span data-ttu-id="85da7-129">[転記制限] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="85da7-130">[転記制限をどのように設定しますか ?] で、[ユーザー グループ別] を選択します。</span><span class="sxs-lookup"><span data-stu-id="85da7-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="85da7-131">ツリーで、「この仕訳帳名で転記を許可するグループ」をチェックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="85da7-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85da7-132">Click OK.</span></span>

