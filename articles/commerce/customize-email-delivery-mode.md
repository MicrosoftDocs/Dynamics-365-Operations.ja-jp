---
title: 配信モードによるトランザクション メールのカスタマイズ
description: このトピックでは、Microsoft Dynamics 365 Commerce で特定の通知タイプと配信のモードに対応したカスタム メール テンプレートを設定する方法について説明します。
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: d0d96ddb20b2b09751d8c0c0bf8af713de35279a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222636"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="e4440-103">配送モードによるトランザクション メールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="e4440-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4440-104">このトピックでは、Microsoft Dynamics 365 Commerce で特定の通知タイプと配信のモードに対応したカスタム メール テンプレートを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e4440-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e4440-105">トランザクション メールは、通知タイプ (たとえば、**注文作成済み**、**注文梱包済み**、**注文の請求済み**) と配送モード (夜間、店舗内のピックアップ、カーブサイド ピックアップなど) を組み合わせてカスタマイズできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e4440-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="e4440-106">カスタム トランザクション メールでは、小売業者は注文の配信のモードに応じたフルフィルメントを行って、顧客の注文を提供することができます。</span><span class="sxs-lookup"><span data-stu-id="e4440-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="e4440-107">たとえば、"注文の梱包済み" イベントをカスタマイズして、カーブサイド ピックアップを選択した顧客に対して、そのためのカーブサイド ピックアップに関する指示を提供できます。</span><span class="sxs-lookup"><span data-stu-id="e4440-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="e4440-108">また、出荷の注文を行う顧客の配送業者と出荷情報を提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="e4440-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="e4440-109">カスタマイズされたトランザクション メールの機能を使用するには、最初にCommerce本社の **ワークスペース \> 機能管理** に移動することで、**配信のモードによるトランザクション メール テンプレートのカスタマイズ** を有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4440-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="e4440-110">メールは、次の通知タイプの配送モードでカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="e4440-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="e4440-111">**注文のキャンセル** - このメール通知タイプは新しいです。</span><span class="sxs-lookup"><span data-stu-id="e4440-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="e4440-112">**注文が作成されました**</span><span class="sxs-lookup"><span data-stu-id="e4440-112">**Order created**</span></span>
- <span data-ttu-id="e4440-113">**注文確認済**</span><span class="sxs-lookup"><span data-stu-id="e4440-113">**Order confirmed**</span></span>
- <span data-ttu-id="e4440-114">**注文の請求済み** - このメール通知タイプは新しいです。</span><span class="sxs-lookup"><span data-stu-id="e4440-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="e4440-115">**注文の出荷済み** 通知タイプの代わりに、(集荷、出荷、または電子的な配信方法のいずれでもない) 配送モードで出荷された請求イベントについての通知が送信されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e4440-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="e4440-116">**注文のピッキング済**</span><span class="sxs-lookup"><span data-stu-id="e4440-116">**Order picked**</span></span>
- <span data-ttu-id="e4440-117">**注文の梱包済み**</span><span class="sxs-lookup"><span data-stu-id="e4440-117">**Order packed**</span></span>
- <span data-ttu-id="e4440-118">**注文のピックアップ準備完了** - この通知タイプは、**複数のピックアップ配送モードのサポート** が有効になっている場合にのみ、配送モードによってカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="e4440-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="e4440-119">この場合、この通知タイプの機能は、**注文の梱包済み** の通知タイプと同じです。</span><span class="sxs-lookup"><span data-stu-id="e4440-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="e4440-120">**支払い失敗**</span><span class="sxs-lookup"><span data-stu-id="e4440-120">**Payment failed**</span></span>
- <span data-ttu-id="e4440-121">**交換注文が作成されました**</span><span class="sxs-lookup"><span data-stu-id="e4440-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="e4440-122">特定の配送モードに対してメール テンプレートをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="e4440-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="e4440-123">この手順では、新しいカスタムメールテンプレートを作成し、**組織のメールテンプレート** ページに追加することを前提としています。</span><span class="sxs-lookup"><span data-stu-id="e4440-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="e4440-124">メール テンプレートを作成およびアップロードする方法の詳細については、[トランザクション イベントのメールテンプレートの作成](email-templates-transactions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4440-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="e4440-125">Commerce 本社の特定の荷渡方法にメール テンプレートをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e4440-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e4440-126">**Commerce メール通知プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4440-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="e4440-127">**小売用イベント通知設定** で、既存の通知タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4440-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="e4440-128">通知タイプが選択されている間に、**配送モードのコンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4440-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="e4440-129">**配送モード** ダイアログボックスで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4440-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="e4440-130">新規行で、**配送モード** フィールドで、この配送モードを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4440-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="e4440-131">**メール ID** フィールドで、配送モードにマップするメール テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4440-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="e4440-132">**有効** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e4440-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="e4440-133">その他の配送モードを追加するには、手順 4 ~ 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="e4440-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="e4440-134">完了したら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4440-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="e4440-135">販売注文の明細行に対して複数の配送モードがある場合は、既定のテンプレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4440-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="e4440-136">既定のテンプレートは、**Commerce メール通知プロファイル** ページの通知タイプにマップされているテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="e4440-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="e4440-137">販売注文の配送モードが、カスタム メール テンプレート用にコンフィギュレーションされていない場合は、既定のメール テンプレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4440-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4440-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e4440-138">Additional resources</span></span>

[<span data-ttu-id="e4440-139">コール センター注文の作成</span><span class="sxs-lookup"><span data-stu-id="e4440-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="e4440-140">POS での荷渡方法の変更</span><span class="sxs-lookup"><span data-stu-id="e4440-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]