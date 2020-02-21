---
title: 一般データ保護規則の概要
description: このトピックでは、Finance and Operations でのユーザー ログの機能に関する情報を提供します。
author: ToddLefor
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 10031
ms.search.region: Global
ms.author: ToddLefor
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ac3b085b7fb8d552977206ea8d298bad04b6475
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3005529"
---
# <a name="general-data-protection-regulation-overview"></a><span data-ttu-id="b3600-103">一般データ保護規則の概要</span><span class="sxs-lookup"><span data-stu-id="b3600-103">General Data Protection Regulation overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview-of-the-gdpr"></a><span data-ttu-id="b3600-104">GDPR の概要</span><span class="sxs-lookup"><span data-stu-id="b3600-104">Overview of the GDPR</span></span>

<span data-ttu-id="b3600-105">欧州連合の一般データ保護規制 (GDPR) は、欧州連合 (EU) の市民および居住者のプライバシー権利、セキュリティ、およびコンプライアンスの新しいグローバル標準を設定します。</span><span class="sxs-lookup"><span data-stu-id="b3600-105">The European Union's General Data Protection Regulation (GDPR) sets a new global standard for privacy rights, security, and compliance for the citizens and residents of the European Union (EU).</span></span> <span data-ttu-id="b3600-106">GDPR は、EU 市民と居住者の個人データの処理および使用を制御します。</span><span class="sxs-lookup"><span data-stu-id="b3600-106">The GDPR governs the handling and use of personal data of EU citizens and residents.</span></span> <span data-ttu-id="b3600-107">GDPR の実施は 2018 年 5 月 25 日から開始され、非規制遵守に重大な影響があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-107">Enforcement of the GDPR begins May 25, 2018, and there are significant consequences for non-compliance.</span></span> <span data-ttu-id="b3600-108">規制の詳細については、[欧州連合サイト](https://europa.eu/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3600-108">For more information about the regulation, see the [European Union site](https://europa.eu/).</span></span>

