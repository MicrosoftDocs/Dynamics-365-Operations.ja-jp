---
title: Talent での個人データ要求に対応
description: このトピックでは、データ コントローラとして Dynamics 365 for Talent for Talent をデータ プロセッサとして使用して、欧州連合のGDPR (General Data Protection Regulation) に基づくデータ要求に対応する方法について説明します。
author: shielasogge
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rschloma
ms.search.scope: Operations
ms.custom: 10031
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 827baf656c34b0bdb35ba32d9dca7421df1c23b6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555522"
---
# <a name="respond-to-requests-for-personal-data-in-talent"></a><span data-ttu-id="39832-103">Talent での個人データ要求に対応</span><span class="sxs-lookup"><span data-stu-id="39832-103">Respond to requests for personal data in Talent</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39832-104">このトピックは、Microsoft Dynamics 365 for Talent を使用する企業と、パートナーおよび独立系ソフトウェア ベンダー (ISV) がデータ主体の権利 (DSR) 要求に適合しているとき、それらの両方の企業に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="39832-104">This topic can help both businesses that use Microsoft Dynamics 365 for Talent, and also partners and independent software vendors (ISVs), when they comply with data subject rights (DSR) requests.</span></span> <span data-ttu-id="39832-105">欧州連合の一般データ保護規則 (GDPR) および Microsoft が提供する関連するリソースの詳細については、[Microsoft Dynamics 365 for Finance and Operations の GDPR に関するガイド](./gdpr-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39832-105">For more information about the European Union's General Data Protection Regulation (GDPR) and the related resources that Microsoft provides, see [Guide to the GDPR for Microsoft Dynamics 365 for Finance and Operations](./gdpr-guide.md).</span></span>

<span data-ttu-id="39832-106">Talent で、Microsoft はプロセッサとして動作します。</span><span class="sxs-lookup"><span data-stu-id="39832-106">For Talent, Microsoft acts as a processor.</span></span> <span data-ttu-id="39832-107">データ プロセッサとして、 Talent はデータ コントローラとしての GDPR 責務に適応させるプロセスと機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="39832-107">As a data processor, Talent provides processes and features that let you comply with your GDPR obligations as a data controller.</span></span>

## <a name="rights"></a><span data-ttu-id="39832-108">権限</span><span class="sxs-lookup"><span data-stu-id="39832-108">Rights</span></span>

<span data-ttu-id="39832-109">データ主体は GDPR の下で次の権限を持ち、データ コントローラーは DSR 要求に応じて各権限の下にリストされている行動のいずれかをとることができる。</span><span class="sxs-lookup"><span data-stu-id="39832-109">Data subjects have the following rights under the GDPR, and a data controller might take any of the actions that are listed under each right in response to a DSR request.</span></span> 

### <a name="right-to-view"></a><span data-ttu-id="39832-110">表示するには右</span><span class="sxs-lookup"><span data-stu-id="39832-110">Right to view</span></span>

