---
title: Modern POS (MPOS) からの電子メール レシートの送信
description: Modern 販売時点管理 (MPOS) では、販売時点管理 (POS) でトランザクションが支払/入金されたときにレシートの電子メールを送信できます。
author: jashanno
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, SysEmailTable,
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 252934
ms.assetid: 4b9f733b-bf28-4b85-94de-4f7adf67a62c
ms.search.region: global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e4a268d746730a5422885b1de7b3bfd08f20661c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408671"
---
# <a name="send-email-receipts-from-modern-pos-mpos"></a><span data-ttu-id="9c391-103">Modern POS (MPOS) からの電子メール レシートの送信</span><span class="sxs-lookup"><span data-stu-id="9c391-103">Send email receipts from Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9c391-104">Modern 販売時点管理 (MPOS) では、販売時点管理 (POS) でトランザクションが支払/入金されたときにレシートの電子メールを送信できます。</span><span class="sxs-lookup"><span data-stu-id="9c391-104">In Modern Point of Sale (MPOS), you can send receipt emails when a transaction is tendered at the point of sale (POS).</span></span>

## <a name="prerequisite"></a><span data-ttu-id="9c391-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="9c391-105">Prerequisite</span></span>

<span data-ttu-id="9c391-106">電子メールのレシートを送信するには、Simple Mail Transfer Protocol (SMTP) サーバーをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c391-106">To send email receipts, you must configure a Simple Mail Transfer Protocol (SMTP) server.</span></span>

## <a name="set-up-email-receipts"></a><span data-ttu-id="9c391-107">電子メールのレシートを設定</span><span class="sxs-lookup"><span data-stu-id="9c391-107">Set up email receipts</span></span>

### <a name="set-default-options-for-email-receipts"></a><span data-ttu-id="9c391-108">電子メールのレシートの既定のオプションの設定</span><span class="sxs-lookup"><span data-stu-id="9c391-108">Set default options for email receipts</span></span>

1. <span data-ttu-id="9c391-109">**Retail とコマース &gt; バックオフィスの設定 &gt; パラメーター &gt; コマース パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-109">Select **Retail and Commerce &gt; Headquarters setup &gt; Parameters &gt; Commerce parameters**.</span></span>
2. <span data-ttu-id="9c391-110">**転記** タブで、**電子メールのレシート** クイックタブの、**レシート オプション** フィールドで既定のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-110">On the **Posting** tab, on the **Email receipt** FastTab, in the **Receipt option** field, select a default option:</span></span>

    - <span data-ttu-id="9c391-111">**標準受領書** – POS レジスターからレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="9c391-111">**Standard receipt** – Print receipts from the POS register.</span></span>
    - <span data-ttu-id="9c391-112">**電子メール** – レシートを電子メール メッセージで顧客に送信します。</span><span class="sxs-lookup"><span data-stu-id="9c391-112">**Email** – Send receipts to customers in email messages.</span></span>
    - <span data-ttu-id="9c391-113">**両方** – POS レジスターからレシートを印刷して、レシートを顧客に電子メールで送信します。</span><span class="sxs-lookup"><span data-stu-id="9c391-113">**Both** – Print receipts from the POS register, and send receipts to customers in email messages.</span></span>

3. <span data-ttu-id="9c391-114">**件名** フィールドに、電子メールで送信するレシートの件名行に既定で表示する必要があるテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="9c391-114">In the **Subject** field, enter the text that should appear by default on the subject line of a receipt that is sent as an email message.</span></span>

### <a name="set-email-receipt-options-for-a-customer"></a><span data-ttu-id="9c391-115">顧客の電子メールのレシート オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="9c391-115">Set email receipt options for a customer</span></span>

1. <span data-ttu-id="9c391-116">**Retail とコマース &gt; 顧客 &gt; 顧客サービス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c391-116">Go to **Retail and Commerce &gt; Customers &gt; All customers**.</span></span>
2. <span data-ttu-id="9c391-117">**すべての顧客** リストページで、顧客を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-117">On the **All customers** list page, select a customer, and then select **Edit**.</span></span>
3. <span data-ttu-id="9c391-118">顧客の詳細ページの、**コマース** クイック タブの、**レシート オプション** フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-118">On the customer details page, on the **Commerce** FastTab, in the **Receipt option** field, select an option:</span></span>

    - <span data-ttu-id="9c391-119">**標準受領書** – 顧客は印刷されたレシートのみを受信します。</span><span class="sxs-lookup"><span data-stu-id="9c391-119">**Standard receipt** – The customer will receive only printed receipts.</span></span> <span data-ttu-id="9c391-120">印刷されたレシートは POS レジスターから生成されます。</span><span class="sxs-lookup"><span data-stu-id="9c391-120">The printed receipt is generated from the POS register.</span></span>
    - <span data-ttu-id="9c391-121">**電子メール** – 顧客は電子メールのレシートのみを受信します。</span><span class="sxs-lookup"><span data-stu-id="9c391-121">**Email** – The customer will receive only email receipts.</span></span>
    - <span data-ttu-id="9c391-122">**両方** – 顧客は印刷されたレシートと電子メールのレシートの両方を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="9c391-122">**Both** – The customer will receive both printed receipts and email receipts.</span></span>

