---
title: "コール センターのカタログ作成"
description: "この記事は、コール センターのカタログを作成するプロセスの概要を提供します。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: bec83606ec6482cba7231356910312c10e20cca2
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="create-a-call-center-catalog"></a><span data-ttu-id="0af00-103">コール センターのカタログ作成</span><span class="sxs-lookup"><span data-stu-id="0af00-103">Create a call center catalog</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="0af00-104">この記事は、コール センターのカタログを作成するプロセスの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="0af00-104">This article provides an overview of the process for creating a catalog for a call center.</span></span> 

<span data-ttu-id="0af00-105">コール センターで、顧客に提供する製品を識別するために小売製品カタログを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="0af00-106">コール センターは、通常、印刷したカタログを使用します。</span><span class="sxs-lookup"><span data-stu-id="0af00-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="0af00-107">印刷したカタログのデザインと生産は、Microsoft Dynamics 365 for Retail の範囲外で処理されます。</span><span class="sxs-lookup"><span data-stu-id="0af00-107">The design and production of a printed catalog is handled outside Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="0af00-108">ただし、オンライン小売カタログの設定で使用するのと同じフォームを使用して、カタログのデジタル フォームを作成および格納できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-108">However, you can create and store a digital form of a catalog by using the same forms that you use to set up online retail catalogs.</span></span> <span data-ttu-id="0af00-109">カタログを作成する前に、製品の品揃えを設定し、コール センターにその品揃えを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af00-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="0af00-110">これらの品揃えから製品を選択して、カタログに製品を追加します。</span><span class="sxs-lookup"><span data-stu-id="0af00-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="0af00-111">製品がカタログに追加され、カタログが完成したら、カタログを検証してデータを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af00-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="0af00-112">それから、確認および承認のためにカタログを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af00-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="0af00-113">カタログが承認されたら、公開できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="0af00-114">コール センターのカタログが作成されたら、カタログが発行される時にカタログ データのスナップショットを取ることができます。</span><span class="sxs-lookup"><span data-stu-id="0af00-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time when the catalog is published.</span></span> <span data-ttu-id="0af00-115">このスナップショットの機能により、カタログが後で変更および更新されても、カタログの特定のバージョンにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="0af00-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="0af00-116">コール センターのカタログは、次のオプション機能を含めるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-116">Call center catalogs can also be set up to include the following optional features.</span></span>

-   <span data-ttu-id="0af00-117">**ソース コード** – 特定のカタログ メーリングへの顧客の応答を追跡するのに使用するコード。</span><span class="sxs-lookup"><span data-stu-id="0af00-117">**Source codes** – Codes that are used to track the customer response to particular catalog mailings.</span></span>
-   <span data-ttu-id="0af00-118">**無料製品** – 追加料金なしで顧客の注文に含まれる製品。</span><span class="sxs-lookup"><span data-stu-id="0af00-118">**Free products** – Products that are included in a customer's order at no additional charge.</span></span> <span data-ttu-id="0af00-119">これらの製品は、カタログのソース コードが注文に入力されると自動的に注文に追加されます。</span><span class="sxs-lookup"><span data-stu-id="0af00-119">These products are automatically added to the order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="0af00-120">**スクリプト** – 販売注文が作成されるときにコール センターの作業者が顧客に読むテキスト。</span><span class="sxs-lookup"><span data-stu-id="0af00-120">**Scripts** – Texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="0af00-121">スクリプトには、あいさつまたは購買提案を含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="0af00-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="0af00-122">**クロス セリングまたはアップ セリングの品目** - 特定の製品が注文に追加されるときに提案として表示します。</span><span class="sxs-lookup"><span data-stu-id="0af00-122">**Upsell or cross-sell items** - Items that are displayed as a suggestion when a specific product is added to the order.</span></span>

<span data-ttu-id="0af00-123">これらのオプションは、カタログの承認前および公開前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af00-123">These options must be set up before the catalog is approved and published.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0af00-124">必要条件</span><span class="sxs-lookup"><span data-stu-id="0af00-124">Prerequisites</span></span>
<span data-ttu-id="0af00-125">始める前に、次の設定手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af00-125">The following tasks must be completed before you start:</span></span>

-   <span data-ttu-id="0af00-126">製品および製品の品揃えを設定します。</span><span class="sxs-lookup"><span data-stu-id="0af00-126">Set up products and product assortments.</span></span>
-   <span data-ttu-id="0af00-127">小売製品を設定します。</span><span class="sxs-lookup"><span data-stu-id="0af00-127">Set up retail products.</span></span>
-   <span data-ttu-id="0af00-128">品揃えを設定します。</span><span class="sxs-lookup"><span data-stu-id="0af00-128">Set up an assortment.</span></span>
-   <span data-ttu-id="0af00-129">コール センターを作成します。</span><span class="sxs-lookup"><span data-stu-id="0af00-129">Create a call center.</span></span>
-   <span data-ttu-id="0af00-130">コール センターを設定します。</span><span class="sxs-lookup"><span data-stu-id="0af00-130">Set up a call center.</span></span>
-   <span data-ttu-id="0af00-131">組織階層にコール センターを追加します。</span><span class="sxs-lookup"><span data-stu-id="0af00-131">Add the call center to an organization hierarchy.</span></span>
-   <span data-ttu-id="0af00-132">組織階層を作成または変更します。</span><span class="sxs-lookup"><span data-stu-id="0af00-132">Create or modify an organization hierarchy.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="0af00-133">カタログの作成</span><span class="sxs-lookup"><span data-stu-id="0af00-133">Create a catalog</span></span>
<span data-ttu-id="0af00-134">まずカタログを作成し、カタログに製品を追加し、製品の属性を確認し、更新します。</span><span class="sxs-lookup"><span data-stu-id="0af00-134">You must first create a catalog, add products to the catalog, and then review and update the attributes for the products.</span></span>

