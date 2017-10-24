---
title: "見込顧客を現金化"
description: "トピックでは、Dynamics 365 for Sales and Dynamics 365 for Finance and Operations, Enterprise edition および Dynamics 365 for Sales における見込顧客を現金化するソリューションの概要を提供します。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="10bf1-103">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="10bf1-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="10bf1-104">見込顧客を現金化ソリューションにより、[データ統合](/common-data-service/entity-reference/dynamics-365-integration)を使用し、Common Data Service (CDS) 経由で Dynamics 365 for Finance and Operations, Enterprise edition および Dynamics 365 for Sales インスタンス間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="10bf1-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="10bf1-105">データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書データの流れを可能にします。</span><span class="sxs-lookup"><span data-stu-id="10bf1-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="10bf1-106">データは Finance and Operations と Sales との間を流れていますが、Sales のセールスおよびマーケティング活動を行い、Finance and Operations の在庫管理で注文の履行を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="10bf1-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="10bf1-107">このソリューションは、次の領域での統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="10bf1-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="10bf1-108">Sales でアカウントの管理、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="10bf1-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="10bf1-109">Sales で連絡先の管理、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="10bf1-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="10bf1-110">Finance and Operations で製品の管理、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="10bf1-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="10bf1-111">Sales で販売見積の作成、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="10bf1-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="10bf1-112">Finance and Operations で販売注文の作成、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="10bf1-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="10bf1-113">Finance and Operations で販売請求書の作成、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="10bf1-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="10bf1-114">Dynamics 365 for Finance and Operations, Enterprise Edition のシステム要件</span><span class="sxs-lookup"><span data-stu-id="10bf1-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="10bf1-115">見込顧客を現金化するソリューションを使用するには、以下をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="10bf1-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="10bf1-116">プラットフォーム アップデート 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212) による Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)</span><span class="sxs-lookup"><span data-stu-id="10bf1-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="10bf1-117">Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 ７ 月) の 2 つの修正プログラム。</span><span class="sxs-lookup"><span data-stu-id="10bf1-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="10bf1-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - この修正プログラムは Finance and Operations から Sales へのデータ統合機能による販売注文明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="10bf1-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="10bf1-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - この修正プログラムは Finance and Operations から Sales へのデータ統合機能による販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="10bf1-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="10bf1-120">[**注記**]: インストールには KB4036461 からの変更が含まれているため、KB4036524 のみをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="10bf1-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="10bf1-121">Dynamics 365 for Sales のシステム要件</span><span class="sxs-lookup"><span data-stu-id="10bf1-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="10bf1-122">見込顧客を現金化するソリューションを使用するには、以下をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="10bf1-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="10bf1-123">Dynamics 365 for Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンラインまたはそれ以降。</span><span class="sxs-lookup"><span data-stu-id="10bf1-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="10bf1-124">Dynamics 365 for Sales バージョン 1.14.0.0 (v14) またはそれ以降の見込顧客を現金化するソリューション。</span><span class="sxs-lookup"><span data-stu-id="10bf1-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="10bf1-125">Sales の見込顧客を現金化するソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="10bf1-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="10bf1-126">CustomerSource で [Dynamics 365 for Sales の見込顧客を現金化ソリューション パッケージ zip ファイル](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="10bf1-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="10bf1-127">zip ファイルがブロックされていないことを確認し、リューション パッケージをインストールする際に、「インポート パッケージが見つかりませんでした」のエラー メッセージが出ないようにします。</span><span class="sxs-lookup"><span data-stu-id="10bf1-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="10bf1-128">ファイルをブロック解除するには、次の点を行います。</span><span class="sxs-lookup"><span data-stu-id="10bf1-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="10bf1-129">zip ファイルを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="10bf1-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="10bf1-130">[**プロパティ**] を選択し、次に [**ブロック解除**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="10bf1-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="10bf1-131">解凍して、PackageDeployer.exe を実行します。</span><span class="sxs-lookup"><span data-stu-id="10bf1-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="10bf1-132">売上インスタンスで見込顧客を現金化するソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="10bf1-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="10bf1-133">[**Office 365**] 配置タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="10bf1-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="10bf1-134">[**高度な表示**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="10bf1-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="10bf1-135">クイック インストールするには、[**地域**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="10bf1-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="10bf1-136">[**わからない**] を選択する場合、システムはすべての地域を検索するためインストールに時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="10bf1-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="10bf1-137">インストールするユーザーの権限を持つ管理者ユーザーに対して [**ユーザー名**] および [**パスワード**] を入力します。</span><span class="sxs-lookup"><span data-stu-id="10bf1-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

