---
title: "会社固有の HR パラメータの設定"
description: "他のパラメーター設定は会社固有ですが、人事管理 (HR) のパラメーター設定は会社間で共有されます。 この記事は、会社固有の HR パラメーターを設定する方法を説明します。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 1ec4fec633b1c697193758cf9f0e80ff46098008
ms.contentlocale: ja-jp
ms.lasthandoff: 01/31/2018

---

# <a name="set-up-company-specific-hr-parameters"></a><span data-ttu-id="9a5bc-104">会社固有の HR パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="9a5bc-104">Set up company-specific HR parameters</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="9a5bc-105">他のパラメーター設定は会社固有ですが、人事管理 (HR) のパラメーター設定は会社間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-105">The settings of some Human resources (HR) parameters are shared across companies, whereas the settings of other parameters are company-specific.</span></span> <span data-ttu-id="9a5bc-106">この記事は、会社固有の HR パラメーターを設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-106">This article explains how to set up company-specific HR parameters.</span></span>

<span data-ttu-id="9a5bc-107">2 つのページが人事管理 (HR) のパラメータの設定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-107">Two pages are used to set Human resources (HR) parameters.</span></span> <span data-ttu-id="9a5bc-108">会社間で共有されるパラメータに、**人事管理の共有パラメーター**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-108">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="9a5bc-109">会社固有のパラメータ (つまり、設定を単一の会社に適用する場合) に、**人事管理パラメータ**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-109">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span> <span data-ttu-id="9a5bc-110">**人事管理パラメーター**ページで、設定は 6 つのタブに分割されます:</span><span class="sxs-lookup"><span data-stu-id="9a5bc-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

-   <span data-ttu-id="9a5bc-111">一般</span><span class="sxs-lookup"><span data-stu-id="9a5bc-111">General</span></span>
-   <span data-ttu-id="9a5bc-112">採用 - これは Dynamics 365 for Talent には含まれていません。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-112">Recruitment - this is not included in Dynamics 365 for Talent</span></span>
-   <span data-ttu-id="9a5bc-113">報酬</span><span class="sxs-lookup"><span data-stu-id="9a5bc-113">Compensation</span></span>
-   <span data-ttu-id="9a5bc-114">番号順序</span><span class="sxs-lookup"><span data-stu-id="9a5bc-114">Number sequences</span></span>
-   <span data-ttu-id="9a5bc-115">育児介護休業法 (FMLA)</span><span class="sxs-lookup"><span data-stu-id="9a5bc-115">Family and Medical Leave Act (FMLA)</span></span>
-   <span data-ttu-id="9a5bc-116">従業員セルフサービス</span><span class="sxs-lookup"><span data-stu-id="9a5bc-116">Employee self-service</span></span>

<span data-ttu-id="9a5bc-117">各タブには単一の会社に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-117">Each tab contains information that pertains to a single company.</span></span> <span data-ttu-id="9a5bc-118">**概要**タブの設定は、休暇、傷害と疾病、新規採用に関する情報の外観を定義します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-118">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="9a5bc-119">このタブの設定は、作業中と表示される既定のエントリも定義します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-119">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="9a5bc-120">特に、このタブでは、未処理の休暇トランザクションに適用する色を選択し、レポートに使用するスタイル シートを指定したり、トレーニング コースと休暇登録の間の統合を有効にし、この統合の管理に使用する休暇コードを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-120">Specifically, this tab lets you select a color to apply to open absence transactions, specify the style sheet to use for reports, enable the integration between training courses and absence registration, and select the absence code that is used to control this integration.</span></span> <span data-ttu-id="9a5bc-121">また、けがと病気のケース インシデントの保持期間を指定することもでき、新しい作業者の雇用時に表示される既定の ID 番号を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-121">You can also indicate how long injury and illness case incidents should be kept, and specify the default identification number that is shown when a new worker is hired.</span></span> 

<span data-ttu-id="9a5bc-122">**採用**タブの設定は、申請者に自動的に送信される通知のドキュメント タイプ、および未承諾の申請に対しての採用プロジェクト (特定の採用プロジェクトに対してでない申請) を定義します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-122">The settings on the **Recruitment** tab define the document types that are used for correspondence that is automatically sent to applicants, and the recruitment project that is used for unsolicited applications (applications that aren't for a specific recruitment project).</span></span> <span data-ttu-id="9a5bc-123">採用プロジェクトのエイジングとして定義されている期間によって、**採用管理**ワークスペースの、**エイジング プロジェクト**タイルに含まれている採用プロジェクトが決まります。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-123">The period that is defined for the recruitment project aging determines the recruitment projects that are included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="9a5bc-124">**採用**ワークスペースの、**申請の期限が近づいています**タイルで申込期限が近づいている採用プロジェクトを表示するために、申請の期限の警告に定義されている期間が使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-124">The period that is defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span> 

