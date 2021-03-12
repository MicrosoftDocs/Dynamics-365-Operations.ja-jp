---
title: トランザクション イベント用の電子メール テンプレートの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce のトランザクション イベントにおける電子メールテンプレートの作成、アップロード、構成する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 06/01/2020
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
ms.openlocfilehash: 245ca998ef3e6d172df3525f06d7901f3f41b650
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000788"
---
# <a name="create-email-templates-for-transactional-events"></a><span data-ttu-id="db872-103">トランザクション イベント用の電子メール テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="db872-103">Create email templates for transactional events</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db872-104">このトピックでは、Microsoft Dynamics 365 Commerce のトランザクション イベントにおける電子メールテンプレートの作成、アップロード、構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="db872-104">This topic describes how to create, upload, and configure email templates for transactional events in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="db872-105">概要</span><span class="sxs-lookup"><span data-stu-id="db872-105">Overview</span></span>

<span data-ttu-id="db872-106">Dynamics 365 Commerce では、トランザクション イベントについて顧客に通知する電子メールを送信する既成のソリューションが用意されています (たとえば、注文が行われたり、注文が集配できる状態になったり、注文が出荷されたりした場合など)。</span><span class="sxs-lookup"><span data-stu-id="db872-106">Dynamics 365 Commerce provides an out-of-box solution for sending emails that alert customers about transactional events (for example, when an order is placed, an order is ready for pickup, or an order has been shipped).</span></span> <span data-ttu-id="db872-107">このトピックでは、トランザクション電子メールの送信に使用される電子メール テンプレートの作成、アップロード、構成をする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="db872-107">This topic describes the steps for creating, uploading, and configuring the email templates that are used to send transactional emails.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="db872-108">電子メール テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="db872-108">Create an email template</span></span>

<span data-ttu-id="db872-109">特定のトランザクション イベントを電子メールのテンプレートにマッピングするには、事前にテンプレートを作成しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="db872-109">Before you can map a specific transactional event to an email template, you must create the template.</span></span>

<span data-ttu-id="db872-110">電子メール テンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="db872-110">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="db872-111">Commerce 本部で **Retail と Commerce \> 本社の設定 \> 組織の電子メール テンプレート** または、**組織管理 \> 設定 \> 組織の電子メール テンプレート** にある **組織の電子メールテンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="db872-111">In Commerce headquarters, go to **Organization email templates**, which is under **Retail and Commerce \> Headquarters setup \> Organization email templates** or **Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="db872-112">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db872-112">Select **New**.</span></span>
1. <span data-ttu-id="db872-113">**全般** 配下で、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="db872-113">Under **General**, set the following fields:</span></span>

    - <span data-ttu-id="db872-114">**電子メール ID** – 電子メール ID はテンプレートに固有の ID であり、イベントにマッピングするテンプレートを選択した際に表示される値です。</span><span class="sxs-lookup"><span data-stu-id="db872-114">**Email ID** – The email ID is the unique identifier for a template, and it's the value that is shown when you select a template to map to an event.</span></span>
    - <span data-ttu-id="db872-115">**電子メールの説明** – このオプション フィールドを使用して、テンプレートの説明を入力できます。</span><span class="sxs-lookup"><span data-stu-id="db872-115">**Email description** – You can use this optional field to provide a description of the template.</span></span> <span data-ttu-id="db872-116">入力した値は、Commerce 本部でのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="db872-116">The value that you enter appears only in Commerce headquarters.</span></span>
    - <span data-ttu-id="db872-117">**送信者名** – ここに入力した名前が、ほとんどの電子メール クライアントの [差出人] フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="db872-117">**Sender name** – The name that you enter appears in the "from" field of most email clients.</span></span>
    - <span data-ttu-id="db872-118">**送信者の電子メール** – このテンプレートを使用して送信する電子メールが使用する電子メールのアドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="db872-118">**Sender email** – Enter the email address that should be used for emails that are sent by using this template.</span></span>
    - <span data-ttu-id="db872-119">**既定の言語コード** – このテンプレートを呼び出すチャネルで言語が提供されていない場合、送信される電子メールのローカライズされたバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="db872-119">**Default language code** – This field specifies the localized version of the email that is sent by default, if no language is provided by the channel that invokes this template.</span></span>

