---
title: "電子メール受領を Retail Modern POS から送信"
description: "Retail Modern 販売時点管理 (MPOS) では、販売時点管理でトランザクションが支払/入金された時点でレシートの電子メールを送信できます。"
author: jashanno
manager: AnnBe
ms.date: 06/20/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 75dfe8aaef823b336ef1c2885d6e298e29f6bac4
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="send-email-receipts-from-retail-modern-pos"></a><span data-ttu-id="2d8ed-103">電子メール受領を Retail Modern POS から送信</span><span class="sxs-lookup"><span data-stu-id="2d8ed-103">Send email receipts from Retail Modern POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d8ed-104">Retail Modern 販売時点管理 (MPOS) では、販売時点管理でトランザクションが支払/入金された時点でレシートの電子メールを送信できます。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-104">In Retail Modern Point of Sale (MPOS), you can send receipt emails at the time a transaction is tendered at the point of sale.</span></span>  

<a name="prerequisite"></a><span data-ttu-id="2d8ed-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="2d8ed-105">Prerequisite</span></span>
------------

<span data-ttu-id="2d8ed-106">電子メールのレシートを送信する SMTP サーバーを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-106">You must configure a SMTP server to send email receipts.</span></span> 

## <a name="set-up-email-receipts"></a><span data-ttu-id="2d8ed-107">電子メールのレシートを設定</span><span class="sxs-lookup"><span data-stu-id="2d8ed-107">Set up email receipts</span></span>
### <a name="set-default-options-for-email-receipts"></a><span data-ttu-id="2d8ed-108">電子メールのレシートの既定のオプションの設定</span><span class="sxs-lookup"><span data-stu-id="2d8ed-108">Set default options for email receipts</span></span>

1.  <span data-ttu-id="2d8ed-109">**小売 &gt; 本社の設定 &gt; パラメーター &gt; 小売パラメーター**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-109">Click **Retail &gt; Headquarters setup &gt; Parameters &gt; Retail parameters**.</span></span>
2.  <span data-ttu-id="2d8ed-110">**転記**タブをクリックし、**電子メールのレシート**下の、**レシート オプション** フィールドで既定のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-110">Click the **Posting** tab, and then under **Email receipt**, in the **Receipt option** field, select a default option:</span></span>
    -   <span data-ttu-id="2d8ed-111">**標準受領書** – 販売時点管理 レジスターからレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-111">**Standard receipt** – Print receipts from the point of sale register.</span></span>
    -   <span data-ttu-id="2d8ed-112">**電子メール** - レシートを電子メール メッセージで顧客に送信します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-112">**E-mail** – Send receipts to customers in email messages.</span></span>
    -   <span data-ttu-id="2d8ed-113">**両方** - POS レジスターからレシートを印刷して、レシートを顧客に電子メールで送信します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-113">**Both** – Print receipts from the point of sale register and send receipts to customers in email messages.</span></span>

3.  <span data-ttu-id="2d8ed-114">**件名**フィールドに、電子メールで送信するレシートの件名行に既定で表示するテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-114">In the **Subject** field, enter the text that you want to appear by default in the subject line of a receipt that is sent as an email message.</span></span>

### <a name="set-email-receipt-options-for-a-customer"></a><span data-ttu-id="2d8ed-115">顧客の電子メールのレシート オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-115">Set email receipt options for a customer</span></span>

1.  <span data-ttu-id="2d8ed-116">**小売 &gt; 顧客 &gt; すべての顧客**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-116">Click **Retail &gt; Customers &gt; All customers**.</span></span>
2.  <span data-ttu-id="2d8ed-117">**すべての顧客**リストページで、顧客を選択し、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-117">On the **All customers** list page, select a customer, then click **Edit**.</span></span>
3.  <span data-ttu-id="2d8ed-118">**顧客の詳細**ページの、**小売**のクイック タブで、**レシート オプション**フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-118">On the **Customers details** page, on the **Retail** FastTab, select an option in the **Receipt option** field:</span></span>
    -   <span data-ttu-id="2d8ed-119">**標準受領書** – 顧客は印刷されたレシートのみを受信します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-119">**Standard receipt** – The customer will receive only printed receipts.</span></span> <span data-ttu-id="2d8ed-120">印刷されたレシートは POS レジスターから生成されます。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-120">The printed receipt is generated from the point of sale register.</span></span>
    -   <span data-ttu-id="2d8ed-121">**電子メール** - 顧客は電子メールのレシートのみを受信します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-121">**E-mail** – The customer will receive only email receipts.</span></span>
    -   <span data-ttu-id="2d8ed-122">**両方** - 顧客は印刷されたレシートと電子メールのレシートの両方を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-122">**Both** – The customer will receive both a printed receipt and an email receipt.</span></span>

4.  <span data-ttu-id="2d8ed-123">**受領書の電子メール** フィールドで、**電子メール**または**両方**のいずれかを**受領書オプション** フィールドで選択した場合、顧客の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-123">In the **Receipt email** field, if you selected either **E-mail** or **Both** in the **Receipt option** field, enter the customer’s email address .</span></span>

### <a name="set-up-an-email-template-for-receipts"></a><span data-ttu-id="2d8ed-124">受信者の電子メール テンプレートを設定</span><span class="sxs-lookup"><span data-stu-id="2d8ed-124">Set up an email template for receipts</span></span>

