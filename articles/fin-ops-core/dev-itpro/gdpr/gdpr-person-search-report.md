---
title: 個人検索レポート
description: このトピックでは、Finance and Operations アプリの個人データ レポートに関する情報を提供します。
author: rschloma
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dadb00a9afc4008c734f895e83476911ecb3b786
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750292"
---
# <a name="person-search-report"></a><span data-ttu-id="f57a0-103">個人検索レポート</span><span class="sxs-lookup"><span data-stu-id="f57a0-103">Person search report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f57a0-104">個人検索レポートは、既存の Finance and Operations アプリのデータ管理フレームワークの機能を強化したものです。</span><span class="sxs-lookup"><span data-stu-id="f57a0-104">The Person search report is a refinement of the existing Data management framework of Finance and Operations apps.</span></span> <span data-ttu-id="f57a0-105">データ管理フレームワークには、ユーザーと、ユーザーが Finance and Operations アプリケーションで割り当てられる可能性があるロールを定義するために使用される個人データを識別するために Microsoft が作成した、事前パッケージ化されたエンティティ セットが用意されています。</span><span class="sxs-lookup"><span data-stu-id="f57a0-105">The Data management framework offers a pre-packaged set of entities that Microsoft authored to identify personal data that is used to define a person and the roles that a person might be assigned to in Finance and Operations applications.</span></span> 

> [!NOTE]
> <span data-ttu-id="f57a0-106">レポートは、Dynamics 365 Finance、Supply Chain Management、コマース、および人事管理で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-106">You can use the report with Dynamics 365 Finance, Supply Chain Management, Commerce, and Human Resources.</span></span> <span data-ttu-id="f57a0-107">Microsoft Dynamics AX 2012 では今のところレポートは使用できません。</span><span class="sxs-lookup"><span data-stu-id="f57a0-107">The report is not currently available for Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="f57a0-108">個人検索レポートは、バージョン 8.0 で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="f57a0-108">The Person search report is available in version 8.0.</span></span> <span data-ttu-id="f57a0-109">レポートはバージョン 7.3 (毎月の更新プログラム 7.3.2 経由で配信)、バージョン 7.2 (KB 4132615 経由)、およびバージョン7.1 (KB 4132441 経由 ) でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-109">The report is also available in version 7.3 (delivered via monthly update 7.3.2), in version 7.2 (via KB 4132615), and in version 7.1 (via KB 4132441).</span></span> <span data-ttu-id="f57a0-110">個人検索レポートが定期的に更新される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-110">The Person search report may be updated periodically.</span></span> <span data-ttu-id="f57a0-111">このレポートを使用する前に、すべての関連する修正プログラムを取得し、適用したことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-111">Before using this report, you need to ensure that you have obtained and applied all relevant hotfixes.</span></span> 

<span data-ttu-id="f57a0-112">グローバル アドレス帳を使用すると、データ モデルで関係者として説明されている人物のインスタンスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-112">You can use the Global address book to create an instance of a person that is described in the data model as a party.</span></span> 

<span data-ttu-id="f57a0-113">Finance and Operations データに、連絡先、顧客、ユーザー、作業者、またはその他の担当者を追加するとき、通常、その担当者のアドレス帳エントリの作成から開始します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-113">When you add a contact, customer, user, worker, or other person in Finance and Operations data, you typically start by creating an address book entry for that person.</span></span> <span data-ttu-id="f57a0-114">アドレス帳の各ユーザーは関係者と呼ばれ、PartyID が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-114">Each person in the address book is referred to as a party and is assigned a PartyID.</span></span> <span data-ttu-id="f57a0-115">担当者は、顧客、ユーザー、または作業者などのシステム内でのロールも保有して、CustID、UserID、WorkerID、および場合によりその他の ロール ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-115">The person also takes on a role in the system, such as customer, user, or worker, and has a role ID: CustID, UserID, WorkerID, and possibly others.</span></span>

