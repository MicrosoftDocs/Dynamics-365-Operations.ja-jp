---
title: 会社データの初期化
description: このトピックでは、デュアル書き込み接続を有効にする前に、会社情報を使用してデータを初期化する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 31301
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 042cefb9fa659ad9511b48365d22fa878b5874bc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751448"
---
# <a name="initialize-company-data"></a><span data-ttu-id="03bd3-103">会社データの初期化</span><span class="sxs-lookup"><span data-stu-id="03bd3-103">Initialize company data</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="03bd3-104">ビジネス データを持つ既存の Microsoft Dataverse インスタンスまたは Finance and Operations アプリ インスタンスを所有している場合、それに対してデュアル書き込み接続を有効にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-104">If have an existing Microsoft Dataverse instance or Finance and Operations app instance that has business data, you might want to enable a dual-write connection against it.</span></span> <span data-ttu-id="03bd3-105">この場合は、デュアル書き込みを有効にする前に、会社情報を使用して Dataverse データまたは Finance and Operations アプリ データを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03bd3-105">In this case, you must initialize the Dataverse data or Finance and Operations app data with company information before you enable dual-write.</span></span> <span data-ttu-id="03bd3-106">この初期化プロセスは、*bootstrapping* と呼ばれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="03bd3-106">This initialization process is sometimes referred to as *bootstrapping*.</span></span>

