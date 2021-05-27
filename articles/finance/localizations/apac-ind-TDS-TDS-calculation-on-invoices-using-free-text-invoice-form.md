---
title: 自由書式の請求書ページからの請求書の TDS 計算
description: このトピックでは、自由形式の請求書ページを使用して、請求書の源泉徴収税 (TDS) を計算する方法について説明します。
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023394"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="510f9-103">自由書式の請求書ページからの請求書の TDS 計算</span><span class="sxs-lookup"><span data-stu-id="510f9-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="510f9-104">このトピックでは、**自由形式の請求書** ページを使用して、請求書の源泉徴収税 (TDS) を計算する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="510f9-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="510f9-105">**売掛金勘定 \> 請求書 \> すべての自由書式の請求書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="510f9-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="510f9-106">[![自由書式の請求書のページ](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="510f9-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="510f9-107">**新規** を選択して自由形式の請求書を作成し、必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="510f9-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="510f9-108">**請求書** タブを選択します。**源泉徴収税グループ** セクションの **課税対象の種類** フィールドに、顧客の課税対象カテゴリの種類が表示されます。</span><span class="sxs-lookup"><span data-stu-id="510f9-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="510f9-109">**TDS グループ** フィールドで、顧客に対して定義されている既定の TDS グループを確認または変更します。</span><span class="sxs-lookup"><span data-stu-id="510f9-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="510f9-110">**TDS グループ** フィールドで値を選択すると、**TDS グループ** フィールドは使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="510f9-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="510f9-111">TDS は、**すべての顧客** ページで顧客の **源泉徴収税の計算** オプションが **はい** に設定されている場合にのみ計算されます。</span><span class="sxs-lookup"><span data-stu-id="510f9-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="510f9-112">**税金情報** タブにある **会社情報** セクションの **名前** フィールドで、会社に対して設定されている代替住所の会社名を選択します。</span><span class="sxs-lookup"><span data-stu-id="510f9-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="510f9-113">**源泉徴収税** セクションの **税勘定番号 (TAN)** フィールドには、選択した会社の税勘定番号 (TAN) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="510f9-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="510f9-114">**請求明細行** タブで、請求明細行を作成し、必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="510f9-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="510f9-115">**源泉徴収税グループ** セクションでは、**税勘定番号 (TAN)** フィールドに、TAN が表示され、**TDS グループ** フィールドには TDS グループが表示されます。</span><span class="sxs-lookup"><span data-stu-id="510f9-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="510f9-116">**源泉徴収税** を選択し、**一時源泉徴収税トランザクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="510f9-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="510f9-117">このページの上部には次のフィールドがあります:</span><span class="sxs-lookup"><span data-stu-id="510f9-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="510f9-118">**合計源泉徴収税額** – TDS グループのトランザクションに対して計算された合計 TDS。</span><span class="sxs-lookup"><span data-stu-id="510f9-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="510f9-119">**値** – トランザクションの TDS の計算に使用された合計割合。</span><span class="sxs-lookup"><span data-stu-id="510f9-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="510f9-120">合計割合は、TDS 税コードに対して定義され、TDS グループに関連付けられた式に基づきます。</span><span class="sxs-lookup"><span data-stu-id="510f9-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="510f9-121">**合計調整済源泉徴収税額** – TDS グループのすべての税コードに対する調整済 TDS 金額の合計。</span><span class="sxs-lookup"><span data-stu-id="510f9-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="510f9-122">**TDS** – 選択したチェック ボックスは、TDS グループがトランザクションに関連付けられていることを示します。</span><span class="sxs-lookup"><span data-stu-id="510f9-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="510f9-123">**概要** タブ、**全般** タブおよび **調整** タブのフィールドには、TDS グループに関連付けられた各 TDS 税コードに対する計算済 TDS 金額と調整済 TDS 金額の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="510f9-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="510f9-124">**しきい値** を選択して、**しきい値** ページを開き、特定の TDS 税コードに関連付けられた TDS 税コンポーネントに定義されているしきい値制限を確認できます。</span><span class="sxs-lookup"><span data-stu-id="510f9-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="510f9-125">**フォーミュラ デザイナー** を選択すると、**フォーミュラ デザイナー** ページを開き、特定の TDS 税コードに対して定義された式を確認できます。</span><span class="sxs-lookup"><span data-stu-id="510f9-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="510f9-126">自由書式の請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="510f9-126">Post the free text invoice.</span></span> <span data-ttu-id="510f9-127">自由書式の請求書で計算された TDS 金額は、TDS グループの各 TDS 税コードに対して定義された売掛金勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="510f9-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="510f9-128">TDS 税コードの売掛金勘定は、**源泉徴収税コード** ページで定義されます。</span><span class="sxs-lookup"><span data-stu-id="510f9-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="510f9-129">**転記済源泉徴収税** を選択し、**源泉徴収税トランザクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="510f9-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="510f9-130">**値** フィールドには、トランザクションの TDS の計算に使用された合計割合が表示されます。</span><span class="sxs-lookup"><span data-stu-id="510f9-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="510f9-131">**概要** タブ、**全般** タブ、および **金額** タブの各フィールドに、請求明細行で計算された TDS 金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="510f9-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="510f9-132">TDS グループに関連付けられた各 TDS 税コードの TDS 計算情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="510f9-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
