---
title: 印刷可能な FTI フォームの生成
description: このトピックでは、電子レポート (ER) フレームワークを使用して、印刷可能な自由書式の請求書 (FTI) フォームを Microsoft Office ドキュメントとして生成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: d27a11a0d925b0f1164578f9c04e6abd4736b2b2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "325529"
---
# <a name="generate-printable-fti-forms"></a><span data-ttu-id="01a4a-103">印刷可能な FTI フォームを生成する</span><span class="sxs-lookup"><span data-stu-id="01a4a-103">Generate printable FTI forms</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="01a4a-104">電子レポート (ER) フレームワークにより、印刷可能な自由書式の請求書 (FTI) フォームを Microsoft Office ドキュメントとして生成することができます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-104">The Electronic reporting (ER) framework lets you generate printable free text invoice (FTI) forms as Microsoft Office documents.</span></span> <span data-ttu-id="01a4a-105">このトピックでは、使用可能なコンフィギュレーション テンプレートと共に、独自のコンフィギュレーションを構築する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="01a4a-105">This topic provides information about how to build your own configurations as well as details of available configuration templates.</span></span>

## <a name="overview"></a><span data-ttu-id="01a4a-106">概要</span><span class="sxs-lookup"><span data-stu-id="01a4a-106">Overview</span></span>

<span data-ttu-id="01a4a-107">Microsoft SQL Server Reporting Services (SSRS) を使用して印刷可能な FTI フォームを生成する既存の機能に加えて、ER フレームワークを使用することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="01a4a-107">In addition to the existing capability of generating printable FTI forms by using Microsoft SQL Server Reporting Services (SSRS), you can now use the ER framework.</span></span> <span data-ttu-id="01a4a-108">Microsoft Office Excel および Word で印刷可能な FTI フォームを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-108">You can manage printable FTI forms in Microsoft Office Excel and Word.</span></span> <span data-ttu-id="01a4a-109">また、コードを変更せずにレイアウト、データ フロー、および形式を特定の要件に合わせて変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-109">You can also modify the layout, data flow, and formatting to meet specific requirements without making code changes.</span></span>

> [!NOTE]
> <span data-ttu-id="01a4a-110">印刷可能な FTI フォーム ソリューションのサンプル用の既存の ER コンフィギュレーションの概要から開始する場合、このトピックで後述する**印刷可能な FTI フォームを生成するための ER コンフィギュレーションのサンプルをダウンロード**のセクションに直接移動します。</span><span class="sxs-lookup"><span data-stu-id="01a4a-110">If you want to start with an overview of existing ER configurations for this sample of the printable FTI forms solution, you can go directly to section **Download sample ER configurations to generate printable FTI forms** later in this topic.</span></span>

## <a name="create-customized-configurations-for-fti-printable-forms"></a><span data-ttu-id="01a4a-111">FTI 印刷可能フォームのカスタマイズされたコンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="01a4a-111">Create customized configurations for FTI printable forms</span></span>
<span data-ttu-id="01a4a-112">印刷可能な FTI フォームのカスタマイズされたソリューションの一部として、ER コンフィギュレーションのセットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-112">As part of your customized solution for printable FTI forms, you must create a set of ER configurations.</span></span>

