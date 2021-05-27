---
title: 発注書フォームと販売注文フォームを使用した TDS 請求書の計算
description: このトピックでは、様々なタイプの請求書のソース (TDS) で税控除を計算する手順を示します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023378"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="e5de7-103">発注書フォームと販売注文フォームを使用した TDS 請求書の計算</span><span class="sxs-lookup"><span data-stu-id="e5de7-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5de7-104">このトピックでは、**発注書**、**購買仕訳帳**、**一括発注**、**販売注文** の各ページをを使ってさまざまな種類の請求書の源泉徴収税 (TDS) を計算する手順を紹介します。</span><span class="sxs-lookup"><span data-stu-id="e5de7-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="e5de7-105">一覧表示されたページを使用して、発注書、購買仕訳帳、購買一括注文、または販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="e5de7-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="e5de7-106">必要な詳細情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5de7-106">Enter the required details.</span></span>

2. <span data-ttu-id="e5de7-107">**設定** タブを選択して、仕入先または顧客の被査定者の性質を表示します。</span><span class="sxs-lookup"><span data-stu-id="e5de7-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="e5de7-108">この情報は、**源泉徴収税グループ** フィールド グループの **被査定者の性質** フィールド に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="e5de7-109">**TDS グループ** フィールドで、仕入先や顧客に対して定義されている既定の TDS グループを確認または変更します。</span><span class="sxs-lookup"><span data-stu-id="e5de7-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e5de7-110">**TDS グループ** フィールドで TDS グループを選択すると、**TCS グループ** フィールドは使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="e5de7-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="e5de7-111">TDS は、**すべての仕入先** または **すべての顧客** ページで、仕入先または顧客の **源泉徴収税を計算する** チェックボックスが選択されている場合にのみ計算されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="e5de7-112">**明細行** タブで品目を作成し、必要な詳細情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5de7-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="e5de7-113">ヘッダー レベルで定義されたTDSグループを表示または変更するには、**設定** タブ (行レベル) を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5de7-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="e5de7-114">TDS グループは、**TDS グループ** フィールド、**源泉徴収税グループ** のフィールド グループの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="e5de7-115">**税金情報** タブを選択し、このフィールドに表示されている会社名に設定されている代替アドレスを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5de7-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="e5de7-116">**名前** フィールドの **会社情報** フィールドグループの下に会社名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="e5de7-117">選択された会社名の TAN は、**源泉徴収税フィールド** グループの下の **税口座番号** (**TAN**) フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="e5de7-118">**源泉徴収税** を選択し、**一時源泉徴収税トランザクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="e5de7-119">**一時源泉徴収票** ページの上部ペインで、以下のフィールドで確認できます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="e5de7-120">**合計源泉徴収税額** – TDS グループのトランザクションに対して計算された TDS の合計です。</span><span class="sxs-lookup"><span data-stu-id="e5de7-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="e5de7-121">**値** – トランザクションの TDS の計算に使用された合計割合です。</span><span class="sxs-lookup"><span data-stu-id="e5de7-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="e5de7-122">合計割合は、TDS 税コードに対して定義され、TDS グループに関連付けられた式に基づきます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="e5de7-123">**合計調整済源泉徴収税額** – TDS グループのすべての税コードに対する調整済 TDS 金額の合計です。</span><span class="sxs-lookup"><span data-stu-id="e5de7-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="e5de7-124">**TDS** - これが選択されている場合、TDS グループはトランザクションに関連付けされます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="e5de7-125">**一時源泉徴収票トランザクション** ページの **概要**、**一般**、 **調整** タブのフィールドには、TDS グループに属する各 TDS 税コードの計算された TDS 金額と調整された TDS 金額の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="e5de7-126">**しきい値** を選択すると、**しきい値** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="e5de7-127">このページでは、特定の TDS 税コードに関連付けられた TDS 税コンポーネントに定義されたしきい値を確認できます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="e5de7-128">**式デザイナー** を選択して **式デザイナー** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="e5de7-129">このページでは、特定の TDS 税コードに定義された計算式が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="e5de7-130">請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="e5de7-130">Post the invoice.</span></span> <span data-ttu-id="e5de7-131">購買請求書で計算された TDS 金額が買掛金勘定に転記され、売上請求書で計算された TDS 金額が TDS グループの各 TDS 税コードに対して定義されている売掛金勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="e5de7-132">TDS 税コードの買掛金勘定や売掛金勘定は、**源泉徴収税コード** ページで定義されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="e5de7-133">**照会** ボタン **> 請求書 > 転記済み源泉徴収税** ボタンを選択し、**源泉徴収税トランザクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="e5de7-134">**値** フィールドには、当該取引の TDS 計算に使用された合計パーセンテージを確認できます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="e5de7-135">**源泉徴収税トランザクション** ページの **概要** タブ、**一般** タブ、および **金額** タブの各フィールドには、トランザクションに対して計算された TDS の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="e5de7-136">TDS グループに関連付けられた各 TDS 税コードの TDS 計算情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5de7-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
