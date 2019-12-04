---
title: ビジネス ドキュメント管理の概要
description: このトピックでは、ER フレームワークのビジネス ドキュメント管理機能を使用する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a2fa6a7f6efef05862a3727a80122c22d591487
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824523"
---
# <a name="business-document-management-overview"></a><span data-ttu-id="8abae-103">ビジネス ドキュメント管理の概要</span><span class="sxs-lookup"><span data-stu-id="8abae-103">Business document management overview</span></span>

<span data-ttu-id="8abae-104">ビジネス ユーザーは、[電子申告 (ER) の概要](general-electronic-reporting.md) を使用し、さまざまな国 / 地域の法的要件に従って発信ドキュメントの形式を構成できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-104">Business users use the [Electronic reporting (ER) overview](general-electronic-reporting.md) to configure formats for outbound documents in accordance with the legal requirements of various countries/regions.</span></span> <span data-ttu-id="8abae-105">また、生成されるドキュメントに配置されるアプリケーション データを指定するため、データフローを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="8abae-105">Users can also define the dataflow to specify what application data is placed in generated documents.</span></span> <span data-ttu-id="8abae-106">ER フレームワークは、定義済みテンプレートを使用して、Microsoft Office 形式 (Excel Workbooks または Word ドキュメント) で発信ドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="8abae-106">The ER framework generates outbound documents in Microsoft Office formats (Excel workbooks or Word documents) by using predefined templates.</span></span> <span data-ttu-id="8abae-107">必要なドキュメントが生成されるときに、構成されたデータフローに従って、テンプレートに必要なデータが設定されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-107">The templates are populated with required data in accordance to configured dataflow while required documents are generated.</span></span> <span data-ttu-id="8abae-108">特定の発信ドキュメントを生成するために、ER ソリューションの一部として、構成された各形式を公開できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-108">Each configured format can be published as part of an ER solution to generate specific outbound documents.</span></span> <span data-ttu-id="8abae-109">これは、異なる発信ドキュメントを生成するために使用できるテンプレートを含める ER 形式コンフィギュレーションによって、表示されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-109">This is represented by an ER format configuration that can contain templates you can use to generate different outbound documents.</span></span> <span data-ttu-id="8abae-110">ビジネス ユーザーは、このフレームワークを使用して、必要なビジネス ドキュメントを管理できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-110">Business users can use this framework to manage required business documents.</span></span>

<span data-ttu-id="8abae-111">**ビジネス ドキュメント管理**は、ER フレームワークを基盤に構築されており、ビジネス ユーザーが Microsoft Office 365 サービスまたは適切な Microsoft Office デスクトップ アプリケーションを使用して、ビジネス ドキュメント テンプレートを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="8abae-111">**Business document management** is built on top of the ER framework and enables business users to edit business document templates by using Microsoft Office 365 service or appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="8abae-112">ドキュメントを編集する際には、ビジネス ドキュメントのデザインを変更したり、ソース コードの変更および新しい配置無しで、追加データ用のプレス ホルダーを追加したりします。</span><span class="sxs-lookup"><span data-stu-id="8abae-112">Edits to the documents might include changing business document designs and adding placeholders for additional data without source code changes and new deployments.</span></span> <span data-ttu-id="8abae-113">ER フレームワークには、ビジネス ドキュメントのテンプレートを更新するために必要な知識がありません。</span><span class="sxs-lookup"><span data-stu-id="8abae-113">No knowledge of the ER framework is required to update templates of business documents.</span></span>

> [!NOTE]
> <span data-ttu-id="8abae-114">ビジネス ドキュメント管理を使用すると、注文書や請求書などのビジネス ドキュメントの作成に使用されるテンプレートを変更できます。テンプレートが変更され新しいバージョンが発行されている間に、このバージョンは必要なビジネス ドキュメントの生成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-114">Be aware that Business document management allows you to modify templates that are used to produce business documents such as orders, invoices, etc. While a template has been modified and a new version of it has been published, this version is used to generate required business documents.</span></span> <span data-ttu-id="8abae-115">ビジネス ドキュメント管理を使用して、既に生成されたビジネス ドキュメントを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="8abae-115">Business document management cannot be used to modify already generated business documents.</span></span>

## <a name="supported-deployments"></a><span data-ttu-id="8abae-116">サポートされている配置</span><span class="sxs-lookup"><span data-stu-id="8abae-116">Supported deployments</span></span>

