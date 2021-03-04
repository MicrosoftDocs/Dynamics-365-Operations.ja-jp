---
title: ウォレット支払のサポート
description: このトピックでは、Microsoft Dynamics 365 Commerce のウォレット支払のサポートの概要を説明します。
author: rubendel
manager: annbe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 57b6b8c524cf6573a691d5aabee106ef62d25166
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012328"
---
# <a name="wallet-payment-support"></a><span data-ttu-id="aadcc-103">ウォレット支払サポート</span><span class="sxs-lookup"><span data-stu-id="aadcc-103">Wallet payment support</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aadcc-104">このトピックでは、Microsoft Dynamics 365 Commerce のウォレット支払のサポートの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="aadcc-104">This topic provides an overview of wallet payment support for Microsoft Dynamics 365 Commerce.</span></span>  

## <a name="key-terms"></a><span data-ttu-id="aadcc-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="aadcc-105">Key terms</span></span>

| <span data-ttu-id="aadcc-106">相談</span><span class="sxs-lookup"><span data-stu-id="aadcc-106">Term</span></span> | <span data-ttu-id="aadcc-107">説明</span><span class="sxs-lookup"><span data-stu-id="aadcc-107">Description</span></span> |
|---|---|
| <span data-ttu-id="aadcc-108">ウォレット</span><span class="sxs-lookup"><span data-stu-id="aadcc-108">Wallet</span></span> | <span data-ttu-id="aadcc-109">BIN 範囲や有効期限など、クレジット カード タイプとデビット カード タイプを区別するために使用される従来の支払特性を含まない支払タイプ。</span><span class="sxs-lookup"><span data-stu-id="aadcc-109">A payment type that does not include traditional payment characteristics, such as the BIN range and expiration date, which are used to differentiate among credit and debit card types.</span></span> |
| <span data-ttu-id="aadcc-110">プロセッサ支払方法</span><span class="sxs-lookup"><span data-stu-id="aadcc-110">Processor payment method</span></span> | <span data-ttu-id="aadcc-111">支払 SDK のプロパティ支払カード プロパティ。</span><span class="sxs-lookup"><span data-stu-id="aadcc-111">A property payment card property in the payments SDK.</span></span> <span data-ttu-id="aadcc-112">このプロパティをコネクタ内のサポートされている支払方法に追加すると、従来の BIN 範囲マッピングを回避するために、Commerce 本社で設定されているカードまたはウォレットにこれらの支払方法をマップできます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-112">When this property is added to supported payment methods within a connector, those payment methods can be mapped to cards or wallets configured in Commerce headquarters to avoid the traditional BIN range mapping.</span></span> 

## <a name="overview"></a><span data-ttu-id="aadcc-113">概要</span><span class="sxs-lookup"><span data-stu-id="aadcc-113">Overview</span></span>

<span data-ttu-id="aadcc-114">従来のクレジット カードやデビット カードとは異なり、ウォレット支払承認応答には BIN 範囲は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="aadcc-114">Unlike traditional credit and debit cards, wallet payment authorization responses do not include BIN ranges.</span></span> <span data-ttu-id="aadcc-115">従来、BIN 範囲は、支払承認応答を BIN 範囲を持つ事前定義カード タイプに一致させるために使用されてきました。</span><span class="sxs-lookup"><span data-stu-id="aadcc-115">Traditionally, BIN ranges have been used to match payment authorization responses to predefined card types with BIN ranges.</span></span> <span data-ttu-id="aadcc-116">この機能は、**プロセッサ支払方法** のサポートを追加し、これらのバリアントを Commerce 本社で設定されたカード タイプにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="aadcc-116">This feature adds support for **Processor payment methods** and mapping of those variants to card types set up in Commerce headquarters.</span></span>

<span data-ttu-id="aadcc-117">**プロセッサ支払方法** は、特定の支払コネクタでサポートされている支払方法に適用できる支払 SDK のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="aadcc-117">**Processor payment method** is a property for the payments SDK that can be applied to payment methods supported for a particular payment connector.</span></span> <span data-ttu-id="aadcc-118">プロセッサの支払方法を含む承認応答を受信すると、そのプロセッサ支払方法がカードまたはウォレットのタイプにマップされているかどうかを確認するルックアップが実行されます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-118">When an authorization response is received that includes the processor payment method, a lookup is performed to determine if that processor payment method has been mapped to a card or wallet type.</span></span> <span data-ttu-id="aadcc-119">マッピングが見つかった場合、その支払は一致するカードまたはウォレットタイプにマップされます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-119">If a mapping is found, that payment is mapped to the matching card or wallet type.</span></span> <span data-ttu-id="aadcc-120">一致するものが見つからない場合は、Commerce の従来の BIN 範囲設定に従って BIN ルックアップが実行されます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-120">If a match can't be found, a BIN lookup is performed following the traditional BIN range settings for Commerce.</span></span> 

