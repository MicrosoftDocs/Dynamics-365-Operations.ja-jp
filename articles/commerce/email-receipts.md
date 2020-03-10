---
title: Modern POS (MPOS) からの電子メール レシートの送信
description: Modern 販売時点管理 (MPOS) では、販売時点管理 (POS) でトランザクションが支払/入金されたときにレシートの電子メールを送信できます。
author: jashanno
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 8be7e17a2e2c65c74a62fd69f6663ffd1a7bb410
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070773"
---
# <a name="send-email-receipts-from-modern-pos-mpos"></a><span data-ttu-id="5fb07-103">Modern POS (MPOS) からの電子メール レシートの送信</span><span class="sxs-lookup"><span data-stu-id="5fb07-103">Send email receipts from Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5fb07-104">Modern 販売時点管理 (MPOS) では、販売時点管理 (POS) でトランザクションが支払/入金されたときにレシートの電子メールを送信できます。</span><span class="sxs-lookup"><span data-stu-id="5fb07-104">In Modern Point of Sale (MPOS), you can send receipt emails when a transaction is tendered at the point of sale (POS).</span></span>

## <a name="prerequisite"></a><span data-ttu-id="5fb07-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="5fb07-105">Prerequisite</span></span>

<span data-ttu-id="5fb07-106">電子メールのレシートを送信するには、Simple Mail Transfer Protocol (SMTP) サーバーをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fb07-106">To send email receipts, you must configure a Simple Mail Transfer Protocol (SMTP) server.</span></span>

## <a name="set-up-email-receipts"></a><span data-ttu-id="5fb07-107">電子メールのレシートを設定</span><span class="sxs-lookup"><span data-stu-id="5fb07-107">Set up email receipts</span></span>

### <a name="set-default-options-for-email-receipts"></a><span data-ttu-id="5fb07-108">電子メールのレシートの既定のオプションの設定</span><span class="sxs-lookup"><span data-stu-id="5fb07-108">Set default options for email receipts</span></span>

1. <span data-ttu-id="5fb07-109">**Retail とコマース &gt; バックオフィスの設定 &gt; パラメーター &gt; コマース パラメーター**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-109">Select **Retail and Commerce &gt; Headquarters setup &gt; Parameters &gt; Commerce parameters**.</span></span>
2. <span data-ttu-id="5fb07-110">**転記**タブで、**電子メールのレシート**クイックタブの、**レシート オプション**フィールドで既定のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-110">On the **Posting** tab, on the **Email receipt** FastTab, in the **Receipt option** field, select a default option:</span></span>

    - <span data-ttu-id="5fb07-111">**標準受領書** – POS レジスターからレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-111">**Standard receipt** – Print receipts from the POS register.</span></span>
    - <span data-ttu-id="5fb07-112">**電子メール** – レシートを電子メール メッセージで顧客に送信します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-112">**Email** – Send receipts to customers in email messages.</span></span>
    - <span data-ttu-id="5fb07-113">**両方** – POS レジスターからレシートを印刷して、レシートを顧客に電子メールで送信します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-113">**Both** – Print receipts from the POS register, and send receipts to customers in email messages.</span></span>

3. <span data-ttu-id="5fb07-114">**件名**フィールドに、電子メールで送信するレシートの件名行に既定で表示する必要があるテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-114">In the **Subject** field, enter the text that should appear by default on the subject line of a receipt that is sent as an email message.</span></span>

### <a name="set-email-receipt-options-for-a-customer"></a><span data-ttu-id="5fb07-115">顧客の電子メールのレシート オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-115">Set email receipt options for a customer</span></span>

1. <span data-ttu-id="5fb07-116">**Retail とコマース &gt; 顧客 &gt; 顧客サービス**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-116">Go to **Retail and Commerce &gt; Customers &gt; All customers**.</span></span>
2. <span data-ttu-id="5fb07-117">**すべての顧客**リストページで、顧客を選択し、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-117">On the **All customers** list page, select a customer, and then select **Edit**.</span></span>
3. <span data-ttu-id="5fb07-118">顧客の詳細ページの、**コマース** クイック タブの、**レシート オプション** フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-118">On the customer details page, on the **Commerce** FastTab, in the **Receipt option** field, select an option:</span></span>

    - <span data-ttu-id="5fb07-119">**標準受領書** – 顧客は印刷されたレシートのみを受信します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-119">**Standard receipt** – The customer will receive only printed receipts.</span></span> <span data-ttu-id="5fb07-120">印刷されたレシートは POS レジスターから生成されます。</span><span class="sxs-lookup"><span data-stu-id="5fb07-120">The printed receipt is generated from the POS register.</span></span>
    - <span data-ttu-id="5fb07-121">**電子メール** – 顧客は電子メールのレシートのみを受信します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-121">**Email** – The customer will receive only email receipts.</span></span>
    - <span data-ttu-id="5fb07-122">**両方** – 顧客は印刷されたレシートと電子メールのレシートの両方を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="5fb07-122">**Both** – The customer will receive both printed receipts and email receipts.</span></span>

