---
title: 仕入先カタログのインポート
description: このトピックでは、仕入先カタログ データをインポートするプロセスについて説明します。
author: RichardLuan
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: riluan
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 6a6fc2b4fe4245a1fe5b5a7eaafe8cc7fd337ab9
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020757"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="f78d5-103">仕入先カタログのインポート</span><span class="sxs-lookup"><span data-stu-id="f78d5-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="f78d5-104">仕入先カタログのインポート</span><span class="sxs-lookup"><span data-stu-id="f78d5-104">Vendor catalogs import</span></span>

<span data-ttu-id="f78d5-105">Dynamics 365 Supply Chain Management では、購買担当者が、会社の従業員が内部で使用する品目およびサービスを注文する際に使用できるカタログの作成および管理を行えます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="f78d5-106">調達カタログを作成するには、製品カタログ データをインポートするか、製品カタログ データを手動で製品マスターに追加することにより、従業員が使用できるようになる品目とサービスを追加できます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="f78d5-107">Microsoft Dynamics 365 クライアントから、仕入先より送信されたカタログ データをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="f78d5-108">仕入先がユーザーに送信する製品データは、カタログ保守要求 (CMR) ファイルの形式で、XML ファイル形式でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f78d5-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="f78d5-109">CMR ファイルには、仕入先が会社に提供する製品の詳細が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f78d5-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="f78d5-110">仕入先カタログ データのインポート</span><span class="sxs-lookup"><span data-stu-id="f78d5-110">Import vendor catalog data</span></span>

<span data-ttu-id="f78d5-111">仕入先データ カタログをインポートするには、次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f78d5-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="f78d5-112">データ マッピング ルールが定義されているデータ管理ワークスペースで、プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="f78d5-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="f78d5-113">**データ管理** を選択し、**データ プロジェクトのロールの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78d5-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="f78d5-114">調達カテゴリ階層を設定し、仕入先を調達カテゴリに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="f78d5-115">商品コードを使用している場合は、調達カテゴリに商品コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="f78d5-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="f78d5-116">調達カテゴリ階層の設定の詳細については、次を参照してください。[調達カテゴリ階層の設定](../procurement/tasks/set-up-procurement-category-hierarchy.md)</span><span class="sxs-lookup"><span data-stu-id="f78d5-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="f78d5-117">仕入先をカタログ インポート用にコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="f78d5-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="f78d5-118">仕入先を選択し、**調達** > **設定** > **仕入先カタログ インポートの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78d5-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="f78d5-119">ワークフローをカタログ インポート用にコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="f78d5-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="f78d5-120">CMR ファイル テンプレートを作成し、これを仕入先と共有します。</span><span class="sxs-lookup"><span data-stu-id="f78d5-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="f78d5-121">**調達** \> **共通** \> **カタログ** \> **仕入先カタログ** を選択して、仕入先のカタログを作成します。</span><span class="sxs-lookup"><span data-stu-id="f78d5-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="f78d5-122">仕入先から受け取るカタログ保守要求 (CMR) ファイルがこのカタログでグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="f78d5-123">CMR ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f78d5-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="f78d5-124">仕入先カタログで製品を確認、承認または却下します。</span><span class="sxs-lookup"><span data-stu-id="f78d5-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="f78d5-125">製品は、調達カテゴリに自動的にマップされます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="f78d5-126">承認済製品は、製品マスターに追加され、選択した法人にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="f78d5-127">承認済製品のみ調達カタログに追加できます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="f78d5-128">カタログ インポート ファイル テンプレートの生成</span><span class="sxs-lookup"><span data-stu-id="f78d5-128">Generate a catalog import file template</span></span>

<span data-ttu-id="f78d5-129">カタログ インポート ファイル テンプレートは、仕入先の製品の CMR ファイルの作成に使用する XSD ファイルです。</span><span class="sxs-lookup"><span data-stu-id="f78d5-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="f78d5-130">CMR ファイルを使用して、新しいカタログの作成、既存のカタログの置換、または既存のカタログの変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="f78d5-131">**調達とソーシング** \> **カタログ** \>**仕入先カタログ** を選択し、使用するカタログをダブル クリックします。</span><span class="sxs-lookup"><span data-stu-id="f78d5-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="f78d5-132">現在のカタログ インポート テンプレート (XSD ファイル) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="f78d5-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="f78d5-133">**関連情報** グループで、**カタログ** タブ、**アクション ウィンドウ** の、**更新カタログ** ページで、**カタログ テンプレートの生成** をクリックし、**調達カテゴリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78d5-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="f78d5-134">**調達カテゴリ** オプションを使用すると、仕入先が製品の提供を許可されている調達カテゴリを含むカタログ テンプレートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="f78d5-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="f78d5-135">**名前を付けて保存** ダイアログ ボックスで、カタログ ファイル テンプレートを保管する場所を選択したり、ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="f78d5-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="f78d5-136">詳細および例については、このブログ投稿を参照してください: [Dynamics AX の仕入先カタログ](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)。</span><span class="sxs-lookup"><span data-stu-id="f78d5-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