1. <span data-ttu-id="db872-120">**電子メール メッセージ コンテンツ** 配下で、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db872-120">Under **Email message content**, select **New**.</span></span>
1. <span data-ttu-id="db872-121">**言語** フィールドに、電子メール テンプレートの言語を入力します。</span><span class="sxs-lookup"><span data-stu-id="db872-121">In the **Language** field, enter the language for the email template.</span></span> <span data-ttu-id="db872-122">言語とローカライズされたテンプレートは後で追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="db872-122">You can add more languages and localized templates later.</span></span>
1. <span data-ttu-id="db872-123">**件名** フィールドには、電子メールの件名フィールドに表示される件名を入力します。</span><span class="sxs-lookup"><span data-stu-id="db872-123">In the **Subject** field, enter the email subject that should appear in the subject field of the email.</span></span>
1. <span data-ttu-id="db872-124">電子メールのテンプレートをアップロードするには、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db872-124">Select **Edit** to upload your email template.</span></span>

## <a name="create-an-email-message-body-by-using-html"></a><span data-ttu-id="db872-125">HTML を使用して電子メール メッセージの本文を作成する</span><span class="sxs-lookup"><span data-stu-id="db872-125">Create an email message body by using HTML</span></span>

<span data-ttu-id="db872-126">電子メール メッセージの本文はHTMLで構成されています。</span><span class="sxs-lookup"><span data-stu-id="db872-126">The message body of your email is composed in HTML.</span></span> <span data-ttu-id="db872-127">HTML およびインライン カスケードスタイルシート (CSS) で使用できる任意のレイアウト、スタイル、ブランディングを使用できます。</span><span class="sxs-lookup"><span data-stu-id="db872-127">You can use any layout, styling, and branding that HTML and inline Cascading Style Sheets (CSS) allow for.</span></span> <span data-ttu-id="db872-128">一般に公開されている web のエンドポイントに画像をホストする場合は、画像を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="db872-128">You can also use images, if you host them on a publicly available web endpoint.</span></span> <span data-ttu-id="db872-129">画像を追加するには、HTML **&lt;img&gt;** タグの **src** 属性に画像のURLを入力します。</span><span class="sxs-lookup"><span data-stu-id="db872-129">To add an image, enter the image's URL in the **src** attribute of the HTML **&lt;img&gt;** tag.</span></span>

> [!NOTE]
> <span data-ttu-id="db872-130">電子メール クライアントにはレイアウトやスタイルの制限があり、メッセージ本文に使用するHTMLや CSS の調整が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="db872-130">Email clients impose layout and style limitations that might require adjustments to the HTML and CSS that you use for the message body.</span></span> <span data-ttu-id="db872-131">人気の高い電子メール クライアントで対応しているHTMLを作成するためのベストプラクティスについて理解しておくことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="db872-131">We recommend that you familiarize yourself with the best practices for creating HTML that will be supported by the most popular email clients.</span></span>

## <a name="add-placeholders-to-the-email-message-body"></a><span data-ttu-id="db872-132">電子メール メッセージの本文にプレースホルダーを追加する</span><span class="sxs-lookup"><span data-stu-id="db872-132">Add placeholders to the email message body</span></span>

<span data-ttu-id="db872-133">電子メールにはプレースホルダーを含めることができます。これは電子メールが生成された際に顧客固有の値やトランザクション固有の値に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="db872-133">Your email can contain placeholders that are replaced with customer-specific and transaction-specific values when the email is generated.</span></span> <span data-ttu-id="db872-134">プレースホルダは常にパーセント記号 (%) で囲まれており、HTML 文書の中に直接挿入されます。</span><span class="sxs-lookup"><span data-stu-id="db872-134">Placeholders are always surrounded by percent signs (%) and are inserted directly into the HTML document.</span></span>

<span data-ttu-id="db872-135">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="db872-135">Here is an example.</span></span>

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a><span data-ttu-id="db872-136">注文のプレースホルダー (販売注文レベル)</span><span class="sxs-lookup"><span data-stu-id="db872-136">Order placeholders (sales order level)</span></span>

<span data-ttu-id="db872-137">以下のプレースホルダーは、販売注文レベルで定義されたデータを取得して表示します (販売明細行レベルとは異なります)。</span><span class="sxs-lookup"><span data-stu-id="db872-137">The following placeholders retrieve and show data that is defined at the sales order level (as opposed to the sales line level).</span></span>

