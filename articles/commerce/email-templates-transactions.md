---
title: トランザクション イベント用の電子メール テンプレートの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce のトランザクション イベント用の電子メール テンプレートの作成、アップロード、および構成する方法について説明します。
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
ms.openlocfilehash: 756e2a64ef4c33c347106968eb6bc79a413c3ff7
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555248"
---
# <a name="create-email-templates-for-transactional-events"></a><span data-ttu-id="cadc2-103">トランザクション イベント用の電子メール テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="cadc2-103">Create email templates for transactional events</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cadc2-104">このトピックでは、Microsoft Dynamics 365 Commerce のトランザクション イベント用の電子メール テンプレートの作成、アップロード、および構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-104">This topic describes how to create, upload, and configure email templates for transactional events in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cadc2-105">概要</span><span class="sxs-lookup"><span data-stu-id="cadc2-105">Overview</span></span>

<span data-ttu-id="cadc2-106">Dynamics 365 Commerce では、トランザクション イベントについて顧客に通知する電子メールを送信する既成のソリューションが用意されています (たとえば、注文が行われたり、注文が集配できる状態になったり、注文が出荷されたりした場合など)。</span><span class="sxs-lookup"><span data-stu-id="cadc2-106">Dynamics 365 Commerce provides an out-of-box solution for sending emails that alert customers about transactional events (for example, when an order is placed, an order is ready for pickup, or an order has been shipped).</span></span> <span data-ttu-id="cadc2-107">このトピックでは、トランザクション電子メールの送信に使用される電子メール テンプレートの作成、アップロード、構成をする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-107">This topic describes the steps for creating, uploading, and configuring the email templates that are used to send transactional emails.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="cadc2-108">電子メール テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="cadc2-108">Create an email template</span></span>

<span data-ttu-id="cadc2-109">特定のトランザクション イベントを電子メールのテンプレートにマッピングするには、事前にテンプレートを作成しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-109">Before you can map a specific transactional event to an email template, you must create the template.</span></span>

<span data-ttu-id="cadc2-110">電子メール テンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cadc2-110">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="cadc2-111">Commerce 本部で、**Retail と Commerce \> 本社の設定 \> 組織の電子メール テンプレート** または、**組織管理 \> 設定 \> 組織の電子メール テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-111">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates** or **Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="cadc2-112">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-112">Select **New**.</span></span>
1. <span data-ttu-id="cadc2-113">**全般** 配下で、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="cadc2-113">Under **General**, set the following fields:</span></span>

    - <span data-ttu-id="cadc2-114">**電子メール ID** – 電子メール ID はテンプレートに固有の ID であり、イベントにマッピングするテンプレートを選択した際に表示される値です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-114">**Email ID** – The email ID is the unique identifier for a template, and it's the value that is shown when you select a template to map to an event.</span></span>
    - <span data-ttu-id="cadc2-115">**電子メールの説明** – このオプション フィールドを使用して、テンプレートの説明を入力できます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-115">**Email description** – You can use this optional field to provide a description of the template.</span></span> <span data-ttu-id="cadc2-116">入力した値は、Commerce 本部でのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-116">The value that you enter appears only in Commerce headquarters.</span></span>
    - <span data-ttu-id="cadc2-117">**送信者名** – ここに入力した名前が、ほとんどの電子メール クライアントの [差出人] フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-117">**Sender name** – The name that you enter appears in the "from" field of most email clients.</span></span>
    - <span data-ttu-id="cadc2-118">**送信者の電子メール** – このテンプレートを使用して送信する電子メールが使用する電子メールのアドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-118">**Sender email** – Enter the email address that should be used for emails that are sent by using this template.</span></span>
    - <span data-ttu-id="cadc2-119">**既定の言語コード** – このテンプレートを呼び出すチャネルで言語が提供されていない場合、送信される電子メールのローカライズされたバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-119">**Default language code** – This field specifies the localized version of the email that is sent by default, if no language is provided by the channel that invokes this template.</span></span>

