---
title: "見込顧客を現金化"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition、および Microsoft Dynamics 365 for Sales における見込顧客を現金化するソリューションについて概説します。"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2017
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
ms.sourcegitcommit: f169b0ee20a7ca0c8d05c8bdcf2c04d411722f01
ms.openlocfilehash: ff166f89d13acbc3aefcbdb39f485881c81cb42c
ms.contentlocale: ja-jp
ms.lasthandoff: 12/21/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="e38dc-103">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="e38dc-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e38dc-104">この見込顧客を現金化するソリューションは、Dynamics 365 for Finance and Operations、Enterprise Edition、および Dynamics 365 for Sales 間で直接同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="e38dc-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="e38dc-105">データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れを可能にします。</span><span class="sxs-lookup"><span data-stu-id="e38dc-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="e38dc-106">データは Finance and Operations と Sales との間を流れていますが、Sales のセールスおよびマーケティング活動を行い、Finance and Operations の在庫管理を使用して注文の履行を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="e38dc-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span>

<span data-ttu-id="e38dc-107">現在のバージョンでは、見込顧客を現金化するソリューションは次のタイプの直接同期を提供します:</span><span class="sxs-lookup"><span data-stu-id="e38dc-107">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="e38dc-108">Sales でアカウントの管理、および Sales から Finance and Operations への直接同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-108">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="e38dc-109">Finance and Operations での製品の管理、および Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-109">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="e38dc-110">Sales の連絡先の管理、および Finance and Operations の連絡先または顧客への直接同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-110">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="e38dc-111">販売見積の Sales から Finance and Operations への直接同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-111">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="e38dc-112">販売注文の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-112">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="e38dc-113">販売注文の Sales と Finance and Operations の間の直接同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="e38dc-114">売上請求書の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="e38dc-115">以前のバージョンでは、見込顧客を現金化するソリューションは次のタイプの非直接同期を提供します:</span><span class="sxs-lookup"><span data-stu-id="e38dc-115">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="e38dc-116">Sales でアカウントの管理、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-116">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="e38dc-117">Sales での連絡先の管理、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-117">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="e38dc-118">Finance and Operations での製品の管理、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-118">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="e38dc-119">Sales での販売見積の作成、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-119">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="e38dc-120">Finance and Operations での販売注文の作成、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-120">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="e38dc-121">Finance and Operations で販売請求書の作成、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="e38dc-121">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="e38dc-122">Finance and Operations のシステム要件</span><span class="sxs-lookup"><span data-stu-id="e38dc-122">System requirements for Finance and Operations</span></span>

<span data-ttu-id="e38dc-123">見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="e38dc-123">To use the Prospect to cash solution, you must install the following components:</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="e38dc-124">Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)</span><span class="sxs-lookup"><span data-stu-id="e38dc-124">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="e38dc-125">プラットフォーム アップデート 8 (プラットフォーム ビルド 7.0.4565.16212 によるアプリケーション ビルド 7.2.11792.56024) による Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)</span><span class="sxs-lookup"><span data-stu-id="e38dc-125">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212)</span></span>
- <span data-ttu-id="e38dc-126">次の修正プログラムが必要です。</span><span class="sxs-lookup"><span data-stu-id="e38dc-126">The following hotfixes are required:</span></span>

    - <span data-ttu-id="e38dc-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – この修正プログラムはデータ統合機能を利用した Sales から Finance and Operations への販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e38dc-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="e38dc-128">他のいくつかの機能拡張も提供されています。</span><span class="sxs-lookup"><span data-stu-id="e38dc-128">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="e38dc-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e38dc-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="e38dc-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e38dc-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e38dc-131">インストールに他の修正プログラムからの変更が含まれているため、KB4045570 のみをインストールしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e38dc-131">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="e38dc-132">Dynamics 365 for Finance and Operations バージョン 1611 (2016 年 11月)</span><span class="sxs-lookup"><span data-stu-id="e38dc-132">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span> 

