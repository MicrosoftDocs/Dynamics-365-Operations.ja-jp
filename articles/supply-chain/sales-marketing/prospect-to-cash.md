---
title: "見込顧客を現金化"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition、および Microsoft Dynamics 365 for Sales における見込顧客を現金化するソリューションについて概説します。"
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 62f328c5a6bf5343c97de0b7d907bbcfe2fcde4d
ms.contentlocale: ja-jp
ms.lasthandoff: 02/23/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="c2e28-103">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="c2e28-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c2e28-104">この見込顧客を現金化するソリューションは、Dynamics 365 for Finance and Operations、Enterprise Edition、および Dynamics 365 for Sales 間で直接同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="c2e28-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="c2e28-105">データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れを可能にします。</span><span class="sxs-lookup"><span data-stu-id="c2e28-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="c2e28-106">データは Finance and Operations と Sales との間を流れていますが、Sales のセールスおよびマーケティング活動を行い、Finance and Operations の在庫管理を使用して注文の履行を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="c2e28-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="c2e28-107">見込顧客を現金化することの詳細については、短い YouTube ビデオを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c2e28-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="c2e28-108">現在のバージョンでは、見込顧客を現金化するソリューションは次のタイプの直接同期を提供します:</span><span class="sxs-lookup"><span data-stu-id="c2e28-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="c2e28-109">Sales でアカウントの管理、および Sales から Finance and Operations への直接同期</span><span class="sxs-lookup"><span data-stu-id="c2e28-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="c2e28-110">Finance and Operations での製品の管理、および Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="c2e28-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="c2e28-111">Sales の連絡先の管理、および Finance and Operations の連絡先または顧客への直接同期</span><span class="sxs-lookup"><span data-stu-id="c2e28-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="c2e28-112">販売見積の Sales から Finance and Operations への直接同期 (リリース保留中のテンプレート)</span><span class="sxs-lookup"><span data-stu-id="c2e28-112">Synchronize sales quotation directly from Sales to Finance and Operations (template pending release)</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="c2e28-113">販売注文の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="c2e28-113">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="c2e28-114">販売注文の Sales と Finance and Operations の間の直接同期 (リリース保留中のテンプレート)</span><span class="sxs-lookup"><span data-stu-id="c2e28-114">Synchronize sales orders directly between Sales and Finance and Operations (template pending release)</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="c2e28-115">売上請求書の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="c2e28-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="c2e28-116">Finance and Operations のシステム要件</span><span class="sxs-lookup"><span data-stu-id="c2e28-116">System requirements for Finance and Operations</span></span>