| <span data-ttu-id="db872-138">プレースホルダー名</span><span class="sxs-lookup"><span data-stu-id="db872-138">Placeholder name</span></span>    | <span data-ttu-id="db872-139">プレースホルダー値</span><span class="sxs-lookup"><span data-stu-id="db872-139">Placeholder value</span></span>                                                |
|---------------------|------------------------------------------------------------------|
| <span data-ttu-id="db872-140">customername</span><span class="sxs-lookup"><span data-stu-id="db872-140">customername</span></span>        | <span data-ttu-id="db872-141">注文を行った顧客の名称です。</span><span class="sxs-lookup"><span data-stu-id="db872-141">The name of the customer who placed the order.</span></span>                   |
| <span data-ttu-id="db872-142">salesid</span><span class="sxs-lookup"><span data-stu-id="db872-142">salesid</span></span>             | <span data-ttu-id="db872-143">注文の販売 ID です。</span><span class="sxs-lookup"><span data-stu-id="db872-143">The sales ID of the order.</span></span>                                       |
| <span data-ttu-id="db872-144">deliveryaddress</span><span class="sxs-lookup"><span data-stu-id="db872-144">deliveryaddress</span></span>     | <span data-ttu-id="db872-145">出荷注文の配送先住所です。</span><span class="sxs-lookup"><span data-stu-id="db872-145">The delivery address for shipped orders.</span></span>                         |
| <span data-ttu-id="db872-146">customeraddress</span><span class="sxs-lookup"><span data-stu-id="db872-146">customeraddress</span></span>     | <span data-ttu-id="db872-147">顧客の住所です。</span><span class="sxs-lookup"><span data-stu-id="db872-147">The address of the customer.</span></span>                                     |
| <span data-ttu-id="db872-148">deliverydate</span><span class="sxs-lookup"><span data-stu-id="db872-148">deliverydate</span></span>        | <span data-ttu-id="db872-149">配送日です。</span><span class="sxs-lookup"><span data-stu-id="db872-149">The delivery date.</span></span>                                               |
| <span data-ttu-id="db872-150">shipdate</span><span class="sxs-lookup"><span data-stu-id="db872-150">shipdate</span></span>            | <span data-ttu-id="db872-151">出荷日です。</span><span class="sxs-lookup"><span data-stu-id="db872-151">The ship date.</span></span>                                                   |
| <span data-ttu-id="db872-152">modeofdelivery</span><span class="sxs-lookup"><span data-stu-id="db872-152">modeofdelivery</span></span>      | <span data-ttu-id="db872-153">注文の出荷モードです。</span><span class="sxs-lookup"><span data-stu-id="db872-153">The delivery mode of the order.</span></span>                                  |
| <span data-ttu-id="db872-154">請求</span><span class="sxs-lookup"><span data-stu-id="db872-154">charges</span></span>             | <span data-ttu-id="db872-155">注文に対する金額の合計です。</span><span class="sxs-lookup"><span data-stu-id="db872-155">The total charges for the order.</span></span>                                 |
| <span data-ttu-id="db872-156">税</span><span class="sxs-lookup"><span data-stu-id="db872-156">tax</span></span>                 | <span data-ttu-id="db872-157">注文の税の合計です。</span><span class="sxs-lookup"><span data-stu-id="db872-157">The total tax for the order.</span></span>                                     |
| <span data-ttu-id="db872-158">合計</span><span class="sxs-lookup"><span data-stu-id="db872-158">total</span></span>               | <span data-ttu-id="db872-159">注文に対する金額の総計です。</span><span class="sxs-lookup"><span data-stu-id="db872-159">The total amount for the order.</span></span>                                  |
| <span data-ttu-id="db872-160">ordernetamount</span><span class="sxs-lookup"><span data-stu-id="db872-160">ordernetamount</span></span>      | <span data-ttu-id="db872-161">注文の合計金額から税の合計を差し引いた金額です。</span><span class="sxs-lookup"><span data-stu-id="db872-161">The total amount for the order, minus the total tax.</span></span>             |
| <span data-ttu-id="db872-162">割引</span><span class="sxs-lookup"><span data-stu-id="db872-162">discount</span></span>            | <span data-ttu-id="db872-163">注文に対する割引の合計です。</span><span class="sxs-lookup"><span data-stu-id="db872-163">The total discount for the order.</span></span>                                |
| <span data-ttu-id="db872-164">storename</span><span class="sxs-lookup"><span data-stu-id="db872-164">storename</span></span>           | <span data-ttu-id="db872-165">注文を行った店舗の名称です。</span><span class="sxs-lookup"><span data-stu-id="db872-165">The name of the store where the order was placed.</span></span>                |
| <span data-ttu-id="db872-166">storeaddress</span><span class="sxs-lookup"><span data-stu-id="db872-166">storeaddress</span></span>        | <span data-ttu-id="db872-167">注文を行った顧客の住所です。</span><span class="sxs-lookup"><span data-stu-id="db872-167">The address of the store that placed the order.</span></span>                  |
| <span data-ttu-id="db872-168">storeopenfrom</span><span class="sxs-lookup"><span data-stu-id="db872-168">storeopenfrom</span></span>       | <span data-ttu-id="db872-169">注文を行った店舗の開店時間です。</span><span class="sxs-lookup"><span data-stu-id="db872-169">The opening time of the store that placed the order.</span></span>             |
| <span data-ttu-id="db872-170">storeopento</span><span class="sxs-lookup"><span data-stu-id="db872-170">storeopento</span></span>         | <span data-ttu-id="db872-171">注文を行った店舗の閉店時間です。</span><span class="sxs-lookup"><span data-stu-id="db872-171">The closing time of the store that placed the order.</span></span>             |
| <span data-ttu-id="db872-172">pickupstorename</span><span class="sxs-lookup"><span data-stu-id="db872-172">pickupstorename</span></span>     | <span data-ttu-id="db872-173">注文が受け取られる店舗の名称です。</span><span class="sxs-lookup"><span data-stu-id="db872-173">The name of the store where the order will be picked up.</span></span>         |
| <span data-ttu-id="db872-174">pickupstoreaddress</span><span class="sxs-lookup"><span data-stu-id="db872-174">pickupstoreaddress</span></span>  | <span data-ttu-id="db872-175">注文がピッキングされる店舗の住所です。</span><span class="sxs-lookup"><span data-stu-id="db872-175">The address of the store where the order will be picked up.</span></span>      |
| <span data-ttu-id="db872-176">pickupopenstorefrom</span><span class="sxs-lookup"><span data-stu-id="db872-176">pickupopenstorefrom</span></span> | <span data-ttu-id="db872-177">注文がピッキングされる店舗の開店時間です。</span><span class="sxs-lookup"><span data-stu-id="db872-177">The opening time of the store where the order will be picked up.</span></span> |
| <span data-ttu-id="db872-178">pickupopenstoreto</span><span class="sxs-lookup"><span data-stu-id="db872-178">pickupopenstoreto</span></span>   | <span data-ttu-id="db872-179">注文がピッキングされる店舗の閉店時間です。</span><span class="sxs-lookup"><span data-stu-id="db872-179">The closing time of the store where the order will be picked up.</span></span> |