- <span data-ttu-id="e38dc-133">プラットフォーム アップデート 8 またはそれ以降による Dynamics 365 for Finance and Operations バージョン 1611 (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="e38dc-133">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="e38dc-134">次の修正プログラムが必要です。</span><span class="sxs-lookup"><span data-stu-id="e38dc-134">The following hotfixes are required:</span></span>

    - <span data-ttu-id="e38dc-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Finance and Operations から Sales へのデータ インテグレーターの販売注文同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e38dc-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="e38dc-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Finance and Operations から Sales へのデータ インテグレーターの販売注文のヘッダーと明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e38dc-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="e38dc-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - データ エンティティによる見込顧客を現金化する統合のサポートが必要です。</span><span class="sxs-lookup"><span data-stu-id="e38dc-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e38dc-138">修正プログラムをインストール後、[**SalesPopulateProspectToCash**] フォームから次のバッチ ジョブをトリガーしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e38dc-138">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="e38dc-139">このフォームは一度しか必要ではないので非表示になります。</span><span class="sxs-lookup"><span data-stu-id="e38dc-139">This form is hidden because you only need it once.</span></span> <span data-ttu-id="e38dc-140">フォームにアクセスするには、環境にログインし、次の事項をブラウザーのアドレス内のURLに追加します。&mi=action:SalesPopulateProspectToCash、たとえば、https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash。</span><span class="sxs-lookup"><span data-stu-id="e38dc-140">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span></span> <span data-ttu-id="e38dc-141">このフォームを開くには、[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e38dc-141">When the form opens, click OK.</span></span> <span data-ttu-id="e38dc-142">これにより固有値を持つ新しい [**SalesLine**]、[**SalesQuotationLine**] および [**CustInvoiceTrans**] テーブルに [**LineCreationSequnceNumber**] フィールドが設定され、製品リストが更新されます。</span><span class="sxs-lookup"><span data-stu-id="e38dc-142">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="e38dc-143">これは見込顧客が現金化の統合を作業するために必要です。</span><span class="sxs-lookup"><span data-stu-id="e38dc-143">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="e38dc-144">Sales のシステム要件</span><span class="sxs-lookup"><span data-stu-id="e38dc-144">System requirements for Sales</span></span>

<span data-ttu-id="e38dc-145">見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="e38dc-145">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="e38dc-146">Dynamics 365 for Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンライン</span><span class="sxs-lookup"><span data-stu-id="e38dc-146">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="e38dc-147">Dynamics 365 for Sales バージョン 1.15.0.0 (v15) の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="e38dc-147">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="e38dc-148">テンプレート バージョン 1.0.0.0 および 1.0.0.1 は Dynamics 365 for Sales、バージョン 1.14.1.0 の見込顧客を現金化するソリューションでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e38dc-148">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="e38dc-149">テンプレート バージョン 2.0.0.0 および 2.1.0.0 は Dynamics 365 for Sales、バージョン 1.15.0.0 の見込顧客を現金化するソリューションでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e38dc-149">Templates with version 2.0.0.0 and 2.1.0.0 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e38dc-150">Sales の見込顧客を現金化するソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="e38dc-150">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="e38dc-151">CustomerSource から [Dynamics 365 for Sales の見込顧客を現金化ソリューション パッケージ zip ファイル](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e38dc-151">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="e38dc-152">zip ファイルがブロックされていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="e38dc-152">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="e38dc-153">それ以外の場合、ソリューション パッケージをインストールする際に次のエラー メッセージを受け取るかもしれません [「インポート パッケージ見つかりませんでした」]。</span><span class="sxs-lookup"><span data-stu-id="e38dc-153">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="e38dc-154">zip ファイルのブロックを解除するには、ファイルを右クリックし [**プロパティ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e38dc-154">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="e38dc-155">[**ブロック解除**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e38dc-155">Select **Unblock**.</span></span>
3. <span data-ttu-id="e38dc-156">解凍して、**PackageDeployer.exe** を実行します。</span><span class="sxs-lookup"><span data-stu-id="e38dc-156">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="e38dc-157">売上インスタンスで見込顧客を現金化するソリューションのインストール:</span><span class="sxs-lookup"><span data-stu-id="e38dc-157">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="e38dc-158">配置タイプとして [**Office 365**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e38dc-158">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="e38dc-159">[**高度な表示**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e38dc-159">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="e38dc-160">クイック インストールするには、[地域] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e38dc-160">For a quick installation, select a region.</span></span> <span data-ttu-id="e38dc-161">[**わからない**] を選択する場合、システムはすべての地域を検索するためインストールに時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="e38dc-161">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="e38dc-162">インストールする権限を持つ管理者ユーザーの [ユーザー名] および [パスワード] を入力します。</span><span class="sxs-lookup"><span data-stu-id="e38dc-162">Enter the user name and password of an admin user who has installation rights.</span></span>

