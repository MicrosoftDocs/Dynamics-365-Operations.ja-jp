---
title: 販売時点管理 (POS) での顧客チェックイン通知を有効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) で顧客チェックイン通知を有効にする方法について説明します。
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937597"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="b1269-103">販売時点管理 (POS) での顧客チェックイン通知を有効にする</span><span class="sxs-lookup"><span data-stu-id="b1269-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b1269-104">このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) で顧客チェックイン通知を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1269-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="b1269-105">"ピックアップ可能な注文" のメールには、顧客が店内にいて荷物が運ばれてくるのを待っていることを店舗に通知するリンクやボタンを設けることができます。</span><span class="sxs-lookup"><span data-stu-id="b1269-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="b1269-106">顧客はチェックイン確認を受け取り、店舗は POS アプリケーションでタスクとして通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="b1269-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="b1269-107">このタスクは、販売担当者が顧客の車両に注文を届けるためのプロンプトとして機能します。</span><span class="sxs-lookup"><span data-stu-id="b1269-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="b1269-108">したがって、顧客は店舗に入る必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b1269-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="b1269-109">顧客のチェックイン ワークフローは、駐車場の番号、車両のメーカー、モデル、色、配送手順など、顧客から追加情報を収集するように構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="b1269-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="b1269-110">小売用店舗のスタッフは、この情報を利用して注文のフルフィルメントを円滑化することができます。</span><span class="sxs-lookup"><span data-stu-id="b1269-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="b1269-111">顧客チェックインを有効にする</span><span class="sxs-lookup"><span data-stu-id="b1269-111">Enable customer check-in</span></span>

<span data-ttu-id="b1269-112">顧客チェックイン機能を有効にすると、Commerce によって注文確認 ID (チャネル参照 ID とも呼ばれます) が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b1269-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="b1269-113">また、販売時点管理 (POS) またはコール センター チャネルを通じて作成された注文の注文確認 ID も生成されます。</span><span class="sxs-lookup"><span data-stu-id="b1269-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="b1269-114">Commerce 本部の顧客チェックイン機能をオンにするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b1269-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b1269-115">**ワークスペース \> 機能管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b1269-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="b1269-116">**チャネル全体で一貫したチャネル参照 ID フォーマットを生成する** 機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="b1269-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="b1269-117">機能を選択し、プロパティ ウィンドウで **今すぐ有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1269-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="b1269-118">チェックイン確認ページの作成</span><span class="sxs-lookup"><span data-stu-id="b1269-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="b1269-119">eコマース サイトで、チェックイン確認エクスペリエンスとして機能する新しいページを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1269-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="b1269-120">このページには、追加の構成を使用して、顧客からの追加情報を収集して注文のフルフィルメントを容易にするフォームを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="b1269-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="b1269-121">ページおよびモジュールの設定方法については、[顧客チェックイン モジュール](check-in-pickup-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1269-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="b1269-122">トランザクション メール テンプレートの構成</span><span class="sxs-lookup"><span data-stu-id="b1269-122">Configure the transactional email template</span></span>

<span data-ttu-id="b1269-123">注文した商品がピックアップ可能になったときに顧客が受け取るトランザクション メールのテンプレートに、**I am here** のリンクまたはボタンを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1269-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="b1269-124">顧客はこのリンクまたはボタンを使用して、注文をピックアップするために到着したことを店舗に通知します。</span><span class="sxs-lookup"><span data-stu-id="b1269-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="b1269-125">通知タイプの **梱包完了済** と、カーブサイド注文のフルフィルメントに使用している配送モードにマッピングされたテンプレートに、リンクまたはボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="b1269-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="b1269-126">テンプレートで、作成したチェックイン確認ページの URL を指す HTML リンクまたはボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="b1269-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="b1269-127">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b1269-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="b1269-128">メール テンプレートの構成方法の詳細については、「[配送モードによるトランザクション メールのカスタマイズ](customize-email-delivery-mode.md)」を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="b1269-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="b1269-129">POS でチェックイン確認タスクが作成される</span><span class="sxs-lookup"><span data-stu-id="b1269-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="b1269-130">顧客が店舗にピックアップのために到着したことを通知すると、チェックイン確認通知が表示され、顧客が注文をピックアップする店舗の POS のタスク リストにタスクが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b1269-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="b1269-131">このタスクには、注文のフルフィルメントを行うために必要なすべての顧客および注文情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1269-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="b1269-132">このタスクでは、指示フィールドには、追加の情報フォームを使用して顧客から収集された情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b1269-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="b1269-133">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b1269-133">Additional resources</span></span>

[<span data-ttu-id="b1269-134">ピックアップのチェックイン モジュール</span><span class="sxs-lookup"><span data-stu-id="b1269-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