![アドレス帳の構成](../../fin-ops/organization-administration/media/address-book-structure.png)

<span data-ttu-id="f57a0-117">時には、入力して説明するのに使用されている情報を確認したり、またはユーザーが正しいことを識別する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-117">At times, you might want to verify that the information that is entered and used to describe or otherwise identify a person is correct.</span></span> <span data-ttu-id="f57a0-118">データを要求したデータ件名と情報を共有すると便利な状況が生じることもあります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-118">Situations might also arise where it's useful to share that information with the data subject who requested the data.</span></span> <span data-ttu-id="f57a0-119">個人検索レポートは、これらの両方のタスクに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-119">The Person search report can help with both these tasks.</span></span>

<span data-ttu-id="f57a0-120">個人検索レポートは拡張可能です。</span><span class="sxs-lookup"><span data-stu-id="f57a0-120">The Person search report is extensible.</span></span> <span data-ttu-id="f57a0-121">既存のエンティティに探しているすべての個人データが含まれていないことがわかった場合、それらを拡張することができたり、新しいエンティティを上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-121">If you find that the existing entities do not contain all of the personal data you are looking for, they can be extended, or new entities can be written.</span></span> <span data-ttu-id="f57a0-122">さらに、各エンティティのデータ マッピングを変更して、エクスポートしないフィールドを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-122">In addition, you can change the data mappings for each entity and remove fields that you don't want to export.</span></span>

<span data-ttu-id="f57a0-123">担当者検索レポートでは、CustomerID または VendorID などのユーザー用のさまざまな ID を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-123">The Person search report lets you specify different identifiers for a person, such as a CustomerID or VendorID.</span></span> <span data-ttu-id="f57a0-124">指定した人物にのみ関連する個人データを収集、フィルターして、エンティティ コレクション セットに設定します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-124">It will then collect, filter, and populate the entity collection set with personal data that is related only to the person you specified.</span></span>

<span data-ttu-id="f57a0-125">あまりないことですが、1 人のユーザーがシステムに複数回入力される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-125">On rare occasions, a single person might be entered in your system more than once.</span></span> <span data-ttu-id="f57a0-126">個人検索レポートを使用すると、1 つのレポートに含める各担当者インスタンスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-126">The Person search report lets you specify each person instance to be included on a single report.</span></span> <span data-ttu-id="f57a0-127">たとえば、Fred Smith という名前のユーザーは、「Fred Smith」および「F」の両方である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-127">For example, someone named Fred Smith might be both "Fred Smith" and "F.</span></span> <span data-ttu-id="f57a0-128">D。</span><span class="sxs-lookup"><span data-stu-id="f57a0-128">D.</span></span> <span data-ttu-id="f57a0-129">アドレス帳の "Smith"。</span><span class="sxs-lookup"><span data-stu-id="f57a0-129">Smith" in your address book.</span></span>

<span data-ttu-id="f57a0-130">個人がデータに複数の関係者として存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-130">An individual might exist as multiple parties in data.</span></span> <span data-ttu-id="f57a0-131">当事者のタイプごとに複数の識別子を提供することができます。各当事者のタイプの個人データは単一のレポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-131">You can provide multiple identifiers for each party type, and each party type's personal data will be included on a single report.</span></span>

## <a name="download-the-default-template"></a><span data-ttu-id="f57a0-132">既定のテンプレートのダウンロード</span><span class="sxs-lookup"><span data-stu-id="f57a0-132">Download the default template</span></span>

<span data-ttu-id="f57a0-133">個人のテンプレートには、情報をダウンロードするために使用されるエンティティの一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-133">The Person template contains a list of the entities that will be used to download information.</span></span> <span data-ttu-id="f57a0-134">テンプレートは、個人検索レポートを使用する前にロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-134">The template must be loaded before the Person search report can be used.</span></span> <span data-ttu-id="f57a0-135">テンプレートは、バージョン 7.2 以降のデータ管理のテンプレート フォームからロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-135">The template can be loaded from within the Templates form in Data management for versions 7.2 and later.</span></span> <span data-ttu-id="f57a0-136">**データ管理** からテンプレートをダウンロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-136">To download templates fronm **Data management**, complete the following steps.</span></span> 