### <a name="order-line-placeholders-sales-line-level"></a><span data-ttu-id="db872-180">注文ラインのプレースホルダー (販売ライン レベル)</span><span class="sxs-lookup"><span data-stu-id="db872-180">Order line placeholders (sales line level)</span></span>

<span data-ttu-id="db872-181">以下のプレースホルダーは、販売注文の個々の製品 (明細行) のデータを取得して表示します。</span><span class="sxs-lookup"><span data-stu-id="db872-181">The following placeholders retrieve and show data for individual products (lines) in the sales order.</span></span>

| <span data-ttu-id="db872-182">プレースホルダー名</span><span class="sxs-lookup"><span data-stu-id="db872-182">Placeholder name</span></span>               | <span data-ttu-id="db872-183">プレースホルダー値</span><span class="sxs-lookup"><span data-stu-id="db872-183">Placeholder value</span></span> |
|--------------------------------|-------------------|
| <span data-ttu-id="db872-184">productid</span><span class="sxs-lookup"><span data-stu-id="db872-184">productid</span></span>                      | <span data-ttu-id="db872-185">明細行の製品 ID です。</span><span class="sxs-lookup"><span data-stu-id="db872-185">The product ID for the line.</span></span> |
| <span data-ttu-id="db872-186">lineproductname</span><span class="sxs-lookup"><span data-stu-id="db872-186">lineproductname</span></span>                | <span data-ttu-id="db872-187">生産の名前。</span><span class="sxs-lookup"><span data-stu-id="db872-187">The name of the product.</span></span> |
| <span data-ttu-id="db872-188">lineproductdescription</span><span class="sxs-lookup"><span data-stu-id="db872-188">lineproductdescription</span></span>         | <span data-ttu-id="db872-189">製品の説明。</span><span class="sxs-lookup"><span data-stu-id="db872-189">The description of the product.</span></span> |
| <span data-ttu-id="db872-190">linequantity</span><span class="sxs-lookup"><span data-stu-id="db872-190">linequantity</span></span>                   | <span data-ttu-id="db872-191">ラインに発注された単位数と測定単位 (**ea**、**pair** など) です。</span><span class="sxs-lookup"><span data-stu-id="db872-191">The number of units that were ordered for the line, plus the unit of measure (for example, **ea**, or **pair**).</span></span> |
| <span data-ttu-id="db872-192">lineunit</span><span class="sxs-lookup"><span data-stu-id="db872-192">lineunit</span></span>                       | <span data-ttu-id="db872-193">ラインの測定単位です。</span><span class="sxs-lookup"><span data-stu-id="db872-193">The unit of measure for the line.</span></span> |
| <span data-ttu-id="db872-194">linequantity_withoutunit</span><span class="sxs-lookup"><span data-stu-id="db872-194">linequantity_withoutunit</span></span>       | <span data-ttu-id="db872-195">ラインに発注された単位数で、測定単位を含まないもの。</span><span class="sxs-lookup"><span data-stu-id="db872-195">The number of units that were ordered for the line, without the unit of measure.</span></span> |
| <span data-ttu-id="db872-196">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="db872-196">linequantitypicked</span></span>             | <span data-ttu-id="db872-197">注文の **PickOrder** イベントが使用された場合の、ピッキングされた単位の数です。</span><span class="sxs-lookup"><span data-stu-id="db872-197">When the **PickOrder** event is used, the number of units that were picked.</span></span> <span data-ttu-id="db872-198">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="db872-198">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="db872-199">linequantitypicked_withoutunit</span><span class="sxs-lookup"><span data-stu-id="db872-199">linequantitypicked_withoutunit</span></span> | <span data-ttu-id="db872-200">**PickOrder** イベントが使用された場合の、測定単位を含まない、ピッキングされた単位の数です。</span><span class="sxs-lookup"><span data-stu-id="db872-200">When the **PickOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="db872-201">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="db872-201">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="db872-202">linequantitypacked</span><span class="sxs-lookup"><span data-stu-id="db872-202">linequantitypacked</span></span>             | <span data-ttu-id="db872-203">**PackOrder** および **ピックアップ可能な注文** イベントが使用された場合の、梱包された単位数です。</span><span class="sxs-lookup"><span data-stu-id="db872-203">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed.</span></span> <span data-ttu-id="db872-204">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="db872-204">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="db872-205">linequantitypacked_withoutuom</span><span class="sxs-lookup"><span data-stu-id="db872-205">linequantitypacked_withoutuom</span></span>  | <span data-ttu-id="db872-206">**PackOrder** および **ピックアップ可能な注文** イベントが使用された場合の、測定単位を含まない、梱包された単位数です。</span><span class="sxs-lookup"><span data-stu-id="db872-206">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed, without the unit of measure.</span></span> <span data-ttu-id="db872-207">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="db872-207">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="db872-208">linequantityshipped</span><span class="sxs-lookup"><span data-stu-id="db872-208">linequantityshipped</span></span>            | <span data-ttu-id="db872-209">以下に説明するように、特定のイベントが使用されている場合を除き、常に **0** となります。</span><span class="sxs-lookup"><span data-stu-id="db872-209">Always **0**, except when specific events are used, as described in the next row.</span></span> |
| <span data-ttu-id="db872-210">linequantityshipped_withoutuom</span><span class="sxs-lookup"><span data-stu-id="db872-210">linequantityshipped_withoutuom</span></span> | <span data-ttu-id="db872-211">**ShipOrder** イベントが使用された場合の、測定単位を含まない、ピッキングされた単位の数です。</span><span class="sxs-lookup"><span data-stu-id="db872-211">When the **ShipOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="db872-212">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="db872-212">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="db872-213">lineprice</span><span class="sxs-lookup"><span data-stu-id="db872-213">lineprice</span></span>                      | <span data-ttu-id="db872-214">一単位の価格です。</span><span class="sxs-lookup"><span data-stu-id="db872-214">The price of a single unit.</span></span> |
| <span data-ttu-id="db872-215">linenetamount</span><span class="sxs-lookup"><span data-stu-id="db872-215">linenetamount</span></span>                  | <span data-ttu-id="db872-216">単位および適用後のラインの価格です。</span><span class="sxs-lookup"><span data-stu-id="db872-216">The price of the line after the number of units and discount are applied.</span></span> |
| <span data-ttu-id="db872-217">linediscount</span><span class="sxs-lookup"><span data-stu-id="db872-217">linediscount</span></span>                   | <span data-ttu-id="db872-218">個々の単位の割引です。</span><span class="sxs-lookup"><span data-stu-id="db872-218">The discount for an individual unit.</span></span> |
| <span data-ttu-id="db872-219">lineshipdate</span><span class="sxs-lookup"><span data-stu-id="db872-219">lineshipdate</span></span>                   | <span data-ttu-id="db872-220">当該ラインの出荷日です。</span><span class="sxs-lookup"><span data-stu-id="db872-220">The ship date for the line.</span></span> |
| <span data-ttu-id="db872-221">linedeliverydate</span><span class="sxs-lookup"><span data-stu-id="db872-221">linedeliverydate</span></span>               | <span data-ttu-id="db872-222">当該ラインの配達日です。</span><span class="sxs-lookup"><span data-stu-id="db872-222">The delivery date for the line.</span></span> |
| <span data-ttu-id="db872-223">linedeliverymode</span><span class="sxs-lookup"><span data-stu-id="db872-223">linedeliverymode</span></span>               | <span data-ttu-id="db872-224">当該ラインの配送モードです。</span><span class="sxs-lookup"><span data-stu-id="db872-224">The delivery mode for the line.</span></span> |
| <span data-ttu-id="db872-225">linedeliveryaddress</span><span class="sxs-lookup"><span data-stu-id="db872-225">linedeliveryaddress</span></span>            | <span data-ttu-id="db872-226">当該ラインの配達先住所です。</span><span class="sxs-lookup"><span data-stu-id="db872-226">The delivery address for the line.</span></span> |
| <span data-ttu-id="db872-227">giftcardnumber</span><span class="sxs-lookup"><span data-stu-id="db872-227">giftcardnumber</span></span>                 | <span data-ttu-id="db872-228">ギフト カード タイプの製品の場合の、ギフトカード番号です。</span><span class="sxs-lookup"><span data-stu-id="db872-228">The gift card number, for products of the gift card type.</span></span> |
| <span data-ttu-id="db872-229">giftcardbalance</span><span class="sxs-lookup"><span data-stu-id="db872-229">giftcardbalance</span></span>                | <span data-ttu-id="db872-230">ギフト カード タイプの製品の場合の、ギフトカード残高です。</span><span class="sxs-lookup"><span data-stu-id="db872-230">The gift card balance, for products of the gift card type.</span></span> |
| <span data-ttu-id="db872-231">giftcardmessage</span><span class="sxs-lookup"><span data-stu-id="db872-231">giftcardmessage</span></span>                | <span data-ttu-id="db872-232">ギフト カード タイプの製品の場合の、ギフトカードのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="db872-232">The gift card message, for products of the gift card type.</span></span> |
| <span data-ttu-id="db872-233">giftcardpin</span><span class="sxs-lookup"><span data-stu-id="db872-233">giftcardpin</span></span>                    | <span data-ttu-id="db872-234">ギフト カード タイプの製品の場合の、ギフトカードの識別番号 (PIN) です。</span><span class="sxs-lookup"><span data-stu-id="db872-234">The personal identification number (PIN) of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="db872-235">(このプレースホルダーは、外部のギフトカードに固有のものです)</span><span class="sxs-lookup"><span data-stu-id="db872-235">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="db872-236">giftcardexpiration</span><span class="sxs-lookup"><span data-stu-id="db872-236">giftcardexpiration</span></span>             | <span data-ttu-id="db872-237">ギフト カード タイプの製品の場合の、ギフトカードの有効期限です。</span><span class="sxs-lookup"><span data-stu-id="db872-237">The expiration date of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="db872-238">(このプレースホルダーは、外部のギフトカードに固有のものです)</span><span class="sxs-lookup"><span data-stu-id="db872-238">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="db872-239">giftcardrecipientname</span><span class="sxs-lookup"><span data-stu-id="db872-239">giftcardrecipientname</span></span>          | <span data-ttu-id="db872-240">ギフト カード タイプの製品の場合の、ギフトカードの受取人の名前です。</span><span class="sxs-lookup"><span data-stu-id="db872-240">The name of the gift card recipient, for products of the gift card type.</span></span> |
| <span data-ttu-id="db872-241">giftcardbuyername</span><span class="sxs-lookup"><span data-stu-id="db872-241">giftcardbuyername</span></span>              | <span data-ttu-id="db872-242">ギフト カード タイプの製品の場合の、ギフトカードの購入者の名前です。</span><span class="sxs-lookup"><span data-stu-id="db872-242">The name of the gift card buyer, for products of the gift card type.</span></span> |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a><span data-ttu-id="db872-243">電子メール メッセージ本文における注文明細行のプレースホルダーの形式</span><span class="sxs-lookup"><span data-stu-id="db872-243">Format of order line placeholders in the email message body</span></span>

