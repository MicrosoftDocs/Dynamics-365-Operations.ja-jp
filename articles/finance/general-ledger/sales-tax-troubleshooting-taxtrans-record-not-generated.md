---
title: TaxTrans レコードが生成されない
description: このトピックでは、TaxTrans レコードが生成されない場合に役立つトラブルシューティング情報を提供します。
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947667"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="97877-103">TaxTrans レコードが生成されない</span><span class="sxs-lookup"><span data-stu-id="97877-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97877-104">トランザクションの **転記済売上税** を選択したが、**転記済売上税** ページに税明細行が表示されていないか、税明細行がない場合は、**TaxTrans** レコードが生成されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="97877-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="97877-105">[![明細行がない品目の転記済売上税ページ](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="97877-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="97877-106">この問題のトラブルシューティングを行う場合は、必要に応じて次のセクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="97877-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="97877-107">トランザクションを転記する前に売上税を確認する</span><span class="sxs-lookup"><span data-stu-id="97877-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="97877-108">トランザクションを転記する前に、**請求の転記** ページで、**売上税** を選択して計算を確認します。</span><span class="sxs-lookup"><span data-stu-id="97877-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="97877-109">[![請求の転記ページの売上税ボタン](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="97877-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="97877-110">**一時的な売上税トランザクション** ページで、計算の結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="97877-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="97877-111">税金が計算されない場合は、[税金が計算されない、または税額がゼロ](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97877-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="97877-112">すべての転記済売上税での TaxTrans レコードの検索</span><span class="sxs-lookup"><span data-stu-id="97877-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="97877-113">**税** \> **照会およびレポート** \> **売上税の照会** > **転記済売上税** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="97877-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="97877-114">**伝票** 列のヘッダーで、フィルター記号を選択して **TaxTrans** レコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="97877-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="97877-115">探している売上税レコードが見つかった場合は、日付を確認します。</span><span class="sxs-lookup"><span data-stu-id="97877-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="97877-116">日付が仕訳帳ヘッダーの日付と異なる場合は、追加のサポートを求める Microsoft サービス要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="97877-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="97877-117">[![転記済売上税ページ](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="97877-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="97877-118">詳細を確認するためにデバッグする</span><span class="sxs-lookup"><span data-stu-id="97877-118">Debug to check details</span></span>

1. <span data-ttu-id="97877-119">**TmpTaxWorkTrans** と **TaxUncommitted** が正しく生成されているかどうかをデバッグして決定する方法については、[TaxTrans のフィールド値が正しくない](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97877-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="97877-120">**TaxTmpWorkTrans** または **TaxUncommitted** が正しく生成されている場合は、**TaxPost::SaveAndPost()** および **Tax::SaveAndPost** でブレークポイントを追加して、**TaxTrans** が挿入されない理由をデバッグします。</span><span class="sxs-lookup"><span data-stu-id="97877-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="97877-121">[![コードに追加されたブレークポイント](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="97877-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="97877-122">[![追加されたブレークポイントの結果](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="97877-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="97877-123">カスタマイズが存在するかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="97877-123">Determine whether customization exists</span></span>

<span data-ttu-id="97877-124">前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="97877-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="97877-125">カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="97877-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