<span data-ttu-id="aadcc-121">ウォレット支払には BIN 範囲が含まれていないので、PayPal などの支払コネクタがウォレット支払をサポートしている場合は、支払コネクタを最新の支払 SDK に更新し、少なくともサポートされているすべてのウォレット支払いについて、プロセッサ支払方法のプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-121">Because wallet payments don't include BIN range, if a payment connector such as PayPal supports wallet payments, the payment connector should be updated to the latest payments SDK and the processor payment method property should be populated at least for all supported wallet payments.</span></span> 

<span data-ttu-id="aadcc-122">プロセッサ支払方法のマッピングは、従来のデビットおよびクレジット カード支払にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-122">Processor payment method mappings are also useful for traditional debit and credit card payments.</span></span> <span data-ttu-id="aadcc-123">プロセッサの支払方法をカードにマッピングすることは、BIN 範囲マッピングよりも簡単で、コネクタでサポートされているすべての支払方法がカードまたはウォレット タイプにマップされるようにするのが簡単であるため、エラーが発生しにくくなります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-123">Mapping processor payment methods to cards is more straightforward than BIN range mapping and less prone to errors because it is easy to ensure all possible payment methods supported by a connector are mapped to a card or wallet type.</span></span> 

## <a name="wallet-payment-method-support-and-processor-payment-methods"></a><span data-ttu-id="aadcc-124">ウォレット支払方法のサポートとプロセッサ支払方法</span><span class="sxs-lookup"><span data-stu-id="aadcc-124">Wallet payment method support and processor payment methods</span></span>

<span data-ttu-id="aadcc-125">この機能は、**ウォレット** と呼ばれる新しい支払方法とカード タイプをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="aadcc-125">This feature supports a new payment method and card type called **Wallet**.</span></span> <span data-ttu-id="aadcc-126">ウォレット支払の主な特徴は BIN の範囲を持たないということです。</span><span class="sxs-lookup"><span data-stu-id="aadcc-126">The primary characteristic of a wallet payment is that it does not have a BIN range.</span></span> <span data-ttu-id="aadcc-127">ただし、ウォレット支払方法では、有効期限や従来必須と考えられていた一部のプロパティが返されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-127">However, wallet payment methods may not return expiration dates and some properties that have traditionally been considered mandatory.</span></span> <span data-ttu-id="aadcc-128">ウォレット支払方法は、従来の BIN 範囲マッピングの代替として、プロセッサ支払方法にマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-128">Wallet payment methods must be mapped to processor payment methods as an alternative to the traditional BIN range mapping.</span></span> 

### <a name="adding-support-of-processor-payment-methods"></a><span data-ttu-id="aadcc-129">プロセッサ支払方法のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="aadcc-129">Adding support of processor payment methods</span></span>

<span data-ttu-id="aadcc-130">プロセッサ支払方法をサポートするには、支払コネクタは **PaymentCardProperties** で **aymentMethodVariant** プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-130">To support processor payment methods, payment connectors need to populate the **PaymentMethodVariant** property in **PaymentCardProperties**.</span></span> <span data-ttu-id="aadcc-131">使用している支払 SDK にこのプロパティが含まれていない場合は、更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-131">If the payments SDK in use does not include this property, it should be updated.</span></span> 

### <a name="processor-payment-method-mapping"></a><span data-ttu-id="aadcc-132">プロセッサ支払方法のマッピング</span><span class="sxs-lookup"><span data-stu-id="aadcc-132">Processor payment method mapping</span></span>

<span data-ttu-id="aadcc-133">**プロセッサ支払方法のマッピング** ページを使用して、設定済みのカードまたはウォレットのタイプにプロセッサ支払方法をマップできます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-133">The **Processor payment method mapping** page can be used to map processor payment methods to configured card or wallet types.</span></span> <span data-ttu-id="aadcc-134">このページにアクセスするには、**カード タイプ** ページの **プロセッサ マッピング** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="aadcc-134">To access this page, select the **Processor mapping** link on the **Card types** page.</span></span>

![プロセッサ支払のマッピング リンク](media/Payments/ProcPmtMap.png)

<span data-ttu-id="aadcc-136">このページが開くと、使用可能な支払コネクタにクエリを実行して、**PaymentMethodVariant** フィールドに入力された一連の設定済みの支払方法を収集します。</span><span class="sxs-lookup"><span data-stu-id="aadcc-136">When this page opens, it queries available payment connectors to collect a set or payment methods with the **PaymentMethodVariant** field populated.</span></span> <span data-ttu-id="aadcc-137">次に、これらの支払方法にカードまたはウォレットへの既存のマッピングがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="aadcc-137">It then checks to determine if those payment methods have an existing mapping to a card or wallet.</span></span> <span data-ttu-id="aadcc-138">マッピングを持たない支払方法は、ページの中央列に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-138">Payment methods that do not have a mapping are listed in the center column of the page.</span></span> 

