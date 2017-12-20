---
title: "見込顧客を現金化"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition、および Microsoft Dynamics 365 for Sales における見込顧客を現金化するソリューションについて概説します。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
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
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: ja-jp
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="aea81-103">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="aea81-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="aea81-104">この見込顧客を現金化するソリューションは、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition、および Microsoft Dynamics 365 for Sales 間で直接同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="aea81-104">The Prospect to cash solution provides direct synchronization across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and Microsoft Dynamics 365 for Sales.</span></span> <span data-ttu-id="aea81-105">データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れを可能にします。</span><span class="sxs-lookup"><span data-stu-id="aea81-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="aea81-106">データは Finance and Operations と Sales との間を流れていますが、Sales のセールスおよびマーケティング活動を行い、Finance and Operations の在庫管理を使用して注文の履行を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="aea81-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span>

<span data-ttu-id="aea81-107">現在のバージョンでは、見込顧客を現金化するソリューションは次のタイプの直接同期を提供します:</span><span class="sxs-lookup"><span data-stu-id="aea81-107">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="aea81-108">Sales でアカウントの管理、および Sales から Finance and Operations への直接同期</span><span class="sxs-lookup"><span data-stu-id="aea81-108">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="aea81-109">Finance and Operations で製品の管理、および Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="aea81-109">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="aea81-110">Sales の連絡先を管理し、Finance and Operations の連絡先または顧客に直接同期させる</span><span class="sxs-lookup"><span data-stu-id="aea81-110">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="aea81-111">販売見積の Sales から Finance and Operations への直接同期</span><span class="sxs-lookup"><span data-stu-id="aea81-111">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="aea81-112">販売注文の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="aea81-112">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="aea81-113">販売注文の Sales と Finance and Operations の間の直接同期</span><span class="sxs-lookup"><span data-stu-id="aea81-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="aea81-114">売上請求書の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="aea81-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="aea81-115">以前のバージョンでは、見込顧客を現金化するソリューションは次のタイプの非直接同期を提供します:</span><span class="sxs-lookup"><span data-stu-id="aea81-115">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="aea81-116">Sales でアカウントの管理、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="aea81-116">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="aea81-117">Sales で連絡先の管理、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="aea81-117">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="aea81-118">Finance and Operations で製品の管理、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="aea81-118">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="aea81-119">Sales で販売見積の作成、および Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="aea81-119">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="aea81-120">Finance and Operations で販売注文の作成、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="aea81-120">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="aea81-121">Finance and Operations で販売請求書の作成、および Sales への同期</span><span class="sxs-lookup"><span data-stu-id="aea81-121">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="aea81-122">Finance and Operations のシステム要件</span><span class="sxs-lookup"><span data-stu-id="aea81-122">System requirements for Finance and Operations</span></span>

<span data-ttu-id="aea81-123">見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="aea81-123">To use the Prospect to cash solution, you must install the following components:</span></span>

### <a name="july-2017"></a><span data-ttu-id="aea81-124">2017 年 7 月</span><span class="sxs-lookup"><span data-stu-id="aea81-124">July 2017</span></span> 

- <span data-ttu-id="aea81-125">プラットフォーム アップデート 8 (プラットフォーム ビルド 7.0.4565.16212 によるアプリケーション ビルド 7.2.11792.56024 ) による Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)</span><span class="sxs-lookup"><span data-stu-id="aea81-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212)</span></span>
- <span data-ttu-id="aea81-126">Finance and Operations の次の修正プログラム。</span><span class="sxs-lookup"><span data-stu-id="aea81-126">The following hotfixes for Finance and Operations:</span></span>

    - <span data-ttu-id="aea81-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – この修正プログラムはデータ統合機能を利用した Sales から Finance and Operations への販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="aea81-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="aea81-128">他のいくつかの機能拡張も提供されています。</span><span class="sxs-lookup"><span data-stu-id="aea81-128">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="aea81-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="aea81-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="aea81-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – この修正プログラムはデータ統合機能を利用した Finance and Operations から Sales への販売注文の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="aea81-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aea81-131">インストールに他の Microsoft サポート技術情報 (KB) からの変更が含まれているため、KB4045570 のみをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aea81-131">You only have to install KB4045570, because the installation includes the changes from the other Microsoft Knowledge Base (KB) articles.</span></span>

### <a name="november-2016-version-1611"></a><span data-ttu-id="aea81-132">2016 年 11 月 (バージョン 1611)</span><span class="sxs-lookup"><span data-stu-id="aea81-132">November 2016 (Version 1611)</span></span>

- <span data-ttu-id="aea81-133">プラットフォーム アップデート 8 またはそれ以降による Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="aea81-133">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (November 2016) with platform update 8 or higher</span></span>