4. <span data-ttu-id="9c391-123">**レシート オプション** フィールドで、**電子メール** または **両方** のいずれかを選択した場合は、**レシート 電子メール** フィールドに顧客の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="9c391-123">If you selected either **Email** or **Both** in the **Receipt option** field, enter the customer's email address in the **Receipt email** field.</span></span>

### <a name="set-up-an-email-receipt-profile"></a><span data-ttu-id="9c391-124">電子メール レシート プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="9c391-124">Set up an email receipt profile</span></span>

1. <span data-ttu-id="9c391-125">**Retail とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 視覚プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c391-125">Go to **Retail and Commerce &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Receipt profiles**.</span></span>
2. <span data-ttu-id="9c391-126">**Ctrl+N** キーを押してレシート プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c391-126">Press **Ctrl+N** to create a receipt profile.</span></span>
3. <span data-ttu-id="9c391-127">**レシート プロファイル ID** および **説明** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c391-127">Enter values in the **Receipt profile ID** and **Description** fields.</span></span>
4. <span data-ttu-id="9c391-128">**一般** クイック タブで、**追加** を選択してレシート タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="9c391-128">On the **General** FastTab, select **Add** to add a receipt type.</span></span>
5. <span data-ttu-id="9c391-129">レシート タイプとして **レシート** を選択し、電子メール レシートに使用するレシート形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-129">Select **Receipt** as the receipt type, and select the receipt format to use for email receipts.</span></span>

### <a name="add-an-email-receipt-profile-to-the-functionality-profile"></a><span data-ttu-id="9c391-130">機能プロファイルに、電子メールのレシート プロファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="9c391-130">Add an email receipt profile to the functionality profile</span></span>

1. <span data-ttu-id="9c391-131">**Retail とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 機能プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c391-131">Go to **Retail and Commerce &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Functionality profiles**.</span></span>
2. <span data-ttu-id="9c391-132">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-132">Select **Edit**.</span></span>
3. <span data-ttu-id="9c391-133">**一般** クイックタブの **レシート プロファイル ID** フィールドで、電子メールのレシート プロファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="9c391-133">On the **General** FastTab, in the **Receipt profile ID** field, specify an email receipt profile.</span></span>

### <a name="set-up-an-email-template-for-receipts"></a><span data-ttu-id="9c391-134">受信者の電子メール テンプレートを設定</span><span class="sxs-lookup"><span data-stu-id="9c391-134">Set up an email template for receipts</span></span>

1. <span data-ttu-id="9c391-135">**Retail と Commerce &gt; 本社の設定 &gt; 設定 &gt; 組織の電子メール テンプレート** または、**組織管理 &gt; 設定 &gt; 組織の電子メール テンプレート** にある **組織の電子メール テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c391-135">Go to **Organization email templates** under either **Retail and Commerce &gt; Headquarters setup &gt; Setup &gt; Organization email templates** or **Organization administration &gt; Setup &gt; Organization email templates**.</span></span>
2. <span data-ttu-id="9c391-136">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-136">Select **New**.</span></span>
3. <span data-ttu-id="9c391-137">以下のフィールドに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c391-137">Enter information in the following fields:</span></span>

    - <span data-ttu-id="9c391-138">**電子メール ID**  フィールドに、**EmailRecpt** を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c391-138">In the **Email ID** field, enter **EmailRecpt**.</span></span>
    - <span data-ttu-id="9c391-139">**電子メールの説明** フィールドに、オプションの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c391-139">In the **Email description** field, enter an optional description.</span></span>
    - <span data-ttu-id="9c391-140">**送信者名** フィールドに、電子メールの送信者として表示する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="9c391-140">In the **Sender name** field, specify the name that should appear as the sender of the email.</span></span> <span data-ttu-id="9c391-141">この名前は、電子メールの **送信者** の名前として表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c391-141">Customers will see this name as the **From** name on the email.</span></span>
    - <span data-ttu-id="9c391-142">**送信者電子メール** フィールドで、有効な電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="9c391-142">In the **Sender email** field, specify a valid email address.</span></span> <span data-ttu-id="9c391-143">このメールアドレスは、電子メールの **送信者** のメール アドレスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c391-143">Customers will see this email address as the **From** email address on the email.</span></span>

4. <span data-ttu-id="9c391-144">**全般** で、次のフィールドに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c391-144">Under **General**, enter information in the following fields:</span></span>
  - <span data-ttu-id="9c391-145">**既定の言語コード** フィールドで、言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-145">In the **Default language code** field, select a language.</span></span> <span data-ttu-id="9c391-146">これは、複数の言語のテンプレートがコンフィギュレーションされていて、店舗または顧客の優先言語がその他の言語と一致しない場合に、レシートの送信に使用される言語になります。</span><span class="sxs-lookup"><span data-stu-id="9c391-146">This is the language that the receipt will be sent in when templates for multiple languages are configured and the store or customer's preferred language doesn't match any of those additional languages.</span></span> 