![マップされていないプロセッサ支払方法](media/Payments/Unmapped.png)

<span data-ttu-id="aadcc-140">プロセッサの支払方法をカードまたはウォレットにマップするには、カードまたはウォレットを選択し、プロセッサ支払方法を選択して、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aadcc-140">To map a processor payment method to a card or wallet, select the card or wallet, select the processor payment method, and then select **Add**.</span></span> <span data-ttu-id="aadcc-141">プロセッサ支払方法が **マップ済み** 列に移動します。</span><span class="sxs-lookup"><span data-stu-id="aadcc-141">The processor payment method moves to the **Mapped** column.</span></span> <span data-ttu-id="aadcc-142">一致する支払承認を受け取ると、選択したカードまたはウォレットにマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-142">When a matching payment authorization is received, it will be mapped to the chosen card or wallet.</span></span>

![マップ済みのプロセッサ支払方法](media/Payments/Mapped.png)

### <a name="when-not-to-use-processor-payment-method-mapping"></a><span data-ttu-id="aadcc-144">プロセッサ支払方法のマッピングを使用しない場合</span><span class="sxs-lookup"><span data-stu-id="aadcc-144">When not to use processor payment method mapping</span></span>

<span data-ttu-id="aadcc-145">場合によっては、プロセッサ支払方法のマッピングがレポートのニーズに対して十分に細かくならない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-145">In certain cases, processor payment method mapping may not be granular enough for reporting needs.</span></span> <span data-ttu-id="aadcc-146">たとえば、一部の小売業者は、同じプロバイダーからの外部ギフト カードを BIN 範囲で区別します。</span><span class="sxs-lookup"><span data-stu-id="aadcc-146">For example, some retailers differentiate external gift cards from the same provider by their BIN range.</span></span> <span data-ttu-id="aadcc-147">このシナリオでは、ギフト カードは、上記のシナリオを使用してマップされません。</span><span class="sxs-lookup"><span data-stu-id="aadcc-147">In this scenario, the gift cards should not be mapped using the above scenario.</span></span> <span data-ttu-id="aadcc-148">代わりに、従来の BIN 範囲マッピングを引き続き使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-148">Instead, they should continue to use traditional BIN range mapping.</span></span> 

## <a name="support-for-unidentified-card-types"></a><span data-ttu-id="aadcc-149">識別されないカード タイプのサポート</span><span class="sxs-lookup"><span data-stu-id="aadcc-149">Support for unidentified card types</span></span>

<span data-ttu-id="aadcc-150">一部のシナリオでは、支払コネクタは、BIN 範囲またはプロセッサ支払方法のマッピングを持たないカードを返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-150">In some scenarios, a payment connector may return a card that does not have a BIN range or processor payment method mapping.</span></span> <span data-ttu-id="aadcc-151">この場合、支払は支払ターミナルによって承認されますが、販売時点管理 (POS) が承認応答を特定のカード タイプにマップできない場合は、支払が取り消されます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-151">If this occurs, the payment is authorized by the payment terminal, but is then reversed when the point of sale (POS) can't map the authorization response to a specific card type.</span></span> <span data-ttu-id="aadcc-152">これに対処するために、不明の承認応答を既定のカード タイプにマップする機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-152">To address this, a capability is provided to map unknown authorization responses to a default card type.</span></span> 

![マップされていないカードの既定](media/Payments/DefaultUnmapped.png)

<span data-ttu-id="aadcc-154">この機能により、支払がターミナルによって承認されず、POS によって取り消されるようになります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-154">This capability ensures that the payment is never authorized by the terminal and then reversed by the POS.</span></span> <span data-ttu-id="aadcc-155">これにより、顧客や店舗の関係者の混乱を避けることができます。</span><span class="sxs-lookup"><span data-stu-id="aadcc-155">This helps avoid confusion for customers and store associates.</span></span> <span data-ttu-id="aadcc-156">この設定を使用する場合、不明な認証の既定のカードを定期的にチェックして、必要なカード タイプが誤って不明なカード タイプのデフォルトにマップされていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-156">When this setting is used, the default card for unknown authorizations should be checked periodically to ensure that wanted card types are not accidentally being mapped to the default for unknown card types.</span></span> <span data-ttu-id="aadcc-157">カード タイプが処理に本当に不要な場合は、プロセッサ レベルでオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aadcc-157">If a card type is truly unwanted for processing, it should be turned off at the processor level.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aadcc-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="aadcc-158">Additional resources</span></span>

- [<span data-ttu-id="aadcc-159">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="aadcc-159">Payments FAQ</span></span>](dev-itpro/payments-retail.md)
- [<span data-ttu-id="aadcc-160">PayPal 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="aadcc-160">Dynamics 365 Payment Connector for PayPal</span></span>](paypal.md)
