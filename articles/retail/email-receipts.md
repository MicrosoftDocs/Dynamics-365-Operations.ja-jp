---
title: "電子メール受領を Retail Modern POS から送信"
description: "Retail Modern 販売時点管理 (MPOS) では、販売時点管理 (POS) でトランザクションが支払/入金されたときにレシートの電子メールを送信できます。"
author: jashanno
manager: AnnBe
ms.date: 06/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 728d5ffebe67997c5fd557e5d760d93fa29401c4
ms.openlocfilehash: f833a273558658605b1c80182e0b6eaee112805f
ms.contentlocale: ja-jp
ms.lasthandoff: 06/07/2018

---

# <a name="send-email-receipts-from-retail-modern-pos"></a><span data-ttu-id="b79bf-103">電子メール受領を Retail Modern POS から送信</span><span class="sxs-lookup"><span data-stu-id="b79bf-103">Send email receipts from Retail Modern POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b79bf-104">Retail Modern 販売時点管理 (MPOS) では、販売時点管理 (POS) でトランザクションが支払/入金されたときにレシートの電子メールを送信できます。</span><span class="sxs-lookup"><span data-stu-id="b79bf-104">In Retail Modern Point of Sale (MPOS), you can send receipt emails when a transaction is tendered at the point of sale (POS).</span></span>

## <a name="prerequisite"></a><span data-ttu-id="b79bf-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="b79bf-105">Prerequisite</span></span>

<span data-ttu-id="b79bf-106">電子メールのレシートを送信するには、Simple Mail Transfer Protocol (SMTP) サーバーをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b79bf-106">To send email receipts, you must configure a Simple Mail Transfer Protocol (SMTP) server.</span></span>

## <a name="set-up-email-receipts"></a><span data-ttu-id="b79bf-107">電子メールのレシートを設定</span><span class="sxs-lookup"><span data-stu-id="b79bf-107">Set up email receipts</span></span>

### <a name="set-default-options-for-email-receipts"></a><span data-ttu-id="b79bf-108">電子メールのレシートの既定のオプションの設定</span><span class="sxs-lookup"><span data-stu-id="b79bf-108">Set default options for email receipts</span></span>

1. <span data-ttu-id="b79bf-109">**小売 &gt; 本社の設定 &gt; パラメーター &gt; 小売パラメーター**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-109">Select **Retail &gt; Headquarters setup &gt; Parameters &gt; Retail parameters**.</span></span>
2. <span data-ttu-id="b79bf-110">**転記**タブで、**電子メールのレシート**クイックタブの、**レシート オプション**フィールドで既定のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-110">On the **Posting** tab, on the **Email receipt** FastTab, in the **Receipt option** field, select a default option:</span></span>

    - <span data-ttu-id="b79bf-111">**標準受領書** – POS レジスターからレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-111">**Standard receipt** – Print receipts from the POS register.</span></span>
    - <span data-ttu-id="b79bf-112">**電子メール** – レシートを電子メール メッセージで顧客に送信します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-112">**Email** – Send receipts to customers in email messages.</span></span>
    - <span data-ttu-id="b79bf-113">**両方** – POS レジスターからレシートを印刷して、レシートを顧客に電子メールで送信します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-113">**Both** – Print receipts from the POS register, and send receipts to customers in email messages.</span></span>

3. <span data-ttu-id="b79bf-114">**件名**フィールドに、電子メールで送信するレシートの件名行に既定で表示する必要があるテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-114">In the **Subject** field, enter the text that should appear by default on the subject line of a receipt that is sent as an email message.</span></span>

### <a name="set-email-receipt-options-for-a-customer"></a><span data-ttu-id="b79bf-115">顧客の電子メールのレシート オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-115">Set email receipt options for a customer</span></span>

1. <span data-ttu-id="b79bf-116">**小売 &gt; 顧客 &gt; すべての顧客**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-116">Select **Retail &gt; Customers &gt; All customers**.</span></span>
2. <span data-ttu-id="b79bf-117">**すべての顧客**リストページで、顧客を選択し、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-117">On the **All customers** list page, select a customer, and then select **Edit**.</span></span>
3. <span data-ttu-id="b79bf-118">顧客の詳細ページの、**小売**クイック タブの、**レシート オプション**フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-118">On the customer details page, on the **Retail** FastTab, in the **Receipt option** field, select an option:</span></span>

    - <span data-ttu-id="b79bf-119">**標準受領書** – 顧客は印刷されたレシートのみを受信します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-119">**Standard receipt** – The customer will receive only printed receipts.</span></span> <span data-ttu-id="b79bf-120">印刷されたレシートは POS レジスターから生成されます。</span><span class="sxs-lookup"><span data-stu-id="b79bf-120">The printed receipt is generated from the POS register.</span></span>
    - <span data-ttu-id="b79bf-121">**電子メール** – 顧客は電子メールのレシートのみを受信します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-121">**Email** – The customer will receive only email receipts.</span></span>
    - <span data-ttu-id="b79bf-122">**両方** – 顧客は印刷されたレシートと電子メールのレシートの両方を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="b79bf-122">**Both** – The customer will receive both printed receipts and email receipts.</span></span>

