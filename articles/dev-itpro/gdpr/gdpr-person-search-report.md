---
title: 個人検索レポート
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のパーソナル データ レポートに関する情報を提供します。
author: rschloma
manager: AnnBe
ms.date: 01/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a56dd8c5c4100b5294cb99c6778fc7bf572fe5a
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595408"
---
# <a name="person-search-report"></a><span data-ttu-id="ee161-103">個人検索レポート</span><span class="sxs-lookup"><span data-stu-id="ee161-103">Person search report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee161-104">担当者検索レポートは、既存の Microsoft Dynamics 365 for Finance and Operations データ管理フレームワークの機能を強化したものです。</span><span class="sxs-lookup"><span data-stu-id="ee161-104">The Person search report is a refinement of the existing Data management framework of Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ee161-105">データ管理フレームワークには、担当者と、担当者が Finance and Operations で割り当てられる可能性があるロールを定義するために使用される個人データを識別するために Microsoft が作成した、事前パッケージ化されたエンティティ セットが用意されています。</span><span class="sxs-lookup"><span data-stu-id="ee161-105">The Data management framework offers a pre-packaged set of entities that Microsoft authored to identify personal data that is used to define a person and the roles that a person might be assigned to in Finance and Operations.</span></span> 

> [!NOTE]
> <span data-ttu-id="ee161-106">Dynamics 365 for Finance and Operations、Dynamics 365 for Retail、および Dynamics 365 for Talent のレポートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee161-106">You can use the report with Dynamics 365 for Finance and Operations, Dynamics 365 for Retail, and Dynamics 365 for Talent.</span></span> <span data-ttu-id="ee161-107">このトピックの Finance and Operations への参照は、Retail と Talent にも当てはまります。</span><span class="sxs-lookup"><span data-stu-id="ee161-107">References to Finance and Operations in this topic also apply to Retail and Talent.</span></span> <span data-ttu-id="ee161-108">Microsoft Dynamics AX 2012 では今のところレポートは使用できません。</span><span class="sxs-lookup"><span data-stu-id="ee161-108">The report is not currently available for Microsoft Dynamics AX 2012.</span></span><span data-ttu-id="ee161-109"> 個人検索レポートは、Finance and Operations バージョン 8.0 で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="ee161-109"> The Person search report is available in Finance and Operations version 8.0.</span></span> <span data-ttu-id="ee161-110">レポートはバージョン 7.3 (毎月の更新プログラム 7.3.2 経由で配信)、バージョン 7.2 (KB 4132615 経由)、およびバージョン7.1 (KB 4132441 経由 ) でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee161-110">The report is also available in version 7.3 (delivered via monthly update 7.3.2), in version 7.2 (via KB 4132615), and in version 7.1 (via KB 4132441).</span></span> <span data-ttu-id="ee161-111">個人検索レポートが定期的に更新される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-111">The Person search report may be updated periodically.</span></span> <span data-ttu-id="ee161-112">このレポートを使用する前に、すべての関連する修正プログラムを取得し、適用したことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-112">Before using this report, you need to ensure that you have obtained and applied all relevant hotfixes.</span></span> 

<span data-ttu-id="ee161-113">Finance and Operations のグローバル アドレス帳を使用すると、データ モデルで関係者として説明されている人物のインスタンスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ee161-113">You can use the Global address book in Finance and Operations to create an instance of a person that is described in the data model as a party.</span></span> 

<span data-ttu-id="ee161-114">Finance and Operations データに、連絡先、顧客、ユーザー、作業者、またはその他の担当者を追加するとき、通常、その担当者のアドレス帳エントリの作成から開始します。</span><span class="sxs-lookup"><span data-stu-id="ee161-114">When you add a contact, customer, user, worker, or other person in Finance and Operations data, you typically start by creating an address book entry for that person.</span></span> <span data-ttu-id="ee161-115">アドレス帳の各ユーザーは関係者と呼ばれ、PartyID が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="ee161-115">Each person in the address book is referred to as a party and is assigned a PartyID.</span></span> <span data-ttu-id="ee161-116">担当者は、顧客、ユーザー、または作業者などのシステム内でのロールも保有して、CustID、UserID、WorkerID、および場合によりその他の ロール ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="ee161-116">The person also takes on a role in the system, such as customer, user, or worker, and has a role ID: CustID, UserID, WorkerID, and possibly others.</span></span>

