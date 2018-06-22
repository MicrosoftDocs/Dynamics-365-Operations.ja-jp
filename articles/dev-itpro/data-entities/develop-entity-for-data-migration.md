---
title: "データ移行のエンティティの開発"
description: "このチュートリアルでは、Microsoft Visual Studio でデータ エンティティを開発し、データ移行に使用する方法を示します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 83692
ms.assetid: ebe9c79a-029d-4f03-9bd8-d17e805baa89
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: cd685b7696a3cd3c3fda319943b5d5f1d540f115
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="develop-an-entity-for-data-migration"></a><span data-ttu-id="45a16-103">データ移行のエンティティの開発</span><span class="sxs-lookup"><span data-stu-id="45a16-103">Develop an entity for data migration</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="45a16-104">このチュートリアルでは、Microsoft Visual Studio でデータ エンティティを開発し、データ移行に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="45a16-104">This tutorial shows how to develop data entities in Microsoft Visual Studio and then use them for data migration.</span></span>

<span data-ttu-id="45a16-105">このチュートリアルは、2 つのセクションと 4 つの演習に分かれています。</span><span class="sxs-lookup"><span data-stu-id="45a16-105">This tutorial is broken out into two sections and four exercises.</span></span> <span data-ttu-id="45a16-106">最初のセクションでは、Visual Studio で**プロジェクト カテゴリ**を構築します。</span><span class="sxs-lookup"><span data-stu-id="45a16-106">In the first section, you will build a **Project Category** entity in Visual Studio.</span></span> <span data-ttu-id="45a16-107">次に、このエンティティを使用して、データをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="45a16-107">You will then use this entity to export data.</span></span> <span data-ttu-id="45a16-108">2 番目のセクションで、新しいデータのインポート/エクスポート フレームワークを使用することで、**顧客グループ**および**顧客**エンティティを使用して複数のセットのファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="45a16-108">In the second section, you will use **Customer Groups** and **Customers** entities to import multiple sets of files by using the new Data Import/Export Framework.</span></span> <span data-ttu-id="45a16-109">**注記:** このチュートリアルは、[データ エンティティの構築と消費](build-consuming-data-entities.md) よりもさらに少し難しく設計されています。</span><span class="sxs-lookup"><span data-stu-id="45a16-109">**Note:** This tutorial is designed to be slightly more challenging than [Building and consuming data entities](build-consuming-data-entities.md).</span></span> <span data-ttu-id="45a16-110">ステップ バイ ステップのガイドを提供するのではなく、シナリオ練習を設けて、期待される結果を示します。</span><span class="sxs-lookup"><span data-stu-id="45a16-110">Instead of providing a step-by-step guide, it has scenario exercises and describes the expected outcomes.</span></span> <span data-ttu-id="45a16-111">Microsoft Office Mix ビデオを通じて、データのインポート/エクスポート フレームワークとエンティティについて既に理解していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="45a16-111">The assumption is that you've already familiarized yourself with entities and the Data Import/Export Framework through Microsoft Office Mix videos.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="45a16-112">前提条件</span><span class="sxs-lookup"><span data-stu-id="45a16-112">Prerequisites</span></span>
<span data-ttu-id="45a16-113">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="45a16-113">This tutorial requires that you access the environment by using Remote Desktop.</span></span> <span data-ttu-id="45a16-114">インスタンスに管理者としてプロビジョニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="45a16-114">You must be provisioned as an administrator on the instance.</span></span>

## <a name="base-url"></a><span data-ttu-id="45a16-115">基準 URL</span><span class="sxs-lookup"><span data-stu-id="45a16-115">Base URL</span></span>
<span data-ttu-id="45a16-116">このチュートリアルでは、「ベース URL」はインスタンスのベース URL を指します。</span><span class="sxs-lookup"><span data-stu-id="45a16-116">Throughout this tutorial, "base URL" refers to the base URL of the  instance.</span></span>

-   <span data-ttu-id="45a16-117">クラウド環境では、ベース URL を Microsoft Dynamics Lifecycle Services (LCS) から取得します。</span><span class="sxs-lookup"><span data-stu-id="45a16-117">In the cloud environment, you obtain the base URL from Microsoft Dynamics Lifecycle Services (LCS).</span></span>
-   <span data-ttu-id="45a16-118">ローカル仮想マシン (VM) の、基準 URL は https://usnconeboxax1aos.cloud.onebox.dynamics.com です。</span><span class="sxs-lookup"><span data-stu-id="45a16-118">On a local virtual machine (VM), the base URL is https://usnconeboxax1aos.cloud.onebox.dynamics.com.</span></span>