1. <span data-ttu-id="2d8ed-125">**組織管理 &gt; 設定 &gt; 電子メール テンプレート**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-125">Click **Organization Administration &gt; Setup &gt; E-mail Templates.**</span></span>
2. <span data-ttu-id="2d8ed-126">新しいテンプレートを作成するには、**CTRL**+**N** を押します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-126">Press **CTRL**+**N** to create a new template.</span></span>
3. <span data-ttu-id="2d8ed-127">**概要**タブで、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-127">On the **Overview** tab, complete the following:</span></span>
   - <span data-ttu-id="2d8ed-128">**電子メール ID** - *EmailRecpt* を入力します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-128">**E-mail ID** - Enter *EmailRecpt*.</span></span>
   - <span data-ttu-id="2d8ed-129">**電子メールの説明**- 説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-129">**E-mail description **- Enter a description.</span></span>
   - <span data-ttu-id="2d8ed-130">**既定の言語コード**- 言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-130">**Default language code **- Select the  language.</span></span>
   - <span data-ttu-id="2d8ed-131"><strong>送信者名** - 電子メールの送信者として表示する名前を指定します。この名前は電子メールで**送信元</strong>の名前として顧客に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-131"><strong>Sender name **- Specify a name to appear as the sender of the email. Customers will see this name on the email as the **From</strong> name.</span></span>
   - <span data-ttu-id="2d8ed-132"><strong>送信者の電子メール** - 有効な電子メール アドレスを指定します。この電子メール アドレスは**送信元</strong>電子メール アドレスとして顧客に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-132"><strong>Sender e-mail **- Specify a valid email address. Customers will see this email address as the **From</strong> email address.</span></span>

4. <span data-ttu-id="2d8ed-133">下部グリッドで次を構成します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-133">In the lower grid, configure the following:</span></span>
   - <span data-ttu-id="2d8ed-134"><em>*電子メール ID**- これは *EmailRecpt として既に入力されている必要があります。</em></span><span class="sxs-lookup"><span data-stu-id="2d8ed-134"><em>*E-mail ID **- This should already be populated as *EmailRecpt</em>.</span></span>
   - <span data-ttu-id="2d8ed-135">**件名** - 電子メール レシートのタイトルを入力します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-135">**Subject **- Enter a title for the email receipts.</span></span>
   - <span data-ttu-id="2d8ed-136">**言語**- 言語を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-136">**Language **- Specify the language.</span></span>
   - <span data-ttu-id="2d8ed-137"><em>*電子メール**: 次の文字列を挿入します: *&lt;pre&gt;%message%&lt;/pre&gt;。</em></span><span class="sxs-lookup"><span data-stu-id="2d8ed-137"><em>*Email **- Insert the following string: *&lt;pre&gt;%message%&lt;/pre&gt;.</em></span></span>
   - <span data-ttu-id="2d8ed-138">メッセージにレシート以上のものを載せる場合、**電子メール メッセージ** ボタンをクリックし、送信される電子メール メッセージの本文のテンプレートを記入します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-138">If you want to have more than just the receipt in the message, click the **E-mail message** button to fill out the template for the body of the email messages to be sent.</span></span> <span data-ttu-id="2d8ed-139">入庫を (MPOS で) 表示するには、プレースホルダー *%message%.* を挿入します。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-139">If you want the receipt to appear (in MPOS), insert the placeholder *%message%.*</span></span>

<span data-ttu-id="2d8ed-140">これは、MPOS の領収書を送信するときに置き換えられる唯一のプレースホルダーです。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-140">This is the only placeholder that will be replaced when sending MPOS receipts.</span></span> <span data-ttu-id="2d8ed-141">より多くのプレースホルダー オプションを取得するには、MPOS 側でカスタマイズを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-141">To get more placeholder options, you'll need to create customization on the MPOS side.</span></span>

<span data-ttu-id="2d8ed-142">設定した設定に応じて、それぞれの配布スケジュールジョブを実行して、変更を MPOS に同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-142">Depending on the settings that you configured, you'll need to run the respective distribution schedule jobs to sync the changes to MPOS.</span></span>

-   <span data-ttu-id="2d8ed-143">**1010** - 顧客</span><span class="sxs-lookup"><span data-stu-id="2d8ed-143">**1010** – Customer</span></span>
-   <span data-ttu-id="2d8ed-144">**1070** - チャンネル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2d8ed-144">**1070** – Channel configuration</span></span>
-   <span data-ttu-id="2d8ed-145">**1090** - レジスター</span><span class="sxs-lookup"><span data-stu-id="2d8ed-145">**1090** – Registers</span></span>
-   <span data-ttu-id="2d8ed-146">**1110** - グローバル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2d8ed-146">**1110** – Global configuration</span></span>

## <a name="mpos-transaction"></a><span data-ttu-id="2d8ed-147">MPOS トランザクション</span><span class="sxs-lookup"><span data-stu-id="2d8ed-147">MPOS transaction</span></span>
<span data-ttu-id="2d8ed-148">店舗への変更を同期した後、MPOS は、ユーザーに各トランザクションの電子メール アドレスも求めます (有効な場合)。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-148">After synchronizing the changes to the store, MPOS will prompt the user for an email address for each transaction (if enabled).</span></span> <span data-ttu-id="2d8ed-149">顧客の電子メール アドレスがファイルに既に割り当てられている場合、そのアドレスは、電子メール アドレス プロンプトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-149">If the customer already has an email address on file, that address will appear in the email address prompt.</span></span> <span data-ttu-id="2d8ed-150">顧客名が指定されていない、または名前付きの顧客が電子メール アドレスを持っていない場合、電子メール アドレスを入力し、**送信**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-150">If a customer hasn't been named, or the named customer doesn’t have an email address, enter an email address and then click **Send**.</span></span> <span data-ttu-id="2d8ed-151">トランザクションが確定すると、リアルタイム サービスによって、上記の構成の通りに、メッセージの本文にレシートが含まれる電子メールが顧客に送信されます。</span><span class="sxs-lookup"><span data-stu-id="2d8ed-151">When the transaction is finalized, the real-time service will send the customer an email with the receipt in the body of the message as configured above.</span></span>




