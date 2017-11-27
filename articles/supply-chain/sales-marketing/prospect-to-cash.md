---
title: "見込顧客を現金化"
description: "トピックでは、Dynamics 365 for Sales and Dynamics 365 for Finance and Operations, Enterprise edition および Dynamics 365 for Sales における見込顧客を現金化するソリューションの概要を提供します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: ja-jp
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="20111-103">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="20111-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="20111-104">見込顧客を現金化ソリューションにより、[データ統合](/common-data-service/entity-reference/dynamics-365-integration)を使用し、Common Data Service (CDS) 経由で Dynamics 365 for Finance and Operations, Enterprise edition および Dynamics 365 for Sales インスタンス間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="20111-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="20111-105">データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書データの流れを可能にします。</span><span class="sxs-lookup"><span data-stu-id="20111-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="20111-106">データは Finance and Operations と Sales との間を流れていますが、Sales のセールスおよびマーケティング活動を行い、Finance and Operations の在庫管理で注文の履行を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="20111-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="20111-107">このソリューションは、次の領域での統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="20111-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="20111-108">Sales でアカウントの管理、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="20111-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="20111-109">Sales で連絡先の管理、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="20111-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="20111-110">Finance and Operations で製品の管理、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="20111-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="20111-111">Sales で販売見積の作成、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="20111-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="20111-112">Finance and Operations で販売注文の作成、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="20111-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="20111-113">Finance and Operations で販売請求書の作成、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="20111-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

<span data-ttu-id="20111-114">このソリューションは、次の領域で直接同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="20111-114">This solution provides direct synchronization in the following areas:</span></span>

-   [<span data-ttu-id="20111-115">Sales でアカウントの管理、および Sales から Finance and Operations への直接同期</span><span class="sxs-lookup"><span data-stu-id="20111-115">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
-   [<span data-ttu-id="20111-116">Finance and Operations で製品の管理、および Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="20111-116">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
-   [<span data-ttu-id="20111-117">Sales の連絡先を管理し、Finance and Operations の連絡先または顧客に直接同期させる</span><span class="sxs-lookup"><span data-stu-id="20111-117">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
-   [<span data-ttu-id="20111-118">販売見積ヘッダーおよび明細行の Sales から Finance and Operations への直接同期</span><span class="sxs-lookup"><span data-stu-id="20111-118">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
-   [<span data-ttu-id="20111-119">Finance and Operations で販売注文の作成、および Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="20111-119">Create sales orders in Finance and Operations and sync them directly to Sales</span></span>](sales-order-template-mapping-direct.md)
-  [<span data-ttu-id="20111-120">販売注文ヘッダーおよび明細行の Sales と Finance and Operations の間の直接同期</span><span class="sxs-lookup"><span data-stu-id="20111-120">Synchronize sales order headers and lines directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-between-sales-fin.md)
-   [<span data-ttu-id="20111-121">販売注文の Sales と Finance and Operations の間の直接同期</span><span class="sxs-lookup"><span data-stu-id="20111-121">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
-   [<span data-ttu-id="20111-122">Finance and Operations で販売請求書の作成および Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="20111-122">Create sales invoices in Finance and Operations and sync them directly to Sales</span></span>](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="20111-123">Dynamics 365 for Finance and Operations, Enterprise Edition のシステム要件</span><span class="sxs-lookup"><span data-stu-id="20111-123">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="20111-124">見込顧客を現金化するソリューションを使用するには、以下をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20111-124">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="20111-125">プラットフォーム アップデート 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212) による Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)</span><span class="sxs-lookup"><span data-stu-id="20111-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="20111-126">Dynamics 365 for Finance and Operations、Enterprise edition (2017 年 7 月) の修正プログラム。</span><span class="sxs-lookup"><span data-stu-id="20111-126">Hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>
        
    -  <span data-ttu-id="20111-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - この修正プログラムは、Sales から Finance and Operations へのデータ統合機能を使用して販売注文の同期をサポートし、他にも多くの拡張機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="20111-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - This hotfix enabels support for sales order synchronization with the Data Integration feature from Sales to Finance and Operations, along with a number of other enhancements.</span></span>

    -  <span data-ttu-id="20111-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - この修正プログラムは Finance and Operations から Sales へのデータ統合機能による販売注文明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="20111-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="20111-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - この修正プログラムは Finance and Operations から Sales へのデータ統合機能による販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="20111-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>

<span data-ttu-id="20111-130">\[**注記**\]: インストールに他の KB からの変更が含まれているため、KB4045570 のみをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20111-130">**Note**: You only need to install KB4045570 because the installation includes the changes from the other KB's.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="20111-131">Dynamics 365 for Sales のシステム要件</span><span class="sxs-lookup"><span data-stu-id="20111-131">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="20111-132">見込顧客を現金化するソリューションを使用するには、以下をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20111-132">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="20111-133">Dynamics 365 for Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンライン。</span><span class="sxs-lookup"><span data-stu-id="20111-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span></span>
- <span data-ttu-id="20111-134">Dynamics 365 for Sales バージョン 1.14.0.0 (v14) またはそれ以降の見込顧客を現金化するソリューション。</span><span class="sxs-lookup"><span data-stu-id="20111-134">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="20111-135">Sales の見込顧客を現金化するソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="20111-135">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="20111-136">CustomerSource で [Dynamics 365 for Sales の見込顧客を現金化ソリューション パッケージ zip ファイル](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="20111-136">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="20111-137">zip ファイルがブロックされていないことを確認し、リューション パッケージをインストールする際に、「インポート パッケージが見つかりませんでした」のエラー メッセージが出ないようにします。</span><span class="sxs-lookup"><span data-stu-id="20111-137">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="20111-138">ファイルをブロック解除するには、次の点を行います。</span><span class="sxs-lookup"><span data-stu-id="20111-138">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="20111-139">zip ファイルを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="20111-139">Right-click the zip file.</span></span>
    -  <span data-ttu-id="20111-140">[プロパティ] を選択し、次に [ブロック解除] を選択します。</span><span class="sxs-lookup"><span data-stu-id="20111-140">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="20111-141">解凍して、PackageDeployer.exe を実行します。</span><span class="sxs-lookup"><span data-stu-id="20111-141">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="20111-142">売上インスタンスで見込顧客を現金化するソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="20111-142">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="20111-143">[Office 365] 配置タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="20111-143">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="20111-144">[高度な表示] を選択します。</span><span class="sxs-lookup"><span data-stu-id="20111-144">Select **Show advanced**.</span></span>
    - <span data-ttu-id="20111-145">クイック インストールするには、[地域] を選択します。</span><span class="sxs-lookup"><span data-stu-id="20111-145">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="20111-146">[わからない] を選択する場合、システムはすべての地域を検索するためインストールに時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="20111-146">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="20111-147">インストールするユーザーの権限を持つ管理者ユーザーに対して [ユーザー名] および [パスワード] を入力します。</span><span class="sxs-lookup"><span data-stu-id="20111-147">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

