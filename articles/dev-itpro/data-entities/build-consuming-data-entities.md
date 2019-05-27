---
title: データ エンティティのビルドおよび使用
description: このチュートリアルでは、エンティティを構築する方法と、統合シナリオで一部のアウト・オブ・バンド (OOB) エンティティを使用する方法を示します。
author: Sunil-Garg
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 77523
ms.assetid: 1de997fb-d5c4-4668-9759-0758d141a3eb
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4214e61b6f03ffd0ae2468a4c4a36c05ff358c0f
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506220"
---
# <a name="build-and-consume-data-entities"></a><span data-ttu-id="972f0-103">データ エンティティのビルドおよび使用</span><span class="sxs-lookup"><span data-stu-id="972f0-103">Build and consume data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="972f0-104">このチュートリアルでは、エンティティを構築する方法と、統合シナリオで一部のアウト・オブ・バンド (OOB) エンティティを使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="972f0-104">This tutorial shows how to build an entity and how to consume some out-of-band (OOB) entities in an integration scenario.</span></span> <span data-ttu-id="972f0-105">データのインポートとエクスポート、統合、および OData サービスなどのさまざまな統合シナリオで、これらのデータ エンティティが使用される方法もプレビューされます。</span><span class="sxs-lookup"><span data-stu-id="972f0-105">You will also preview how these data entities will be consumed in various integrations scenarios, such as data import and export, integration, and OData services.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="972f0-106">前提条件</span><span class="sxs-lookup"><span data-stu-id="972f0-106">Prerequisites</span></span>
<span data-ttu-id="972f0-107">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-107">This tutorial requires that you access an environment by using Remote Desktop, and that you be provisioned as an administrator on the instance.</span></span>

<span data-ttu-id="972f0-108">このチュートリアルでは、baseUrl はインスタンスのベース URL を指します。</span><span class="sxs-lookup"><span data-stu-id="972f0-108">Throughout this tutorial, baseUrl refers to the base URL of the instance.</span></span>

- <span data-ttu-id="972f0-109">クラウド環境では、ベース URL は Microsoft Dynamics Lifecycle Services (LCS) から取得されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-109">In the cloud environment, the base URL is obtained from Microsoft Dynamics Lifecycle Services (LCS).</span></span>
- <span data-ttu-id="972f0-110">ローカル仮想マシン (VM) の、基準 URL は https://usnconeboxax1aos.cloud.onebox.dynamics.com です。</span><span class="sxs-lookup"><span data-stu-id="972f0-110">On a local virtual machine (VM), the base URL is https://usnconeboxax1aos.cloud.onebox.dynamics.com.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="972f0-111">重要な概念</span><span class="sxs-lookup"><span data-stu-id="972f0-111">Key concepts</span></span>
- <span data-ttu-id="972f0-112">Microsoft Visual Studio のデータ エンティティの開発</span><span class="sxs-lookup"><span data-stu-id="972f0-112">Developing a data entity in Microsoft Visual Studio</span></span>
- <span data-ttu-id="972f0-113">データ管理および OData サービスのデータ エンティティを有効化</span><span class="sxs-lookup"><span data-stu-id="972f0-113">Enabling a data entity for data management and OData services</span></span>
- <span data-ttu-id="972f0-114">統合シナリオでデータ エンティティを消費する</span><span class="sxs-lookup"><span data-stu-id="972f0-114">Consuming a data entity in integration scenarios</span></span>

## <a name="business-problem"></a><span data-ttu-id="972f0-115">ビジネスの問題</span><span class="sxs-lookup"><span data-stu-id="972f0-115">Business problem</span></span>
<span data-ttu-id="972f0-116">フリート管理は、FMCustomer table テーブルに顧客データを、FMAddressTable テーブルにアドレス データを格納します。</span><span class="sxs-lookup"><span data-stu-id="972f0-116">Fleet Management stores customer data in the FMCustomer table and address data in the FMAddressTable table.</span></span> <span data-ttu-id="972f0-117">顧客情報にアクセスまたは更新するには、複数のテーブルにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-117">To access or update customer information, users must access multiple tables.</span></span> <span data-ttu-id="972f0-118">代わりに、機能的に顧客情報を表し、統合ソリューションを構築するために使用できるビジネス オブジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="972f0-118">Instead, you can create a business object that functionally represents customer information, and that you can use to build integration solutions.</span></span>

## <a name="building-the-fmlabcustomer-entity"></a><span data-ttu-id="972f0-119">FMLabCustomer エンティティの作成</span><span class="sxs-lookup"><span data-stu-id="972f0-119">Building the FMLabCustomer entity</span></span>
<span data-ttu-id="972f0-120">このセクションでは、フリート管理モデルで FMLabCustomer のデータ エンティティを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-120">In this section, you must create a data entity for FMLabCustomer in the Fleet Management model.</span></span> <span data-ttu-id="972f0-121">このエンティティは、インポート/エクスポートおよび統合サービスを通じてマスター データを管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-121">This entity will be used to manage master data through import/export and integration services.</span></span> <span data-ttu-id="972f0-122">プライマリ データ ソースが FMCustomer で、セカンダリ データ ソースが FMAddressTable です。</span><span class="sxs-lookup"><span data-stu-id="972f0-122">The primary data source is FMCustomer, and the secondary data source is FMAddressTable.</span></span>

### <a name="data-entity"></a><span data-ttu-id="972f0-123">データ エンティティ</span><span class="sxs-lookup"><span data-stu-id="972f0-123">Data entity</span></span>

<span data-ttu-id="972f0-124">FMLabCustomerEntity</span><span class="sxs-lookup"><span data-stu-id="972f0-124">FMLabCustomerEntity</span></span>

#### <a name="data-entity-fields"></a><span data-ttu-id="972f0-125">データ エンティティ フィールド</span><span class="sxs-lookup"><span data-stu-id="972f0-125">Data entity fields</span></span>

| <span data-ttu-id="972f0-126">氏名</span><span class="sxs-lookup"><span data-stu-id="972f0-126">Name</span></span>          | <span data-ttu-id="972f0-127">マッピング</span><span class="sxs-lookup"><span data-stu-id="972f0-127">Mapping</span></span>                     |
|---------------|-----------------------------|
| <span data-ttu-id="972f0-128">CellPhone</span><span class="sxs-lookup"><span data-stu-id="972f0-128">CellPhone</span></span>     | <span data-ttu-id="972f0-129">FMCustomer.CellPhone</span><span class="sxs-lookup"><span data-stu-id="972f0-129">FMCustomer.CellPhone</span></span>        |
| <span data-ttu-id="972f0-130">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="972f0-130">DriverLicense</span></span> | <span data-ttu-id="972f0-131">FMCustomer.DriverLicense</span><span class="sxs-lookup"><span data-stu-id="972f0-131">FMCustomer.DriverLicense</span></span>    |
| <span data-ttu-id="972f0-132">電子メール</span><span class="sxs-lookup"><span data-stu-id="972f0-132">Email</span></span>         | <span data-ttu-id="972f0-133">FMCustomer.Email</span><span class="sxs-lookup"><span data-stu-id="972f0-133">FMCustomer.Email</span></span>            |
| <span data-ttu-id="972f0-134">名</span><span class="sxs-lookup"><span data-stu-id="972f0-134">FirstName</span></span>     | <span data-ttu-id="972f0-135">FMCustomer.FirstName</span><span class="sxs-lookup"><span data-stu-id="972f0-135">FMCustomer.FirstName</span></span>        |
| <span data-ttu-id="972f0-136">姓</span><span class="sxs-lookup"><span data-stu-id="972f0-136">LastName</span></span>      | <span data-ttu-id="972f0-137">FMCustomer.LastName</span><span class="sxs-lookup"><span data-stu-id="972f0-137">FMCustomer.LastName</span></span>         |
| <span data-ttu-id="972f0-138">CustomerGroup</span><span class="sxs-lookup"><span data-stu-id="972f0-138">CustomerGroup</span></span> | <span data-ttu-id="972f0-139">FMCustomer.CustGroup</span><span class="sxs-lookup"><span data-stu-id="972f0-139">FMCustomer.CustGroup</span></span>        |
| <span data-ttu-id="972f0-140">AddressLine1</span><span class="sxs-lookup"><span data-stu-id="972f0-140">AddressLine1</span></span>  | <span data-ttu-id="972f0-141">FMAddressTable.AddressLine1</span><span class="sxs-lookup"><span data-stu-id="972f0-141">FMAddressTable.AddressLine1</span></span> |
| <span data-ttu-id="972f0-142">AddressLine2</span><span class="sxs-lookup"><span data-stu-id="972f0-142">AddressLine2</span></span>  | <span data-ttu-id="972f0-143">FMAddressTable.AddressLine2</span><span class="sxs-lookup"><span data-stu-id="972f0-143">FMAddressTable.AddressLine2</span></span> |
| <span data-ttu-id="972f0-144">市町村</span><span class="sxs-lookup"><span data-stu-id="972f0-144">City</span></span>          | <span data-ttu-id="972f0-145">FMAddressTable.City</span><span class="sxs-lookup"><span data-stu-id="972f0-145">FMAddressTable.City</span></span>         |
| <span data-ttu-id="972f0-146">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="972f0-146">State</span></span>         | <span data-ttu-id="972f0-147">FMAddressTable.State</span><span class="sxs-lookup"><span data-stu-id="972f0-147">FMAddressTable.State</span></span>        |
| <span data-ttu-id="972f0-148">ZipCode</span><span class="sxs-lookup"><span data-stu-id="972f0-148">ZipCode</span></span>       | <span data-ttu-id="972f0-149">FMAddressTable.ZipCode</span><span class="sxs-lookup"><span data-stu-id="972f0-149">FMAddressTable.ZipCode</span></span>      |
| <span data-ttu-id="972f0-150">国</span><span class="sxs-lookup"><span data-stu-id="972f0-150">Country</span></span>       | <span data-ttu-id="972f0-151">FMAddressTable.Country</span><span class="sxs-lookup"><span data-stu-id="972f0-151">FMAddressTable.Country</span></span>      |

