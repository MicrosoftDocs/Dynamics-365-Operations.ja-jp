---
title: 電子メール通知プロファイルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 17ffdcbf4b1801bd6ee9c9ddc18622d5d04b8a98
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180198"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="bc3a3-103">電子メール通知プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="bc3a3-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bc3a3-104">このトピックでは、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bc3a3-105">概要</span><span class="sxs-lookup"><span data-stu-id="bc3a3-105">Overview</span></span>

<span data-ttu-id="bc3a3-106">チャネルを作成する前に、プロファイルを設定して、発注書の作成、注文出荷の状態、支払不履行など、さまざまなイベントに対して電子メール通知を送信できるようにします。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="bc3a3-107">追加の電子メールのコンフィギュレーションに関する詳細については、[電子メールのコンフィギュレーションおよび送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="bc3a3-108">電子メール通知プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="bc3a3-108">Create an email notification profile</span></span>

<span data-ttu-id="bc3a3-109">電子メール通知プロファイルを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="bc3a3-110">ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="bc3a3-111">アクション ウィンドウで、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="bc3a3-112">**電子メール通知プロファイル** フィールドに、プロファイルを識別する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="bc3a3-113">**説明**フィールドに関連する説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="bc3a3-114">**有効な**スイッチを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="bc3a3-115">電子メール テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="bc3a3-115">Create an email template</span></span>

<span data-ttu-id="bc3a3-116">電子メール通知を作成する前に、送信者の電子メール情報および電子メール テンプレートを含む組織の電子メール テンプレートを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="bc3a3-117">電子メール テンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="bc3a3-118">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 本社の設定 \> パラメーター \> 組織の電子メール テンプレート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="bc3a3-119">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="bc3a3-120">**電子メール ID** フィールドに、このテンプレートを識別するための ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="bc3a3-121">**送信者名**フィールドに、送信者の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="bc3a3-122">**電子メールの説明**フィールドに、意味のある名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="bc3a3-123">**送信電子メール** フィールドに、送信者の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="bc3a3-124">**一般**セクションで、必要なオプション情報すべて (電子メールの優先順位など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="bc3a3-125">電子**メール メッセージのコンテンツ** セクションを**展開**し、新規を選択して、テンプレート コンテンツを作成します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="bc3a3-126">各コンテンツ項目について、言語を選択し、電子メールの件名行を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="bc3a3-127">電子メールに本文が含まれる場合、**本文**ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="bc3a3-128">アクション ウィンドウで、電子メール**本文テンプレート**を提供する電子メール メッセージを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="bc3a3-129">次の画像は、電子メール テンプレートの設定例を示しています。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-129">The following image shows some example email template settings.</span></span>

![電子メール テンプレート設定](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="bc3a3-131">電子メール イベントの作成</span><span class="sxs-lookup"><span data-stu-id="bc3a3-131">Create an email event</span></span>

<span data-ttu-id="bc3a3-132">電子メール イベントを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="bc3a3-133">ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="bc3a3-134">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="bc3a3-135">**電子メール ID** ドロップダウン リストから電子メール テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="bc3a3-136">ドロップダウン リストから適切な**電子メール通知タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="bc3a3-137">**有効**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="bc3a3-138">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="bc3a3-139">次の画像は、イベント通知の設定例を示しています。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-139">The following image shows some example event notification settings.</span></span>

![イベント通知設定](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="bc3a3-141">次のステップ</span><span class="sxs-lookup"><span data-stu-id="bc3a3-141">Next steps</span></span>

<span data-ttu-id="bc3a3-142">メールを送信する前に、送信メール サービスをコンフィギュレーションし、バッチ ジョブを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-142">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="bc3a3-143">詳細については、[電子メールのコンフィギュレーションと送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc3a3-143">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="bc3a3-144">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bc3a3-144">Additional resources</span></span>

[<span data-ttu-id="bc3a3-145">電子メールのコンフィギュレーションと送信</span><span class="sxs-lookup"><span data-stu-id="bc3a3-145">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="bc3a3-146">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="bc3a3-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="bc3a3-147">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="bc3a3-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="bc3a3-148">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="bc3a3-148">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
