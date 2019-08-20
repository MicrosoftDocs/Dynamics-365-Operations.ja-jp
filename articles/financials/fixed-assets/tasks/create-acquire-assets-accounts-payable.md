---
title: 買掛金勘定からの資産の作成と取得
description: このタスク ガイドでは、購買プロセスで固定資産を作成し、取得する方法を説明します。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2626877c907994d03cdae960c8501a858ca214bd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840028"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="1a26a-103">買掛金勘定からの資産の作成と取得</span><span class="sxs-lookup"><span data-stu-id="1a26a-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a26a-104">このタスク ガイドでは、購買プロセスで固定資産を作成し、取得する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1a26a-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="1a26a-105">ここでは、経理担当者、買掛金勘定係、デモ会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a26a-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="1a26a-106">固定資産パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="1a26a-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="1a26a-107">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a26a-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="1a26a-108">[発注書] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="1a26a-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="1a26a-109">[購買からの資産の取得を許可する] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="1a26a-110">[製品受領書または請求書の転記時に資産を作成する] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="1a26a-111">新しい仕入先請求書の作成</span><span class="sxs-lookup"><span data-stu-id="1a26a-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="1a26a-112">[買掛金勘定] > [ワークスペース] > [仕入先請求書入力] に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a26a-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="1a26a-113">[新しい仕入先請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="1a26a-114">[請求元仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1a26a-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1a26a-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1a26a-116">[数] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a26a-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="1a26a-117">[転記日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a26a-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="1a26a-118">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-118">Click Add line.</span></span>
8. <span data-ttu-id="1a26a-119">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1a26a-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1a26a-120">在庫のない品目または調達カテゴリが、固定資産の取得に使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a26a-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="1a26a-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="1a26a-122">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a26a-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1a26a-123">数量に関係なく、1 つの請求明細行が作成する固定資産は 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="1a26a-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="1a26a-124">請求書の数量フィールドの値は、固定資産の数量に転送されます。</span><span class="sxs-lookup"><span data-stu-id="1a26a-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="1a26a-125">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a26a-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="1a26a-126">[明細行の詳細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="1a26a-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="1a26a-127">[固定資産] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="1a26a-128">[新しい固定資産の作成] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="1a26a-129">[固定資産グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1a26a-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="1a26a-130">新しい固定資産を作成するときに使用する固定資産グループを一覧で選択します。</span><span class="sxs-lookup"><span data-stu-id="1a26a-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="1a26a-131">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="1a26a-132">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a26a-132">Click Post.</span></span>
    * <span data-ttu-id="1a26a-133">固定資産は、請求書の転記時に作成および取得されます。</span><span class="sxs-lookup"><span data-stu-id="1a26a-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