1. <span data-ttu-id="cadc2-120">**電子メール メッセージ コンテンツ** 配下で、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-120">Under **Email message content**, select **New**.</span></span>
1. <span data-ttu-id="cadc2-121">**言語** フィールドに、電子メール テンプレートの言語を入力します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-121">In the **Language** field, enter the language for the email template.</span></span> <span data-ttu-id="cadc2-122">言語とローカライズされたテンプレートは後で追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-122">You can add more languages and localized templates later.</span></span>
1. <span data-ttu-id="cadc2-123">**件名** フィールドには、電子メールの件名フィールドに表示される件名を入力します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-123">In the **Subject** field, enter the email subject that should appear in the subject field of the email.</span></span>
1. <span data-ttu-id="cadc2-124">電子メールのテンプレートをアップロードするには、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-124">Select **Edit** to upload your email template.</span></span>

## <a name="create-an-email-message-body-by-using-html"></a><span data-ttu-id="cadc2-125">HTML を使用して電子メール メッセージの本文を作成する</span><span class="sxs-lookup"><span data-stu-id="cadc2-125">Create an email message body by using HTML</span></span>

<span data-ttu-id="cadc2-126">電子メール メッセージの本文はHTMLで構成されています。</span><span class="sxs-lookup"><span data-stu-id="cadc2-126">The message body of your email is composed in HTML.</span></span> <span data-ttu-id="cadc2-127">HTML およびインライン カスケードスタイルシート (CSS) で使用できる任意のレイアウト、スタイル、ブランディングを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-127">You can use any layout, styling, and branding that HTML and inline Cascading Style Sheets (CSS) allow for.</span></span> <span data-ttu-id="cadc2-128">一般に公開されている web のエンドポイントに画像をホストする場合は、画像を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-128">You can also use images, if you host them on a publicly available web endpoint.</span></span> <span data-ttu-id="cadc2-129">画像を追加するには、HTML **&lt;img&gt;** タグの **src** 属性に画像のURLを入力します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-129">To add an image, enter the image's URL in the **src** attribute of the HTML **&lt;img&gt;** tag.</span></span>

> [!NOTE]
> <span data-ttu-id="cadc2-130">電子メール クライアントにはレイアウトやスタイルの制限があり、メッセージ本文に使用するHTMLや CSS の調整が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-130">Email clients impose layout and style limitations that might require adjustments to the HTML and CSS that you use for the message body.</span></span> <span data-ttu-id="cadc2-131">人気の高い電子メール クライアントで対応しているHTMLを作成するためのベストプラクティスについて理解しておくことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-131">We recommend that you familiarize yourself with the best practices for creating HTML that will be supported by the most popular email clients.</span></span>

## <a name="add-placeholders-to-the-email-message-body"></a><span data-ttu-id="cadc2-132">電子メール メッセージの本文にプレースホルダーを追加する</span><span class="sxs-lookup"><span data-stu-id="cadc2-132">Add placeholders to the email message body</span></span>

<span data-ttu-id="cadc2-133">電子メールにはプレースホルダーを含めることができます。これは電子メールが生成された際に顧客固有の値やトランザクション固有の値に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-133">Your email can contain placeholders that are replaced with customer-specific and transaction-specific values when the email is generated.</span></span> <span data-ttu-id="cadc2-134">プレースホルダは常にパーセント記号 (%) で囲まれており、HTML 文書の中に直接挿入されます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-134">Placeholders are always surrounded by percent signs (%) and are inserted directly into the HTML document.</span></span>

<span data-ttu-id="cadc2-135">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-135">Here is an example.</span></span>

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a><span data-ttu-id="cadc2-136">注文のプレースホルダー (販売注文レベル)</span><span class="sxs-lookup"><span data-stu-id="cadc2-136">Order placeholders (sales order level)</span></span>

