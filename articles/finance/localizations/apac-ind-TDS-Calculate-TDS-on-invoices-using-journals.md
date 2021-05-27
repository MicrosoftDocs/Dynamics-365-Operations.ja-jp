---
title: 仕訳帳を使用して請求書の TDS を計算する
description: このトピックでは、仕訳帳のソース (TDS) で税控除を計算する手順を示します。
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023402"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="ab517-103">仕訳帳を使用して請求書の TDS を計算する</span><span class="sxs-lookup"><span data-stu-id="ab517-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab517-104">このトピックでは、仕訳帳のソース (TDS) で税控除を計算する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="ab517-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="ab517-105">**一般仕訳帳** ページを開きます (**一般会計 > 仕訳入力 > 一般仕訳帳**)。</span><span class="sxs-lookup"><span data-stu-id="ab517-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="ab517-106">[![一般仕訳帳](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="ab517-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="ab517-107">テーブルに記載されている仕訳フォームを使用して、仕訳の明細を作成します。</span><span class="sxs-lookup"><span data-stu-id="ab517-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="ab517-108">勘定タイプとオフセット勘定タイプを選択し、取引の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="ab517-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="ab517-109">**請求書承認仕訳帳** ページで、**伝票の検索** を選択し、TDS を計算する請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab517-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="ab517-110">**請求書の登録** ページや **伝票の検索** ページで作成した請求書を表示します。</span><span class="sxs-lookup"><span data-stu-id="ab517-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="ab517-111">**仕訳帳伝票** ページ **一般** タブの **TDS グループ** で、仕入先または顧客に対して定義されている既定の TDS グループを確認または変更します。</span><span class="sxs-lookup"><span data-stu-id="ab517-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="ab517-112">仕訳帳明細行で計算される TDS の金額は、**TDS グループ** フィールドに記載された TDS の税コードに定義された計算式に基づいています。</span><span class="sxs-lookup"><span data-stu-id="ab517-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="ab517-113">**TDS グループ** フィルードで TDS グループを選択すると、**源泉徴収票グループ** フィルードと **TCS グループ** フィルードが利用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="ab517-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="ab517-114">**源泉徴収税グループ** フィールド は、**一般仕訳帳** ページでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ab517-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="ab517-115">TDS は、**すべてのベンダー** または **すべての顧客** ページで、ベンダーまたはカスタマーの **源泉徴収税を計算する** チェックボックスが選択されている場合にのみ計算されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="ab517-116">**税金情報** タブを選択し、必要に応じて、このフィールドで会社に対して設定されている会社の代替住所を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab517-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="ab517-117">**名前** フィールドの **会社情報** フィールドグループの下に会社名を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ab517-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="ab517-118">**源泉徴収税** フィールド グループの下にある **被査定者の性質** フィールドで、ベンダーまたは顧客の被査定者の性質カテゴリを表示します。</span><span class="sxs-lookup"><span data-stu-id="ab517-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="ab517-119">**税勘定番号** (**TAN**) フィールドで、選択された社名の TAN が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="ab517-120">**源泉徴収票** メニューの **源泉徴収** を選択すると、**源泉徴収の一時的な取引** のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="ab517-121">**一時源泉徴収票ページの上部** ペインには、以下のフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="ab517-122">**合計源泉徴収税額** – TDS グループのトランザクションに対して計算された TDS の合計です。</span><span class="sxs-lookup"><span data-stu-id="ab517-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="ab517-123">**値** – トランザクションの TDS の計算に使用された合計割合です。</span><span class="sxs-lookup"><span data-stu-id="ab517-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="ab517-124">合計割合は、TDS 税コードに対して定義され、TDS グループに関連付けられた式に基づきます。</span><span class="sxs-lookup"><span data-stu-id="ab517-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="ab517-125">**合計調整済源泉徴収税額** – TDS グループのすべての税コードに対する調整済 TDS 金額の合計です。</span><span class="sxs-lookup"><span data-stu-id="ab517-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="ab517-126">**TDS** - これが選択されている場合、TDS グループはトランザクションに関連付けされます。</span><span class="sxs-lookup"><span data-stu-id="ab517-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="ab517-127">**一時源泉徴収票トランザクション** ページの **概要**、**一般**、 **調整** タブのフィールドには、TDS グループに属する各 TDS 税コードの計算された TDS 金額と調整された TDS 金額の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="ab517-128">**しきい値** を選択すると、**しきい値** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="ab517-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="ab517-129">このページでは、特定の TDS 税コードに関連付けられた TDS 税コンポーネントに定義されたしきい値と例外となるしきい値を確認できます。</span><span class="sxs-lookup"><span data-stu-id="ab517-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="ab517-130">**式デザイナー** を選択して **式デザイナー** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="ab517-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="ab517-131">このページでは、特定の TDS 税コードに定義された計算式が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="ab517-132">**フォーミュラ デザイナー** と **一時的な源泉徴収税トランザクション** ページを閉じて、**仕訳伝票** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="ab517-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="ab517-133">他に必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="ab517-133">Enter the other required details.</span></span> <span data-ttu-id="ab517-134">仕訳を検証して転記します。</span><span class="sxs-lookup"><span data-stu-id="ab517-134">Validate and post the journal.</span></span> <span data-ttu-id="ab517-135">購買請求書で計算される TDS 金額は、買掛金勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="ab517-136">売上請求書で計算された TDS の金額は、TDS グループ内の TDS 税コードごとに定義された売掛金勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="ab517-137">TDS 税コードの買掛金勘定や売掛金勘定は、**源泉徴収税コード** ページで定義されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="ab517-138">**転記済源泉徴収税** を選択し、**源泉徴収税トランザクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="ab517-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="ab517-139">**値** フィールドには、当該取引の TDS 計算に使用された合計パーセンテージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="ab517-140">源泉徴収票ページの **概要**、**一般**、**金額** タブのフィールドには、TDS グループに属する各 TDS 税コードの計算された TDS 金額と調整された TDS 金額の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab517-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