<span data-ttu-id="8abae-117">現在、ビジネス ドキュメント管理の機能はクラウド配置に対してのみ実装されています。</span><span class="sxs-lookup"><span data-stu-id="8abae-117">Currently, the Business document management feature is implemented only for cloud deployments.</span></span> <span data-ttu-id="8abae-118">この機能が、オンプレミス配置にとって重要な場合は、[アイデア](https://experience.dynamics.com/ideas/) サイトからフィードバックを提供し通知します。</span><span class="sxs-lookup"><span data-stu-id="8abae-118">If this feature is critical to your on-premises deployment, let us know by providing feedback on the [Ideas](https://experience.dynamics.com/ideas/) site.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="8abae-119">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="8abae-119">Supported Microsoft Office applications</span></span>

<span data-ttu-id="8abae-120">Microsoft Office のデスクトップ アプリケーションを使用して、Excel または Word 形式でテンプレートを編集するビジネス ドキュメント管理を使うには、Microsoft Office の 2010 またはそれ以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="8abae-120">To use Business document management for editing templates in Excel or Word formats by using Microsoft Office desktop applications, you must have Microsoft Office 2010 or later installed.</span></span> <span data-ttu-id="8abae-121">これはクラウドおよびオンプレミス配置でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8abae-121">This is supported in cloud and on-premises deployment.</span></span>

## <a name="business-document-availability"></a><span data-ttu-id="8abae-122">ビジネス ドキュメントの使用可能性</span><span class="sxs-lookup"><span data-stu-id="8abae-122">Business document availability</span></span>

<span data-ttu-id="8abae-123">次のレポートは、Excel ベースのテンプレートと共に、パブリック プレビューのリリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-123">The following reports, with Excel-based templates, will available with the release of the public preview:</span></span>

<span data-ttu-id="8abae-124">**売掛金勘定** (2019 年 8 月)</span><span class="sxs-lookup"><span data-stu-id="8abae-124">**Accounts receivable** (August 2019)</span></span>

- <span data-ttu-id="8abae-125">販売前請求書</span><span class="sxs-lookup"><span data-stu-id="8abae-125">Sales advance invoice</span></span>
- <span data-ttu-id="8abae-126">販売注文梱包明細票</span><span class="sxs-lookup"><span data-stu-id="8abae-126">Sales order packing slip</span></span>

<span data-ttu-id="8abae-127">**買掛金勘定** (2019 年 8 月)</span><span class="sxs-lookup"><span data-stu-id="8abae-127">**Accounts payable** (August 2019)</span></span>

- <span data-ttu-id="8abae-128">仕入事前請求書</span><span class="sxs-lookup"><span data-stu-id="8abae-128">Purchase advance invoice</span></span>
- <span data-ttu-id="8abae-129">発注書</span><span class="sxs-lookup"><span data-stu-id="8abae-129">Purchase order</span></span>
- <span data-ttu-id="8abae-130">発注書の梱包明細</span><span class="sxs-lookup"><span data-stu-id="8abae-130">Purchase order packing slip</span></span>

<span data-ttu-id="8abae-131">さらに多くのレポートが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="8abae-131">More reports will become available.</span></span> <span data-ttu-id="8abae-132">追加のレポートに関する特別な通知は、個別に送信されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-132">Special notifications about additional reports will be sent separately.</span></span> 

<span data-ttu-id="8abae-133">2019 年 10 月のリリースに予定されているすべてのレポートの全一覧は、[Word および Excel のコンフィギュレーション可能なビジネス ドキュメント レポート](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details) に表示されています。</span><span class="sxs-lookup"><span data-stu-id="8abae-133">A complete list of all the reports planned for the October 2019 release can be found in [Configurable business documents reporting in Word and Excel](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).</span></span> <span data-ttu-id="8abae-134">この機能の詳細を知るには、このトピックの例を実行します。</span><span class="sxs-lookup"><span data-stu-id="8abae-134">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="configure-er-parameters"></a><span data-ttu-id="8abae-135">ER パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8abae-135">Configure ER parameters</span></span>

<span data-ttu-id="8abae-136">ビジネス ドキュメント管理は ER フレームワーク上に構築されているので、ER パラメータをコンフィギュレーションして、ビジネス ドキュメント管理の操作を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8abae-136">Because Business document management is built on top of the ER framework, you must configure the ER parameters to start working with Business document management.</span></span> <span data-ttu-id="8abae-137">これを行うには、[電子申告 (ER) フレームワークのコンフィギュレーション](electronic-reporting-er-configure-parameters.md) で説明されているように、ER パラメーターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8abae-137">To do this, you need to set up the ER parameters as described in [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md).</span></span> <span data-ttu-id="8abae-138">[コンフィギュレーション プロバイダーの作成および有効としてマーク](tasks/er-configuration-provider-mark-it-active-2016-11.md) で説明されているように、新しいコンフィギュレーション プロバイダーを追加する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="8abae-138">You also need to add a new configuration provider as described in [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

![ER ワークスペース](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a><span data-ttu-id="8abae-140">ER ソリューションのインポート</span><span class="sxs-lookup"><span data-stu-id="8abae-140">Import ER solutions</span></span>

<span data-ttu-id="8abae-141">この手順の例では、サンプル ER コンフィギュレーションが使用されています。</span><span class="sxs-lookup"><span data-stu-id="8abae-141">Sample ER configurations are used in the example of this procedure.</span></span> <span data-ttu-id="8abae-142">ビジネス ドキュメント管理を使用して編集できるビジネス ドキュメント テンプレートを含む ER コンフィギュレーションを、現在の Dynamics 365 Finance インスタンスにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8abae-142">You must import, into your current instance of Dynamics 365 Finance, the ER configurations that contain the business document templates that can be edited by using Business document management.</span></span> <span data-ttu-id="8abae-143">この手順を実行するには、次のファイルをダウンロードしてローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="8abae-143">Download, and then locally store the following files to complete this procedure.</span></span>

<span data-ttu-id="8abae-144">**サンプル ER 顧客請求ソリューション**</span><span class="sxs-lookup"><span data-stu-id="8abae-144">**Sample ER customer invoicing solution**</span></span>

| <span data-ttu-id="8abae-145">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8abae-145">**File**</span></span>                                  | <span data-ttu-id="8abae-146">**コンテンツ**</span><span class="sxs-lookup"><span data-stu-id="8abae-146">**Content**</span></span>                                |
|-------------------------------------------|--------------------------------------------|
| <span data-ttu-id="8abae-147">Customer invoicing model.version.2.xml</span><span class="sxs-lookup"><span data-stu-id="8abae-147">Customer invoicing model.version.2.xml</span></span>    | [<span data-ttu-id="8abae-148">ER データ モデル構成</span><span class="sxs-lookup"><span data-stu-id="8abae-148">ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="8abae-149">Customer FTI report (GER).version.2.3.xml</span><span class="sxs-lookup"><span data-stu-id="8abae-149">Customer FTI report (GER).version.2.3.xml</span></span> | [<span data-ttu-id="8abae-150">自由書式の請求書 ER 形式コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8abae-150">Free text invoice ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="8abae-151">**サンプル ER 支払 チェック ソリューション**</span><span class="sxs-lookup"><span data-stu-id="8abae-151">**Sample ER payment checks solution**</span></span>

| <span data-ttu-id="8abae-152">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8abae-152">**File**</span></span>                                  | <span data-ttu-id="8abae-153">**コンテンツ**</span><span class="sxs-lookup"><span data-stu-id="8abae-153">**Content**</span></span>                                |
|-------------------------------------------|--------------------------------------------|
| <span data-ttu-id="8abae-154">Model for cheques.version.10.xml</span><span class="sxs-lookup"><span data-stu-id="8abae-154">Model for cheques.version.10.xml</span></span>          | [<span data-ttu-id="8abae-155">ER データ モデル構成</span><span class="sxs-lookup"><span data-stu-id="8abae-155">ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="8abae-156">Cheques printing format.version.10.9.xml</span><span class="sxs-lookup"><span data-stu-id="8abae-156">Cheques printing format.version.10.9.xml</span></span>  | [<span data-ttu-id="8abae-157">支払小切手 ER 形式コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8abae-157">Payment cheque ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="8abae-158">**サンプル ER 対外取引ソリューション**</span><span class="sxs-lookup"><span data-stu-id="8abae-158">**Sample ER foreign trade solution**</span></span>

| <span data-ttu-id="8abae-159">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8abae-159">**File**</span></span>                                  | <span data-ttu-id="8abae-160">**コンテンツ**</span><span class="sxs-lookup"><span data-stu-id="8abae-160">**Content**</span></span>                                |
|-------------------------------------------|--------------------------------------------|
| <span data-ttu-id="8abae-161">Intrastat model.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="8abae-161">Intrastat model.version.1.xml</span></span>             | [<span data-ttu-id="8abae-162">ER データ モデル構成</span><span class="sxs-lookup"><span data-stu-id="8abae-162">ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="8abae-163">Intrastat report.version.1.9.xml</span><span class="sxs-lookup"><span data-stu-id="8abae-163">Intrastat report.version.1.9.xml</span></span>          | [<span data-ttu-id="8abae-164">イントラスタット管理レポート ER 形式コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8abae-164">Intrastat control report ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="8abae-165">各ファイルをインポートするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="8abae-165">Use the following procedure to import each file.</span></span> <span data-ttu-id="8abae-166">対応する ER *形式*コンフィギュレーションをインポートする前に、上のテーブルにある各 ER ソリューションの ER *データ モデル*コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="8abae-166">Import the ER *data model* configuration of each ER solution in the tables above before you import the corresponding ER *format* configuration.</span></span>

1. <span data-ttu-id="8abae-167">**組織管理** \> **電子申告** \> **コンフィギュレーション**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8abae-167">Open the **Organization administration** \> **Electronic reporting** \> **Configurations** page.</span></span>
2. <span data-ttu-id="8abae-168">ページ上部で、**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-168">On the top of the page, select **Exchange**.</span></span>
3. <span data-ttu-id="8abae-169">**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-169">Select **Load from XML file**.</span></span>
4. <span data-ttu-id="8abae-170">**参照**を選択して、必要な XML ファイルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="8abae-170">Select **Browse** to load the required XML file.</span></span>
5. <span data-ttu-id="8abae-171">**OK** を選択して、コンフィギュレーションのインポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-171">Select **OK** to confirm configuration’s import.</span></span>

![ER コンフィギュレーション ページ](./media/BDM-Overview-ERSolutions.png)


<span data-ttu-id="8abae-173">また、正式に公開された ER 形式コンフィギュレーションを Microsoft Dynamics Lifecycle サービス (LCS) からインポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="8abae-173">Alternatively, you can import the officially published ER format configurations from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="8abae-174">たとえば、この手順を実行するには、最新バージョンの**自由書式の請求書 (Excel)** ER 形式コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="8abae-174">For example, to complete this procedure you can import the latest version of the **Free text invoice (Excel)** ER format configuration.</span></span> <span data-ttu-id="8abae-175">対応する ER データ モデルと ER モデル マッピングのコンフィギュレーションが自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="8abae-175">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

![LCS 共有資産ライブラリのコンテンツ ページ](./media/BDM-Overview-SharedAssetLibrary.png)

<span data-ttu-id="8abae-177">ER コンフィギュレーションのインポートの詳細については、[ER コンフィギュレーション ライフサイクルの管理](general-electronic-reporting-manage-configuration-lifecycle.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8abae-177">For more information about importing ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>


## <a name="enable-business-document-management"></a><span data-ttu-id="8abae-178">ビジネス ドキュメント管理の有効</span><span class="sxs-lookup"><span data-stu-id="8abae-178">Enable Business document management</span></span>

<span data-ttu-id="8abae-179">ビジネス ドキュメント管理を開始するには、**機能管理**ワークスペースを開いて、**ビジネス ドキュメント管理**機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8abae-179">To start Business document management, you need to open the **Feature management** workspace and enable the **Business document management** feature.</span></span>

<span data-ttu-id="8abae-180">すべての法人に対してビジネス ドキュメント管理の機能を有効にするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="8abae-180">Use the following procedure to enable Business document management functionality for all legal entities.</span></span>

1. <span data-ttu-id="8abae-181">**機能管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="8abae-181">Open the **Feature management** workspace.</span></span>
2. <span data-ttu-id="8abae-182">**新規**タブで、一覧から**ビジネス ドキュメント管理**の機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-182">On the **New** tab, select the **Business document management** feature in the list.</span></span>
3. <span data-ttu-id="8abae-183">**直ちに有効化**を選択し、選択した機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="8abae-183">Select **Enable now** to turn on the selected feature.</span></span>
4. <span data-ttu-id="8abae-184">ページを更新して、新しい機能にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8abae-184">Refresh the page to access the new feature.</span></span>

>[!NOTE]
> <span data-ttu-id="8abae-185">また、新しいビジネス ドキュメント管理インターフェイスを使用するために、**ビジネス ドキュメント管理の Office 同様の UI エクスペリエンス**を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8abae-185">Also you need to enable **Office-like UI experience for Business document management** for using new business document management interface</span></span>

![機能管理ワークスペース](./media/BDM-Overview-FMEnabling.png)

<span data-ttu-id="8abae-187">新規機能の有効化についての詳細は、[機能管理の概要](../../fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8abae-187">For more information about activating new features, see [Feature management overview](../../fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-parameters"></a><span data-ttu-id="8abae-188">パラメータのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8abae-188">Configure parameters</span></span>

<span data-ttu-id="8abae-189">次のセクションの情報を使用して、ビジネス ドキュメント管理の基本パラメータを設定します。</span><span class="sxs-lookup"><span data-stu-id="8abae-189">Use the information in the following sections to set up the basic parameters for Business document management.</span></span>

### <a name="prerequisites-for-parameter-setup"></a><span data-ttu-id="8abae-190">パラメーター セットアップの前提条件</span><span class="sxs-lookup"><span data-stu-id="8abae-190">Prerequisites for parameter setup</span></span>
<span data-ttu-id="8abae-191">ビジネス ドキュメント管理を設定する前に、ドキュメント管理のフレームワークで必要なドキュメント タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8abae-191">Before you can set up Business document management, you must set up the required document type in the Document management framework.</span></span> <span data-ttu-id="8abae-192">このドキュメント タイプは、ER レポート用のテンプレートとして使用される、Office 形式 (Excel および Word) のドキュメントの一時的な保管場所を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-192">This document type is used to specify a temporary storage of documents in Office formats (Excel and Word) that are used as templates for ER reports.</span></span> <span data-ttu-id="8abae-193">一時保管テンプレートは、Office デスクトップ アプリケーションを使用して編集できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-193">The temporary storage template can be edited by using the Office desktop applications.</span></span>

<span data-ttu-id="8abae-194">このドキュメント タイプについては、次の属性値を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8abae-194">For this document type, the following attribute values must be selected.</span></span>

| <span data-ttu-id="8abae-195">**属性名**</span><span class="sxs-lookup"><span data-stu-id="8abae-195">**Attribute name**</span></span>  | <span data-ttu-id="8abae-196">**属性値**</span><span class="sxs-lookup"><span data-stu-id="8abae-196">**Attribute value**</span></span>   |
|---------------------|-----------------------|
| <span data-ttu-id="8abae-197">クラス</span><span class="sxs-lookup"><span data-stu-id="8abae-197">Class</span></span>               | <span data-ttu-id="8abae-198">ファイルの添付</span><span class="sxs-lookup"><span data-stu-id="8abae-198">Attach file</span></span>           |
| <span data-ttu-id="8abae-199">グループ化</span><span class="sxs-lookup"><span data-stu-id="8abae-199">Group</span></span>               | <span data-ttu-id="8abae-200">ファイル</span><span class="sxs-lookup"><span data-stu-id="8abae-200">File</span></span>                  |
| <span data-ttu-id="8abae-201">保管場所</span><span class="sxs-lookup"><span data-stu-id="8abae-201">Location</span></span>            | <span data-ttu-id="8abae-202">SharePoint</span><span class="sxs-lookup"><span data-stu-id="8abae-202">SharePoint</span></span>            |

<span data-ttu-id="8abae-203">必要なドキュメント管理パラメータおよびドキュメント タイプの設定方法については、[ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8abae-203">For information about how to set up the required document management parameters and document types, see [Configure document management](../../fin-ops/organization-administration/configure-document-management.md).</span></span>

![ドキュメント管理のドキュメント タイプを設定](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><span data-ttu-id="8abae-205">パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="8abae-205">Set up parameters</span></span>

<span data-ttu-id="8abae-206">基本ビジネス ドキュメント管理パラメータは、**ビジネス ドキュメント パラメーター**ページで設定できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-206">Basic Business document management parameters can be set up on the **Business document parameters** page.</span></span> <span data-ttu-id="8abae-207">特定のユーザーのみがページにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8abae-207">Only specific users can access the page.</span></span> <span data-ttu-id="8abae-208">これには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8abae-208">This includes:</span></span>

- <span data-ttu-id="8abae-209">**システム管理者**ロールに割り当てられるユーザー。</span><span class="sxs-lookup"><span data-stu-id="8abae-209">Users who are assigned to the **System administrator** role.</span></span>
- <span data-ttu-id="8abae-210">職務権限を実行するようコンフィギュレーションされているロールに割り当てられているユーザー、**ビジネス ドキュメント パラメーターを維持** (AOT 名 **ERBDMaintainParameters**)。</span><span class="sxs-lookup"><span data-stu-id="8abae-210">Users who are assigned to any role that is configured to perform the duty, **Maintain Business document management parameters** (AOT name **ERBDMaintainParameters**).</span></span>

<span data-ttu-id="8abae-211">すべての法人に対して基本パラメーターを設定するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="8abae-211">Use the following procedure to set up the basic parameters for all legal entities.</span></span>

1. <span data-ttu-id="8abae-212">**ビジネス ドキュメント パラメーター** ページへのアクセス権を持つユーザーとして、ログインします。</span><span class="sxs-lookup"><span data-stu-id="8abae-212">Sign in as a user with access to the **Business document parameters** page.</span></span>
2. <span data-ttu-id="8abae-213">**組織管理** \> **電子レポート** \> **ビジネス ドキュメント管理** \> **ビジネス ドキュメント パラメーター**の順で移動します。</span><span class="sxs-lookup"><span data-stu-id="8abae-213">Go to **Organization administration** \> **Electronic reporting** \> **Business document management** \> **Business document parameters**.</span></span>
3.  <span data-ttu-id="8abae-214">**ビジネス ドキュメント パラメーター**ページの**添付ファイル**タブから、**SharePoint ドキュメント タイプ**フィールドで、Office デスクトップ アプリケーションを使用して編集する間に、Office 形式のテンプレートを一時的に保存する際に使用するドキュメント タイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="8abae-214">On the **Business document parameters** page, on the **Attachments** tab, in the **SharePoint document type** field, define the document type that should be used to temporarily store templates in Office formats while they are edited using the Office desktop applications.</span></span> 

> [!NOTE]
> <span data-ttu-id="8abae-215">このパラメーターでは、SharePoint 場所を使用してコンフィギュレーションされているタイプのドキュメントのみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-215">Only document types that are configured using a SharePoint location are available for this parameter.</span></span>

![ビジネス ドキュメント管理パラメーターの設定](./media/BDM-Overview-BDMSetting.png)

<span data-ttu-id="8abae-217">選択したドキュメント タイプは会社固有であり、選択したドキュメント タイプがコンフィギュレーションされている会社のビジネス ドキュメント管理をユーザーが使用する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-217">The selected document type is company-specific and will be used when the user is working with Business document management in the company for which the selected document type is configured.</span></span> <span data-ttu-id="8abae-218">ユーザーがもう一つの会社のビジネス ドキュメント管理を使用している際、この会社にコンフィギュレーションされていない場合は、選択された同じドキュメント タイプが使われます。</span><span class="sxs-lookup"><span data-stu-id="8abae-218">When the user is working with Business document management in another company, the same selected document type will be used if one has not been configured for this company.</span></span> <span data-ttu-id="8abae-219">ドキュメント タイプが構成されている際、**SharePoint ドキュメント**タイプ フィールドで選択されたものの代わりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-219">When a document type has been configured, it will be used instead of the one selected in the **SharePoint document type** field.</span></span>

## <a name="configure-access-permissions"></a><span data-ttu-id="8abae-220">アクセス許可のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8abae-220">Configure access permissions</span></span>

<span data-ttu-id="8abae-221">既定では、ビジネス ドキュメント管理のアクセス許可が有効になっていない場合、ビジネス ドキュメント管理のワークスペースへのアクセス権を持つすべてのユーザーには、使用可能な ER ソリューション テンプレートがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-221">By default, when access to Business document management permissions is not enabled, every user with access to the Business document management workspace will see all of the ER solution templates that are available.</span></span> <span data-ttu-id="8abae-222">ビジネス ドキュメント管理のワークスペースには、**ビジネス ドキュメント タイプ**タグによってマークされた ER 形式コンフィギュレーションに存在するテンプレートのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-222">The Business document management workspace will show only those templates that reside in ER format configurations and that are marked by a **Business document type** tag.</span></span>

![ER コンフィギュレーション ページ](./media/BDM-Overview-ERFormatTags.png)

<span data-ttu-id="8abae-224">ビジネス ドキュメント管理のワークスペースで使用できるテンプレートの一覧は、アクセス許可をコンフィギュレーションすることによって制限できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-224">The list of templates available in the Business document management workspace can be restricted by configuring access permissions.</span></span> <span data-ttu-id="8abae-225">異なるテンプレートがさまざまなビジネス ドメイン (機能領域) のビジネス ドキュメントを作成するため使用されることは重要で、特定のユーザーがビジネス ドキュメント管理のワークスペースで編集するために別のテンプレートにアクセスできるように許可します。</span><span class="sxs-lookup"><span data-stu-id="8abae-225">This may be important when different templates are used to produce business documents for different business domains (functional areas), and you want to allow specific users access to different templates for editing in the Business document management workspace.</span></span>

<span data-ttu-id="8abae-226">ビジネス ドキュメント管理のアクセス許可は、**アクセス許可のコンフィギュレーター**に対して設定できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-226">Business document management access permissions can be set on the **Configurator of access permissions**.</span></span> <span data-ttu-id="8abae-227">次のユーザーのみがページにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8abae-227">Only the following users can access the page:</span></span>

- <span data-ttu-id="8abae-228">**システム管理者**ロールに割り当てられるユーザー。</span><span class="sxs-lookup"><span data-stu-id="8abae-228">Users assigned to the **System administrator** role.</span></span>
- <span data-ttu-id="8abae-229">職務権限を実行するようにコンフィギュレーションされている他のロールに割り当てられたユーザー、**編集用にビジネス ドキュメント テンプレートにアクセスするよう許可をコンフィギュレーション** (AOT 名 **ERBDTemplatesSecurity**)。</span><span class="sxs-lookup"><span data-stu-id="8abae-229">Users assigned to any other role that is configured to perform the duty, **Configure permissions to access Business document templates for editing** (AOT name **ERBDTemplatesSecurity**).</span></span>

<span data-ttu-id="8abae-230">すべての法人に対してビジネス ドキュメント管理の許可のアクセス設定をするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="8abae-230">Use the following procedure to set up the access Business document management permissions for all legal entities.</span></span>

1. <span data-ttu-id="8abae-231">**アクセス許可のコンフィギュレーター** ページへのアクセス権を持つユーザーとして、ログインします。</span><span class="sxs-lookup"><span data-stu-id="8abae-231">Sign in as a user with access to the **Configurator of access permissions** page.</span></span>
2. <span data-ttu-id="8abae-232">**組織管理** \> **電子レポート** \> **ビジネス ドキュメント管理** \> **アクセス許可の管理**の順で移動します。</span><span class="sxs-lookup"><span data-stu-id="8abae-232">Go to **Organization administration** \> **Electronic reporting** \> **Business document management** \> **Manage access permissions**.</span></span>

    <span data-ttu-id="8abae-233">ビジネス ドキュメント管理のアクセス許可の使用が現在有効になっていないことを知らせる通知に、注意してください。</span><span class="sxs-lookup"><span data-stu-id="8abae-233">Pay attention to the notification informing you that the usage of access permissions for Business document management is currently not enabled.</span></span>

    ![ビジネス ドキュメント管理のアクセス許可ページのコンフィギュレーター](./media/BDM-Overview-TemplatesAccess1.png)

    <span data-ttu-id="8abae-235">この設定では、**ビジネス ドキュメント テンプレートの管理** (AOT 名 **ERBDManageTemplates**) の職務権限を実行するようにコンフィギュレーションされているセキュリティ ロールに割り当てられているすべてのユーザーが、ビジネス ドキュメント管理のワークスペースを開くことができます。そして、使用できるすべてのテンプレートを編集できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-235">With this setting, every user assigned to any security role that is configured to perform the **Manage Business document templates** (AOT name **ERBDManageTemplates**) duty is able to open the Business document management workspace and can edit any template that is available.</span></span>

    <span data-ttu-id="8abae-236">次の図は、**売掛金管理係**ロールに割り当てられたユーザーのビジネス ドキュメント管理のワークスペースで使用できるものを示しています。</span><span class="sxs-lookup"><span data-stu-id="8abae-236">The following graphic shows what is available in the Business document management workspace for users assigned to the **Accounts receivable clerk** role.</span></span> <span data-ttu-id="8abae-237">現在のアクセス許可の設定を使用すると、ユーザーは、請求、規制上のレポート、および支払など、さまざまな機能領域からビジネス ドキュメント テンプレートを編集できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-237">With the current access permissions setting, the user can edit business document templates from different functional areas including invoicing, regulatory reporting, and payments.</span></span>

    ![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM-Overview-TemplatesForAlice1.png)

3. <span data-ttu-id="8abae-239">**アクセス許可のコンフィギュレーター**ページで、**アクセス許可の設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-239">On the **Configurator of access permissions** page, select **Access permissions setting**.</span></span>
4. <span data-ttu-id="8abae-240">**テンプレートを編集するためのアクセス許可を設定**ダイアログ ボックスで、**コンフィギュレーションされたアクセス許可の適用**オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="8abae-240">In the **Settings of access permissions to edit templates** dialog box, enable the **Apply configured access permissions** option.</span></span>
5. <span data-ttu-id="8abae-241">**OK** を選択して、ビジネス ドキュメント管理のアクセス権が有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-241">Select **OK** to confirm that Business document management access permissions have been enabled.</span></span>

    ![ビジネス ドキュメント管理のアクセス許可ページのコンフィギュレーション](./media/BDM-Overview-TemplatesAccess2.png)

6. <span data-ttu-id="8abae-243">**追加**を選択して、ビジネス ドキュメント管理のテンプレートにアクセスするための許可をコンフィギュレーションする必要がある新しいビジネス ロールを入力します。</span><span class="sxs-lookup"><span data-stu-id="8abae-243">Select **Add** to enter a new business role for which permissions to access Business document management templates must be configured.</span></span>
7. <span data-ttu-id="8abae-244">**セキュリティ ロール** ダイアログ ボックスで、**売掛金管理係**ロールを選択し、**OK** を選択してロールの選択を確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-244">In the **Security roles** dialog box, select the **Accounts receivable clerk** role and then select **OK** to confirm the role selection.</span></span>
8. <span data-ttu-id="8abae-245">**コンフィギュレーションのタグごとのアクセス許可**タブで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-245">On the **Access permissions per tags of configurations** tab, select **New**.</span></span>
9. <span data-ttu-id="8abae-246">**タグ タイプ**フィールドで、**機能領域**を選択し、**ID** フィールドで、**請求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-246">In the **Tag type** field, select **Functional area**, and in the **ID** field, select **Invoicing**.</span></span>
10. <span data-ttu-id="8abae-247">**保存**を選択すると、選択したロールに対してコンフィギュレーションされたアクセス許可が格納されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-247">Select **Save** to store configured access permissions for the selected role.</span></span>

    <span data-ttu-id="8abae-248">現在の設定とは、**売掛金管理係**ロールに割り当てられ、職務権限である**ビジネス ドキュメント テンプレートの管理** (AOT 名 **ERBDManageTemplates**) を実行しているすべてのユーザーのことであり、**機能領域**タグの**請求**値を持つ ER 形式コンフィギュレーション テンプレートが、ビジネス ドキュメント管理のワークスペースで編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8abae-248">The current setting means that for any user who is assigned to the **Accounts receivable clerk** role and performing the duty, **Manage Business document templates** (AOT name **ERBDManageTemplates**), ER format configuration templates that have the **Invoicing** value for the **Functional area** tag will be available to edit in the Business document management workspace.</span></span>

11. <span data-ttu-id="8abae-249">**関連情報**ウィンドウを現在のページの右側から切り替えます。</span><span class="sxs-lookup"><span data-stu-id="8abae-249">Switch the **Related information** pane from the right side of the current page.</span></span> <span data-ttu-id="8abae-250">**関連情報**ウィンドウには、コンフィギュレーション済のアクセス許可がどのように適用されるか示されます。これには、**売掛金管理係**ロールに割り当てられているユーザーが使用できる ER コンフィギュレーション テンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8abae-250">The **Related information** pane shows how the configured access permissions will be applied, including what ER configuration templates will be available for users that are assigned to the **Accounts receivable clerk** role.</span></span>

    ![ビジネス ドキュメント管理のアクセス許可ページのコンフィギュレーション](./media/BDM-Overview-TemplatesAccess3.png)

12. <span data-ttu-id="8abae-252">**コンフィギュレーションごとのアクセス許可**タブで、**追加**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-252">On the **Access permissions per configurations** tab, select the **Add** option.</span></span>
13. <span data-ttu-id="8abae-253">**コンフィギュレーションの選択**ダイアログボックスで、**イントラスタット レポート**の ER 形式コンフィギュレーションをマークします。</span><span class="sxs-lookup"><span data-stu-id="8abae-253">In the **Select configuration** dialog box, mark the **Intrastat report** ER format configuration.</span></span>
14. <span data-ttu-id="8abae-254">**OK** を選択して、選択したコンフィギュレーションのエントリを確認し、**保存**を選択して、選択したロールのコンフィギュレーション済のアクセス許可を保存します。</span><span class="sxs-lookup"><span data-stu-id="8abae-254">Select **OK** to confirm the entry of the selected configurations and then select **Save** to store the configured access permissions for the selected role.</span></span>

<span data-ttu-id="8abae-255">現在の設定とは、**売掛金管理係**ロールに割り当てられ、職務権限である**ビジネス ドキュメント テンプレートの管理** (AOT 名 **ERBDManageTemplates**) を実行しているすべてのユーザーのことであり、次のテンプレートが、ビジネス ドキュメント管理のワークスペースで編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8abae-255">The current setting means that for any user assigned to the **Accounts receivable clerk** role and performing the duty, **Manage Business document templates** (AOT name **ERBDManageTemplates**), the following templates will be available to edit in the Business document management workspace:</span></span>

- <span data-ttu-id="8abae-256">**機能領域**タグの値**請求**をもつテンプレート。</span><span class="sxs-lookup"><span data-stu-id="8abae-256">Templates that have the value, **Invoicing** for the **Functional area** tag.</span></span>
- <span data-ttu-id="8abae-257">**コンフィギュレーションごとのアクセス許可**タブで表示される ER 形式コンフィギュレーションからテンプレートを行います (この例の**法令報告**ドメインの**イントラスタット レポート**形式コンフィギュレーションからテンプレート)。</span><span class="sxs-lookup"><span data-stu-id="8abae-257">Templates from ER format configurations that are listed on the **Access permissions per configurations** tab (templates from the **Intrastat report** format configuration of the **Statutory reporting** domain in this example).</span></span>

![ビジネス ドキュメント管理のアクセス許可ページのコンフィギュレーション](./media/BDM-Overview-TemplatesAccess4.png)

<span data-ttu-id="8abae-259">次の図では、ビジネス ドキュメント管理のワークスペースが**売掛金管理係**ロールに割り当てられたユーザーに提供するものを示します。</span><span class="sxs-lookup"><span data-stu-id="8abae-259">The following graphic shows what the Business document management workspace provides to a user assigned to the **Accounts receivable clerk** role.</span></span> <span data-ttu-id="8abae-260">現在のビジネス ドキュメントの管理アクセス許可の設定では、ユーザーは**請求**ドメインおよび**イントラスタット レポート**の ER形式コンフィギュレーションからビジネス ドキュメント テンプレートを編集できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-260">With the current Business document management access permissions setting, the user can edit business document templates from the **Invoicing** domain and the **Intrastat report** ER format configuration.</span></span> <span data-ttu-id="8abae-261">**支払**ドメインからのテンプレートでは、**売掛金勘定係**ロールにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="8abae-261">Templates from the **Payments** domain are not accessible for the **Accounts receivable clerk** role.</span></span>

![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> <span data-ttu-id="8abae-263">**コンフィギュレーションごとのアクセス許可**ルールでは、ER 形式コンフィギュレーションの固有の特定 ID を使用して保存されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-263">The **Access permissions per configurations** rules are stored by using the unique identification ID of an ER format configuration.</span></span> <span data-ttu-id="8abae-264">つまり、これらのルールは、それらを参照する ER コンフィギュレーションが削除されると、削除されません。</span><span class="sxs-lookup"><span data-stu-id="8abae-264">This means that these rules will not be deleted when an ER configuration that refers to them are deleted.</span></span> <span data-ttu-id="8abae-265">削除したコンフィギュレーションをこのインスタンスに戻すと、これらのルールによって再度参照されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-265">When you import deleted configurations back to this instance, these rules will refer to them again.</span></span> <span data-ttu-id="8abae-266">削除したコンフィギュレーションを再度インポートした後で、再度ルールを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8abae-266">There is no need to set up the rules again after the deleted configurations are imported again.</span></span>

## <a name="use-business-document-management-to-edit-templates"></a><span data-ttu-id="8abae-267">ビジネス ドキュメント管理を使用して、テンプレートの編集</span><span class="sxs-lookup"><span data-stu-id="8abae-267">Use Business document management to edit templates</span></span>

<span data-ttu-id="8abae-268">ビジネス ユーザーは、ビジネス ドキュメント管理ワークスペースで、ビジネス ドキュメント テンプレートにアクセスして編集を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8abae-268">Business users can access business document templates for editing in the Business document management workspace.</span></span> <span data-ttu-id="8abae-269">ビジネス ドキュメント管理のワークスペースにアクセスできるのは、次のユーザーだけです。</span><span class="sxs-lookup"><span data-stu-id="8abae-269">Only the following users can access the Business document management workspace:</span></span>

- <span data-ttu-id="8abae-270">ロールに割り当てられるユーザー、**システム管理者**。</span><span class="sxs-lookup"><span data-stu-id="8abae-270">Users assigned to the role, **System administrator**.</span></span>
- <span data-ttu-id="8abae-271">職務権限を実行するようにコンフィギュレーションされているロールに割り当てられたユーザー、**ビジネス ドキュメント テンプレートの管理** (AOT 名 **ERBDManageTemplates**)。</span><span class="sxs-lookup"><span data-stu-id="8abae-271">Users assigned to any role that is configured to perform the duty, **Manage Business document templates** (AOT name **ERBDManageTemplates**).</span></span>

<span data-ttu-id="8abae-272">ビジネス ドキュメント管理のワークスペースにて、自由書式の請求書テンプレートを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8abae-272">Use the following procedure to edit free text invoice templates in the Business document management workspace.</span></span> <span data-ttu-id="8abae-273">この手順を実行する前に、トピックの上記の手順をすべて完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="8abae-273">Before you complete this procedure, you must have completed all of the preceding procedures in this topic.</span></span>

1. <span data-ttu-id="8abae-274">ビジネス ドキュメント管理のワークスペースへのアクセス権を持つユーザーとして、ログインします。</span><span class="sxs-lookup"><span data-stu-id="8abae-274">Sign in as a user with access to the Business document management workspace.</span></span>
2. <span data-ttu-id="8abae-275">ビジネス ドキュメント管理のワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="8abae-275">Open the Business document management workspace.</span></span>

![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM-Overview-EditingTemplate1.png)

<span data-ttu-id="8abae-277">**テンプレート**タブには、選択したテンプレートの内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-277">The **Template** tab presents the content of the selected template.</span></span> <span data-ttu-id="8abae-278">**詳細**タブを選択して、選択したテンプレートとこのテンプレートが格納されている ER 形式コンフィギュレーションの詳細をレビューします。</span><span class="sxs-lookup"><span data-stu-id="8abae-278">Select the **Details** tab to review details of the selected template as well as details of an ER format configuration this template resides in.</span></span> <span data-ttu-id="8abae-279">すべてのテンプレートが**発行済**の状態になっており、**リビジョン**列に詳細が含まれていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-279">Notice that all of the templates have a status of **Published**, and contain no details in the **Revision** column.</span></span> <span data-ttu-id="8abae-280">これは、テンプレートが現在編集されていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="8abae-280">This means that these templates are not currently being edited.</span></span>

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a><span data-ttu-id="8abae-281">コンフィギュレーション プロバイダーが所有する編集テンプレートを開始します。</span><span class="sxs-lookup"><span data-stu-id="8abae-281">Initiate editing templates owned by your configuration provider</span></span>

1. <span data-ttu-id="8abae-282">ビジネス ドキュメント管理のワークスペースで、一覧の**小切手の印刷形式**テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-282">In the Business document management workspace, select the **Cheques printing format** template in the list.</span></span>
2. <span data-ttu-id="8abae-283">**詳細**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-283">Select the **Details** tab.</span></span>

![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM-Overview-EditingTemplate2.png)

<span data-ttu-id="8abae-285">**編集テンプレート**オプションでは、選択したテンプレートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-285">The **Edit template** option is available for the selected template.</span></span> <span data-ttu-id="8abae-286">このオプションは、有効な ER コンフィギュレーション プロバイダー (この例では **Litware, inc.**) によって所有されている ER フォーマット コンフィギュレーションのテンプレートに対して、常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-286">This option is always available for a template in an ER format configuration that is owned by the active ER configuration provider (**Litware, Inc.** in this example).</span></span> <span data-ttu-id="8abae-287">**テンプレートの編集**を選択すると、基になる ER 形式コンフィギュレーションの下書きバージョンの既存のテンプレートが編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8abae-287">When **Edit template** is selected, the existing template from the draft version of the underlying ER format configuration will be available to edit.</span></span>

### <a name="initiate-editing-templates-owned-by-other-providers"></a><span data-ttu-id="8abae-288">他のプロバイダーが所有する編集テンプレートを開始</span><span class="sxs-lookup"><span data-stu-id="8abae-288">Initiate editing templates owned by other providers</span></span>

1. <span data-ttu-id="8abae-289">ビジネス ドキュメント管理ワークスペースで、**新規ドキュメント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-289">In the Business document management workspace, select the **New document**.</span></span>

![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="8abae-291">テンプレートとして使用するドキュメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-291">Select the document that you want to use as a template.</span></span>

![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="8abae-293">**ドキュメントの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8abae-293">Click **Create document**</span></span>
4. <span data-ttu-id="8abae-294"> **タイトル**フィールドで、必要に応じて編集可能なテンプレートのタイトルを変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-294">In the **Title** field, change the title of the editable template if needed.</span></span> <span data-ttu-id="8abae-295">このテキストは、自動的に作成される ER 形式コンフィギュレーションに名前を付けるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-295">The text will be used to name the ER format configuration that is automatically created.</span></span> <span data-ttu-id="8abae-296">編集したテンプレートを含む、このコンフィギュレーション (**顧客 FTI レポート (GER) コピー**) のドラフト バージョンは、現在のユーザーに対して ER 形式を実行するよう自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-296">Note that the draft version of this configuration (**Customer FTI report (GER) Copy**) that will contain the edited template will automatically be marked to run this ER format for the current user.</span></span> <span data-ttu-id="8abae-297">同時に、基本 ER 形式コンフィギュレーションからの変更されていない元のテンプレートを使用して、他のユーザーがこの ER 形式を実行します。</span><span class="sxs-lookup"><span data-stu-id="8abae-297">At the same time, the non-modified original template from the base ER format configuration will be used to run this ER format for any other user.</span></span>
5. <span data-ttu-id="8abae-298">**名前**フィールドで、自動的に作成される編集可能なテンプレートの最初のリビジョンの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-298">In the **Name** field, change the name of the first revision of the editable template that will be created automatically.</span></span>
6. <span data-ttu-id="8abae-299">**コメント**フィールドで、自動的に作成された編集可能なテンプレートのリビジョンの注釈を変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-299">In the **Comment** field, change the remark for the automatically created revision of the editable template.</span></span>
7. <span data-ttu-id="8abae-300">**OK** を選択して、編集プロセスの開始を確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-300">Select **OK** to confirm the start of the editing process</span></span>

![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM_overview_new_template3.png)

<span data-ttu-id="8abae-302">**新規ドキュメント**オプションは、別のプロバイダー (この例では Microsoft) によって提供されている ER フォーマット コンフィギュレーションのテンプレートに対して、常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-302">The **New document** option is always available for a template in an ER format configuration provided by another provider (Microsoft in this example).</span></span> <span data-ttu-id="8abae-303">**新規ドキュメント**をクリックすると、現在のプロバイダーと他のプロバイダーが所有するすべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-303">When you click **New document**  you see all templates owned by current and other providers.</span></span> <span data-ttu-id="8abae-304">テンプレートを選択すると、編集用に開かれます。</span><span class="sxs-lookup"><span data-stu-id="8abae-304">After you choose the template it will be opened for editing.</span></span> <span data-ttu-id="8abae-305">編集したテンプレートは、自動的に生成される新規 ER 形式コンフィギュレーションで保存されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-305">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

### <a name="start-editing-a-template"></a><span data-ttu-id="8abae-306">テンプレートの編集開始</span><span class="sxs-lookup"><span data-stu-id="8abae-306">Start editing a template</span></span>

1. <span data-ttu-id="8abae-307">選択したテンプレートで、**ドキュメントの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-307">From the selected template, select **Edit document**.</span></span>
2. <span data-ttu-id="8abae-308">**名前**フィールドで、自動的に作成される編集可能なテンプレートの最初のリビジョンの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-308">In the **Name** field, change the name of the first revision of the editable template that will be created automatically.</span></span>
3. <span data-ttu-id="8abae-309">**コメント**フィールドで、自動的に作成された編集可能なテンプレートのリビジョンの注釈を変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-309">In the **Comment** field, change the remark for the automatically created revision of the editable template.</span></span>

    ![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM_overview_new_template4.png)

5. <span data-ttu-id="8abae-311">**OK** を選択して、編集プロセスの開始を確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-311">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="8abae-312">**BDM テンプレート エディター** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="8abae-312">The **BDM template editor** page will open.</span></span> <span data-ttu-id="8abae-313">選択したテンプレートは、Office 365 を使用してオンライン編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8abae-313">The selected template will be available for online editing by using Office 365.</span></span>

![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-office-365"></a><span data-ttu-id="8abae-315">Office 365 でテンプレートを編集</span><span class="sxs-lookup"><span data-stu-id="8abae-315">Edit a template in Office 365</span></span>

<span data-ttu-id="8abae-316">Office 365 機能を使用して、テンプレートを変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-316">Modify the template by using the functionality of the Office 365.</span></span> <span data-ttu-id="8abae-317">たとえば、Office online で、テンプレート ヘッダーの**レギュラー**から**太字**にフィールド プロンプトのフォントを変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-317">For example, in Office online, change the font of the field prompts in the template header from **Regular** to **Bold**.</span></span> <span data-ttu-id="8abae-318">これらの変更は、ER フレームワーク用にコンフィギュレーションされているプライマリ テンプレートのストレージ (既定では、Azure blob storage) に保存されている編集可能なテンプレートに対して自動的に保存されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-318">These changes are automatically stored for the editable template that is stored in the primary template’s storage (by default, the Azure blob storage) that is configured for the ER framework.</span></span>

![ビジネス ドキュメント管理のテンプレートのエディター ページ](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><span data-ttu-id="8abae-320">Office のデスクトップ アプリケーションでのテンプレートの編集</span><span class="sxs-lookup"><span data-stu-id="8abae-320">Edit a template in the Office desktop application</span></span>

1. <span data-ttu-id="8abae-321">**デスクトップ アプリケーションで開く**オプションを選択して、Office のデスクトップ アプリケーション (この例では Excel) の機能を使用し、テンプレートを変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-321">Select the **Open in Desktop App** option to modify the template by using the functionality of the Office desktop application (Excel in this example).</span></span> <span data-ttu-id="8abae-322">編集可能なテンプレートは、固定保管場所から、SharePoint フォルダーとしてビジネス ドキュメント管理パラメータでコンフィギュレーションされている一時的な保管場所にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8abae-322">The editable template is copied from the permanent storage to the temporary storage configured in the Business document management parameters as a SharePoint folder.</span></span>
2. <span data-ttu-id="8abae-323">Office のデスクトップ Excel アプリケーションにて、一時的なファイルの保管場所からテンプレートを開くことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-323">Confirm that you want to open the template from the temporary file storage in the Office desktop Excel application.</span></span>

    ![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM-Overview-EditingLayout3.png)

3. <span data-ttu-id="8abae-325">テンプレートを変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-325">Modify the template.</span></span> <span data-ttu-id="8abae-326">たとえば、**黒**から**青**に色を更新してテンプレート ヘッダーのフィールド プロンプトのフォントを変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-326">For example, change the font of the fields prompts in the template header by updating color from **Black** to **Blue**.</span></span>

    ![ビジネス ドキュメント管理のテンプレートのエディター ページ](./media/BDM-Overview-EditingLayout4.png)

4. <span data-ttu-id="8abae-328">Excel デスクトップ アプリケーションで**保存**を選択して、一時的な保管場所にテンプレートの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="8abae-328">Select **Save** in the Excel desktop application to store the template changes in the temporary storage.</span></span>

    ![ビジネス ドキュメント管理のテンプレートのエディター ページ](./media/BDM-Overview-EditingLayout5.png)

5. <span data-ttu-id="8abae-330">Excel デスクトップ アプリケーションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8abae-330">Close the Excel desktop application.</span></span>
6. <span data-ttu-id="8abae-331">**保存されたコピーを同期**を選択して、一時的テンプレート保管を固定テンプレート保管に同期します。</span><span class="sxs-lookup"><span data-stu-id="8abae-331">Select **Sync stored copy** to synchronize the temporary template storage to the permanent template storage.</span></span>

> [!NOTE]
> <span data-ttu-id="8abae-332">一時的ファイル保管内の編集可能なテンプレートのコピーは、テンプレート編集の現セッションでのみ保持されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-332">The copy of the editable template in the temporary file storage is kept for only the current session of template editing.</span></span> <span data-ttu-id="8abae-333">**BDM テンプレート エディター**ページを閉じて、このセッションを終了すると、コピーは削除されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-333">When you finish this session by closing the **BDM template editor** page, this copy will be deleted.</span></span> <span data-ttu-id="8abae-334">一時的ファイル保管場所でテンプレートを調整し、**保存されたコピーの同期**選択しなかった場合は、**BDM テンプレート エディター**ページを閉じようとすると、変更を保存するかどうかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-334">If you adjusted the template in the temporary file storage and did not select **Sync stored copy**, when you try to close the **BDM template editor** page, a message will ask whether you want to store introduced changes.</span></span> <span data-ttu-id="8abae-335">固定ファイル場所のテンプレートへの変更を保存したい場合は、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-335">Select **Yes** if you want to save your changes to the template in the permanent file location.</span></span>

### <a name="validate-a-template"></a><span data-ttu-id="8abae-336">テンプレートの検証</span><span class="sxs-lookup"><span data-stu-id="8abae-336">Validate a template</span></span>

1. <span data-ttu-id="8abae-337">**BDM テンプレート エディター**ページで、**問題点を確認**を選択して、基になる ER 形式コンフィギュレーションに対して変更したテンプレートを検証します。</span><span class="sxs-lookup"><span data-stu-id="8abae-337">On the **BDM template editor** page, select **Check for issues** to validate the modified template against the underlying ER format configuration.</span></span> <span data-ttu-id="8abae-338">推奨事項 (該当する場合) に従って、テンプレートを基本の ER 形式コンフィギュレーションの形式の構造に配置します。</span><span class="sxs-lookup"><span data-stu-id="8abae-338">Follow the recommendations (if any) to align the template with the structure of the format from the base ER format configuration.</span></span>
2. <span data-ttu-id="8abae-339">**形式の表示**を選択すると、編集可能なテンプレートに配置する必要がある基本の ER 形式コンフィギュレーションからの形式の現構造が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-339">Select **Show format** to view the current structure of the format from the base ER format configuration that must be aligned with the editable template.</span></span> 
3. <span data-ttu-id="8abae-340">**フォーマットの非表示**を選択して、ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8abae-340">Select **Hide format** to close the pane.</span></span>

    ![BDM テンプレートのエディター ページ](./media/BDM-Overview-EditingTemplate6.png)

4. <span data-ttu-id="8abae-342">**BDM テンプレートのエディター**ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8abae-342">Close the **BDM template editor** page.</span></span>

<span data-ttu-id="8abae-343">更新されたテンプレートが**テンプレート**タブに表示されます。編集したテンプレートの状態が**ドラフト**になり、現在のリビジョンが空ではなくなったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-343">The updated template is shown on the **Template** tab. Notice that the status of the edited template is now **Draft** and the current revision is no longer empty.</span></span> <span data-ttu-id="8abae-344">これは、このテンプレートの編集のプロセスが開始されたことを意味します。</span><span class="sxs-lookup"><span data-stu-id="8abae-344">This means that the process of this template’s editing has been started.</span></span>

![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a><span data-ttu-id="8abae-346">変更したテンプレートのテスト</span><span class="sxs-lookup"><span data-stu-id="8abae-346">Test the modified template</span></span> 

1. <span data-ttu-id="8abae-347">アプリケーションで、会社 **USMF** に変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-347">In the application, change to the company, **USMF**.</span></span>
2. <span data-ttu-id="8abae-348">**売掛金勘定** \> **請求書** \> **すべての自由書式の請求書**に移動します。</span><span class="sxs-lookup"><span data-stu-id="8abae-348">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
3. <span data-ttu-id="8abae-349">**FTI-00000002** 請求書を選択し、**印刷管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-349">Select the **FTI-00000002** invoice, and then select **Print management**.</span></span>
4. <span data-ttu-id="8abae-350">**モジュール - 売掛金** \> **ドキュメント** \> **自由書式の請求** \> **元のドキュメント**レベルを選択して、処理する請求書の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="8abae-350">Select the **Module - accounts receivable** \> **Documents** \> **Free text invoice** \> **Original document** level to specify the scope of invoices for processing.</span></span>
5. <span data-ttu-id="8abae-351">**レポート形式**フィールドで、指定したドキュメント レベルの**顧客 FTI レポート (GER) コピー**の ER 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-351">In the **Report format** field, select the **Customer FTI report (GER) Copy** ER format for the specified document level.</span></span>

    ![管理設定ページを印刷](./media/BDM-Overview-TestRun1.png)

6. <span data-ttu-id="8abae-353">**エスケープ**を押して、現在のページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8abae-353">Press **Escape** to close the current page.</span></span>
7. <span data-ttu-id="8abae-354">**印刷**を選択し、**選択済**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8abae-354">Select **Print**, and then click **Selected**.</span></span>
8. <span data-ttu-id="8abae-355">ドキュメントをダウンロードし、Excel デスクトップ アプリケーションを使用して開きます。</span><span class="sxs-lookup"><span data-stu-id="8abae-355">Download the document and open it using the Excel desktop application.</span></span>

![自由書式の請求書のページ](./media/BDM-Overview-TestRun2.png)

<span data-ttu-id="8abae-357">変更したテンプレートは、選択した品目に対して自由書式の請求書レポートを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-357">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="8abae-358">テンプレートに加えた変更によってこのレポートがどのように影響を受けるかを分析するには、別のアプリケーション セッションでテンプレートを変更した直後に、1 つのアプリケーション セッションでこのレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="8abae-358">To analyze how this report is affected by the changes that you introduced to the template, you can run this report in one application session right after you modified the template in another application session.</span></span>

### <a name="create-an-alternative-template-revision"></a><span data-ttu-id="8abae-359">代替テンプレート リビジョンの作成</span><span class="sxs-lookup"><span data-stu-id="8abae-359">Create an alternative template revision</span></span>

1. <span data-ttu-id="8abae-360">**BDM テンプレート エディター**ページを開いて、**顧客 FTI レポート (GER) コピー**のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-360">Open the **BDM template editor** page and select the **Customer FTI report (GER) Copy** template.</span></span>
2. <span data-ttu-id="8abae-361">**リビジョン**タブで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-361">On the **Revisions** tab, select **New**.</span></span>
3. <span data-ttu-id="8abae-362">必要に応じて、**名前**フィールドで 2 番目のリビジョンの名前を変更し、現在有効な最初のリビジョンの基準とします。</span><span class="sxs-lookup"><span data-stu-id="8abae-362">If needed, in the **Name** field, change the name of the second revision and base it on the currently active first revision.</span></span>
4. <span data-ttu-id="8abae-363">必要であれば、**コメント**フィールドで、自動的に作成された編集可能なテンプレートのリビジョンの注釈を変更します。</span><span class="sxs-lookup"><span data-stu-id="8abae-363">If needed, in the **Comment** field, change the remark for the automatically created revision of the editable template.</span></span>

    ![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM-Overview-AddRevision.png)

    <span data-ttu-id="8abae-365">固定テンプレートの保管場所に保存されているテンプレートの新しいリビジョンを作成しました。</span><span class="sxs-lookup"><span data-stu-id="8abae-365">You created a new revision of your template that has been stored in the permanent template’s storage.</span></span> <span data-ttu-id="8abae-366">現在アクティブとして選択されている 2 番目のリビジョンのテンプレートの編集を続けることができます。</span><span class="sxs-lookup"><span data-stu-id="8abae-366">Now you can continue editing the template of the second revision that is currently selected as active.</span></span>

5. <span data-ttu-id="8abae-367">最初のリビジョンを選択し、**アクティブに設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-367">Select the first revision and then select **Set active**.</span></span> <span data-ttu-id="8abae-368">いつでもそのテンプレートのリビジョンに戻りたい場合、アクティブである別のリビジョンを選択できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-368">You can select another revision as active if at any time you want to return to that revision of the template.</span></span>
6. <span data-ttu-id="8abae-369">2 番目のリビジョンを選択し、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-369">Select the second revision, and then select **Delete**.</span></span>
7. <span data-ttu-id="8abae-370">**OK** を選択し、選択したリビジョンを削除することを確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-370">Select **OK** to confirm that you want to delete the selected revision.</span></span> <span data-ttu-id="8abae-371">非アクティブなリビジョンは、不要になった時点で削除できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-371">You can delete any of the non-active revisions when they are no longer needed.</span></span>

### <a name="delete-a-modified-template"></a><span data-ttu-id="8abae-372">変更したテンプレートの削除</span><span class="sxs-lookup"><span data-stu-id="8abae-372">Delete a modified template</span></span>

1. <span data-ttu-id="8abae-373">**BDM テンプレート エディター**ページで、**テンプレート**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-373">On the **BDM template editor** page, select the **Template** tab.</span></span>
2. <span data-ttu-id="8abae-374">**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-374">Select **Delete**.</span></span>
3. <span data-ttu-id="8abae-375">**OK** を選択して削除を確認した場合、変更したテンプレートを持つ**顧客 FTI レポート (GER) コピー**の ER 形式は削除されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-375">If you select **OK** to confirm deletion, the **Customer FTI report (GER) Copy** ER format with the modified template will be deleted.</span></span> <span data-ttu-id="8abae-376">**キャンセル**を選択して、他のオプションをエクスプローラーします。</span><span class="sxs-lookup"><span data-stu-id="8abae-376">Select **Cancel** to explore other options.</span></span>

### <a name="revoke-changes-of-template"></a><span data-ttu-id="8abae-377">テンプレートの変更の無効化</span><span class="sxs-lookup"><span data-stu-id="8abae-377">Revoke changes of template</span></span>

<span data-ttu-id="8abae-378">現在アクティブなプロバイダーによって所有されている ER 形式からテンプレートを編集する場合は、テンプレートに導入された変更を取り消すためのオプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-378">When you edit the template from an ER format that is owned by the current active provider, you will be offered the option to revoke changes introduced for the template.</span></span>

![ビジネス ドキュメント管理のワークスペース ページ](./media/BDM-Overview-RevokeChanges.png)

1. <span data-ttu-id="8abae-380">**BDM テンプレート エディター**ページで、**テンプレート**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-380">On the **BDM template editor** page, select the **Template** tab.</span></span>
2. <span data-ttu-id="8abae-381">**取り消し**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-381">Select **Undo**.</span></span>
3. <span data-ttu-id="8abae-382">**OK** を選択しテンプレートに導入された変更を取り消す場合、変更したテンプレートは元のテンプレートに置き換えられ、すべての変更が削除されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-382">If you select **OK** to revoke the changes introduced for the template, the modified template will be replaced by the original template and all changes will be removed.</span></span> <span data-ttu-id="8abae-383">テンプレートに対する変更を取り消すと、テンプレートを削除できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8abae-383">When you revoke changes to the template, you will be able to delete the template.</span></span> <span data-ttu-id="8abae-384">**キャンセル**を選択して、他のオプションをエクスプローラーします。</span><span class="sxs-lookup"><span data-stu-id="8abae-384">Select **Cancel** to explore other options.</span></span>

### <a name="publish-a-modified-template"></a><span data-ttu-id="8abae-385">変更したテンプレートの公開</span><span class="sxs-lookup"><span data-stu-id="8abae-385">Publish a modified template</span></span>
1. <span data-ttu-id="8abae-386">**BDM テンプレート エディター**ページの**テンプレート**タブで、**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-386">On the **BDM template editor** page, on the **Template** tab, select **Publish**.</span></span>
2. <span data-ttu-id="8abae-387">**OK** を選択して公開の確認をする場合、変更したテンプレートが含まれる派生**顧客 FTI レポート (GER) コピー**の ER 形式の下書きバージョンが完了としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="8abae-387">If you select **OK** to confirm publishing, the draft version of the derived **Customer FTI report (GER) Copy** ER format that contains the modified template will be marked as completed.</span></span> <span data-ttu-id="8abae-388">変更したテンプレートは、他のユーザーが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8abae-388">The modified template becomes available for other users.</span></span> <span data-ttu-id="8abae-389">この ER 形式の完全版では、テンプレートの最後のアクティブ リビジョンのみが保持されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-389">The completed versions of this ER format will keep only the last active revision of your template.</span></span> <span data-ttu-id="8abae-390">他のリビジョンは削除されます。</span><span class="sxs-lookup"><span data-stu-id="8abae-390">Other revisions will be deleted.</span></span> <span data-ttu-id="8abae-391">**キャンセル**を選択して、他のオプションをエクスプローラーします。</span><span class="sxs-lookup"><span data-stu-id="8abae-391">Select **Cancel** to explore other options.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8abae-392">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="8abae-392">Frequently asked questions</span></span>

#### <a name="i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a><span data-ttu-id="8abae-393">**ドキュメントの編集**を選択したが、Finance and Operations の **BDM テンプレート エディター**ページが開く代わりに、Office 365 の Web ページに送信されました。</span><span class="sxs-lookup"><span data-stu-id="8abae-393">I selected **Edit document**, but instead of opening the **BDM template editor** page in Finance and Operations, I have been sent to the Office 365 web page.</span></span>
<span data-ttu-id="8abae-394">これは、Office 365 リダイレクトに関する既知の問題です。</span><span class="sxs-lookup"><span data-stu-id="8abae-394">This is a known issue with the Office 365 redirection.</span></span> <span data-ttu-id="8abae-395">これは、最初に Office 365 に署名したときに発生します。</span><span class="sxs-lookup"><span data-stu-id="8abae-395">This happens when you sign to Office 365 the first time.</span></span> <span data-ttu-id="8abae-396">この問題を回避するには、ブラウザーの**戻る**ボタンを選択して戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="8abae-396">To work around this issue, select the **Back** button of your browser to navigate back.</span></span>

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a><span data-ttu-id="8abae-397">最初のアプリケーション セッションで Office 365 を使用してテンプレートを編集する方法と、テンプレートを調整して 2 番目のアプリケーション セッションでテンプレートを使う方法を理解し、変更が生成されたビジネス ドキュメントにどのように影響するかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8abae-397">I understand how to edit a template by using Office 365 in the first application session and how to use the template in the second application session adjusting the template to see how my changes affect the generated business document.</span></span> <span data-ttu-id="8abae-398">Office デスクトップ アプリケーションを使用してこれを行うことができますか。</span><span class="sxs-lookup"><span data-stu-id="8abae-398">Can I do this using the Office desktop application?</span></span>
<span data-ttu-id="8abae-399">はい、できます。</span><span class="sxs-lookup"><span data-stu-id="8abae-399">Yes, you can.</span></span> <span data-ttu-id="8abae-400">最初のアプリケーション セッションで、**デスクトップ アプリケーションを開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-400">In the first application session, select **Open in Desktop App**.</span></span> <span data-ttu-id="8abae-401">テンプレートは一時ファイル保管場所に保存され、Office デスクトップ アプリケーションで開かれます。</span><span class="sxs-lookup"><span data-stu-id="8abae-401">Your template will be stored in the temporary file storage and opened in the Office desktop application.</span></span> <span data-ttu-id="8abae-402">次に、生成されたビジネス ドキュメントのテンプレートの変更をプレビューするために、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8abae-402">Next, complete the following steps to preview your template changes in the generated business document:</span></span>

1. <span data-ttu-id="8abae-403">Office デスクトップ アプリケーションを使用して、テンプレートに変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="8abae-403">Make changes in the template by using the Office desktop application.</span></span>
2. <span data-ttu-id="8abae-404">Office デスクトップ アプリケーションで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-404">Select **Save** in the Office desktop application.</span></span>
3. <span data-ttu-id="8abae-405">最初のアプリケーション セッションの **BDM テンプレート エディター**ページで、**保存されたコピーの同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8abae-405">On the **BDM template editor** page of the first application session, select **Sync stored copy**.</span></span>
4. <span data-ttu-id="8abae-406">2 番目のアプリケーション セッションで、このテンプレートの ER 形式を実行します。</span><span class="sxs-lookup"><span data-stu-id="8abae-406">Execute this template ER format in the second application session.</span></span>

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a><span data-ttu-id="8abae-407">「値を Null にすることは出来ません」というエラーが発生。</span><span class="sxs-lookup"><span data-stu-id="8abae-407">I get the error ‘Value cannot be null.</span></span> <span data-ttu-id="8abae-408">パラメーター名: externalId’、**デスクトップ アプリケーションを開く**を選択した場合。</span><span class="sxs-lookup"><span data-stu-id="8abae-408">Parameter name: externalId’ when I select **Open in Desktop App**.</span></span> <span data-ttu-id="8abae-409">回避するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="8abae-409">How do I work around this?</span></span> 
<span data-ttu-id="8abae-410">ほとんどの場合、このインスタンスを配置するために使用された Azure AD ドメインと異なる Azure AD ドメイン アプリケーションの、現インスタンスにログインします。</span><span class="sxs-lookup"><span data-stu-id="8abae-410">Most likely you signed in to the current instance of the app of the Azure AD domain which differs from the Azure AD domain that was used to deploy this instance.</span></span> <span data-ttu-id="8abae-411">Office デスクトップ アプリケーションを使用して編集可能にするためのテンプレートを保存するために使用される SharePoint サービスは、同じドメインに属しているので、SharePoint サービスにアクセスするためのアクセス許可はありません。</span><span class="sxs-lookup"><span data-stu-id="8abae-411">Because the SharePoint service, which is used to store templates for making them available for editing by using the Office desktop applications, belongs to the same domain, we have no permissions to access the SharePoint service.</span></span> <span data-ttu-id="8abae-412">この問題を解決するには、適切な Azure AD ドメインを持つユーザーの資格情報を使用して、現インスタンスにログインします。</span><span class="sxs-lookup"><span data-stu-id="8abae-412">To resolve this issue, sign in to the current instance using the credentials of a user with the correct Azure AD domain.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8abae-413">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8abae-413">Additional resources</span></span>

[<span data-ttu-id="8abae-414">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="8abae-414">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="8abae-415">OPENXML 形式でレポートを生成する ER コンフィギュレーションを設計する (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="8abae-415">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>](tasks/er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="8abae-416">Word 形式でレポートを生成するための ER コンフィギュレーションのデザイン</span><span class="sxs-lookup"><span data-stu-id="8abae-416">Design ER configurations to generate reports in Word format</span></span>](tasks/er-design-configuration-word-2016-11.md)

[<span data-ttu-id="8abae-417">ER を使用して生成されるドキュメントへの画像や図形の埋め込み</span><span class="sxs-lookup"><span data-stu-id="8abae-417">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="8abae-418">Power BI にデータをプルするよう電子申告 (ER) を構成する</span><span class="sxs-lookup"><span data-stu-id="8abae-418">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)
