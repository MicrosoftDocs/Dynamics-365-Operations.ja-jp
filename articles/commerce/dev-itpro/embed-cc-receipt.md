---
title: 顧客のレシートにプロセッサのクレジット カードのレシートを埋め込む
description: このトピックでは、決済処理業者からのクレジットカードの領収書を顧客の項目別取引レシートに埋め込む方法について説明します。
author: rubendel
manager: annbe
ms.date: 04/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 04-31-2020
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 9b4ea930f6353585eb8535df54ccd7c5b87949fa
ms.sourcegitcommit: 728cd7f723ee821337eee315a27977e99a44d9d3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/11/2020
ms.locfileid: "3258664"
---
# <a name="embed-processor-credit-card-receipts-in-customer-receipts"></a><span data-ttu-id="95c2b-103">顧客のレシートにプロセッサのクレジット カードのレシートを埋め込む</span><span class="sxs-lookup"><span data-stu-id="95c2b-103">Embed processor credit card receipts in customer receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95c2b-104">このトピックでは、決済処理業者からのクレジットカードの領収書を顧客の項目別取引レシートに埋め込む方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-104">This topic explains how to embed credit card receipts from payment processors into a customer's itemized transaction receipt.</span></span> <span data-ttu-id="95c2b-105">この機能は、Microsoft Dynamics 365 Commerce バージョン 10.0.8 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="95c2b-105">This capability is available in Microsoft Dynamics 365 Commerce version 10.0.8 and later.</span></span>

## <a name="key-terms"></a><span data-ttu-id="95c2b-106">重要な用語</span><span class="sxs-lookup"><span data-stu-id="95c2b-106">Key terms</span></span>

| <span data-ttu-id="95c2b-107">期間</span><span class="sxs-lookup"><span data-stu-id="95c2b-107">Term</span></span> | <span data-ttu-id="95c2b-108">説明</span><span class="sxs-lookup"><span data-stu-id="95c2b-108">Description</span></span> |
|---|---|
| <span data-ttu-id="95c2b-109">顧客のレシート</span><span class="sxs-lookup"><span data-stu-id="95c2b-109">Customer's receipt</span></span> | <span data-ttu-id="95c2b-110">販売時点管理 (Point of Sale) でのキャッシュ アンド キャリー取引の際に発生するレシート。</span><span class="sxs-lookup"><span data-stu-id="95c2b-110">The receipt that is generated for a cash-and-carry transaction at the point of sale (POS).</span></span> |
| <span data-ttu-id="95c2b-111">顧客のクレジット カード レシート</span><span class="sxs-lookup"><span data-stu-id="95c2b-111">Customer's credit card receipt</span></span> | <span data-ttu-id="95c2b-112">クレジットカードの支払またはトランザクションで使用されるその他の電子支払のレコードとして印刷されるクレジットカード レシート。</span><span class="sxs-lookup"><span data-stu-id="95c2b-112">The credit card receipt that is printed as a record of the credit card payment or other electronic payment that is used in a transaction.</span></span> |

## <a name="overview"></a><span data-ttu-id="95c2b-113">概要</span><span class="sxs-lookup"><span data-stu-id="95c2b-113">Overview</span></span>

<span data-ttu-id="95c2b-114">このトピックでは、決済処理業者からのクレジットカードのレシートを顧客のレシートに直接埋め込むにあたって必要となる手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-114">This topic describes the steps that are required to embed the credit card receipt from a payment processor directly into a customer's receipt.</span></span> <span data-ttu-id="95c2b-115">Dynamics 365 Retail バージョン 10.0.7 およびそれ以前のバージョンでは、顧客のクレジットカードのレシートからいくつかの要素を顧客の項目別の取引レシートに埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="95c2b-115">In Dynamics 365 Retail version 10.0.7 and earlier, several elements from the customer's credit card receipt could be embedded into the customer's itemized transaction receipt.</span></span> <span data-ttu-id="95c2b-116">ただし、決済処理業者から取得した実際のレシートを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="95c2b-116">However, the actual receipt that comes from the payment processor could not be included.</span></span> <span data-ttu-id="95c2b-117">このソリューションは、すべての小売業者にとって受け入れられるものではありませんでした。なぜなら、顧客のクレジットカードのレシートに設定可能なレシートフィールドには、現地の法定要件で規定されているすべての詳細が含まれているとは限らなかったからです。</span><span class="sxs-lookup"><span data-stu-id="95c2b-117">That solution wasn't acceptable for all retailers, because the configurable receipt fields in the customer's credit card receipt didn't always include all the details that are stipulated by local statutory requirements.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="95c2b-118">必要条件</span><span class="sxs-lookup"><span data-stu-id="95c2b-118">Prerequisites</span></span>

<span data-ttu-id="95c2b-119">次の項目は、決済処理業者のクレジットカードのレシートを顧客のレシートに組み込むために必要です。</span><span class="sxs-lookup"><span data-stu-id="95c2b-119">The following items are required to embed processor credit card receipts into customer receipts:</span></span>

