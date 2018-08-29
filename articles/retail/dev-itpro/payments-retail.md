---
title: "支払の FAQ"
description: "このトピックでは、Dynamics 365 for Operations for Retail で使用できる支払オプションについて説明します。"
author: athinesh99
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 65801
ms.assetid: 99079d81-fde2-4432-8cee-82bbcc3bd57e
ms.search.region: Global
ms.author: athinesh
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0e1be78baa0deee7f86a21ed23b1990ff4215907
ms.openlocfilehash: 296f9aec795432254f965a09028b1d797f451af0
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="payments-faq"></a><span data-ttu-id="36e6e-103">支払の FAQ</span><span class="sxs-lookup"><span data-stu-id="36e6e-103">Payments FAQ</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="what-payment-scenarios-are-supported"></a><span data-ttu-id="36e6e-104">どのような支払シナリオがサポートされますか ?</span><span class="sxs-lookup"><span data-stu-id="36e6e-104">What payment scenarios are supported?</span></span>
- <span data-ttu-id="36e6e-105">マーチャント口座を設定します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-105">Set up a merchant account.</span></span>
- <span data-ttu-id="36e6e-106">コール センター注文を処理します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-106">Process a call center order.</span></span>
- <span data-ttu-id="36e6e-107">オフライン注文を処理します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-107">Process an online order.</span></span>
- <span data-ttu-id="36e6e-108">受諾ページを使用して、POS 現金払い取引を処理します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-108">Process a POS cash-and-carry transaction by using an accepting page.</span></span>
- <span data-ttu-id="36e6e-109">受諾ページを使用して、POS 現金払い返品を処理します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-109">Process a POS cash-and-carry return by using an accepting page.</span></span>
- <span data-ttu-id="36e6e-110">受諾ページを使用して、POS 現金払い返品を処理します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-110">Process a POS cash-and-carry return by using an accepting page.</span></span>
- <span data-ttu-id="36e6e-111">受諾ページを使用して POS 顧客注文を処理します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-111">Process a POS customer order by using an accepting page.</span></span>
- <span data-ttu-id="36e6e-112">Microsoft Dynamics AX 2012 Retail ハードウェア ステーションを使用して、POS 現金払いトランザクションを処理します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-112">Process a POS cash-and-carry transaction by using Microsoft Dynamics AX 2012 Retail Hardware Station.</span></span>
- <span data-ttu-id="36e6e-113">ハードウェア ステーションを使用して、POS 現金払い返品を処理します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-113">Process a POS cash-and-carry return by using Hardware Station.</span></span>
- <span data-ttu-id="36e6e-114">ハードウェア ステーションを使用して POS 顧客注文を処理します。</span><span class="sxs-lookup"><span data-stu-id="36e6e-114">Process a POS customer order by using Hardware Station.</span></span>

        
## <a name="which-payment-providers-are-supported-and-in-what-regions"></a><span data-ttu-id="36e6e-115">どの支払プロバイダーがどの地域でサポートされていますか。</span><span class="sxs-lookup"><span data-stu-id="36e6e-115">Which payment providers are supported and in what regions?</span></span>
- <span data-ttu-id="36e6e-116">Verifoneは、カードが存在する取引 (デバイスを使用してを実行) 、およびカードが存在しない取引 (電子商取引やコールセンター取引など) のために米国でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="36e6e-116">Verifone is supported in the United States for transactions where the card is present (performed using devices), and for transactions where the card is not present (for example, e-commerce or call center transactions).</span></span>
- <span data-ttu-id="36e6e-117">カードが次の国に存在しない場合、トランザクションでは Mastercard がサポートされています: オーストラリア、カナダ、デンマーク、フランス、ドイツ、アイスランド、アイルランド、メキシコ、オランダ、ニュージーランド、南アフリカ、英国、および米国。</span><span class="sxs-lookup"><span data-stu-id="36e6e-117">Mastercard is supported for transactions where the card is not present in the following countries: Australia, Canada, Denmark, France, Germany, Iceland, Ireland, Mexico, Netherlands, New Zealand, South Africa, United Kingdom, and United States.</span></span>


## <a name="what-is-a-payment-connector-and-in-what-cases-do-i-need-to-deploy-and-implement-a-payment-connector"></a><span data-ttu-id="36e6e-118">支払コネクタとは何ですか、またどのような場合に支払コネクタの配置と実装が必要ですか ?</span><span class="sxs-lookup"><span data-stu-id="36e6e-118">What is a payment connector and in what cases do I need to deploy and implement a payment connector?</span></span>
<span data-ttu-id="36e6e-119">支払コネクタは、カードが存在しないトランザクションとカードが存在するトランザクションの支払いをアプリケーションが処理できるようにする、設定可能なソフトウェア コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="36e6e-119">Payment connectors are software components that can be set up which enable an application to process payments for transactions where the card is not present and transactions where the card is present.</span></span>

