---
title: 支払の FAQ
description: このトピックでは、Dynamics 365 Commerce で使用できる支払いオプションについて説明します。
author: athinesh99
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 65801
ms.assetid: 99079d81-fde2-4432-8cee-82bbcc3bd57e
ms.search.region: Global
ms.author: athinesh
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: beb314ddd752ed1d9420a87fd0bdf4f4252449f0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004661"
---
# <a name="payments-faq"></a><span data-ttu-id="2d045-103">支払に関してよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="2d045-103">Payments FAQ</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="what-payment-scenarios-are-supported"></a><span data-ttu-id="2d045-104">どのような支払シナリオがサポートされますか ?</span><span class="sxs-lookup"><span data-stu-id="2d045-104">What payment scenarios are supported?</span></span>
- <span data-ttu-id="2d045-105">マーチャント口座を設定します。</span><span class="sxs-lookup"><span data-stu-id="2d045-105">Set up a merchant account.</span></span>
- <span data-ttu-id="2d045-106">コール センター注文を処理します。</span><span class="sxs-lookup"><span data-stu-id="2d045-106">Process a call center order.</span></span>
- <span data-ttu-id="2d045-107">オフライン注文を処理します。</span><span class="sxs-lookup"><span data-stu-id="2d045-107">Process an online order.</span></span>
- <span data-ttu-id="2d045-108">受諾ページを使用して、POS 現金払い取引を処理します。</span><span class="sxs-lookup"><span data-stu-id="2d045-108">Process a POS cash-and-carry transaction by using an accepting page.</span></span>
- <span data-ttu-id="2d045-109">受諾ページを使用して、POS 現金払い返品を処理します。</span><span class="sxs-lookup"><span data-stu-id="2d045-109">Process a POS cash-and-carry return by using an accepting page.</span></span>
- <span data-ttu-id="2d045-110">受諾ページを使用して、POS 現金払い返品を処理します。</span><span class="sxs-lookup"><span data-stu-id="2d045-110">Process a POS cash-and-carry return by using an accepting page.</span></span>
- <span data-ttu-id="2d045-111">受諾ページを使用して POS 顧客注文を処理します。</span><span class="sxs-lookup"><span data-stu-id="2d045-111">Process a POS customer order by using an accepting page.</span></span>
- <span data-ttu-id="2d045-112">Microsoft Dynamics AX 2012 Retail ハードウェア ステーションを使用して、POS 現金払いトランザクションを処理します。</span><span class="sxs-lookup"><span data-stu-id="2d045-112">Process a POS cash-and-carry transaction by using Microsoft Dynamics AX 2012 Retail Hardware Station.</span></span>
- <span data-ttu-id="2d045-113">ハードウェア ステーションを使用して、POS 現金払い返品を処理します。</span><span class="sxs-lookup"><span data-stu-id="2d045-113">Process a POS cash-and-carry return by using Hardware Station.</span></span>
- <span data-ttu-id="2d045-114">ハードウェア ステーションを使用して POS 顧客注文を処理します。</span><span class="sxs-lookup"><span data-stu-id="2d045-114">Process a POS customer order by using Hardware Station.</span></span>

        
## <a name="which-payment-providers-are-supported-and-in-what-regions"></a><span data-ttu-id="2d045-115">どの支払プロバイダーがどの地域でサポートされていますか。</span><span class="sxs-lookup"><span data-stu-id="2d045-115">Which payment providers are supported and in what regions?</span></span>
- <span data-ttu-id="2d045-116">Adyenはカードが存在する、またはカードが存在しない商取引に対応しています。</span><span class="sxs-lookup"><span data-stu-id="2d045-116">Adyen is supported for card present and card not present transactions.</span></span> <span data-ttu-id="2d045-117">対応している地域の一覧については、 [Adyen 向け Dynamics 365 Payment Connector の概要ページ](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d045-117">For a list of supported regions, visit the [Dynamics 365 Payment Connector for Adyen overview page](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3).</span></span>
- <span data-ttu-id="2d045-118">Verifoneは、カードが存在する取引 (デバイスを使用してを実行) 、およびカードが存在しない取引 (電子商取引やコールセンター取引など) のために米国でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2d045-118">Verifone is supported in the United States for transactions where the card is present (performed using devices), and for transactions where the card is not present (for example, e-commerce or call center transactions).</span></span>
- <span data-ttu-id="2d045-119">Mastercard Simplify は新しい顧客に対しては対応していません。</span><span class="sxs-lookup"><span data-stu-id="2d045-119">Mastercard Simplify is no longer supported for new customers.</span></span>


## <a name="what-is-a-payment-connector-and-in-what-cases-do-i-need-to-deploy-and-implement-a-payment-connector"></a><span data-ttu-id="2d045-120">支払コネクタとは何ですか、またどのような場合に支払コネクタの配置と実装が必要ですか ?</span><span class="sxs-lookup"><span data-stu-id="2d045-120">What is a payment connector and in what cases do I need to deploy and implement a payment connector?</span></span>
<span data-ttu-id="2d045-121">支払コネクタは、カードが存在しないトランザクションとカードが存在するトランザクションの支払いをアプリケーションが処理できるようにする、設定可能なソフトウェア コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="2d045-121">Payment connectors are software components that can be set up which enable an application to process payments for transactions where the card is not present and transactions where the card is present.</span></span>

<span data-ttu-id="2d045-122">Verifone および Adyen などの Microsoft によって指定されたコネクタを使用するか、または ISV パートナーがカスタム コネクタを開発することができます。</span><span class="sxs-lookup"><span data-stu-id="2d045-122">Microsoft-provided connectors such as Verifone and Adyen can be used, or custom connectors can be built by ISV partners.</span></span> <span data-ttu-id="2d045-123">コネクタは通常、顧客の業務でのニーズを満たすために構築されます。</span><span class="sxs-lookup"><span data-stu-id="2d045-123">A connector is typically built to meet the business needs of a customer.</span></span> <span data-ttu-id="2d045-124">新しいタイプの支払いタイプ (リンク払い戻しなど) が必要なシナリオがある場合、カスタム コネクタが作成されることがあります。</span><span class="sxs-lookup"><span data-stu-id="2d045-124">Custom connectors are often created when there is a scenario that requires a new type of payment type (for example, linked refunds).</span></span> <span data-ttu-id="2d045-125">特定の地域でビジネスを行っている顧客は、最初から用意されているコネクタがこれらの地域をサポートしていない場合、新しいコネクタが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="2d045-125">Customers doing business in certain geographies may need new connectors if the out-of-box connectors do not support those regions.</span></span>
          
## <a name="are-other-payment-connector-providers-supported"></a><span data-ttu-id="2d045-126">その他の支払コネクタ プロバイダーはサポートされていますか。</span><span class="sxs-lookup"><span data-stu-id="2d045-126">Are other payment connector providers supported?</span></span>
<span data-ttu-id="2d045-127">はい、ただしカスタマイズを使用してそれらを接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d045-127">Yes, but you must connect them using customization.</span></span>

## <a name="what-is-the-service-level-agreement-sla-for-out-of-box-payment-connectors-like-verifone-and-adyen"></a><span data-ttu-id="2d045-128">Verifone および Adyen などの革新的な支払いコネクタ の サービス レベル アグリーメント (SLA) はどうなっているか ?</span><span class="sxs-lookup"><span data-stu-id="2d045-128">What is the Service level agreement (SLA) for out-of-box payment connectors like Verifone and Adyen?</span></span>
<span data-ttu-id="2d045-129">Verifone のコネクタに対するSLAは、Verifoneによって管理されています。</span><span class="sxs-lookup"><span data-stu-id="2d045-129">The SLA for the out-of-box Verifone connector is owned by Verifone.</span></span> <span data-ttu-id="2d045-130">Verifone の SLA については、Verifone のサポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="2d045-130">Please contact Verifone support for information about their SLA.</span></span> <span data-ttu-id="2d045-131">Adyenコネクタに関して、設定に関する問題の場合は Adyenコネクタの [概要ページ](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d045-131">For the Adyen connector, refer to the Adyen connector [overview page](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) if the issue is related to setup.</span></span> <span data-ttu-id="2d045-132">コネクタに関するその他の設定、または機能の問題については、Microsoftへのサポートリクエストを作成してください。</span><span class="sxs-lookup"><span data-stu-id="2d045-132">For other setup or functional issues with the connector itself, create a support request with Microsoft.</span></span> <span data-ttu-id="2d045-133">問題がデバイス本体、またはAdyenの処理サービスに起因する場合は、support-dynamics365@adyen.com Adyenのサポートに連絡してください。</span><span class="sxs-lookup"><span data-stu-id="2d045-133">If the issue is originating from the device itself or Adyen's processing service, contact Adyen support at support-dynamics365@adyen.com.</span></span> 
        
## <a name="if-a-supported-payment-provider-issues-an-update-will-microsoft-automatically-update-the-payment-connector-or-do-i-need-to-work-with-the-payment-provider-to-get-the-updated-payment-connector"></a><span data-ttu-id="2d045-134">サポートされている支払プロバイダーが更新プログラムを発行した場合は、Microsoft は自動的に支払コネクタを更新してくれますか? または更新された支払コネクタを取得するために支払プロバイダーと連携する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="2d045-134">If a supported payment provider issues an update, will Microsoft automatically update the payment connector or do I need to work with the payment provider to get the updated payment connector?</span></span>
<span data-ttu-id="2d045-135">支払いコネクターの更新プログラムが支払コネクター プロバイダーによって発行された場合、支払いコネクターの更新バージョンは Dynamics 365 Commerce の次の予定リリースに含まれます。</span><span class="sxs-lookup"><span data-stu-id="2d045-135">If a payment connector update is issued by the payment connector provider, the updated version of the payment connector will be included in the next planned release of Dynamics 365 Commerce.</span></span> <span data-ttu-id="2d045-136">ただし、顧客は早期に取得するため、支払コネクタ プロバイダと直接作業することもできます。</span><span class="sxs-lookup"><span data-stu-id="2d045-136">However, the customer can also work directly with the payment connector provider to uptake it earlier.</span></span>

        
<span data-ttu-id="2d045-137">関連トピック:</span><span class="sxs-lookup"><span data-stu-id="2d045-137">Related topics:</span></span> 
- [<span data-ttu-id="2d045-138">支払端末のエンド・ツー・エンド支払統合を作成する</span><span class="sxs-lookup"><span data-stu-id="2d045-138">Create an end-to-end payment integration for a payment terminal</span></span>](end-to-end-payment-extension.md)
- [<span data-ttu-id="2d045-139">支払コネクタの配置</span><span class="sxs-lookup"><span data-stu-id="2d045-139">Deploy payment connectors</span></span>](deploy-payment-connector.md)
- [<span data-ttu-id="2d045-140">支払コネクタ用の Windows インストーラーの作成</span><span class="sxs-lookup"><span data-stu-id="2d045-140">Create Windows installers for payment connectors</span></span>](create-windows-installer-payment-connector.md)
- [<span data-ttu-id="2d045-141">Verifone 支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="2d045-141">Verifone Payment Connector</span></span>](https://dynamics.verifone.com/repo/)