## <a name="validate-the-catalog"></a><span data-ttu-id="0af00-135">カタログの検証</span><span class="sxs-lookup"><span data-stu-id="0af00-135">Validate the catalog</span></span>
<span data-ttu-id="0af00-136">カタログを設定したら、検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af00-136">After you've finished setting up the catalog, you must validate it.</span></span> <span data-ttu-id="0af00-137">検証プロセスでは、チャンネル属性および製品属性に必要なデータがすべてそろっており、有効であり、カタログを公開できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0af00-137">The validation process verifies that the data that is required for channel attributes and product attributes is complete and valid, and that the catalog can be published.</span></span>

## <a name="submit-the-catalog-for-review-and-approval"></a><span data-ttu-id="0af00-138">レビューと承認のためにカタログを送信</span><span class="sxs-lookup"><span data-stu-id="0af00-138">Submit the catalog for review and approval</span></span>
<span data-ttu-id="0af00-139">カタログが検証されたら、確認および承認のためにカタログを送信できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-139">After a catalog is validated, you can submit the catalog for review and approval.</span></span> <span data-ttu-id="0af00-140">カタログは、公開する前に承認される必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af00-140">A catalog must be approved before it can be published.</span></span> <span data-ttu-id="0af00-141">カタログが自動的に承認されるか、またはカタログが手動承認を要求するようにワークフローをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="0af00-141">You can configure a workflow so that catalogs either are automatically approved or require manual approval.</span></span>

## <a name="optional-add-source-codes-free-products-and-scripts"></a><span data-ttu-id="0af00-142">オプション: ソース コード、無料製品およびスクリプトを追加する</span><span class="sxs-lookup"><span data-stu-id="0af00-142">Optional: Add source codes, free products, and scripts</span></span>
<span data-ttu-id="0af00-143">また、コール センターのカタログに次の項目を追加できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-143">You can also add the following items to a call center catalog.</span></span> <span data-ttu-id="0af00-144">これらの項目はオプションです。</span><span class="sxs-lookup"><span data-stu-id="0af00-144">These items are optional.</span></span>

-   <span data-ttu-id="0af00-145">印刷カタログを提供する会社は、**ソース コード**を使用して、個々のカタログに対する顧客の応答を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-145">**Source codes** can be used by companies that provide printed catalogs to track the customer response to particular catalogs.</span></span> <span data-ttu-id="0af00-146">ソース コードは、多くの場合、カタログの裏面に印刷され、顧客が購買を行うときに販売注文に入力されます。</span><span class="sxs-lookup"><span data-stu-id="0af00-146">Source codes are often printed on the back of a catalog and are entered into the sales order when a customer makes a purchase.</span></span> <span data-ttu-id="0af00-147">カタログにソース コードを追加するには、最初にターゲット マーケットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af00-147">To add a source code to the catalog, you must first create a target market.</span></span> <span data-ttu-id="0af00-148">ターゲット マーケットは通常、所有または借用しているメーリング リストにマップされています。</span><span class="sxs-lookup"><span data-stu-id="0af00-148">The target market is usually mapped to an owned or rented mailing list.</span></span>
-   <span data-ttu-id="0af00-149">**無料製品**は、顧客がカタログを参照して注文をするときに無料で含まれる促進品目です。</span><span class="sxs-lookup"><span data-stu-id="0af00-149">**Free products** are promotional items that are included free of charge with the customer's order when the catalog is referenced.</span></span>
-   <span data-ttu-id="0af00-150">**スクリプト**は、カタログ内のカタログまたは製品のコンテキストで、作業者から顧客への働きかけを補助するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-150">**Scripts** can be used to guide the worker's interactions with customers in the context of a catalog or a product within a catalog.</span></span>

## <a name="publish-the-catalog"></a><span data-ttu-id="0af00-151">カタログの公開</span><span class="sxs-lookup"><span data-stu-id="0af00-151">Publish the catalog</span></span>
<span data-ttu-id="0af00-152">コール センターにカタログを公開して、カタログの製品情報を確定します。</span><span class="sxs-lookup"><span data-stu-id="0af00-152">By publishing a catalog for a call center, you finalize the product information in the catalog.</span></span> <span data-ttu-id="0af00-153">公開は、カタログが、実行したい任意の追加アクションへの準備が整っていることを示します。</span><span class="sxs-lookup"><span data-stu-id="0af00-153">Publication also indicates that the catalog is ready for any additional actions that you want to perform.</span></span> <span data-ttu-id="0af00-154">たとえば、印刷されたカタログを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-154">For example, you can create a printed catalog.</span></span> <span data-ttu-id="0af00-155">カタログを手動で公開することも、バッチ処理を使用してスケジュールに基づいて公開することもできます。</span><span class="sxs-lookup"><span data-stu-id="0af00-155">You can publish your catalogs manually, or you can use a batch process to publish according to a schedule.</span></span> <span data-ttu-id="0af00-156">カタログを公開する前に、カタログが検証され、承認される必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af00-156">Before you can publish a catalog, the catalog must be validated and approved.</span></span> <span data-ttu-id="0af00-157">発行された後にカタログを変更するには、カタログを取り消して再発行できます。</span><span class="sxs-lookup"><span data-stu-id="0af00-157">To change the catalog after it's published, you can retract the catalog and then republish it.</span></span>




