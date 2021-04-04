---
title: 次回の支払のために保存するオプションが表示されない
description: このトピックでは、e コマース サイトのチェックアウト ページで次回の支払のために保存するチェック ボックスが e コマース サイトのチェックアウト ページの支払方法で表示されない場合に役立つトラブルシューティング ガイドを示します。
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
ms.openlocfilehash: 3a4fbcd522651ed1b82b72b751ff6ead44c94a71
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585413"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="f6023-103">「次回の支払のために保存する」 オプションが表示されない</span><span class="sxs-lookup"><span data-stu-id="f6023-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6023-104">このトピックでは、**次回の支払のために保存する** チェック ボックスが e コマース サイトのチェックアウト ページの **支払方法** の下に表示されない場合に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="f6023-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="f6023-105">説明</span><span class="sxs-lookup"><span data-stu-id="f6023-105">Description</span></span>

<span data-ttu-id="f6023-106">**次回の支払のために保存する** チェックボックスは e コマース サイトのチェックアウト ページの **支払方法** セクションに表示されません。</span><span class="sxs-lookup"><span data-stu-id="f6023-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="f6023-107">次の図は、**次回の支払のために保存する** チェック ボックスを含むチェックアウト ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f6023-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![支払いモジュールの次回の支払のために保存するチェック ボックス](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="f6023-109">解像度</span><span class="sxs-lookup"><span data-stu-id="f6023-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="f6023-110">Commerce 本社で Ayden 向け Dynamics 365 Payment Connector が正しく構成されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="f6023-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="f6023-111">Commerce 本社で Ayden 向け Dynamics 365 Payment Connector が正しく構成されていることを確認するためには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f6023-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f6023-112">**Retail と Commerce \>チャネル\>オンライン ストア** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f6023-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="f6023-113">オンライン ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="f6023-113">Select the online store.</span></span>
1. <span data-ttu-id="f6023-114">**支払口座** クイック タブで **e コマースでの支払情報の保存を許可する** フィールドが **True** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f6023-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Commerce 本部で e コマース フィールドに支払情報の保存を許可する](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="f6023-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f6023-116">Additional resources</span></span>

[<span data-ttu-id="f6023-117">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="f6023-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="f6023-118">オンライン支払手段を Adyen コネクタで保存</span><span class="sxs-lookup"><span data-stu-id="f6023-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)