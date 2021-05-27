---
title: TDS 税タイプに対する源泉徴収税コードの設定
description: このトピックでは、源泉徴収税 (TDS) の税コードの設定方法について説明します。
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023400"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="1f636-103">TDS 税タイプに対する源泉徴収税コードの設定</span><span class="sxs-lookup"><span data-stu-id="1f636-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f636-104">このトピックでは、源泉徴収税 (TDS) の税コードの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1f636-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="1f636-105">**税 \> 間接税 \> 源泉徴収税 \> 源泉徴収税コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1f636-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="1f636-106">[![源泉徴収税コード ページ](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="1f636-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="1f636-107">アクション ペインで、**新規** を選択して、 TDS の源泉徴収税コードを作成し、必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f636-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="1f636-108">**一般** クイック タブの **税タイプ** フィールドで、**TDS** を選択して、税コードを TDS 税コードとして分類します。</span><span class="sxs-lookup"><span data-stu-id="1f636-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="1f636-109">**決済期間** フィールドで、TDS 税コードの TDS 決済プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="1f636-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="1f636-110">**主要勘定** フィールドで、TDS 金額を転記する勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f636-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="1f636-111">**売掛金勘定** フィールドで、販売トランザクションで控除されるTDS金額の転記が必要な売掛金勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f636-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="1f636-112">**発生元** フィールドは自動的に **総額の割合** に設定され、値を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="1f636-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f636-113">TDS 税タイプの税コードの発生元を **正味金額の割合** に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f636-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="1f636-114">**源泉徴収税コンポーネント** フィールドで、TDS 税コードの TDS 税コンポーネントを選択します。</span><span class="sxs-lookup"><span data-stu-id="1f636-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="1f636-115">アクション ペインで **値** を選択して、**源泉徴収税の値** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="1f636-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="1f636-116">**開始日** フィールドで、TDS 値の開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f636-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="1f636-117">**終了日** フィールドに終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f636-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f636-118">**最小制限**、**上限**、および **除外率** フィールドは、TDS 税タイプの税コードには使用できません。</span><span class="sxs-lookup"><span data-stu-id="1f636-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="1f636-119">**値** フィールドに、TDS 税コードの TDS の割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f636-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="1f636-120">**源泉徴収税の値** ページを閉じて、**源泉徴収税コード** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="1f636-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f636-121">**源泉徴収税コード** ページの **制限** ボタンは、TDS 税タイプの税コードには使用できません。</span><span class="sxs-lookup"><span data-stu-id="1f636-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="1f636-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1f636-122">Close the page.</span></span>