4. <span data-ttu-id="b79bf-123">**レシート オプション**フィールドで、**電子メール**または**両方**のいずれかを選択した場合は、**レシート 電子メール**フィールドに顧客の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-123">If you selected either **Email** or **Both** in the **Receipt option** field, enter the customer's email address in the **Receipt email** field.</span></span>

### <a name="set-up-an-email-receipt-profile"></a><span data-ttu-id="b79bf-124">電子メール レシート プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="b79bf-124">Set up an email receipt profile</span></span>

1. <span data-ttu-id="b79bf-125">**小売 &gt; チャンネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; レシート プロファイル**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-125">Select **Retail &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Receipt profiles**.</span></span>
2. <span data-ttu-id="b79bf-126">Ctrl + N キーを押してレシート プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-126">Press Ctrl+N to create a receipt profile.</span></span>
3. <span data-ttu-id="b79bf-127">**レシート プロファイル ID** および**説明**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-127">Enter values in the **Receipt profile ID** and **Description** fields.</span></span>
4. <span data-ttu-id="b79bf-128">**一般**クイック タブで、**追加**を選択してレシート タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-128">On the **General** FastTab, select **Add** to add a receipt type.</span></span>
5. <span data-ttu-id="b79bf-129">レシート タイプとして**レシート**を選択し、電子メール レシートに使用するレシート形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-129">Select **Receipt** as the receipt type, and select the receipt format to use for email receipts.</span></span>

### <a name="add-an-email-receipt-profile-to-the-functionality-profile"></a><span data-ttu-id="b79bf-130">機能プロファイルに、電子メールのレシート プロファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-130">Add an email receipt profile to the functionality profile</span></span>

1. <span data-ttu-id="b79bf-131">**小売 &gt; チャンネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 機能プロファイル**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-131">Select **Retail &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Functionality profiles**.</span></span>
2. <span data-ttu-id="b79bf-132">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-132">Select **Edit**.</span></span>
3. <span data-ttu-id="b79bf-133">**一般**クイックタブの**レシート プロファイル ID** フィールドで、電子メールのレシート プロファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-133">On the **General** FastTab, in the **Receipt profile ID** field, specify an email receipt profile.</span></span>

### <a name="set-up-an-email-template-for-receipts"></a><span data-ttu-id="b79bf-134">受信者の電子メール テンプレートを設定</span><span class="sxs-lookup"><span data-stu-id="b79bf-134">Set up an email template for receipts</span></span>

1. <span data-ttu-id="b79bf-135">**組織管理 &gt; 設定 &gt; 電子メール テンプレート**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-135">Select **Organization administration &gt; Setup &gt; Email templates**.</span></span>
2. <span data-ttu-id="b79bf-136">Ctrl + N キーを押して新しいテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-136">Press Ctrl+N to create a template.</span></span>
3. <span data-ttu-id="b79bf-137">**概要**タブで、次のフィールドを入力します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-137">On the **Overview** tab, complete the following fields:</span></span>

    - <span data-ttu-id="b79bf-138">**電子メール ID**  フィールドに、**EmailRecpt** を入力します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-138">In the **Email ID** field, enter **EmailRecpt**.</span></span>
    - <span data-ttu-id="b79bf-139">**電子メールの説明**フィールドに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-139">In the **Email description** field, enter a description.</span></span>
    - <span data-ttu-id="b79bf-140">**既定の言語コード**フィールドで、言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-140">In the **Default language code** field, select the language.</span></span>
    - <span data-ttu-id="b79bf-141">**送信者名**フィールドに、電子メールの送信者として表示する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-141">In the **Sender name** field, specify the name that should appear as the sender of the email.</span></span> <span data-ttu-id="b79bf-142">この名前は、電子メールの**送信者**の名前として表示されます。</span><span class="sxs-lookup"><span data-stu-id="b79bf-142">Customers will see this name as the **From** name on the email.</span></span>
    - <span data-ttu-id="b79bf-143">**送信者電子メール**フィールドで、有効な電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-143">In the **Sender email** field, specify a valid email address.</span></span> <span data-ttu-id="b79bf-144">このメールアドレスは、電子メールの**送信者**のメール アドレスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="b79bf-144">Customers will see this email address as the **From** email address on the email.</span></span>