> [!NOTE]
> <span data-ttu-id="b3600-109">このドキュメントのスコープおよび補充の詳細については、このトピックの最後にある [このコンテンツの範囲の説明](#clarification-of-the-scope-of-this-content) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3600-109">For information about the scope and coverage of this documentation, see [Clarification of the scope of this content](#clarification-of-the-scope-of-this-content) section at the end of this topic.</span></span>
>
> <span data-ttu-id="b3600-110">GDPR コンプライアンスの実行をサポートする製品の機能を使用する前に、すべての関連する修正プログラムを適用したことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b3600-110">Before utilizing any product features in support of your GDPR compliance efforts, please ensure that you have applied all of the related hotfixes.</span></span>

<span data-ttu-id="b3600-111">GDPR は、次のアクションを実行できるように EU 市民に特定のデータ主体権利 (DSR) を与えます。</span><span class="sxs-lookup"><span data-stu-id="b3600-111">The GDPR gives EU citizens specific data subject rights (DSRs) that let them perform the following actions:</span></span>

+ <span data-ttu-id="b3600-112">個人データの表示。</span><span class="sxs-lookup"><span data-stu-id="b3600-112">View their personal data.</span></span>
+ <span data-ttu-id="b3600-113">個人データのエラーを訂正する。</span><span class="sxs-lookup"><span data-stu-id="b3600-113">Correct errors in their personal data.</span></span>
+ <span data-ttu-id="b3600-114">個人データの削除。</span><span class="sxs-lookup"><span data-stu-id="b3600-114">Erase their personal data.</span></span>
+ <span data-ttu-id="b3600-115">個人データを処理するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="b3600-115">Object to processing of their personal data.</span></span>
+ <span data-ttu-id="b3600-116">個人データをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="b3600-116">Export their personal data.</span></span>

<span data-ttu-id="b3600-117">GDPR は、[規制](https://data.consilium.europa.eu/doc/document/ST-5419-2016-INIT/en/pdf)の第 4 項の次の方法で個人データを定義しています (組織は個人データを持っていない)。</span><span class="sxs-lookup"><span data-stu-id="b3600-117">The GDPR defines personal data in the following way in article 4 of [the regulation](https://data.consilium.europa.eu/doc/document/ST-5419-2016-INIT/en/pdf) (organizations do not have personal data):</span></span>

> <span data-ttu-id="b3600-118">(1) 「個人データ」とは、特定または識別可能な自然人 (「データ主体」) に関するすべての情報を意味します。識別可能な自然人とは、特に、名前、識別番号、位置データ、オンライン識別子のような識別子、または身体的、生理学的、遺伝的、精神的、経済的、文化的、社会的アイデンティティーなど、その自然人固有の 1 つ以上の要因を参照することによって、直接的または間接的に、識別できる人のことです。</span><span class="sxs-lookup"><span data-stu-id="b3600-118">(1) 'personal data' means any information relating to an identified or identifiable natural person ('data subject'); an identifiable natural person is one who can be identified, directly or indirectly, in particular by reference to an identifier such as a name, an identification number, location data, an online identifier or to one or more factors specific to the physical, physiological, genetic, mental, economic, cultural or social identity of that natural person;</span></span>

<span data-ttu-id="b3600-119">コンプライアンスの責任を決定するために、GDPR は次のロールを識別します。</span><span class="sxs-lookup"><span data-stu-id="b3600-119">To determine responsibilities for compliance, the GDPR identifies the following roles:</span></span>

+ <span data-ttu-id="b3600-120">**データ コントローラー** - コントローラーは個人データを管理し、その使用方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="b3600-120">**Data controller** – The controller controls personal data and determines how it's used.</span></span> <span data-ttu-id="b3600-121">コントローラーの責任には、個人データの収集、維持、指揮、保護、変更、削除が含まれますが、これらに限定されません。</span><span class="sxs-lookup"><span data-stu-id="b3600-121">The responsibilities of the controller include but are not limited to collecting, maintaining, directing actions, protecting, modifying and deleting personal data.</span></span> <span data-ttu-id="b3600-122">コントローラーは、ユーザーをシステムに追加し、システムへのアクセスを許可し、データサブジェクトからデータを収集するか、会社のためにこれらのタスクを完了する従業員を持っています。</span><span class="sxs-lookup"><span data-stu-id="b3600-122">The controller either adds users to the system, grants access to the system, and collects data from data subjects, or has employees who complete these tasks on the company's behalf.</span></span> <span data-ttu-id="b3600-123">GDPR 要求のプロセスを理解し、GDPR 要求を実行する負担は、コントローラーにあります。</span><span class="sxs-lookup"><span data-stu-id="b3600-123">The burden of understanding the process for GDPR requests and carrying out a GDPR request rests with the controller.</span></span>
+ <span data-ttu-id="b3600-124">**データ プロセッサ** - プロセッサは、データ コントローラーにサービスを提供し、データ コントローラーに代わってデータを処理します。</span><span class="sxs-lookup"><span data-stu-id="b3600-124">**Data processor** – The processor provides services to, and processes data on behalf of, the data controller.</span></span> <span data-ttu-id="b3600-125">プロセッサは、コントローラーに代わってアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="b3600-125">The processor performs actions on behalf of the controller.</span></span> <span data-ttu-id="b3600-126">プロセッサにより、コントローラーは GDPR に準拠できるようになりますが、データの所有権はなく DSR 要求に直接応答しません。</span><span class="sxs-lookup"><span data-stu-id="b3600-126">The processor makes it possible for the controller to be GDPR compliant, but has no ownership of the data and does not respond directly to DSR requests.</span></span>
+ <span data-ttu-id="b3600-127">**データ主体** - データ主体は、個人情報が使用されている自然人です。</span><span class="sxs-lookup"><span data-stu-id="b3600-127">**Data subject** – A data subject is a natural person whose personal information is being used.</span></span>
+ <span data-ttu-id="b3600-128">**C1** - C1 は Microsoft の直接顧客 (エンタープライズ クラウドの IT 管理者) です。</span><span class="sxs-lookup"><span data-stu-id="b3600-128">**C1** – C1 is a Microsoft direct customer (IT Admin in the Enterprise Cloud).</span></span>
+ <span data-ttu-id="b3600-129">**C2** - C2 は C1 の顧客です。</span><span class="sxs-lookup"><span data-stu-id="b3600-129">**C2** – C2 is C1's customer.</span></span>

<span data-ttu-id="b3600-130">Finance and Operations アプリでは、Microsoft はプロセッサとして動作します。</span><span class="sxs-lookup"><span data-stu-id="b3600-130">For Finance and Operations apps, Microsoft acts as a processor.</span></span> <span data-ttu-id="b3600-131">データ プロセッサとして、Finance and Operations はデータ コントローラーとしての GDPR 責務に適応するのに役立つプロセスと機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="b3600-131">As a data processor, Finance and Operations provides processes and features that help you comply with your GDPR obligations as a data controller.</span></span>

<span data-ttu-id="b3600-132">次の図は、顧客からアプリケーション データベースへのデータの流れ、およびお客様と Microsoft がそのプロセスで果たすロールを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3600-132">The following illustration shows the flow of data from your customer to the application database, and the roles that you and Microsoft play in that process.</span></span> <span data-ttu-id="b3600-133">それぞれのアプリケーションで、コントローラーはテナント管理者、Microsoft はプロセッサです。</span><span class="sxs-lookup"><span data-stu-id="b3600-133">For each application, the controller is the tenant administrator, and Microsoft is the processor.</span></span> <span data-ttu-id="b3600-134">このシナリオでは、データを保管、取得、並べ替えなどを行うことでデータを処理するプロセッサ (Microsoft) にデータが送信されます。</span><span class="sxs-lookup"><span data-stu-id="b3600-134">In this scenario, the data is sent to the processor (Microsoft), who then processes the data by storing it, retrieving it, sorting it, and so on.</span></span>

![顧客からのデータ フロー](../media/gdpr-customers-controller-processor.jpg)

<span data-ttu-id="b3600-136">データ主体が DSR の送信を選択すると、そのデータ主体はコントローラーに要求を出します。</span><span class="sxs-lookup"><span data-stu-id="b3600-136">When a data subject chooses to submit a DSR, the data subject makes the request to the controller.</span></span> <span data-ttu-id="b3600-137">データ主体は、ビジネスで収集したデータに対する Microsoft の権限を行使することはありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-137">Data subjects won't approach Microsoft to exercise their rights for data that your business has collected.</span></span> <span data-ttu-id="b3600-138">プロセッサとして、Microsoft は機能を提供することによって、またはアクションが可能であることを確認することによってコントローラを支援します。</span><span class="sxs-lookup"><span data-stu-id="b3600-138">As the processor, Microsoft assists the controller by providing features, or just by making sure that the actions are possible.</span></span> <span data-ttu-id="b3600-139">つまり、コントローラーは DSR 要求の受け入れて応答し、プロセッサはコンプライアンス要求を扱ったり有効化したりします。</span><span class="sxs-lookup"><span data-stu-id="b3600-139">In other words, the controller accepts and responds to a DSR request, and the processor assists with or enables the compliance request.</span></span> <span data-ttu-id="b3600-140">以下のテーブルは、関連するいくつかのロールと職責の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3600-140">The following table outlines some of the roles and responsibilities that are relevant.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="45%" />
<col width="25%" />
<col width="10%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3600-141">
<strong>役割</strong>
</span><span class="sxs-lookup"><span data-stu-id="b3600-141">
<strong>Role</strong>
</span></span></td>
<td><span data-ttu-id="b3600-142">
<strong>シナリオ</strong>
</span><span class="sxs-lookup"><span data-stu-id="b3600-142">
<strong>Scenarios</strong>
</span></span></td>
<td><span data-ttu-id="b3600-143">
<strong>実装</strong>
</span><span class="sxs-lookup"><span data-stu-id="b3600-143">
<strong>Implementation</strong>
</span></span></td>
<td><span data-ttu-id="b3600-144">
<strong>データ アクセスのレベル</strong>
</span><span class="sxs-lookup"><span data-stu-id="b3600-144">
<strong>Level of data access</strong>
</span></span></td>
</tr>
<tr class="even">
<td>
<p><span data-ttu-id="b3600-145"><strong>顧客 (2)</strong></span><span class="sxs-lookup"><span data-stu-id="b3600-145"><strong>Your customer (2)</strong></span></span></p>
</td>
<td>
<ul>
<li><span data-ttu-id="b3600-146">個人データの表示</span><span class="sxs-lookup"><span data-stu-id="b3600-146">View personal data</span></span> </li>
<li><span data-ttu-id="b3600-147">個人データの修正</span><span class="sxs-lookup"><span data-stu-id="b3600-147">Correct personal data</span></span></li>
<li><span data-ttu-id="b3600-148">個人データの消去</span><span class="sxs-lookup"><span data-stu-id="b3600-148">Erase personal data</span></span> </li>
<li><span data-ttu-id="b3600-149">処理するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="b3600-149">Object to processing</span></span></li>
<li><span data-ttu-id="b3600-150">個人データをエクスポート</span><span class="sxs-lookup"><span data-stu-id="b3600-150">Export personal data</span></span></li></ul>
</td>
<td>
<p><span data-ttu-id="b3600-151">顧客が DSR (プロセスまたはサービス) を実行するためのメカニズムを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-151">You must provide a mechanism for your customer to exercise a DSR (process or service).</span></span></p>
</td>
<td>
<p><span data-ttu-id="b3600-152">顧客には、自分たちのデータのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3600-152">Your customer sees only their personal data.</span></span></p>
</td>
</tr>
<tr class="odd">
<td>
<p><span data-ttu-id="b3600-153"><strong>従業員 - インフォメーション ワーカー</strong></span><span class="sxs-lookup"><span data-stu-id="b3600-153"><strong>Your employee – information worker</strong></span></span></p>
</td>
<td>
<ul>
<li><span data-ttu-id="b3600-154">個人データの表示</span><span class="sxs-lookup"><span data-stu-id="b3600-154">View personal data</span></span> </li>
<li><span data-ttu-id="b3600-155">個人データの修正</span><span class="sxs-lookup"><span data-stu-id="b3600-155">Correct personal data</span></span></li>
<li><span data-ttu-id="b3600-156">個人データの消去</span><span class="sxs-lookup"><span data-stu-id="b3600-156">Erase personal data</span></span> </li>
<li><span data-ttu-id="b3600-157">処理するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="b3600-157">Object to processing</span></span></li>
<li><span data-ttu-id="b3600-158">個人データをエクスポート</span><span class="sxs-lookup"><span data-stu-id="b3600-158">Export personal data</span></span></li></ul>
</td>
<td>
<p><span data-ttu-id="b3600-159">作業者が DSR (プロセスまたはサービス) を実行するためのメカニズムを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-159">You must provide a mechanism for your worker to exercise a DSR (process or service).</span></span> <span data-ttu-id="b3600-160">一部のアクティビティ情報は、Microsoft から入手できます</span><span class="sxs-lookup"><span data-stu-id="b3600-160">Some activity information may be obtained from Microsoft</span></span></p>
</td>
<td>
<p><span data-ttu-id="b3600-161">インフォメーション ワーカーには、自分たちのデータのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3600-161">Your information worker sees only their personal data.</span></span></p>
</td>
</tr>
<tr class="odd">
<td>
<p><span data-ttu-id="b3600-162"><strong>従業員 - GDPR 管理者</strong></span><span class="sxs-lookup"><span data-stu-id="b3600-162"><strong>Your employee – GDPR administrator</strong></span></span></p>
</td>
<td>
<ul>
<li><span data-ttu-id="b3600-163">ユーザー ID 要求の検証</span><span class="sxs-lookup"><span data-stu-id="b3600-163">Validates the user identity request</span></span>  </li>
<li><span data-ttu-id="b3600-164">システムでの個人データの検索</span><span class="sxs-lookup"><span data-stu-id="b3600-164">Locates the personal data across systems</span></span> </li>
<li><span data-ttu-id="b3600-165">ポリシーに基づいてデータを調整する</span><span class="sxs-lookup"><span data-stu-id="b3600-165">Curates the data based on your policy</span></span></li>
<li><span data-ttu-id="b3600-166">データ パッケージを作成するか、アクションを実行する</span><span class="sxs-lookup"><span data-stu-id="b3600-166">Creates a data package or executes an action</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="b3600-167">Finance and Operations を使用してデータを検索し、要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="b3600-167">Uses Finance and Operations to locate the data and fulfill the request.</span></span> </li>
<li><span data-ttu-id="b3600-168">カスタマイズを記述します。</span><span class="sxs-lookup"><span data-stu-id="b3600-168">Writes a customization.</span></span></li>
<li><span data-ttu-id="b3600-169">サード パーティに共有コントローラー DSR を求めます。</span><span class="sxs-lookup"><span data-stu-id="b3600-169">Reaches out to third parties for shared-controller DSRs.</span></span></li>
<li><span data-ttu-id="b3600-170">Microsoft にアクティビティ データを求めます。</span><span class="sxs-lookup"><span data-stu-id="b3600-170">Reaches out to Microsoft for activity data.</span></span></li> 
</ul>
</td>
<td>
<p><span data-ttu-id="b3600-171">GDRP 管理者は、DSR 要求を満たすために取得したデータを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3600-171">Your GDRP administrator sees the data that has been obtained to fulfill the DSR request.</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="responding-to-requests-to-view-correct-erase-object-or-export-personal-data"></a><span data-ttu-id="b3600-172">個人データを表示、修正、消去、却下、またはエクスポートする要求に対応</span><span class="sxs-lookup"><span data-stu-id="b3600-172">Responding to requests to view, correct, erase, object, or export personal data</span></span>

<span data-ttu-id="b3600-173">顧客は、自分の個人データが組織によって管理されることを理解する必要があると判断したとします。</span><span class="sxs-lookup"><span data-stu-id="b3600-173">Suppose that a customer decides that he or she wants to understand what personal data of theirs is maintained by an organization.</span></span> <span data-ttu-id="b3600-174">その顧客は、その組織に近づき、自分の DSR を実行するよう求めます。</span><span class="sxs-lookup"><span data-stu-id="b3600-174">That customer approaches that organization and asks to exercise his or her DSR.</span></span> <span data-ttu-id="b3600-175">データ主体が自分たちの DSR 行使するとき、コント ローラーは次の各項目に具体的に対処する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-175">When data subjects exercise their DSRs, controllers must address each of the following items specifically:</span></span>

+ <span data-ttu-id="b3600-176">データ件名が自身の要求の一部として与えた情報を使用してユーザーとロール (ユーザーは従業員、顧客、仕入先ですか?) を適切に識別します。</span><span class="sxs-lookup"><span data-stu-id="b3600-176">Properly identify the person and role (is the person an employee, a customer, a vendor?) by using information that the data subject gave you as part of his or her request.</span></span> <span data-ttu-id="b3600-177">この情報は、名前、従業員 ID や顧客番号、または別の識別子である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-177">This information might be a name, an employee ID or customer number, or another identifier.</span></span>
+ <span data-ttu-id="b3600-178">リクエストの日付と時刻を記録します。</span><span class="sxs-lookup"><span data-stu-id="b3600-178">Record the date and time of the request.</span></span> <span data-ttu-id="b3600-179">(要求を完了するまでに 30 日あります。)</span><span class="sxs-lookup"><span data-stu-id="b3600-179">(You have 30 days to complete the request.)</span></span>
+ <span data-ttu-id="b3600-180">DSR 要求が適切かつ有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3600-180">Affirm that the DSR request is proper and valid.</span></span> <span data-ttu-id="b3600-181">法律顧問と連携して、有効な内容を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-181">You will need to work with your legal counsel to determine what is valid.</span></span> <span data-ttu-id="b3600-182">たとえば、DSR 要求のコンプライアンスが、ユーザーのその他の法的義務と競合しないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-182">For example, you must make sure that compliance with a DSR request doesn't conflict with any other legal obligations that you have.</span></span>
+ <span data-ttu-id="b3600-183">要求に関連する情報があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3600-183">Verify that you have the information that is related to the request.</span></span>

### <a name="reasons-why-certain-personal-data-may-not-be-modified-or-deleted"></a><span data-ttu-id="b3600-184">特定の個人データを変更または削除できない理由</span><span class="sxs-lookup"><span data-stu-id="b3600-184">Reasons why certain personal data may not be modified or deleted</span></span>

<span data-ttu-id="b3600-185">次のテーブルは、特定のシナリオで個人データの変更または削除が制限される理由を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3600-185">The following table lists several reasons why personal data modification or deletion is restricted in certain scenarios.</span></span>

| <span data-ttu-id="b3600-186">理由</span><span class="sxs-lookup"><span data-stu-id="b3600-186">Reason</span></span> | <span data-ttu-id="b3600-187">コメント</span><span class="sxs-lookup"><span data-stu-id="b3600-187">Comment</span></span> |
|--------|---------|
| <span data-ttu-id="b3600-188">財務、税金、一般会計原則 (GAAP)</span><span class="sxs-lookup"><span data-stu-id="b3600-188">Financial, tax, generally accepted accounting principles (GAAP)</span></span> | <span data-ttu-id="b3600-189">関係者を削除することはできませんが、関係者の名前は更新できます。</span><span class="sxs-lookup"><span data-stu-id="b3600-189">A party can't be deleted, but the party's name can be updated.</span></span> |
| <span data-ttu-id="b3600-190">財務、税、GAAP</span><span class="sxs-lookup"><span data-stu-id="b3600-190">Financial, tax, GAAP</span></span> | <span data-ttu-id="b3600-191">現在の作業者のデータは削除できませんが、作業者の名前を更新することはできます。</span><span class="sxs-lookup"><span data-stu-id="b3600-191">A current worker's data can't be deleted, but the worker's name can be updated.</span></span> | 
| <span data-ttu-id="b3600-192">GAAP</span><span class="sxs-lookup"><span data-stu-id="b3600-192">GAAP</span></span> | <span data-ttu-id="b3600-193">転記済または完了済みトランザクションは変更できません。</span><span class="sxs-lookup"><span data-stu-id="b3600-193">Posted or completed transactions can't be modified.</span></span> |


### <a name="right-to-view"></a><span data-ttu-id="b3600-194">表示するには右</span><span class="sxs-lookup"><span data-stu-id="b3600-194">Right to view</span></span>

<span data-ttu-id="b3600-195">組織は、データを表示する DSR 要求に応じて、次のアクションのいずれかを決定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-195">An organization might decide to take any of the following actions in response to a DSR request to view data:</span></span>

+ <span data-ttu-id="b3600-196">担当者検索レポートを使用して、個人データを検索および収集します。</span><span class="sxs-lookup"><span data-stu-id="b3600-196">Use the Person search report to find and collect personal data.</span></span> <span data-ttu-id="b3600-197">このレポートにアクセスするには、ナビゲーション ウィンドウで **モジュール > システム管理 > 問い合わせ >個人検索レポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3600-197">To access this report, from the navigation pane, select **Modules > System administration > Inquiries > Person search report**.</span></span> 
+ <span data-ttu-id="b3600-198">新しいエンティティを作成または既存のエンティティを拡張して、担当者検索レポートを拡張します。</span><span class="sxs-lookup"><span data-stu-id="b3600-198">Extend the Person search report by authoring a new entity or extending an existing entity.</span></span>
+ <span data-ttu-id="b3600-199">検索機能とフィルター機能を使用して特定の個人データを検索し、そのデータを Microsoft Office のエクスポート機能を使用してエクスポートするか、ブラウザーの拡張機能を使用して pdf に印刷します。</span><span class="sxs-lookup"><span data-stu-id="b3600-199">Use search and filter features to find specific personal data and export that data by using the Microsoft Office Export functionality or print that information to a .pdf using browser extensions.</span></span>
+ <span data-ttu-id="b3600-200">提供されたドキュメントを使用して、コントローラーが個人データとして識別したデータを含むデータ テーブルを識別します。</span><span class="sxs-lookup"><span data-stu-id="b3600-200">Use provided documentation to identify data tables that contain data that the controller has identified as personal data.</span></span>
+ <span data-ttu-id="b3600-201">個人データを検索してエクスポートするカスタム フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3600-201">Author a custom form that locates and exports personal data.</span></span>
+ <span data-ttu-id="b3600-202">認証された顧客が個人データを見ることを可能にする外部ポータルまたは Web サイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3600-202">Author an external portal or website that allows an authenticated customer to see his or her personal data.</span></span>

<span data-ttu-id="b3600-203">個人検索レポートは、DSRの要求の対象となる個人データを見つける際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b3600-203">The Person search report might help you discover personal data that is subject to a DSR request.</span></span> <span data-ttu-id="b3600-204">レポートに探している情報が含まれていない場合は、 Microsoft Dynamics Lifecycle Services (LCS) サイトで、その情報が載っている修正プログラムがあるか確認します。</span><span class="sxs-lookup"><span data-stu-id="b3600-204">If the report doesn't include the information that you're looking for, check the Microsoft Dynamics Lifecycle Services (LCS) site for possible hotfixes that include the information.</span></span> <span data-ttu-id="b3600-205">また、追加エンティティを作成、または提供されたエンティティを拡張することにより、レポートを自分で拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-205">You can also extend the report yourself by creating additional entities, or extending the provided entities.</span></span>

<span data-ttu-id="b3600-206">担当者検索レポートに、データの件名を要求しているすべての情報が含まれていない場合、Microsoft が提供するツールを使用して拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-206">If the Person search report doesn't contain all the information that the data subject is requesting, you can extend it by using tools that Microsoft has provided.</span></span> <span data-ttu-id="b3600-207">個人検索レポートを拡張する方法の詳細については、[個人検索レポートを拡張](./gdpr-extend-person-search-report.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3600-207">For information about how to extend the Person search report, see [Extend the Person search report](./gdpr-extend-person-search-report.md).</span></span>

### <a name="right-to-correct-"></a><span data-ttu-id="b3600-208">修正するには右\* \*\*</span><span class="sxs-lookup"><span data-stu-id="b3600-208">Right to correct\* \*\*</span></span>

<span data-ttu-id="b3600-209">組織は、データを修正するための DSR 要求に応じて、次のいずれかのアクションを実行することを決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-209">An organization might decide to take any of the following actions in response to a DSR request to correct data:</span></span>

+ <span data-ttu-id="b3600-210">担当者検索レポートを使用して、個人データを検索および収集します。</span><span class="sxs-lookup"><span data-stu-id="b3600-210">Use the Person search report to find and collect personal data.</span></span> 
+ <span data-ttu-id="b3600-211">新しいエンティティを作成または既存のエンティティを拡張して、担当者検索レポートを拡張します。</span><span class="sxs-lookup"><span data-stu-id="b3600-211">Extend the Person search report by authoring a new entity or extending an existing entity.</span></span>
+ <span data-ttu-id="b3600-212">特定の個人データを検索するには、検索機能とフィルター機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3600-212">Use search and filter features to find specific personal data.</span></span>
+ <span data-ttu-id="b3600-213">個人データを検索するカスタム フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3600-213">Author a custom form that locates personal data.</span></span>
+ <span data-ttu-id="b3600-214">認証された顧客が個人データを修正することを可能にする外部ポータルまたは Web サイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3600-214">Author an external portal or website that allows an authenticated customer to correct his or her personal data.</span></span>

<span data-ttu-id="b3600-215">データが特定されたら、製品内機能を使用して、製品が実行するための機能を提供する場所でデータを修正します。</span><span class="sxs-lookup"><span data-stu-id="b3600-215">When data is located, use in-product features to correct the data where the product offers the ability to do so.</span></span>

<span data-ttu-id="b3600-216">\*個人データと見なされるデータの中には、直接変更することができないものもあります。</span><span class="sxs-lookup"><span data-stu-id="b3600-216">\*You might find that some data that qualifies as personal data can't be modified directly.</span></span> <span data-ttu-id="b3600-217">このデータは通常、財務法 (税法など)、詐欺防止 (セキュリティ監査証跡)、または業界認定への準拠のために「現状のまま」保たれる金融取引やその他の業務データの一部です 。</span><span class="sxs-lookup"><span data-stu-id="b3600-217">Typically, this data is part of a financial transaction or other business data that is kept "as is" for compliance with financial laws (for example, tax laws), prevention of fraud (such as security audit trail), or compliance with industry certifications.</span></span>

<span data-ttu-id="b3600-218">\*\* GDPR は他のすべての法律を排除する法律ではありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-218">\*\* GDPR is not a law exclusive of all other laws.</span></span> <span data-ttu-id="b3600-219">エンタープライズ リソース プラン システムとして、Finance and Operations は特定のビジネスまたはトランザクション データの変更を許可していません。他の法律や認証のコンプライアンスに必要なビジネス データの変更のための機能を提供しておらず一切保証もしません。</span><span class="sxs-lookup"><span data-stu-id="b3600-219">As an enterprise resource planning system, Finance and Operations does not allow for modification of certain business or transactional data, and will not endorse nor provide functionality for the modification of business data that is necessary for compliance with other laws or certifications.</span></span> <span data-ttu-id="b3600-220">Finance and Operations は、参照の破損またはビジネス データの整合性が生じる変更/カスタマイズまたはその他のアクションに対して、サポートを提供しません。</span><span class="sxs-lookup"><span data-stu-id="b3600-220">Finance and Operations will not provide support for modifications/customizations or other actions that result in the corruption of referential or business data integrity.</span></span>


### <a name="right-to-be-forgotten"></a><span data-ttu-id="b3600-221">消去するには右\*</span><span class="sxs-lookup"><span data-stu-id="b3600-221">Right to be forgotten\*</span></span>

<span data-ttu-id="b3600-222">組織は、消去データの DSR 要求に応じて、次のアクションのいずれかを決定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-222">An organization might decide to take any of the following actions in response to a DSR request to erase data:</span></span>

+ <span data-ttu-id="b3600-223">製品が直接アクションを有効にする場所では、個人データを削除するか消去してください。</span><span class="sxs-lookup"><span data-stu-id="b3600-223">Delete or otherwise erase personal data where the product enables that action directly.</span></span>
+ <span data-ttu-id="b3600-224">製品が直接アクションを有効にする場合、個人データを匿名にします。</span><span class="sxs-lookup"><span data-stu-id="b3600-224">Anonymize the personal data where the product enables that action directly.</span></span>
+ <span data-ttu-id="b3600-225">個人データを消去または変更するカスタマイズを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3600-225">Author a customization to erase/modify the personal data.</span></span>

<span data-ttu-id="b3600-226">\* GDPR は他のすべての法律を排除する法律ではありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-226">\* GDPR is not a law exclusive of all other laws.</span></span> <span data-ttu-id="b3600-227">エンタープライズ リソース プラン システムとして、Finance and Operations は特定のビジネスまたはトランザクション データの削除を許可していません。他の法律や認証のコンプライアンスに必要なビジネス データの削除のための機能を提供しておらず一切保証もしません。</span><span class="sxs-lookup"><span data-stu-id="b3600-227">As an enterprise resource planning system, Finance and Operations does not allow for deletion of certain business or transactional data, and will not endorse nor provide functionality for the deletion of business data that is necessary for compliance with other laws or certifications.</span></span> <span data-ttu-id="b3600-228">Finance and Operations は、参照の破損またはビジネス データの整合性が生じる変更/カスタマイズまたはその他のアクションに対して、サポートを提供しません。</span><span class="sxs-lookup"><span data-stu-id="b3600-228">Finance and Operations will not provide support for modifications/customizations or other actions that result in the corruption of referential or business data integrity.</span></span>

### <a name="right-to-port"></a><span data-ttu-id="b3600-229">移植するには右</span><span class="sxs-lookup"><span data-stu-id="b3600-229">Right to port</span></span>

<span data-ttu-id="b3600-230">組織は、ポート データの DSR 要求に応じて、次のアクションのいずれかを決定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-230">An organization might decide to take any of the following actions in response to a DSR request to port data:</span></span>

+ <span data-ttu-id="b3600-231">Microsoft Office アドインを使用して、個人データをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="b3600-231">Use the Microsoft Office Add-in to export personal data.</span></span>
+ <span data-ttu-id="b3600-232">個人データのエクスポートを可能にするカスタム レポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3600-232">Author a custom report that enables the export of personal data.</span></span>
+ <span data-ttu-id="b3600-233">個人データをエクスポートするカスタマイズを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3600-233">Author a customization that exports personal data.</span></span>
+ <span data-ttu-id="b3600-234">人物検索レポートを使用または拡張して、データ対象者の個人情報のコピー要求に役立つ情報を収集します。</span><span class="sxs-lookup"><span data-stu-id="b3600-234">Use or extend the Person search report to gather information in support of a request for a copy of the data subject's personal information.</span></span>

<span data-ttu-id="b3600-235">個人検索レポートは、DSRの要求の対象となる個人データを見つける際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b3600-235">The Person search report might help you discover personal data that is subject to a DSR request.</span></span> <span data-ttu-id="b3600-236">レポートに探している情報が含まれていない場合は、情報が載っている修正プログラムの LCS サイトを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3600-236">If the report doesn't include the information that you're looking for, check the LCS site for possible hotfixes that include the information.</span></span> <span data-ttu-id="b3600-237">また、追加エンティティを作成することにより自分でレポートを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-237">You can also extend the report yourself by creating additional entities.</span></span>

<span data-ttu-id="b3600-238">担当者検索レポートに、データの件名を要求しているすべての情報が含まれていない場合、Microsoft が提供するツールを使用して拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-238">If the Person search report doesn't contain all the information that the data subject is requesting, you can extend it by using tools that Microsoft has provided.</span></span> <span data-ttu-id="b3600-239">個人検索レポートを拡張する方法の詳細については、[個人検索レポートを拡張](./gdpr-extend-person-search-report.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3600-239">For information about how to extend the Person search report, see [Extend the Person search report](./gdpr-extend-person-search-report.md).</span></span>

<span data-ttu-id="b3600-240">コントローラは、GDPR 内で定義されているようにデータ主体に返されなければならないデータの範囲外にある特定の種類の情報を、独自の裁量で編集することを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-240">The controller may, at their sole discretion choose to redact certain types of information that may fall outside of the scope of data that must be returned to the data subject as defined within the GDPR.</span></span>

## <a name="right-to-restrict"></a><span data-ttu-id="b3600-241">制限するには右</span><span class="sxs-lookup"><span data-stu-id="b3600-241">Right to restrict</span></span>

<span data-ttu-id="b3600-242">組織は、オプションのデータ処理を制限する DSR 要求に応じて、次のアクションのいずれかを決定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-242">An organization might decide to take the following action in response to a DSR request to restrict optional data processing:</span></span>

+ <span data-ttu-id="b3600-243">たとえば、マーケティング キャンペーンから顧客を削除します。</span><span class="sxs-lookup"><span data-stu-id="b3600-243">Remove the customer from, for example, a marketing campaign.</span></span>

<span data-ttu-id="b3600-244">\* GDPR は他のすべての法律を排除する法律ではありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-244">\* GDPR is not a law exclusive of all other laws.</span></span> <span data-ttu-id="b3600-245">エンタープライズ リソース プラン システムとして、Finance and Operations は特定のビジネスまたはトランザクション データの制限された処理を許可していません。他の法律や認証のコンプライアンスに必要なビジネス データの処理の制限に関する機能を提供しておらず一切保証もしません。</span><span class="sxs-lookup"><span data-stu-id="b3600-245">As an enterprise resource planning system, Finance and Operations does not allow for restricted processing of certain business or transactional data, and will not endorse nor provide functionality for the restriction of processing of business data that is necessary for compliance with other laws or certifications.</span></span> <span data-ttu-id="b3600-246">Finance and Operations は、参照の破損またはビジネス データの整合性が生じる変更/カスタマイズまたはその他のアクションに対して、サポートを提供しません。</span><span class="sxs-lookup"><span data-stu-id="b3600-246">Finance and Operations will not provide support for modifications/customizations or other actions that result in the corruption of referential or business data integrity.</span></span>


## <a name="controller-considerations"></a><span data-ttu-id="b3600-247">コントローラーの考慮事項</span><span class="sxs-lookup"><span data-stu-id="b3600-247">Controller considerations</span></span>

<span data-ttu-id="b3600-248">コントローラは、以下の情報を使用して DSR 要求を完了できます。</span><span class="sxs-lookup"><span data-stu-id="b3600-248">Controllers can use the following information to complete DSR requests.</span></span>

#### <a name="system-inventory"></a><span data-ttu-id="b3600-249">システム インベントリ</span><span class="sxs-lookup"><span data-stu-id="b3600-249">System inventory</span></span>

+ <span data-ttu-id="b3600-250">**データの在庫およびタグ付け** - Microsoft は、開発者と顧客が使用できるタグ付けインフラストラクチャを実現しました。</span><span class="sxs-lookup"><span data-stu-id="b3600-250">**Data inventory and tagging** – Microsoft has enabled a tagging infrastructure that developers and customers can use.</span></span> <span data-ttu-id="b3600-251">メタデータに定義されている各データ フィールドには、コントローラーが個人データの定義に適合すると判断したデータを識別するために選択した値または用語を、確認または変更できる推奨値を持つ分類プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3600-251">Each data field that is defined in metadata contains a classification property that has a suggested value that the controller can confirm or change to any value or term they choose in order to identify data that they deem fits within the definition of personal data.</span></span>
+ <span data-ttu-id="b3600-252">**データ フロー ダイアグラム** - Microsoft は、顧客の生産環境におけるシステム間のデータのフローを識別するデータ フロー ダイアグラムを公開します。</span><span class="sxs-lookup"><span data-stu-id="b3600-252">**Data flow diagram** – Microsoft will publish a data flow diagram that identifies flows of data between systems in the customers production environments.</span></span>
+ <span data-ttu-id="b3600-253">**個人検索レポート** – Finance and Operations には、要求者の個人情報のコピーの要求をサポートする情報を収集するために使用できる個人検索レポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3600-253">**Person search report** – Finance and Operations includes the Person search report, which can be used to gather information in support of a request for a copy of the requestor's personal information.</span></span> 

## <a name="activity-and-diagnostic-information"></a><span data-ttu-id="b3600-254">活動と診断情報</span><span class="sxs-lookup"><span data-stu-id="b3600-254">Activity and diagnostic information</span></span>

<span data-ttu-id="b3600-255">コントローラーは、[Microsoft Enterprise Privacy Portal](https://www.microsoft.com/trustcenter/privacy) を使用してテレメトリ データに関する DSR 要求を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-255">The controller can make DSR requests regarding telemetry data by using the [Microsoft Enterprise Privacy Portal](https://www.microsoft.com/trustcenter/privacy).</span></span> <span data-ttu-id="b3600-256">収集する一部のテレメトリ データは、システムで生成されるログです。</span><span class="sxs-lookup"><span data-stu-id="b3600-256">Some telemetry data that we collect is in system generated logs.</span></span> <span data-ttu-id="b3600-257">追加情報または支援なしでは、ユーザーの ID は匿名です。</span><span class="sxs-lookup"><span data-stu-id="b3600-257">Without additional information or your assistance, the user's identity is anonymous.</span></span>

## <a name="representation-of-a-person-in-finance-and-operations"></a><span data-ttu-id="b3600-258">Finance and Operations のユーザーの表示</span><span class="sxs-lookup"><span data-stu-id="b3600-258">Representation of a person in Finance and Operations</span></span>

<span data-ttu-id="b3600-259">Finance and Operations には共通の [グローバル アドレス帳](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/overview-global-address-book) があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-259">Finance and Operations has a common [Global address book](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/overview-global-address-book).</span></span> <span data-ttu-id="b3600-260">連絡先、顧客、ユーザー、作業者、または他の担当者をシステムに追加するたびに、通常はアドレス帳にその人物のエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3600-260">Typically, every time that you add a contact, customer, user, worker, or other person in your system, you first create an address book entry for that person.</span></span> <span data-ttu-id="b3600-261">アドレス帳の各ユーザーは関係者と呼ばれ、PartyID が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b3600-261">Each person in the address book is referred to as a party and is assigned a PartyID.</span></span> <span data-ttu-id="b3600-262">担当者は、顧客、ユーザー、または作業者などのシステム内でのロールも保有して、CustID、UserID、WorkerID などの ロール ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="b3600-262">The person also takes on a role in the system, such as Customer, User, or Worker, and has a role ID: CustID, UserID, WorkerID, and so on.</span></span>

![グローバル アドレス帳のデータ モデル](../media/gdpr-address-data-model.jpg)

### <a name="each-person-is-a-type-of-party"></a><span data-ttu-id="b3600-264">各担当者は、関係者のタイプです。</span><span class="sxs-lookup"><span data-stu-id="b3600-264">Each person is a type of party</span></span>

<span data-ttu-id="b3600-265">関係者レコードに関連付けられているロールは、関係者ロールと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b3600-265">Roles that are associated with party records are referred to as party roles.</span></span> <span data-ttu-id="b3600-266">パーティーの役割はいくつかあり、パーティーの両方のタイプ (個人と組織) に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-266">There are several party roles, and they can be assigned to both party types (person and organization):</span></span>

+ <span data-ttu-id="b3600-267">**顧客** - 他の個人、会社、またはエンティティによって生産される商品やサービスを購入する個人、会社、または他のエンティティ。</span><span class="sxs-lookup"><span data-stu-id="b3600-267">**Customer** – An individual, company, or other entity that purchases goods and services that are produced by other individuals, companies, or entities.</span></span>
+ <span data-ttu-id="b3600-268">**見込顧客** – 組織が提供する商品やサービスに興味がある当事者。</span><span class="sxs-lookup"><span data-stu-id="b3600-268">**Prospect** – A party that might be interested in goods or services an organization provides.</span></span>
+ <span data-ttu-id="b3600-269">**作業者** – 従業員または契約社員のロールを引き受けるか、またはサービスと引き換えに給与が支払われる人。</span><span class="sxs-lookup"><span data-stu-id="b3600-269">**Worker** – A person who assumes the role of an employee or a contractor, or who is paid in exchange for services.</span></span>
+ <span data-ttu-id="b3600-270">**ユーザー** – システムのユーザーになっている人物。</span><span class="sxs-lookup"><span data-stu-id="b3600-270">**User** – A person who is a user of the system.</span></span> <span data-ttu-id="b3600-271">ユーザーは、グローバル アドレス帳で識別されません。</span><span class="sxs-lookup"><span data-stu-id="b3600-271">The user isn't identified in the Global address book.</span></span>
+ <span data-ttu-id="b3600-272">**仕入先** – 支払いと引き換えに、1 社かそれ以上の法人に製品を供給する関係者。</span><span class="sxs-lookup"><span data-stu-id="b3600-272">**Vendor** – A party that supplies products to one or more legal entities in exchange for payment.</span></span>
+ <span data-ttu-id="b3600-273">**競合他社** - 自社が提供する商品やサービスのような商品やサービスを提供する個人や組織。</span><span class="sxs-lookup"><span data-stu-id="b3600-273">**Competitor** – A person or organization that provides goods or services that are like the goods or services that your business provides.</span></span> <span data-ttu-id="b3600-274">初期状態では、競合他社の特定の ID がありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-274">Out of the box, there is no particular identification for competitors.</span></span>
+ <span data-ttu-id="b3600-275">**申請者** - 組織の業務をしたり、組織内の空席の職務を埋めるための正式な書面または電子形式の要求を行う人。</span><span class="sxs-lookup"><span data-stu-id="b3600-275">**Applicant** – A person who makes a formal written or electronic request to work for an organization or fill an open position in it.</span></span>
+ <span data-ttu-id="b3600-276">**連絡先** - 組織の内部または外部のいずれかで、エントリーを作成した個人。</span><span class="sxs-lookup"><span data-stu-id="b3600-276">**Contact** – A person, either inside or outside your organization, that you've created an entry for.</span></span> <span data-ttu-id="b3600-277">このエントリでは、個人の住所、電子メール アドレス、電話や FAX 番号、および Web ページの URL などの情報を保存できます。</span><span class="sxs-lookup"><span data-stu-id="b3600-277">In this entry, you can save information such as the person's street and email addresses, telephone and fax numbers, and webpage URLs.</span></span>

### <a name="the-right-to-view-and-port-its-all-about-the-party"></a><span data-ttu-id="b3600-278">表示する権限およびポート: 関係者に関するすべて</span><span class="sxs-lookup"><span data-stu-id="b3600-278">The right to view and port: It's all about the party</span></span>

<span data-ttu-id="b3600-279">データ主体がコントローラーに申し入れてユーザーの個人データのコピーを要求するとき、そのコントローラーは、個人を説明するデータを特定するためにグローバル アドレス帳情報を使用する選択をすることがあります。</span><span class="sxs-lookup"><span data-stu-id="b3600-279">When a data subject approaches the controller to request a copy of his or her personal data, the controller might choose to use the Global address book information to locate the data that describes the person.</span></span> <span data-ttu-id="b3600-280">このトピックの前の図で説明したように、**人物**は**ロール**を担う**関係者**のタイプです。</span><span class="sxs-lookup"><span data-stu-id="b3600-280">As noted in the illustration earlier in this topic, a **person** is a type of **party** that plays a **role**.</span></span>

<span data-ttu-id="b3600-281">組織によっては、企業間の関係を通じてのみその活動を実施しているため、DSR の義務がそれほど多くありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-281">Some organizations conduct their activities only through business-to-business relationships and will have modest DSR obligations.</span></span> <span data-ttu-id="b3600-282">対照的に、他の組織はビジネスと顧客関係を通じて活動を実施します。</span><span class="sxs-lookup"><span data-stu-id="b3600-282">By contrast, other organizations conduct their activities through business-to-customer relationships.</span></span> <span data-ttu-id="b3600-283">これらの組織は、グローバル アドレス帳や、拡張性、カスタマイズ機能、[Excel で開く](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-edit-excel)操作を使用して、カスタム レポート、カスタム フォーム、カスタム クエリ、カスタム データ エクスポート の各機能を書き込み、ビジネスが顧客から収集するデータなどの特殊なニーズに地対応する、この関連データ リレーションシップを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-283">These organization might choose to use the Global address book and its associative data relationship to write custom reports, custom forms, custom queries, and custom data export features by using the extensibility and customization capabilities and [Open in Excel](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-edit-excel) experiences to serve the specific needs of the kinds of data that their business collects from their customers.</span></span>

## <a name="the-person-search-report"></a><span data-ttu-id="b3600-284">個人検索レポート</span><span class="sxs-lookup"><span data-stu-id="b3600-284">The Person search report</span></span>

<span data-ttu-id="b3600-285">コントローラーをサポートするために、このレポートでは、**データ管理** 作業領域で利用可能な既存のエンティティ モデル レポート機能を改善しています。</span><span class="sxs-lookup"><span data-stu-id="b3600-285">To support the controller, this report offers a refinement of the existing entity model reporting functionality that is available in the **Data management** workspace.</span></span> <span data-ttu-id="b3600-286">**データ管理** ワークスペースは、ほとんどのロールの種類のパッケージ化された表現のコレクションを提供します。</span><span class="sxs-lookup"><span data-stu-id="b3600-286">The **Data management** workspace offers a collection of pre-packaged representations of most role types.</span></span> <span data-ttu-id="b3600-287">これらの表現はエンティティと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b3600-287">These representations are known as entities.</span></span>

> [!NOTE]
> <span data-ttu-id="b3600-288">個人検索レポートは、Finance、Supply Chain Management、コマース、および人事管理に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3600-288">The Person search report is available for Finance, Supply Chain Managament, Commerce, and Human Resources.</span></span> <span data-ttu-id="b3600-289">現在、レポートは Microsoft Dynamics AX 2012 をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b3600-289">Currently the report does not support Microsoft Dynamics AX 2012.</span></span> 

<span data-ttu-id="b3600-290">エンティティは特定のロールのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="b3600-290">An entity represents an instance of a specific role.</span></span> <span data-ttu-id="b3600-291">データ管理機能を使用すると、コントローラーはエンティティ データを、コロン区切り値、コンマ区切り値 (CSV)、セミコロン区切り値、タブ区切り値、Microsoft Excel、および XML などの複数の形式にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="b3600-291">The data management functionality lets the controller export entity data to several formats, such as colon-separated values, comma-separated values (CSV), semicolon-separated values, tab-separated values, Microsoft Excel, and XML.</span></span>

<span data-ttu-id="b3600-292">担当者検索レポートは、当事者と関連付けられた**すべて**のロール (および対応するエンティティ) を識別するために使用される当事者 ID を提供することにより、**データ管理**ワークスペースでエンティティ データをエクスポートする追加の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="b3600-292">The Person search report provides additional capabilities in the **Data management** workspace that export entity data by providing a party ID that is used to identify **all** roles (and corresponding entities) that are associated with the party.</span></span> <span data-ttu-id="b3600-293">この機能を使用すると、すべてのエンティティ データとトランザクション データを単一のアクションまたは単一の関係者または複数の関係者のいずれかでエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="b3600-293">This capability lets you export all entity and transaction data in a single action, for either a single party or a collection of parties.</span></span>

<span data-ttu-id="b3600-294">データ主体がコントローラーに申し入れてユーザーの個人データのコピーを要求するとき、そのコントローラーは、個人を説明するデータを特定するためにグローバル アドレス帳情報を使用する選択をすることがあります。</span><span class="sxs-lookup"><span data-stu-id="b3600-294">When a data subject approaches the controller to request a copy of his or her personal data, the controller might choose to use the Global address book information to locate the data that describes the person.</span></span> <span data-ttu-id="b3600-295">このトピックの前の図で説明したように、**人物**は**ロール**を担う**関係者**のタイプです。</span><span class="sxs-lookup"><span data-stu-id="b3600-295">As noted in the illustration earlier in this topic, a **person** is a type of **party** that plays a **role**.</span></span>

<span data-ttu-id="b3600-296">組織によっては、企業間の関係を通じてのみその活動を実施しているため、DSR の義務がそれほど多くありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-296">Some organizations conduct their activities only through business-to-business relationships and will have modest DSR obligations.</span></span> <span data-ttu-id="b3600-297">対照的に、他の組織はビジネスと顧客関係を通じて活動を実施します。</span><span class="sxs-lookup"><span data-stu-id="b3600-297">By contrast, other organizations conduct their activities through business-to-customer relationships.</span></span> <span data-ttu-id="b3600-298">これらの組織は、グローバル アドレス帳や、拡張性、カスタマイズ機能、[Excel で開く](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-edit-excel#how-do-i-add-an-explicit-button-for-a-template-open-in-excel-option)操作を使用して、カスタム レポート、カスタム フォーム、カスタム クエリ、カスタム データ エクスポート の各機能を書き込み、ビジネスが顧客から収集するデータなどの特殊なニーズに地対応する、この関連データ リレーションシップを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-298">These organization might choose to use the Global address book and its associative data relationship to write custom reports, custom forms, custom queries, and custom data export features by using the extensibility and customization capabilities and [Open in Excel](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-edit-excel#how-do-i-add-an-explicit-button-for-a-template-open-in-excel-option) experiences to serve the specific needs of the kinds of data that their business collects from their customers.</span></span>

## <a name="additional-notes-that-apply-to-requests-for-data"></a><span data-ttu-id="b3600-299">データの要求に適用される追加のメモ</span><span class="sxs-lookup"><span data-stu-id="b3600-299">Additional notes that apply to requests for data</span></span>

+ <span data-ttu-id="b3600-300">Management Reporter および Microsoft Power BI プレゼンテーションのデータは、さまざまな財務書類に入力された情報から生成され、レポート目的でそれらのアプリケーションに転送されます。</span><span class="sxs-lookup"><span data-stu-id="b3600-300">Data in Management Reporter and in Microsoft Power BI presentations is generated from the information that is entered in various financial documents and then transferred to those applications for reporting purposes.</span></span> <span data-ttu-id="b3600-301">レポート、Excel にエクスポートおよび個人検索レポートなどのツールを使用して、財務書類からデータの要求を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-301">Any request for data should be fulfilled from the financial documents by using tools such as reports, Export to Excel, and the Person search report.</span></span> <span data-ttu-id="b3600-302">基本機能を変更するカスタマイズを行わなかった場合は、GDPR 要求を満たすために、Management Reporter や Power BI から追加のレポートを行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-302">You should not need to do additional reporting from Management Reporter or Power BI to fulfill a GDPR request unless you have made customizations that have altered the base functionality.</span></span>
+ <span data-ttu-id="b3600-303">ドキュメントや添付ファイルに含まれる個人用のデータは、レポートに依存しないデータ件名に返す必要もあります。</span><span class="sxs-lookup"><span data-stu-id="b3600-303">Personal data that is included in documents or attachments might also need to be returned to the data subject, independent of any reporting.</span></span>
+ <span data-ttu-id="b3600-304">マスター レコードに関連付けられているトランザクションのデータがある場合は削除できません。</span><span class="sxs-lookup"><span data-stu-id="b3600-304">If a master record has transactional data associated with it, it can't be deleted.</span></span>
+ <span data-ttu-id="b3600-305">同様に、転記済または完了済みのトランザクションは削除できません。</span><span class="sxs-lookup"><span data-stu-id="b3600-305">Similarly, transactions that have been posted or completed can't be deleted.</span></span>

### <a name="reasons-why-finance-and-operations-might-not-support-modifying-or-deleting-data-out-of-the-box"></a><span data-ttu-id="b3600-306">Finance and Operations がそのままではデータの変更と削除をサポートしない理由</span><span class="sxs-lookup"><span data-stu-id="b3600-306">Reasons why Finance and Operations might not support modifying or deleting data out of the box</span></span>

<span data-ttu-id="b3600-307">次のテーブルは、データの変更が制限される理由を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3600-307">The following table lists several reasons why data modifications might be restricted.</span></span>

|<span data-ttu-id="b3600-308">理由</span><span class="sxs-lookup"><span data-stu-id="b3600-308">Reason</span></span> | <span data-ttu-id="b3600-309">コメント</span><span class="sxs-lookup"><span data-stu-id="b3600-309">Comment</span></span> |
|-------|---------|
| <span data-ttu-id="b3600-310">監査</span><span class="sxs-lookup"><span data-stu-id="b3600-310">Audit</span></span> | <span data-ttu-id="b3600-311">コンプライアンスと監査のためにデータを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-311">Data must be preserved for compliance and auditing.</span></span> |
| <span data-ttu-id="b3600-312">計算済</span><span class="sxs-lookup"><span data-stu-id="b3600-312">Calculated</span></span> | <span data-ttu-id="b3600-313">計算されたデータは、計算に含まれるデータを変更することによってのみ変更できます。</span><span class="sxs-lookup"><span data-stu-id="b3600-313">Data that has been calculated can be changed only by changing the data that is included in the calculation.</span></span> |
| <span data-ttu-id="b3600-314">財務、税金、一般会計原則 (GAAP)</span><span class="sxs-lookup"><span data-stu-id="b3600-314">Financial, tax, generally accepted accounting principles (GAAP)</span></span> | <span data-ttu-id="b3600-315">転記済トランザクションは変更または削除できません。</span><span class="sxs-lookup"><span data-stu-id="b3600-315">Posted transactions can't be modified or deleted.</span></span> |
| <span data-ttu-id="b3600-316">インポート ログ</span><span class="sxs-lookup"><span data-stu-id="b3600-316">Import log</span></span> | <span data-ttu-id="b3600-317">コンプライアンスと監査のためにデータを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-317">Data must be preserved for compliance and auditing.</span></span> |

### <a name="what-types-of-personal-data-might-exist-in-the-product"></a><span data-ttu-id="b3600-318">製品に存在する可能性のある個人データの種類</span><span class="sxs-lookup"><span data-stu-id="b3600-318">What types of personal data might exist in the product</span></span>

<span data-ttu-id="b3600-319">会社にデータ要求が送られることを想定してください。</span><span class="sxs-lookup"><span data-stu-id="b3600-319">You should expect data requests to come to your company.</span></span> <span data-ttu-id="b3600-320">データを要求する人を、会社との 1 つまたは場合によっては複数のリレーションシップに分類することができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-320">You can categorize the people who request data into one or, in some cases, more than one relationship with your company:</span></span>

+ <span data-ttu-id="b3600-321">顧客</span><span class="sxs-lookup"><span data-stu-id="b3600-321">Customers</span></span> 
+ <span data-ttu-id="b3600-322">仕入先</span><span class="sxs-lookup"><span data-stu-id="b3600-322">Vendors</span></span>
+ <span data-ttu-id="b3600-323">作業者</span><span class="sxs-lookup"><span data-stu-id="b3600-323">Workers</span></span>
+ <span data-ttu-id="b3600-324">ユーザー</span><span class="sxs-lookup"><span data-stu-id="b3600-324">Users</span></span>
+ <span data-ttu-id="b3600-325">倉庫作業者</span><span class="sxs-lookup"><span data-stu-id="b3600-325">Warehouse workers</span></span>
+ <span data-ttu-id="b3600-326">トラック運転手</span><span class="sxs-lookup"><span data-stu-id="b3600-326">Truck drivers</span></span>
+ <span data-ttu-id="b3600-327">見込顧客</span><span class="sxs-lookup"><span data-stu-id="b3600-327">Prospects</span></span>
+ <span data-ttu-id="b3600-328">連絡先</span><span class="sxs-lookup"><span data-stu-id="b3600-328">Contacts</span></span>
+ <span data-ttu-id="b3600-329">応募者</span><span class="sxs-lookup"><span data-stu-id="b3600-329">Applicants</span></span>
+ <span data-ttu-id="b3600-330">競合他社</span><span class="sxs-lookup"><span data-stu-id="b3600-330">Competitors</span></span>

<span data-ttu-id="b3600-331">個人データは、ここにリストされていない他のロールにも含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-331">Personal data might also be contained in other roles that aren't listed here.</span></span> <span data-ttu-id="b3600-332">個人データの入力、表示、編集するために使用されるページは、上記の一覧のほとんどのロールのワークシートで提供されてきました。</span><span class="sxs-lookup"><span data-stu-id="b3600-332">Pages used to enter, view or edit personal data have been provided in worksheets for most roles in the preceding list.</span></span> <span data-ttu-id="b3600-333">CustomerSource の[個人データの検索および管理の参照ドキュメント](https://mbs.microsoft.com/customersource/global/AX/learning/documentation/white-papers/referencedocumentspersonaldata)ページからスプレッドシートを表示したりダウンロードしたりできます。</span><span class="sxs-lookup"><span data-stu-id="b3600-333">You can view or download the spreadsheets from the [Reference documents for finding and managing personal data](https://mbs.microsoft.com/customersource/global/AX/learning/documentation/white-papers/referencedocumentspersonaldata) page on CustomerSource.</span></span> 

## <a name="detailed-inventory"></a><span data-ttu-id="b3600-334">詳細な在庫</span><span class="sxs-lookup"><span data-stu-id="b3600-334">Detailed inventory</span></span>

<span data-ttu-id="b3600-335">Finance and Operations アプリを使用する場合は、複数のデータ ストアに存在する大量のデータを生成または収集する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="b3600-335">As you use Finance and Operations apps, you might find that you generate or collect large amounts of data that resides in multiple data stores.</span></span> <span data-ttu-id="b3600-336">データの格納場所を理解するのに役立つように、データ ストア内のデータごとにデータ マーカーを導入しました。</span><span class="sxs-lookup"><span data-stu-id="b3600-336">To help you make sense of where your data resides, we've introduced a data marker for each piece of data in our data stores.</span></span> <span data-ttu-id="b3600-337">このマーカーは「資産分類」と呼ばれ、個人データの識別や追跡に使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3600-337">This marker is called "Asset Classification," and it can be used to identify or track personal data.</span></span> <span data-ttu-id="b3600-338">収集するデータは「顧客コンテンツ」として説明されています。</span><span class="sxs-lookup"><span data-stu-id="b3600-338">Any data that you collect has been described as "customer content."</span></span> <span data-ttu-id="b3600-339">一部の顧客コンテンツには個人データが含まれていることがあり、一部の顧客コンテンツはビジネス データを含む場合があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-339">Some customer content might contain personal data, and some customer content might contain business data.</span></span> <span data-ttu-id="b3600-340">顧客のすべてのコンテンツを個人データとして処理することを選択、または「個人データ」であるとみなす任意のデータを識別して追跡できるように分類を自分で変更することができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-340">You can choose to treat all customer content as personal data, or you can change the classification yourself, so that you can identify and track any data that you feel is considered "Personal Data."</span></span> <span data-ttu-id="b3600-341">Microsoft は既定の分類のセットで指定されてはいますが、選択した分類や識別子を自由に使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3600-341">Although Microsoft has a supplied a set of default classifications, you're free to use any classification or identifiers that you choose.</span></span>

<Link to documentation on how to modify asset classifications>

<Asset Classification table>

<Link to form that prints the full inventory>

![プロパティに AssetClassification フィールドを示しているソリューション エクスプローラー](../media/gdpr-asset-classification-detail-invent-section.jpg)

## <a name="age-gating-preventing-minors-from-using-the-service"></a><span data-ttu-id="b3600-343">年齢ゲーティング: 未成年がサービスを利用できないようにします。</span><span class="sxs-lookup"><span data-stu-id="b3600-343">Age Gating: Preventing minors from using the service</span></span>

### <a name="overview"></a><span data-ttu-id="b3600-344">概要</span><span class="sxs-lookup"><span data-stu-id="b3600-344">Overview</span></span>

<span data-ttu-id="b3600-345">Microsoft は、個人データが収集される Microsoft ソフトウェアのすべてのユーザーが、認証に Microsoft アカウント (MSA) または Microsoft Azure Active Directory (Azure AD) アカウントを使用することを必須とします。</span><span class="sxs-lookup"><span data-stu-id="b3600-345">Microsoft mandates that all users of Microsoft software where personal data is collected must use a Microsoft account (MSA) or Microsoft Azure Active Directory (Azure AD) account for authentication.</span></span> <span data-ttu-id="b3600-346">また、これらのアカウントは、ソフトウェアまたはサービスを使用する未成年者が個人データを使用するためにサービスに対して保護者の同意を得ることを確認するように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-346">Additionally, those accounts must be configured to enable minors who use the software or service to affirm parental consent for the service to use their personal data.</span></span>

### <a name="what-is-this-feature"></a><span data-ttu-id="b3600-347">これはどういう機能ですか ?</span><span class="sxs-lookup"><span data-stu-id="b3600-347">What is this feature?</span></span>

<span data-ttu-id="b3600-348">サービスのテナント管理者としては、Azure AD 年齢ゲーティングまたは MSA 年齢ゲーティングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-348">As the tenant admin of the service, you will be required to set up Azure AD Age Gating and/or MSA age gating.</span></span> <link to azure doc>

<span data-ttu-id="b3600-349">Azure 年齢ゲーティングを使用して設定されていないユーザーは、ユーザーがマイナーでない場合でも、サービスの使用を制限されます。</span><span class="sxs-lookup"><span data-stu-id="b3600-349">Any user who isn't configured by using Azure Age Gating will be restricted from using the service, even if the user isn't a minor.</span></span> <span data-ttu-id="b3600-350">年齢ゲーティングをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3600-350">Age Gating must be configured.</span></span>

<span data-ttu-id="b3600-351">サインイン年齢ゲートを使用して、マイクロソフトのソフトウェアおよびシステムへのアクセスを制限します。</span><span class="sxs-lookup"><span data-stu-id="b3600-351">We will restrict access to our software and systems by using a sign-in age gate.</span></span>

### <a name="how-will-age-gating-work"></a><span data-ttu-id="b3600-352">年齢ゲーティングはどのように機能しますか。</span><span class="sxs-lookup"><span data-stu-id="b3600-352">How will age gating work?</span></span>

<span data-ttu-id="b3600-353">GDPR は、未成年者に保護者の同意がない場合、システムがその未成年者の個人データの処理を停止する必要があることを定めています。</span><span class="sxs-lookup"><span data-stu-id="b3600-353">The GDPR specifies that systems must stop processing a minor's personal data if that minor doesn't have parental consent.</span></span> <span data-ttu-id="b3600-354">同意を付与してから取り消しできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b3600-354">Note that consent can be given and then withdrawn.</span></span> <span data-ttu-id="b3600-355">したがって、ユーザーはシステムに 1 日しかアクセスできず、次の日にアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b3600-355">Therefore, a user might have access to the system one day but not the next.</span></span>

## <a name="privacy-notices-and-user-subject-rights"></a><span data-ttu-id="b3600-356">プライバシーに関する通知およびユーザー件名権限</span><span class="sxs-lookup"><span data-stu-id="b3600-356">Privacy notices and user subject rights</span></span>

### <a name="displaying-your-organizations-user-rights-and-privacy-notice"></a><span data-ttu-id="b3600-357">組織のユーザー権限およびプライバシー通知を表示</span><span class="sxs-lookup"><span data-stu-id="b3600-357">Displaying your organizations user rights and privacy notice</span></span>

<span data-ttu-id="b3600-358">**情報**ボックスに、Microsoft のユーザー権利のドキュメントおよび Microsoft のプライバシーと Cookie のドキュメントへのリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3600-358">In the **About** box, you will find links to the Microsoft user rights documentation, and to the Microsoft privacy and cookies documentation.</span></span> <span data-ttu-id="b3600-359">また、組織のプライバシーに関する声明にリンクを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-359">You can also add a link to your organization's privacy statement.</span></span>

![資産を示すソリューション エクスプローラー](../media/gdpr-privacy-01-w-note.jpg)

<span data-ttu-id="b3600-361">**システム パラメーター**ページで、システム管理者は、組織のユーザー権限およびプライバシーに関する通知へのリンクを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3600-361">On the **System parameters** page, system administrator can add links to the organization's user rights and privacy notices.</span></span> <span data-ttu-id="b3600-362">通知タイプのいずれかまたは両方に、有効な URL を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b3600-362">You can add a valid URL for one or both notice types.</span></span>

![組織のプライバシーに関する声明にリンクを追加するシステム パラメーター](../media/gdpr-privacy-02.jpg)

<span data-ttu-id="b3600-364">システム パラメーターへの入力が完了したら、次の図に示されているように、組織のプライバシー通知へのリンクが **情報** ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3600-364">When you've completed your entries in the system parameters, the link to your organization's privacy notice will appear in the **About** box, as show in the following illustration.</span></span>

![組織のプライバシーに関する通知へのリンクがある変更詳細ボックス](../media/gdpr-privacy-03-w-note.jpg)

## <a name="clarification-of-the-scope-of-this-content"></a><span data-ttu-id="b3600-366">このコンテンツのスコープの明確化</span><span class="sxs-lookup"><span data-stu-id="b3600-366">Clarification of the scope of this content</span></span>

+ <span data-ttu-id="b3600-367">このドキュメントは、公開日現在の Microsoft が解釈する GDPR の解説です。</span><span class="sxs-lookup"><span data-stu-id="b3600-367">This documentation is a commentary on the GDPR, as Microsoft interprets it, as of the publication date.</span></span> <span data-ttu-id="b3600-368">GDPR に多くの時間を費やしたことにより、その目的と意味について深い思慮を持っていると考えています。</span><span class="sxs-lookup"><span data-stu-id="b3600-368">We have spent a lot of time with the GDPR and believe that we have been thoughtful about its intent and meaning.</span></span> <span data-ttu-id="b3600-369">ただし、GDPR のアプリケーションは非常に個別に異なっており、GDPR のすべての側面および解釈が十分に解決されているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-369">But the application of the GDPR is highly fact-specific, and not all aspects and interpretations of the GDPR are well-settled.</span></span>
+ <span data-ttu-id="b3600-370">このドキュメントは、情報提供のみを目的としたものであり、法的なアドバイスとして、または GDPR がユーザーおよび組織にどのように適用されるかを判断するためには使用できません。</span><span class="sxs-lookup"><span data-stu-id="b3600-370">This documentation is provided for informational purposes only, and should not be relied upon as legal advice or to determine how the GDPR might apply to you and your organization.</span></span> <span data-ttu-id="b3600-371">法的に資格のある専門家と連携して、GDPR、組織への GDPR の具体的な適用方法、およびコンプライアンスをもっとも確実にする方法について検討されることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b3600-371">We encourage you to work with a legally qualified professional to discuss the GDPR, how it applies specifically to your organization, and how to best ensure compliance.</span></span>
+ <span data-ttu-id="b3600-372">Microsoft はこのプレゼンテーションに記載されている情報に関して一切保証せず、明示的、暗示的、または法的に保証することもありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-372">MICROSOFT MAKES NO WARRANTIES, EXPRESS, IMPLIED, OR STATUTORY AS TO THE INFORMATION PROVIDED IN THIS PRESENTATION.</span></span> <span data-ttu-id="b3600-373">このドキュメントは、「現状のまま」で提供されています。</span><span class="sxs-lookup"><span data-stu-id="b3600-373">This documentation is provided "as is."</span></span> <span data-ttu-id="b3600-374">URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="b3600-374">Information and views expressed in this documentation, including URL and other Internet website references, may change without notice.</span></span>
+ <span data-ttu-id="b3600-375">このドキュメントは、Microsoft 製品の知的財産に対する法的権利をお客様に提供するものではありません。</span><span class="sxs-lookup"><span data-stu-id="b3600-375">This documentation does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="b3600-376">内部での参照目的のみの場合、このプレゼンテーションをコピーして使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3600-376">You may copy and use this presentation for your internal, reference purposes only.</span></span>
