---
title: "法人間の HR パラメータの設定"
description: "職位レコードなど、会社間で共有されるのレコードの共有パラメーターを設定する必要があります。 この記事は、法人間に人事管理パラメーターを設定する方法を説明します。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 25d342272581abb96127d8761b3eac8d4f7695df
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-hr-parameters-across-legal-entities"></a><span data-ttu-id="a6513-104">法人間の HR パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="a6513-104">Set up HR parameters across legal entities</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a6513-105">職位レコードなど、会社間で共有されるのレコードの共有パラメーターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6513-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="a6513-106">この記事は、法人間に人事管理パラメーターを設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a6513-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="a6513-107">職位レコードなどの一部のレコード タイプは、会社間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="a6513-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="a6513-108">これらのレコードに対して、共有パラメータを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6513-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="a6513-109">たとえば、法人間で人事管理パラメーターを設定する場合、**人事管理、パラメータを共有**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6513-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="a6513-110">**人事管理の共有パラメーター**ページで、パラメータは機能に基づいて領域にグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="a6513-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="a6513-111">以前にリリースされた機能</span><span class="sxs-lookup"><span data-stu-id="a6513-111">Previously released functionality</span></span>
<span data-ttu-id="a6513-112">**ID** タブで、ページに表示される ID 番号を表す ID タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6513-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="a6513-113">作業者の ID 情報を入力する前に、ID タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6513-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="a6513-114">社会保障番号、国民 ID 番号、外国人 ID 番号、および個人の ID コードに関する情報が**ID タイプ**ページで管理されます。</span><span class="sxs-lookup"><span data-stu-id="a6513-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="a6513-115">新しい ID タイプを定義する、または既存のタイプの一覧を確認するには、[**人事管理**] &gt; [**リンク タブ**] &gt; [**設定**] &gt; [**ID タイプ**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6513-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="a6513-116">簡単なコードと説明を入力できます。</span><span class="sxs-lookup"><span data-stu-id="a6513-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="a6513-117">Dynamics 365 for Talent を使用している場合</span><span class="sxs-lookup"><span data-stu-id="a6513-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="a6513-118">**ID** タブで、ページに表示される ID 番号を表す ID タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6513-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="a6513-119">作業者の ID 情報を入力する前に、ID タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6513-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="a6513-120">社会保障番号、国民 ID 番号、外国人 ID 番号、および個人の ID コードに関する情報が**ID タイプ**ページで管理されます。</span><span class="sxs-lookup"><span data-stu-id="a6513-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="a6513-121">新しい ID タイプを定義する、または既存のタイプの一覧を確認するには、[**人事管理**] &gt; [**設定**] &gt; [**ID タイプ**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6513-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="a6513-122">簡単なコードと説明を入力できます。</span><span class="sxs-lookup"><span data-stu-id="a6513-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="a6513-123">**番号順序**タブで、次のレコードに使用する番号順序を選択できます: 個人番号、職位、ユーザー要求 ID、I-9 ドキュメント、申請者、ディスカッション、福利厚生のID、および従業員のアクション (このレコード タイプが有効な場合)。</span><span class="sxs-lookup"><span data-stu-id="a6513-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="a6513-124">番号順序およびコードを管理するには、**番号順序**リスト ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6513-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="a6513-125">このページを検索するには、ページの検索機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6513-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="a6513-126">**職位**タブで、新しい職位が既定で割り当てに使用できるかどうかを指定します:</span><span class="sxs-lookup"><span data-stu-id="a6513-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="a6513-127">**常時** – 職位の作成時に新しい職位に作業者を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="a6513-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="a6513-128">職位を作成すると、[**職位**] ページの [**概要**] タブ上の [**割り当てに使用可能**] 日時が、自動的に作成日時に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a6513-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="a6513-129">**なし** – 職位の作成時に新しい職位に作業者を割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="a6513-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="a6513-130">このオプションを選択する場合、新しい各職位が使用できるように**職位**ページを開き、作業者の割り当てを有効にするのに**一般**タブの**割り当てに使用可能**日付を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6513-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="see-also"></a><span data-ttu-id="a6513-131">参照</span><span class="sxs-lookup"><span data-stu-id="a6513-131">See also</span></span>
--------

[<span data-ttu-id="a6513-132">会社固有の HR パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="a6513-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)