<span data-ttu-id="cadc2-137">以下のプレースホルダーは、販売注文レベルで定義されたデータを取得して表示します (販売明細行レベルとは異なります)。</span><span class="sxs-lookup"><span data-stu-id="cadc2-137">The following placeholders retrieve and show data that is defined at the sales order level (as opposed to the sales line level).</span></span>

| <span data-ttu-id="cadc2-138">プレースホルダー名</span><span class="sxs-lookup"><span data-stu-id="cadc2-138">Placeholder name</span></span>     | <span data-ttu-id="cadc2-139">プレースホルダー値</span><span class="sxs-lookup"><span data-stu-id="cadc2-139">Placeholder value</span></span>                                            |
| -------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="cadc2-140">customername</span><span class="sxs-lookup"><span data-stu-id="cadc2-140">customername</span></span>         | <span data-ttu-id="cadc2-141">注文を行った顧客の名称です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-141">The name of the customer who placed the order.</span></span>               |
| <span data-ttu-id="cadc2-142">salesid</span><span class="sxs-lookup"><span data-stu-id="cadc2-142">salesid</span></span>              | <span data-ttu-id="cadc2-143">注文の販売 ID です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-143">The sales ID of the order.</span></span>                                   |
| <span data-ttu-id="cadc2-144">deliveryaddress</span><span class="sxs-lookup"><span data-stu-id="cadc2-144">deliveryaddress</span></span>      | <span data-ttu-id="cadc2-145">出荷注文の配送先住所です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-145">The delivery address for shipped orders.</span></span>                     |
| <span data-ttu-id="cadc2-146">customeraddress</span><span class="sxs-lookup"><span data-stu-id="cadc2-146">customeraddress</span></span>      | <span data-ttu-id="cadc2-147">顧客の住所です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-147">The address of the customer.</span></span>                                 |
| <span data-ttu-id="cadc2-148">customeremailaddress</span><span class="sxs-lookup"><span data-stu-id="cadc2-148">customeremailaddress</span></span> | <span data-ttu-id="cadc2-149">顧客がチェックアウト時に入力した電子メール アドレスです。</span><span class="sxs-lookup"><span data-stu-id="cadc2-149">The email address that the customer entered at checkout.</span></span>     |
| <span data-ttu-id="cadc2-150">deliverydate</span><span class="sxs-lookup"><span data-stu-id="cadc2-150">deliverydate</span></span>         | <span data-ttu-id="cadc2-151">配送日です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-151">The delivery date.</span></span>                                           |
| <span data-ttu-id="cadc2-152">shipdate</span><span class="sxs-lookup"><span data-stu-id="cadc2-152">shipdate</span></span>             | <span data-ttu-id="cadc2-153">出荷日です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-153">The ship date.</span></span>                                               |
| <span data-ttu-id="cadc2-154">modeofdelivery</span><span class="sxs-lookup"><span data-stu-id="cadc2-154">modeofdelivery</span></span>       | <span data-ttu-id="cadc2-155">注文の出荷モードです。</span><span class="sxs-lookup"><span data-stu-id="cadc2-155">The delivery mode of the order.</span></span>                              |
| <span data-ttu-id="cadc2-156">請求</span><span class="sxs-lookup"><span data-stu-id="cadc2-156">charges</span></span>              | <span data-ttu-id="cadc2-157">注文に対する金額の合計です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-157">The total charges for the order.</span></span>                             |
| <span data-ttu-id="cadc2-158">税</span><span class="sxs-lookup"><span data-stu-id="cadc2-158">tax</span></span>                  | <span data-ttu-id="cadc2-159">注文の税の合計です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-159">The total tax for the order.</span></span>                                 |
| <span data-ttu-id="cadc2-160">合計</span><span class="sxs-lookup"><span data-stu-id="cadc2-160">total</span></span>                | <span data-ttu-id="cadc2-161">注文に対する金額の総計です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-161">The total amount for the order.</span></span>                              |
| <span data-ttu-id="cadc2-162">ordernetamount</span><span class="sxs-lookup"><span data-stu-id="cadc2-162">ordernetamount</span></span>       | <span data-ttu-id="cadc2-163">注文の合計金額から税の合計を差し引いた金額です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-163">The total amount for the order, minus the total tax.</span></span>         |
| <span data-ttu-id="cadc2-164">割引</span><span class="sxs-lookup"><span data-stu-id="cadc2-164">discount</span></span>             | <span data-ttu-id="cadc2-165">注文に対する割引の合計です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-165">The total discount for the order.</span></span>                            |
| <span data-ttu-id="cadc2-166">storename</span><span class="sxs-lookup"><span data-stu-id="cadc2-166">storename</span></span>            | <span data-ttu-id="cadc2-167">注文を行った店舗の名称です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-167">The name of the store where the order was placed.</span></span>            |
| <span data-ttu-id="cadc2-168">storeaddress</span><span class="sxs-lookup"><span data-stu-id="cadc2-168">storeaddress</span></span>         | <span data-ttu-id="cadc2-169">注文を行った顧客の住所です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-169">The address of the store that placed the order.</span></span>              |
| <span data-ttu-id="cadc2-170">storeopenfrom</span><span class="sxs-lookup"><span data-stu-id="cadc2-170">storeopenfrom</span></span>        | <span data-ttu-id="cadc2-171">注文を行った店舗の開店時間です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-171">The opening time of the store that placed the order.</span></span>         |
| <span data-ttu-id="cadc2-172">storeopento</span><span class="sxs-lookup"><span data-stu-id="cadc2-172">storeopento</span></span>          | <span data-ttu-id="cadc2-173">注文を行った店舗の閉店時間です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-173">The closing time of the store that placed the order.</span></span>         |
| <span data-ttu-id="cadc2-174">pickupstorename</span><span class="sxs-lookup"><span data-stu-id="cadc2-174">pickupstorename</span></span>      | <span data-ttu-id="cadc2-175">注文が受け取られる店舗の名称です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-175">The name of the store where the order will be picked up.</span></span>     |
| <span data-ttu-id="cadc2-176">pickupstoreaddress</span><span class="sxs-lookup"><span data-stu-id="cadc2-176">pickupstoreaddress</span></span>   | <span data-ttu-id="cadc2-177">注文がピッキングされる店舗の住所です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-177">The address of the store where the order will be picked up.</span></span>  |
| <span data-ttu-id="cadc2-178">pickupopenstorefrom</span><span class="sxs-lookup"><span data-stu-id="cadc2-178">pickupopenstorefrom</span></span>  | <span data-ttu-id="cadc2-179">注文がピッキングされる店舗の開店時間です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-179">The opening time of the store where the order will be picked up.</span></span> |
| <span data-ttu-id="cadc2-180">pickupopenstoreto</span><span class="sxs-lookup"><span data-stu-id="cadc2-180">pickupopenstoreto</span></span>    | <span data-ttu-id="cadc2-181">注文がピッキングされる店舗の閉店時間です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-181">The closing time of the store where the order will be picked up.</span></span> |

