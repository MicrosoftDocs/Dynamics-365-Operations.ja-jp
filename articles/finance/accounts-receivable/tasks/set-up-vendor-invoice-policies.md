---
title: 仕入先請求ポリシーの設定
description: このトピックでは、仕入先請求ポリシーを設定する方法について説明します。
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
ms.openlocfilehash: 72f017294c976dcd1b7ddda01ac9e39252f036d6
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250282"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="fc345-103">仕入先請求ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="fc345-103">Set up vendor invoice policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc345-104">このトピックでは、仕入先請求ポリシーを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fc345-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="fc345-105">[仕入先請求ポリシー] は、[仕入先請求書] ページを使用して仕入先請求書を転記するか、仕入先請求書の [ポリシー違反] ページを開いたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="fc345-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="fc345-106">また、ワークフローに請求書を送信するたびに、仕入先請求書ワークフローを構成して仕入先請求書ポリシーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="fc345-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="fc345-107">仕入先請求ポリシーは仕入帳や請求仕訳帳で作成した請求書には適用しません。</span><span class="sxs-lookup"><span data-stu-id="fc345-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="fc345-108">請求書照合の検証は、仕入先請求ポリシーを使用せず、[買掛金管理パラメーター] ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="fc345-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="fc345-109">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc345-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="fc345-110">買掛金勘定マネージャーまたは会計マネージャーのロールでは、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fc345-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="fc345-111">始める前に、[請求書照合] コンフィギュレーション キーが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc345-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="fc345-112">仕入先請求書ポリシーの作成準備</span><span class="sxs-lookup"><span data-stu-id="fc345-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="fc345-113">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > 設定 > 買掛金勘定パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fc345-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="fc345-114">**請求書検証** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="fc345-115">**請求書ヘッダーの状態を自動的に更新**チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="fc345-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="fc345-116">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-116">Select **OK**.</span></span>
5. <span data-ttu-id="fc345-117">**不一致のある請求書を転記**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="fc345-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fc345-118">Close the page.</span></span>
7. <span data-ttu-id="fc345-119">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ポリシー設定 > 仕入先請求書ポリシー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fc345-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="fc345-120">**パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="fc345-121">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-121">Select **Add**.</span></span>
10. <span data-ttu-id="fc345-122">ページを閉じて、ホーム ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="fc345-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="fc345-123">仕入先請求書のポリシー ルール タイプの作成</span><span class="sxs-lookup"><span data-stu-id="fc345-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="fc345-124">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ポリシー設定 > 仕入先請求書ポリシー ルール タイプ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fc345-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="fc345-125">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-125">Select **New**.</span></span>
3. <span data-ttu-id="fc345-126">**ルール名**および**説明**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fc345-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="fc345-127">**クエリ名**フィールドで、ドロップ ダウン ボタンを選択してルックアップを開き、目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-127">In the **Query name** field, select the drop-down button to open the lookup, then selec the desired record.</span></span>
5. <span data-ttu-id="fc345-128">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-128">Select **Save**.</span></span>
6. <span data-ttu-id="fc345-129">ページを閉じて、ホーム ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="fc345-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="fc345-130">仕入先請求書ポリシーを定義します。</span><span class="sxs-lookup"><span data-stu-id="fc345-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="fc345-131">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ポリシー設定 > 仕入先請求書ポリシー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fc345-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="fc345-132">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-132">Select **New**.</span></span>
3. <span data-ttu-id="fc345-133">**名前**および**説明**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fc345-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="fc345-134">**ポリシーの組織**セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="fc345-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="fc345-135">ツリーで、**Contoso Entertainment System USA** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="fc345-136">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-136">Select **Add**.</span></span>
7. <span data-ttu-id="fc345-137">**ポリシー ルール** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="fc345-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="fc345-138">**ポリシー ルールの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="fc345-139">**ポリシー ルールの説明**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fc345-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="fc345-140">**フィルター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-140">Select **Filter**.</span></span>
11. <span data-ttu-id="fc345-141">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-141">Select **Add**.</span></span> <span data-ttu-id="fc345-142">目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-142">Select the desired record.</span></span>
12. <span data-ttu-id="fc345-143">**テーブル**、**派生テーブル**、および**フィールド**フィールドで、ドロップ ダウン メニューからオプションを選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="fc345-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="fc345-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fc345-144">Close the page.</span></span>
14. <span data-ttu-id="fc345-145">**基準**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fc345-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="fc345-146">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-146">Select **OK**.</span></span>
16. <span data-ttu-id="fc345-147">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc345-147">Select **OK**.</span></span>
17. <span data-ttu-id="fc345-148">ページを閉じて、ホーム ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="fc345-148">Close the pages to return to the home page.</span></span>
