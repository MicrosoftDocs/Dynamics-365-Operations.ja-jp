---
title: 顧客ポータルをカスタマイズして使用する
description: このトピックでは、顧客ポータルをシステムに追加した後でカスタマイズする方法について説明します。
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3ab79bc9203309c0cfa1ff18f75580297ae1001
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413984"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="0f0a5-103">顧客ポータルをカスタマイズして使用する</span><span class="sxs-lookup"><span data-stu-id="0f0a5-103">Customize and use the Customer portal</span></span>

<span data-ttu-id="0f0a5-104">このトピックでは、顧客ポータルで使用できるさまざまなページについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="0f0a5-105">ここでは、ページの機能とカスタマイズ方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="0f0a5-106">顧客 ポータルでは、既成 の Web ページとアクションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="0f0a5-107">次のサイトマップは、これら Web ページとアクションの概要と、アクションを実行できるロールを示しています。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

![![顧客ポータルのサイトマップ](media/customer-portal-site-map.png "顧客ポータルのサイトマップ")](media/customer-portal-site-map.png "Customer portal site map")

## <a name="typical-customizations"></a><span data-ttu-id="0f0a5-109">一般的なカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="0f0a5-109">Typical customizations</span></span>

<span data-ttu-id="0f0a5-110">次のトピックでは、Power Apps ポータルの基本とポータルのカスタマイズ方法について説明し ます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="0f0a5-111">[テンプレートで作業する](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) - このトピックでは、Power Apps ポータルの機能概要と、ポータルを簡単にカスタマイズする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-111">[Work with templates](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="0f0a5-112">[ポータル コンテンツの管理](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) - このトピックでは、ポータルに表示されるコンテンツの管理方法とカスタマイズする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-112">[Manage portal content](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="0f0a5-113">[編集 CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) - このトピックでは、ポータルのユーザー インターフェイス (UI) に対してさらに複雑なカスタマイズを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-113">[Edit CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="0f0a5-114">[ポータルのテーマを作成する](https://docs.microsoft.com/dynamics365/portals/create-theme) - このトピックは、ポータルの UI のテーマを作成する際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-114">[Create a theme for your portal](https://docs.microsoft.com/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="0f0a5-115">[ポータルのコンテンツを簡単に作成して公開する](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) - このトピックでは、ポータルで使用する基となるデータとエンティティの管理について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-115">[Create and expose portal content easily](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and entities that you use for your portal.</span></span>
- <span data-ttu-id="0f0a5-116">[ポータルで使用する連絡先の構成](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) - このトピックでは、ユーザー ロールの作成とカスタマイズの方法、および Power Apps ポータルにおけるセキュリティと認証機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-116">[Configure a contact for use on a portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="0f0a5-117">[ポータルでのエンティティ フォームと Web フォームのメモの構成](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) - このトピックでは、ドキュメントと追加のストレージをポータルに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-117">[Configure notes for entity forms and web forms on portals](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="0f0a5-118">[ポータル Web サイトのエラー処理 ](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) - このトピックでは、ポータルのエラーログを表示して Microsoft Azure Blob ストレージ アカウントに保管する方法について説明し ます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-118">[Error handling for portal website](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="0f0a5-119">注文作成プロセスのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="0f0a5-119">Customize the order creation process</span></span>

<span data-ttu-id="0f0a5-120">ユーザーが顧客ポータルを使用して注文を送信すると、対応する Dynamics 365 Supply Chain Management 環境に注文が自動的に同期されます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="0f0a5-121">ユーザーは外部の顧客であるため、必要な情報の一部は、意図的に非表示となっています。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="0f0a5-122">この情報は、フォームの送信時に自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="0f0a5-123">ここでは、連絡先を設定してエラーを回避する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="0f0a5-124">自動的に設定されるフィールドと、必要に応じてこれらフィールドの値を変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="0f0a5-125">既成の注文作成プロセス</span><span class="sxs-lookup"><span data-stu-id="0f0a5-125">The out-of-box order creation process</span></span>

<span data-ttu-id="0f0a5-126">ここでは、顧客ポータルから注文を送信する標準的な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="0f0a5-127">ホーム ページの**注文の作成**タイルを選択して、**注文の作成**ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="0f0a5-128">**注文情報** ページで、次のフィールドを設定します :</span><span class="sxs-lookup"><span data-stu-id="0f0a5-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="0f0a5-129">**入荷希望日** - 配送日を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="0f0a5-130">**配送先住所** - 注文の配送先の住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="0f0a5-131">**会社** - 顧客の会社名を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="0f0a5-132">このフィールドは、管理者以外のユーザーには自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="0f0a5-133">**要求番号** - 注文の要求番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="0f0a5-134">このフィールドは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-134">This field isn't required.</span></span>
    - <span data-ttu-id="0f0a5-135">**配送先の国/地域** - 品目が配送される国または地域を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="0f0a5-136">このフィールドは、管理者以外のユーザーには自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-136">This field is automatically set for non-admin users.</span></span>

    ![![注文情報のページ](media/customer-portal-order-information.png "注文情報のページ")](media/customer-portal-order-information.png "Order Information page")

1. <span data-ttu-id="0f0a5-138">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-138">Select **Next**.</span></span>
1. <span data-ttu-id="0f0a5-139">**品目**ページで、**品目の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-139">On the **Items** page, select **Add Item**.</span></span>

    ![![品目ページ](media/customer-portal-items.png "品目ページ")](media/customer-portal-items.png "Items page")

1. <span data-ttu-id="0f0a5-141">**品目情報**のダイアログ ボックスで、次のフィールドを設定します :</span><span class="sxs-lookup"><span data-stu-id="0f0a5-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="0f0a5-142">**製品名** - 注文に追加する製品を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="0f0a5-143">**数量** - 選択した製品のの数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="0f0a5-144">**単位** - 測定単位を指定します ( **個**、**kg**、**箱** など )。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="0f0a5-145">**見積正味金額** - この値は、選択された単位の品目の見積価格 × 数量で計算されます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    ![![品目情報のダイアログ ボックスの追加](media/customer-portal-item-information.png "品目情報のダイアログ ボックスの追加")](media/customer-portal-item-information.png "Item Information dialog box")

1. <span data-ttu-id="0f0a5-147">**送信** を選択して、品目を注文に追加します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="0f0a5-148">手順 4 から 6 を繰り返して、注文するすべての品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="0f0a5-149">品目の追加の完了後は、**品目** ページで **次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="0f0a5-150">**注文情報** ページに注文の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="0f0a5-151">注文内容と配送の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="0f0a5-152">すべてが正しい場合は、**送信**を選択して注文を送信します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    ![![注文情報のページ](media/customer-portal-order-submit.png "注文情報のページ")](media/customer-portal-order-submit.png "Order Information page")

### <a name="standard-data-setup"></a><span data-ttu-id="0f0a5-154">標準データの設定</span><span class="sxs-lookup"><span data-stu-id="0f0a5-154">Standard data setup</span></span>

<span data-ttu-id="0f0a5-155">円滑なユーザーエクスペリエンスを実現する目的でに、顧客ポータルでは、いくつかの必須フィールドの値が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="0f0a5-156">これらの値は、注文を送信する顧客の連絡先レコードの情報に基づいています。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="0f0a5-157">顧客ポータルを使用して注文を送信する顧客の[連絡先レコード](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) には、以下の必須フィールドに値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-157">For each [contact record](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="0f0a5-158">それ以外の場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="0f0a5-159">**会社** - 注文が属するエンティティを選択します</span><span class="sxs-lookup"><span data-stu-id="0f0a5-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="0f0a5-160">**見込み顧客** - 選択した注文に関連付けられている顧客 ID</span><span class="sxs-lookup"><span data-stu-id="0f0a5-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="0f0a5-161">**価格リスト** - 顧客のカスタム価格リスト</span><span class="sxs-lookup"><span data-stu-id="0f0a5-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="0f0a5-162">**通貨** - 価格に適用する通貨</span><span class="sxs-lookup"><span data-stu-id="0f0a5-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="0f0a5-163">**配送先の国/地域** - 品目を配送する国または地域</span><span class="sxs-lookup"><span data-stu-id="0f0a5-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="0f0a5-164">販売注文エンティティには、次のフィールドが自動的に設定されます :</span><span class="sxs-lookup"><span data-stu-id="0f0a5-164">The following fields are automatically set for the sales order entity:</span></span>

- <span data-ttu-id="0f0a5-165">**言語** - 注文の言語 (既定では、この値は連絡先レコードから取得されます)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="0f0a5-166">**配送先の国/地域** : 品目の配送先の国または地域 (既定では、この値は連絡先レコードから取得されます)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="0f0a5-167">**連絡担当者** - 注文に関する情報の問い合わせの担当ユーザー (既定では、この値は連絡先レコードから取得されます)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="0f0a5-168">**会社** - 注文が属するエンティティ (既定では、この値は連絡先レコードから取得されます)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="0f0a5-169">**見込み顧客** – 注文に関連付けられている顧客 ID (既定では、この値は連絡先レコードから取得されます)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="0f0a5-170">**請求書顧客** - 注文に関連付けられている顧客 ID (既定では、この値は連絡先レコードから取得されます)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="0f0a5-171">**販売注文の名前**- 販売注文の名前 (既定値は **販売注文**です)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="0f0a5-172">**通貨** - 注文の通貨 (既定では、この値は連絡先レコードから取得されます)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="0f0a5-173">**価格表** - 顧客向けのカスタム価格リスト (既定では、連絡先レコードから取得されます)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="0f0a5-174">**配送先住所の説明** - 販売注文の配送先住所 (既定値は **配送先住所の説明**です)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="0f0a5-175">注文作成プロセスの修正</span><span class="sxs-lookup"><span data-stu-id="0f0a5-175">Modify the order creation process</span></span>

<span data-ttu-id="0f0a5-176">基本の注文作成プロセスを変更していない場合は、顧客ポータルの外観と UI を自由に変更できます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="0f0a5-177">注文の作成プロセスを変更する場合は、いくつかの点に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="0f0a5-178">デュアル書き込みにて販売注文を作成する必要があるため、Common Data Service の販売注文エンティティでは以下のフィールドを削除しないでください :</span><span class="sxs-lookup"><span data-stu-id="0f0a5-178">Don't remove the following fields from the sales order entity in Common Data Service, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="0f0a5-179">**会社** - 注文が属するエンティティを選択します</span><span class="sxs-lookup"><span data-stu-id="0f0a5-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="0f0a5-180">**名前** - 販売注文の名前</span><span class="sxs-lookup"><span data-stu-id="0f0a5-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="0f0a5-181">**通貨** - 価格に適用する通貨</span><span class="sxs-lookup"><span data-stu-id="0f0a5-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="0f0a5-182">**価格リスト** - 顧客のカスタム価格リスト</span><span class="sxs-lookup"><span data-stu-id="0f0a5-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="0f0a5-183">**配送先の国/地域** - 品目を配送する国または地域</span><span class="sxs-lookup"><span data-stu-id="0f0a5-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="0f0a5-184">**見込み顧客** - 選択した注文に関連付けられている顧客 ID</span><span class="sxs-lookup"><span data-stu-id="0f0a5-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="0f0a5-185">**言語** - 注文で使用する言語 (通常は、潜在顧客の使用する言語です)</span><span class="sxs-lookup"><span data-stu-id="0f0a5-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="0f0a5-186">**配送先住所の説明** - 販売注文の配送先住所です</span><span class="sxs-lookup"><span data-stu-id="0f0a5-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="0f0a5-187">品目には、以下のフィールドが必須です :</span><span class="sxs-lookup"><span data-stu-id="0f0a5-187">For items, the following fields are required:</span></span>

- <span data-ttu-id="0f0a5-188">**製品** - 注文する製品</span><span class="sxs-lookup"><span data-stu-id="0f0a5-188">**Product** – The product to order</span></span>
- <span data-ttu-id="0f0a5-189">**数量** - 選択した製品のの数量</span><span class="sxs-lookup"><span data-stu-id="0f0a5-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="0f0a5-190">**単位** - 測定単位 ( **個**、**kg**、**箱** など )</span><span class="sxs-lookup"><span data-stu-id="0f0a5-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="0f0a5-191">**出荷先の国/地域** 出荷先の国または地域</span><span class="sxs-lookup"><span data-stu-id="0f0a5-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="0f0a5-192">**配送先住所の説明** - 注文の配送先住所</span><span class="sxs-lookup"><span data-stu-id="0f0a5-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="0f0a5-193">顧客 ポータルでは、これらのすべてのフィールドの値が必ず送信されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-193">You must make sure that your Customer portal somehow submits values for all these fields.</span></span>

<span data-ttu-id="0f0a5-194">ページにフィールドを追加、削除するには、[簡易作成フォームの作成または編集編集して、効率的なデータ入力を実現する](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-194">If you want to add fields to the page, or remove fields, see [Create or edit quick create forms for a streamlined data entry experience](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="0f0a5-195">フィールドの規定値とページ保存時の値の設定を変更する場合は、Power Apps ポータル ドキュメントの次の情報を参照してください :</span><span class="sxs-lookup"><span data-stu-id="0f0a5-195">If you want to change how fields are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="0f0a5-196">フィールドの事前入力</span><span class="sxs-lookup"><span data-stu-id="0f0a5-196">Prepopulate field</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="0f0a5-197">保存時に値を設定する</span><span class="sxs-lookup"><span data-stu-id="0f0a5-197">Set Value On Save</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="0f0a5-198">ホームページのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="0f0a5-198">Customize the home page</span></span>

<span data-ttu-id="0f0a5-199">顧客ポータルのすべてのコントロールには、Power Apps ポータル コントロールが実装されています。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="0f0a5-200">これらをカスタマイズするには、Power Apps ポータル ドキュメントで[ページを作成する](https://docs.microsoft.com/powerapps/maker/portals/compose-page) に記載の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-200">You can customize them by following the steps in [Compose a page](https://docs.microsoft.com/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="0f0a5-201">ホームページのタイル作成には、顧客ポータルのテンプレートに含まれるカスタム コントロールのみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

![![ホームページのタイル](media/customer-portal-home-page-tiles.png "ホームページのタイル")](media/customer-portal-home-page-tiles.png "Tiles on the home page")

<span data-ttu-id="0f0a5-203">タイルを変更するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="0f0a5-204">[ポータル管理アプリ](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal)を開きます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-204">Open the [Portal Management app](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="0f0a5-205">左のナビゲーション ウィンドウで、**ページ テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    ![![ポータル管理ナビゲーション ウィンドウ](media/customer-portal-nav.png "ポータル管理ナビゲーション ウィンドウ")](media/customer-portal-nav.png "Portal Management navigation pane")

1. <span data-ttu-id="0f0a5-207">**ホーム** という名前のページ テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="0f0a5-208">**Web テンプレート** フィールドで、**ホーム** リンクを選択して、そのページのソース コードを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    ![![Web テンプレートのフィールド](media/customer-portal-web-template.png "Web テンプレートのフィールド")](media/customer-portal-web-template.png "Web Template field")

1. <span data-ttu-id="0f0a5-210">ホーム ページのすべてのソース コードが表示され、必要に応じて変更できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0f0a5-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="0f0a5-211">リソース</span><span class="sxs-lookup"><span data-stu-id="0f0a5-211">Resources</span></span>

<span data-ttu-id="0f0a5-212">顧客ポータルを設定、カスタマイズする方法の詳細については、次のリソースを参照してください :</span><span class="sxs-lookup"><span data-stu-id="0f0a5-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="0f0a5-213">Power Apps ポータル ドキュメント</span><span class="sxs-lookup"><span data-stu-id="0f0a5-213">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="0f0a5-214">デュアル書き込みのドキュメント</span><span class="sxs-lookup"><span data-stu-id="0f0a5-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="0f0a5-215">ポータルのライフ サイクルについて</span><span class="sxs-lookup"><span data-stu-id="0f0a5-215">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="0f0a5-216">ポータルのアップグレード</span><span class="sxs-lookup"><span data-stu-id="0f0a5-216">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="0f0a5-217">ポータルの構成の移行</span><span class="sxs-lookup"><span data-stu-id="0f0a5-217">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="0f0a5-218">ソリューションのライフサイクル管理 : Dynamics 365 for Customer Engagement アプリ</span><span class="sxs-lookup"><span data-stu-id="0f0a5-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)