1. <span data-ttu-id="f57a0-137">**データ管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-137">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="f57a0-138">ワークスペースが初めて開かれた場合は、すべてのデータ エンティティが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-138">If this is the first time that the workspace has been opened, it will load all of the data entities.</span></span> <span data-ttu-id="f57a0-139">テンプレートをロードする前に、すべてのデータ エンティティをロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-139">You must load all the data entities before you load the template.</span></span>
3. <span data-ttu-id="f57a0-140">**テンプレート** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-140">Click the **Templates** tile.</span></span>
4. <span data-ttu-id="f57a0-141">**既定のテンプレートの読み込み** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-141">Select the **Load default templates** button.</span></span>
5. <span data-ttu-id="f57a0-142">**個人検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-142">Select **Person search**.</span></span>
6. <span data-ttu-id="f57a0-143">**選択済の読み込み** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-143">Click  **Load selected**.</span></span>

<span data-ttu-id="f57a0-144">LCS からテンプレートをダウンロードすることも、7.1 以降のバージョンのインポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-144">You can also download a template from LCS and import it for versions 7.1 or later.</span></span> <span data-ttu-id="f57a0-145">そのためには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-145">To do so, complete the following steps.</span></span>
1.  <span data-ttu-id="f57a0-146">LCS にログインします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-146">Log in to LCS.</span></span>
2.  <span data-ttu-id="f57a0-147">**共有資産ライブラリ** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-147">Click the **Shared asset library** tile.</span></span>
3.  <span data-ttu-id="f57a0-148">**データ パッケージ資産** タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-148">Select the **Data package asset** type.</span></span>
4.  <span data-ttu-id="f57a0-149">**テンプレート -x.x- 個人の検索** (x.x は現在お使いのアプリケーションのバージョン) という名前のテンプレートをクリックしてダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-149">Click the template named **Template-x.x-Person search**, where x.x is the application version that you're using, and download it.</span></span>
5.  <span data-ttu-id="f57a0-150">**データ管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-150">Open the **Data Management** workspace.</span></span>
6.  <span data-ttu-id="f57a0-151">ワークスペースが初めて開かれた場合は、ワークスペースはすべてのデータ エンティティを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-151">If this is the first time that the workspace has been opened, the workspace will load all of the data entities.</span></span> <span data-ttu-id="f57a0-152">すべてのエンティティは、テンプレートをダウンロードする前に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-152">All entities loaded before you download the template.</span></span>
7.  <span data-ttu-id="f57a0-153">**テンプレート** タイルでクリックします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-153">Click on the **Templates** tile.</span></span>
8.  <span data-ttu-id="f57a0-154">**個人検索** と呼ばれる新しいテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-154">Create a new template called **Person search**.</span></span>
9.  <span data-ttu-id="f57a0-155">**テンプレートのインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-155">Click **Import template**.</span></span>
10. <span data-ttu-id="f57a0-156">テンプレートを参照して、**アップロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-156">Browse to the template and click **Upload**.</span></span>
11. <span data-ttu-id="f57a0-157">テンプレートをインポートするには、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-157">Click **OK** to import the template.</span></span>


## <a name="generate-a-person-search"></a><span data-ttu-id="f57a0-158">個人検索を生成します</span><span class="sxs-lookup"><span data-stu-id="f57a0-158">Generate a person search</span></span>

<span data-ttu-id="f57a0-159">個人検索レポートを使用するには、次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-159">To use the Person search report, you must complete these tasks.</span></span>