![アドレス帳の構成](../../fin-and-ops/organization-administration/media/address-book-structure.png)

<span data-ttu-id="ee161-118">時には、入力して説明するのに使用されている情報を確認したり、または Finance and Operations のユーザーが正しいことを識別する場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-118">At times, you might want to verify that the information that is entered and used to describe or otherwise identify a person in Finance and Operations is correct.</span></span> <span data-ttu-id="ee161-119">データを要求したデータ件名と情報を共有すると便利な状況が生じることもあります。</span><span class="sxs-lookup"><span data-stu-id="ee161-119">Situations might also arise where it's useful to share that information with the data subject who requested the data.</span></span> <span data-ttu-id="ee161-120">個人検索レポートは、これらの両方のタスクに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ee161-120">The Person search report can help with both these tasks.</span></span>

<span data-ttu-id="ee161-121">個人検索レポートは拡張可能です。</span><span class="sxs-lookup"><span data-stu-id="ee161-121">The Person search report is extensible.</span></span> <span data-ttu-id="ee161-122">既存のエンティティに探しているすべての個人データが含まれていないことがわかった場合、それらを拡張することができたり、新しいエンティティを上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="ee161-122">If you find that the existing entities do not contain all of the personal data you are looking for, they can be extended, or new entities can be written.</span></span> <span data-ttu-id="ee161-123">さらに、各エンティティのデータ マッピングを変更して、エクスポートしないフィールドを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="ee161-123">In addition, you can change the data mappings for each entity and remove fields that you don't want to export.</span></span>

<span data-ttu-id="ee161-124">担当者検索レポートでは、CustomerID または VendorID などのユーザー用のさまざまな ID を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ee161-124">The Person search report lets you specify different identifiers for a person, such as a CustomerID or VendorID.</span></span> <span data-ttu-id="ee161-125">指定した人物にのみ関連する個人データを収集、フィルターして、エンティティ コレクション セットに設定します。</span><span class="sxs-lookup"><span data-stu-id="ee161-125">It will then collect, filter, and populate the entity collection set with personal data that is related only to the person you specified.</span></span>

<span data-ttu-id="ee161-126">あまりないことですが、1 人のユーザーがシステムに複数回入力される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-126">On rare occasions, a single person might be entered in your system more than once.</span></span> <span data-ttu-id="ee161-127">個人検索レポートを使用すると、1 つのレポートに含める各担当者インスタンスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ee161-127">The Person search report lets you specify each person instance to be included on a single report.</span></span> <span data-ttu-id="ee161-128">たとえば、Fred Smith という名前のユーザーは、「Fred Smith」および「F」の両方である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-128">For example, someone named Fred Smith might be both "Fred Smith" and "F.</span></span> <span data-ttu-id="ee161-129">D。</span><span class="sxs-lookup"><span data-stu-id="ee161-129">D.</span></span> <span data-ttu-id="ee161-130">アドレス帳の "Smith"。</span><span class="sxs-lookup"><span data-stu-id="ee161-130">Smith" in your address book.</span></span>

<span data-ttu-id="ee161-131">個々が Finance and Operations のデータに複数の関係者として存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-131">An individual might exist as multiple parties in Finance and Operations data.</span></span> <span data-ttu-id="ee161-132">当事者のタイプごとに複数の識別子を提供することができます。各当事者のタイプの個人データは単一のレポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee161-132">You can provide multiple identifiers for each party type, and each party type's personal data will be included on a single report.</span></span>

## <a name="download-the-default-template"></a><span data-ttu-id="ee161-133">既定のテンプレートのダウンロード</span><span class="sxs-lookup"><span data-stu-id="ee161-133">Download the default template</span></span>

<span data-ttu-id="ee161-134">個人のテンプレートには、情報をダウンロードするために使用されるエンティティの一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee161-134">The Person template contains a list of the entities that will be used to download information.</span></span> <span data-ttu-id="ee161-135">テンプレートは、個人検索レポートを使用する前にロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-135">The template must be loaded before the Person search report can be used.</span></span> <span data-ttu-id="ee161-136">テンプレートは、バージョン 7.2 以降のデータ管理のテンプレート フォームからロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="ee161-136">The template can be loaded from within the Templates form in Data management for versions 7.2 and later.</span></span> <span data-ttu-id="ee161-137">**データ管理**からテンプレートをダウンロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ee161-137">To download templates fronm **Data management**, complete the following steps.</span></span> 

