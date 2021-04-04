---
title: 返品注文の払戻が拒否される
description: このトピックでは、請求に使用されるクレジット カードが、元の支払認証時に使用されたカードと異なるため、返品注文の払戻が拒否された場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e202c6b4b9e025d5af1cd5eb6235884aab6444e6
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585417"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="ca9c3-103">返品注文の払戻が拒否される</span><span class="sxs-lookup"><span data-stu-id="ca9c3-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca9c3-104">このトピックでは、請求に使用されるクレジット カードが、元の支払認証時に使用されたカードと異なるため、返品注文の払戻が拒否された場合に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="ca9c3-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="ca9c3-105">説明</span><span class="sxs-lookup"><span data-stu-id="ca9c3-105">Description</span></span>

<span data-ttu-id="ca9c3-106">返品注文の請求に使用されるクレジット カードが、元の支払認証時に使用されたカードと異なる場合、払戻は拒否されます。</span><span class="sxs-lookup"><span data-stu-id="ca9c3-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="ca9c3-107">次のエラーメッセージが表示されます。「一部の支払が転記に対して正しいステータスではありません。</span><span class="sxs-lookup"><span data-stu-id="ca9c3-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="ca9c3-108">請求する前に、すべての支払のステータスを再検証してください。」</span><span class="sxs-lookup"><span data-stu-id="ca9c3-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="ca9c3-109">支払承認の詳細には、次のエラー メッセージが含まれます。「Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);」</span><span class="sxs-lookup"><span data-stu-id="ca9c3-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![返品注文のエラーで払戻が拒否される](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="ca9c3-111">解像度</span><span class="sxs-lookup"><span data-stu-id="ca9c3-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="ca9c3-112">Adyen のブラインド返品の有効化</span><span class="sxs-lookup"><span data-stu-id="ca9c3-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="ca9c3-113">ブラインド返品を有効にするには、[Adyen 向け Dynamics 365 Payment Connector の問題のトラブルシューティング](adyen-support.md) の手順に従って、Adyen サポート チームに連絡し、Adyen のマーチャント口座でブラインド返品を有効にするように要求します。</span><span class="sxs-lookup"><span data-stu-id="ca9c3-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca9c3-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ca9c3-114">Additional resources</span></span>

[<span data-ttu-id="ca9c3-115">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="ca9c3-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="ca9c3-116">Dynamics 365 の Adyen 支払コネクタを設定</span><span class="sxs-lookup"><span data-stu-id="ca9c3-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)