<span data-ttu-id="9a5bc-125">[**報酬**] タブの設定は、ユーザーが固定または変動報酬プランの情報を保存するかどうかの確認を定義します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-125">The settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="9a5bc-126">[**保存の検証を有効にします**] チェック ボックスをオンにすると、そのユーザーが報酬に関連付けられたページを閉じるといつでも、レコードを保存するかどうか確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-126">If you select the **Enable save validation** check box, any time that users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="9a5bc-127">報酬管理の一部のページでは、ユーザーが情報を削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-127">Some pages in compensation management don't let users delete information.</span></span> <span data-ttu-id="9a5bc-128">したがって、ユーザーに情報を保存するかどうかを確認するよう促すことにより、後で削除できない保存される情報の量を限定できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-128">Therefore, by prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="9a5bc-129">**保存の検証を有効にします**チェック ボックスがオフの場合、場合によってはユーザーの準備ができる前に、レコードは常にすぐに保存されます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-129">If the **Enable save validation** check box is cleared, records are always saved immediately, possibly before the user is ready.</span></span> <span data-ttu-id="9a5bc-130">パフォーマンス管理を使用している場合は、**報酬**タブでも、パフォーマンスを評価するときに報酬プランに割り当てられているモデルの代わりに使用する評価モデルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-130">If you're using performance management, the **Compensation** tab also lets you select a rating model to use instead of the model that is assigned to compensation plans when performance is rated.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="9a5bc-131">以前にリリースされた機能</span><span class="sxs-lookup"><span data-stu-id="9a5bc-131">Previously released functionality</span></span>
<span data-ttu-id="9a5bc-132">**番号順序**タブの設定により、申請、休暇登録、報酬プロセス結果、ケース番号、コース、およびコースの議題などの人事管理の品目に ID を自動的に割り当てるのに使用される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-132">The settings on the **Number sequence** tab determine the sequences that are used to automatically assign IDs to items in Human resources, such as applications, absence registrations, compensation process results, case numbers, courses, and course agendas.</span></span> <span data-ttu-id="9a5bc-133">番号順序およびコードを管理するには、[**番号順序**] リスト ページを使用します。([**組織管理**] &gt; [**番号順序**] &gt; [**番号順序**] の順にクリックします)。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-133">To maintain number sequence references and codes, use the **Number sequences** list page (click **Organization administration** &gt; **Number sequences** &gt; **Number sequences**).</span></span>

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="9a5bc-134">Dynamics 365 for Talent を使用している場合</span><span class="sxs-lookup"><span data-stu-id="9a5bc-134">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="9a5bc-135">**番号順序**タブの設定により、申請、休暇登録、報酬プロセス結果、ケース番号、コース、およびコースの議題などの人事管理の品目に ID を自動的に割り当てるのに使用される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-135">The settings on the **Number sequence** tab determine the sequences that are used to automatically assign IDs to items in Human resources, such as applications, absence registrations, compensation process results, case numbers, courses, and course agendas.</span></span> <span data-ttu-id="9a5bc-136">番号順序およびコードを管理するには、[**番号順序**] リスト ページを使用します ([**システム管理**] &gt; [**リンク タブ**] &gt; [**番号順序**] &gt; [**番号順序**] の順にクリックします)。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-136">To maintain number sequence references and codes, use the **Number sequences** list page (click **System administration** &gt; **Links tab** &gt; **Number sequences** &gt; **Number sequences**).</span></span> 

<span data-ttu-id="9a5bc-137">**FMLA** タブの設定で、FMLA 給付金を受給できるために従業員が働く必要がある時間、適格性に必要な雇用期間、および雇用期間の決定に使用される雇用開始日を定義します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-137">The settings on the **FMLA** tab define how many hours an employee must work in order to be eligible for FMLA benefits, the length of employment that is required for eligibility, and the employment start date that is used to determine the length of employment.</span></span> <span data-ttu-id="9a5bc-138">設定は、従業員に権利がある FMLA 時間数、および従業員が使用した FMLA 時間の計算に使用される FMLA 休暇カレンダーも定義します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-138">The settings also define the number of FMLA hours that employees are entitled to and the FMLA leave calendar that is used to calculate how many FMLA hours employees have used.</span></span> <span data-ttu-id="9a5bc-139">**FMLA** タブは、米国の会社にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-139">The **FMLA** tab is available only to companies in the United States.</span></span> 

<span data-ttu-id="9a5bc-140">**注記:** 作業時間数は 1,250 を超えることはできず、雇用期間は 12 か月を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-140">**Note:** The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="9a5bc-141">これらの最大値は米国の連邦法に従います。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-141">These maximum values are in accordance with federal law in the United States.</span></span> <span data-ttu-id="9a5bc-142">最後に、**従業員セルフサービス**タブの設定で、マネージャが自分の従業員に代わって入力できる情報を決定します。</span><span class="sxs-lookup"><span data-stu-id="9a5bc-142">Finally, the settings on the **Employee self-service** tab determine the information that a manager can enter on behalf of his or her employees.</span></span>

<a name="see-also"></a><span data-ttu-id="9a5bc-143">参照</span><span class="sxs-lookup"><span data-stu-id="9a5bc-143">See also</span></span>
--------

[<span data-ttu-id="9a5bc-144">法人間の HR パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="9a5bc-144">Set up HR parameters across legal entities</span></span>](set-up-hr-parameters-across-legal-entities.md)