### <a name="order-line-placeholders-sales-line-level"></a><span data-ttu-id="cadc2-182">注文ラインのプレースホルダー (販売ライン レベル)</span><span class="sxs-lookup"><span data-stu-id="cadc2-182">Order line placeholders (sales line level)</span></span>

<span data-ttu-id="cadc2-183">以下のプレースホルダーは、販売注文の個々の製品 (明細行) のデータを取得して表示します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-183">The following placeholders retrieve and show data for individual products (lines) in the sales order.</span></span>

| <span data-ttu-id="cadc2-184">プレースホルダー名</span><span class="sxs-lookup"><span data-stu-id="cadc2-184">Placeholder name</span></span>               | <span data-ttu-id="cadc2-185">プレースホルダー値</span><span class="sxs-lookup"><span data-stu-id="cadc2-185">Placeholder value</span></span> |
|--------------------------------|-------------------|
| <span data-ttu-id="cadc2-186">productid</span><span class="sxs-lookup"><span data-stu-id="cadc2-186">productid</span></span>                      | <span data-ttu-id="cadc2-187">明細行の製品 ID です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-187">The product ID for the line.</span></span> |
| <span data-ttu-id="cadc2-188">lineproductname</span><span class="sxs-lookup"><span data-stu-id="cadc2-188">lineproductname</span></span>                | <span data-ttu-id="cadc2-189">生産の名前。</span><span class="sxs-lookup"><span data-stu-id="cadc2-189">The name of the product.</span></span> |
| <span data-ttu-id="cadc2-190">lineproductdescription</span><span class="sxs-lookup"><span data-stu-id="cadc2-190">lineproductdescription</span></span>         | <span data-ttu-id="cadc2-191">製品の説明。</span><span class="sxs-lookup"><span data-stu-id="cadc2-191">The description of the product.</span></span> |
| <span data-ttu-id="cadc2-192">linequantity</span><span class="sxs-lookup"><span data-stu-id="cadc2-192">linequantity</span></span>                   | <span data-ttu-id="cadc2-193">ラインに発注された単位数と測定単位 (**ea**、**pair** など) です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-193">The number of units that were ordered for the line, plus the unit of measure (for example, **ea**, or **pair**).</span></span> |
| <span data-ttu-id="cadc2-194">lineunit</span><span class="sxs-lookup"><span data-stu-id="cadc2-194">lineunit</span></span>                       | <span data-ttu-id="cadc2-195">ラインの測定単位です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-195">The unit of measure for the line.</span></span> |
| <span data-ttu-id="cadc2-196">linequantity_withoutunit</span><span class="sxs-lookup"><span data-stu-id="cadc2-196">linequantity_withoutunit</span></span>       | <span data-ttu-id="cadc2-197">ラインに発注された単位数で、測定単位を含まないもの。</span><span class="sxs-lookup"><span data-stu-id="cadc2-197">The number of units that were ordered for the line, without the unit of measure.</span></span> |
| <span data-ttu-id="cadc2-198">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="cadc2-198">linequantitypicked</span></span>             | <span data-ttu-id="cadc2-199">注文の **PickOrder** イベントが使用された場合の、ピッキングされた単位の数です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-199">When the **PickOrder** event is used, the number of units that were picked.</span></span> <span data-ttu-id="cadc2-200">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-200">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="cadc2-201">linequantitypicked_withoutunit</span><span class="sxs-lookup"><span data-stu-id="cadc2-201">linequantitypicked_withoutunit</span></span> | <span data-ttu-id="cadc2-202">**PickOrder** イベントが使用された場合の、測定単位を含まない、ピッキングされた単位の数です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-202">When the **PickOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="cadc2-203">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-203">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="cadc2-204">linequantitypacked</span><span class="sxs-lookup"><span data-stu-id="cadc2-204">linequantitypacked</span></span>             | <span data-ttu-id="cadc2-205">**PackOrder** および **ピックアップ可能な注文** イベントが使用された場合の、梱包された単位数です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-205">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed.</span></span> <span data-ttu-id="cadc2-206">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-206">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="cadc2-207">linequantitypacked_withoutuom</span><span class="sxs-lookup"><span data-stu-id="cadc2-207">linequantitypacked_withoutuom</span></span>  | <span data-ttu-id="cadc2-208">**PackOrder** および **ピックアップ可能な注文** イベントが使用された場合の、測定単位を含まない、梱包された単位数です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-208">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed, without the unit of measure.</span></span> <span data-ttu-id="cadc2-209">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-209">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="cadc2-210">linequantityshipped</span><span class="sxs-lookup"><span data-stu-id="cadc2-210">linequantityshipped</span></span>            | <span data-ttu-id="cadc2-211">以下に説明するように、特定のイベントが使用されている場合を除き、常に **0** となります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-211">Always **0**, except when specific events are used, as described in the next row.</span></span> |
| <span data-ttu-id="cadc2-212">linequantityshipped_withoutuom</span><span class="sxs-lookup"><span data-stu-id="cadc2-212">linequantityshipped_withoutuom</span></span> | <span data-ttu-id="cadc2-213">**ShipOrder** イベントが使用された場合の、測定単位を含まない、ピッキングされた単位の数です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-213">When the **ShipOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="cadc2-214">これに該当しない場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-214">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="cadc2-215">lineprice</span><span class="sxs-lookup"><span data-stu-id="cadc2-215">lineprice</span></span>                      | <span data-ttu-id="cadc2-216">一単位の価格です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-216">The price of a single unit.</span></span> |
| <span data-ttu-id="cadc2-217">linenetamount</span><span class="sxs-lookup"><span data-stu-id="cadc2-217">linenetamount</span></span>                  | <span data-ttu-id="cadc2-218">単位および適用後のラインの価格です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-218">The price of the line after the number of units and discount are applied.</span></span> |
| <span data-ttu-id="cadc2-219">linediscount</span><span class="sxs-lookup"><span data-stu-id="cadc2-219">linediscount</span></span>                   | <span data-ttu-id="cadc2-220">個々の単位の割引です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-220">The discount for an individual unit.</span></span> |
| <span data-ttu-id="cadc2-221">lineshipdate</span><span class="sxs-lookup"><span data-stu-id="cadc2-221">lineshipdate</span></span>                   | <span data-ttu-id="cadc2-222">当該ラインの出荷日です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-222">The ship date for the line.</span></span> |
| <span data-ttu-id="cadc2-223">linedeliverydate</span><span class="sxs-lookup"><span data-stu-id="cadc2-223">linedeliverydate</span></span>               | <span data-ttu-id="cadc2-224">当該ラインの配達日です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-224">The delivery date for the line.</span></span> |
| <span data-ttu-id="cadc2-225">linedeliverymode</span><span class="sxs-lookup"><span data-stu-id="cadc2-225">linedeliverymode</span></span>               | <span data-ttu-id="cadc2-226">当該ラインの配送モードです。</span><span class="sxs-lookup"><span data-stu-id="cadc2-226">The delivery mode for the line.</span></span> |
| <span data-ttu-id="cadc2-227">linedeliveryaddress</span><span class="sxs-lookup"><span data-stu-id="cadc2-227">linedeliveryaddress</span></span>            | <span data-ttu-id="cadc2-228">当該ラインの配達先住所です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-228">The delivery address for the line.</span></span> |
| <span data-ttu-id="cadc2-229">giftcardnumber</span><span class="sxs-lookup"><span data-stu-id="cadc2-229">giftcardnumber</span></span>                 | <span data-ttu-id="cadc2-230">ギフト カード タイプの製品の場合の、ギフトカード番号です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-230">The gift card number, for products of the gift card type.</span></span> |
| <span data-ttu-id="cadc2-231">giftcardbalance</span><span class="sxs-lookup"><span data-stu-id="cadc2-231">giftcardbalance</span></span>                | <span data-ttu-id="cadc2-232">ギフト カード タイプの製品の場合の、ギフトカード残高です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-232">The gift card balance, for products of the gift card type.</span></span> |
| <span data-ttu-id="cadc2-233">giftcardmessage</span><span class="sxs-lookup"><span data-stu-id="cadc2-233">giftcardmessage</span></span>                | <span data-ttu-id="cadc2-234">ギフト カード タイプの製品の場合の、ギフトカードのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="cadc2-234">The gift card message, for products of the gift card type.</span></span> |
| <span data-ttu-id="cadc2-235">giftcardpin</span><span class="sxs-lookup"><span data-stu-id="cadc2-235">giftcardpin</span></span>                    | <span data-ttu-id="cadc2-236">ギフト カード タイプの製品の場合の、ギフトカードの識別番号 (PIN) です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-236">The personal identification number (PIN) of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="cadc2-237">(このプレースホルダーは、外部のギフトカードに固有のものです)</span><span class="sxs-lookup"><span data-stu-id="cadc2-237">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="cadc2-238">giftcardexpiration</span><span class="sxs-lookup"><span data-stu-id="cadc2-238">giftcardexpiration</span></span>             | <span data-ttu-id="cadc2-239">ギフト カード タイプの製品の場合の、ギフトカードの有効期限です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-239">The expiration date of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="cadc2-240">(このプレースホルダーは、外部のギフトカードに固有のものです)</span><span class="sxs-lookup"><span data-stu-id="cadc2-240">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="cadc2-241">giftcardrecipientname</span><span class="sxs-lookup"><span data-stu-id="cadc2-241">giftcardrecipientname</span></span>          | <span data-ttu-id="cadc2-242">ギフト カード タイプの製品の場合の、ギフトカードの受取人の名前です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-242">The name of the gift card recipient, for products of the gift card type.</span></span> |
| <span data-ttu-id="cadc2-243">giftcardbuyername</span><span class="sxs-lookup"><span data-stu-id="cadc2-243">giftcardbuyername</span></span>              | <span data-ttu-id="cadc2-244">ギフト カード タイプの製品の場合の、ギフトカードの購入者の名前です。</span><span class="sxs-lookup"><span data-stu-id="cadc2-244">The name of the gift card buyer, for products of the gift card type.</span></span> |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a><span data-ttu-id="cadc2-245">電子メール メッセージ本文における注文明細行のプレースホルダーの形式</span><span class="sxs-lookup"><span data-stu-id="cadc2-245">Format of order line placeholders in the email message body</span></span>

