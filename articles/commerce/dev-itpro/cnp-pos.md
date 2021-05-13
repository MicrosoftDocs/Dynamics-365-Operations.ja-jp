---
title: ハードウェア ステーションを使用しないクレジットカードの処理
description: このトピックでは、ハードウェア ステーションを含まない POS クライアントで "カードが存在しない" トランザクションの処理をする販売時点管理 (POS) を設定する方法について説明します。
author: rubendel
ms.date: 09/03/2020
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
ms.search.validFrom: 2020-08-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 59c343b7e23d053d0b0411cd86a78063ced8c8cb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936926"
---
# <a name="process-credit-cards-without-a-hardware-station"></a><span data-ttu-id="34956-103">ハードウェア ステーションを使用しないクレジットカードの処理</span><span class="sxs-lookup"><span data-stu-id="34956-103">Process credit cards without a hardware station</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34956-104">このトピックでは、ハードウェア ステーションを含まない POS クライアントで "カードが存在しない" トランザクションの処理をする販売時点管理 (POS) を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="34956-104">This topic describes how to configure the point of sale (POS) to process "card not present" transactions in POS clients that don't include a hardware station.</span></span> <span data-ttu-id="34956-105">この機能では特に、カーブサイド ピックアップなどの新しいシナリオを対象としています。</span><span class="sxs-lookup"><span data-stu-id="34956-105">This feature specifically targets emerging scenarios such as curbside pickup.</span></span>

<span data-ttu-id="34956-106">この機能が有効になっている場合、クラウド POS や iOS 向けの最新の POS などのクライアントは、Commerce Scale Unit を介してクレジットカード処理の呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="34956-106">When this feature is turned on, clients such as Cloud POS and Modern POS for iOS can make credit card processing calls through Commerce Scale Unit.</span></span> <span data-ttu-id="34956-107">ローカル ネットワークに配置されているスタンドアロンのハードウェア ステーションに依存する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="34956-107">They don't have to depend on a standalone hardware station that is deployed on the local network.</span></span> <span data-ttu-id="34956-108">したがって、すべての POS クライアントでカーブサイド ピックアップに対応することができ、必要とされる設定手順も少なく済ませられます。</span><span class="sxs-lookup"><span data-stu-id="34956-108">Therefore, any POS client can support curbside pickup, and fewer setup steps are required.</span></span>

> [!NOTE]
> <span data-ttu-id="34956-109">オフライン モードに対応しているレジに対しては、この機能をオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="34956-109">This feature should not be turned on for registers that support offline mode.</span></span> <span data-ttu-id="34956-110">この機能を使用すると、すべての「カードが存在しない」支払い要求を Commerce Scale Unit にルーティングしますが、レジがオフラインになると Commerce Scale Unit は利用できません。</span><span class="sxs-lookup"><span data-stu-id="34956-110">The feature routes all "card not present" payment requests through the Commerce Scale Unit, but the Commerce Scale Unit isn't available when the register goes offline.</span></span>

## <a name="key-terms"></a><span data-ttu-id="34956-111">重要な用語</span><span class="sxs-lookup"><span data-stu-id="34956-111">Key terms</span></span>