<span data-ttu-id="36e6e-120">Verifone および MasterCard などの Microsoft によって指定されたコネクタを使用するか、ISV パートナーがカスタム コネクタを構築することができます。</span><span class="sxs-lookup"><span data-stu-id="36e6e-120">Microsoft-provided connectors such as Verifone and MasterCard can be used, or custom connectors can be built by ISV partners.</span></span> <span data-ttu-id="36e6e-121">コネクタは通常、顧客の業務でのニーズを満たすために構築されます。</span><span class="sxs-lookup"><span data-stu-id="36e6e-121">A connector is typically built to meet the business needs of a customer.</span></span> <span data-ttu-id="36e6e-122">新しいタイプの支払いタイプ (リンク払い戻しなど) が必要なシナリオがある場合、カスタム コネクタが作成されることがあります。</span><span class="sxs-lookup"><span data-stu-id="36e6e-122">Custom connectors are often created when there is a scenario that requires a new type of payment type (for example, linked refunds).</span></span> <span data-ttu-id="36e6e-123">特定の地域でビジネスを行っている顧客は、最初から用意されているコネクタがこれらの地域をサポートしていない場合、新しいコネクタが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="36e6e-123">Customers doing business in certain geographies may need new connectors if the out-of-box connectors do not support those regions.</span></span>
          
## <a name="are-other-payment-connector-providers-supported"></a><span data-ttu-id="36e6e-124">その他の支払コネクタ プロバイダーはサポートされていますか。</span><span class="sxs-lookup"><span data-stu-id="36e6e-124">Are other payment connector providers supported?</span></span>
<span data-ttu-id="36e6e-125">はい、ただしカスタマイズを使用してそれらを接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36e6e-125">Yes, but you must connect them using customization.</span></span>

## <a name="what-is-the-service-level-agreement-sla-for-out-of-box-payment-connectors-like-verifone-and-mastercard"></a><span data-ttu-id="36e6e-126">Verifone および Mastercard などの標準の支払いコネクタのサービス レベル アグリーメント (SLA) とは何ですか ?</span><span class="sxs-lookup"><span data-stu-id="36e6e-126">What is the Service level agreement (SLA) for out-of-box payment connectors like Verifone and Mastercard?</span></span>
<span data-ttu-id="36e6e-127">Verifone や Mastercard などの標準コネクタの SLA は、支払コネクタ プロバイダー自体によって所有されます。</span><span class="sxs-lookup"><span data-stu-id="36e6e-127">The SLA for the out-of-box connectors like Verifone and Mastercard is owned by the payment connector providers themselves.</span></span> <span data-ttu-id="36e6e-128">その SLA については、Verifone または Mastercard サポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="36e6e-128">Please contact Verifone or Mastercard support for information about their SLAs.</span></span>
        
## <a name="if-a-supported-payment-provider-issues-an-update-will-microsoft-automatically-update-the-payment-connector-or-do-i-need-to-work-with-the-payment-provider-to-get-the-updated-payment-connector"></a><span data-ttu-id="36e6e-129">サポートされている支払プロバイダーが更新プログラムを発行した場合は、Microsoft は自動的に支払コネクタを更新してくれますか? または更新された支払コネクタを取得するために支払プロバイダーと連携する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="36e6e-129">If a supported payment provider issues an update, will Microsoft automatically update the payment connector or do I need to work with the payment provider to get the updated payment connector?</span></span>
<span data-ttu-id="36e6e-130">支払いコネクターの更新プログラムが支払コネクター プロバイダーによって発行された場合、支払いコネクターの更新バージョンは Dynamics 365 for Retail の次の予定リリースに含まれます。</span><span class="sxs-lookup"><span data-stu-id="36e6e-130">If a payment connector update is issued by the payment connector provider, the updated version of the payment connector will be included in the next planned release of Dynamics 365 for Retail.</span></span> <span data-ttu-id="36e6e-131">ただし、顧客は早期に取得するため、支払コネクタ プロバイダと直接作業することもできます。</span><span class="sxs-lookup"><span data-stu-id="36e6e-131">However, the customer can also work directly with the payment connector provider to uptake it earlier.</span></span>

        
<span data-ttu-id="36e6e-132">関連トピック:</span><span class="sxs-lookup"><span data-stu-id="36e6e-132">Related topics:</span></span> 
- [<span data-ttu-id="36e6e-133">支払ターミナルとの支払の統合</span><span class="sxs-lookup"><span data-stu-id="36e6e-133">Payment integration with a payment terminal</span></span>](end-to-end-payment-extension.md)
- [<span data-ttu-id="36e6e-134">支払コネクタの配置</span><span class="sxs-lookup"><span data-stu-id="36e6e-134">Deploying a Payment Connector</span></span>](deploy-payment-connector.md)
- [<span data-ttu-id="36e6e-135">支払コネクタ用の Windows インストーラーの作成</span><span class="sxs-lookup"><span data-stu-id="36e6e-135">Create a Windows Installer for Payment Connector</span></span>](create-windows-installer-payment-connector.md)
- [<span data-ttu-id="36e6e-136">Verifone 支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="36e6e-136">Verifone Payment Connector</span></span>](https://dynamics.verifone.com/repo/)
- [<span data-ttu-id="36e6e-137">MasterCard 支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="36e6e-137">MasterCard Payment Connector</span></span>](https://www.simplify.com/microsoft/) 

