---
title: 支払 SDK でのチップのサポート
description: このトピックでは、支払ソフトウェア開発キット (SDK) での支払ターミナルのチップのサポートについて説明します。
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
ms.openlocfilehash: e9ccdb68005e8076d08359ea3e0d1b7fb4739eac
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993387"
---
# <a name="support-for-tipping-in-the-payments-sdk"></a><span data-ttu-id="a2334-103">支払 SDK でのチップのサポート</span><span class="sxs-lookup"><span data-stu-id="a2334-103">Support for tipping in the payments SDK</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2334-104">このトピックでは、Microsoft Dynamics 365 Commerce の支払ソフトウェア開発キット (SDK) が、支払ターミナルを介して入力されるチップ金額をサポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a2334-104">This topic describes how the payments software development kit (SDK) for Microsoft Dynamics 365 Commerce supports tip amounts that are entered through a payment terminal.</span></span> <span data-ttu-id="a2334-105">この機能の目的は、承認の応答にチップ金額のフィールドを個別に含めることによって、支払 SDK にファーストクラスのサポートを追加することです。</span><span class="sxs-lookup"><span data-stu-id="a2334-105">The purpose of this feature is to add first-class support to the payments SDK by including a separate field for the tip amount in authorization responses.</span></span>

<span data-ttu-id="a2334-106">この機能は、販売時点管理 (POS) でのチップまたはチップ レポートのサポートは追加されません。</span><span class="sxs-lookup"><span data-stu-id="a2334-106">This feature doesn't add support for tipping or tip reporting at the point of sale (POS).</span></span> <span data-ttu-id="a2334-107">完全なチップ機能を実装するには、POS 拡張機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="a2334-107">Implementation of full tipping capabilities requires POS extensions.</span></span>

## <a name="key-terms"></a><span data-ttu-id="a2334-108">重要な用語</span><span class="sxs-lookup"><span data-stu-id="a2334-108">Key terms</span></span>

| <span data-ttu-id="a2334-109">相談</span><span class="sxs-lookup"><span data-stu-id="a2334-109">Term</span></span> | <span data-ttu-id="a2334-110">説明</span><span class="sxs-lookup"><span data-stu-id="a2334-110">Description</span></span> |
|---|---|
| <span data-ttu-id="a2334-111">ヒント</span><span class="sxs-lookup"><span data-stu-id="a2334-111">Tips</span></span> | <span data-ttu-id="a2334-112">チップは、チップとも呼ばれ、簡易サービス業界やホスピタリティ業界では一般的です。</span><span class="sxs-lookup"><span data-stu-id="a2334-112">Tips, which are also known as gratuities, are common in the quick service and hospitality industries.</span></span> <span data-ttu-id="a2334-113">これにより、サービスを提供する店舗またはレストランの従業員に対して直接支払を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a2334-113">They enable a payment to be given directly to the store or restaurant employee who provides services.</span></span> |
| <span data-ttu-id="a2334-114">ヘッダーレベルの請求金額</span><span class="sxs-lookup"><span data-stu-id="a2334-114">Header-level charge</span></span> | <span data-ttu-id="a2334-115">購入に適用できる料金ですが、特定の品目には適用されません。</span><span class="sxs-lookup"><span data-stu-id="a2334-115">A charge that can be applied to a purchase, but that isn't for a specific line item.</span></span> |

## <a name="overview-of-the-tipping-feature"></a><span data-ttu-id="a2334-116">チップ機能の概要</span><span class="sxs-lookup"><span data-stu-id="a2334-116">Overview of the tipping feature</span></span>

<span data-ttu-id="a2334-117">チップは、一部のロケールおよび業界では一般的です。</span><span class="sxs-lookup"><span data-stu-id="a2334-117">Tipping is common in some locales and industries.</span></span> <span data-ttu-id="a2334-118">たとえば、簡易サービスとホスピタリティ業界では、チップは現在、米国のほぼすべての場所で行われています。</span><span class="sxs-lookup"><span data-stu-id="a2334-118">For example, in the quick service and hospitality industries, tipping is now done almost everywhere in the United States.</span></span> <span data-ttu-id="a2334-119">多くの企業にとって、支払ターミナルを介したチップをサポートする機能は、従業員を引き付けるのに役立つ重要な要素になりつつあります。</span><span class="sxs-lookup"><span data-stu-id="a2334-119">For many businesses, the ability to support tipping through payment terminals is becoming an important factor that helps attract employees.</span></span> <span data-ttu-id="a2334-120">この機能は、支払 SDK に個別の **TipAmount** フィールドが追加され、支払ターミナルで選択されたチップ金額を承認の応答の一部として POS に送り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="a2334-120">This feature adds a separate **TipAmount** field to the payments SDK, so that tip amounts that are selected on the payment terminal can be sent back to the POS as part of the authorization response.</span></span>

