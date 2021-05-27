---
title: TDS 支払および TDS 清算期間に対して転記されたトランザクションの表示
description: このトピックでは、決済期間に転記された源泉徴収税 (TDS) の支払およびトランザクションでを表示する方法について説明します。
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 2bada42073e46c69101e6d31f3328a2eeb95f880
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023381"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a><span data-ttu-id="54f26-103">TDS 支払および TDS 清算期間に対して転記されたトランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="54f26-103">View posted TDS payments and transactions for a TDS settlement period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54f26-104">このトピックでは、決済期間に転記された源泉徴収税 (TDS) の支払およびトランザクションでを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="54f26-104">This topic explains how to view the Tax Deducted at Source (TDS) payments and transactions that were posted for a settlement period.</span></span>

1. <span data-ttu-id="54f26-105">**税 \> 間接税 \> 源泉徴収税 \> 源泉徴収税決済期間** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="54f26-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="54f26-106">[![源泉徴収税の背取るメント期間ページ](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span><span class="sxs-lookup"><span data-stu-id="54f26-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span></span>

2. <span data-ttu-id="54f26-107">**源泉徴収税の精算期間** ページで、**源泉徴収税の支払い** を選択して **源泉徴収税の支払** ページを開き、特定の TDS 決済期間に対して行われた TDS 決済を表示できます。</span><span class="sxs-lookup"><span data-stu-id="54f26-107">On the **Withholding tax settlement periods** page, select **Withholding tax payments** to open the **Withholding tax payments** page, where you can view the TDS settlements that were made for a specific TDS settlement period.</span></span>

    <span data-ttu-id="54f26-108">**概要** タブには次の情報が表示されます:</span><span class="sxs-lookup"><span data-stu-id="54f26-108">The **Overview** tab shows the following information:</span></span>

    - <span data-ttu-id="54f26-109">**日付** – TDS 決済の日付。</span><span class="sxs-lookup"><span data-stu-id="54f26-109">**Date** – The date of TDS settlement.</span></span>
    - <span data-ttu-id="54f26-110">**伝票** – TDS 決済取引の伝票番号。</span><span class="sxs-lookup"><span data-stu-id="54f26-110">**Voucher** – The voucher number of the TDS settlement transaction.</span></span>
    - <span data-ttu-id="54f26-111">**税タイプ** - 決済プロセスが実行される税タイプ。</span><span class="sxs-lookup"><span data-stu-id="54f26-111">**Tax type** – The tax type that the settlement process is run for.</span></span>
    - <span data-ttu-id="54f26-112">**税勘定番号 (TAN)** - 決算済 TDS トランザクションの税勘定番号。</span><span class="sxs-lookup"><span data-stu-id="54f26-112">**Tax Account Number (TAN)** – The Tax Account Number (TAN) of the settled TDS transaction.</span></span>
    - <span data-ttu-id="54f26-113">**決済期間** - 決済プロセスを実行する TDS の決済期間。</span><span class="sxs-lookup"><span data-stu-id="54f26-113">**Settlement period** – The settlement period that the TDS settlement process is run for.</span></span>
    - <span data-ttu-id="54f26-114">**開始日** - 決済期間の開始日。</span><span class="sxs-lookup"><span data-stu-id="54f26-114">**From date** – The start date of the settlement period.</span></span>
    - <span data-ttu-id="54f26-115">**終了日** - 決済期間の終了日。</span><span class="sxs-lookup"><span data-stu-id="54f26-115">**To date** – The end date of the settlement period.</span></span>
    - <span data-ttu-id="54f26-116">**源泉徴収税の支払バージョン** -  源泉徴収税支払のバージョン: **元の**、**最新の訂正**、または **合計リスト**。</span><span class="sxs-lookup"><span data-stu-id="54f26-116">**Withholding tax payment version** – The version of the withholding tax payment: **Original**, **Latest corrections**, or **Total list**.</span></span>

5. <span data-ttu-id="54f26-117">TDS トランザクションの伝票エントリを表示するには、**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54f26-117">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
6. <span data-ttu-id="54f26-118">精算期間中に特定の期間に決済された TDS トランザクションの詳細を表示するには、**源泉徴収税トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54f26-118">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for a specific period during a settlement period.</span></span> <span data-ttu-id="54f26-119">TDS トランザクションの伝票エントリを表示するには、**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54f26-119">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span> <span data-ttu-id="54f26-120">特定の TDS 税コードの TDS 税要素ごとに計算された TDS を表示するには、**源泉徴収税コンポーネント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54f26-120">Select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>
7. <span data-ttu-id="54f26-121">**源泉徴収税の支払** ページを閉じて、**源泉徴収税の精算期間** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="54f26-121">Close the **Withholding tax payments** page to return to the **Withholding tax settlement periods** page.</span></span>
8. <span data-ttu-id="54f26-122">精算期間中に特定の期間に決済された TDS トランザクションの詳細を表示するには、**源泉徴収税トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54f26-122">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for the settlement period.</span></span>