#### <a name="corresponding-staging-table"></a><span data-ttu-id="972f0-152">対応するステージング テーブル</span><span class="sxs-lookup"><span data-stu-id="972f0-152">Corresponding staging table</span></span>

<span data-ttu-id="972f0-153">ステージング テーブルは、ファイルの解析と変換時に中間ストレージを提供するため、インポート/エクスポートのシナリオで使用されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-153">Staging tables are used in import/export scenarios to provide intermediary storage during file parsing and transformation.</span></span> <span data-ttu-id="972f0-154">これらのテーブルは、コネクター統合シナリオでも使用されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-154">These tables are also used in connector integration scenarios.</span></span> <span data-ttu-id="972f0-155">多くの場合、ステージング テーブルはエンティティに対して 1 対 1 でマップされます。</span><span class="sxs-lookup"><span data-stu-id="972f0-155">In many cases, staging table are mapped 1:1 to an entity.</span></span> <span data-ttu-id="972f0-156">**FMLabCustomerEntity** エンティティに対応するステージング テーブルの名前は FMLabCustomerStaging です。</span><span class="sxs-lookup"><span data-stu-id="972f0-156">The staging table that corresponds to the **FMLabCustomerEntity** entity is named FMLabCustomerStaging.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="972f0-157">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="972f0-157">Create a new project</span></span>

1. <span data-ttu-id="972f0-158">Visual Studio で、**ファイル** &gt; **新規** &gt; **プロジェクト** の順にクリックしてから、**Finance and Operations のプロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-158">In Visual Studio click **File** &gt; **New** &gt; **Project**, and then select **Finance and Operations Project**.</span></span>
2. <span data-ttu-id="972f0-159">プロジェクトを右クリックして **プロパティ** をクリックし、プロジェクトがフリート管理モデルであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="972f0-159">Right-click the project, click **Properties**, and verify that the project is in the Fleet Management model.</span></span> <span data-ttu-id="972f0-160">設定されていない場合、**モデル** プロパティを**フリート管理**に設定します。</span><span class="sxs-lookup"><span data-stu-id="972f0-160">If it isn't, set the **Model** property to **Fleet Management**.</span></span>

### <a name="add-a-new-data-entity-to-your-project"></a><span data-ttu-id="972f0-161">プロジェクトへの新しいデータ エンティティの追加</span><span class="sxs-lookup"><span data-stu-id="972f0-161">Add a new data entity to your project</span></span>