<span data-ttu-id="a2334-121">この機能は、支払 SDK のレベルでのチップのサポートを追加しますが、チップ機能の他の重要な側面のサポートは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="a2334-121">Although this feature adds support for tipping at the level of the payments SDK, it doesn't include support for other important aspects of tipping functionality.</span></span> <span data-ttu-id="a2334-122">たとえば、この機能は、シフト終了時のチップ支払いのレポート、チップをプールする機能、または給与のチップをレポートする機能をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="a2334-122">For example, the feature doesn't support reporting of tip payouts at the end of shifts, the ability to pool tips, or the ability to report tips for payroll.</span></span> <span data-ttu-id="a2334-123">完全なチップ サポートを有効にするには、拡張機能を介してこれらの機能を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2334-123">To enable full tipping support, you must implement those capabilities through extensions.</span></span>

<span data-ttu-id="a2334-124">このトピックで説明されている支払ターミナル統合と SDK 参照を作成する方法の詳細については、[支払ターミナルの支払統合全体の作成](end-to-end-payment-extension.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2334-124">For more information about how to create the payment terminal integrations and SDK references that are mentioned in this topic, see [Create an end-to-end payment integration for a payment terminal](end-to-end-payment-extension.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a2334-125">必要条件</span><span class="sxs-lookup"><span data-stu-id="a2334-125">Prerequisites</span></span>

| <span data-ttu-id="a2334-126">前提条件</span><span class="sxs-lookup"><span data-stu-id="a2334-126">Prerequisite</span></span> | <span data-ttu-id="a2334-127">説明</span><span class="sxs-lookup"><span data-stu-id="a2334-127">Description</span></span> |
|---|---|
| <span data-ttu-id="a2334-128">デバイスのチップ サポート</span><span class="sxs-lookup"><span data-stu-id="a2334-128">Tip support on devices</span></span> | <span data-ttu-id="a2334-129">顧客は、支払ターミナルでチップ金額を選択できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2334-129">Customers must be able to select a tip amount on the payment terminal.</span></span> |
| <span data-ttu-id="a2334-130">**isTippingEnabled** サポート</span><span class="sxs-lookup"><span data-stu-id="a2334-130">**isTippingEnabled** support</span></span> | <span data-ttu-id="a2334-131">支払いコネクタは、支払いの初期化のために **isTippingEnabled** 変数をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2334-131">Payment connectors must support the **isTippingEnabled** variable for payment initialization.</span></span> |
| <span data-ttu-id="a2334-132">**TipAmount** フィールド</span><span class="sxs-lookup"><span data-stu-id="a2334-132">**TipAmount** field</span></span> | <span data-ttu-id="a2334-133">チップ金額は、承認応答の **TipAmount** フィールドの支払いコネクタから返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2334-133">The tip amount must be returned from the payment connector in the **TipAmount** field of the authorization response.</span></span> |
| <span data-ttu-id="a2334-134">拡張による POS チップのサポート</span><span class="sxs-lookup"><span data-stu-id="a2334-134">POS tip support through extension</span></span> | <span data-ttu-id="a2334-135">支払いコネクタから返されるチップ金額は、ヘッダーレベルの料金として販売に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2334-135">The tip amount that is returned from the payment connector should be added to the sale as a header-level charge.</span></span> <span data-ttu-id="a2334-136">チップのレポートおよび管理は、そのままでは提供されません。</span><span class="sxs-lookup"><span data-stu-id="a2334-136">Tip reporting and management aren't provided out of the box.</span></span> |

### <a name="tipping-support-by-payment-processors"></a><span data-ttu-id="a2334-137">支払プロセッサによるチップのサポート</span><span class="sxs-lookup"><span data-stu-id="a2334-137">Tipping support by payment processors</span></span>

<span data-ttu-id="a2334-138">この機能は、新しい **isTippingEnabled** 変数を **AuthorizePaymentTerminalDeviceRequest** リクエストに追加します。</span><span class="sxs-lookup"><span data-stu-id="a2334-138">This feature adds a new **isTippingEnabled** variable to the **AuthorizePaymentTerminalDeviceRequest** request.</span></span> <span data-ttu-id="a2334-139">POS から支払いが要求されると、この変数は、承認要求がチップを追加する資格があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a2334-139">When a payment is requested from the POS, this variable indicates whether the authorization request is eligible to have a tip added.</span></span> <span data-ttu-id="a2334-140">このリクエストを受信した支払コネクタは、接続された支払サービスまたはターミナルからチップ適格承認をリクエストできます。</span><span class="sxs-lookup"><span data-stu-id="a2334-140">Payment connectors that receive this request can then request a tip-eligible authorization from the connected payment service or terminal.</span></span>

<span data-ttu-id="a2334-141">**isTippingEnabled** 変数が **True** に設定されている場合、顧客が支払ターミナルでチップ金額を選択すると、その金額は支払コネクタから返される **AuthorizePaymentCardPaymentResponse** 応答の **TipAmount** フィールドに返されます。</span><span class="sxs-lookup"><span data-stu-id="a2334-141">When the **isTippingEnabled** variable is set to **True**, if a customer selects a tip amount on the payment terminal, that amount should be returned in the **TipAmount** field of the **AuthorizePaymentCardPaymentResponse** response that is returned from the payment connector.</span></span> <span data-ttu-id="a2334-142">チップ金額は、承認応答の **ApprovedAmount** フィールドにも含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2334-142">The tip amount is also included in the **ApprovedAmount** field of the authorization response.</span></span>

### <a name="tipping-support-for-the-adyen-connector"></a><span data-ttu-id="a2334-143">Adyen コネクタのチップ サポート</span><span class="sxs-lookup"><span data-stu-id="a2334-143">Tipping support for the Adyen connector</span></span>

<span data-ttu-id="a2334-144">Adyen コネクタにはチップ サポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2334-144">The Adyen connector includes tip support.</span></span> <span data-ttu-id="a2334-145">承認応答がコネクターに渡されるときに **isTippingEnabled** 変数を **True** に設定するには、カスタマイズが必要です。</span><span class="sxs-lookup"><span data-stu-id="a2334-145">Customization is required to set the **isTippingEnabled** variable to **True** when the authorization response is passed to the connector.</span></span> <span data-ttu-id="a2334-146">**isTippingEnabled** 変数が **True** に設定されている場合、顧客がデバイスでチップ金額を選択すると、その金額が承認応答の **TipAmount** フィールドに返されます。</span><span class="sxs-lookup"><span data-stu-id="a2334-146">When the **isTippingEnabled** variable is set to **True**, if a customer selects a tip amount on the device, that amount should be returned in the **TipAmount** field of the authorization response.</span></span>

<span data-ttu-id="a2334-147">顧客が Adyen ターミナルでチップの金額を選択するように求められる前に、ターミナルはチップ用に構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2334-147">Before a customer can be prompted to select a tip amount on the Adyen terminal, the terminal must be configured for tipping.</span></span> <span data-ttu-id="a2334-148">この構成は、Adyen 顧客領域を介して行われます。</span><span class="sxs-lookup"><span data-stu-id="a2334-148">This configuration is done through the Adyen customer area.</span></span> <span data-ttu-id="a2334-149">チップを有効にするには、Adyen ポータルの **販売時点管理** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2334-149">To enable tipping, select the **Point of Sale** tab in the Adyen portal.</span></span> <span data-ttu-id="a2334-150">チップは、ターミナルまたはフリート全体の **ターミナル設定** オプションを介して有効にできます。</span><span class="sxs-lookup"><span data-stu-id="a2334-150">Tipping can be enabled by terminal or through the fleet-wide **Terminal settings** option.</span></span> <span data-ttu-id="a2334-151">個々のターミナルの設定とフリート全体のターミナル設定の両方で、**支払機能** タブでチップが有効になっています。Adyen デバイスでチップを有効にした後、デバイスの設定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2334-151">In both the settings for individual terminals and the fleet-wide terminal settings, tipping is enabled on the **Payment features** tab. After tipping is enabled on your Adyen device, settings on the device must be updated.</span></span> <span data-ttu-id="a2334-152">この更新が完了するまで、変更は有効になりません。</span><span class="sxs-lookup"><span data-stu-id="a2334-152">The change won't take effect until this update is done.</span></span>

### <a name="suggested-implementation"></a><span data-ttu-id="a2334-153">推奨される実装</span><span class="sxs-lookup"><span data-stu-id="a2334-153">Suggested implementation</span></span>

<span data-ttu-id="a2334-154">支払いコネクタから承認応答が返された後、ヘッダーレベルの料金を使用してチップ金額をトランザクションに追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a2334-154">We recommend that a header-level charge be used to add the tip amount to the transaction after the authorization response is returned from the payment connector.</span></span> <span data-ttu-id="a2334-155">この機能をサポートするには、**PaymentTerminalAuthorizePaymentRequestHandler** ハンドラーの拡張機能を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2334-155">To support this functionality, an extension should be created for the **PaymentTerminalAuthorizePaymentRequestHandler** handler.</span></span> <span data-ttu-id="a2334-156">その拡張機能には、承認応答で **TipAmount** 値が返された場合に、取引にヘッダーレベルの料金を追加するロジックを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2334-156">That extension should include logic to add a header-level charge to the transaction if a **TipAmount** value is returned in the authorization response.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2334-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a2334-157">Additional resources</span></span>

- [<span data-ttu-id="a2334-158">Adyen コネクタの概要</span><span class="sxs-lookup"><span data-stu-id="a2334-158">Adyen connector overview</span></span>](adyen-connector.md?tabs=10-0-14.md)
- [<span data-ttu-id="a2334-159">支払端末のエンド・ツー・エンド支払統合を作成する</span><span class="sxs-lookup"><span data-stu-id="a2334-159">Create an end-to-end payment integration for a payment terminal</span></span>](end-to-end-payment-extension.md)