<span data-ttu-id="db872-244">電子メールのメッセージ本文内の個々の注文明細行の HTML を作成する際には、HTML の繰り返しブロックとその行のプレースホルダーを、HTML のコメントタグの中に入れた以下のプレースホルダーで囲みます。</span><span class="sxs-lookup"><span data-stu-id="db872-244">When you create the HTML for the individual order lines in the email message body, surround the repeating block of HTML and placeholders for the lines with the following placeholders that are put inside HTML comment tags.</span></span>

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

<span data-ttu-id="db872-245">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="db872-245">Here is an example.</span></span>

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a><span data-ttu-id="db872-246">メールで送信される領収書のテンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="db872-246">Create a template for emailed receipts</span></span>

<span data-ttu-id="db872-247">領収書は、販売時点管理 (POS) で購入した顧客に電子メールで送信することができます。</span><span class="sxs-lookup"><span data-stu-id="db872-247">Receipts can be emailed to customers who make purchases at a retail point of sale (POS).</span></span> <span data-ttu-id="db872-248">一般的には、メールで送信する領収書のテンプレートの作成手順は、その他のトランザクション イベントのテンプレートの作成手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="db872-248">In general, the steps for creating the emailed receipt template are the same as the steps for creating templates for other transactional events.</span></span> <span data-ttu-id="db872-249">この場合、以下の変更が必要となります:</span><span class="sxs-lookup"><span data-stu-id="db872-249">However, the following changes are required:</span></span>

