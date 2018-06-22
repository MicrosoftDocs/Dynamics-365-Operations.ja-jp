---
title: "個人検索レポート"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations の個人データ レポートについて説明します。"
author: rschloma
manager: AnnBe
ms.date: 01/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 21a933fd242791d03a3cc44ebdfa7b8de1baa11b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="the-person-search-report"></a><span data-ttu-id="9a178-103">個人検索レポート</span><span class="sxs-lookup"><span data-stu-id="9a178-103">The Person search report</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="9a178-104">担当者検索レポートは、Microsoft Dynamics 365 for Finance and Operations の既存のデータ管理フレームワークの機能強化です。</span><span class="sxs-lookup"><span data-stu-id="9a178-104">The Person search report is a refinement of the existing Data management framework of Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="9a178-105">データ管理フレームワークには、担当者と、担当者が Finance and Operations で割り当てられる可能性があるロールを定義するために使用される個人データを識別するために Microsoft が作成した、事前パッケージ化されたエンティティ セットが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9a178-105">The Data management framework offers a pre-packaged set of entities that Microsoft authored to identify personal data that is used to define a person and the roles that a person might be assigned to in Finance and Operations.</span></span> 

> [!Note]
> <span data-ttu-id="9a178-106">個人検索レポートは、今後のリリースで使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="9a178-106">The Person search report will be available in an upcoming release.</span></span> <span data-ttu-id="9a178-107">使用可能な場合、Finance and Operations、Microsoft Dynamics 365 for Retail、および Microsoft Dynamics 365 for Talent でレポートを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9a178-107">When available, you'll be able to use the report withFinance and Operations, Microsoft Dynamics 365 for Retail, and Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="9a178-108">このトピックの Finance and Operations への参照は、Retail と Talent にも当てはまります。</span><span class="sxs-lookup"><span data-stu-id="9a178-108">References to Finance and Operations in this topic also apply to Retail and Talent.</span></span> <span data-ttu-id="9a178-109">このレポートは現在、Microsoft Dynamics AX 2012 では使用できません。</span><span class="sxs-lookup"><span data-stu-id="9a178-109">The report is not currently available for Microsoft Dynamics AX 2012.</span></span> 

<span data-ttu-id="9a178-110">Finance and Operations のグローバル アドレス帳を使用すると、データ モデルで関係者として説明されている人物のインスタンスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="9a178-110">You can use the Global address book in Finance and Operations to create an instance of a person that is described in the data model as a party.</span></span> 

<span data-ttu-id="9a178-111">Finance and Operations データに、連絡先、顧客、ユーザー、作業者、またはその他の担当者を追加するとき、通常、その担当者のアドレス帳エントリの作成から開始します。</span><span class="sxs-lookup"><span data-stu-id="9a178-111">When you add a contact, customer, user, worker, or other person in Finance and Operations data, you typically start by creating an address book entry for that person.</span></span> <span data-ttu-id="9a178-112">アドレス帳の各ユーザーは関係者と呼ばれ、PartyID が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="9a178-112">Each person in the address book is referred to as a party and is assigned a PartyID.</span></span> <span data-ttu-id="9a178-113">担当者は、顧客、ユーザー、または作業者などのシステム内でのロールも保有して、CustID、UserID、WorkerID、および場合によりその他の ロール ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="9a178-113">The person also takes on a role in the system, such as customer, user, or worker, and has a role ID: CustID, UserID, WorkerID, and possibly others.</span></span>

![アドレス帳の構成](../../fin-and-ops/organization-administration/media/address-book-structure.png)

<span data-ttu-id="9a178-115">時には、入力して説明するのに使用されている情報を確認したり、または Finance and Operations のユーザーが正しいことを識別する場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a178-115">At times, you might want to verify that the information that is entered and used to describe or otherwise identify a person in Finance and Operations is correct.</span></span> <span data-ttu-id="9a178-116">データを要求したデータ件名と情報を共有すると便利な状況が生じることもあります。</span><span class="sxs-lookup"><span data-stu-id="9a178-116">Situations might also arise where it's useful to share that information with the data subject who requested the data.</span></span> <span data-ttu-id="9a178-117">個人検索レポートは、これらの両方のタスクに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9a178-117">The Person search report can help with both these tasks.</span></span>

<span data-ttu-id="9a178-118">個人検索レポートは拡張可能です。</span><span class="sxs-lookup"><span data-stu-id="9a178-118">The Person search report is extensible.</span></span> <span data-ttu-id="9a178-119">既存のエンティティに探しているすべての個人データが含まれていないことがわかった場合、それらを拡張することができたり、新しいエンティティを上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="9a178-119">If you find that the existing entities do not contain all of the personal data you are looking for, they can be extended, or new entities can be written.</span></span> <span data-ttu-id="9a178-120">さらに、各エンティティのデータ マッピングを変更して、エクスポートしないフィールドを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="9a178-120">In addition, you can change the data mappings for each entity and remove fields that you don't want to export.</span></span>

<span data-ttu-id="9a178-121">担当者検索レポートでは、CustomerID または VendorID などのユーザー用のさまざまな ID を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9a178-121">The Person search report lets you specify different identifiers for a person, such as a CustomerID or VendorID.</span></span> <span data-ttu-id="9a178-122">指定した人物にのみ関連する個人データを収集、フィルターして、エンティティ コレクション セットに設定します。</span><span class="sxs-lookup"><span data-stu-id="9a178-122">It will then collect, filter, and populate the entity collection set with personal data that is related only to the person you specified.</span></span>