+ <span data-ttu-id="39832-111">担当者検索レポートを使用して、DSR 要求の対象となる個人データを検索および収集します。</span><span class="sxs-lookup"><span data-stu-id="39832-111">Use the Person search report to find and collect personal data that is subject to a DSR request.</span></span> <span data-ttu-id="39832-112">このレポートの使用の詳細については、[個人検索レポート](gdpr-person-search-report.md) トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="39832-112">For information about using this report, see the [Person search report](gdpr-person-search-report.md) topic.</span></span>  
+ <span data-ttu-id="39832-113">高度な検索とフィルターを使用して、特定の個人データを検索し、Microsoft Office のエクスポート機能を使用してそのデータをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="39832-113">Use advanced search and filters to find specific personal data and export that data by using the Microsoft Office Export functionality.</span></span>
+ <span data-ttu-id="39832-114">既存のエンティティを追加して、担当者検索レポートを拡張します。</span><span class="sxs-lookup"><span data-stu-id="39832-114">Extend the Person search report by adding an existing entity.</span></span> <span data-ttu-id="39832-115">レポートを拡張するのに役立つ情報の詳細については、[独自のデータで個人検索レポートを拡張](gdpr-extend-person-search-report.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39832-115">For information that can help you extend the report, see [Extend the Person search report with your own data](gdpr-extend-person-search-report.md).</span></span>

### <a name="right-to-modify"></a><span data-ttu-id="39832-116">修正するには右\*</span><span class="sxs-lookup"><span data-stu-id="39832-116">Right to modify\*</span></span>

+ <span data-ttu-id="39832-117">高度な検索とフィルターを使用して修正すべきデータを見つけ、Talent で直接データを修正します。</span><span class="sxs-lookup"><span data-stu-id="39832-117">Use advanced search and filters to find the data that should be corrected, and correct the data directly in Talent.</span></span>

<span data-ttu-id="39832-118">\* 個人データと見なされるデータの一部は、製品または機能で直接変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="39832-118">\* You might find that some data that qualifies as personal data can't be modified directly in the product or feature.</span></span> <span data-ttu-id="39832-119">このデータは通常、財務法 (税法など)、詐欺防止 (セキュリティ監査証跡)、または業界認定への準拠のために「現状のまま」保たれる金融取引やその他の業務データの一部です 。</span><span class="sxs-lookup"><span data-stu-id="39832-119">Typically, this data is part of a financial transaction or other business data that is kept "as is" for compliance with financial laws (for example, tax laws), prevention of fraud (such as security audit trail), or compliance with industry certifications.</span></span> <span data-ttu-id="39832-120">コントローラーとして、不正確または未完了の個人データを修正する責任があります。</span><span class="sxs-lookup"><span data-stu-id="39832-120">As the controller, it's your responsibility to correct inaccurate or incomplete personal data.</span></span>

### <a name="right-to-be-forgotten"></a><span data-ttu-id="39832-121">消去するには右\*</span><span class="sxs-lookup"><span data-stu-id="39832-121">Right to be forgotten\*</span></span>

+ <span data-ttu-id="39832-122">製品が直接アクションを有効にする場所では、個人データを削除または消去することができます。</span><span class="sxs-lookup"><span data-stu-id="39832-122">You can delete or erase personal data where the product enables that action directly.</span></span> <span data-ttu-id="39832-123">コントローラーとして、データ主体の要求が消去された個人データが、支払証明または税の証明などのデータ保持に関する組織のその他のコンプライアンス責務と競合しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="39832-123">As the controller, you should ensure any personal data that a data subject requests be erased does not conflict with other compliance obligations your organization may have around data retention, for example proof of payment or proof of tax.</span></span>

<span data-ttu-id="39832-124">\* 個人データと見なされるデータの一部は、製品または機能で直接変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="39832-124">\* You might find that some data that qualifies as personal data can't be modified directly in the product or feature.</span></span> <span data-ttu-id="39832-125">このデータは通常、財務法 (税法など)、詐欺防止 (セキュリティ監査証跡)、または業界認定への準拠のために「現状のまま」保たれる金融取引やその他の業務データの一部です 。</span><span class="sxs-lookup"><span data-stu-id="39832-125">Typically, this data is part of a financial transaction or other business data that is kept "as is" for compliance with financial laws (for example, tax laws), prevention of fraud (such as security audit trail), or compliance with industry certifications.</span></span> <span data-ttu-id="39832-126">コントローラーとして、不正確または未完了の個人データを修正する責任があります。</span><span class="sxs-lookup"><span data-stu-id="39832-126">As the controller, it's your responsibility to correct inaccurate or incomplete personal data.</span></span>

### <a name="right-to-port"></a><span data-ttu-id="39832-127">移植するには右</span><span class="sxs-lookup"><span data-stu-id="39832-127">Right to port</span></span>
<span data-ttu-id="39832-128">次のオプションは、データ権利要求に応じて個人データを転送するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="39832-128">The following options are available to help you port personal data in response to a data rights request.</span></span> 

+ <span data-ttu-id="39832-129">Microsoft Office アドインを使用して、個人データをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="39832-129">Use the Microsoft Office Add-in to export personal data.</span></span>
+ <span data-ttu-id="39832-130">個人データのエクスポートを可能にするカスタム レポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="39832-130">Author a custom report that enables the export of personal data.</span></span>
+ <span data-ttu-id="39832-131">人物検索レポートを使用または拡張して、データ対象者の個人データのコピー要求に役立つ情報を収集します。</span><span class="sxs-lookup"><span data-stu-id="39832-131">Use or extend the Person search report to gather information in support of a request for a copy of the data subject's personal data.</span></span>

### <a name="right-to-restrict-processing"></a><span data-ttu-id="39832-132">処理を制限するには右</span><span class="sxs-lookup"><span data-stu-id="39832-132">Right to restrict processing</span></span>

+ <span data-ttu-id="39832-133">たとえば、コースから従業員を削除します。</span><span class="sxs-lookup"><span data-stu-id="39832-133">Remove the employee from, for example, a course.</span></span>
+ <span data-ttu-id="39832-134">組織の法的なカウンセリングからのガイダンスに従い、その他の法律または産業委任に準拠するための会社により、必要なデータの処理を制限する権限を会社が拒否する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="39832-134">Following guidance from an organization's legal counsel, the company might refuse the right to restrict processing where data is needed by the company for compliance with other legal or industry mandates.</span></span>

## <a name="additional-notes-that-apply-to-requests-for-personal-data"></a><span data-ttu-id="39832-135">個人データの要求に適用される追加のメモ</span><span class="sxs-lookup"><span data-stu-id="39832-135">Additional notes that apply to requests for personal data</span></span>

+ <span data-ttu-id="39832-136">Microsoft Power BI で見つかる個人データは、Talent で入力される情報から生成され、レポート目的でそのアプリケーションに転送されます。</span><span class="sxs-lookup"><span data-stu-id="39832-136">Personal data that is found in Microsoft Power BI is generated from the information that is entered in Talent and then transferred to that application for reporting purposes.</span></span> <span data-ttu-id="39832-137">Talent の情報から、レポート、Excel にエクスポートおよび個人検索レポートなどのツールを使用して個人データの要求を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="39832-137">Any request for personal data should be fulfilled from the information in Talent, by using tools such as reports, Export to Excel, and the Person search report.</span></span> <span data-ttu-id="39832-138">DSR 要求を満たすために Power BI から追加の報告を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="39832-138">You should not need to do additional reporting from Power BI to fulfill a DSR request.</span></span> 
+ <span data-ttu-id="39832-139">Talent は、レコードに関連付けられたドキュメントをエクスポートしません。</span><span class="sxs-lookup"><span data-stu-id="39832-139">Talent doesn't export documents that are attached to records.</span></span> <span data-ttu-id="39832-140">これらの添付ファイルは、手動でダウンロードし、DSR を作成した個人と共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39832-140">These attachments must be manually downloaded and shared with the individual who has made the DSR.</span></span>
+ <span data-ttu-id="39832-141">トランザクション データがマスター レコードに関連付けられている場合、レコードは削除できません。</span><span class="sxs-lookup"><span data-stu-id="39832-141">If transactional data is associated with a master record, that record can't be deleted.</span></span> 
+ <span data-ttu-id="39832-142">同様に、転記済または完了済みのトランザクションは削除できません。</span><span class="sxs-lookup"><span data-stu-id="39832-142">Similarly, transactions that have been posted or completed can't be deleted.</span></span>

### <a name="reasons-why-certain-personal-data-may-not-be-modified-or-deleted-in-talent"></a><span data-ttu-id="39832-143">Talent で特定の個人データを変更または削除できない理由</span><span class="sxs-lookup"><span data-stu-id="39832-143">Reasons why certain personal data may not be modified or deleted in Talent</span></span>

<span data-ttu-id="39832-144">次のテーブルは、特定のシナリオで個人データの変更または削除が制限される理由を示しています。</span><span class="sxs-lookup"><span data-stu-id="39832-144">The following table lists several reasons why personal data modification or deletion is restricted in certain scenarios.</span></span>

| <span data-ttu-id="39832-145">理由</span><span class="sxs-lookup"><span data-stu-id="39832-145">Reason</span></span> | <span data-ttu-id="39832-146">コメント</span><span class="sxs-lookup"><span data-stu-id="39832-146">Comment</span></span> |
|--------|---------|
| <span data-ttu-id="39832-147">財務、税金、一般会計原則 (GAAP)</span><span class="sxs-lookup"><span data-stu-id="39832-147">Financial, tax, generally accepted accounting principles (GAAP)</span></span> | <span data-ttu-id="39832-148">関係者を削除することはできませんが、関係者の名前は更新できます。</span><span class="sxs-lookup"><span data-stu-id="39832-148">A party can't be deleted, but the party's name can be updated.</span></span> |
| <span data-ttu-id="39832-149">財務、税、GAAP</span><span class="sxs-lookup"><span data-stu-id="39832-149">Financial, tax, GAAP</span></span> | <span data-ttu-id="39832-150">現在の作業者のデータは削除できませんが、作業者の名前を更新することはできます。</span><span class="sxs-lookup"><span data-stu-id="39832-150">A current worker's data can't be deleted, but the worker's name can be updated.</span></span> | 
| <span data-ttu-id="39832-151">GAAP</span><span class="sxs-lookup"><span data-stu-id="39832-151">GAAP</span></span> | <span data-ttu-id="39832-152">転記済または完了済みトランザクションは変更できません。</span><span class="sxs-lookup"><span data-stu-id="39832-152">Posted or completed transactions can't be modified.</span></span> |

## <a name="additional-information"></a><span data-ttu-id="39832-153">追加情報</span><span class="sxs-lookup"><span data-stu-id="39832-153">Additional information</span></span>

<span data-ttu-id="39832-154">退職済作業者のみ Talent から削除できます。</span><span class="sxs-lookup"><span data-stu-id="39832-154">Only terminated workers can be deleted from Talent.</span></span> <span data-ttu-id="39832-155">退職済従業者を削除するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="39832-155">Follow these steps to delete terminated workers.</span></span>

+ <span data-ttu-id="39832-156">作業者職位を削除します。</span><span class="sxs-lookup"><span data-stu-id="39832-156">Delete position assignments.</span></span> 

    <span data-ttu-id="39832-157">職位の割り当てを削除するには、**作業者** ページで **職位の割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39832-157">To delete a position assignment, select **Position assignments** on the **Worker** page.</span></span> <span data-ttu-id="39832-158">**次の日の時点** および **すべてのレコードを表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39832-158">Select **As of date** and select **Display all records**.</span></span> <span data-ttu-id="39832-159">位置番号をドリルインするには、**タイムラインの変更** &gt; **変更の管理** &gt; **職位作業者割り当て**を選択し、削除している作業員に割り当てられている位置の割り当てレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="39832-159">Drill into the position number, select **Changes timeline** &gt; **Manage changes** &gt; **Position worker assignments**, and remove the position assignment record that is associated with the worker that you're deleting.</span></span>

+ <span data-ttu-id="39832-160">固定報酬を削除します。</span><span class="sxs-lookup"><span data-stu-id="39832-160">Delete fixed compensation.</span></span>

    <span data-ttu-id="39832-161">固定報酬を削除するには、**作業者** ページで **雇用履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39832-161">To delete fixed compensation, select **Employment history** on the **Worker** page.</span></span> <span data-ttu-id="39832-162">**雇用履歴** &gt; **雇用** &gt; **固定報酬** を選択し、作業者の固定報酬プランを削除します。</span><span class="sxs-lookup"><span data-stu-id="39832-162">Select **Employment history** &gt; **Employment** &gt; **Fixed compensation**, and delete the fixed compensation plans for the worker.</span></span>

+ <span data-ttu-id="39832-163">変動報酬登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="39832-163">Delete variable compensation enrollments.</span></span>

    <span data-ttu-id="39832-164">変動報酬を削除するには、**作業者** ページで **雇用履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39832-164">To delete variable compensation, select **Employment history** on the **Worker** page.</span></span> <span data-ttu-id="39832-165">**雇用履歴** &gt; **雇用** &gt; **変動報酬プラン登録** を選択し、作業者の変動報酬プランの登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="39832-165">Select **Employment history** &gt; **Employment** &gt; **Variable compensation plan enrollment** and delete the variable compensation plan enrollments for the worker.</span></span>

+ <span data-ttu-id="39832-166">関連付けられている任意のチェックリストを削除します。</span><span class="sxs-lookup"><span data-stu-id="39832-166">Delete any associated checklists.</span></span>

    <span data-ttu-id="39832-167">チェックリストを削除するには、**作業者** ページで **チェックリスト** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="39832-167">To delete the checklists, select the **Checklists** option on the **Worker** page.</span></span>

<span data-ttu-id="39832-168">補償は契約者に割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="39832-168">Compensation isn't assigned to contractors.</span></span> <span data-ttu-id="39832-169">したがって、これらのステップは、前のプロセスでスキップすることができます。</span><span class="sxs-lookup"><span data-stu-id="39832-169">Therefore, those steps can be skipped in the preceding process.</span></span>

<span data-ttu-id="39832-170">管理者は、Microsoft Dynamics 365 for Talent の個人データを検索し、エクスポートできます。Attract および Microsoft Dynamics 365 for Talent: <https://attract.talent.dynamics.com/personreport> 経由でのオンボーディングです。</span><span class="sxs-lookup"><span data-stu-id="39832-170">An admin can search and export personal data in Microsoft Dynamics 365 for Talent: Attract and Microsoft Dynamics 365 for Talent: Onboarding via <https://attract.talent.dynamics.com/personreport>.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39832-171">追加リソース</span><span class="sxs-lookup"><span data-stu-id="39832-171">Additional resources</span></span>
<span data-ttu-id="39832-172">GDPR の詳細については、[欧州連合の Web サイト](https://europa.eu/) および [Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39832-172">You can learn more about the GDPR on the [European Union's website](https://europa.eu/) and on the [Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx).</span></span>



### <a name="disclaimer"></a><span data-ttu-id="39832-173">免責事項</span><span class="sxs-lookup"><span data-stu-id="39832-173">Disclaimer</span></span>
<span data-ttu-id="39832-174">(c)2018 Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="39832-174">(c)2018 Microsoft Corporation.</span></span> <span data-ttu-id="39832-175">All rights reserved.</span><span class="sxs-lookup"><span data-stu-id="39832-175">All rights reserved.</span></span> <span data-ttu-id="39832-176">このドキュメントは、"現状のまま" 提供されます。</span><span class="sxs-lookup"><span data-stu-id="39832-176">This document is provided "as-is."</span></span> <span data-ttu-id="39832-177">URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="39832-177">Information and views expressed in this document, including URL and other Internet Web site references, may change without notice.</span></span> <span data-ttu-id="39832-178">このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。</span><span class="sxs-lookup"><span data-stu-id="39832-178">You bear the risk of using it.</span></span> <span data-ttu-id="39832-179">このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。</span><span class="sxs-lookup"><span data-stu-id="39832-179">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="39832-180">内部での参照を目的とする場合、このドキュメントをコピーして使用できます。</span><span class="sxs-lookup"><span data-stu-id="39832-180">You may copy and use this document for your internal, reference purposes.</span></span>