- <span data-ttu-id="db872-250">電子メールのテンプレートで使用するメール ID には **emailRecpt** を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db872-250">The email ID of the email template must be **emailRecpt**.</span></span>
- <span data-ttu-id="db872-251">領収書のテキストは、**%message%** のプレースホルダーを使用して電子メールに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="db872-251">The text of the receipt is inserted into the email by using the **%message%** placeholder.</span></span> <span data-ttu-id="db872-252">領収書の本文が正しく表示されるように、 **%message%** プレースホルダーを HTML タグの **&lt;pre&gt;** **&lt;/pre&gt;** で囲みます。</span><span class="sxs-lookup"><span data-stu-id="db872-252">To ensure that the receipt body is correctly rendered, surround the **%message%** placeholder with HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tags.</span></span>
- <span data-ttu-id="db872-253">電子メールのヘッダーとフッターにおける HTML の改行は、領収書の本文が正しく表示されるように HTML の **&lt;br /&gt;** タグに変換されます。</span><span class="sxs-lookup"><span data-stu-id="db872-253">Line breaks in the HTML for the header and footer of the email are converted to HTML **&lt;br /&gt;** tags so that the receipt body is rendered correctly.</span></span> <span data-ttu-id="db872-254">領収書メールの不要な縦のスペースを削除するには、HTML 内の縦のスペースが不要な場所で改行を削除します。</span><span class="sxs-lookup"><span data-stu-id="db872-254">To eliminate unwanted vertical space in your receipt emails, remove line breaks from any place in the HTML where vertical space isn't required.</span></span>