## <a name="developing-an-entity-in-visual-studio-and-enabling-it-for-data-export"></a><span data-ttu-id="45a16-119">Visual Studio でエンティティを開発し、データをエクスポートできるようにする</span><span class="sxs-lookup"><span data-stu-id="45a16-119">Developing an entity in Visual Studio and enabling it for data export</span></span>
### <a name="business-problem"></a><span data-ttu-id="45a16-120">ビジネスの問題</span><span class="sxs-lookup"><span data-stu-id="45a16-120">Business problem</span></span>

<span data-ttu-id="45a16-121">プロジェクト モジュールの新しいソリューションを開発しています。</span><span class="sxs-lookup"><span data-stu-id="45a16-121">You're developing a new solution for a Project module.</span></span> <span data-ttu-id="45a16-122">実装の一環として、このデータをシステムにインポートするか、システムからエクスポートできるようにプロジェクト カテゴリのデータを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="45a16-122">As part of your implementation, you must represent the data from project categories, so that this data can be imported into the system or exported from it.</span></span> <span data-ttu-id="45a16-123">この目標を達成するには、まずプロジェクト カテゴリのエンティティを作成し、エクスポート機能を使用してデータ抽出をテストします。</span><span class="sxs-lookup"><span data-stu-id="45a16-123">To accomplish this goal, you will first build an entity for the project category and then use the export functionality to test data extraction.</span></span>

### <a name="exercise-1-build-a-project-category-entity"></a><span data-ttu-id="45a16-124">手順 1: プロジェクト カテゴリのエンティティを構築</span><span class="sxs-lookup"><span data-stu-id="45a16-124">Exercise 1: Build a Project Category entity</span></span>

<span data-ttu-id="45a16-125">この練習では、**プロジェクト カテゴリ**というエンティティを構築し、ProjCategory テーブルをプライマリ データ ソースとして使用します。</span><span class="sxs-lookup"><span data-stu-id="45a16-125">In this exercise, you will build an entity, **Project Category**, that uses the ProjCategory table as its primary data source.</span></span> <span data-ttu-id="45a16-126">このエンティティには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="45a16-126">This entity has the following properties.</span></span>


| <span data-ttu-id="45a16-127">プロパティ</span><span class="sxs-lookup"><span data-stu-id="45a16-127">Property</span></span>               | <span data-ttu-id="45a16-128">先頭値</span><span class="sxs-lookup"><span data-stu-id="45a16-128">Value</span></span>                 |
|------------------------|-----------------------|
| <span data-ttu-id="45a16-129">エンティティ AOT の名前</span><span class="sxs-lookup"><span data-stu-id="45a16-129">Entity AOT name</span></span>        | <span data-ttu-id="45a16-130">ProjectCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="45a16-130">ProjectCategoryEntity</span></span> |
| <span data-ttu-id="45a16-131">ラベル</span><span class="sxs-lookup"><span data-stu-id="45a16-131">Label</span></span>                  | <span data-ttu-id="45a16-132">プロジェクト カテゴリ</span><span class="sxs-lookup"><span data-stu-id="45a16-132">Project Categories</span></span>    |
| <span data-ttu-id="45a16-133">エンティティ カテゴリ</span><span class="sxs-lookup"><span data-stu-id="45a16-133">Entity category</span></span>        | <span data-ttu-id="45a16-134">参照</span><span class="sxs-lookup"><span data-stu-id="45a16-134">Reference</span></span>             |
| <span data-ttu-id="45a16-135">パブリック名</span><span class="sxs-lookup"><span data-stu-id="45a16-135">Public name</span></span>            | <span data-ttu-id="45a16-136">ProjectCategory</span><span class="sxs-lookup"><span data-stu-id="45a16-136">ProjectCategory</span></span>       |
| <span data-ttu-id="45a16-137">グループ名</span><span class="sxs-lookup"><span data-stu-id="45a16-137">Collection name</span></span>        | <span data-ttu-id="45a16-138">ProjectCategories</span><span class="sxs-lookup"><span data-stu-id="45a16-138">ProjectCategories</span></span>     |
| <span data-ttu-id="45a16-139">パブリック API の有効化</span><span class="sxs-lookup"><span data-stu-id="45a16-139">Enable public API</span></span>      | <span data-ttu-id="45a16-140">有</span><span class="sxs-lookup"><span data-stu-id="45a16-140">Yes</span></span>                   |
| <span data-ttu-id="45a16-141">データ管理の有効化</span><span class="sxs-lookup"><span data-stu-id="45a16-141">Enable data management</span></span> | <span data-ttu-id="45a16-142">有</span><span class="sxs-lookup"><span data-stu-id="45a16-142">Yes</span></span>                   |

<span data-ttu-id="45a16-143">エンティティには、次のフィールドもあります。</span><span class="sxs-lookup"><span data-stu-id="45a16-143">The entity also has the following fields.</span></span>