<span data-ttu-id="cadc2-246">電子メールのメッセージ本文内の個々の注文明細行の HTML を作成する際には、HTML の繰り返しブロックとその行のプレースホルダーを、HTML のコメントタグの中に入れた以下のプレースホルダーで囲みます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-246">When you create the HTML for the individual order lines in the email message body, surround the repeating block of HTML and placeholders for the lines with the following placeholders that are put inside HTML comment tags.</span></span>

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

<span data-ttu-id="cadc2-247">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-247">Here is an example.</span></span>

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

## <a name="create-a-template-for-emailed-receipts"></a><span data-ttu-id="cadc2-248">メールで送信される領収書のテンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="cadc2-248">Create a template for emailed receipts</span></span>

<span data-ttu-id="cadc2-249">領収書は、販売時点管理 (POS) で購入した顧客に電子メールで送信することができます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-249">Receipts can be emailed to customers who make purchases at a retail point of sale (POS).</span></span> <span data-ttu-id="cadc2-250">一般的には、メールで送信する領収書のテンプレートの作成手順は、その他のトランザクション イベントのテンプレートの作成手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="cadc2-250">In general, the steps for creating the emailed receipt template are the same as the steps for creating templates for other transactional events.</span></span> <span data-ttu-id="cadc2-251">この場合、以下の変更が必要となります:</span><span class="sxs-lookup"><span data-stu-id="cadc2-251">However, the following changes are required:</span></span>