<span data-ttu-id="db872-255">電子メールで送信する領収書の構成方法については、[電子メールで送信する領収書の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db872-255">For more information about how to configure email receipts, see [Set up email receipts](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts).</span></span>

## <a name="upload-the-email-html"></a><span data-ttu-id="db872-256">電子メールの HTML をアップロードする</span><span class="sxs-lookup"><span data-stu-id="db872-256">Upload the email HTML</span></span>

<span data-ttu-id="db872-257">HTML を作成し、テストした後は、メッセージの本文を Commerce 本部にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="db872-257">After you've created and tested the HTML for your message body, it must be uploaded to Commerce headquarters.</span></span> <span data-ttu-id="db872-258">現時点では、電子メールの HTML はエクスポートできません。</span><span class="sxs-lookup"><span data-stu-id="db872-258">Currently, email HTML can't be exported.</span></span> <span data-ttu-id="db872-259">そのため、HTML のマスターコピーは Commerce 本部以外で管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db872-259">Therefore, you must maintain the master copy of your HTML outside Commerce headquarters.</span></span>

<span data-ttu-id="db872-260">新規、または編集した電子メールのテンプレート HTML をアップロードするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="db872-260">To upload a new or edited email template HTML, follow these steps.</span></span>

1. <span data-ttu-id="db872-261">Commerce 本部で、**小売りとコマース \> 本部の設定 \> 組織の電子メールのテンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="db872-261">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="db872-262">HTML を追加または置換する言語の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="db872-262">Select the row for the language that you want to add or replace HTML for.</span></span> <span data-ttu-id="db872-263">または、**新規** を選択して新しい言語の行を作成します。</span><span class="sxs-lookup"><span data-stu-id="db872-263">Alternatively, select **New** to create a row for a new language.</span></span>
1. <span data-ttu-id="db872-264">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db872-264">Select **Edit**.</span></span>
1. <span data-ttu-id="db872-265">表示されたダイアログ ボックスで、**参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db872-265">In the dialog box that appears, select **Browse**.</span></span> <span data-ttu-id="db872-266">アップロードする HTMLドキュメントを参照して選択し、**開く** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="db872-266">Browse to the HTML document that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="db872-267">**アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db872-267">Select **Upload**.</span></span>
1. <span data-ttu-id="db872-268">プレビュー ウィンドウに電子メールの HTML が表示されたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db872-268">After your email HTML appears in the preview window, select **OK**.</span></span>
1. <span data-ttu-id="db872-269">行に対して、 **本文** のチェック ボックスが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="db872-269">Make sure that the **Has body** check box is selected for the row.</span></span>

<span data-ttu-id="db872-270">Commerce 本部が電子メールを送信するように設定済みの場合は、テンプレートにマッピングされたイベントを呼び出すトランザクションを実行するすべての顧客に、新規または更新された電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="db872-270">If you've already configured Commerce headquarters to send email, your new or updated email will be sent to all customers who perform a transaction that invokes the event that is mapped to the template.</span></span>

<span data-ttu-id="db872-271">Dynamics 365 Commerce で電子メールを構成する方法の詳細については、[電子メールの構成と送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db872-271">For more information about how to configure emails in Dynamics 365 Commerce, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db872-272">追加リソース</span><span class="sxs-lookup"><span data-stu-id="db872-272">Additional resources</span></span> 

[<span data-ttu-id="db872-273">電子メール通知プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="db872-273">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="db872-274">電子メールのコンフィギュレーションと送信</span><span class="sxs-lookup"><span data-stu-id="db872-274">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[<span data-ttu-id="db872-275">電子メールのレシートを設定</span><span class="sxs-lookup"><span data-stu-id="db872-275">Set up email receipts</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[<span data-ttu-id="db872-276">Modern POS (MPOS) からの領収書メールを送信する</span><span class="sxs-lookup"><span data-stu-id="db872-276">Send email receipts from Modern POS </span></span>](email-receipts.md)