5. <span data-ttu-id="9c391-147">**電子メールのコンテンツ** ウィンドウで、**新規** を選択して新しいテンプレート インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c391-147">In the **Email message content** pane, select **New** to create a new template instance.</span></span> <span data-ttu-id="9c391-148">以下のフィールドに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c391-148">Enter information in the following fields:</span></span>
    - <span data-ttu-id="9c391-149">**言語** フィールドで、このテンプレートをローカライズする言語を指定します。</span><span class="sxs-lookup"><span data-stu-id="9c391-149">In the **Language** field, specify the language this template will be localized in.</span></span> <span data-ttu-id="9c391-150">これは、%message% プレースホルダーの上下に静的なコンテンツを含む HTML を含む、電子メールで送信されるレシートにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9c391-150">Note that this only applies to emailed receipts that contain HTML with static content above and/or below the %message% placeholder.</span></span>
    - <span data-ttu-id="9c391-151">**件名** フィールドに、電子メール レシートのタイトルを入力します。</span><span class="sxs-lookup"><span data-stu-id="9c391-151">In the **Subject** field, enter a title for the email receipts.</span></span>
    - <span data-ttu-id="9c391-152">**本文** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9c391-152">Select the **Has body** check box.</span></span>
    - <span data-ttu-id="9c391-153">テンプレート HTML をアップロードするには、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-153">Select **Edit** to upload your template HTML.</span></span> <span data-ttu-id="9c391-154">テンプレート インスタンスには、少なくとも次のコードが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c391-154">At a minimum, your template instance must contain the following code:</span></span> 
 
    ``` xml
    <pre>
    %message%
    </pre>
    ```
<span data-ttu-id="9c391-155">また、HTML を追加して、レシートの電子メールに含めるヘッダー、フッター、ロゴ、またはその他の静的コンテンツを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="9c391-155">You can also add HTML to display a header, footer, logo or any other static content that you want included in the receipt email.</span></span> <span data-ttu-id="9c391-156">HTML レシート テンプレートの作成の詳細については、[メールで送信される領収書のテンプレートを作成する](email-templates-transactions.md#create-a-template-for-emailed-receipts)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c391-156">For more information about creating HTML receipt templates, see [Create a template for emailed receipts](email-templates-transactions.md#create-a-template-for-emailed-receipts).</span></span> 

5. <span data-ttu-id="9c391-157">設定した設定に応じて、適切な配布スケジュール ジョブを実行し、変更を MPOS に同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c391-157">Depending on the settings that you configured, you must run the appropriate distribution schedule jobs to synchronize the changes to MPOS.</span></span>

    - <span data-ttu-id="9c391-158">**1010** - 顧客</span><span class="sxs-lookup"><span data-stu-id="9c391-158">**1010** – Customer</span></span>
    - <span data-ttu-id="9c391-159">**1070** - チャンネル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9c391-159">**1070** – Channel configuration</span></span>
    - <span data-ttu-id="9c391-160">**1090** - レジスター</span><span class="sxs-lookup"><span data-stu-id="9c391-160">**1090** – Registers</span></span>
    - <span data-ttu-id="9c391-161">**1110** - グローバル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9c391-161">**1110** – Global configuration</span></span>

## <a name="mpos-transactions"></a><span data-ttu-id="9c391-162">MPOS トランザクション</span><span class="sxs-lookup"><span data-stu-id="9c391-162">MPOS transactions</span></span>

<span data-ttu-id="9c391-163">店舗への変更が同期された後、MPOS は、ユーザーに各トランザクションの電子メール アドレスを求めます (フィーチャーが有効な場合)。</span><span class="sxs-lookup"><span data-stu-id="9c391-163">After the changes are synchronized to the store, MPOS prompts the user for an email address for each transaction (if this feature is enabled).</span></span> <span data-ttu-id="9c391-164">電子メール アドレスが既に顧客のファイルに割り当てられている場合、そのアドレスは電子メール アドレス プロンプトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c391-164">If an email address is already on file for the customer, that address appears in the email address prompt.</span></span> <span data-ttu-id="9c391-165">顧客の名前がない場合、または名前付き顧客の電子メール アドレスが入力されていない場合は、電子メール アドレスを入力して、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c391-165">If a customer hasn't been named, or if an email address hasn't been entered for a named customer, enter an email address, and then select **Send**.</span></span> <span data-ttu-id="9c391-166">トランザクションが確定すると、リアルタイム サービスによって、前に構成したとおり、メッセージの本文にレシートが含まれる電子メールが顧客に送信されます。</span><span class="sxs-lookup"><span data-stu-id="9c391-166">When the transaction is finalized, the real-time service will send the customer an email that has the receipt in the body of the message, as you configured earlier.</span></span>