| <span data-ttu-id="34956-112">相談</span><span class="sxs-lookup"><span data-stu-id="34956-112">Term</span></span> | <span data-ttu-id="34956-113">説明</span><span class="sxs-lookup"><span data-stu-id="34956-113">Description</span></span> |
|---|---|
| <span data-ttu-id="34956-114">BOPIS</span><span class="sxs-lookup"><span data-stu-id="34956-114">BOPIS</span></span> | <span data-ttu-id="34956-115">この略語は、"buy online, pick up in store (オンラインで買って、店舗で受け取る)"を意味します。</span><span class="sxs-lookup"><span data-stu-id="34956-115">This abbreviation is short for "buy online, pick up in store."</span></span> |
| <span data-ttu-id="34956-116">カーブサイド ピックアップ</span><span class="sxs-lookup"><span data-stu-id="34956-116">Curbside pickup</span></span> | <span data-ttu-id="34956-117">このシナリオは BOPIS と似通っています。</span><span class="sxs-lookup"><span data-stu-id="34956-117">This scenario resembles BOPIS.</span></span> <span data-ttu-id="34956-118">しかし、店内で商品を受け取るのではなく、お客さんは店に入ることなく、車に乗ったままで商品を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="34956-118">However, instead of picking up items in the store, customers don't usually enter the store and often don't even leave their vehicle.</span></span> |
| <span data-ttu-id="34956-119">カードなし</span><span class="sxs-lookup"><span data-stu-id="34956-119">Card not present</span></span> | <span data-ttu-id="34956-120">この用語は、CNP と略される場合もあります。</span><span class="sxs-lookup"><span data-stu-id="34956-120">This term is sometimes abbreviated CNP.</span></span> <span data-ttu-id="34956-121">クレジットカード、またはその他の形式の電子支払が物理的に存在しない場合のシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="34956-121">It describes scenarios where the credit card or other form of electronic payment isn't physically present.</span></span> <span data-ttu-id="34956-122">BOPIS と カーブサイドのシナリオでは、顧客はオンラインや電話で支払を行うと、ピックアップ時にPOSから支払いが取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="34956-122">In BOPIS and curbside pickup scenarios, customers make a payment online or over the phone, and the payment is then captured from the POS at the time of pickup.</span></span> |
| <span data-ttu-id="34956-123">Hardware station</span><span class="sxs-lookup"><span data-stu-id="34956-123">Hardware station</span></span> | <span data-ttu-id="34956-124">この用語は、POS と決済端末、またはレシート プリンターなどの小売周辺機器との相互作用を促進するビジネス ロジックを表しています。</span><span class="sxs-lookup"><span data-stu-id="34956-124">This term describes the business logic that drives interactions between the POS and payment terminals or retail peripherals such as receipt printers.</span></span> <span data-ttu-id="34956-125">ハードウェア ステーションは、Windows 向け最新 POS と Android クライアント向け最新 POS に組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="34956-125">The hardware station is built into the Modern POS for Windows and Modern POS for Android clients.</span></span> <span data-ttu-id="34956-126">クラウド POS および iOS クライアント向けの最新の POS では、物理デバイスとの相互作用をするために、スタンドアロンで展開されたハードウェア ステーションが必要となります。</span><span class="sxs-lookup"><span data-stu-id="34956-126">The Cloud POS and Modern POS for iOS clients require a standalone deployed hardware station to interact with physical devices.</span></span> |

## <a name="overview"></a><span data-ttu-id="34956-127">概要</span><span class="sxs-lookup"><span data-stu-id="34956-127">Overview</span></span>

<span data-ttu-id="34956-128">この機能をオフにすると、クラウド POS や iOS 向け最新の POS では、ハードウェア ステーションが内蔵されていないため、「カードが存在しない」という要求を自分で処理することはできません。</span><span class="sxs-lookup"><span data-stu-id="34956-128">When this feature is turned off, Cloud POS and Modern POS for iOS can't process "card not present" credit card requests by themselves, because they don't have a built-in hardware station.</span></span> <span data-ttu-id="34956-129">この機能をオンにすると、Commerce Scale Unit を使用して、それらのクライアントに対する要求を容易にすることができます。</span><span class="sxs-lookup"><span data-stu-id="34956-129">When the feature is turned on, the Commerce Scale Unit can be used to facilitate the requests for those clients.</span></span>

<span data-ttu-id="34956-130">この機能は、クラウド POS や iOS 向けの最新 POS に加えて、Windows 向け最新 POS や Android 向け最新 POS でも使用することができますが、オフライン モードには対応していません。</span><span class="sxs-lookup"><span data-stu-id="34956-130">Although this feature can also be used for Modern POS for Windows and Modern POS for Android, in addition to Cloud POS and Modern POS for iOS, it isn't supported for offline mode.</span></span> <span data-ttu-id="34956-131">したがって、Windows クライアントがオフラインモードを使用するシナリオでは、この機能を使用すべきではありません。</span><span class="sxs-lookup"><span data-stu-id="34956-131">Therefore, the feature should not be used in scenarios where a Windows client uses offline mode.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="34956-132">サポートされているシナリオ</span><span class="sxs-lookup"><span data-stu-id="34956-132">Supported scenarios</span></span>

