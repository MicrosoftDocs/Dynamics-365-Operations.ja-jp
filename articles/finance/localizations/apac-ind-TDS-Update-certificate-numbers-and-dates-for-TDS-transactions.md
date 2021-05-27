---
title: (TDS) トランザクションの証明書番号および日付の更新
description: このトピックでは、ソース (TDS) における、源泉徴収のための仕入先、顧客、または元帳のアカウントのために記録された復元可能な証明書番号と日付を方針する方法について説明します。
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023384"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="0a963-103">(TDS) トランザクションの証明書番号および日付の更新</span><span class="sxs-lookup"><span data-stu-id="0a963-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a963-104">このトピックでは、ソース (TDS) における、源泉徴収のための仕入先、顧客、または元帳のアカウントのために記録された復元可能な証明書番号と日付を方針する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a963-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="0a963-105">**復元可能な証明書** ページ上の TDS トランザクションの証明書を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="0a963-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="0a963-106">**証明書の更新** ページを使用することで、証明書 を更新できます。</span><span class="sxs-lookup"><span data-stu-id="0a963-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="0a963-107">TDS トランザクションの証明書番号と日付けを更新するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0a963-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="0a963-108">**税 \> 申告 \> 源泉徴収税 \> 証明書の更新** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0a963-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="0a963-109">[![証明書ページの更新](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="0a963-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="0a963-110">**証明書の更新** ページの **選択** セクションの、**税タイプ** フィールドで、**TDS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a963-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="0a963-111">**証明書番号** フィールドで、顧客または仕入先の TDS 証明書番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a963-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0a963-112">**証明書番号** フィールドには、**回収可能な証明書** ページで **終了** チェック ボックスがオフに設定された TDS 証明書番号 だけが表示 されます。</span><span class="sxs-lookup"><span data-stu-id="0a963-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="0a963-113">**証明書の日付** フィールドで、証明書の日付を表示します。</span><span class="sxs-lookup"><span data-stu-id="0a963-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="0a963-114">**勘定タイプ** フィールドには TDS 証明書番号を受け取る勘定のタイプが表示され、**名前** フィールドには勘定の名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a963-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="0a963-115">**開始日** フィールドおよび **終了日** フィールドに、TDS トランザクションの目的を表示するための開始日と終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a963-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="0a963-116">選択した期間中に転記された TDS トランザクションを表示するには、**データの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a963-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="0a963-117">**概要** タブの上部ウィンドウのグリッドには、選択した期間中に仕入先または顧客に対して転記された各 TDS トランザクションに関する次の情報 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a963-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="0a963-118">**伝票** – TDS 取引の伝票番号を表示します。</span><span class="sxs-lookup"><span data-stu-id="0a963-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="0a963-119">**日付** – TDS トランザクションの日付です。</span><span class="sxs-lookup"><span data-stu-id="0a963-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="0a963-120">**金額** – TDSが計算された請求書の金額です。</span><span class="sxs-lookup"><span data-stu-id="0a963-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="0a963-121">**税額** - 取引に対して計算された TDS の税額です。</span><span class="sxs-lookup"><span data-stu-id="0a963-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="0a963-122">特定の TDS トランザクションを上部グリッドから下部グリッドに移動するには、トランザクションを選択し、**含める** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a963-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="0a963-123">または、**すべて含める** を選択すると、すべての TDS トランザクションが上部グリッドから下部グリッドに移動します。</span><span class="sxs-lookup"><span data-stu-id="0a963-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="0a963-124">特定の TDS トランザクションまたはすべての TDS トランザクションを下部グリッドから上部グリッドに移動するには、**すべて除外** ボタンまたは **すべて除外** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="0a963-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="0a963-125">下部グリッドの TDS トランザクションの **証明書番号** フィールドおよび **証明書の日付** フィールドを更新するには、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a963-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="0a963-126">**税 \> 間接税 \> 源泉徴収税 \> 回復可能な証明書** に移動し、**照会** を選択して、**証明書トランザクション** ページに新しい証明書番号を持つ更新されたトランザクション明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="0a963-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="0a963-127">[![証明書トランザクション ページ](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="0a963-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
