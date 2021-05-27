---
title: TDS の税コードを TDS 税グループに添付し、TDS の計算に使用する式を定義する
description: このトピックでは、源泉徴収税 (TDS) のグループを設定し、TDS の税コードを TDS の税グループに関連付ける方法について説明します。 TDS 税グループの TDS を計算するには、TDS 税グループに関連付けられた TDS 税コードの式を定義する必要があります。
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023397"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="e3751-104">TDS の税コードを TDS 税グループに添付し、TDS の計算に使用する式を定義する</span><span class="sxs-lookup"><span data-stu-id="e3751-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3751-105">このトピックでは、源泉徴収税 (TDS) のグループを設定し、TDS の税コードを TDS の税グループに関連付ける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e3751-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="e3751-106">TDS 税グループの TDS を計算するには、TDS 税グループに関連付けられた TDS 税コードの式を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3751-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="e3751-107">次の手順に従って、TDS の税グループを設定し、TDS の税コードを関連付け、TDS の計算で使用する式を定義します。</span><span class="sxs-lookup"><span data-stu-id="e3751-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="e3751-108">**税 \> 間接税\> 源泉徴収税\> 源泉徴収税グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3751-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="e3751-109">[![源泉徴収税グループ ページ](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="e3751-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="e3751-110">アクション ペインで、**新規** を選択して、 TDS の源泉徴収税を作成し、必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="e3751-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="e3751-111">**税タイプ** フィールドで、**TDS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3751-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="e3751-112">**設定** クイック タブで、**追加** を選択して明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="e3751-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="e3751-113">**源泉徴収税コード** フィールドで、TDS の税グループに使用する TDS 税を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3751-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="e3751-114">**源泉徴収税の名前** フィールドには TDS 税コードの名前が表示され、**値** フィールドに値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e3751-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="e3751-115">TDS トランザクションの TDS 税コードに添付されている TDS 税コンポーネントに定義されているしきい値制限およびしきい値の制限例外を無視するには、**しきい値を無視する** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="e3751-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="e3751-116">トランザクションで税グループを計算しないようにするには、**除外する** のチェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="e3751-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="e3751-117">アクション ウィンドウで、**デザイナー** を選択してフォーミュラ デザイナーを開きます。このデザイナーで、TDS 税グループの TDS を計算する式を定義できます。</span><span class="sxs-lookup"><span data-stu-id="e3751-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="e3751-118">**デザイナー** ページの **税金** タブには、TDS 税グループに対して選択されている TDS 税コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e3751-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="e3751-119">[![デザイナーのページ](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="e3751-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="e3751-120">**計算** タブ で 、**Alt+N** キーを押して行を作成します。</span><span class="sxs-lookup"><span data-stu-id="e3751-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="e3751-121">**ID フィールド** には、自動的に生成されたTDS の計算に使用するプライオリティー ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e3751-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="e3751-122">**税コード** フィールドで、計算式を定義する TDS の税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="e3751-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="e3751-123">TDS 税グループで選択されているすべての TDS 税コードがこのフィールドで選択可能です。</span><span class="sxs-lookup"><span data-stu-id="e3751-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="e3751-124">**課税 対象基準** フィールドで、TDS の計算基準を選択します:</span><span class="sxs-lookup"><span data-stu-id="e3751-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="e3751-125">**総額** - 税コードに定義されている計算式を用いて、取引総額 (請求額) をもとに TDS を計算します。</span><span class="sxs-lookup"><span data-stu-id="e3751-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="e3751-126">**総額を除外** - コードに定義されている計算式に基づいて TDS を計算します。</span><span class="sxs-lookup"><span data-stu-id="e3751-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3751-127">優先 ID が **1** の TDS 税コードでは、**課税基準** フィールドを **Excl 総額** に設定できません。</span><span class="sxs-lookup"><span data-stu-id="e3751-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="e3751-128">TDS の計算は、TDS の税グループにアタッチ関連付けられている各税コードの **計算式** フィールドに定義されている計算式に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="e3751-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="e3751-129">プラス記号 (**+**)、マイナス記号 (**-**)、乗算記号 (**\**_)、または区分記号 (_*/**) ボタンを選択し、**計算式** フィールドに選択した TDS 税コードの計算式を入力します。</span><span class="sxs-lookup"><span data-stu-id="e3751-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3751-130">優先度 ID が **1** の TDS の税コードには、計算式を定義できません。</span><span class="sxs-lookup"><span data-stu-id="e3751-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="e3751-131">**計算式** フィールドで TDS 税コードの計算式を定義するには、**税** タブで使用できる TDS 税コードを追加します。**計算式** フィールドに TDS 税コードを追加するには、次の方法があります:</span><span class="sxs-lookup"><span data-stu-id="e3751-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="e3751-132">**税** タブから **計算式** フィールドに必要な税コードをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="e3751-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="e3751-133">**税** タブで必要な税コードをダブル タップ (またはダブル クリック) します。</span><span class="sxs-lookup"><span data-stu-id="e3751-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="e3751-134">**税** タブで必要な税コードを選択してホールド (または右クリック) し、**税コードの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3751-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3751-135">各 TDS 税コードの前に計算式を挿入します。</span><span class="sxs-lookup"><span data-stu-id="e3751-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="e3751-136">計算式に追加された TDS の税コードが括弧内 (\[...\]) に表示されています。</span><span class="sxs-lookup"><span data-stu-id="e3751-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="e3751-137">**計算式** フィールドの税コードに対して定義されている計算式をクリアするには、**C** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="e3751-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="e3751-138">**計算** タブでレコード 削除するには 、**削除** を選択 します。</span><span class="sxs-lookup"><span data-stu-id="e3751-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="e3751-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e3751-139">Close the page.</span></span>