<span data-ttu-id="34956-133">ハードウェア ステーションを内蔵していない POS クライアントでは、次のシナリオに対応しています。</span><span class="sxs-lookup"><span data-stu-id="34956-133">The following scenarios are supported for POS clients that don't have a built-in hardware station.</span></span>

| <span data-ttu-id="34956-134">シナリオ</span><span class="sxs-lookup"><span data-stu-id="34956-134">Scenario</span></span> | <span data-ttu-id="34956-135">説明</span><span class="sxs-lookup"><span data-stu-id="34956-135">Description</span></span> |
|---|---|
| <span data-ttu-id="34956-136">支払の取り込み</span><span class="sxs-lookup"><span data-stu-id="34956-136">Payment capture</span></span> | <span data-ttu-id="34956-137">注文をリコールしてピックアップすることができ、注文に関連したクレジットカード決済を取り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="34956-137">An order can be recalled for pickup, and the credit card payment that is associated with the order can be captured.</span></span> |
| <span data-ttu-id="34956-138">リンクされた払戻</span><span class="sxs-lookup"><span data-stu-id="34956-138">Linked refund</span></span> | <span data-ttu-id="34956-139">返品注文やキャッシュ アンド キャリー取引の場合、払戻を元の支払い方法にリンクさせることができます。</span><span class="sxs-lookup"><span data-stu-id="34956-139">A refund can be linked to the original payment instrument for return orders and cash-and-carry transactions.</span></span> |
| <span data-ttu-id="34956-140">注文の編集</span><span class="sxs-lookup"><span data-stu-id="34956-140">Order editing</span></span> | <span data-ttu-id="34956-141">POS では注文をリコールして編集することができ、支払いに使用したものと同じカードを認証して、新しい注文合計に対応することができます。</span><span class="sxs-lookup"><span data-stu-id="34956-141">Orders can be recalled and edited in the POS, and the same payment card can be authorized to support the new order total.</span></span> |
| <span data-ttu-id="34956-142">注文取消</span><span class="sxs-lookup"><span data-stu-id="34956-142">Order cancellation</span></span> | <span data-ttu-id="34956-143">キャンセルされた注文については、顧客に戻される残高を、支払いに使用したカードに返金できます。</span><span class="sxs-lookup"><span data-stu-id="34956-143">For orders that are canceled, the balance that is due back to the customer can be refunded to the original payment card.</span></span> |

## <a name="unsupported-scenarios"></a><span data-ttu-id="34956-144">サポートされないシナリオ</span><span class="sxs-lookup"><span data-stu-id="34956-144">Unsupported scenarios</span></span>

<span data-ttu-id="34956-145">クレジットカード認証の作成には対応していません。</span><span class="sxs-lookup"><span data-stu-id="34956-145">Creation of credit card authorizations isn't supported.</span></span> <span data-ttu-id="34956-146">既に存在するカード支払のみを、取得、払戻、または編集することができます。</span><span class="sxs-lookup"><span data-stu-id="34956-146">Only existing card payments can be captured, refunded, or edited.</span></span>

