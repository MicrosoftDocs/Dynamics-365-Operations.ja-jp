---
title: 'Adyen コネクタを使用した強力な顧客認証 (Strong Customer Authentication: SCA)'
description: このトピックでは、店舗内チェックアウトにおける強力な顧客認証 (SCA) について説明します。
author: rubendel
ms.date: 05/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 4045ea58844bc343ac594952fc77b1065bc7ab17
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797371"
---
# <a name="strong-customer-authentication-sca-using-the-adyen-connector"></a><span data-ttu-id="b9f44-103">Adyen コネクタを使用した強力な顧客認証 (Strong Customer Authentication: SCA)</span><span class="sxs-lookup"><span data-stu-id="b9f44-103">Strong Customer Authentication (SCA) using the Adyen connector</span></span>


[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9f44-104">このトピックでは、Adyen コネクタに組み込まれている強力な顧客認証 (SCA) サポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b9f44-104">This topic describes Strong Customer Authentication (SCA) support built into the Adyen connector.</span></span>

## <a name="key-terms"></a><span data-ttu-id="b9f44-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="b9f44-105">Key terms</span></span>

| <span data-ttu-id="b9f44-106">期間</span><span class="sxs-lookup"><span data-stu-id="b9f44-106">Term</span></span> | <span data-ttu-id="b9f44-107">説明</span><span class="sxs-lookup"><span data-stu-id="b9f44-107">Description</span></span> |
|---|---|
| <span data-ttu-id="b9f44-108">リダイレクト</span><span class="sxs-lookup"><span data-stu-id="b9f44-108">Redirect</span></span> | <span data-ttu-id="b9f44-109">オンラインの買い物客の閲覧セッションを、販売者の店舗外に移動するアクション。</span><span class="sxs-lookup"><span data-stu-id="b9f44-109">The action of moving an online shopper's browsing session out of the context of the merchant's storefront.</span></span> |
| <span data-ttu-id="b9f44-110">SCA</span><span class="sxs-lookup"><span data-stu-id="b9f44-110">SCA</span></span> | <span data-ttu-id="b9f44-111">強力な顧客認証。</span><span class="sxs-lookup"><span data-stu-id="b9f44-111">Strong Customer Authentication.</span></span> <span data-ttu-id="b9f44-112">電子決済方法で決済する場合、オンラインで買い物をする人は、オンライン ショッピング以外で認証を受けることを義務付ける EU 決済サービス指令 2.0 (Payment Services Directive 2.0: PSD 2.0) の一部。</span><span class="sxs-lookup"><span data-stu-id="b9f44-112">Part of the EU Payment Services Directive 2.0 (PSD2.0) that requires online shoppers to be authenticated outside of their online shopping experience when paying with an electronic payment method.</span></span> |
| <span data-ttu-id="b9f44-113">発行銀行</span><span class="sxs-lookup"><span data-stu-id="b9f44-113">Issuing bank</span></span> | <span data-ttu-id="b9f44-114">顧客に支払手段を発行する金融機関。</span><span class="sxs-lookup"><span data-stu-id="b9f44-114">The financial institution that issues a payment instrument to a customer.</span></span> |

## <a name="overview"></a><span data-ttu-id="b9f44-115">概要</span><span class="sxs-lookup"><span data-stu-id="b9f44-115">Overview</span></span>

<span data-ttu-id="b9f44-116">PSD 2.0 では、オンライン ショッピングのチェックアウト時に SCA がサポートされ、支払方法を発行した銀行が顧客を認証できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9f44-116">PSD2.0 requires that SCA be supported during online shopping checkout so a customer can be authenticated by the bank that issued their payment method.</span></span> <span data-ttu-id="b9f44-117">認証は、通常、買い物客がオンライン注文のためにチェックアウト中で、支払詳細を提供した後に行われます。</span><span class="sxs-lookup"><span data-stu-id="b9f44-117">The authentication commonly occurs when a shopper is going through the checkout for an online order and after they have provided their payment details.</span></span> <span data-ttu-id="b9f44-118">これらの詳細は評価され、PSD2.0 の条件に基づいて顧客が銀行にリダイレクトされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9f44-118">Those details are evaluated, and based on criteria provided by PSD2.0, the customer may be redirected to their bank.</span></span> <span data-ttu-id="b9f44-119">銀行にリダイレクトされた後、顧客は支払方法に対して認証されたユーザーであることを確定するために、何らかの形式の認証を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9f44-119">After being redirected to their bank, the customer is required to provide some form of authentication to confirm that they are an authorized user for the payment instrument.</span></span> <span data-ttu-id="b9f44-120">ユーザーがカード所有者であることが確認されると、支払が既に送信された店舗にリダイレクトされ、その後、チェックアウトの続行が許可されます。</span><span class="sxs-lookup"><span data-stu-id="b9f44-120">If the user is confirmed to be the cardholder, they are then redirected back to the storefront where the payment was previously submitted, after which checkout is allowed to proceed.</span></span> <span data-ttu-id="b9f44-121">SCA が失敗した場合、そのトランザクションに対してプロセスは続行できません。</span><span class="sxs-lookup"><span data-stu-id="b9f44-121">If SCA fails, the process will not allowed to continue for the transaction.</span></span>

## <a name="prerequisites-for-sca-support"></a><span data-ttu-id="b9f44-122">SCA サポートの前提条件</span><span class="sxs-lookup"><span data-stu-id="b9f44-122">Prerequisites for SCA support</span></span>

<span data-ttu-id="b9f44-123">SCA のサポートは、直ぐに使える [Adyen 向け Dynamics 365 Payment Connector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3) によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="b9f44-123">Support for SCA is provided by the out-of-box [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).</span></span> <span data-ttu-id="b9f44-124">これは、支払 SDK を使用するサード パーティ コネクタによって実装できます。</span><span class="sxs-lookup"><span data-stu-id="b9f44-124">This can be implemented by any third-party connector using the payments SDK.</span></span>

## <a name="setup"></a><span data-ttu-id="b9f44-125">セットアップ</span><span class="sxs-lookup"><span data-stu-id="b9f44-125">Setup</span></span>

<span data-ttu-id="b9f44-126">設定の詳細は、支払コネクタによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b9f44-126">Setup details will vary by payment connector.</span></span> <span data-ttu-id="b9f44-127">標準の Adyen コネクタに関連する設定の詳細については、Adyen コネクタ トピックの [E コマース セクション](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9f44-127">For setup details related to the out-of-box Adyen connector, see the [e-Commerce section](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce) of the Adyen connector topic.</span></span> 

## <a name="functional-experience"></a><span data-ttu-id="b9f44-128">機能のエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="b9f44-128">Functional experience</span></span>

<span data-ttu-id="b9f44-129">顧客が SCA にリダイレクトされると、通常、新しいブラウザ ウィンドウまたは iFrame 内で、銀行から課題が提出されます。</span><span class="sxs-lookup"><span data-stu-id="b9f44-129">When a customer is redirected for SCA, they will be presented with a challenge by their bank, typically within a new browser window or iFrame.</span></span> <span data-ttu-id="b9f44-130">認証されると、チェックアウト セッションにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="b9f44-130">After they have been authenticated, they will be redirected back to the checkout session.</span></span> <span data-ttu-id="b9f44-131">検証に失敗すると、チェックアウトを続行することはできません。</span><span class="sxs-lookup"><span data-stu-id="b9f44-131">If the validation fails, they will not be allowed to continue with checkout.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="b9f44-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b9f44-132">Additional resources</span></span>

- [<span data-ttu-id="b9f44-133">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b9f44-133">Payments FAQ</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [<span data-ttu-id="b9f44-134">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="b9f44-134">Dynamics 365 Payment Connector for Adyen</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [<span data-ttu-id="b9f44-135">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="b9f44-135">Checkout module</span></span>](https://docs.microsoft.com/dynamics365/commerce/add-checkout-module)


[!INCLUDE[footer-include](../includes/footer-banner.md)]