| <span data-ttu-id="45a16-144">フィールド</span><span class="sxs-lookup"><span data-stu-id="45a16-144">Fields</span></span>                   |
|--------------------------|
| <span data-ttu-id="45a16-145">ActiveInJournals</span><span class="sxs-lookup"><span data-stu-id="45a16-145">ActiveInJournals</span></span>         |
| <span data-ttu-id="45a16-146">CategoryGroup</span><span class="sxs-lookup"><span data-stu-id="45a16-146">CategoryGroup</span></span>            |
| <span data-ttu-id="45a16-147">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="45a16-147">Category</span></span>                 |
| <span data-ttu-id="45a16-148">TransactionType</span><span class="sxs-lookup"><span data-stu-id="45a16-148">TransactionType</span></span>          |
| <span data-ttu-id="45a16-149">CategoryName</span><span class="sxs-lookup"><span data-stu-id="45a16-149">CategoryName</span></span>             |
| <span data-ttu-id="45a16-150">ワーカー</span><span class="sxs-lookup"><span data-stu-id="45a16-150">Worker</span></span>                   |
| <span data-ttu-id="45a16-151">CustomerPaymentRetention</span><span class="sxs-lookup"><span data-stu-id="45a16-151">CustomerPaymentRetention</span></span> |
| <span data-ttu-id="45a16-152">IndirectCostComponent</span><span class="sxs-lookup"><span data-stu-id="45a16-152">IndirectCostComponent</span></span>    |
| <span data-ttu-id="45a16-153">ItemSalesTaxGroup</span><span class="sxs-lookup"><span data-stu-id="45a16-153">ItemSalesTaxGroup</span></span>        |
| <span data-ttu-id="45a16-154">ServiceCode</span><span class="sxs-lookup"><span data-stu-id="45a16-154">ServiceCode</span></span>              |
| <span data-ttu-id="45a16-155">休暇</span><span class="sxs-lookup"><span data-stu-id="45a16-155">Absence</span></span>                  |

#### <a name="steps"></a><span data-ttu-id="45a16-156">ステップ</span><span class="sxs-lookup"><span data-stu-id="45a16-156">Steps</span></span>

1.  <span data-ttu-id="45a16-157">Visual Studio で、新しい Microsoft Dynamics 365 for Finance and Operations プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="45a16-157">In Visual Studio, create a new Microsoft Dynamics 365 for Finance and Operations project.</span></span>
2.  <span data-ttu-id="45a16-158">ソリューション エクスプローラーで、プロジェクトを選択してから**プロパティ**を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-158">In Solution Explorer, select the project, and then right-click **Properties**.</span></span>
3.  <span data-ttu-id="45a16-159">次のプロジェクト プロパティを指定し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-159">Specify the following project properties, and then click **OK**.</span></span>

    | <span data-ttu-id="45a16-160">プロパティ</span><span class="sxs-lookup"><span data-stu-id="45a16-160">Property</span></span>                      | <span data-ttu-id="45a16-161">先頭値</span><span class="sxs-lookup"><span data-stu-id="45a16-161">Value</span></span>             |
    |-------------------------------|-------------------|
    | <span data-ttu-id="45a16-162">モデル</span><span class="sxs-lookup"><span data-stu-id="45a16-162">Model</span></span>                         | <span data-ttu-id="45a16-163">Application Suite</span><span class="sxs-lookup"><span data-stu-id="45a16-163">Application Suite</span></span> |
    | <span data-ttu-id="45a16-164">法人</span><span class="sxs-lookup"><span data-stu-id="45a16-164">Company</span></span>                       | <span data-ttu-id="45a16-165">USSI</span><span class="sxs-lookup"><span data-stu-id="45a16-165">USSI</span></span>              |
    | <span data-ttu-id="45a16-166">ビルド上にデータベースを同期</span><span class="sxs-lookup"><span data-stu-id="45a16-166">Synchronize Database on build</span></span> | <span data-ttu-id="45a16-167">はい</span><span class="sxs-lookup"><span data-stu-id="45a16-167">True</span></span>              |

4.  <span data-ttu-id="45a16-168">プロジェクトから、**追加** &gt; **新しい品目**を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-168">From the project, right-click **Add** &gt; **New item**.</span></span>
5.  <span data-ttu-id="45a16-169">**データ モデル** &gt; **データ エンティティ** を新しい項目として選択します。</span><span class="sxs-lookup"><span data-stu-id="45a16-169">Select **Data Model** &gt; **Data Entity** as your new item.</span></span>
6.  <span data-ttu-id="45a16-170">名前を入力し、次に**追加**をクリックすると**データ** **エンティティ**ウィザードが開始されます。</span><span class="sxs-lookup"><span data-stu-id="45a16-170">Enter a name, and then click **Add** to start the **Data** **Entity** wizard.</span></span>
7.  <span data-ttu-id="45a16-171">ウィザードの最初のページで、この練習の前の表を使用して、エンティティのプロパティのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="45a16-171">On the first page of the wizard, specify the set of properties for the entity by using the table earlier in this exercise.</span></span> <span data-ttu-id="45a16-172">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-172">Then click **Next**.</span></span> 