### <a name="configure-the-er-data-model"></a><span data-ttu-id="01a4a-113">ER データ モデルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="01a4a-113">Configure the ER data model</span></span>
<span data-ttu-id="01a4a-114">アプリケーションには、顧客請求ビジネス ドメインを説明するデータ モデルを含む ER データ モデルのコンフィギュレーションを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-114">Your application must include the ER data model configuration that contains a data model that describes the customer invoicing business domain.</span></span> <span data-ttu-id="01a4a-115">要件として、データ モデルの名前は **CustomersInvoicing** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-115">As a requirement, the name of the data model must be **CustomersInvoicing**.</span></span> <span data-ttu-id="01a4a-116">ER データ モデルを設計する方法の詳細については、[電子申告 (ER) 用にドメイン固有のデータ モデルを設計](tasks/er-design-domain-specific-data-model-2016-11.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01a4a-116">For information about how to design ER data models, see [Design a domain-specific data model for electronic reporting (ER)](tasks/er-design-domain-specific-data-model-2016-11.md).</span></span>

### <a name="configure-the-er-model-mapping"></a><span data-ttu-id="01a4a-117">ER データ マッピングのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="01a4a-117">Configure the ER model mapping</span></span>
<span data-ttu-id="01a4a-118">アプリケーションには、CustomersInvoicing データ モデルの ER モデル マッピングを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-118">Your application must include the ER model mapping for the CustomersInvoicing data model.</span></span> <span data-ttu-id="01a4a-119">モデル マッピングは、ER データ モデル コンフィギュレーションまたは ER モデル マッピング コンフィギュレーションのいずれかにすることができます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-119">The model mapping can be in either the ER data model configuration or the ER model mapping configuration.</span></span> <span data-ttu-id="01a4a-120">ただし、モデル マッピングのルート記述子の名前は **FreeTextInvoice** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-120">However, the name of the root descriptor of the model mapping must be **FreeTextInvoice**.</span></span>

<span data-ttu-id="01a4a-121">マッピングには、次のデータ ソースを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-121">The mapping must contain the following data sources:</span></span>

- <span data-ttu-id="01a4a-122">データ ソース タイプ: **テーブル レコード**</span><span class="sxs-lookup"><span data-stu-id="01a4a-122">Data source type: **Table records**</span></span>

    - <span data-ttu-id="01a4a-123">このデータ ソースには **CustInvoiceJour** という名前を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-123">This data source must be named **CustInvoiceJour**.</span></span>
    - <span data-ttu-id="01a4a-124">CustInvoiceJour アプリケーション テーブルを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-124">It must refer to the CustInvoiceJour application table.</span></span>
    - <span data-ttu-id="01a4a-125">印刷のために選択されている請求書の一覧をアプリケーションから ER モデル マッピングに渡すため、実行時に使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-125">It's used at runtime to pass from the application to the ER model mapping the list of invoices that have been selected for printing.</span></span>

- <span data-ttu-id="01a4a-126">データ ソース タイプ: **オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="01a4a-126">Data source type: **Object**</span></span>

    - <span data-ttu-id="01a4a-127">このデータ ソースには **PrintMgmtPrintSettingDetail** という名前を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-127">This data source must be named **PrintMgmtPrintSettingDetail**.</span></span>
    - <span data-ttu-id="01a4a-128">**PrintMgmtPrintSettingDetail** アプリケーション クラスを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-128">It must refer to the **PrintMgmtPrintSettingDetail** application class.</span></span>
    - <span data-ttu-id="01a4a-129">実行している ER 形式のための印刷管理設定の詳細をアプリケーションから ER モデル マッピングに渡すため、実行時に使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-129">It's used at runtime to pass from the application to the ER model mapping details of the print management settings for the ER format that is running.</span></span>

<span data-ttu-id="01a4a-130">ER フレームワークとのアプリケーション統合の詳細については、アプリケーションのソース コードの**ERPrintMgmtReportFormatSubscriber** クラス (ER アプリケーション スイート統合モデル) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01a4a-130">The details of the application integration with the ER framework can be found in the **ERPrintMgmtReportFormatSubscriber** class (ER Application Suite integration model) in the source code of the application.</span></span>

<span data-ttu-id="01a4a-131">ER モデル マッピングの設計に関する詳細については、[モデル マッピングの定義および電子申告 (ER) のデータ ソースの選択](tasks/er-define-model-mapping-select-data-sources-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01a4a-131">For more information about the design of ER model mappings, see [Define model mapping and select data sources for electronic reporting (ER)](tasks/er-define-model-mapping-select-data-sources-2016-11.md).</span></span>

### <a name="configure-the-er-format"></a><span data-ttu-id="01a4a-132">ER 形式のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="01a4a-132">Configure the ER format</span></span>
<span data-ttu-id="01a4a-133">アプリケーション インスタンスには、FTI フォームを生成するために使用される ER 形式のコンフィギュレーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="01a4a-133">In your application instance, you must have the ER format configuration that will be used to generate FTI forms.</span></span> 

> [!NOTE]
> <span data-ttu-id="01a4a-134">この形式のコンフィギュレーションは CustomersInvoicing データ モデル用に作成され、**FreeTextInvoice** ルート記述子があるモデル マッピングを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-134">This format configuration must be created for the CustomersInvoicing data model, and it must use the model mapping that has the **FreeTextInvoice** root descriptor.</span></span>

<span data-ttu-id="01a4a-135">ER 形式をコンフィギュレーションする方法の詳細については、[電子申告 (ER) 用の形式のコンフィギュレーションの作成](tasks/er-format-configuration-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01a4a-135">For information about how to configure ER formats, see [Create a format configuration for electronic reporting (ER)](tasks/er-format-configuration-2016-11.md).</span></span> <span data-ttu-id="01a4a-136">OpenXML 形式でレポートを生成するために ER 形式を設計する方法の詳細については、[電子申告 (ER) 用に OpenXML 形式でレポートを生成するためのコンフィギュレーションの設計](tasks/er-design-reports-openxml-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01a4a-136">For information about how to design ER formats to generate reports in OpenXML format, see [Design a configuration for generating reports in OpenXML format for electronic reporting (ER)](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="configure-print-management"></a><span data-ttu-id="01a4a-137">印刷管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="01a4a-137">Configure print management</span></span>
<span data-ttu-id="01a4a-138">ER フレームワークを使用して FTI フォームを生成するために、SSRS レポートを割り当てる場合と同じ方法で ER 形式を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-138">To generate FTI forms by using the ER framework, you can assign ER formats in the same way that you assign SSRS reports.</span></span> <span data-ttu-id="01a4a-139">ER 形式とすべての売掛金勘定 FTI を関連付けるには、**売掛金勘定** \> **設定** \> **フォーム** \> **フォームの設定** \> **一般** \> **印刷管理** \> **自由書式の請求書** \> **オリジナル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="01a4a-139">To associate the ER format with all Accounts receivable FTIs, go to **Accounts receivable** \> **Setup** \> **Forms** \> **Form setup** \> **General** \> **Print management** \> **Free text invoice** \> **Original**.</span></span> <span data-ttu-id="01a4a-140">ER 形式と特定の顧客または請求書を関連付けるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="01a4a-140">To associate the ER format with a specific customer or invoice, follow these steps.</span></span>

1. <span data-ttu-id="01a4a-141">**売掛金勘定** \> **請求書** \> **すべての自由書式の請求書**に移動します。</span><span class="sxs-lookup"><span data-stu-id="01a4a-141">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="01a4a-142">ER 形式を関連付ける FTI を選択し、**印刷管理設定**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-142">Select the FTI to associate the ER format with, and open the **Print management setup** page.</span></span>
3. <span data-ttu-id="01a4a-143">処理する請求書のスコープを指定するドキュメント レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="01a4a-143">Select the document level to specify the scope of invoices for processing.</span></span>
4. <span data-ttu-id="01a4a-144">指定されたドキュメント レベルの ER 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="01a4a-144">Select the ER format for the specified document level.</span></span>

![印刷管理設定](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> <span data-ttu-id="01a4a-146">**CustomersInvoicing** データ モデルの **FreeTextInvoice** ルート記述子を使用している ER 形式のみが、選択された形式の**レポート形式の検索**フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-146">Only ER formats that use the **FreeTextInvoice** root descriptor of the **CustomersInvoicing** data model appear in the **Report format lookup** field for the selected format.</span></span>

## <a name="generate-fti-forms"></a><span data-ttu-id="01a4a-147">FTI フォームの生成</span><span class="sxs-lookup"><span data-stu-id="01a4a-147">Generate FTI forms</span></span>
<span data-ttu-id="01a4a-148">FTI フォームは、SSRS レポートが生成される場合と同じ方法で ER フレームワークに生成されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-148">FTI forms are generated in the ER framework in the same way that SSRS reports are generated.</span></span>

<span data-ttu-id="01a4a-149">FTI フォームを生成するために、範囲または選択のいずれかによって請求書を選択できます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-149">To generate FTI forms, you can select invoices either by range or by selection.</span></span> 

![請求書の選択](media/FTIbyGER-InvoiceSelection.png)

![請求書の確認](media/FTIbyGER-InvoiceExcelPreview.png)

<span data-ttu-id="01a4a-152">この方法で FTI フォームを印刷するために ER 形式を使用する場合、既定の ER ファイル出力先が使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-152">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="01a4a-153">出力先は変更できません。</span><span class="sxs-lookup"><span data-stu-id="01a4a-153">You can't change the destination.</span></span> <span data-ttu-id="01a4a-154">ER 形式の ER 出力先をコンフィギュレーションする方法の詳細については、[電子申告の出力先](electronic-reporting-destinations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01a4a-154">For more information about how to configure the ER destinations for ER formats, see [Electronic reporting destinations](electronic-reporting-destinations.md).</span></span>

<span data-ttu-id="01a4a-155">**請求書の印刷**を有効にし、また**印刷管理の出力先の使用**を無効にすることによって、FTI の転記時に FTI フォームを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-155">You can also generate FTI forms when you post an FTI, by turning **Print invoice** on and turning **Use print management destinations** off.</span></span>

> [!NOTE]
> <span data-ttu-id="01a4a-156">この方法で FTI フォームを印刷するために ER 形式を使用する場合、既定の ER ファイル出力先が使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-156">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="01a4a-157">出力先が既にコンフィギュレーションされている場合、実行時に既定の出力先を変更できます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-157">You can change the default destination at runtime if the destination has already been configured.</span></span> <span data-ttu-id="01a4a-158">出力先を変更するには、次のセキュリティ権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="01a4a-158">To change the destination, you must have the following security privilege:</span></span>
>
> - <span data-ttu-id="01a4a-159">**名前:** ERFormatDestinationRuntimeMaintain</span><span class="sxs-lookup"><span data-stu-id="01a4a-159">**Name:** ERFormatDestinationRuntimeMaintain</span></span>
> - <span data-ttu-id="01a4a-160">**ラベル:** 実行時に電子申告形式の出力先を管理</span><span class="sxs-lookup"><span data-stu-id="01a4a-160">**Label:** Maintain electronic reporting format destination during runtime</span></span>

![電子申告の送信先](media/FTIbyGER-ERFileDestinationSetting.png)

![電子申告形式の出力先](media/FTIbyGER-ERFileDestinationUsage.png)

<span data-ttu-id="01a4a-163">ER フレームワークは現在、生成されたドキュメントのために次の出力先をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-163">The ER framework currently supports the following destinations for generated documents:</span></span>

- <span data-ttu-id="01a4a-164">**ダウンロードしたファイル** – 生成されたフォームは、ブラウザーを使用して保存することができるダウンロードとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-164">**Downloaded file** – Generated forms are offered as downloads that you can save by using the browser.</span></span>
- <span data-ttu-id="01a4a-165">**画面** – 生成された FTI フォームを Excel 形式でプレビューするために、Microsoft Office 365 Excel が使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-165">**Screen** – Microsoft Office 365 Excel is used to preview generated FTI forms in Excel format.</span></span>
- <span data-ttu-id="01a4a-166">**SharePoint フォルダー** – 生成されたフォームはドキュメント管理フレームワークの設定に基づいて保管されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-166">**SharePoint folder** – Generated forms are stored based on the settings of the Document management framework.</span></span>
- <span data-ttu-id="01a4a-167">**アプリケーション アーカイブ** – 生成されたフォームは、Microsoft Azure ストレージ内の実行ログ レコードの添付ファイルとして保管されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-167">**Application archive** – Generated forms are stored as attachments of execution log records in the Microsoft Azure Storage.</span></span>
- <span data-ttu-id="01a4a-168">**電子メール** – 生成されたフォームは電子メールの添付ファイルとして送信されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-168">**Email** – Generated forms are sent as email attachments.</span></span>

> [!NOTE]
> <span data-ttu-id="01a4a-169">現在、Dynamics プリンター回覧エージェントを使用する直接印刷はサポートされていないため、プリンターに直接生成された FTI フォームを送信することはできません。</span><span class="sxs-lookup"><span data-stu-id="01a4a-169">You can't send the FTI forms that are generated directly to the printer, because direct printing that uses the Dynamics Printer Routing Agent isn't currently supported.</span></span>

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a><span data-ttu-id="01a4a-170">印刷可能な FTI フォームを生成するためのサンプル ER コンフィギュレーションのダウンロード</span><span class="sxs-lookup"><span data-stu-id="01a4a-170">Download sample ER configurations to generate printable FTI forms</span></span>
<span data-ttu-id="01a4a-171">サンプル ER コンフィギュレーションをダウンロードし、FTI ソリューションのテンプレートとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-171">You can download sample ER configurations to use as a template for your FTI solution.</span></span> <span data-ttu-id="01a4a-172">コンフィギュレーションは、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリに保管されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-172">The configurations are stored in the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="01a4a-173">コンフィギュレーションには次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-173">The configurations include:</span></span>

- <span data-ttu-id="01a4a-174">**顧客請求モデル** コンフィギュレーションには、必要なデータ モデルとモデル マッピングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-174">The **Customer invoicing model** configuration contains the required data model and model mapping.</span></span>
- <span data-ttu-id="01a4a-175">**顧客 FTI レポート (GER)** コンフィギュレーションには、サンプルの形式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-175">The **Customer FTI report (GER)** configuration contains the sample format.</span></span>

> [!NOTE]
> <span data-ttu-id="01a4a-176">これらのコンフィギュレーションは、すべての可能なシナリオを明確にするのに役立つサンプルとして作成されました。</span><span class="sxs-lookup"><span data-stu-id="01a4a-176">These configurations have been created as samples to help clarify possible scenarios.</span></span> <span data-ttu-id="01a4a-177">これらの構成の今後は、この評価と受け取るすべてのフィードバックの結果によって決まります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-177">The future of these configurations depends on the results of this evaluation and any feedback that is received.</span></span>

### <a name="features-that-are-implemented-in-the-sample-er-format"></a><span data-ttu-id="01a4a-178">サンプル ER 形式に実装されている機能</span><span class="sxs-lookup"><span data-stu-id="01a4a-178">Features that are implemented in the sample ER format</span></span>
<span data-ttu-id="01a4a-179">サンプル ER 形式のコンフィギュレーションでは、FTI フォームを生成するためのテンプレートとして Excel ファイルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-179">In the sample ER format configuration, an Excel file is used as a template to generate FTI forms.</span></span>

![形式デザイナー](media/FTIbyGER-ERFormat.png)

<span data-ttu-id="01a4a-181">現在、このサンプル ER 形式では、FTI フォームを生成するために次の機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-181">Currently, this sample ER format supports the following features to generate FTI forms:</span></span>

- <span data-ttu-id="01a4a-182">FTI フォームは、転記された元の請求書およびまだ転記されていない元の請求書の両方に対して生成されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-182">FTI forms are generated for both original invoices that have been posted and original invoices that haven't yet been posted.</span></span> <span data-ttu-id="01a4a-183">修正済請求書および訂正票はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="01a4a-183">Corrected invoices and credit notes aren't supported.</span></span>
- <span data-ttu-id="01a4a-184">FTI フォームは、請求書の言語で生成されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-184">FTI forms are generated in the invoice language.</span></span> <span data-ttu-id="01a4a-185">生成されたフォーム内の値および日付の形式は、ユーザーのクライアント ロケールの設定に基づきます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-185">The format of values and dates in the generated forms is based on the settings of the user's client locale.</span></span>
- <span data-ttu-id="01a4a-186">処理された請求書に明細行が含まれていない場合、生成される請求書にはデータ使用不可能の通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-186">Generated invoices show data unavailability notifications if there are no lines in the invoices that are processed.</span></span>
- <span data-ttu-id="01a4a-187">生成される請求書のヘッダーは、**売掛金勘定パラメーター** ページ上で FTI フォームに対して選択されている用紙の書式に基づきます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-187">Generated invoice headers are based on the paper format that has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="01a4a-188">会社の詳細は、用紙の書式が空白の場合のみ、生成される請求書フォームのヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-188">Company details appear in the header of the generated invoice form only if the paper format is blank.</span></span>
- <span data-ttu-id="01a4a-189">生成される請求書フォームには、**売掛金勘定パラメーター** ページ上で適切なオプションが FTI フォームに対して選択されている場合、会社および顧客の課税控除番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-189">Generated invoice forms show company and customer tax exempt numbers when the appropriate option has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="01a4a-190">生成される請求書の明細行および請求書の合計セクションでは、請求書登録通貨に既定の請求書金額の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="01a4a-190">The generated invoice lines and invoice totals sections show the default invoice's monetary details in the invoice registration currency.</span></span>
- <span data-ttu-id="01a4a-191">生成される請求書の合計セクションには、**売掛金勘定パラメーター** ページ上で**ユーロを表す通貨で金額を印刷**オプションが有効になっている場合、ユーロ通貨と請求書登録通貨で金額の詳細を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-191">The generated invoice totals section can show monetary details in the euro currency and the invoice registration currency when the **Print amount in currency representing the euro** option is enabled on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="01a4a-192">生成される請求書フォームには、**売掛金勘定パラメーター** ページ上の設定に基づいて、利用可能なすべての処理請求書の注記が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-192">Generated invoice forms show any process invoice notes that are available, based on settings on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="01a4a-193">注記は請求書全体と各請求明細行の両方に含められます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-193">Notes are included for both the whole invoice and each invoice line.</span></span>
- <span data-ttu-id="01a4a-194">AR フォームの注記の一覧でコンフィギュレーションされている場合、生成される請求書フォームには顧客 FTI フォームおよび処理中の請求書の言語に対する注記が含められます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-194">Generated invoice forms include notes for the customer FTI form and the processing invoice language when they have been configured in the AR form notes list.</span></span>
- <span data-ttu-id="01a4a-195">印刷管理の設定に応じて、請求書の言語、ER 形式、および FTI ドキュメント スコープに対してコンフィギュレーションされている場合、生成される請求書にはカスタム フッター テキストが含められます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-195">Depending on the Print management settings, generated invoices include custom footer text when it has been configured for the invoice language, the ER format, and the FTI document scope.</span></span>
- <span data-ttu-id="01a4a-196">生成される請求書フォームの合計セクションには、利用可能なすべての現金割引情報が含められます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-196">The totals section of generated invoice forms includes any cash discount information that is available.</span></span>
- <span data-ttu-id="01a4a-197">生成される請求書フォームの支払スケジュールのセクションには、利用可能なすべての支払スケジュールの詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-197">The payment schedule section of generated invoice forms includes any payment schedule details that are available.</span></span>
- <span data-ttu-id="01a4a-198">生成される請求書フォームの利幅セクションには、利用可能なすべての任意の雑費トランザクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-198">The markup section of generated invoice forms includes any charges transactions that are available.</span></span>
- <span data-ttu-id="01a4a-199">**売掛金勘定パラメーター** ページ上の**売上税の仕様**の設定に基づいて、生成される請求書フォームには売上税の詳細が含められます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-199">Generated invoice forms include sales tax details, based on the **Sales tax specification** setting on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="01a4a-200">このセクションでは、請求書登録通貨でのみ表示するか、または請求書登録通貨および会社の会計通貨で同時に表示するか、いずれかの方法で税の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-200">This section can show tax details either in the invoice registration currency only, or in the invoice registration currency and the company accounting currency at the same time.</span></span>
- <span data-ttu-id="01a4a-201">生成される請求書フォームには、口座引落通知の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-201">Generated invoice forms show direct debit notification details.</span></span> <span data-ttu-id="01a4a-202">たとえば、請求書に対して必須の口座引落の委任状 ID を持つ支払方法が選択された場合、請求書の処理がユーロ通貨で登録された場合、および口座引落の委任状 ID が請求書に対して定義された場合に表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-202">For example, they show when the method of payment that has the mandatory direct debit mandate ID was selected for the invoice, when the processing invoice was registered in the euro currency, and when the direct debit mandate ID was defined for the invoice.</span></span>
- <span data-ttu-id="01a4a-203">生成される請求書には、転記された請求書に対して使用可能であるすべての前払の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-203">Generated invoices show any prepayment details that are available for posted invoices.</span></span>
- <span data-ttu-id="01a4a-204">生成される請求書フォームは、電子メールの添付ファイルとして請求書の顧客に送信できます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-204">Generated invoice forms can be sent to an invoice customer as an email attachment.</span></span> <span data-ttu-id="01a4a-205">適切な ER ファイルの出力先は、使用されている ER 形式に対してコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-205">The appropriate ER file destination should be configured for the ER format that is being used.</span></span>

### <a name="countryregion-specific-features"></a><span data-ttu-id="01a4a-206">国/地域固有の機能</span><span class="sxs-lookup"><span data-stu-id="01a4a-206">Country/region-specific features</span></span> 
<span data-ttu-id="01a4a-207">次の国/地域に固有の機能は、固有の要件が ER コンフィギュレーションでどのように処理されるかを示すために、サンプル ER 形式に含められています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-207">The following country/region-specific features are included in the sample ER format to show how specific requirements can be handled in ER configurations.</span></span>

#### <a name="norway"></a><span data-ttu-id="01a4a-208">ノルウェー</span><span class="sxs-lookup"><span data-stu-id="01a4a-208">Norway</span></span>
<span data-ttu-id="01a4a-209">エンタープライズ レジスターの条件は、請求書が次のようにコンフィギュレーションされている法人に対して処理される場合、生成される請求書フォームのヘッダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-209">The Enterprise register term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="01a4a-210">ノルウェー用の国/地域コンテキストが使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-210">The country/region context for Norway is used.</span></span>
- <span data-ttu-id="01a4a-211">**Foretaksregisteret の印刷**パラメータが販売ドキュメントで有効です。</span><span class="sxs-lookup"><span data-stu-id="01a4a-211">The **Print Foretaksregisteret** parameter is active on sales documents.</span></span>

#### <a name="spain"></a><span data-ttu-id="01a4a-212">スペイン</span><span class="sxs-lookup"><span data-stu-id="01a4a-212">Spain</span></span>
<span data-ttu-id="01a4a-213">**現金勘定方法の特別な制度**の条件は、請求書が次のようにコンフィギュレーションされている法人に対して処理される場合、生成される請求書フォームのヘッダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-213">The **Special regime for cash accounting method** term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="01a4a-214">スペイン用の国/地域コンテキストが使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-214">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="01a4a-215">現金勘定方法の特別な制度は請求書の処理日に有効です。</span><span class="sxs-lookup"><span data-stu-id="01a4a-215">The special regime for the cash accounting method is enabled on the invoice processing date.</span></span>

<span data-ttu-id="01a4a-216">現金割引金額および請求明細行の正味金額など、現金割引の詳細が利用可能な場合、次のようにコンフィギュレーションされている法人に対して処理される時、生成される請求書フォームの請求合計のセクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-216">When cash discount details, such as the cash discount amount and invoice line net amount, are available, they are presented in the invoice totals section of the generated invoice form when it has been processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="01a4a-217">スペイン用の国/地域コンテキストが使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-217">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="01a4a-218">請求書のオプション (**一般会計パラメーター** \> **消費税セクション**) で、**請求書に現金割引を適用**が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-218">**Cash discount is applied in the invoice** is turned on in the invoice option (**General ledger parameters** \> **Sales tax section**).</span></span>

#### <a name="italy"></a><span data-ttu-id="01a4a-219">イタリア</span><span class="sxs-lookup"><span data-stu-id="01a4a-219">Italy</span></span>
<span data-ttu-id="01a4a-220">商品割引マークは、イタリア用の国/地域コンテキストを使用してコンフィギュレーションされている法人に対して処理される場合、生成される請求書の請求明細行に含められます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-220">The goods discount mark is included on the invoice lines of the generated invoice when it's being processed for a legal entity that is configured using the country/region context for Italy.</span></span>

#### <a name="finland"></a><span data-ttu-id="01a4a-221">フィンランド</span><span class="sxs-lookup"><span data-stu-id="01a4a-221">Finland</span></span>
<span data-ttu-id="01a4a-222">生成される請求書フォームに加えて、次のように振替送金伝票を生成できます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-222">In addition to the generated invoice form, Giro money transfer slips can be generated as follows:</span></span>

- <span data-ttu-id="01a4a-223">フィンランド用の国/地域コンテキストを使用しており、**振替口座**および**銀行のバーコード**としてマークされている銀行口座を少なくとも 1 つ所有している法人に対して。</span><span class="sxs-lookup"><span data-stu-id="01a4a-223">For the legal entity that uses the country/region context for Finland, and that has at least one bank account that is marked as **Giro account** and **Bank bar code**.</span></span> 
- <span data-ttu-id="01a4a-224">**フィンランド**の関連する支払添付書類に対して必要であるとマークされている請求書に対して。</span><span class="sxs-lookup"><span data-stu-id="01a4a-224">For an invoice that is marked as required for the **Finnish** associated payment attachment.</span></span>

![振替伝票](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> <span data-ttu-id="01a4a-226">サンプル ER 形式は、必要に応じて別のワークシートに振替送金伝票を生成するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-226">The sample ER format has been configured to optionally generate the Giro money transfer slips in the separate worksheet.</span></span>

> [!NOTE]
> <span data-ttu-id="01a4a-227">Excel 形式で生成される請求書フォームをプレビューするローカル コンピューター上でバーコードを生成するために使用するフォントを、まずインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-227">You must first install the font that is used to generate the bar code on the local machine where the generated invoice form in Excel format will be previewed.</span></span>

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a><span data-ttu-id="01a4a-228">サンプル ER 形式を使用した電子メール送信先のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="01a4a-228">Use the sample ER format to configure email destinations</span></span>
<span data-ttu-id="01a4a-229">サンプル ER 形式の次の要素を使用した電子メール送信先のコンフィギュレーション:</span><span class="sxs-lookup"><span data-stu-id="01a4a-229">Use the following elements of the sample ER format to configure email destinations:</span></span>

- <span data-ttu-id="01a4a-230">顧客の連絡先の電子メール アドレスは、次の ER 式からアクセスできます: **model.InvoiceBase.Contact.ElectronicMail**。</span><span class="sxs-lookup"><span data-stu-id="01a4a-230">The email address of a customer contact can be accessed through the following ER expression: **model.InvoiceBase.Contact.ElectronicMail**.</span></span>
- <span data-ttu-id="01a4a-231">電子メールの件名のテキストは、次の ER 式からアクセスできます: **Emailing.TxtToUse.Subject**。</span><span class="sxs-lookup"><span data-stu-id="01a4a-231">The email subject text can be accessed through the following ER expression: **Emailing.TxtToUse.Subject**.</span></span>
- <span data-ttu-id="01a4a-232">電子メールの本文のテキストは、次の ER 式からアクセスできます: **Emailing.TxtToUse.Body**。</span><span class="sxs-lookup"><span data-stu-id="01a4a-232">The email body text can be accessed through the following ER expression: **Emailing.TxtToUse.Body**.</span></span>

![宛先設定](media/FTIbyGER-ERFileDestinationSettingEmail.png)

<span data-ttu-id="01a4a-234">電子メールの件名と本文の既定のテキストは、サンプル ER 形式で定義されています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-234">The default text of the email's subject and body is defined in the sample ER format.</span></span> <span data-ttu-id="01a4a-235">言語は形式のラベルによって異なります。</span><span class="sxs-lookup"><span data-stu-id="01a4a-235">The language depends on the format's labels.</span></span> <span data-ttu-id="01a4a-236">事前定義された **ERFTITMP** ID を持つ組織電子メールのカスタム テンプレートが追加されていない場合、既定のテキストが電子メールに使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-236">This default text will be used for emails if a custom organization email template that has the predefined **ERFTITMP** ID hasn't been added.</span></span>

> [!NOTE]
> <span data-ttu-id="01a4a-237">**ERFTITMP** 電子メール テンプレート ID がサンプル ER 形式で定義されています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-237">The **ERFTITMP** email template ID has been defined in the sample ER format.</span></span> <span data-ttu-id="01a4a-238">必要に応じて、このサンプル形式から作成される新しい ER 形式で変更することができます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-238">It can be changed as required in a new ER format that is created from this sample format.</span></span>

<span data-ttu-id="01a4a-239">事前定義された **ERFTITMP** ID を持つ組織の電子メールが、請求書を処理する法人に対して追加されている場合、電子メールの件名および本文のテキストのテンプレートが電子メールを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-239">If the organization email template that has the predefined **ERFTITMP** ID has been added for the legal entity that you're processing the invoice for, the template for the email subject and body text will be used to generate the email.</span></span> 

![組織の電子メール テンプレート](media/FTIbyGER-EmailTemplate.png)

![電子メール テンプレートのアップロード](media/FTIbyGER-EmailTemplateBody.png)

<span data-ttu-id="01a4a-242">サンプル ER 形式の ER 式 **Emailing.TxtToUse.Subject** は、すべてのプレースホルダー %1 を請求書処理 ID によって置換するようコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-242">The **Emailing.TxtToUse.Subject** ER expression of the sample ER format is configured to replace any occurrences of the placeholder %1 by the processing invoice ID.</span></span>

<span data-ttu-id="01a4a-243">サンプル形式の **Emailing.TxtToUse.Body** 式は、プレースホルダーに対して次の代用のためにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="01a4a-243">The **Emailing.TxtToUse.Body** expression of the sample format is configured for the following substitutions for placeholders:</span></span>

- <span data-ttu-id="01a4a-244">「%1」は顧客の連絡担当者の名前に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-244">"%1" is replaced with the name of the customer's contact person.</span></span>
- <span data-ttu-id="01a4a-245">「%2」は会社名に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-245">"%2" is replaced with the company name.</span></span>
- <span data-ttu-id="01a4a-246">「%3」は顧客名に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-246">"%3" is replaced with the customer name.</span></span>
- <span data-ttu-id="01a4a-247">「%4」は会社の連絡担当者の名前に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-247">"%4" is replaced with the name of the company's contact person.</span></span>
- <span data-ttu-id="01a4a-248">「%5」は会社の連絡担当者の肩書きに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-248">"%5" is replaced with the job title of the company's contact person.</span></span>
- <span data-ttu-id="01a4a-249">「%6」は会社の連絡担当者の電子メール アドレスに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="01a4a-249">"%6" is replaced with the email address of the company's contact person.</span></span>

![電子メール](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a><span data-ttu-id="01a4a-251">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="01a4a-251">Additional resources</span></span>
[<span data-ttu-id="01a4a-252">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="01a4a-252">Electronic reporting overview</span></span>](general-electronic-reporting.md)
