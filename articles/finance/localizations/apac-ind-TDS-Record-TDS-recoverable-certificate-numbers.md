---
title: TDS 復元可能証明書番号の記録
description: このトピックでは、[復元可能な証明書] ページを使用して、特定の仕入先、顧客、または元帳について受け取る源泉徴収 (TDS) 証明書の証明書番号と日付を記録する方法について説明します。
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023374"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="24759-103">TDS 復元可能証明書番号の記録</span><span class="sxs-lookup"><span data-stu-id="24759-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24759-104">このトピックでは、**復元可能な証明書** ページを使用して、特定の仕入先、顧客、または元帳について受け取る源泉徴収 (TDS) 証明書の証明書番号と日付を記録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="24759-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="24759-105">このページでTDSトランザクションについて記録されたTDS証明書番号と日付を更新するには、**証明書の更新** ページ (**一般会計 \>定期処理 \> 源泉徴収税 \> 更新証明書**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="24759-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="24759-106">TDS 証明書番号の更新完了後は、それらを閉じます。</span><span class="sxs-lookup"><span data-stu-id="24759-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="24759-107">TDS 証明書番号と日付けを取得して記録するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="24759-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="24759-108">**税 \> 間接税 \> 源泉徴収税 \> 復元可能証明書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="24759-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="24759-109">[![復元可能な証明書ページ](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="24759-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="24759-110">**回収可能な証明書** ページの **税タイプ** フィールドで 、**TDS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24759-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="24759-111">**新規** を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="24759-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="24759-112">**証明書番号** フィールドに、TDS 特約証明書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="24759-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="24759-113">**勘定タイプ** フィールドで、TDS 証明書を受け取る勘定のタイプ (**仕入先r**、**顧客**、**元帳**)を選択します。</span><span class="sxs-lookup"><span data-stu-id="24759-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="24759-114">**勘定** フィールドでは、選択した勘定タイプに応じて仕入先、顧客、または勘定科目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="24759-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="24759-115">**名前** フィールドには、仕入先、顧客、または勘定科目の名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="24759-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="24759-116">**証明書の金額** フィールドに、TDS 証明書の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="24759-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="24759-117">**日付け** フィールドに、証明書番号の証明書日付けを入力します。</span><span class="sxs-lookup"><span data-stu-id="24759-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="24759-118">**照会** を選択すると、**証明書トランザクション** ページが開き、ここでは、TDS 証明書の番号と日付が更新された TDS 取引を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="24759-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="24759-119">この情報は、**証明書の更新** ページ (**税 \> 申告\> 源泉徴収税 \> 更新証明書**) で更新できます 。</span><span class="sxs-lookup"><span data-stu-id="24759-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="24759-120">**証明書の更新** ページには、各 TDS トランザクションについて次の情報が表示されます:</span><span class="sxs-lookup"><span data-stu-id="24759-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="24759-121">**日付** – TDS 取引の転記日付です。</span><span class="sxs-lookup"><span data-stu-id="24759-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="24759-122">**伝票** – TDS 取引の伝票番号を表示します。</span><span class="sxs-lookup"><span data-stu-id="24759-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="24759-123">**ソース** - TDS 取引が作成されたモジュールです。</span><span class="sxs-lookup"><span data-stu-id="24759-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="24759-124">**勘定** – TDS 取引が作成された仕入先、顧客、または勘定科目番号です。</span><span class="sxs-lookup"><span data-stu-id="24759-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="24759-125">**名前** – TDS 取引が作成された仕入先、顧客、または元帳アカウントの名前です。</span><span class="sxs-lookup"><span data-stu-id="24759-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="24759-126">**金額** – TDSが計算された請求書の金額です。</span><span class="sxs-lookup"><span data-stu-id="24759-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="24759-127">**税額** - 取引に対して計算された TDS の税額です。</span><span class="sxs-lookup"><span data-stu-id="24759-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="24759-128">**証明書の日付** - TDS 取引に対して更新された TDS 証明書の日付です。</span><span class="sxs-lookup"><span data-stu-id="24759-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="24759-129">**証明書番号** - TDS 取引に対して更新された TDS 証明書番号です。</span><span class="sxs-lookup"><span data-stu-id="24759-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="24759-130">**復元可能な証明書** ページで、**終了済** チェック ボックスをオンにして、**証明書の更新** ページで TDS 取引の更新が完了した後に TDS 証明書番号を閉じます。</span><span class="sxs-lookup"><span data-stu-id="24759-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="24759-131">ページのすべてのレコードに対して **終了済** チェック ボックスをオンにするには、**すべてマークする** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="24759-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="24759-132">**証明書の更新** ページで **終了済** チェック ボックスがオンにされている TDS 証明書番号は使用できません。</span><span class="sxs-lookup"><span data-stu-id="24759-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