- <span data-ttu-id="aea81-134">Finance and Operations の次の修正プログラム。</span><span class="sxs-lookup"><span data-stu-id="aea81-134">The following hotfixes for Finance and Operations:</span></span>

    - <span data-ttu-id="aea81-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Microsoft Dynamics 365 for Finance and Operations から Sales へのデータ インテグレーターの販売注文同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="aea81-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Microsoft Dynamics 365 for Finance and Operations to Sales</span></span> 
    - <span data-ttu-id="aea81-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Microsoft Dynamics 365 for Finance and Operations から Sales へのデータ インテグレーターの販売注文ヘッダーと明細行の同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="aea81-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Microsoft Dynamics 365 for Finance and Operations to Sales</span></span>
    - <span data-ttu-id="aea81-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - データ エンティティによる見込顧客を現金化する統合のサポートが必要です</span><span class="sxs-lookup"><span data-stu-id="aea81-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="aea81-138">修正プログラムをインストール後、に SalesPopulateProspectToCash フォームから次のバッチ ジョブをトリガーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aea81-138">After installing the hotfixes you have to trigger the following batch job from the form SalesPopulateProspectToCash.</span></span> <span data-ttu-id="aea81-139">このフォームは 1 度しか必要ではないので非表示になります。</span><span class="sxs-lookup"><span data-stu-id="aea81-139">This form is hidden as you only need it once.</span></span> <span data-ttu-id="aea81-140">これにアクセスするためには、環境にログインした時に、ブラウザのアドレスに以下を追加してください: &mi=action:SalesPopulateProspectToCash E.g.</span><span class="sxs-lookup"><span data-stu-id="aea81-140">To access it add the following to your browser address, when logged in to the environment: &mi=action:SalesPopulateProspectToCash E.g.</span></span> <span data-ttu-id="aea81-141">https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash オープンするフォームで OK をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aea81-141">https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash In the form that opens click OK.</span></span>
    <span data-ttu-id="aea81-142">これにより固有値を持つ新しい 「SalesLine」、「SalesQuotationLine」 および 「CustInvoiceTrans」 テーブルに 「LineCreationSequnceNumber」 フィールドが設定され、製品リストが更新されます。</span><span class="sxs-lookup"><span data-stu-id="aea81-142">This will populate a new “LineCreationSequnceNumber” field in “SalesLine”, “SalesQuotationLine” and “CustInvoiceTrans” tables with unique values and refresh the product list.</span></span> <span data-ttu-id="aea81-143">これは P2C の統合が 7.1 で機能するために必要です。</span><span class="sxs-lookup"><span data-stu-id="aea81-143">This is needed for the P2C integration to work on 7.1</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="aea81-144">Sales のシステム要件</span><span class="sxs-lookup"><span data-stu-id="aea81-144">System requirements for Sales</span></span>

<span data-ttu-id="aea81-145">見込顧客を現金化するソリューションを使用するには、以下のコンポーネントをインストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="aea81-145">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="aea81-146">Microsoft Dynamics 365 for Sales バージョン 1612 (8.2.1.207) (DB 8.2.1.207) オンライン</span><span class="sxs-lookup"><span data-stu-id="aea81-146">Microsoft Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="aea81-147">Microsoft Dynamics 365 for Sales バージョン 1.15.0.0 (v15) の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="aea81-147">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="aea81-148">テンプレート バージョン 1.0.0.0 および 1.0.0.1 は Microsoft Dynamics 365 for Sales、バージョン 1.14.1.0 の見込顧客を現金化するソリューションでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="aea81-148">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="aea81-149">テンプレート バージョン 2.0.0.0 および 2.1.0.0 は Microsoft Dynamics 365 for Sales、バージョン 1.15.0.0 の見込顧客を現金化するソリューションでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="aea81-149">Templates with version 2.0.0.0 and 2.1.0.0 are upported on Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="aea81-150">Sales の見込顧客を現金化するソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="aea81-150">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="aea81-151">CustomerSource から [Dynamics 365 for Sales の見込顧客を現金化ソリューション パッケージ zip ファイル](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="aea81-151">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="aea81-152">zip ファイルがブロックされていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="aea81-152">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="aea81-153">それ以外の場合、ソリューション パッケージをインストールするさいに次のエラー メッセージを受け取ります: [「インポート パッケージ見つかりませんでした」]。</span><span class="sxs-lookup"><span data-stu-id="aea81-153">Otherwise, when you try to install the solution package, you receive the following error message: "No import packages were found."</span></span> <span data-ttu-id="aea81-154">zip ファイルのブロックを解除するには、ファイルを右クリックし [**プロパティ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aea81-154">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="aea81-155">次に [**ブロック解除**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aea81-155">Then select **Unblock**.</span></span>
3. <span data-ttu-id="aea81-156">解凍して、**PackageDeployer.exe** を実行します。</span><span class="sxs-lookup"><span data-stu-id="aea81-156">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="aea81-157">売上インスタンスで見込顧客を現金化するソリューションのインストール:</span><span class="sxs-lookup"><span data-stu-id="aea81-157">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="aea81-158">配置タイプとして [**Office 365**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aea81-158">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="aea81-159">[**高度な表示**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aea81-159">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="aea81-160">クイック インストールするには、[地域] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aea81-160">For a quick installation, select a region.</span></span> <span data-ttu-id="aea81-161">[**わからない**] を選択する場合、システムはすべての地域を検索するためインストールに時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="aea81-161">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="aea81-162">インストールする権限を持つ管理者ユーザーの [ユーザー名] および [パスワード] を入力します。</span><span class="sxs-lookup"><span data-stu-id="aea81-162">Enter the user name and password of an admin user who has installation rights.</span></span>