4. <span data-ttu-id="5fb07-123">**レシート オプション**フィールドで、**電子メール**または**両方**のいずれかを選択した場合は、**レシート 電子メール**フィールドに顧客の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-123">If you selected either **Email** or **Both** in the **Receipt option** field, enter the customer's email address in the **Receipt email** field.</span></span>

### <a name="set-up-an-email-receipt-profile"></a><span data-ttu-id="5fb07-124">電子メール レシート プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="5fb07-124">Set up an email receipt profile</span></span>

1. <span data-ttu-id="5fb07-125">**Retail とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 視覚プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-125">Go to **Retail and Commerce &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Receipt profiles**.</span></span>
2. <span data-ttu-id="5fb07-126">**Ctrl+N** キーを押してレシート プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-126">Press **Ctrl+N** to create a receipt profile.</span></span>
3. <span data-ttu-id="5fb07-127">**レシート プロファイル ID** および**説明**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-127">Enter values in the **Receipt profile ID** and **Description** fields.</span></span>
4. <span data-ttu-id="5fb07-128">**一般**クイック タブで、**追加**を選択してレシート タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-128">On the **General** FastTab, select **Add** to add a receipt type.</span></span>
5. <span data-ttu-id="5fb07-129">レシート タイプとして**レシート**を選択し、電子メール レシートに使用するレシート形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-129">Select **Receipt** as the receipt type, and select the receipt format to use for email receipts.</span></span>

### <a name="add-an-email-receipt-profile-to-the-functionality-profile"></a><span data-ttu-id="5fb07-130">機能プロファイルに、電子メールのレシート プロファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-130">Add an email receipt profile to the functionality profile</span></span>

1. <span data-ttu-id="5fb07-131">**Retail とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 機能プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-131">Go to **Retail and Commerce &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Functionality profiles**.</span></span>
2. <span data-ttu-id="5fb07-132">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-132">Select **Edit**.</span></span>
3. <span data-ttu-id="5fb07-133">**一般**クイックタブの**レシート プロファイル ID** フィールドで、電子メールのレシート プロファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-133">On the **General** FastTab, in the **Receipt profile ID** field, specify an email receipt profile.</span></span>

### <a name="set-up-an-email-template-for-receipts"></a><span data-ttu-id="5fb07-134">受信者の電子メール テンプレートを設定</span><span class="sxs-lookup"><span data-stu-id="5fb07-134">Set up an email template for receipts</span></span>

1. <span data-ttu-id="5fb07-135">**組織管理 &gt; 設定 &gt; 組織の電子メール テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-135">Go to **Organization administration &gt; Setup &gt; Organization email templates**.</span></span>
2. <span data-ttu-id="5fb07-136">**Ctrl+N** キーを押して新しいテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-136">Press **Ctrl+N** to create a template.</span></span>
3. <span data-ttu-id="5fb07-137">**概要**タブで、次のフィールドを入力します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-137">On the **Overview** tab, complete the following fields:</span></span>

    - <span data-ttu-id="5fb07-138">**電子メール ID**  フィールドに、**EmailRecpt** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-138">In the **Email ID** field, enter **EmailRecpt**.</span></span>
    - <span data-ttu-id="5fb07-139">**電子メールの説明**フィールドに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-139">In the **Email description** field, enter a description.</span></span>
    - <span data-ttu-id="5fb07-140">**既定の言語コード**フィールドで、言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-140">In the **Default language code** field, select the language.</span></span>
    - <span data-ttu-id="5fb07-141">**送信者名**フィールドに、電子メールの送信者として表示する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-141">In the **Sender name** field, specify the name that should appear as the sender of the email.</span></span> <span data-ttu-id="5fb07-142">この名前は、電子メールの**送信者**の名前として表示されます。</span><span class="sxs-lookup"><span data-stu-id="5fb07-142">Customers will see this name as the **From** name on the email.</span></span>
    - <span data-ttu-id="5fb07-143">**送信者電子メール**フィールドで、有効な電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-143">In the **Sender email** field, specify a valid email address.</span></span> <span data-ttu-id="5fb07-144">このメールアドレスは、電子メールの**送信者**のメール アドレスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="5fb07-144">Customers will see this email address as the **From** email address on the email.</span></span>

4. <span data-ttu-id="5fb07-145">下部グリッドで次のフィールドを構成します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-145">In the lower grid, configure the following fields:</span></span>

    - <span data-ttu-id="5fb07-146">**電子メール ID** フィールドが **EmailRecpt** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5fb07-146">Make sure that the **Email ID** field is set to **EmailRecpt**.</span></span>
    - <span data-ttu-id="5fb07-147">**件名**フィールドに、電子メール レシートのタイトルを入力します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-147">In the **Subject** field, enter a title for the email receipts.</span></span>
    - <span data-ttu-id="5fb07-148">**言語**フィールドで、言語を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-148">In the **Language** field, specify the language.</span></span>
   -   <span data-ttu-id="5fb07-149">**電子メール** - 次の文字列を挿入します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-149">**Email**- Insert the following string:</span></span>


    ``` xml
    <pre>
    %message%
    </pre>
    ```