<span data-ttu-id="45a16-173">[![プロパティ ページの指定](./media/specifyproperties_devoentity.png)](./media/specifyproperties_devoentity.png)</span><span class="sxs-lookup"><span data-stu-id="45a16-173">[![Specify properties page](./media/specifyproperties_devoentity.png)](./media/specifyproperties_devoentity.png)</span></span>

8.  <span data-ttu-id="45a16-174">次のページで、プライマリ データ ソースからフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="45a16-174">On the next page, add fields from the primary data source.</span></span> <span data-ttu-id="45a16-175">フィールド名ごとに、パブリック契約が反映されていることを確認します (この練習では前の表を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="45a16-175">Make sure that each field name reflects the public contract (see the table earlier in this exercise).</span></span> <span data-ttu-id="45a16-176">フィールドのラベルをフィールド名として使用するには、**ラベルをフィールド名に変換** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="45a16-176">To use the field's label as the field name, select the **Convert label to field names** option.</span></span> <span data-ttu-id="45a16-177">エンティティに必須ではないフィールドのオプションをクリアします。</span><span class="sxs-lookup"><span data-stu-id="45a16-177">Clear the option for any fields that are not required for the entity.</span></span>
9.  <span data-ttu-id="45a16-178">ウィザードを完了し、エンティティとそのコンポーネントをプロジェクトに追加するには、**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-178">Click **Finish** to complete the wizard, and to add the entity and its artifacts to the project.</span></span>
10. <span data-ttu-id="45a16-179">エンティティの使用を開始できるように、プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="45a16-179">Build your project, so that you can start to use the entity.</span></span>

#### <a name="expected-outcome"></a><span data-ttu-id="45a16-180">予想される結果</span><span class="sxs-lookup"><span data-stu-id="45a16-180">Expected outcome</span></span>

-   <span data-ttu-id="45a16-181">Visual Studio で、**データ エンティティ** ウィザードを完了すると、次のアーティファクトがプロジェクトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a16-181">In Visual Studio, the following artifacts will appear in the project after you've completed the **Data Entity** wizard.</span></span> 
<span data-ttu-id="45a16-182">[![新規プロジェクト コンポーネント](./media/testappsuite_devoentity.png)](./media/testappsuite_devoentity.png)</span><span class="sxs-lookup"><span data-stu-id="45a16-182">[![New project artifacts](./media/testappsuite_devoentity.png)](./media/testappsuite_devoentity.png)</span></span>

-   <span data-ttu-id="45a16-183">データ エンティティを右クリックし、**テーブル ブラウザーを開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="45a16-183">Right-click the data entity, and then select **Open table browser**.</span></span> <span data-ttu-id="45a16-184">**注記:** 会社が **USSI** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="45a16-184">**Note:** Make sure that your company is set to **USSI**.</span></span>

### <a name="exercise-2-export-a-limited-set-of-data-by-using-a-sample-file-mapping-and-filters"></a><span data-ttu-id="45a16-185">手順 2: サンプル ファイル マッピングおよびフィルターを使用して限られたデータ セットをエクスポート</span><span class="sxs-lookup"><span data-stu-id="45a16-185">Exercise 2: Export a limited set of data by using a sample file mapping and filters</span></span>

<span data-ttu-id="45a16-186">この練習では、データをエクスポートするために構築した**プロジェクト カテゴリ** エンティティを使用します。</span><span class="sxs-lookup"><span data-stu-id="45a16-186">In this exercise, you will use the **Project Category** entity that you just built to export data.</span></span> <span data-ttu-id="45a16-187">データのサブセットのみをエクスポートするには、サンプル ファイルのマッピングとフィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="45a16-187">To export only a subset of the data, you will use a sample file mapping and filters.</span></span> <span data-ttu-id="45a16-188">エクスポートされたデータは XML 形式です。</span><span class="sxs-lookup"><span data-stu-id="45a16-188">The exported data will be in XML format.</span></span>

#### <a name="steps"></a><span data-ttu-id="45a16-189">ステップ</span><span class="sxs-lookup"><span data-stu-id="45a16-189">Steps</span></span>

1.  <span data-ttu-id="45a16-190">**プロジェクト カテゴリ** エンティティを作成した後、クライアントを開始します。</span><span class="sxs-lookup"><span data-stu-id="45a16-190">After you've finished building the **Project Category** entity, start the client.</span></span>
2.  <span data-ttu-id="45a16-191">会社を **USSI** に変更します。</span><span class="sxs-lookup"><span data-stu-id="45a16-191">Change the company to **USSI**.</span></span>
3.  <span data-ttu-id="45a16-192">**データ管理**ワークスペースで、**エクスポート**をクリックしてデータの抽出を開始します。</span><span class="sxs-lookup"><span data-stu-id="45a16-192">In the **Data management** workspace, click **Export** to begin data extraction.</span></span>
4.  <span data-ttu-id="45a16-193">エンティティ名およびターゲット データ形式などのエクスポートの詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="45a16-193">Enter the export details, such as entity name and target data format.</span></span>

<span data-ttu-id="45a16-194">[![エクスポートの詳細の入力](./media/exportprojectcategory_devoentity.png)](./media/exportprojectcategory_devoentity.png)</span><span class="sxs-lookup"><span data-stu-id="45a16-194">[![Entering export details](./media/exportprojectcategory_devoentity.png)](./media/exportprojectcategory_devoentity.png)</span></span> 

<span data-ttu-id="45a16-195">XML のサンプル ファイル形式として、[ProjectCategoryExport\_Sample](https://go.microsoft.com/fwlink/?linkid=845209) ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="45a16-195">Use the following file as the sample file format for XML: [ProjectCategoryExport\_Sample](https://go.microsoft.com/fwlink/?linkid=845209).</span></span> 

<span data-ttu-id="45a16-196">テキスト エディタでこのファイルを開き、XML ファイルとして保存します。</span><span class="sxs-lookup"><span data-stu-id="45a16-196">Open this file in a text editor, and save it as an XML file.</span></span> <span data-ttu-id="45a16-197">サンプル ファイル マッピングが無効の場合、エンティティに不適切なフィールド名があります。</span><span class="sxs-lookup"><span data-stu-id="45a16-197">If the sample file mapping isn't valid, there is an incorrect field name in the entity.</span></span> <span data-ttu-id="45a16-198">続行するため、エンティティまたはサンプル ファイルのいずれかを修正します。</span><span class="sxs-lookup"><span data-stu-id="45a16-198">Fix either the entity or the sample file to continue.</span></span>

5.  <span data-ttu-id="45a16-199">**フィルター**をクリックし、フィルター条件として**プロジェクト**を指定すると、限定されたデータのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="45a16-199">Click **Filter**, and then specify **Project** as the filter criterion, so that only limited data is exported.</span></span> 
<span data-ttu-id="45a16-200">[![プロジェクトによるフィルター処理](./media/inquiry_devoentity.png)](./media/inquiry_devoentity.png)</span><span class="sxs-lookup"><span data-stu-id="45a16-200">[![Filtering by project](./media/inquiry_devoentity.png)](./media/inquiry_devoentity.png)</span></span>

6.  <span data-ttu-id="45a16-201">**エクスポート** ダイアログ ボックスで、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-201">In the **Export** dialog box, click **OK**.</span></span>

#### <a name="expected-outcome"></a><span data-ttu-id="45a16-202">予想される結果</span><span class="sxs-lookup"><span data-stu-id="45a16-202">Expected outcome</span></span>

-   <span data-ttu-id="45a16-203">15 のレコードは正常にエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="45a16-203">Fifteen records are successfully exported.</span></span>
-   <span data-ttu-id="45a16-204">出力は次のファイルに似ています。[ProjectCategoryExport\_Output](https://go.microsoft.com/fwlink/?linkid=845210)。</span><span class="sxs-lookup"><span data-stu-id="45a16-204">The output is similar to the following file: [ProjectCategoryExport\_Output](https://go.microsoft.com/fwlink/?linkid=845210).</span></span> <span data-ttu-id="45a16-205">(この結果を確認するにはテキスト エディタでファイルを開きます。)</span><span class="sxs-lookup"><span data-stu-id="45a16-205">(Open the file in a text editor to verify this outcome.)</span></span>

## <a name="migrating-data-in-multiple-files-by-using-the-data-importexport-framework"></a><span data-ttu-id="45a16-206">データのインポート/エクスポート フレームワークを使用した複数のファイルのデータの移行</span><span class="sxs-lookup"><span data-stu-id="45a16-206">Migrating data in multiple files by using the Data Import/Export Framework</span></span>
### <a name="business-problem"></a><span data-ttu-id="45a16-207">ビジネスの問題</span><span class="sxs-lookup"><span data-stu-id="45a16-207">Business problem</span></span>

<span data-ttu-id="45a16-208">新しい環境を実装しています。</span><span class="sxs-lookup"><span data-stu-id="45a16-208">You're implementing a new environment.</span></span> <span data-ttu-id="45a16-209">この実装の一環として、レガシ顧客データを移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45a16-209">As part of this implementation, you want to migrate some legacy customer data.</span></span> <span data-ttu-id="45a16-210">データは 2 つのファイル セットに含まれ、各ファイルには**顧客**および**顧客顧客グループ**のエンティティのデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="45a16-210">The data is contained in two sets of files, each of which has data for the **Customers** and **Customer Groups** entities.</span></span> <span data-ttu-id="45a16-211">データ ファイルの一部の列がエンティティに直接マップされないため、この移行はやや複雑です。</span><span class="sxs-lookup"><span data-stu-id="45a16-211">This migration is slightly complex, because some columns in the data files don't map directly to the entities.</span></span> <span data-ttu-id="45a16-212">また、ファイルには、インポート処理中に修正する必要がある検証エラーがあります。</span><span class="sxs-lookup"><span data-stu-id="45a16-212">Additionally, the files have validation errors that must be corrected during the import process.</span></span>

### <a name="exercise-3-create-a-data-project-and-import-multiple-files"></a><span data-ttu-id="45a16-213">手順 3: データ プロジェクトを作成し、複数のファイルをインポート</span><span class="sxs-lookup"><span data-stu-id="45a16-213">Exercise 3: Create a data project and import multiple files</span></span>

<span data-ttu-id="45a16-214">この練習では、新しいデータのインポート/エクスポート フレームワークを使用して、2 つのファイルを **USRT** という会社にインポートします。</span><span class="sxs-lookup"><span data-stu-id="45a16-214">In this exercise, you will import two files into the **USRT** company by using the new Data Import/Export Framework.</span></span> <span data-ttu-id="45a16-215">これらのファイルは、単一のデータ プロジェクトを使用して順番にインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="45a16-215">These files need to be imported in sequence by using a single data project.</span></span> <span data-ttu-id="45a16-216">**顧客** エンティティには、**顧客グループ** エンティティへの参照があります。</span><span class="sxs-lookup"><span data-stu-id="45a16-216">The **Customers** entity has a reference to the **Customer Groups** entity.</span></span> <span data-ttu-id="45a16-217">Customers1 ファイルが**顧客**エンティティに正しくマップされないため、ファイルをアップロードするときにエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a16-217">Because the Customers1 file doesn't map correctly to the **Customers** entity, you will receive an error when you upload the file.</span></span> <span data-ttu-id="45a16-218">したがって、インポート プロセスを完了するには、**Customers** エンティティに正しい列マッピングを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45a16-218">Therefore, to complete the import process, you will have to provide the correct column mappings for the **Customers** entity.</span></span>

#### <a name="steps"></a><span data-ttu-id="45a16-219">ステップ</span><span class="sxs-lookup"><span data-stu-id="45a16-219">Steps</span></span>

1.  <span data-ttu-id="45a16-220">Microsoft Excel で以下のファイルを開いて、ローカル ディレクトリ内の CSV ファイルとして保存する:</span><span class="sxs-lookup"><span data-stu-id="45a16-220">Open the following files in Microsoft Excel, and save them as CSV files in your local directory:</span></span>
    -   [<span data-ttu-id="45a16-221">Customers1</span><span class="sxs-lookup"><span data-stu-id="45a16-221">Customers1</span></span>](https://go.microsoft.com/fwlink/?linkid=845211)
    -   [<span data-ttu-id="45a16-222">CustomerGroups1</span><span class="sxs-lookup"><span data-stu-id="45a16-222">CustomerGroups1</span></span>](https://go.microsoft.com/fwlink/?linkid=845212)

2.  <span data-ttu-id="45a16-223">クライアントで、会社を **USRT** に変更します。</span><span class="sxs-lookup"><span data-stu-id="45a16-223">In the client, change the company to **USRT**.</span></span>
3.  <span data-ttu-id="45a16-224">**ユーザー**ダッシュ ボードから、**データ管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="45a16-224">From the **User** dashboard, open the **Data Management** workspace.</span></span>
4.  <span data-ttu-id="45a16-225">新しいデータ プロジェクトを設定するには、**インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-225">Click **Import** to configure a new data project.</span></span>
5.  <span data-ttu-id="45a16-226">名前およびファイルの形式などのプロジェクト詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="45a16-226">Enter the project details, such as the name and file format.</span></span>
6.  <span data-ttu-id="45a16-227">各ファイルについては、エンティティを選択し、次にデータ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="45a16-227">For each file, select an entity, and then upload the data file.</span></span>
7.  <span data-ttu-id="45a16-228">Customer1.csv ファイルが**顧客**エンティティに正しくマップされないため、ファイルをアップロードするときにエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a16-228">Because the Customer1.csv file doesn't map correctly to the **Customers** entity, you will receive an error when you upload the file.</span></span> <span data-ttu-id="45a16-229">ファイルがアップロードされた後、**マッピングの表示**をクリックし、**顧客**エンティティ列のマッピングを修正します。</span><span class="sxs-lookup"><span data-stu-id="45a16-229">After the file is uploaded, click **View mappings** to fix the column mappings for the **Customers** entity.</span></span> <span data-ttu-id="45a16-230">**ヒント:** **CustomerAccount** はインポート中にエンティティで必要です。</span><span class="sxs-lookup"><span data-stu-id="45a16-230">**Hint:** **CustomerAccount** is required in the entity during import.</span></span> <span data-ttu-id="45a16-231">ソース ファイルで **AccountNum** からマップされます。</span><span class="sxs-lookup"><span data-stu-id="45a16-231">It is mapped from **AccountNum** in the source file.</span></span> <span data-ttu-id="45a16-232">住所フィールドは、インポートのオプションです。</span><span class="sxs-lookup"><span data-stu-id="45a16-232">Address fields are optional for the import.</span></span>
8.  <span data-ttu-id="45a16-233">完了したら、ブラウザの **戻る** ボタンをクリックして、データ プロジェクトに戻ります。</span><span class="sxs-lookup"><span data-stu-id="45a16-233">When you've finished, click the **Back** button in your browser to return to the data project.</span></span>
9.  <span data-ttu-id="45a16-234">**データ プロジェクト**ページで、**今すぐインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-234">On the **Data Project** page, click **Import now**.</span></span>

#### <a name="expected-outcome"></a><span data-ttu-id="45a16-235">予想される結果</span><span class="sxs-lookup"><span data-stu-id="45a16-235">Expected outcome</span></span>

<span data-ttu-id="45a16-236">4 つの更新および 23 の挿入が正常にインポートされ、**実行の要約**ページが結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="45a16-236">Four updates and 23 inserts are successfully imported and the **Execution summary** page shows the results.</span></span>

### <a name="exercise-4-re-import-by-using-an-existing-data-project-and-manage-data-in-staging"></a><span data-ttu-id="45a16-237">手順 4: 既存のデータ プロジェクトを使い再インポートし、ステージングでデータを管理</span><span class="sxs-lookup"><span data-stu-id="45a16-237">Exercise 4: Re-import by using an existing data project and manage data in staging</span></span>

<span data-ttu-id="45a16-238">この練習では、新しいファイルのセットを使用して、既存のデータ プロジェクトからデータをインポートします。</span><span class="sxs-lookup"><span data-stu-id="45a16-238">In this exercise, you will use a new set of files to import data through the existing data project.</span></span> <span data-ttu-id="45a16-239">Customers2 は**顧客**エンティティの新規および更新されたデータを含みます。</span><span class="sxs-lookup"><span data-stu-id="45a16-239">Customers2 contains new and updated data for the **Customers** entity.</span></span> <span data-ttu-id="45a16-240">CustomerGroups2 は**顧客グループ** エンティティの更新されたデータを含みます。</span><span class="sxs-lookup"><span data-stu-id="45a16-240">CustomerGroups2 contains updated data for the **Customer Groups** entity.</span></span> <span data-ttu-id="45a16-241">Customers2 には、いくつかのエラー レコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="45a16-241">Customers2 contains some error records.</span></span> <span data-ttu-id="45a16-242">ステージングでのこれらのエラーを修正し、データを検証し、それをターゲットに送って、インポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="45a16-242">You will fix these errors in staging, validate the data, and then push it to the target to complete the import.</span></span>

#### <a name="steps"></a><span data-ttu-id="45a16-243">ステップ</span><span class="sxs-lookup"><span data-stu-id="45a16-243">Steps</span></span>

1.  <span data-ttu-id="45a16-244">**データ管理**ワークスペースで、既存のデータ プロジェクトを選択し、**再インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-244">In the **Data management** workspace, select the existing data project, and the click **Re-import**.</span></span> <span data-ttu-id="45a16-245">再インポート機能を使用することにより、データ プロジェクトの以前の設定を保持し、インポートに新しいファイルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="45a16-245">By using the re-import functionality, you can preserve your previous settings for the data project and use new files for the import.</span></span> <span data-ttu-id="45a16-246">ただし、**データ プロジェクトの再読み込み**をクリックし、代わりに新しいファイルをアップロードする場合、以前のマッピングが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="45a16-246">However, if you click **Reload data project** and upload new files instead, the previous mappings will be overridden.</span></span>
2.  <span data-ttu-id="45a16-247">Excel で以下のファイルを開いて、ローカル ディレクトリ内の CSV ファイルとして保存する:</span><span class="sxs-lookup"><span data-stu-id="45a16-247">Open the following files in Excel, and save them as CSV files in your local directory:</span></span>
    -   [<span data-ttu-id="45a16-248">Customers2</span><span class="sxs-lookup"><span data-stu-id="45a16-248">Customers2</span></span>](https://go.microsoft.com/fwlink/?linkid=845213)
    -   [<span data-ttu-id="45a16-249">CustomerGroups2</span><span class="sxs-lookup"><span data-stu-id="45a16-249">CustomerGroups2</span></span>](https://go.microsoft.com/fwlink/?linkid=845214)

3.  <span data-ttu-id="45a16-250">各エンティティの新しいファイルをアップロードし、**今すぐインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-250">Upload the new files for each entity, and then click **Import now**.</span></span>
4.  <span data-ttu-id="45a16-251">**ステータス**ページで、**実行ログの表示**をクリックしてエラーを調査します。</span><span class="sxs-lookup"><span data-stu-id="45a16-251">On the **Status** page, click **View execution log** to investigate the errors.</span></span>
5.  <span data-ttu-id="45a16-252">**ステータス**ページで、**ステージングの表示**をクリックして、ステージング テーブルのデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="45a16-252">On the **Status** page, click **View staging** to view the data in a staging table.</span></span> <span data-ttu-id="45a16-253">このビューには、エラーのあるレコードも表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a16-253">This view will also show records that have errors.</span></span>
6.  <span data-ttu-id="45a16-254">エラーが発生したレコードを修正するには、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-254">Click **Edit** to fix records that have errors.</span></span> <span data-ttu-id="45a16-255">(DM10221 および DM1022 レコードの**顧客グループ**値は無効です。)</span><span class="sxs-lookup"><span data-stu-id="45a16-255">(The **Customer Group** value for records DM10221 and DM1022 isn't valid.)</span></span>
7.  <span data-ttu-id="45a16-256">修正したレコードを選択し、**検証** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-256">Select the records that you fixed, and then click **Validate**.</span></span> <span data-ttu-id="45a16-257">ページを更新し、レコードのステータスが **検証済み** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="45a16-257">Refresh the page to verify that the status of the records is **Validated**.</span></span>
8.  <span data-ttu-id="45a16-258">**データをターゲットにコピー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-258">Click **Copy data to target**.</span></span>
9.  <span data-ttu-id="45a16-259">**実行するジョブ ID の選択**ダイアログ ボックスの**実行**フィールドで**基準**を選択して、**ユーザーによって選択された行**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="45a16-259">In the **Select a job ID to run** dialog box, in the **Run for** field, select **Criteria**, and set **Row selected by user** to **Yes**.</span></span> <span data-ttu-id="45a16-260">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-260">Then click **OK**.</span></span> 

<span data-ttu-id="45a16-261">[![実行するジョブの選択](./media/selectjob_devoentity.png)](./media/selectjob_devoentity.png)</span><span class="sxs-lookup"><span data-stu-id="45a16-261">[![Selecting a job to run](./media/selectjob_devoentity.png)](./media/selectjob_devoentity.png)</span></span>

10. <span data-ttu-id="45a16-262">**ターゲット データ実行**ページで、**実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a16-262">On the **Target data execution** page, click **Run**.</span></span>
11. <span data-ttu-id="45a16-263">実行が完了したら、ページを更新して、最新のステージングの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="45a16-263">When the run is completed, refresh the page to see the latest staging status.</span></span>

#### <a name="expected-outcome"></a><span data-ttu-id="45a16-264">予想される結果</span><span class="sxs-lookup"><span data-stu-id="45a16-264">Expected outcome</span></span>

-   <span data-ttu-id="45a16-265">最初の試行で、**顧客グループ**エンティティのインポートが成功し、**顧客**エンティティでは部分的に成功します。</span><span class="sxs-lookup"><span data-stu-id="45a16-265">On the first try, the import succeeds for the **Customer Groups** entity and partially succeeds for the **Customers** entity.</span></span>
-   <span data-ttu-id="45a16-266">**実行の概要** ページには、5 つのレコードが作成され、3 つのレコードが更新され、2 つのレコードにエラーがあることが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a16-266">The **Execution summary** page shows that five records were created, three records were updated, and two records have errors.</span></span>
-   <span data-ttu-id="45a16-267">ステージング ビューでは、2 つのレコードにエラーがあります。</span><span class="sxs-lookup"><span data-stu-id="45a16-267">In the staging view, two records have errors.</span></span>
-   <span data-ttu-id="45a16-268">レコードを修正し再度インポートを実行すると、ステージング ビューにすべてのレコードが完了したことが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45a16-268">After you fix the records and run the import again, the staging view shows that all records are completed.</span></span>





