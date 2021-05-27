---
title: 伝票が生成されない
description: このトピックでは、伝票を生成する必要があるが、生成しない場合に役立つトラブルシューティング情報を提供します。
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ba23b597b1d7d283b99638fb7d5d91da00afb09c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018760"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="ad964-103">伝票が生成されない</span><span class="sxs-lookup"><span data-stu-id="ad964-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad964-104">伝票を生成する必要があるのに、**伝票トランザクション** ページに伝票が表示されない場合、この問題のトラブルシューティングを行うには、必要に応じて次のセクションの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="ad964-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="ad964-105">[![伝票がない伝票トランザクション ページ](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="ad964-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="ad964-106">税の適用性の確認</span><span class="sxs-lookup"><span data-stu-id="ad964-106">Check the tax applicability</span></span>

1. <span data-ttu-id="ad964-107">**税金** \> **定期処理のタスク** \> **まだ転送されていない補助元帳仕訳エントリ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad964-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="ad964-108">仕訳帳レコードがある場合は、それを選択して、**今すぐ転送** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad964-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="ad964-109">[![まだ転送されていない補助元帳仕訳エントリ ページの今すぐ転送ボタン](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="ad964-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="ad964-110">**伝票トランザクション** ページを再度開き、伝票が生成されたかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ad964-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="ad964-111">カスタマイズが存在するかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="ad964-111">Determine whether customization exists</span></span>

<span data-ttu-id="ad964-112">前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ad964-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="ad964-113">カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="ad964-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
