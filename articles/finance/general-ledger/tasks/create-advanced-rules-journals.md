---
title: 仕訳帳の詳細なルールの作成
description: この手順は、仕訳帳の詳細なルールの作成について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea6ca24d27bb5b00bbe31060ce2f7e40bf2fb335
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445263"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="d5f78-103">仕訳帳の詳細なルールの作成</span><span class="sxs-lookup"><span data-stu-id="d5f78-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5f78-104">この手順は、仕訳帳の詳細なルールの作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="d5f78-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="d5f78-105">これには、仕訳帳のコントロールおよびユーザーの転記制限の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d5f78-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="d5f78-106">この手順では、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="d5f78-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="d5f78-107">仕訳帳コントロールの設定</span><span class="sxs-lookup"><span data-stu-id="d5f78-107">Set up journal control</span></span>
1. <span data-ttu-id="d5f78-108">**ナビゲーション ウィンドウ** で、**モジュール > 総勘定元帳 > 仕訳帳の設定 > 仕訳帳名** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d5f78-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="d5f78-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d5f78-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d5f78-110">**アクション ウィンドウ** で、**仕訳帳コントロール** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="d5f78-111">**転記できる勘定タイプはどれですか** クイック タブで、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="d5f78-112">**会社コード** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d5f78-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d5f78-113">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d5f78-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d5f78-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d5f78-115">**この仕訳に対して有効な区分値はどれですか** クイック タブで、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="d5f78-116">**勘定構造** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d5f78-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="d5f78-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d5f78-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="d5f78-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d5f78-119">**区分** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d5f78-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="d5f78-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d5f78-121">**開始値** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d5f78-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="d5f78-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d5f78-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="d5f78-123">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="d5f78-124">**終了値** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d5f78-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="d5f78-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d5f78-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="d5f78-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="d5f78-127">転記制限の設定</span><span class="sxs-lookup"><span data-stu-id="d5f78-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="d5f78-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d5f78-128">Close the page.</span></span>
2. <span data-ttu-id="d5f78-129">**転記制限** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="d5f78-130">**転記制限をどのように設定しますか** フィールドで、'ユーザー グループ別' を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5f78-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="d5f78-131">ツリーで、「この仕訳帳名で転記を許可するグループ」をチェックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="d5f78-132">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5f78-132">Click **OK**.</span></span>