-   <span data-ttu-id="5fb07-150">メッセージにレシート以上のものを含める場合は、**電子メール メッセージ**を選択し、送信する電子メール メッセージの本文用のテンプレートを記入します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-150">If you want to have more than just the receipt in the message, select **E-mail message** to fill out the template for the body of the email messages to be sent.</span></span> <span data-ttu-id="5fb07-151">プレースホルダー *%message%.*</span><span class="sxs-lookup"><span data-stu-id="5fb07-151">The placeholder *%message%.*</span></span> <span data-ttu-id="5fb07-152">を使用して MPOS からレシートを挿入します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-152">is used to insert the receipt from MPOS.</span></span> 

    <span data-ttu-id="5fb07-153">**%message%** プレースホルダーは、MPOS レシートの送信時に置き換えられる唯一のプレースホルダーです。</span><span class="sxs-lookup"><span data-stu-id="5fb07-153">The **%message%** placeholder is the only placeholder that will be replaced when MPOS receipts are sent.</span></span> <span data-ttu-id="5fb07-154">より多くのプレースホルダー オプションを取得するには、MPOS 側でカスタマイズを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fb07-154">If you want more placeholder options, you must create a customization on the MPOS side.</span></span>

<span data-ttu-id="5fb07-155">メモ帳などのテキスト エディターに HTML コンテンツを配置し、それをアップロードする前に .txt ファイルとして保存するのが最善です。</span><span class="sxs-lookup"><span data-stu-id="5fb07-155">It's a best practice to put the HTML content in a text editor, such as Notepad, and save it as a .txt file before uploading.</span></span> <span data-ttu-id="5fb07-156">これにより、レシート配置を保持し、電子メールで送信したレシートのヘッダーとフッターのスペースを節約できます。</span><span class="sxs-lookup"><span data-stu-id="5fb07-156">This will help to preserve receipt alignment and reduce header and footer space in the emailed receipt.</span></span>

<span data-ttu-id="5fb07-157">印刷されたレシートのロゴとバー コードは、電子メールで送信したレシート バージョンには含まれません。</span><span class="sxs-lookup"><span data-stu-id="5fb07-157">The logo and bar code from the printed receipt will not be included in the emailed receipt version.</span></span> <span data-ttu-id="5fb07-158">ロゴを含めるには、一般的な HTML 電子メール テンプレートを作成し、プレースホルダーを埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="5fb07-158">To include the logo, create a generic HTML email template and embed the placeholder.</span></span> <span data-ttu-id="5fb07-159">電子メールで送信したレシートにバー コードを含めるには、カスタマイズが必要です。</span><span class="sxs-lookup"><span data-stu-id="5fb07-159">Including bar codes in the emailed receipt requires customization.</span></span> 

5. <span data-ttu-id="5fb07-160">設定した設定に応じて、適切な配布スケジュール ジョブを実行し、変更を MPOS に同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fb07-160">Depending on the settings that you configured, you must run the appropriate distribution schedule jobs to synchronize the changes to MPOS.</span></span>

    - <span data-ttu-id="5fb07-161">**1010** - 顧客</span><span class="sxs-lookup"><span data-stu-id="5fb07-161">**1010** – Customer</span></span>
    - <span data-ttu-id="5fb07-162">**1070** - チャンネル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5fb07-162">**1070** – Channel configuration</span></span>
    - <span data-ttu-id="5fb07-163">**1090** - レジスター</span><span class="sxs-lookup"><span data-stu-id="5fb07-163">**1090** – Registers</span></span>
    - <span data-ttu-id="5fb07-164">**1110** - グローバル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5fb07-164">**1110** – Global configuration</span></span>

## <a name="mpos-transactions"></a><span data-ttu-id="5fb07-165">MPOS トランザクション</span><span class="sxs-lookup"><span data-stu-id="5fb07-165">MPOS transactions</span></span>

<span data-ttu-id="5fb07-166">店舗への変更が同期された後、MPOS は、ユーザーに各トランザクションの電子メール アドレスを求めます (フィーチャーが有効な場合)。</span><span class="sxs-lookup"><span data-stu-id="5fb07-166">After the changes are synchronized to the store, MPOS prompts the user for an email address for each transaction (if this feature is enabled).</span></span> <span data-ttu-id="5fb07-167">電子メール アドレスが既に顧客のファイルに割り当てられている場合、そのアドレスは電子メール アドレス プロンプトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5fb07-167">If an email address is already on file for the customer, that address appears in the email address prompt.</span></span> <span data-ttu-id="5fb07-168">顧客の名前がない場合、または名前付き顧客の電子メール アドレスが入力されていない場合は、電子メール アドレスを入力して、**送信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5fb07-168">If a customer hasn't been named, or if an email address hasn't been entered for a named customer, enter an email address, and then select **Send**.</span></span> <span data-ttu-id="5fb07-169">トランザクションが確定すると、リアルタイム サービスによって、前に構成したとおり、メッセージの本文にレシートが含まれる電子メールが顧客に送信されます。</span><span class="sxs-lookup"><span data-stu-id="5fb07-169">When the transaction is finalized, the real-time service will send the customer an email that has the receipt in the body of the message, as you configured earlier.</span></span>