<span data-ttu-id="9a178-123">あまりないことですが、1 人のユーザーがシステムに複数回入力される場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a178-123">On rare occasions, a single person might be entered in your system more than once.</span></span> <span data-ttu-id="9a178-124">個人検索レポートを使用すると、1 つのレポートに含める各担当者インスタンスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9a178-124">The Person search report lets you specify each person instance to be included on a single report.</span></span> <span data-ttu-id="9a178-125">たとえば、Fred Smith という名前のユーザーは、「Fred Smith」および「F」の両方である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9a178-125">For example, someone named Fred Smith might be both "Fred Smith" and "F.</span></span> <span data-ttu-id="9a178-126">D。</span><span class="sxs-lookup"><span data-stu-id="9a178-126">D.</span></span> <span data-ttu-id="9a178-127">アドレス帳の "Smith"。</span><span class="sxs-lookup"><span data-stu-id="9a178-127">Smith" in your address book.</span></span>

<span data-ttu-id="9a178-128">個々が Finance and Operations のデータに複数の関係者として存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9a178-128">An individual might exist as multiple parties in Finance and Operations data.</span></span> <span data-ttu-id="9a178-129">当事者のタイプごとに複数の識別子を提供することができます。各当事者のタイプの個人データは単一のレポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="9a178-129">You can provide multiple identifiers for each party type, and each party type's personal data will be included on a single report.</span></span>

<span data-ttu-id="9a178-130">個人検索レポートを使用するには、次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a178-130">To use the Person search report, you must complete these tasks.</span></span>

1.  <span data-ttu-id="9a178-131">システム管理メニューから個人検索リスト ページを開き、新しい検索を作成します。</span><span class="sxs-lookup"><span data-stu-id="9a178-131">From the System administration menu, open the Person search list page, and create a new search.</span></span>

    ![個人の検索リスト ページ](../media/gdpr-person-search-list-page.png)

2.  <span data-ttu-id="9a178-133">検索には、ID、名前、アドレスの 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="9a178-133">The search gives you three options: you can search by ID, by name, or by address.</span></span> <span data-ttu-id="9a178-134">必要な検索のタイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="9a178-134">Add the type of search that you want.</span></span>

    ![検索の定義](../media/gdpr-define-search.png)

3.  <span data-ttu-id="9a178-136">結果を表示するために検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a178-136">Run the search to show the results.</span></span>

4.  <span data-ttu-id="9a178-137">結果が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a178-137">Verify that the results are valid.</span></span> <span data-ttu-id="9a178-138">レポートに含めたくない情報を返してくる選択を解除します。</span><span class="sxs-lookup"><span data-stu-id="9a178-138">Clear any selections that return information that you don't want to include on the report.</span></span>

    ![検索結果の確認](../media/gdpr-review-search-results.png)

5.  <span data-ttu-id="9a178-140">**プロセス レポート** を選択し、担当者検索テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a178-140">Select **Process report**, and then select the Person search template.</span></span>

    ![レポートを処理する](../media/gdpr-process-report.png)

6.  <span data-ttu-id="9a178-142">**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a178-142">Select **OK**.</span></span> <span data-ttu-id="9a178-143">データ パッケージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="9a178-143">A data package is generated.</span></span>

7. <span data-ttu-id="9a178-144">パッケージが生成されたら、選択したデータ形式でそれをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="9a178-144">When the package has been generated, export it to your selected data format.</span></span> 

> <span data-ttu-id="9a178-145">レコードに添付されたドキュメントは、データ エクスポートに含まれません。</span><span class="sxs-lookup"><span data-stu-id="9a178-145">Documents that are attached to records are not included in the data export.</span></span> <span data-ttu-id="9a178-146">添付ファイルは手動でダウンロードし、個人データを要求した各個人と共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a178-146">Attachments must be manually downloaded and shared with the individual who requested personal data.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a178-147">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="9a178-147">Additional resources</span></span>

<span data-ttu-id="9a178-148">GDPR の詳細については、[欧州連合の Web サイト](http://europa.eu/)、[Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx) および [Microsoft Dynamics 365 for Finance and Operations の GDPR に関するガイド](./gdpr-guide.md) のトピックの情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a178-148">You can learn more about the GDPR on the [European Union's website](http://europa.eu/), from information on the [Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx) and in the [Guide to the GDPR for Microsoft Dynamics 365 for Finance and Operations](./gdpr-guide.md) topic.</span></span>


### <a name="disclaimer"></a><span data-ttu-id="9a178-149">免責事項</span><span class="sxs-lookup"><span data-stu-id="9a178-149">Disclaimer</span></span>
<span data-ttu-id="9a178-150">(c)2018 Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="9a178-150">(c)2018 Microsoft Corporation.</span></span> <span data-ttu-id="9a178-151">All rights reserved.</span><span class="sxs-lookup"><span data-stu-id="9a178-151">All rights reserved.</span></span> <span data-ttu-id="9a178-152">このドキュメントは、"現状のまま" 提供されます。</span><span class="sxs-lookup"><span data-stu-id="9a178-152">This document is provided "as-is."</span></span> <span data-ttu-id="9a178-153">URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="9a178-153">Information and views expressed in this document, including URL and other Internet Web site references, may change without notice.</span></span> <span data-ttu-id="9a178-154">このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。</span><span class="sxs-lookup"><span data-stu-id="9a178-154">You bear the risk of using it.</span></span> <span data-ttu-id="9a178-155">このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。</span><span class="sxs-lookup"><span data-stu-id="9a178-155">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="9a178-156">内部での参照を目的とする場合、このドキュメントをコピーして使用できます。</span><span class="sxs-lookup"><span data-stu-id="9a178-156">You may copy and use this document for your internal, reference purposes.</span></span> 