1. <span data-ttu-id="972f0-162">**FMLabCustomerEntity** という名前の新しいエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="972f0-162">Create a new entity that is named **FMLabCustomerEntity**.</span></span> <span data-ttu-id="972f0-163">プロジェクトを右クリックし、**追加** &gt; **新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-163">Right-click you project, and then click **Add** &gt; **New item**.</span></span> <span data-ttu-id="972f0-164">**新しい項目の追加** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="972f0-164">The **Add New Item** dialog box opens.</span></span>
2. <span data-ttu-id="972f0-165">**データ エンティティ** を選択し、**名前** プロパティを **FMLabCustomerEntity** に設定します。</span><span class="sxs-lookup"><span data-stu-id="972f0-165">Select **Data Entity**, and then set the **Name** property to **FMLabCustomerEntity**.</span></span>
3. <span data-ttu-id="972f0-166">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-166">Click **Add**.</span></span>
4. <span data-ttu-id="972f0-167">**データ エンティティ** ウィザードで、作成しているデータ エンティティのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="972f0-167">In the **Data entity** wizard, specify the properties for the data entity that you're creating.</span></span> <span data-ttu-id="972f0-168">次のスクリーン ショットに表示される値を使用します。</span><span class="sxs-lookup"><span data-stu-id="972f0-168">Use the values that are shown in the following screen shot.</span></span>

    > [!NOTE]
    > <span data-ttu-id="972f0-169">エンティティの名前に「_」や数字 (0...9) を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="972f0-169">The name of an entity must not have '_' or any numeric digits (0…9).</span></span> <span data-ttu-id="972f0-170">これらの文字を使用すると、後でマッピング エラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="972f0-170">Using these characters may result in mapping errors later.</span></span>

    <span data-ttu-id="972f0-171">[![データ エンティティ ウィザード](./media/data-entity-wizard.png)](./media/data-entity-wizard.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-171">[![Data Entity Wizard](./media/data-entity-wizard.png)](./media/data-entity-wizard.png)</span></span>

5. <span data-ttu-id="972f0-172">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-172">Click **Next**.</span></span> <span data-ttu-id="972f0-173">各プロパティ機能の詳細については、[データ エンティティ](data-entities.md)の「エンティティのカテゴリ」および「エンティティの作成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="972f0-173">For more information about the function of each property, see "Categories of entities" and "Building an entity" in [Data entities](data-entities.md).</span></span>
6. <span data-ttu-id="972f0-174">次のスクリーン ショットに示すように、データ ソースから新しいエンティティにフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="972f0-174">Add fields to the new entity from your data source, as shown in the following screen shot.</span></span> <span data-ttu-id="972f0-175">主要なデータ ソース、**FMCustomer** からフィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="972f0-175">You can add fields from the primary data source, **FMCustomer**.</span></span> <span data-ttu-id="972f0-176">このエンティティについては、テストを効率化するため**画像**および **LicenseImage** コンテナー タイプのチェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="972f0-176">For this entity, clear the check box for the **Image** and **LicenseImage** container types to simplify testing.</span></span>
7. <span data-ttu-id="972f0-177">データ エンティティのフィールドの名前を、パブリック データ コントラクト標準を反映するように変更するか、**ラベルをフィールド名に変換** をクリックして既存のラベルから名前を生成します。</span><span class="sxs-lookup"><span data-stu-id="972f0-177">Rename the data entity fields to reflect public data contract standards, or click **Convert labels to field names** to generate names from the existing labels.</span></span>
8. <span data-ttu-id="972f0-178">**DriverLicense** フィールドの行で、**必須**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-178">On the line for the **DriverLicense** field, select the **Is mandatory** check box.</span></span> <span data-ttu-id="972f0-179">このフィールドはエンティティのナチュラル キーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-179">This field will be used as the natural key for the entity.</span></span>

    <span data-ttu-id="972f0-180">[![データ エンティティ ウィザード 2](./media/data-entity-wizard-2.png)](./media/data-entity-wizard-2.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-180">[![Data Entity Wizard 2](./media/data-entity-wizard-2.png)](./media/data-entity-wizard-2.png)</span></span>

9. <span data-ttu-id="972f0-181">**データ ソース** フィールドで、**PrimaryAddress** を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-181">In the **Data source** field, select **PrimaryAddress**.</span></span> <span data-ttu-id="972f0-182">**AddressID** の自動拡張または代理外部キー交換のため、**PrimaryAddress** データ ソースが自動的に追加されることに注意します。</span><span class="sxs-lookup"><span data-stu-id="972f0-182">Notice that the **PrimaryAddress** data source is automatically added because of automatic expansion or the surrogate foreign key replacement of **AddressID**.</span></span>

    <span data-ttu-id="972f0-183">[![手順およびフィールドの追加](./media/steps-and-add-fields.png)](./media/steps-and-add-fields.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-183">[![Steps and add fields](./media/steps-and-add-fields.png)](./media/steps-and-add-fields.png)</span></span>

10. <span data-ttu-id="972f0-184">エンティティの一部にする **PrimaryAddress** データ ソースからフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-184">Select the fields from the **PrimaryAddress** data source that you want to be part of your entity.</span></span> <span data-ttu-id="972f0-185">また、次のフィールドの名前を変更して、適切な公開データ契約の名前付けを反映します。</span><span class="sxs-lookup"><span data-stu-id="972f0-185">Additionally, rename the following fields to reflect proper public data contract naming:</span></span>

    - <span data-ttu-id="972f0-186">PrimaryAddress \_AddressLine1 &gt; AddressLine1</span><span class="sxs-lookup"><span data-stu-id="972f0-186">PrimaryAddress \_AddressLine1 &gt; AddressLine1</span></span>
    - <span data-ttu-id="972f0-187">PrimaryAddress \_AddressLine2 &gt; AddressLine2</span><span class="sxs-lookup"><span data-stu-id="972f0-187">PrimaryAddress \_AddressLine2 &gt; AddressLine2</span></span>
    - <span data-ttu-id="972f0-188">PrimaryAddress \_City &gt; City</span><span class="sxs-lookup"><span data-stu-id="972f0-188">PrimaryAddress \_City &gt; City</span></span>
    - <span data-ttu-id="972f0-189">PrimaryAddress \_State &gt; State</span><span class="sxs-lookup"><span data-stu-id="972f0-189">PrimaryAddress \_State &gt; State</span></span>
    - <span data-ttu-id="972f0-190">PrimaryAddress \_ZipCode &gt; ZipCode</span><span class="sxs-lookup"><span data-stu-id="972f0-190">PrimaryAddress \_ZipCode &gt; ZipCode</span></span>
    - <span data-ttu-id="972f0-191">PrimaryAddress \_Country &gt; Country</span><span class="sxs-lookup"><span data-stu-id="972f0-191">PrimaryAddress \_Country &gt; Country</span></span>

    ![データ エンティティ ウィザード](./media/data-entity-wizard-3.png)

11. <span data-ttu-id="972f0-193">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-193">Click **Finish**.</span></span> <span data-ttu-id="972f0-194">データ エンティティの品目およびステージング テーブルは、プロジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-194">A data entity item and staging table are added to the project.</span></span>

    <span data-ttu-id="972f0-195">[![ソリューション エクスプローラー](./media/solution-explorer.png)](./media/solution-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-195">[![Solution explorer](./media/solution-explorer.png)](./media/solution-explorer.png)</span></span>

### <a name="build-your-project"></a><span data-ttu-id="972f0-196">プロジェクトの構築</span><span class="sxs-lookup"><span data-stu-id="972f0-196">Build your project</span></span>

1. <span data-ttu-id="972f0-197">ソリューション エクスプローラーで、プロジェクトを右クリックしてから**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-197">In Solution Explorer, right-click your project, and then click **Properties**.</span></span>
2. <span data-ttu-id="972f0-198">**ビルドでのデータベースの同期**プロパティの値を **True** に変更し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-198">Change the value of the **Synchronize database on build** property to **True**, and then click **OK**.</span></span> <span data-ttu-id="972f0-199">このプロパティは、プロジェクトごとに 1 回のみ設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-199">This property must be set only one time per project.</span></span>

    > [!NOTE]
    > <span data-ttu-id="972f0-200">エンティティが Microsoft SQL Server のビューとして作成され、ステージング テーブルが追加されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-200">Entities are created as views in Microsoft SQL Server, and staging tables are also added.</span></span> <span data-ttu-id="972f0-201">したがって、エンティティを作成するときにデータベースを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-201">Therefore, you must sync a database when you build entities.</span></span>

    ![プロパティ ページ](./media/property-pages.png)

3. <span data-ttu-id="972f0-203">Visual Studio ツールバーで、**構築** &gt; **ソリューションの構築** の順にクリックしてプロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="972f0-203">On the Visual Studio toolbar, click **Build** &gt; **Build Solution** to build the project.</span></span>
4. <span data-ttu-id="972f0-204">ビルドにエラーが含まれていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="972f0-204">Verify that the build doesn't contain any errors.</span></span> <span data-ttu-id="972f0-205">この時点でチュートリアルは警告が許可されています。</span><span class="sxs-lookup"><span data-stu-id="972f0-205">At this point in the tutorial, warnings are allowed.</span></span>

### <a name="visually-validate-and-customize-an-entity"></a><span data-ttu-id="972f0-206">目視による検証とエンティティのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="972f0-206">Visually validate and customize an entity</span></span>

1. <span data-ttu-id="972f0-207">ソリューション エクスプローラーで、**FMLabCustomerEntity** ノードを右クリックしてから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-207">In Solution Explorer, right-click the **FMLabCustomerEntity** node, and then click **Open**.</span></span> <span data-ttu-id="972f0-208">エンティティのデザイナーが中央のウィンドウに開きます。</span><span class="sxs-lookup"><span data-stu-id="972f0-208">The designer for the entity opens in the middle pane.</span></span>
2. <span data-ttu-id="972f0-209">**FMLabCustomerEntity** エンティティのプロパティを検証します。</span><span class="sxs-lookup"><span data-stu-id="972f0-209">Validate the properties of the **FMLabCustomerEntity** entity.</span></span> <span data-ttu-id="972f0-210">ソリューション エクスプ ローラーでエンティティを選択し、**プロパティ** ウィンドウの値と次のスクリーンショットを比較します。</span><span class="sxs-lookup"><span data-stu-id="972f0-210">Select the entity in Solution Explorer, and compare the **Properties** pane values to the following screen shot.</span></span>
3. <span data-ttu-id="972f0-211">**ラベル** プロパティを **フリート ラボ顧客** に設定します。</span><span class="sxs-lookup"><span data-stu-id="972f0-211">Set the **Label** property to **Fleet Lab Customers**.</span></span>

    <span data-ttu-id="972f0-212">[![FMLabCustomerEntity - プロパティ](./media/fmlabcustomerentity-properties.png)](./media/fmlabcustomerentity-properties.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-212">[![FMLabCustomerEntity - Properties](./media/fmlabcustomerentity-properties.png)](./media/fmlabcustomerentity-properties.png)</span></span>

4. <span data-ttu-id="972f0-213">左ウィンドウで、**データ ソース** &gt; **FMCustomer** &gt; **データ ソース** &gt; **FMAddressTable** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-213">In the left pane, click **Data Sources** &gt; **FMCustomer** &gt; **Data Sources** &gt; **FMAddressTable**.</span></span>
5. <span data-ttu-id="972f0-214">**読み取り専用**プロパティを**いいえ**に変更します。</span><span class="sxs-lookup"><span data-stu-id="972f0-214">Change the **Is Read Only** property to **No**.</span></span> <span data-ttu-id="972f0-215">これは、既知の問題です。</span><span class="sxs-lookup"><span data-stu-id="972f0-215">This is a known issue.</span></span> <span data-ttu-id="972f0-216">最終的に、この値は結合のタイプに基づき、自動的に**はい**または**いいえ**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-216">Eventually, the value will be set to **Yes** or **No** automatically, based on the type of join.</span></span> <span data-ttu-id="972f0-217">合成シナリオの場合、値は **Yes**、アソシエーションの場合、値は **No** にしてください (代理外部キー拡張)。</span><span class="sxs-lookup"><span data-stu-id="972f0-217">The value should be **Yes** for composition scenarios, and **No** for associations (surrogate foreign key expansions).</span></span> <span data-ttu-id="972f0-218">このプロパティを使用すると、データ ソースを読み取り/書き込みをすることができます。</span><span class="sxs-lookup"><span data-stu-id="972f0-218">This property enables the data source to be read/write.</span></span>

    <span data-ttu-id="972f0-219">[![FMLabCustomerEntity - プロパティ 2](./media/fmlabcustomerentity-properties2.png)](./media/fmlabcustomerentity-properties2.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-219">[![FMLabCustomerEntity - Properties2](./media/fmlabcustomerentity-properties2.png)](./media/fmlabcustomerentity-properties2.png)</span></span>

6. <span data-ttu-id="972f0-220">**FMLabCustomerEntity** デザイナーで、**キー** &gt; **EntityKey** とクリックしてから**フィールド** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="972f0-220">In the **FMLabCustomerEntity** designer, click **Keys** &gt; **EntityKey**, and then expand the **Fields** node.</span></span> <span data-ttu-id="972f0-221">フィールドの一覧が次のスクリーン ショットと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="972f0-221">Verify that the list of fields matches the following screen shot.</span></span>

    <span data-ttu-id="972f0-222">[![FMLabCustomerEntity](./media/fmlabcustomerentity.png)](./media/fmlabcustomerentity.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-222">[![FMLabCustomerEntity](./media/fmlabcustomerentity.png)](./media/fmlabcustomerentity.png)</span></span>

7. <span data-ttu-id="972f0-223">インポート/エクスポートに使用するステージング テーブルを視覚的に検証するには、デザイナーの **FMLabCustomerStaging** テーブルを開き、**FMLabCustomerStaging** ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-223">To visually validate the staging table that will be used for import/export, open the **FMLabCustomerStaging** table in the designer, and then select the **FMLabCustomerStaging** node.</span></span>

    <span data-ttu-id="972f0-224">[![fMLabCustomerStaging - プロパティ](./media/fmlabcustomerstaging-properties.png)](./media/fmlabcustomerstaging-properties.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-224">[![fMLabCustomerStaging - Properties](./media/fmlabcustomerstaging-properties.png)](./media/fmlabcustomerstaging-properties.png)</span></span>

8. <span data-ttu-id="972f0-225">**FMLabCustomerStaging** &gt; **フィールド**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-225">Click **FMLabCustomerStaging** &gt; **Fields**.</span></span> <span data-ttu-id="972f0-226">次のスクリーン ショットでは、ステージング テーブルの標準フィールドが選択されています。</span><span class="sxs-lookup"><span data-stu-id="972f0-226">In the following screen shot, the standard fields of the staging tables are selected.</span></span> <span data-ttu-id="972f0-227">すべてのエンティティ ステージング テーブルにはこれらの標準的なフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="972f0-227">All entity staging tables have these standard fields.</span></span> <span data-ttu-id="972f0-228">スクリーンショットには、このデー タエンティティに属するデータ フィールドも表示されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-228">The screen shot also shows the data fields that belong on this data entity.</span></span>

    <span data-ttu-id="972f0-229">[![FMLabCustomerStaging](./media/fmlabcustomerstaging.png)](./media/fmlabcustomerstaging.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-229">[![FMLabCustomerStaging](./media/fmlabcustomerstaging.png)](./media/fmlabcustomerstaging.png)</span></span>

9. <span data-ttu-id="972f0-230">ソリューション エクスプローラーで、プロジェクトを右クリックしてから、**再構築**を選択して、プロジェクトを再構築して同期します。</span><span class="sxs-lookup"><span data-stu-id="972f0-230">In Solution Explorer, right-click your project, and then select **Rebuild** to rebuild and synchronize the project.</span></span>

## <a name="testing-data-entities"></a><span data-ttu-id="972f0-231">データ エンティティのテスト</span><span class="sxs-lookup"><span data-stu-id="972f0-231">Testing data entities</span></span>
<span data-ttu-id="972f0-232">エンティティは、データのインポート/エキスポートまたは統合を通じ、X++ のさまざまなメソッドを使用してテストできます。</span><span class="sxs-lookup"><span data-stu-id="972f0-232">Entities can be tested by using various methods in X++, through data import/export, or through integrations.</span></span> <span data-ttu-id="972f0-233">このセクションでは、エンティティを検証するためのシナリオについて調べます。</span><span class="sxs-lookup"><span data-stu-id="972f0-233">In this section, we'll explore scenarios for validating entities.</span></span>

### <a name="test-the-entity-by-using-x-code"></a><span data-ttu-id="972f0-234">X++ コードを使用してエンティティをテスト</span><span class="sxs-lookup"><span data-stu-id="972f0-234">Test the entity by using X++ code</span></span>

<span data-ttu-id="972f0-235">データ エンティティとの対話の最も一般的な方法の 1 つは、単体テストまたは実行可能なジョブを使用してエンティティが構築されたことを検証することによって、x++ を使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="972f0-235">One of the most common ways of interacting with data entities is through X++, by using a unit test or a runnable job to validate that the entities have been built.</span></span> <span data-ttu-id="972f0-236">この例では、実行可能なジョブを使用します。</span><span class="sxs-lookup"><span data-stu-id="972f0-236">In this example, we will use a runnable job.</span></span>

1. <span data-ttu-id="972f0-237">ソリューション エクスプローラーで、**追加** &gt; **新しい項目** &gt; **実行可能なクラス**をクリックして、実行可能なクラスをプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="972f0-237">In Solution Explorer, click **Add** &gt; **New item** &gt; **Runnable class** to add a runnable class to your project.</span></span>
2. <span data-ttu-id="972f0-238">次のコードをコピーしてクラスに貼り付け、データ エンティティをテストします。</span><span class="sxs-lookup"><span data-stu-id="972f0-238">Copy and paste the following code into the class to test your data entity.</span></span>

    ```
    public static void main(Args _args)
    {
        FMLabCustomerEntity customer;
        str license = "License";
        Random r = new Random();
        int rand = r.nextInt();
        license = license + int2str(rand);

        //Create a new record in FM lab customer entity
        customer.clear();
        customer.FirstName = "Bob";
        customer.LastName = "Smith";
        customer.DriverLicense = license;
        customer.insert();

        info(strfmt("Tried to insert customer '%1 %2' with license %3", 
            customer.FirstName, customer.LastName, customer.DriverLicense));

        //Display newly created record
        select forupdate customer where customer.DriverLicense==license;
        info(strfmt("Found newly created customer '%1 %2' with license %3", 
            customer.FirstName, customer.LastName, customer.DriverLicense));

        //Now delete the record from the entity
        customer.delete();
        select customer where customer.DriverLicense==license ;
        info(strfmt("Deleted customer does not exist: license- %1", customer.DriverLicense));
    }
    ```

3. <span data-ttu-id="972f0-239">スタートアップ オブジェクトとして設定するためデバッガーでコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="972f0-239">Run the code in debugger to set it as a startup object.</span></span>
4. <span data-ttu-id="972f0-240">エンティティを検証するには、デバッガー ウィンドウまたは Web サイトの通知で Infolog を調べます。</span><span class="sxs-lookup"><span data-stu-id="972f0-240">To validate the entity, view the Infolog in the debugger window or in notifications on the website.</span></span> <span data-ttu-id="972f0-241">3 つの成功メッセージが記録されていることが確認されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-241">You will see that three successful messages are logged.</span></span> <span data-ttu-id="972f0-242">実行されたアクションも表示されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-242">You will also see the actions that were taken.</span></span>

## <a name="importing-data-by-using-entities"></a><span data-ttu-id="972f0-243">エンティティを使用したデータのインポート</span><span class="sxs-lookup"><span data-stu-id="972f0-243">Importing data by using entities</span></span>
<span data-ttu-id="972f0-244">**データ管理を有効**プロパティを持つデータ エンティティは、さまざまなファイル形式のデータをインポートおよびエクスポートするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="972f0-244">Data entities that have the **Data Management Enabled** property can be used to import and export data in various file formats.</span></span> <span data-ttu-id="972f0-245">このセクションでは、**FMLabCustomer** エンティティについて CSV ファイル形式でデータをインポートします。</span><span class="sxs-lookup"><span data-stu-id="972f0-245">In this section, you will import data in a CSV file format for the **FMLabCustomer** entity.</span></span>

### <a name="file-import"></a><span data-ttu-id="972f0-246">ファイル インポート</span><span class="sxs-lookup"><span data-stu-id="972f0-246">File import</span></span>

<span data-ttu-id="972f0-247">データ エンティティを作成した後は、インポート/エクスポートを検証することができます。</span><span class="sxs-lookup"><span data-stu-id="972f0-247">After you create your data entity, you can validate import/export.</span></span>

1. <span data-ttu-id="972f0-248">インポートすることができる CSV ファイルのサンプルを作成します。</span><span class="sxs-lookup"><span data-stu-id="972f0-248">Create a sample CSV file that you can import.</span></span> <span data-ttu-id="972f0-249">次のテキストをコピーし、**FM Lab Customer Import.csv** として保存します。</span><span class="sxs-lookup"><span data-stu-id="972f0-249">Copy the following text, and save it as **FM Lab Customer Import.csv**.</span></span>

    ```
    CELLPHONE,DRIVERSLICENSE,EMAIL,FIRSTNAME,LASTNAME,CUSTOMERGROUP,ADDRESSLINE1,ADDRESSLINE2,CITY,STATE,ZIPCODE,COUNTRY(999) 555-0100,S615-3939-2349,chris.spencer@adatum.com,Chris,Spencer,adv\_mem\_1,444 Main Street,,Orlando,FL,77899,US(188) 555-0101,S615-3939-2350,Ichiro.lannin@blueyonderairlines.com,Ichiro,Lannin,non\_mem\_1,12 Long Street,,New York City,NY,99087,US(777) 555-0102,S615-3939-2351,josh.smith@fourthcoffee.com,Josh,Smith,adv\_mem\_1,9606 122th Avenue,,Sydney,TX,99874,US(456) 555-0103,S615-3939-2352,Vince@fabrikam.us,Vince,Ahmed,non\_mem\_1,123 Microsoft Way,Unit 87,Seattle,WA,90001,US(345) 555-0104,S615-3939-2353,tony.parker@lucernepublishing.com,Tony,Parker,non\_mem\_1,12012 11th PLNE,Apt 160,San Francisco,CA,75645,US(312) 555-0105,S615-3939-2354,Julia@fineartschool.net,Julia,Natarajan,exec\_mem\_1,449 Long Street,Apt 160,Bruxelles,ID,34213,US
    ```

2. <span data-ttu-id="972f0-250">**ユーザー ダッシュ ボード** &gt; **データ管理**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-250">Click **User Dashboard** &gt; **Data management**.</span></span>
3. <span data-ttu-id="972f0-251">**データ管理**ワークスペースで、**インポート** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-251">In the **Data Management** workspace, click the **Import** tile.</span></span>
4. <span data-ttu-id="972f0-252">**インポート** ページで、次のスクリーン ショットに表示されるインポートの詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="972f0-252">On the **Import** page, enter the import details, as shown in the following screen shot.</span></span>

    ![新しいレコードのインポート](./media/import-new-record.png)

5. <span data-ttu-id="972f0-254">**エンティティ ファイルのアップロード** フィールドの隣にある **データのアップロード** ボタンをクリックし、作成した CSV ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-254">Click the **Upload data** button next to the **Upload file for entity** field, and select the CSV file that you created.</span></span>
6. <span data-ttu-id="972f0-255">ファイルがアップロードされると、エンティティが中間セクションに追加された事が表示されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-255">After the file is uploaded, you will notice that the entity is added to the middle section.</span></span> <span data-ttu-id="972f0-256">また、マッピングが無効であることを示すエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-256">You will also receive an error that states that the mapping isn't valid.</span></span> <span data-ttu-id="972f0-257">いくつかのフィールドは、ソース ファイルとターゲット エンティティの間で正しくマップされていません。</span><span class="sxs-lookup"><span data-stu-id="972f0-257">A few fields aren't mapped correctly between the source file and the target entity.</span></span>
7. <span data-ttu-id="972f0-258">エンティティ リストで**マップの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-258">In the entities list, click **View map**.</span></span>
8. <span data-ttu-id="972f0-259">**AddressLine1** および **AddressLine2** は、ターゲット フィールドにマップされていないソース内の 2 つのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="972f0-259">**AddressLine1** and **AddressLine2** are two fields in the source that aren't mapped to target fields.</span></span> <span data-ttu-id="972f0-260">ビジュアル マッパー、または詳細表示で、これらのフィールドを次のようにマップして**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-260">In the visual mapper, or details view, map these fields as follows, and then click **Save**:</span></span>

    - <span data-ttu-id="972f0-261">AddressLine1 – Address1</span><span class="sxs-lookup"><span data-stu-id="972f0-261">AddressLine1 – Address1</span></span>
    - <span data-ttu-id="972f0-262">AddressLine2 – Address2</span><span class="sxs-lookup"><span data-stu-id="972f0-262">AddressLine2 – Address2</span></span>

    <span data-ttu-id="972f0-263">[![ソースをステージングにマップ](./media/map-source-to-staging.png)](./media/map-source-to-staging.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-263">[![Map source to staging](./media/map-source-to-staging.png)](./media/map-source-to-staging.png)</span></span>

9. <span data-ttu-id="972f0-264">ブラウザーの **戻る** ボタンをクリックして、**インポート ジョブ** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="972f0-264">Click the **Back** button in your browser to go back to the **Import job** page.</span></span> <span data-ttu-id="972f0-265">エンティティ リストのチェック マークは、エンティティがインポートの準備ができていることを示します。</span><span class="sxs-lookup"><span data-stu-id="972f0-265">The check mark in the entities list indicates that the entity is now ready for import.</span></span>

    <span data-ttu-id="972f0-266">[![新規レコード 2 のインポート](./media/import-new-record-2.png)](./media/import-new-record-2.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-266">[![Import new record 2](./media/import-new-record-2.png)](./media/import-new-record-2.png)</span></span>

10. <span data-ttu-id="972f0-267">**今すぐインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-267">Click **Import Now**.</span></span> <span data-ttu-id="972f0-268">インポートが完了したら、ジョブ ステータス ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="972f0-268">After the import is completed, the job status page opens.</span></span>

## <a name="consuming-entities-by-using-odata"></a><span data-ttu-id="972f0-269">OData を使用してエンティティを消費する</span><span class="sxs-lookup"><span data-stu-id="972f0-269">Consuming entities by using OData</span></span>
<span data-ttu-id="972f0-270">このセクションでは、OData のエンティティを公開して使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="972f0-270">In this section, you will learn how to expose and consume an entity for OData.</span></span> <span data-ttu-id="972f0-271">開始する前に、クライアントからフリート デモ データが読み込まれたことを確認します。\[baseURL\]/?f=FMSetup</span><span class="sxs-lookup"><span data-stu-id="972f0-271">Before you begin, verify that the Fleet demo data is loaded from the client: \[baseURL\]/?f=FMSetup</span></span>

### <a name="review-the-fleetrental-entity-and-add-a-navigation-property-for-odata"></a><span data-ttu-id="972f0-272">FleetRental エンティティを確認し、OData のナビゲーション プロパティを追加</span><span class="sxs-lookup"><span data-stu-id="972f0-272">Review the FleetRental entity and add a navigation property for OData</span></span>

<span data-ttu-id="972f0-273">既存の **FleetRental** エンティティをレビューしてから、1 つのデータ エンティティと別のデータ エンティティ間のリレーションシップを作成します。</span><span class="sxs-lookup"><span data-stu-id="972f0-273">You will review the existing **FleetRental** entity and then create a relationship from one data entity to another.</span></span> <span data-ttu-id="972f0-274">この関係は、OData エンティティのナビゲーション プロパティとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-274">This relationship will be used as a navigation property for OData entities.</span></span>

1. <span data-ttu-id="972f0-275">ソリューション エクスプローラーで、**FMEntityLab** プロジェクトの中であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="972f0-275">In Solution Explorer, verify that you're in the **FMEntityLab** project.</span></span>
2. <span data-ttu-id="972f0-276">アプリケーション エクスプローラーで、**FMRentalEntity** を検索して右クリックしてから、**プロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-276">In Application Explorer, search for **FMRentalEntity**, right-click it, and then select **Add to Project**.</span></span>
3. <span data-ttu-id="972f0-277">アプリケーション エクスプローラーで、**FMCustomerEntity** を検索して右クリックしてから、**プロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-277">In Application Explorer, search for **FMCustomerEntity**, right-click it, and then select **Add to project**.</span></span>
4. <span data-ttu-id="972f0-278">ソリューション エクスプローラーで、**FMRentalEntity** を右クリックしてから、**開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-278">In Solution Explorer, right-click **FMRentalEntity**, and then select **Open**.</span></span>
5. <span data-ttu-id="972f0-279">ビュー デザイナーで、ルート ノード **FMRentalEntity** を選択し、次のプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="972f0-279">In the view designer, select the root node, **FMRentalEntity**, and review the following properties.</span></span>

    | <span data-ttu-id="972f0-280">プロパティ</span><span class="sxs-lookup"><span data-stu-id="972f0-280">Property</span></span>               | <span data-ttu-id="972f0-281">先頭値</span><span class="sxs-lookup"><span data-stu-id="972f0-281">Value</span></span>        | <span data-ttu-id="972f0-282">説明</span><span class="sxs-lookup"><span data-stu-id="972f0-282">Description</span></span> |
    |------------------------|--------------|-------------|
    | <span data-ttu-id="972f0-283">IsPublic</span><span class="sxs-lookup"><span data-stu-id="972f0-283">IsPublic</span></span>               | <span data-ttu-id="972f0-284">有</span><span class="sxs-lookup"><span data-stu-id="972f0-284">Yes</span></span>          | <span data-ttu-id="972f0-285">このプロパティを **はい** に設定すると、OData アプリケーション プログラミング インターフェイス (API) を使用して、エンティティを表示できます。</span><span class="sxs-lookup"><span data-stu-id="972f0-285">When this property is set to **Yes**, the entity is visible by using the OData application programming interface (API).</span></span> |
    | <span data-ttu-id="972f0-286">パブリック エンティティ名</span><span class="sxs-lookup"><span data-stu-id="972f0-286">Public Entity Name</span></span>     | <span data-ttu-id="972f0-287">FleetRental</span><span class="sxs-lookup"><span data-stu-id="972f0-287">FleetRental</span></span>  | <span data-ttu-id="972f0-288">**EntityType** の OData API で使用される名前。</span><span class="sxs-lookup"><span data-stu-id="972f0-288">The name that will be used in the OData APIs for **EntityType**.</span></span> |
    | <span data-ttu-id="972f0-289">パブリック コレクション名</span><span class="sxs-lookup"><span data-stu-id="972f0-289">Public Collection Name</span></span> | <span data-ttu-id="972f0-290">FleetRentals</span><span class="sxs-lookup"><span data-stu-id="972f0-290">FleetRentals</span></span> | <span data-ttu-id="972f0-291">OData コレクション エンティティに使用される名前。</span><span class="sxs-lookup"><span data-stu-id="972f0-291">The name that will be used for the OData collection entity.</span></span> |

6. <span data-ttu-id="972f0-292">ビュー デザイナーで、**関係**ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="972f0-292">In the view designer, expand the **Relations** node.</span></span>
7. <span data-ttu-id="972f0-293">**顧客関係** を選択し、**削除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-293">Select **Customer Relation**, and then click **Delete**.</span></span>
8. <span data-ttu-id="972f0-294">**関係** を右クリックし、**新規** &gt; **関係** を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-294">Right-click **Relations**, and then select **New** &gt; **Relation**.</span></span>
9. <span data-ttu-id="972f0-295">**関係 1** を選択し、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="972f0-295">Select **Relation1**, and set the following properties.</span></span>

    | <span data-ttu-id="972f0-296">プロパティ</span><span class="sxs-lookup"><span data-stu-id="972f0-296">Property</span></span>                        | <span data-ttu-id="972f0-297">先頭値</span><span class="sxs-lookup"><span data-stu-id="972f0-297">Value</span></span>            |
    |---------------------------------|------------------|
    | <span data-ttu-id="972f0-298">基数</span><span class="sxs-lookup"><span data-stu-id="972f0-298">Cardinality</span></span>                     | <span data-ttu-id="972f0-299">ZeroMore</span><span class="sxs-lookup"><span data-stu-id="972f0-299">ZeroMore</span></span>         |
    | <span data-ttu-id="972f0-300">氏名</span><span class="sxs-lookup"><span data-stu-id="972f0-300">Name</span></span>                            | <span data-ttu-id="972f0-301">CustomerRelation</span><span class="sxs-lookup"><span data-stu-id="972f0-301">CustomerRelation</span></span> |
    | <span data-ttu-id="972f0-302">関連するデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="972f0-302">Related Data Entity</span></span>             | <span data-ttu-id="972f0-303">FMCustomerEntity</span><span class="sxs-lookup"><span data-stu-id="972f0-303">FMCustomerEntity</span></span> |
    | <span data-ttu-id="972f0-304">関連データ エンティティ カーディナリティ</span><span class="sxs-lookup"><span data-stu-id="972f0-304">Related Data Entity Cardinality</span></span> | <span data-ttu-id="972f0-305">ExactlyOne</span><span class="sxs-lookup"><span data-stu-id="972f0-305">ExactlyOne</span></span>       |
    | <span data-ttu-id="972f0-306">関連するデータ エンティティ ロール</span><span class="sxs-lookup"><span data-stu-id="972f0-306">Related Data Entity Role</span></span>        | <span data-ttu-id="972f0-307">CustomerRole</span><span class="sxs-lookup"><span data-stu-id="972f0-307">CustomerRole</span></span>     |
    | <span data-ttu-id="972f0-308">関係のタイプ</span><span class="sxs-lookup"><span data-stu-id="972f0-308">Relationship Type</span></span>               | <span data-ttu-id="972f0-309">関連</span><span class="sxs-lookup"><span data-stu-id="972f0-309">Association</span></span>      |
    | <span data-ttu-id="972f0-310">役割</span><span class="sxs-lookup"><span data-stu-id="972f0-310">Role</span></span>                            | <span data-ttu-id="972f0-311">レンタル</span><span class="sxs-lookup"><span data-stu-id="972f0-311">Rental</span></span>           |

10. <span data-ttu-id="972f0-312">ビュー デザイナーで、**CustomerRelation** ノードを右クリックしてから、**新規** &gt; **標準**を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-312">In the view designer, right-click the **CustomerRelation** node, and then select **New** &gt; **Normal**.</span></span>
11. <span data-ttu-id="972f0-313">**CustomerRelation** で新しいノードを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-313">Right-click the new node under **CustomerRelation**, and then select **Properties**.</span></span>
12. <span data-ttu-id="972f0-314">次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="972f0-314">Set the following properties.</span></span>

    | <span data-ttu-id="972f0-315">プロパティ</span><span class="sxs-lookup"><span data-stu-id="972f0-315">Property</span></span>      | <span data-ttu-id="972f0-316">先頭値</span><span class="sxs-lookup"><span data-stu-id="972f0-316">Value</span></span>                                                                         |
    |---------------|-------------------------------------------------------------------------------|
    | <span data-ttu-id="972f0-317">フィールド</span><span class="sxs-lookup"><span data-stu-id="972f0-317">Field</span></span>         | <span data-ttu-id="972f0-318">**CustomerDriverLicense** これは、**FMRentalEntity** の外部キーフィールドです。</span><span class="sxs-lookup"><span data-stu-id="972f0-318">**CustomerDriverLicense**This is the foreign key field on **FMRentalEntity**.</span></span> |
    | <span data-ttu-id="972f0-319">関連フィールド</span><span class="sxs-lookup"><span data-stu-id="972f0-319">Related Field</span></span> | <span data-ttu-id="972f0-320">**DriverLicense** これは、**FMCustomerEntity** の固有のキーです。</span><span class="sxs-lookup"><span data-stu-id="972f0-320">**DriverLicense**This is the unique key on **FMCustomerEntity**.</span></span>              |

    <span data-ttu-id="972f0-321">次のスクリーンショットは、Visual Studio での関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="972f0-321">The following screen shot shows the relation in Visual Studio.</span></span>

    <span data-ttu-id="972f0-322">[![FMRentalEntity - ソリューション エクスプローラー](./media/fmrentalentity-solution-explorer.png)](./media/fmrentalentity-solution-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-322">[![FMRentalEntity - Solution explorer](./media/fmrentalentity-solution-explorer.png)](./media/fmrentalentity-solution-explorer.png)</span></span>

13. <span data-ttu-id="972f0-323">**ビルド**メニューで、**ソリューションのビルド**をクリックして変更を保存し、プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="972f0-323">On the **BUILD** menu, click **Build Solution** to save your changes and build the project.</span></span> <span data-ttu-id="972f0-324">**出力** ウィンドウでビルドの進行状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="972f0-324">You can view the build progress in the **Output** window.</span></span>
14. <span data-ttu-id="972f0-325">OData エンドポイントをこの変更と併せて更新するには、**iisreset** コマンドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-325">To update the OData endpoint with the changes, you must run an **iisreset** command.</span></span> <span data-ttu-id="972f0-326">管理者として**コマンド プロンプト** ウィンドウを開き、**iisreset** と入力します。</span><span class="sxs-lookup"><span data-stu-id="972f0-326">Open a **Command Prompt** window as an administrator, and enter **iisreset**.</span></span>

<span data-ttu-id="972f0-327">これで、**FMRentalEntity** と **FMCustomerEntity** 間に、ナビゲーション プロパティの作成を完了しました。</span><span class="sxs-lookup"><span data-stu-id="972f0-327">You've now created a navigation property between **FMRentalEntity** and **FMCustomerEntity**.</span></span>

### <a name="use-standard-odata-syntax-to-retrieve-data"></a><span data-ttu-id="972f0-328">標準の OData 構文を使用してデータを取得する</span><span class="sxs-lookup"><span data-stu-id="972f0-328">Use standard OData syntax to retrieve data</span></span>

<span data-ttu-id="972f0-329">このセクションでは、標準の OData 構文の一部を使用し、フリート管理モデルで公開されている OData エンティティを操作して照会します。</span><span class="sxs-lookup"><span data-stu-id="972f0-329">In this section, you will use some of the standard OData syntax to navigate and query the OData entities that are exposed in the Fleet Management model.</span></span> <span data-ttu-id="972f0-330">最初に、以下の手順に従って、JSON 形式のデータを表示する Internet Explorer を有効にします。</span><span class="sxs-lookup"><span data-stu-id="972f0-330">First, follow these steps to enable Internet Explorer to view JSON formatted data.</span></span>

1. <span data-ttu-id="972f0-331">すべての Internet Explorer ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="972f0-331">Close all Internet Explorer windows.</span></span>
2. <span data-ttu-id="972f0-332">C:\\FMLab に移動し、json.ie.reg ファイルを選択してダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-332">Go to C:\\FMLab, and select and double-click the json.ie.reg file.</span></span>
3. <span data-ttu-id="972f0-333">**レジストリ エディター** ダイアログ ボックスで、**はい**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-333">In the **Registry Editor** dialog box, click **Yes**.</span></span>
4. <span data-ttu-id="972f0-334">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-334">Click **OK**.</span></span>

<span data-ttu-id="972f0-335">Internet Explorer  を使用して一部の OData URI を表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="972f0-335">You can now use Internet Explorer to explore some OData URIs.</span></span>

1. <span data-ttu-id="972f0-336">Internet Explorer を起動し、アドレス バーに URL \[baseURL\]/data/$metadata を入力します。OData エンティティに関連付けられたすべてのメタデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-336">Start Internet Explorere, and enter the following URL in the address bar: \[baseURL\]/data/$metadata You will see all the metadata that is associated with OData entities.</span></span>

    > [!NOTE]
    > <span data-ttu-id="972f0-337">最初にアクセスする場合、メタデータの表示に数分かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="972f0-337">The metadata might take a few minutes to appear the first time that you access it.</span></span> <span data-ttu-id="972f0-338">XML で、OData エンティティに関連付けられているすべてのプロパティおよびナビゲーション プロパティを表示できます。</span><span class="sxs-lookup"><span data-stu-id="972f0-338">In the XML, you can see all of the properties and navigation properties associated with the OData entities.</span></span>

2. <span data-ttu-id="972f0-339">ブラウザーで **FleetRental** を検索します。</span><span class="sxs-lookup"><span data-stu-id="972f0-339">In the browser, find **FleetRental**.</span></span> <span data-ttu-id="972f0-340">次のスクリーン ショットは、**FleetRental** エンティティのメタデータと、新しいリレーションシップ **NavigationProperty** を示しています。</span><span class="sxs-lookup"><span data-stu-id="972f0-340">The following screen shot shows the metadata of the **FleetRental** entity, together with the new relationship, **NavigationProperty**.</span></span>

    <span data-ttu-id="972f0-341">[![FleetRental メタデータ](./media/fleetrental-metadata.png)](./media/fleetrental-metadata.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-341">[![FleetRental metadata](./media/fleetrental-metadata.png)](./media/fleetrental-metadata.png)</span></span>

3. <span data-ttu-id="972f0-342">フリート管理アプリケーションのすべての顧客を JSON 形式で表示するには、ブラウザーのアドレス バーに \[baseURL\]/data/FleetCustomer の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="972f0-342">To view all the customers in the Fleet Management application in JSON format, enter the following URL into the address bar of your browser: \[baseURL\]/data/FleetCustomer</span></span>

    > [!NOTE]
    > <span data-ttu-id="972f0-343">エンティティ名は大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-343">Entity names are case-sensitive.</span></span>

4. <span data-ttu-id="972f0-344">顧客のすべてのプロパティを取得しない場合は、選択したプロパティのみを取得できます。</span><span class="sxs-lookup"><span data-stu-id="972f0-344">If you don't want to retrieve all properties for the customers, you can retrieve just selected properties.</span></span> <span data-ttu-id="972f0-345">たとえば、**FirstName** および **LastName** のみを取得するには、次の URL を入力します: \[baseURL\]/data/FleetCustomers?$filter=FirstName.LastName</span><span class="sxs-lookup"><span data-stu-id="972f0-345">For example, to retrieve only **FirstName** and **LastName**, enter the following URL: \[baseURL\]/data/FleetCustomers?$filter=FirstName.LastName</span></span>
5. <span data-ttu-id="972f0-346">また、フィルターを適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="972f0-346">You can also apply filters.</span></span> <span data-ttu-id="972f0-347">たとえば、**FirstName**=**Phil** であるすべての顧客をフィルター処理するには、次の URL を入力します: \[baseUrl\]/data/FleetCustomers?$filter=FirstName%20eq%20'Phil'</span><span class="sxs-lookup"><span data-stu-id="972f0-347">For example, to filter on all customers where **FirstName**=**Phil**, enter the following URL: \[baseUrl\]/data/FleetCustomers?$filter=FirstName%20eq%20'Phil'</span></span>

    > [!NOTE]
    > <span data-ttu-id="972f0-348">これらの URL はコピーおよび貼り付けする場合、機能しません。</span><span class="sxs-lookup"><span data-stu-id="972f0-348">These URLs won't work if you copy and paste them.</span></span> <span data-ttu-id="972f0-349">アドレス バーに手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-349">You must manually enter them in the address bar.</span></span>

6. <span data-ttu-id="972f0-350">顧客のすべての詳細とともにすべての**レンタル**レコードを取得するには、URL "\[baseURL\]/data/FleetRentals?$expand=CustomerRole" を入力します。次の例は、**レンタル**レコードと、リンクされた顧客の詳細を JSON 形式で示しています。</span><span class="sxs-lookup"><span data-stu-id="972f0-350">To retrieve all the **Rental** records, together with all details of the customers, enter the following URL: \[baseURL\]/data/FleetRentals?$expand=CustomerRole The following example shows a **Rental** record, together with details of the linked customer, in JSON format.</span></span>

    ```
    "@odata.context":"https://testax32aos.cloud.test.dynamics.com/en/data/$metadata#FleetRentals","value":
    {  
        { 
            "@odata.etag":"W/"JzEsNTYzNzE0NDU3NjsxLDU2MzcxNDQ1NzY7MTc4NjA2OTg1Niw1NjM3MTQ0NjA1Jw=="",
            "Comments":"","StartMileage":0,"VehicleRatePerDay":40,"CustomerDriverLicense":
            "S468-3184-6541","VehicleRateTotal":280,"VehicleId":"Litware_LitwareFour_1",
            "RentalId":"000001",
            "StartFuelLevel":"Full","StartDate":"2010-04-09T00:00:00Z","CustomerLastName":"Spencer",
            "EndMileage":0,"VehicleVIN":"2J4FY19P0NJ710529",
            "RecId":5637144576,"EndDate":"2010-04-16T00:00:00Z",
            "VehicleRatePerWeek":270,"CustomerFirstName":"Phil","State":3,
            "EndFuelLevel":"","CustomerRole":

            {"@odata.etag":"W/"JzEsNTYzNzE0NDU3NjsxLDU2MzcxNDQ1NzYn"",
            "CellPhone":"(999) 555-0100",
            "DriverLicense":"S468-3184-6541","AddressLine2":"",
            "State":"FL","Country":"US","FirstName":"Phil",
            "Email":"phil.spencer@adatum.com","CustomerGroup":
            "adv_mem_1","AddressLine1":"167 BBN Way","City":"Orlando",
            "ZipCode":77899,"RecId":5637144576,"LastName":"Spencer"
        }  
    }
    ```

### <a name="add-an-action-to-odata-entity"></a><span data-ttu-id="972f0-351">OData エンティティへのアクションの追加</span><span class="sxs-lookup"><span data-stu-id="972f0-351">Add an action to OData entity</span></span>

<span data-ttu-id="972f0-352">アクションは、動作をデータ モデルに挿入する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="972f0-352">Actions provide a way to inject behaviors into the data model.</span></span> <span data-ttu-id="972f0-353">Dynamics 'AX 7' では、データ エンティティにメソッドを追加して特定の属性を持つメソッドを修飾することで、アクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="972f0-353">In Dynamics 'AX 7,' you add actions by adding a method to the data entity and then decorating the method with specific attributes.</span></span> <span data-ttu-id="972f0-354">このセクションでは、アクションを追加するための手順を見てみましょう。</span><span class="sxs-lookup"><span data-stu-id="972f0-354">In this section, we'll walk through the steps for adding an action.</span></span>

1. <span data-ttu-id="972f0-355">ソリューション エクスプローラーで、**FMRentalEntity** を右クリックしてから、**コードの表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-355">In Solution Explorer, right-click **FMRentalEntity**, and then select **View code**.</span></span>
2. <span data-ttu-id="972f0-356">次のコード明細行をコピーし、**コード**ウィンドウに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="972f0-356">Copy the following code lines, and paste them into the **Code** window.</span></span>

    ```
    public class FMRentalEntity extends common
    {
        [SysODataActionAttribute("ReturnRental", true)]
        public str ReturnRental()
        {
            //do something
            return "Rental was successfully returned. Thanks for your business";
        }
    }
    ```

3. <span data-ttu-id="972f0-357">**ビルド**メニューで、**ソリューションの再構築**をクリックして変更を保存し、プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="972f0-357">On the **BUILD** menu, click **Rebuild Solution** to save your changes and build the project.</span></span> <span data-ttu-id="972f0-358">**出力** ウィンドウでビルドの進行状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="972f0-358">You can view the build progress in the **Output** window.</span></span>
4. <span data-ttu-id="972f0-359">OData エンドポイントをこの変更と併せて更新するには、**iisreset** コマンドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-359">To update the OData endpoint with the changes, you must run an **iisreset** command.</span></span> <span data-ttu-id="972f0-360">管理者として**コマンド プロンプト** ウィンドウを開き、**iisreset** と入力します。</span><span class="sxs-lookup"><span data-stu-id="972f0-360">Open a **Command Prompt** window as an administrator, and enter **iisreset**.</span></span>

    <span data-ttu-id="972f0-361">追加したアクションは、次のセクションに示すように、コードで呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="972f0-361">The action that you just added can be invoked through code, as you will see in the next section.</span></span>

### <a name="consume-the-odata-api-from-an-external-console-application"></a><span data-ttu-id="972f0-362">外部コンソール アプリケーションから OData API を消費する</span><span class="sxs-lookup"><span data-stu-id="972f0-362">Consume the OData API from an external console application</span></span>

<span data-ttu-id="972f0-363">このセクションでは、コンソール アプリケーションを使用して、フリート管理アプリケーションで公開されている OData エンドポイントを使用します。</span><span class="sxs-lookup"><span data-stu-id="972f0-363">In this section, you will use a console application to consume the OData endpoints that are exposed in the Fleet Management application.</span></span> <span data-ttu-id="972f0-364">コンソール アプリケーションは、最初に、新規顧客を作成し、その顧客の新しい予約を作成します。</span><span class="sxs-lookup"><span data-stu-id="972f0-364">The console application first creates a new customer and then creates a new reservation for that customer.</span></span> <span data-ttu-id="972f0-365">このチュートリアルでは、標準の .NET Windows Communication Foundation (WCF) データ サービス ライブラリと共に OData を使用して、Dynamics AX と統合することがいかに簡単であるかを示します。</span><span class="sxs-lookup"><span data-stu-id="972f0-365">This tutorial shows how easy it is to use OData together with standard .NET Windows Communication Foundation (WCF) data service libraries to integrate with Dynamics AX.</span></span>

1. <span data-ttu-id="972f0-366">Visual Studio の新しいインスタンスを開始します。</span><span class="sxs-lookup"><span data-stu-id="972f0-366">Start a new instance of Visual Studio.</span></span>
2. <span data-ttu-id="972f0-367">**ファイル**メニューで、**開く** &gt; **プロジェクト/ソリューション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-367">On the **File** menu, click **Open** &gt; **Project/Solution**.</span></span>
3. <span data-ttu-id="972f0-368">**プロジェクトを開く**ダイアログ ボックスで、**C:\\FMLab\\Odata4ConsoleApplication** を参照してから **Odata4ConsoleApplication.csproj** を選択します。</span><span class="sxs-lookup"><span data-stu-id="972f0-368">In the **Open Project** dialog box, browse to **C:\\FMLab\\Odata4ConsoleApplication**, and then select **Odata4ConsoleApplication.csproj**.</span></span>
4. <span data-ttu-id="972f0-369">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-369">Click **Open**.</span></span> <span data-ttu-id="972f0-370">**Odata4ConsoleApplication** プロジェクトがソリューション エクスプローラーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-370">The **Odata4ConsoleApplication** project appears in Solution Explorer.</span></span>
5. <span data-ttu-id="972f0-371">ソリューション エクスプローラーで、**OdataProxyGenerator.tt** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-371">In Solution Explorer, double-click **OdataProxyGenerator.tt**.</span></span>
6. <span data-ttu-id="972f0-372">コード エディターで、次の文字列を組織の URL に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="972f0-372">In the code editor, replace the following string with your organization's URL.</span></span>

    ```
    <baseURL> public const string MetadataDocumentUri = "<baseURL>/data/"
    ```

7. <span data-ttu-id="972f0-373">OdataProxyGenerator.tt ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="972f0-373">Save the OdataProxyGenerator.tt file.</span></span>
8. <span data-ttu-id="972f0-374">**読み取り専用ファイルの保存**ダイアログ ボックスで、**上書き**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-374">In the **Save of Read-only file** dialog box, click **Overwrite**.</span></span> <span data-ttu-id="972f0-375">OData メタデータ エンドポイントのプロキシ クラスが生成されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-375">The proxy class for the OData metadata endpoint is generated.</span></span> <span data-ttu-id="972f0-376">この操作には数分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-376">This operation might take a few minutes.</span></span>
9. <span data-ttu-id="972f0-377">ソリューション エクスプローラーで、**Program.cs** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-377">In Solution Explorer, double-click **Program.cs**.</span></span>
10. <span data-ttu-id="972f0-378">**dynamicsBaseUri** 変数の値を組織の URL に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="972f0-378">Replace the value of the **dynamicsBaseUri** variable with your organization's URL.</span></span>
11. <span data-ttu-id="972f0-379">URL に最後の終了スラッシュ (/) があることを確認してから、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-379">Verify that there is a final closing slash (/) in the URL, and then click **Save**.</span></span>
12. <span data-ttu-id="972f0-380">**読み取り専用ファイルの保存**ダイアログ ボックスで、**上書き**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="972f0-380">In the **Save of Read-only file** dialog box, click **Overwrite**.</span></span>
13. <span data-ttu-id="972f0-381">F5 キーを押してアプリケーションを実行し、出力コンソール ウィンドウで指示に従います。</span><span class="sxs-lookup"><span data-stu-id="972f0-381">Press F5 to run the application, and then follow the instructions in the output console window.</span></span> <span data-ttu-id="972f0-382">アプリケーションによって、Dynamics AX の資格情報を入力するよう求められる場合があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-382">The application might prompt you for your Dynamics AX credentials.</span></span> <span data-ttu-id="972f0-383">アプリケーションが実行された後、新しい顧客と対応する引当が作成されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-383">After the application has run, the new customer and the corresponding reservation are created.</span></span>
14. <span data-ttu-id="972f0-384">**レンタル**ページで新しい予約が表示されることを確認するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="972f0-384">Follow these steps to verify that the new reservation appears on the **Rental** page:</span></span>

    1. <span data-ttu-id="972f0-385">Internet Explorer を起動して、アドレス バーに URL \[baseURL\]/?mi=FMRental を入力します。**FMRental**  ページにレンタルの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="972f0-385">Start Internet Explorer, and enter the following URL in the address bar: \[baseURL\]/?mi=FMRental The **FMRental** page shows the list of rentals.</span></span>

        <span data-ttu-id="972f0-386">[![レンタル リスト](./media/rental-list.png)](./media/rental-list.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-386">[![Rental list](./media/rental-list.png)](./media/rental-list.png)</span></span>

    2. <span data-ttu-id="972f0-387">リストの下部にある**次へ**をクリックして、次のページを表示します。</span><span class="sxs-lookup"><span data-stu-id="972f0-387">At the bottom of the list, click **Next** to view the next page.</span></span> <span data-ttu-id="972f0-388">このページで、追加された新しい顧客の予約が作成されたことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="972f0-388">On this page, you can see that the reservation was created for the new customer that you added.</span></span>

        <span data-ttu-id="972f0-389">[![顧客引当](./media/customer-reservation.png)](./media/customer-reservation.png)</span><span class="sxs-lookup"><span data-stu-id="972f0-389">[![customer reservation](./media/customer-reservation.png)](./media/customer-reservation.png)</span></span>

<span data-ttu-id="972f0-390">これで、OData エンドポイントを使用して フリート管理モデルと対話する外部クライアントを見たウォークスルーは完了です。</span><span class="sxs-lookup"><span data-stu-id="972f0-390">This completes the walkthrough, where you've seen an external client interacting with the Fleet Management model by using OData endpoint.</span></span>

## <a name="casing-rules-in-data-entities"></a><span data-ttu-id="972f0-391">データ エンティティでのケーシング規則</span><span class="sxs-lookup"><span data-stu-id="972f0-391">Casing rules in data entities</span></span>

### <a name="xml-format"></a><span data-ttu-id="972f0-392">XML 形式</span><span class="sxs-lookup"><span data-stu-id="972f0-392">XML format</span></span>
<span data-ttu-id="972f0-393">エクスポート中、エンティティ名とフィールド名は大文字でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="972f0-393">During an export, the entity name and the field names are exported in uppercase.</span></span> <span data-ttu-id="972f0-394">変換を適用する必要がある場合、変換ではすべての参照で大文字を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-394">If there is a need to apply a transformation, the transformation must use uppercase in all references.</span></span>

<span data-ttu-id="972f0-395">インポート中、データ管理は大文字、小文字どちらの入力ファイルも受け入れます。</span><span class="sxs-lookup"><span data-stu-id="972f0-395">During an import, data management accepts input file in any casing.</span></span> <span data-ttu-id="972f0-396">ただし、ファイル内の特定の属性/要素に同じ形式を使用するように注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="972f0-396">However, care must be taken to have the same format for a given attribute/element in the file.</span></span> <span data-ttu-id="972f0-397">変換を適用するときは、変換が着信ファイル内のすべての参照で同じケーシング規則を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="972f0-397">When applying a transformation, ensure that the transformation is using the same casing rules in all references as in the incoming file.</span></span>

### <a name="excel-format"></a><span data-ttu-id="972f0-398">Excel 形式</span><span class="sxs-lookup"><span data-stu-id="972f0-398">Excel format</span></span>
<span data-ttu-id="972f0-399">エクスポート中、列名は大文字でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="972f0-399">During an export, column names will be exported in uppercase.</span></span> <span data-ttu-id="972f0-400">インポートでは大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="972f0-400">Imports are not case sensitive.</span></span>

### <a name="csv-format"></a><span data-ttu-id="972f0-401">CSV 形式</span><span class="sxs-lookup"><span data-stu-id="972f0-401">CSV format</span></span>
<span data-ttu-id="972f0-402">エクスポート中、列名は大文字でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="972f0-402">During an export, column names will be exported in uppercase.</span></span> <span data-ttu-id="972f0-403">インポートでは大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="972f0-403">Imports are not case sensitive.</span></span>

## <a name="tips-and-tricks"></a><span data-ttu-id="972f0-404">ヒントや秘訣</span><span class="sxs-lookup"><span data-stu-id="972f0-404">Tips and tricks</span></span>

### <a name="max-join-limits"></a><span data-ttu-id="972f0-405">最大結合の制限</span><span class="sxs-lookup"><span data-stu-id="972f0-405">Max join limits</span></span>
<span data-ttu-id="972f0-406">エンティティの開発中に、エンティティの全体的な構造が最大統合制限である 26 を超えないように注意してください。</span><span class="sxs-lookup"><span data-stu-id="972f0-406">During entity development, take care to ensure that the overall structure of the entity does not exceed the max join limit of 26.</span></span> <span data-ttu-id="972f0-407">これは、Finance and Operations で既定の限度です。</span><span class="sxs-lookup"><span data-stu-id="972f0-407">This is the default limit in Finance and Operations.</span></span> <span data-ttu-id="972f0-408">統合制限を増やすことは意図しない結果をもたらす可能性があるためお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="972f0-408">Increasing the join limit is not recomended becaues it can have unintended consequences.</span></span> <span data-ttu-id="972f0-409">この制限を超えると、エンティティはレコードの処理に失敗する可能性が高く、次の SQL エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="972f0-409">If this limit is exceeded, the entity will most likely fail to process records and will result in the following SQL error.</span></span> <span data-ttu-id="972f0-410">また、エラーを回避するエンティティで列の合計数を管理することもお勧めします。</span><span class="sxs-lookup"><span data-stu-id="972f0-410">It is also recomended to manage the total number of columns in the entity to avoid this error.</span></span>

```
Cannot create a row of size xxx which is greater than the allowable maximum row size of 8060
```

## <a name="additional-resources"></a><span data-ttu-id="972f0-411">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="972f0-411">Additional resources</span></span>

[<span data-ttu-id="972f0-412">エンティティを開発してデータ移行に使用する</span><span class="sxs-lookup"><span data-stu-id="972f0-412">Developing an entity and using it for data migration</span></span>](develop-entity-for-data-migration.md)