> 1. <span data-ttu-id="ee161-138">**データ管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="ee161-138">Open the **Data management** workspace.</span></span>
> 2. <span data-ttu-id="ee161-139">ワークスペースが初めて開かれた場合は、すべてのデータ エンティティが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="ee161-139">If this is the first time that the workspace has been opened, it will load all of the data entities.</span></span> <span data-ttu-id="ee161-140">テンプレートをロードする前に、すべてのデータ エンティティをロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-140">You must load all the data entities before you load the template.</span></span>
> 3. <span data-ttu-id="ee161-141">**テンプレート**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee161-141">Click the **Templates** tile.</span></span>
> 4. <span data-ttu-id="ee161-142">**既定のテンプレートの読み込み**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee161-142">Select the **Load default templates** button.</span></span>
> 5. <span data-ttu-id="ee161-143">**個人検索**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee161-143">Select **Person search**.</span></span>
> 6. <span data-ttu-id="ee161-144">**選択済の読み込み**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee161-144">Click  **Load selected**.</span></span>

<span data-ttu-id="ee161-145">LCS からテンプレートをダウンロードすることも、7.1 以降のバージョンのインポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="ee161-145">You can also download a template from LCS and import it for versions 7.1 or later.</span></span> <span data-ttu-id="ee161-146">そのためには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ee161-146">To do so, complete the following steps.</span></span>
> 1.    <span data-ttu-id="ee161-147">LCS にログインします。</span><span class="sxs-lookup"><span data-stu-id="ee161-147">Log in to LCS.</span></span>
> 2.    <span data-ttu-id="ee161-148">**共有資産ライブラリ**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee161-148">Click the **Shared asset library** tile.</span></span>
> 3.    <span data-ttu-id="ee161-149">**データ パッケージ資産**タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee161-149">Select the **Data package asset** type.</span></span>
> 4.    <span data-ttu-id="ee161-150">**テンプレート -x.x- 個人の検索** (x.x は現在お使いの Finance and Operations、Talent or Retail のバージョン) という名前のテンプレートをクリックしてダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="ee161-150">Click the template named **Template-x.x-Person search**, where x.x is the version of Finance and Operations, Talent or Retail that you're using, and download it.</span></span>
> 5.    <span data-ttu-id="ee161-151">**データ管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="ee161-151">Open the **Data Management** workspace.</span></span>
> 6.    <span data-ttu-id="ee161-152">ワークスペースが初めて開かれた場合は、ワークスペースはすべてのデータ エンティティを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="ee161-152">If this is the first time that the workspace has been opened, the workspace will load all of the data entities.</span></span> <span data-ttu-id="ee161-153">すべてのエンティティは、テンプレートをダウンロードする前に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="ee161-153">All entities loaded before you download the template.</span></span>
> 7.    <span data-ttu-id="ee161-154">**テンプレート**タイルでクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee161-154">Click on the **Templates** tile.</span></span>
> 8.    <span data-ttu-id="ee161-155">**個人検索**と呼ばれる新しいテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee161-155">Create a new template called **Person search**.</span></span>
> 9.    <span data-ttu-id="ee161-156">**テンプレートのインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee161-156">Click **Import template**.</span></span>
> 10.   <span data-ttu-id="ee161-157">テンプレートを参照して、**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee161-157">Browse to the template and click **Upload**.</span></span>
> 11.   <span data-ttu-id="ee161-158">テンプレートをインポートするには、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee161-158">Click **OK** to import the template.</span></span>


## <a name="generate-a-person-search"></a><span data-ttu-id="ee161-159">個人検索を生成します</span><span class="sxs-lookup"><span data-stu-id="ee161-159">Generate a person search</span></span>

<span data-ttu-id="ee161-160">個人検索レポートを使用するには、次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-160">To use the Person search report, you must complete these tasks.</span></span>

