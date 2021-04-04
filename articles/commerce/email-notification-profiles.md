---
title: 電子メール通知プロファイルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
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
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555310"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="12847-103">電子メール通知プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="12847-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12847-104">このトピックでは、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="12847-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="12847-105">チャンネルを作成する場合は、電子メール通知プロファイルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="12847-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="12847-106">このようにして、発注書の作成、注文出荷の状態、支払不履行など、さまざまなトランザクション イベントについて顧客に電子メールを送信できます。</span><span class="sxs-lookup"><span data-stu-id="12847-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="12847-107">追加の電子メールのコンフィギュレーションに関する詳細については、[電子メールのコンフィギュレーションおよび送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12847-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="12847-108">電子メール通知プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="12847-108">Create an email notification profile</span></span>

<span data-ttu-id="12847-109">電子メール通知プロファイルを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="12847-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="12847-110">ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="12847-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="12847-111">アクション ウィンドウで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12847-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="12847-112">**電子メール通知プロファイル** フィールドに、プロファイルを識別する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="12847-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="12847-113">**説明** フィールドに関連する説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="12847-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="12847-114">**有効な** スイッチを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="12847-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="12847-115">電子メール テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="12847-115">Create an email template</span></span>

<span data-ttu-id="12847-116">電子メール通知タイプを有効にする前に、Commerce 本社で組織の電子メール テンプレートを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12847-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="12847-117">このテンプレートでは、サポートする各言語の電子メールの件名、送信者、既定の言語、および電子メールの本文を定義します。</span><span class="sxs-lookup"><span data-stu-id="12847-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="12847-118">電子メール テンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="12847-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="12847-119">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 本社の設定 \> パラメーター \> 組織の電子メール テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="12847-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="12847-120">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12847-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="12847-121">**電子メール ID** フィールドに、このテンプレートを識別するための ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="12847-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="12847-122">**送信者名** フィールドに、送信者の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="12847-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="12847-123">**電子メールの説明** フィールドに、意味のある名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="12847-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="12847-124">**送信電子メール** フィールドに、送信者の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="12847-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="12847-125">**一般** セクションで、電子メール テンプレートの既定の言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="12847-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="12847-126">既定の言語は、指定された言語にローカライズされたテンプレートが存在しない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="12847-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="12847-127">電子 **メール メッセージのコンテンツ** セクションを **展開** し、新規を選択して、テンプレート コンテンツを作成します。</span><span class="sxs-lookup"><span data-stu-id="12847-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="12847-128">各コンテンツ項目について、言語を選択し、電子メールの件名行を入力します。</span><span class="sxs-lookup"><span data-stu-id="12847-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="12847-129">電子メールに本文が含まれる場合、**本文** ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12847-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="12847-130">アクション ウィンドウで、電子メール **本文テンプレート** を提供する電子メール メッセージを選択します。</span><span class="sxs-lookup"><span data-stu-id="12847-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="12847-131">次の画像は、電子メール テンプレートの設定例を示しています。</span><span class="sxs-lookup"><span data-stu-id="12847-131">The following image shows some example email template settings.</span></span>

![電子メール テンプレート設定](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="12847-133">電子メール イベントの作成</span><span class="sxs-lookup"><span data-stu-id="12847-133">Create an email event</span></span>

<span data-ttu-id="12847-134">電子メール イベントを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="12847-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="12847-135">ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="12847-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="12847-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="12847-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="12847-137">**電子メール ID** ドロップダウン リストから電子メール テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="12847-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="12847-138">ドロップダウン リストから適切な **電子メール通知タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12847-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="12847-139">**有効** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="12847-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="12847-140">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12847-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="12847-141">次の画像は、イベント通知の設定例を示しています。</span><span class="sxs-lookup"><span data-stu-id="12847-141">The following image shows some example event notification settings.</span></span>

![イベント通知設定](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="12847-143">次のステップ</span><span class="sxs-lookup"><span data-stu-id="12847-143">Next steps</span></span>

<span data-ttu-id="12847-144">メールを送信する前に、送信メール サービスをコンフィギュレーションし、バッチ ジョブを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12847-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="12847-145">詳細については、[電子メールのコンフィギュレーションと送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12847-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="12847-146">追加リソース</span><span class="sxs-lookup"><span data-stu-id="12847-146">Additional resources</span></span>

[<span data-ttu-id="12847-147">電子メールのコンフィギュレーションと送信</span><span class="sxs-lookup"><span data-stu-id="12847-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="12847-148">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="12847-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="12847-149">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="12847-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="12847-150">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="12847-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