- <span data-ttu-id="95c2b-120">支払ソフトウェア開発キット (SDK) に準拠して実装される支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="95c2b-120">A payment connector that is implemented in accordance with the payments software development kit (SDK)</span></span>
- <span data-ttu-id="95c2b-121">プリンターとつながっている POS</span><span class="sxs-lookup"><span data-stu-id="95c2b-121">A POS that has a working printer</span></span>

## <a name="set-up-receipts"></a><span data-ttu-id="95c2b-122">レシートの設定</span><span class="sxs-lookup"><span data-stu-id="95c2b-122">Set up receipts</span></span>

1. <span data-ttu-id="95c2b-123">POSで、"レシートの形式" を検索して **レシートの形式** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="95c2b-123">In the POS, search for "receipt formats" to open the **Receipt formats** page.</span></span>
2. <span data-ttu-id="95c2b-124">POS で使用する**顧客のクレジットカード レシート**形式のレシートを選択します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-124">Select the receipt of the **Customer's credit card receipt** type that will be used at the POS.</span></span> <span data-ttu-id="95c2b-125">デモ データを使用している場合は、レシート形式に **3\_P** を選択し、**印刷の動作** フィールドを **印刷しない** に設定します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-125">If you're using demo data, select receipt format **3\_P**, and set the **Print Behavior** field to **Do not print**.</span></span>
3. <span data-ttu-id="95c2b-126">**デザイナー** を設定し、レシート デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="95c2b-126">Select **Designer** to open the receipt designer.</span></span>
4. <span data-ttu-id="95c2b-127">レシートの形式からすべてのフィールドを削除します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-127">Remove all the fields from the receipt format.</span></span>

    <span data-ttu-id="95c2b-128">レシートのセクションを編集するには、まず、レシート デザイナーの左ウィンドウの下部で、当該セクションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95c2b-128">To edit a section of the receipt, you must first select that section at the bottom of the left pane in the receipt designer.</span></span> <span data-ttu-id="95c2b-129">次に、[選択済] セクションで目的のレシートの変数を選択します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-129">Then select the desired receipt variable in the selected section.</span></span> <span data-ttu-id="95c2b-130">最後に、選択した変数を削除するには **、Alt + D** のキーボード ショートカットを使用します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-130">Finally, to delete the selected variable, you can use the **Alt+D** keyboard shortcut.</span></span>

5. <span data-ttu-id="95c2b-131">左ウィンドウの下部にある**ヘッダー** セクションを選択し、**EFTメッセージ**のレシートの変数をヘッダーにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="95c2b-131">Select the **Header** section at the bottom of the left pane, and then drag the **EFT Message** receipt variable into the header.</span></span>

    ![カード所有者のレシートのヘッダにおける EFT メッセージ変数](media/Cardholders.png)

6. <span data-ttu-id="95c2b-133">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-133">Select **Save**.</span></span>
7. <span data-ttu-id="95c2b-134">レシート デザイナーがまだ開いている場合は、左上隅にある **形式の選択** を選択してレシート セレクターを開きます。</span><span class="sxs-lookup"><span data-stu-id="95c2b-134">While the receipt designer is still open, select **Select format** in the upper-left corner to open the receipt selector.</span></span>
8. <span data-ttu-id="95c2b-135">レシート セレクターで、 POS で使用する **レシート** の形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-135">In the receipt selector, select the receipt of the **Receipt** type that will be used at the POS.</span></span> <span data-ttu-id="95c2b-136">デモ データを使用している場合は、レシート形式に **1\_p**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-136">If you're using demo data, select receipt format **1\_p**.</span></span>
9. <span data-ttu-id="95c2b-137">レシート デザイナーで、左ウィンドウの**下部**にあるフッター セクションを選択し、**カード支払/入金明細** のレシート変数をフッターにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="95c2b-137">In the receipt designer, select the **Footer** section at the bottom of the left pane, and then drag the **Card Tender Details** receipt variable into the footer.</span></span>

    ![顧客のレシートのフッターにおけるカードの支払/入金の詳細変数](media/customersreceipt.png)

10. <span data-ttu-id="95c2b-139">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-139">Select **Save**.</span></span>
11. <span data-ttu-id="95c2b-140">**1090** 配送スケジュールを使用して、変更をPOSに同期します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-140">Sync the changes to the POS by using the **1090** distribution schedule.</span></span>
12. <span data-ttu-id="95c2b-141">POS のシフトを閉じ、新しいシフトを開きます。</span><span class="sxs-lookup"><span data-stu-id="95c2b-141">Close the shift in the POS, and then open a new shift.</span></span>
13. <span data-ttu-id="95c2b-142">クレジットカード取引を実行して、決済処理業者のクレジット カード レシートが顧客のレシートに埋め込まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="95c2b-142">Perform a credit card transaction to confirm that the processor's credit card receipt is embedded into the customer's receipt.</span></span>

    ![クレジットカード情報が記載された顧客のレシート](media/receipt_w_cc.png)
