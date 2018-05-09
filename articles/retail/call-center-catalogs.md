---
title: "[コール センターのカタログ]"
description: "この記事は、Microsoft Dynamics 365 for Retail でのカタログのコール センター固有の機能について説明します。"
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
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 99f66e975cf5875f357af095ead66529b9784eff
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="call-center-catalogs"></a><span data-ttu-id="57184-103">コール センターのカタログ</span><span class="sxs-lookup"><span data-stu-id="57184-103">Call center catalogs</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57184-104">この記事は、Microsoft Dynamics 365 for Retail でのカタログのコール センター固有の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="57184-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="57184-105">コール センターで、顧客に提供する製品を識別するために小売製品カタログを使用できます。</span><span class="sxs-lookup"><span data-stu-id="57184-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="57184-106">コール センターは、通常、印刷したカタログを使用します。</span><span class="sxs-lookup"><span data-stu-id="57184-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="57184-107">印刷したカタログのデザインと生産は、Dynamics 365 for Retail の範囲外で処理されます。</span><span class="sxs-lookup"><span data-stu-id="57184-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="57184-108">ただし、オンライン小売カタログの設定で使用するのと同じページを使用して、カタログのデジタル フォームを作成および格納できます。</span><span class="sxs-lookup"><span data-stu-id="57184-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="57184-109">カタログを作成する前に、製品の品揃えを設定し、コール センターにその品揃えを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="57184-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="57184-110">これらの品揃えから製品を選択して、カタログに製品を追加します。</span><span class="sxs-lookup"><span data-stu-id="57184-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="57184-111">製品がカタログに追加され、カタログが完成したら、カタログを検証してデータを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57184-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="57184-112">それから、確認および承認のためにカタログを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57184-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="57184-113">カタログが承認されたら、公開できます。</span><span class="sxs-lookup"><span data-stu-id="57184-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="57184-114">コール センターのカタログが作成されたら、カタログが発行される時にカタログ データのスナップショットを取ることができます。</span><span class="sxs-lookup"><span data-stu-id="57184-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="57184-115">このスナップショットの機能により、カタログが後で変更および更新されても、カタログの特定のバージョンにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="57184-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="57184-116">コール センターのカタログは、次のオプション機能を含めるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="57184-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="57184-117">[ソース コード] – ソース コードは特定のカタログ メーリングへの顧客の応答を追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="57184-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="57184-118">[無料製品] – 追加料金なしで顧客の注文に含まれる製品です。</span><span class="sxs-lookup"><span data-stu-id="57184-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="57184-119">これらの製品は、カタログのソース コードが注文に入力されると自動的に注文に追加されます。</span><span class="sxs-lookup"><span data-stu-id="57184-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="57184-120">[スクリプト] – スクリプトは販売注文が作成されるときにコール センターの作業者が顧客に読むテキストです。</span><span class="sxs-lookup"><span data-stu-id="57184-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="57184-121">スクリプトには、あいさつまたは購買提案を含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="57184-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="57184-122">[ページ レイアウト] – ページのレイアウトは印刷したカタログの製品のページ位置を示します。</span><span class="sxs-lookup"><span data-stu-id="57184-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="57184-123">この情報は、カタログ領域の分析レポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="57184-123">This information is used for the catalog area analysis report.</span></span>