- <span data-ttu-id="cadc2-252">領収書のテキストは、**%message%** のプレースホルダーを使用して電子メールに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-252">The text of the receipt is inserted into the email by using the **%message%** placeholder.</span></span> <span data-ttu-id="cadc2-253">領収書の本文が正しく表示されるように、**%message%** プレースホルダーを HTML タグの **&lt;pre&gt;** および **&lt;/pre&gt;** で囲みます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-253">To ensure that the receipt body is correctly rendered, surround the **%message%** placeholder with HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tags.</span></span>
- <span data-ttu-id="cadc2-254">**%receiptid%** プレースホルダーは、領収書の ID を表す QRコードまたはバーコードを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-254">The **%receiptid%** placeholder can be used to show a QR code or bar code that represents the receipt ID.</span></span> <span data-ttu-id="cadc2-255">(QRコードおよびバーコードはサード パーティ サービスによって動的に生成および提供されます。) 電子メールで送信する領収書の QRコードまたはバーコードを表示する方法については、[QRコードまたはバーコードをトランザクションおよび領収書の電子メールに追加する](add-qr-code-barcode-email.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cadc2-255">(QR codes and bar codes are dynamically generated and served by a third-party service.) For more information about how to show a QR code or bar code in an emailed receipt, see [Add a QR code or bar code to transactional and receipt emails](add-qr-code-barcode-email.md).</span></span>