| <span data-ttu-id="34956-147">シナリオ</span><span class="sxs-lookup"><span data-stu-id="34956-147">Scenario</span></span> | <span data-ttu-id="34956-148">説明</span><span class="sxs-lookup"><span data-stu-id="34956-148">Description</span></span> |
|---|---|
| <span data-ttu-id="34956-149">支払の作成</span><span class="sxs-lookup"><span data-stu-id="34956-149">Creating a payment</span></span> | <span data-ttu-id="34956-150">この機能では、新規顧客注文の作成とフルフィルメントに対する支払いの承認には対応していません。</span><span class="sxs-lookup"><span data-stu-id="34956-150">This feature doesn't support the creation of new customer orders and authorization of payments for fulfillment.</span></span> <span data-ttu-id="34956-151">新しい支払を作成する場合は、ハードウェア ステーションが必要になります。</span><span class="sxs-lookup"><span data-stu-id="34956-151">Creation of new payments will continue to require a hardware station.</span></span> |
| <span data-ttu-id="34956-152">支払カードの変更</span><span class="sxs-lookup"><span data-stu-id="34956-152">Changing the payment card</span></span> | <span data-ttu-id="34956-153">注文が POS で取り消された場合は、ピッキングに対して同じ支払方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34956-153">If an order is recalled in the POS, the same payment method must be used for pickup.</span></span> <span data-ttu-id="34956-154">店舗関係者は、ハードウェア ステーションが利用可能な場合に限り、注文に関連付けられたカードの代わりに別のカードを代用することができます。</span><span class="sxs-lookup"><span data-stu-id="34956-154">Store associates can substitute a different card for the card that is associated with an order only if a hardware station is available.</span></span> |
| <span data-ttu-id="34956-155">オフライン モード</span><span class="sxs-lookup"><span data-stu-id="34956-155">Offline mode</span></span> | <span data-ttu-id="34956-156">この機能がオンになっている場合、"カードがありません" という要求は常に Commerce Scale Unit に送信されます。</span><span class="sxs-lookup"><span data-stu-id="34956-156">When this feature is turned on, "card not present" requests are always sent to the Commerce Scale Unit.</span></span> <span data-ttu-id="34956-157">レジがオフラインになっている場合は、Commerce Scale Unit が使用できなくなるため、"カードがありません" の要求は失敗します。</span><span class="sxs-lookup"><span data-stu-id="34956-157">If a register goes offline, "card not present" requests will fail, because the Commerce Scale Unit is no longer available.</span></span> <span data-ttu-id="34956-158">オフライン モードに対応するように構成されているレジに対しては、この機能をオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="34956-158">The feature should not be turned on for registers that are configured to support offline mode.</span></span> |

## <a name="set-up-the-pos-to-process-card-not-present-transactions-without-a-hardware-station"></a><span data-ttu-id="34956-159">POS を設定sいてハードウェア ステーションなしで "カードが存在しない" トランザクションを処理する</span><span class="sxs-lookup"><span data-stu-id="34956-159">Set up the POS to process "card not present" transactions without a hardware station</span></span>

<span data-ttu-id="34956-160">この機能を有効にする構成は、レジのみで完了できます。</span><span class="sxs-lookup"><span data-stu-id="34956-160">The configuration to turn on this feature is completed at the register level.</span></span>

1. <span data-ttu-id="34956-161">バック オフィスで、**小売りとコマース\> チャンネル設定 \> POS 設定 \> レジスター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="34956-161">In the back office, go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="34956-162">該当のレジを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34956-162">Select the relevant register, and then select **Edit**.</span></span>
3. <span data-ttu-id="34956-163">**全般** クイックタブの **カードが存在しない処理** フィールドで、**小売サーバーを使用する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34956-163">On the **General** FastTab, in the **Card not present processing** field, select **Use retail server**.</span></span> <span data-ttu-id="34956-164">(既定では、このフィールドは **ハードウェア ステーションを使用する** に設定されています。)</span><span class="sxs-lookup"><span data-stu-id="34956-164">(By default, this field is set to **Use hardware station**.)</span></span>

    ![カードが存在しない処理フィールド](media/PAYMENTS/CNP-POS.png)

4. <span data-ttu-id="34956-166">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34956-166">Select **Save**.</span></span>
5. <span data-ttu-id="34956-167">変更を保存した後で、**1090** の配送スケジュールを実行して変更を POS に同期します。</span><span class="sxs-lookup"><span data-stu-id="34956-167">After the change is saved, run the **1090** distribution schedule to sync the changes to the POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34956-168">追加リソース</span><span class="sxs-lookup"><span data-stu-id="34956-168">Additional resources</span></span>

[<span data-ttu-id="34956-169">オムニチャネル支払の概要</span><span class="sxs-lookup"><span data-stu-id="34956-169">Omni-channel payments overview</span></span>](../omni-channel-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]