1.  <span data-ttu-id="ee161-161">システム管理メニューから個人検索リスト ページを開き、新しい検索を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee161-161">From the System administration menu, open the Person search list page, and create a new search.</span></span>

    ![個人の検索リスト ページ](../media/gdpr-person-search-list-page.png)

2.  <span data-ttu-id="ee161-163">検索には、ID、名前、アドレスの 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="ee161-163">The search gives you three options: you can search by ID, by name, or by address.</span></span> <span data-ttu-id="ee161-164">必要な検索のタイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="ee161-164">Add the type of search that you want.</span></span>

    ![検索の定義](../media/gdpr-define-search.png)

3.  <span data-ttu-id="ee161-166">結果を表示するために検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="ee161-166">Run the search to show the results.</span></span>

4.  <span data-ttu-id="ee161-167">結果が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ee161-167">Verify that the results are valid.</span></span> <span data-ttu-id="ee161-168">レポートに含めたくない情報を返してくる選択を解除します。</span><span class="sxs-lookup"><span data-stu-id="ee161-168">Clear any selections that return information that you don't want to include on the report.</span></span>

    ![検索結果の確認](../media/gdpr-review-search-results.png)

5.  <span data-ttu-id="ee161-170">**プロセス レポート** を選択し、担当者検索テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee161-170">Select **Process report**, and then select the Person search template.</span></span>

    ![レポートを処理する](../media/gdpr-process-report.png)

6.  <span data-ttu-id="ee161-172">**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee161-172">Select **OK**.</span></span> <span data-ttu-id="ee161-173">データ パッケージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="ee161-173">A data package is generated.</span></span>

7. <span data-ttu-id="ee161-174">パッケージが生成されたら、選択したデータ形式でそれをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="ee161-174">When the package has been generated, export it to your selected data format.</span></span> 

> <span data-ttu-id="ee161-175">レコードに添付されたドキュメントは、データ エクスポートに含まれません。</span><span class="sxs-lookup"><span data-stu-id="ee161-175">Documents that are attached to records are not included in the data export.</span></span> <span data-ttu-id="ee161-176">添付ファイルは手動でダウンロードし、個人データを要求した各個人と共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee161-176">Attachments must be manually downloaded and shared with the individual who requested personal data.</span></span>



## <a name="additional-resources"></a><span data-ttu-id="ee161-177">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="ee161-177">Additional resources</span></span>

<span data-ttu-id="ee161-178">GDPR の詳細については、[欧州連合の Web サイト](https://europa.eu/)、[Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx)  および [Microsoft Dynamics 365 for Finance and Operations の GDPR に関するガイド](./gdpr-guide.md) トピックの情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee161-178">You can learn more about the GDPR on the [European Union's website](https://europa.eu/), from information on the [Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx) and in the [Guide to the GDPR for Microsoft Dynamics 365 for Finance and Operations](./gdpr-guide.md) topic.</span></span>


### <a name="disclaimer"></a><span data-ttu-id="ee161-179">免責事項</span><span class="sxs-lookup"><span data-stu-id="ee161-179">Disclaimer</span></span>
<span data-ttu-id="ee161-180">(c)2018 Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="ee161-180">(c)2018 Microsoft Corporation.</span></span> <span data-ttu-id="ee161-181">All rights reserved.</span><span class="sxs-lookup"><span data-stu-id="ee161-181">All rights reserved.</span></span> <span data-ttu-id="ee161-182">このドキュメントは、"現状のまま" 提供されます。</span><span class="sxs-lookup"><span data-stu-id="ee161-182">This document is provided "as-is."</span></span> <span data-ttu-id="ee161-183">URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="ee161-183">Information and views expressed in this document, including URL and other Internet Web site references, may change without notice.</span></span> <span data-ttu-id="ee161-184">このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。</span><span class="sxs-lookup"><span data-stu-id="ee161-184">You bear the risk of using it.</span></span> <span data-ttu-id="ee161-185">このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。</span><span class="sxs-lookup"><span data-stu-id="ee161-185">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="ee161-186">内部での参照を目的とする場合、このドキュメントをコピーして使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee161-186">You may copy and use this document for your internal, reference purposes.</span></span> 