## <a name="upload-the-email-html"></a><span data-ttu-id="cadc2-256">電子メールの HTML をアップロードする</span><span class="sxs-lookup"><span data-stu-id="cadc2-256">Upload the email HTML</span></span>

<span data-ttu-id="cadc2-257">HTML を作成し、テストした後は、メッセージの本文を Commerce 本部にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-257">After you've created and tested the HTML for your message body, it must be uploaded to Commerce headquarters.</span></span> <span data-ttu-id="cadc2-258">現時点では、電子メールの HTML はエクスポートできません。</span><span class="sxs-lookup"><span data-stu-id="cadc2-258">Currently, email HTML can't be exported.</span></span> <span data-ttu-id="cadc2-259">そのため、HTML のマスターコピーは Commerce 本部以外で管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cadc2-259">Therefore, you must maintain the master copy of your HTML outside Commerce headquarters.</span></span>

<span data-ttu-id="cadc2-260">新規、または編集した電子メールのテンプレート HTML をアップロードするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cadc2-260">To upload a new or edited email template HTML, follow these steps.</span></span>

1. <span data-ttu-id="cadc2-261">Commerce 本部で、**小売りとコマース \> 本部の設定 \> 組織の電子メールのテンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-261">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="cadc2-262">HTML を追加または置換する言語の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-262">Select the row for the language that you want to add or replace HTML for.</span></span> <span data-ttu-id="cadc2-263">または、**新規** を選択して新しい言語の行を作成します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-263">Alternatively, select **New** to create a row for a new language.</span></span>
1. <span data-ttu-id="cadc2-264">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-264">Select **Edit**.</span></span>
1. <span data-ttu-id="cadc2-265">表示されたダイアログ ボックスで、**参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-265">In the dialog box that appears, select **Browse**.</span></span> <span data-ttu-id="cadc2-266">アップロードする HTMLドキュメントを参照して選択し、**開く** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-266">Browse to the HTML document that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="cadc2-267">**アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-267">Select **Upload**.</span></span>
1. <span data-ttu-id="cadc2-268">プレビュー ウィンドウに電子メールの HTML が表示されたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-268">After your email HTML appears in the preview window, select **OK**.</span></span>
1. <span data-ttu-id="cadc2-269">行に対して、 **本文** のチェック ボックスが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cadc2-269">Make sure that the **Has body** check box is selected for the row.</span></span>