4. <span data-ttu-id="b79bf-145">下部グリッドで次のフィールドを構成します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-145">In the lower grid, configure the following fields:</span></span>

    - <span data-ttu-id="b79bf-146">**電子メール ID** フィールドが **EmailRecpt** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b79bf-146">Make sure that the **Email ID** field is set to **EmailRecpt**.</span></span>
    - <span data-ttu-id="b79bf-147">**件名**フィールドに、電子メール レシートのタイトルを入力します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-147">In the **Subject** field, enter a title for the email receipts.</span></span>
    - <span data-ttu-id="b79bf-148">**言語**フィールドで、言語を指定します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-148">In the **Language** field, specify the language.</span></span>
    - <span data-ttu-id="b79bf-149">**電子メール**フィールドに、**%message%** を入力します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-149">In the **Email** field, enter **%message%**.</span></span>
    - <span data-ttu-id="b79bf-150">送信されるメッセージにレシート以上のものを含める場合は、**電子メール メッセージ**を選択し、電子メール メッセージの本文用のテンプレートを記入します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-150">If you want the messages that are sent to include more than just the receipt, select **Email message**, and fill in the template for the body of the email messages.</span></span> <span data-ttu-id="b79bf-151">レシートが MPOS で表示されるようにするには、プレースホルダー **%message%** を挿入します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-151">If you want the receipt to appear in MPOS, insert the placeholder **%message%**.</span></span>

    <span data-ttu-id="b79bf-152">**%message%** プレースホルダーは、MPOS レシートの送信時に置き換えられる唯一のプレースホルダーです。</span><span class="sxs-lookup"><span data-stu-id="b79bf-152">The **%message%** placeholder is the only placeholder that will be replaced when MPOS receipts are sent.</span></span> <span data-ttu-id="b79bf-153">より多くのプレースホルダー オプションを取得するには、MPOS 側でカスタマイズを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b79bf-153">If you want more placeholder options, you must create a customization on the MPOS side.</span></span>

5. <span data-ttu-id="b79bf-154">設定した設定に応じて、適切な配布スケジュール ジョブを実行し、変更を MPOS に同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b79bf-154">Depending on the settings that you configured, you must run the appropriate distribution schedule jobs to synchronize the changes to MPOS.</span></span>

    - <span data-ttu-id="b79bf-155">**1010** - 顧客</span><span class="sxs-lookup"><span data-stu-id="b79bf-155">**1010** – Customer</span></span>
    - <span data-ttu-id="b79bf-156">**1070** - チャンネル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b79bf-156">**1070** – Channel configuration</span></span>
    - <span data-ttu-id="b79bf-157">**1090** - レジスター</span><span class="sxs-lookup"><span data-stu-id="b79bf-157">**1090** – Registers</span></span>
    - <span data-ttu-id="b79bf-158">**1110** - グローバル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b79bf-158">**1110** – Global configuration</span></span>

## <a name="mpos-transactions"></a><span data-ttu-id="b79bf-159">MPOS トランザクション</span><span class="sxs-lookup"><span data-stu-id="b79bf-159">MPOS transactions</span></span>

<span data-ttu-id="b79bf-160">店舗への変更が同期された後、MPOS は、ユーザーに各トランザクションの電子メール アドレスを求めます (フィーチャーが有効な場合)。</span><span class="sxs-lookup"><span data-stu-id="b79bf-160">After the changes are synchronized to the store, MPOS prompts the user for an email address for each transaction (if this feature is enabled).</span></span> <span data-ttu-id="b79bf-161">電子メール アドレスが既に顧客のファイルに割り当てられている場合、そのアドレスは電子メール アドレス プロンプトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b79bf-161">If an email address is already on file for the customer, that address appears in the email address prompt.</span></span> <span data-ttu-id="b79bf-162">顧客の名前がない場合、または名前付き顧客の電子メール アドレスが入力されていない場合は、電子メール アドレスを入力して、**送信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b79bf-162">If a customer hasn't been named, or if an email address hasn't been entered for a named customer, enter an email address, and then select **Send**.</span></span> <span data-ttu-id="b79bf-163">トランザクションが確定すると、リアルタイム サービスによって、前に構成したとおり、メッセージの本文にレシートが含まれる電子メールが顧客に送信されます。</span><span class="sxs-lookup"><span data-stu-id="b79bf-163">When the transaction is finalized, the real-time service will send the customer an email that has the receipt in the body of the message, as you configured earlier.</span></span>