1.  <span data-ttu-id="f57a0-160">システム管理メニューから個人検索リスト ページを開き、新しい検索を作成します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-160">From the System administration menu, open the Person search list page, and create a new search.</span></span>

    ![個人の検索リスト ページ](../media/gdpr-person-search-list-page.png)

2.  <span data-ttu-id="f57a0-162">検索には、ID、名前、アドレスの 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-162">The search gives you three options: you can search by ID, by name, or by address.</span></span> <span data-ttu-id="f57a0-163">必要な検索のタイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-163">Add the type of search that you want.</span></span>

    ![検索の定義](../media/gdpr-define-search.png)

3.  <span data-ttu-id="f57a0-165">結果を表示するために検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-165">Run the search to show the results.</span></span>

4.  <span data-ttu-id="f57a0-166">結果が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-166">Verify that the results are valid.</span></span> <span data-ttu-id="f57a0-167">レポートに含めたくない情報を返してくる選択を解除します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-167">Clear any selections that return information that you don't want to include on the report.</span></span>

    ![検索結果の確認](../media/gdpr-review-search-results.png)

5.  <span data-ttu-id="f57a0-169">**プロセス レポート** を選択し、担当者検索テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-169">Select **Process report**, and then select the Person search template.</span></span>

    ![レポートを処理する](../media/gdpr-process-report.png)

6.  <span data-ttu-id="f57a0-171">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f57a0-171">Select **OK**.</span></span> <span data-ttu-id="f57a0-172">データ パッケージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-172">A data package is generated.</span></span>

7. <span data-ttu-id="f57a0-173">パッケージが生成されたら、選択したデータ形式でそれをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-173">When the package has been generated, export it to your selected data format.</span></span> 

> [!NOTE]
> <span data-ttu-id="f57a0-174">レコードに添付されたドキュメントは、データ エクスポートに含まれません。</span><span class="sxs-lookup"><span data-stu-id="f57a0-174">Documents that are attached to records are not included in the data export.</span></span> <span data-ttu-id="f57a0-175">添付ファイルは手動でダウンロードし、個人データを要求した各個人と共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-175">Attachments must be manually downloaded and shared with the individual who requested personal data.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="f57a0-176">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f57a0-176">Additional resources</span></span>

<span data-ttu-id="f57a0-177">GDPR の詳細については、[欧州連合の Web サイト](https://europa.eu/)、[Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx) および[一般データ保護規則の概要](./gdpr-guide.md) の情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f57a0-177">You can learn more about the GDPR on the [European Union's website](https://europa.eu/), from information on the [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx) and in [General Data Protection Regulation overview](./gdpr-guide.md).</span></span>


### <a name="disclaimer"></a><span data-ttu-id="f57a0-178">免責事項</span><span class="sxs-lookup"><span data-stu-id="f57a0-178">Disclaimer</span></span>
<span data-ttu-id="f57a0-179">(c)2019 Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="f57a0-179">(c)2019 Microsoft Corporation.</span></span> <span data-ttu-id="f57a0-180">All rights reserved.</span><span class="sxs-lookup"><span data-stu-id="f57a0-180">All rights reserved.</span></span> <span data-ttu-id="f57a0-181">このドキュメントは、"現状のまま" 提供されます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-181">This document is provided "as-is."</span></span> <span data-ttu-id="f57a0-182">URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="f57a0-182">Information and views expressed in this document, including URL and other Internet Web site references, may change without notice.</span></span> <span data-ttu-id="f57a0-183">このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。</span><span class="sxs-lookup"><span data-stu-id="f57a0-183">You bear the risk of using it.</span></span> <span data-ttu-id="f57a0-184">このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。</span><span class="sxs-lookup"><span data-stu-id="f57a0-184">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="f57a0-185">内部での参照を目的とする場合、このドキュメントをコピーして使用できます。</span><span class="sxs-lookup"><span data-stu-id="f57a0-185">You may copy and use this document for your internal, reference purposes.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]