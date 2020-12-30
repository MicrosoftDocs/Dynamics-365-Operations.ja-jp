---
title: 見込顧客を現金化
description: このトピックでは、Dynamics 365 Supply Chain Management と Dynamics 365 Sales における見込顧客を現金化するソリューションの概要を示します。
author: ChristianRytt
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55c39fac40498488519fcb539b3c3f7560a46b30
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431891"
---
# <a name="prospect-to-cash"></a><span data-ttu-id="222e8-103">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="222e8-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="222e8-104">見込顧客を現金化するソリューションは、Dynamics 365 Supply Chain Management および Dynamics 365 Sales 間で直接同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="222e8-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="222e8-105">データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。</span><span class="sxs-lookup"><span data-stu-id="222e8-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices.</span></span> <span data-ttu-id="222e8-106">データが流れている間、Sales で販売およびマーケティング活動を行い、Supply Chain Management の在庫管理を使用して注文の履行を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="222e8-106">While data is flowing, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Supply Chain Management.</span></span> 

<span data-ttu-id="222e8-107">見込顧客の現金化への統合の詳細については、短い YouTube ビデオ[見込顧客の現金化への統合](https://www.youtube.com/watch?v=AVV9x5x-XCg)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="222e8-107">For more information about the Prospect to cash integration, watch the short YouTube video [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span></span>

<span data-ttu-id="222e8-108">現在のバージョンでは、見込顧客を現金化するソリューションは次のタイプの直接同期を提供します:</span><span class="sxs-lookup"><span data-stu-id="222e8-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="222e8-109">Supply Chain Management の顧客への Sales の勘定の直接同期</span><span class="sxs-lookup"><span data-stu-id="222e8-109">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="222e8-110">製品を Supply Chain Management から Sales の製品に直接同期する</span><span class="sxs-lookup"><span data-stu-id="222e8-110">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="222e8-111">Supply Chain Management の連絡先または顧客への Sales の連絡先の直接同期</span><span class="sxs-lookup"><span data-stu-id="222e8-111">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="222e8-112">販売見積のヘッダーおよび明細行の Sales から Supply Chain Management への直接同期</span><span class="sxs-lookup"><span data-stu-id="222e8-112">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="222e8-113">販売注文の Sales と Supply Chain Management の間の直接同期</span><span class="sxs-lookup"><span data-stu-id="222e8-113">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="222e8-114">売上請求書のヘッダーおよび明細行の Supply Chain Management から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="222e8-114">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="222e8-115">Supply Chain Management のシステム要件</span><span class="sxs-lookup"><span data-stu-id="222e8-115">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="222e8-116">見込顧客の現金化は次のバージョンでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="222e8-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="222e8-117">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 (2017 年 12 月)</span><span class="sxs-lookup"><span data-stu-id="222e8-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="222e8-118">Dynamics 365 for Finance and Operations、Enterprise edition (2017 年 12 月) - アプリケーション ビルド 7.3.11971.56116 とプラットフォーム更新プログラム 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="222e8-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="222e8-119">Dynamics 365 for Finance and Operations Enterprise edition (2017 年 7 月)</span><span class="sxs-lookup"><span data-stu-id="222e8-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="222e8-120">Dynamics 365 for Finance and Operations、Enterprise edition (2017 年 7 月) - プラットフォーム更新プログラム 8 (アプリケーション ビルド 7.2.11792.56024 とプラットフォーム ビルド 7.0.4565.16212)。</span><span class="sxs-lookup"><span data-stu-id="222e8-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="222e8-121">次の修正プログラムが必要です。</span><span class="sxs-lookup"><span data-stu-id="222e8-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="222e8-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – この修正プログラムはデータ統合機能を利用した Sales から Supply Chain Management への販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="222e8-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Supply Chain Management via the Data Integration feature.</span></span> <span data-ttu-id="222e8-123">他のいくつかの機能拡張も提供されています。</span><span class="sxs-lookup"><span data-stu-id="222e8-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="222e8-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Supply Chain Management から Sales への販売注文明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="222e8-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="222e8-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Supply Chain Management から Sales への販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="222e8-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="222e8-126">インストールに他の修正プログラムからの変更が含まれているため、KB4045570 のみをインストールしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="222e8-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="222e8-127">Dynamics 365 for Finance and Operations バージョン 1611 (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="222e8-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="222e8-128">Dynamics 365 for Finance and Operations バージョン1611 (2016 年 11 月) プラットフォーム更新プログラム 8 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="222e8-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="222e8-129">次の修正プログラムが必要です。</span><span class="sxs-lookup"><span data-stu-id="222e8-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="222e8-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Supply Chain Management から Sales へのデータ インテグレーターの販売注文同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="222e8-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Supply Chain Management to Sales.</span></span> 
  - <span data-ttu-id="222e8-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - データ インテグレーターによる Supply Chain Management から Sales への販売注文ヘッダーと明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="222e8-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Supply Chain Management to Sales.</span></span>
  - <span data-ttu-id="222e8-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - データ エンティティによる見込顧客を現金化する統合のサポートが必要です。</span><span class="sxs-lookup"><span data-stu-id="222e8-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="222e8-133">修正プログラムをインストール後、**SalesPopulateProspectToCash** フォームから次のバッチ ジョブをトリガーしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="222e8-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="222e8-134">このフォームは一度しか必要ではないので非表示になります。</span><span class="sxs-lookup"><span data-stu-id="222e8-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="222e8-135">フォームにアクセスするためには、環境にログインし、ブラウザのアドレスに以下の URL を追加してください:*&mi=action:SalesPopulateProspectToCash*、たとえば、`https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`。</span><span class="sxs-lookup"><span data-stu-id="222e8-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="222e8-136">このフォームを開くには、[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="222e8-136">When the form opens, click OK.</span></span> <span data-ttu-id="222e8-137">これにより固有値を持つ新しい **SalesLine**、**SalesQuotationLine** および **CustInvoiceTrans** テーブルに **LineCreationSequnceNumber** フィールドが設定され、製品リストが更新されます。</span><span class="sxs-lookup"><span data-stu-id="222e8-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="222e8-138">これは見込顧客が現金化の統合を作業するために必要です。</span><span class="sxs-lookup"><span data-stu-id="222e8-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="222e8-139">Sales のシステム要件</span><span class="sxs-lookup"><span data-stu-id="222e8-139">System requirements for Sales</span></span>

<span data-ttu-id="222e8-140">見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="222e8-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="222e8-141">Dynamics 365 Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンラインまたはそれ以降のバージョン</span><span class="sxs-lookup"><span data-stu-id="222e8-141">Dynamics 365 Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="222e8-142">Dynamics 365 Sales バージョン 1.15.0.0 またはそれ以降のバージョンの見込顧客を現金化するソリューション。</span><span class="sxs-lookup"><span data-stu-id="222e8-142">Prospect to cash solution for Dynamics 365 Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="222e8-143">このソリューションは、AppSource からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="222e8-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="222e8-144">[Dynamics 365、見込顧客を現金化のダウンロード](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)。</span><span class="sxs-lookup"><span data-stu-id="222e8-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