<span data-ttu-id="c2e28-117">見込顧客の現金化は次のバージョンでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c2e28-117">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="c2e28-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (2017 年 12 月)</span><span class="sxs-lookup"><span data-stu-id="c2e28-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="c2e28-119">Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 12 月) - プラットフォーム アップデート 12 (7.0.4709.41129) によるアプリケーション ビルド 7.3.11971.56116</span><span class="sxs-lookup"><span data-stu-id="c2e28-119">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="c2e28-120">Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)</span><span class="sxs-lookup"><span data-stu-id="c2e28-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="c2e28-121">Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) - プラットフォーム アップデート 8 (プラットフォーム ビルド 7.0.4565.16212 によるアプリケーション ビルド 7.2.11792.56024) による。</span><span class="sxs-lookup"><span data-stu-id="c2e28-121">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="c2e28-122">次の修正プログラムが必要です。</span><span class="sxs-lookup"><span data-stu-id="c2e28-122">The following hotfixes are required:</span></span>

    - <span data-ttu-id="c2e28-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – この修正プログラムはデータ統合機能を利用した Sales から Finance and Operations への販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c2e28-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="c2e28-124">他のいくつかの機能拡張も提供されています。</span><span class="sxs-lookup"><span data-stu-id="c2e28-124">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="c2e28-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c2e28-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="c2e28-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c2e28-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c2e28-127">インストールに他の修正プログラムからの変更が含まれているため、KB4045570 のみをインストールしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c2e28-127">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="c2e28-128">Dynamics 365 for Finance and Operations バージョン 1611 (2016 年 11月)</span><span class="sxs-lookup"><span data-stu-id="c2e28-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="c2e28-129">プラットフォーム アップデート 8 またはそれ以降による Dynamics 365 for Finance and Operations バージョン 1611 (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="c2e28-129">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="c2e28-130">次の修正プログラムが必要です。</span><span class="sxs-lookup"><span data-stu-id="c2e28-130">The following hotfixes are required:</span></span>

    - <span data-ttu-id="c2e28-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Finance and Operations から Sales へのデータ インテグレーターの販売注文同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c2e28-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="c2e28-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Finance and Operations から Sales へのデータ インテグレーターの販売注文のヘッダーと明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c2e28-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="c2e28-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - データ エンティティによる見込顧客を現金化する統合のサポートが必要です。</span><span class="sxs-lookup"><span data-stu-id="c2e28-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c2e28-134">修正プログラムをインストール後、[**SalesPopulateProspectToCash**] フォームから次のバッチ ジョブをトリガーしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c2e28-134">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="c2e28-135">このフォームは一度しか必要ではないので非表示になります。</span><span class="sxs-lookup"><span data-stu-id="c2e28-135">This form is hidden because you only need it once.</span></span> <span data-ttu-id="c2e28-136">フォームにアクセスするためには、環境にログインし、ブラウザのアドレスに以下の URL を追加してください: &mi=action:SalesPopulateProspectToCash、たとえば、`https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`。</span><span class="sxs-lookup"><span data-stu-id="c2e28-136">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="c2e28-137">このフォームを開くには、[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2e28-137">When the form opens, click OK.</span></span> <span data-ttu-id="c2e28-138">これにより固有値を持つ新しい [**SalesLine**]、[**SalesQuotationLine**] および [**CustInvoiceTrans**] テーブルに [**LineCreationSequnceNumber**] フィールドが設定され、製品リストが更新されます。</span><span class="sxs-lookup"><span data-stu-id="c2e28-138">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="c2e28-139">これは見込顧客が現金化の統合を作業するために必要です。</span><span class="sxs-lookup"><span data-stu-id="c2e28-139">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="c2e28-140">Sales のシステム要件</span><span class="sxs-lookup"><span data-stu-id="c2e28-140">System requirements for Sales</span></span>

<span data-ttu-id="c2e28-141">見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="c2e28-141">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="c2e28-142">Dynamics 365 for Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンライン</span><span class="sxs-lookup"><span data-stu-id="c2e28-142">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="c2e28-143">Dynamics 365 for Sales バージョン 1.15.0.0 (v15) の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="c2e28-143">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c2e28-144">Sales の見込顧客を現金化するソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="c2e28-144">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="c2e28-145">CustomerSource から [Dynamics 365 for Sales の見込顧客を現金化ソリューション パッケージ zip ファイル](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c2e28-145">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="c2e28-146">zip ファイルがブロックされていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c2e28-146">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="c2e28-147">それ以外の場合、ソリューション パッケージをインストールする際に次のエラー メッセージを受け取るかもしれません [「インポート パッケージ見つかりませんでした」]。</span><span class="sxs-lookup"><span data-stu-id="c2e28-147">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="c2e28-148">zip ファイルのブロックを解除するには、ファイルを右クリックし [**プロパティ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e28-148">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="c2e28-149">[**ブロック解除**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e28-149">Select **Unblock**.</span></span>
3. <span data-ttu-id="c2e28-150">解凍して、**PackageDeployer.exe** を実行します。</span><span class="sxs-lookup"><span data-stu-id="c2e28-150">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="c2e28-151">売上インスタンスで見込顧客を現金化するソリューションのインストール:</span><span class="sxs-lookup"><span data-stu-id="c2e28-151">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="c2e28-152">配置タイプとして [**Office 365**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e28-152">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="c2e28-153">[**高度な表示**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e28-153">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="c2e28-154">クイック インストールするには、[地域] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2e28-154">For a quick installation, select a region.</span></span> <span data-ttu-id="c2e28-155">[**わからない**] を選択する場合、システムはすべての地域を検索するためインストールに時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="c2e28-155">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="c2e28-156">インストールする権限を持つ管理者ユーザーの [ユーザー名] および [パスワード] を入力します。</span><span class="sxs-lookup"><span data-stu-id="c2e28-156">Enter the user name and password of an admin user who has installation rights.</span></span>