<span data-ttu-id="cadc2-270">Commerce 本部が電子メールを送信するように設定済みの場合は、テンプレートにマッピングされたイベントを呼び出すトランザクションを実行するすべての顧客に、新規または更新された電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="cadc2-270">If you've already configured Commerce headquarters to send email, your new or updated email will be sent to all customers who perform a transaction that invokes the event that is mapped to the template.</span></span>

<span data-ttu-id="cadc2-271">Dynamics 365 Commerce で電子メールを構成する方法の詳細については、[電子メールの構成と送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cadc2-271">For more information about how to configure emails in Dynamics 365 Commerce, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cadc2-272">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cadc2-272">Additional resources</span></span> 

[<span data-ttu-id="cadc2-273">電子メール通知プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="cadc2-273">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="cadc2-274">電子メールのコンフィギュレーションと送信</span><span class="sxs-lookup"><span data-stu-id="cadc2-274">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[<span data-ttu-id="cadc2-275">電子メールのレシートを設定</span><span class="sxs-lookup"><span data-stu-id="cadc2-275">Set up email receipts</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[<span data-ttu-id="cadc2-276">Modern POS (MPOS) からの領収書メールを送信する</span><span class="sxs-lookup"><span data-stu-id="cadc2-276">Send email receipts from Modern POS </span></span>](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
