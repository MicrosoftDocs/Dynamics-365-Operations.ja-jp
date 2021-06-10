---
title: 申請者追跡システム統合APIの概要
description: このトピックでは、Dynamics 365 Human Resources 申請者追跡システム (ATS) 統合 API について説明します。
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c043ac9c19a810d1718f0d4907cd5e9d651d778f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055295"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="e2b55-103">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="e2b55-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e2b55-104">このトピックでは、Dynamics 365 Human Resources 申請者追跡システム (ATS) 統合 API について説明します。</span><span class="sxs-lookup"><span data-stu-id="e2b55-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="e2b55-105">API の目的は、ATS 間およびパートナー間の合理化された Dynamics 365 Human Resources 統合を実現することです。</span><span class="sxs-lookup"><span data-stu-id="e2b55-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS 統合のフロー](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="e2b55-107">統合されたエクスペリエンスは、採用マネージャーが採用要求を作成する際に Human Resources で開始されます。</span><span class="sxs-lookup"><span data-stu-id="e2b55-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="e2b55-108">要求が有効化されると、ATS によって要求の詳細が引き出され、採用プロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e2b55-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="e2b55-109">その後、採用パイプラインに従ってポジションの候補者を選択・採用します。</span><span class="sxs-lookup"><span data-stu-id="e2b55-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="e2b55-110">ATSは最後に、選択した候補者のレコードを Human Resources に送信することで、ラウンド トリップの統合を完了します。</span><span class="sxs-lookup"><span data-stu-id="e2b55-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="e2b55-111">その後、その候補者レコードに対して、多くの修正の検証およびワークフローを実行して、従業員レコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e2b55-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="e2b55-112">Human Resources では、統合を有効にするあたり、次のコンポーネントが追加されています。</span><span class="sxs-lookup"><span data-stu-id="e2b55-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="e2b55-113">採用の要求を作成する機能。</span><span class="sxs-lookup"><span data-stu-id="e2b55-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="e2b55-114">拡張された候補者プロファイルと関連するワークフロー。</span><span class="sxs-lookup"><span data-stu-id="e2b55-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="e2b55-115">アプリケーションを統合する新機能をオープンにした統合 API。</span><span class="sxs-lookup"><span data-stu-id="e2b55-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="e2b55-116">採用要求と候補者の機能の設定と使用の詳細については、[採用ジョブ候補者](hr-personnel-recruit.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2b55-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="e2b55-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="e2b55-117">Microsoft Dataverse</span></span>

<span data-ttu-id="e2b55-118">この API は Microsoft Dataverse (旧 Common Data Service) に構築されています。</span><span class="sxs-lookup"><span data-stu-id="e2b55-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="e2b55-119">この API との RESTful の対話は、ODataを使用する Microsoft Dataverse Web API を介して行われます。</span><span class="sxs-lookup"><span data-stu-id="e2b55-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="e2b55-120">この API は Dataverse Web API のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="e2b55-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="e2b55-121">Dataverse Web APIでは、認証、SLA、バッチ、同時実行制御、エラー処理などの特性が定義されます。</span><span class="sxs-lookup"><span data-stu-id="e2b55-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="e2b55-122">Microsoft Dataverse Web API の詳細については、次を参照してください :</span><span class="sxs-lookup"><span data-stu-id="e2b55-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="e2b55-123">Microsoft Dataverse とは</span><span class="sxs-lookup"><span data-stu-id="e2b55-123">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="e2b55-124">Microsoft Dataverse Web API を使用する</span><span class="sxs-lookup"><span data-stu-id="e2b55-124">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="e2b55-125">Microsoft Dataverse 開発者ガイド</span><span class="sxs-lookup"><span data-stu-id="e2b55-125">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="e2b55-126">上記のドキュメントでは、[認証の管理](/powerapps/developer/data-platform/webapi/authenticate-web-api)、[操作の実行](/powerapps/developer/data-platform/webapi/perform-operations-web-api)、[API での Postman の使用](/powerapps/developer/data-platform/webapi/use-postman-web-api)、APIによる[変更追跡トークンまたはデルタ トークンの使用](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)などの、Dataverse Web API の使用に関する詳細なガイドと開発者ガイドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2b55-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="e2b55-127">オプション セット</span><span class="sxs-lookup"><span data-stu-id="e2b55-127">Option sets</span></span>

<span data-ttu-id="e2b55-128">このドキュメントで説明する ATS 統合 API のデータ モデルには、エンティティ プロパティに関連付けられた列挙値を提供するオプション セットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2b55-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="e2b55-129">Dataverse Web API でのオプション セットの操作の詳細については、[Web APIを使用したオプション セットの作成と更新](/powerapps/developer/data-platform/webapi/create-update-optionsets)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2b55-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="e2b55-130">オプション セットは各 Dataverse 環境ごとに定義されます。</span><span class="sxs-lookup"><span data-stu-id="e2b55-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="e2b55-131">Dataverse における Human Resources の仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="e2b55-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="e2b55-132">ATS 統合 API のエンドポイントは、Microsoft Dataverse の仮想テーブルプラットフォーム機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2b55-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="e2b55-133">既定では、仮想テーブルと関連する API エンドポイントは人事環境には配置されていないため、組織は環境で公開される OData エンドポイントを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="e2b55-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="e2b55-134">このAPIを使用するには、その環境に対して Human Resources エンティティの仮想テーブルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2b55-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="e2b55-135">API 用の仮想テーブルの生成の詳細については、[Dataverse 仮想テーブルの構成](./hr-admin-integration-common-data-service-virtual-entities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2b55-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="e2b55-136">データ モデル</span><span class="sxs-lookup"><span data-stu-id="e2b55-136">Data model</span></span>

<span data-ttu-id="e2b55-137">データ モデルは、次の2つの主要なエンティティの中央に位置しています。</span><span class="sxs-lookup"><span data-stu-id="e2b55-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="e2b55-138">**RecruitingRequest** は、ATS に対して、ひとつまたは複数のオープンなポジションの募集を依頼していることを表しています。クエリの例については、[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2b55-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="e2b55-139">**CandidateToHire** は、ポジションのオファーを受けた候補者の詳細を表します。</span><span class="sxs-lookup"><span data-stu-id="e2b55-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="e2b55-140">**人物** は、採用候補者を表します。</span><span class="sxs-lookup"><span data-stu-id="e2b55-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="e2b55-141">候補者、労働者、社員、契約社員など、会社の中で複数の役割を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="e2b55-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="e2b55-142">クエリの例については、[採用する候補者のクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2b55-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="e2b55-143">次の図では、API 内の関係性を示しています。</span><span class="sxs-lookup"><span data-stu-id="e2b55-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="e2b55-144">Human Resources 内の既存のエンティティには、その他のエンティティに対する外部キーがあり、それについてはここでは示されていません。</span><span class="sxs-lookup"><span data-stu-id="e2b55-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="e2b55-145">このドキュメントでは、統合の採用のシナリオに固有のエンティティに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2b55-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="e2b55-146">しかし、Dynamics 365 Human Resources 向け Dataverse Web API には他にも多くのエンティティが存在しており、これらのエンティティも統合に関連している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e2b55-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="e2b55-147">たとえば、ここで定義していない作業者、ジョブ、職位、または他のエンティティの詳細が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="e2b55-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="e2b55-148">これらのエンティティの多くは、外部キーとの関係性やナビゲーション プロパティで参照されます。</span><span class="sxs-lookup"><span data-stu-id="e2b55-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS 統合の API データ モデル](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="e2b55-150">採用要求と関連するエンティティとオプション セット</span><span class="sxs-lookup"><span data-stu-id="e2b55-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="e2b55-151">クエリの例 :</span><span class="sxs-lookup"><span data-stu-id="e2b55-151">Example query:</span></span> 

- [<span data-ttu-id="e2b55-152">採用要求のクエリの例</span><span class="sxs-lookup"><span data-stu-id="e2b55-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="e2b55-153">エンティティ:</span><span class="sxs-lookup"><span data-stu-id="e2b55-153">Entities:</span></span>

- [<span data-ttu-id="e2b55-154">採用要求</span><span class="sxs-lookup"><span data-stu-id="e2b55-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="e2b55-155">採用要求職位</span><span class="sxs-lookup"><span data-stu-id="e2b55-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="e2b55-156">採用で要求するスキル</span><span class="sxs-lookup"><span data-stu-id="e2b55-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="e2b55-157">採用で要求する教育</span><span class="sxs-lookup"><span data-stu-id="e2b55-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="e2b55-158">採用要求場所</span><span class="sxs-lookup"><span data-stu-id="e2b55-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="e2b55-159">オプション セット :</span><span class="sxs-lookup"><span data-stu-id="e2b55-159">Option sets:</span></span>

- [<span data-ttu-id="e2b55-160">ジョブ除外する状態</span><span class="sxs-lookup"><span data-stu-id="e2b55-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="e2b55-161">採用で要求するポジションの状態</span><span class="sxs-lookup"><span data-stu-id="e2b55-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="e2b55-162">採用で要求する状態</span><span class="sxs-lookup"><span data-stu-id="e2b55-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="e2b55-163">規制のジョブ カテゴリ</span><span class="sxs-lookup"><span data-stu-id="e2b55-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="e2b55-164">採用候補者と関連するエンティティおよびオプション セット</span><span class="sxs-lookup"><span data-stu-id="e2b55-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="e2b55-165">クエリの例 :</span><span class="sxs-lookup"><span data-stu-id="e2b55-165">Example query:</span></span>

- [<span data-ttu-id="e2b55-166">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="e2b55-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="e2b55-167">エンティティ:</span><span class="sxs-lookup"><span data-stu-id="e2b55-167">Entities:</span></span>

- [<span data-ttu-id="e2b55-168">採用候補者</span><span class="sxs-lookup"><span data-stu-id="e2b55-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="e2b55-169">名前</span><span class="sxs-lookup"><span data-stu-id="e2b55-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="e2b55-170">人物の教育</span><span class="sxs-lookup"><span data-stu-id="e2b55-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="e2b55-171">人物の職務経験</span><span class="sxs-lookup"><span data-stu-id="e2b55-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="e2b55-172">人物の住所</span><span class="sxs-lookup"><span data-stu-id="e2b55-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="e2b55-173">関係者の連絡先</span><span class="sxs-lookup"><span data-stu-id="e2b55-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="e2b55-174">人物のスキル</span><span class="sxs-lookup"><span data-stu-id="e2b55-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="e2b55-175">評価レベル</span><span class="sxs-lookup"><span data-stu-id="e2b55-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="e2b55-176">人物の証明書</span><span class="sxs-lookup"><span data-stu-id="e2b55-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="e2b55-177">証明書タイプ</span><span class="sxs-lookup"><span data-stu-id="e2b55-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="e2b55-178">個人の審査</span><span class="sxs-lookup"><span data-stu-id="e2b55-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="e2b55-179">審査タイプ</span><span class="sxs-lookup"><span data-stu-id="e2b55-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="e2b55-180">人物の ID 番号</span><span class="sxs-lookup"><span data-stu-id="e2b55-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="e2b55-181">オプション セット :</span><span class="sxs-lookup"><span data-stu-id="e2b55-181">Option sets:</span></span>

- [<span data-ttu-id="e2b55-182">申請者の統合結果</span><span class="sxs-lookup"><span data-stu-id="e2b55-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- <span data-ttu-id="e2b55-183">[空白の [はい] と [いいえ]](hr-admin-integration-ats-api-blank-yes-no.md)</span><span class="sxs-lookup"><span data-stu-id="e2b55-183">[Blank Yes No](hr-admin-integration-ats-api-blank-yes-no.md)</span></span>
- [<span data-ttu-id="e2b55-184">完了の状態</span><span class="sxs-lookup"><span data-stu-id="e2b55-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="e2b55-185">連絡先タイプ</span><span class="sxs-lookup"><span data-stu-id="e2b55-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="e2b55-186">教育クレジット基準</span><span class="sxs-lookup"><span data-stu-id="e2b55-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="e2b55-187">種類</span><span class="sxs-lookup"><span data-stu-id="e2b55-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="e2b55-188">配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="e2b55-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="e2b55-189">月</span><span class="sxs-lookup"><span data-stu-id="e2b55-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="e2b55-190">いいえ はい</span><span class="sxs-lookup"><span data-stu-id="e2b55-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="e2b55-191">期間の単位</span><span class="sxs-lookup"><span data-stu-id="e2b55-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="e2b55-192">審査の頻度</span><span class="sxs-lookup"><span data-stu-id="e2b55-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="e2b55-193">審査頻度の生成方法</span><span class="sxs-lookup"><span data-stu-id="e2b55-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="e2b55-194">スキル レベル タイプ</span><span class="sxs-lookup"><span data-stu-id="e2b55-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="e2b55-195">参照</span><span class="sxs-lookup"><span data-stu-id="e2b55-195">See also</span></span>

[<span data-ttu-id="e2b55-196">職務候補者の採用</span><span class="sxs-lookup"><span data-stu-id="e2b55-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="e2b55-197">Microsoft Dataverse とは</span><span class="sxs-lookup"><span data-stu-id="e2b55-197">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="e2b55-198">Microsoft Dataverse Web API を使用する</span><span class="sxs-lookup"><span data-stu-id="e2b55-198">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="e2b55-199">Web API を使用したオプション セットの作成と更新</span><span class="sxs-lookup"><span data-stu-id="e2b55-199">Create and update option sets using the Web API</span></span>](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]