<span data-ttu-id="03bd3-107">このトピックには、デュアル書き込み用 Dataverse のデータを初期化するために、[Azure Data Factory](https://docs.microsoft.com/azure/data-factory/introduction) の使い方をを説明するサンプル シナリオが含まれます。</span><span class="sxs-lookup"><span data-stu-id="03bd3-107">This topic includes sample scenarios that explain how to use [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/introduction) to initialize data in Dataverse tables for dual-write.</span></span> <span data-ttu-id="03bd3-108">すべてのテーブル、エラー処理のシナリオ、またはルックアップについては説明しません。</span><span class="sxs-lookup"><span data-stu-id="03bd3-108">It doesn't cover all tables, error handling scenarios, or lookups.</span></span> <span data-ttu-id="03bd3-109">照会としてこのトピックとテンプレートを使用し、独自の Azure Data Factory パイプラインを設定して、データを Dataverse にインポートまたは  Dataverse に更新します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-109">Use this topic and template as a reference to set up your own Azure Data Factory pipeline to import data into Dataverse or update data in Dataverse.</span></span>

## <a name="high-level-scenario"></a><span data-ttu-id="03bd3-110">高レベルのシナリオ</span><span class="sxs-lookup"><span data-stu-id="03bd3-110">High-level scenario</span></span>

<span data-ttu-id="03bd3-111">Finance and Operations アプリに **顧客** テーブル、および Dataverse に **アカウント** テーブルを考慮します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-111">Consider the **Customers** table in a Finance and Operations app, and the **Account** table in Dataverse.</span></span>

- <span data-ttu-id="03bd3-112">最初の書き込みを使用して、Finance and Operations アプリから Dataverse へ、**会社**、**顧客グループ** および **支払条件** などの照会と依存テーブルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-112">Use initial write to copy reference and dependent tables, such as **Company**, **Customer groups**, and **Terms of payment**, from the Finance and Operations app to Dataverse.</span></span>
- <span data-ttu-id="03bd3-113">データ管理フレームワークを使用して、コンマ区切り値 (CSV) 形式で Finance and Operations アプリからデータをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-113">Use the Data management framework to export data from the Finance and Operations app in comma-separated values (CSV) format.</span></span> <span data-ttu-id="03bd3-114">たとえば、データ管理のプロジェクトを設定し、Finance and Operations アプリの **DataAreaId** フィールドを使用して会社ごとに顧客をエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-114">For example, set up an export project in Data management to export customers from each company by using the **DataAreaId** field in the Finance and Operations app.</span></span> <span data-ttu-id="03bd3-115">このプロセスは、1 回の手動プロセスです。</span><span class="sxs-lookup"><span data-stu-id="03bd3-115">This process is a one-time manual process.</span></span>
- <span data-ttu-id="03bd3-116">Azure Blob Storage を使用し、ルックアップと変換用の CSV ファイルを格納します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-116">Use Azure Blob Storage to store the CSV files for lookup and transformation.</span></span> <span data-ttu-id="03bd3-117">Finance and Operations 顧客の CSV ファイルを Azure Blob Storage にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-117">Upload the CSV file for your Finance and Operations customers into Azure Blob Storage.</span></span>
- <span data-ttu-id="03bd3-118">Azure Data Factory を使用し、Dataverse のデータを初期化します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-118">Use Azure Data Factory to initialize data in Dataverse.</span></span>

<span data-ttu-id="03bd3-119">次の図はワークフローを示します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-119">The following illustration shows the workflow.</span></span>

:::image type="content" source="media/boot-process-flow.png" alt-text="高レベル フロー":::

<span data-ttu-id="03bd3-121">このシナリオは、次の前提に基づいています。</span><span class="sxs-lookup"><span data-stu-id="03bd3-121">This scenario is based on the following assumptions:</span></span>

- <span data-ttu-id="03bd3-122">ソース データは Finance and Operations アプリにあります。</span><span class="sxs-lookup"><span data-stu-id="03bd3-122">The source data is in the Finance and Operations app.</span></span>
- <span data-ttu-id="03bd3-123">アカウントが Dataverse に存在し、Finance and Operations アプリに存在しない場合は、このフローの一部として初期化されません。</span><span class="sxs-lookup"><span data-stu-id="03bd3-123">If an account exists in Dataverse, but it doesn't exist in the Finance and Operations app, it won't be initialized as part of this flow.</span></span>
- <span data-ttu-id="03bd3-124">顧客関与アプリのすべてのアカウント レコードには、Finance and Operations ナチュラル キーと一致するナチュラル キー (アカウント番号) が設定されています (**CustomerAccount**)。</span><span class="sxs-lookup"><span data-stu-id="03bd3-124">All account records in the customer engagement apps have a natural key (account number) that matches the Finance and Operations natural key (**CustomerAccount**).</span></span>
- <span data-ttu-id="03bd3-125">行には、アプリ全体での 1 対 1 (1:1) マッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="03bd3-125">Rows have a one-to-one (1:1) mapping across the apps.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="03bd3-126">必要条件</span><span class="sxs-lookup"><span data-stu-id="03bd3-126">Prerequisites</span></span>

- <span data-ttu-id="03bd3-127">**Azure の定期売買** – 既存の Azure 定期売買に対する **貢献者のアクセス** があります。</span><span class="sxs-lookup"><span data-stu-id="03bd3-127">**Azure subscription** – You have **contributor access** to an existing Azure subscription.</span></span> <span data-ttu-id="03bd3-128">Azure 定期売買をお持ちでない場合は、開始前に[フリー Azure アカウント](https://azure.microsoft.com/free/) を作成してください。</span><span class="sxs-lookup"><span data-stu-id="03bd3-128">If you don't have an Azure subscription, create a [free Azure account](https://azure.microsoft.com/free/) before you begin.</span></span>
- <span data-ttu-id="03bd3-129">**Azure Storage アカウント** – Azure Srage アカウントがあります。</span><span class="sxs-lookup"><span data-stu-id="03bd3-129">**Azure storage account** – You have an Azure storage account.</span></span> <span data-ttu-id="03bd3-130">ストレージ アカウントを持っていない場合は、[Azure Storage アカウントを作成](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal#create-a-storage-account) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="03bd3-130">If you don't have a storage account, follow the steps in [Create an Azure storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal#create-a-storage-account) to create one.</span></span>
- <span data-ttu-id="03bd3-131">**Azure データ ファクトリ** – [データ ファクトリを作成](https://docs.microsoft.com/azure/data-factory/tutorial-copy-data-portal#create-a-data-factory) の手順に従い Azure Data Factory のリソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-131">**Azure data factory** – Create an Azure Data Factory resource by following the steps in [Create a data factory](https://docs.microsoft.com/azure/data-factory/tutorial-copy-data-portal#create-a-data-factory).</span></span>
- <span data-ttu-id="03bd3-132">**Finance and Operations アプリ**  – データ管理フレームワークを使用して、CSV 形式でデータをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-132">**Finance and Operations app** – Use the Data management framework to export the data in CSV format.</span></span> <span data-ttu-id="03bd3-133">詳細については、 [データ管理の概要](../data-entities-data-packages.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03bd3-133">For more information, see [Data management overview](../data-entities-data-packages.md).</span></span> <span data-ttu-id="03bd3-134">このテンプレートでは、顧客が **CustCustomerV3Entity** テーブルを使用してエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="03bd3-134">In this template, customers are exported by using the **CustCustomerV3Entity** table.</span></span>
- <span data-ttu-id="03bd3-135">**Dynamics 365 Dataverse** – Dataverse 管理者ユーザーの認証情報を使い、データを初期化します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-135">**Dynamics 365 Dataverse** – Use the credentials for the Dataverse admin user to initialize the data.</span></span>
- <span data-ttu-id="03bd3-136">**デュアル書き込み** – デュアル書き込みソリューションがインストールされ、初期書き込みを使用して参照データがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="03bd3-136">**Dual-write** – Dual-write solutions are installed, and reference data is copied by using initial write.</span></span>

## <a name="deployment-steps"></a><span data-ttu-id="03bd3-137">配置の手順</span><span class="sxs-lookup"><span data-stu-id="03bd3-137">Deployment steps</span></span>

### <a name="set-up-an-azure-storage-account"></a><span data-ttu-id="03bd3-138">Azure ストレージ アカウントの設定</span><span class="sxs-lookup"><span data-stu-id="03bd3-138">Set up an Azure storage account</span></span>

<span data-ttu-id="03bd3-139">Azure ストレージ アカウントを持っていない場合は、[Azure ストレージ アカウントを作成](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal#create-a-storage-account) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="03bd3-139">If you don't have an Azure storage account, follow these steps in [Create an Azure storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal#create-a-storage-account) to create one.</span></span> <span data-ttu-id="03bd3-140">ストレージ アカウントで、**ce-data** という名前のコンテナーを 1 つ作成します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-140">In your storage account, create one container that is named **ce-data**.</span></span> <span data-ttu-id="03bd3-141">このコンテナには、すべてのデータ ファイルが格納されます。</span><span class="sxs-lookup"><span data-stu-id="03bd3-141">This container will store all data files.</span></span> <span data-ttu-id="03bd3-142">データセットおよびパイプライン内のコンテナは、必要に応じ変更できます。</span><span class="sxs-lookup"><span data-stu-id="03bd3-142">You can change the container in your datasets and pipelines as you require.</span></span> <span data-ttu-id="03bd3-143">次の図に示すように、**アクセス キー** に移動し、**接続文字列** 値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-143">Go to **Access keys**, and copy the **Connection string** value, as shown in the following illustration.</span></span> <span data-ttu-id="03bd3-144">この値は、Azure Data Factory テンプレートをインポートする際に必須です。</span><span class="sxs-lookup"><span data-stu-id="03bd3-144">This value is required when you import the Azure Data Factory template.</span></span>

:::image type="content" source="media/boot-storage-account.png" alt-text="アクセス キーの設定":::

### <a name="deploy-an-azure-data-factory-template"></a><span data-ttu-id="03bd3-146">Azure Data Factory テンプレートの配置</span><span class="sxs-lookup"><span data-stu-id="03bd3-146">Deploy an Azure Data Factory template</span></span>

1. <span data-ttu-id="03bd3-147">作成した Azure データ ファクトリーの名前をメモします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-147">Make a note of the name of the Azure data factory that you created.</span></span>
2. <span data-ttu-id="03bd3-148">Azure ストレージ アカウントの接続文字列をメモします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-148">Make a note of the connection string for the Azure storage account.</span></span>
3. <span data-ttu-id="03bd3-149">Dataverse インスタンスのサービス URI と管理者ユーザーの名前、パスワードをメモします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-149">Make a note of the service URI of the Dataverse instance, and the admin user name and password.</span></span>

    <span data-ttu-id="03bd3-150">次の表に、必要なパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-150">The following table shows the parameters that are required.</span></span>

    | <span data-ttu-id="03bd3-151">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="03bd3-151">Parameter name</span></span> | <span data-ttu-id="03bd3-152">説明</span><span class="sxs-lookup"><span data-stu-id="03bd3-152">Description</span></span> | <span data-ttu-id="03bd3-153">サンプル値</span><span class="sxs-lookup"><span data-stu-id="03bd3-153">Example value</span></span> |
    |---|---|---|
    | <span data-ttu-id="03bd3-154">ファクトリー名</span><span class="sxs-lookup"><span data-stu-id="03bd3-154">Factory name</span></span> | <span data-ttu-id="03bd3-155">データ ファクトリー名</span><span class="sxs-lookup"><span data-stu-id="03bd3-155">The name of your data factory</span></span> | <span data-ttu-id="03bd3-156">*BootstrapDataverseDataADF*</span><span class="sxs-lookup"><span data-stu-id="03bd3-156">*BootstrapDataverseDataADF*</span></span> |
    | <span data-ttu-id="03bd3-157">Bootstrap blob storage account Linked Service\_connection String</span><span class="sxs-lookup"><span data-stu-id="03bd3-157">Bootstrap blob storage account Linked Service\_connection String</span></span> | <span data-ttu-id="03bd3-158">Blob ストレージの接続文字列</span><span class="sxs-lookup"><span data-stu-id="03bd3-158">The connection string for blob storage</span></span> | <span data-ttu-id="03bd3-159">ストレージ アカウントの作成時にコピーした値</span><span class="sxs-lookup"><span data-stu-id="03bd3-159">The value that you copied when you created the storage account</span></span> |
    | <span data-ttu-id="03bd3-160">Bootstrap Dynamics 365 Linked Service\_service URI</span><span class="sxs-lookup"><span data-stu-id="03bd3-160">Bootstrap Dynamics 365 Linked Service\_service Uri</span></span> | <span data-ttu-id="03bd3-161">Dataverse インスタンスの URI</span><span class="sxs-lookup"><span data-stu-id="03bd3-161">The URI of the Dataverse instance</span></span> | `https://contosod365.crm4.dynamics.com` |
    | <span data-ttu-id="03bd3-162">Bootstrap Dynamics 365 Linked Service\_properties\_type Properties\_username</span><span class="sxs-lookup"><span data-stu-id="03bd3-162">Bootstrap Dynamics 365 Linked Service\_properties\_type Properties\_username</span></span> | <span data-ttu-id="03bd3-163">Dynamics 365 管理者ユーザーのユーザー ID</span><span class="sxs-lookup"><span data-stu-id="03bd3-163">The Dynamics 365 admin user's user ID</span></span> | `<adminservice@contoso.onmicrosoft.com>` |
    | <span data-ttu-id="03bd3-164">Bootstrap Dynamics 365 Linked Service\_password</span><span class="sxs-lookup"><span data-stu-id="03bd3-164">Bootstrap Dynamics 365 Linked Service\_password</span></span> | <span data-ttu-id="03bd3-165">Dynamics 365 管理者ユーザーのパスワード</span><span class="sxs-lookup"><span data-stu-id="03bd3-165">The Dynamics 365 admin user's password</span></span> | _\*\*\*\*\*\*\*\*_ | 

4. <span data-ttu-id="03bd3-166">[Azure Resource Manager (ARM) テンプレート ファイル](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Bootstrapping/arm_template.json) をローカル ディレクトリにダウンロートします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-166">Download the [Azure Resource Manager (ARM) template file](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Bootstrapping/arm_template.json) to your local directory.</span></span>
5. <span data-ttu-id="03bd3-167">Azure ポータルで、[カスタム デプロイ](https://ms.portal.azure.com/#create/Microsoft.Template) に移動します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-167">In the Azure portal, go to [Custom deployment](https://ms.portal.azure.com/#create/Microsoft.Template).</span></span>
6. <span data-ttu-id="03bd3-168">**独自のテンプレートをエディターに作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-168">Select **Build your own template in the editor**.</span></span>
7. <span data-ttu-id="03bd3-169">**ファイルの読み込み** を選択し、先にダウンロードした ARM テンプレート ファイルを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-169">Select **Load file**, and find and select the ARM template file that you downloaded earlier.</span></span> <span data-ttu-id="03bd3-170">その後、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-170">Then select **Save**.</span></span>
8. <span data-ttu-id="03bd3-171">必要なパラメータを指定し、**確認** を選び、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-171">Provide the required parameters, select **Review**, and then select **Create**.</span></span>

    :::image type="content" source="media/boot-custom-deployment.png" alt-text="テンプレートのカスタマイズ":::

9. <span data-ttu-id="03bd3-173">デプロイ後、リスト ウィンドウに **パイプライン**、**データセット** および **データ フロー** セクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03bd3-173">After deployment, you will see **Pipelines**, **Datasets**, and **Data flows** sections in the list pane.</span></span>

    :::image type="content" source="media/boot-pipeline.png" alt-text="パイプライン、データセット、およびデータ フロー":::

## <a name="run-the-process"></a><span data-ttu-id="03bd3-175">プロセスを実行する</span><span class="sxs-lookup"><span data-stu-id="03bd3-175">Run the process</span></span>

1. <span data-ttu-id="03bd3-176">Finance and Operations アプリで、データ管理フレームワークを使用して、CSV 形式でデータをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-176">In the Finance and Operations app, use the Data management framework to export data in CSV format.</span></span> <span data-ttu-id="03bd3-177">詳細については、 [データ管理の概要](../data-entities-data-packages.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03bd3-177">For more information, see [Data management overview](../data-entities-data-packages.md).</span></span> <span data-ttu-id="03bd3-178">このテンプレートでは、顧客データが **CustCustomerV3Entity** テーブルからエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="03bd3-178">In this template, customer data was exported from the **CustCustomerV3Entity** table.</span></span> <span data-ttu-id="03bd3-179">**CustCustomerV3Entity** を設定し、**FullPripriyAdtomer** フィールド マップをマッピングから削除します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-179">Set up **CustCustomerV3Entity**, and remove the **FullPrimaryAddress** field map from the mapping.</span></span> <span data-ttu-id="03bd3-180">**DataAreaId** フィールドを CSV ファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-180">Add the **DataAreaId** field to the CSV file.</span></span> <span data-ttu-id="03bd3-181">エクスポートしたファイル名を **01-CustomersV3Export-Customers V3.csv** にして、**ce-data** と名前をつけた Azure ストレージ アカウントにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-181">Rename the exported file **01-CustomersV3Export-Customers V3.csv**, and upload it to the Azure storage account that you named **ce-data**.</span></span>

    :::image type="content" source="media/boot-customer-file.png" alt-text="Finance and Operations顧客ファイル":::

2. <span data-ttu-id="03bd3-183">[サンプル顧客ファイル](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Bootstrapping/01-CustomersV3Export-Customers%20V3.csv) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="03bd3-183">Download the [sample customer file](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Bootstrapping/01-CustomersV3Export-Customers%20V3.csv).</span></span>

3. <span data-ttu-id="03bd3-184">Azure Data Factory から **CountAccountsPipeline** を実行します。</span><span class="sxs-lookup"><span data-stu-id="03bd3-184">Run **BootstrapAccountsPipeline** from Azure Data Factory.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]