---
title: 仕入先請求ポリシーの設定
description: このトピックでは、Dynamics 365 for Finance and Operations において仕入先請求ポリシーを設定する方法について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 328aafd16496fdbb963c9aa40a5c13005be7a382
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842812"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="d50cc-103">仕入先請求ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="d50cc-103">Set up vendor invoice policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d50cc-104">このトピックでは、Dynamics 365 for Finance and Operations において仕入先請求ポリシーを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-104">This topic explains how to set up vendor invoice policies in Dynamics 365 for Finance and Operatoins.</span></span> <span data-ttu-id="d50cc-105">[仕入先請求ポリシー] は、[仕入先請求書] ページを使用して仕入先請求書を転記するか、仕入先請求書の [ポリシー違反] ページを開いたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="d50cc-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="d50cc-106">また、ワークフローに請求書を送信するたびに、仕入先請求書ワークフローを構成して仕入先請求書ポリシーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d50cc-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="d50cc-107">仕入先請求ポリシーは仕入帳や請求仕訳帳で作成した請求書には適用しません。</span><span class="sxs-lookup"><span data-stu-id="d50cc-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="d50cc-108">請求書照合の検証は、仕入先請求ポリシーを使用せず、[買掛金管理パラメーター] ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="d50cc-109">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="d50cc-110">買掛金勘定マネージャーまたは会計マネージャーのロールでは、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="d50cc-111">始める前に、[請求書照合] コンフィギュレーション キーが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="d50cc-112">仕入先請求書ポリシーの作成準備</span><span class="sxs-lookup"><span data-stu-id="d50cc-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="d50cc-113">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > 設定 > 買掛金勘定パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="d50cc-114">**請求書検証** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="d50cc-115">**請求書ヘッダーの状態を自動的に更新**チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="d50cc-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="d50cc-116">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-116">Select **OK**.</span></span>
5. <span data-ttu-id="d50cc-117">**不一致のある請求書を転記**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="d50cc-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d50cc-118">Close the page.</span></span>
7. <span data-ttu-id="d50cc-119">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ポリシー設定 > 仕入先請求書ポリシー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="d50cc-120">**パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="d50cc-121">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-121">Select **Add**.</span></span>
10. <span data-ttu-id="d50cc-122">ページを閉じて、ホーム ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="d50cc-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="d50cc-123">仕入先請求書のポリシー ルール タイプの作成</span><span class="sxs-lookup"><span data-stu-id="d50cc-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="d50cc-124">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ポリシー設定 > 仕入先請求書ポリシー ルール タイプ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="d50cc-125">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-125">Select **New**.</span></span>
3. <span data-ttu-id="d50cc-126">**ルール名**および**説明**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="d50cc-127">**クエリ名**フィールドで、ドロップ ダウン ボタンを選択してルックアップを開き、目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-127">In the **Query name** field, select the drop-down button to open the lookup, then selec the desired record.</span></span>
5. <span data-ttu-id="d50cc-128">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-128">Select **Save**.</span></span>
6. <span data-ttu-id="d50cc-129">ページを閉じて、ホーム ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="d50cc-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="d50cc-130">仕入先請求書ポリシーを定義します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="d50cc-131">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ポリシー設定 > 仕入先請求書ポリシー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="d50cc-132">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-132">Select **New**.</span></span>
3. <span data-ttu-id="d50cc-133">**名前**および**説明**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="d50cc-134">**ポリシーの組織**セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="d50cc-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="d50cc-135">ツリーで、**Contoso Entertainment System USA** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="d50cc-136">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-136">Select **Add**.</span></span>
7. <span data-ttu-id="d50cc-137">**ポリシー ルール** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="d50cc-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="d50cc-138">**ポリシー ルールの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="d50cc-139">**ポリシー ルールの説明**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="d50cc-140">**フィルター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-140">Select **Filter**.</span></span>
11. <span data-ttu-id="d50cc-141">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-141">Select **Add**.</span></span> <span data-ttu-id="d50cc-142">目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-142">Select the desired record.</span></span>
12. <span data-ttu-id="d50cc-143">**テーブル**、**派生テーブル**、および**フィールド**フィールドで、ドロップ ダウン メニューからオプションを選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="d50cc-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d50cc-144">Close the page.</span></span>
14. <span data-ttu-id="d50cc-145">**基準**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="d50cc-146">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-146">Select **OK**.</span></span>
16. <span data-ttu-id="d50cc-147">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d50cc-147">Select **OK**.</span></span>
17. <span data-ttu-id="d50cc-148">ページを閉じて、ホーム ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="d50cc-148">Close the pages to return to the home page.</span></span>

