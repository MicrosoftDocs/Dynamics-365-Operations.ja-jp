---
title: "機密データへのアクセスを管理"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のユーザー ログ機能について説明します。"
author: ToddLefor
manager: AnnBe
ms.date: 12/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 10031
ms.search.region: Global
ms.author: 
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: f00763144b7e65fa1dfb2d967a0ee36ede4b0047
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="guide-to-the-gdpr-for-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="8b534-103">Microsoft Dynamics 365 for Finance and Operations の GDPR に関するガイド</span><span class="sxs-lookup"><span data-stu-id="8b534-103">Guide to the GDPR for Microsoft Dynamics 365 for Finance and Operations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

## <a name="overview-of-the-gdpr"></a><span data-ttu-id="8b534-104">GDPR の概要</span><span class="sxs-lookup"><span data-stu-id="8b534-104">Overview of the GDPR</span></span>

<span data-ttu-id="8b534-105">欧州連合の一般データ保護規制 (GDPR) は、欧州連合 (EU) の市民および居住者のプライバシー権利、セキュリティ、およびコンプライアンスの新しいグローバル標準を設定します。</span><span class="sxs-lookup"><span data-stu-id="8b534-105">The European Union's General Data Protection Regulation (GDPR) sets a new global standard for privacy rights, security, and compliance for the citizens and residents of the European Union (EU).</span></span> <span data-ttu-id="8b534-106">GDPR は、EU 市民と居住者の個人データの処理および使用を制御します。</span><span class="sxs-lookup"><span data-stu-id="8b534-106">The GDPR governs the handling and use of personal data of EU citizens and residents.</span></span> <span data-ttu-id="8b534-107">GDPR の実施は 2018 年 5 月 25 日から開始され、非規制遵守に重大な影響があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-107">Enforcement of the GDPR begins May 25, 2018, and there are significant consequences for non-compliance.</span></span> <span data-ttu-id="8b534-108">規制の詳細については、[欧州連合サイト](https://europa.eu/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b534-108">For more information about the regulation, see the [European Union site](https://europa.eu/).</span></span>

> [!NOTE]
> <span data-ttu-id="8b534-109">このドキュメントのスコープおよび補充の詳細については、このトピックの最後にある [このコンテンツの範囲の説明](#clarification-of-the-scope-of-this-content) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b534-109">For information about the scope and coverage of this documentation, see [Clarification of the scope of this content](#clarification-of-the-scope-of-this-content) section at the end of this topic.</span></span>

<span data-ttu-id="8b534-110">GDPR は、次のアクションを実行できるように EU 市民に特定のデータ主体権利 (DSR) を与えます。</span><span class="sxs-lookup"><span data-stu-id="8b534-110">The GDPR gives EU citizens specific data subject rights (DSRs) that let them perform the following actions:</span></span>

+ <span data-ttu-id="8b534-111">個人データの表示。</span><span class="sxs-lookup"><span data-stu-id="8b534-111">View their personal data.</span></span>
+ <span data-ttu-id="8b534-112">個人データのエラーを訂正する。</span><span class="sxs-lookup"><span data-stu-id="8b534-112">Correct errors in their personal data.</span></span>
+ <span data-ttu-id="8b534-113">個人データの削除。</span><span class="sxs-lookup"><span data-stu-id="8b534-113">Erase their personal data.</span></span>
+ <span data-ttu-id="8b534-114">個人データを処理するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="8b534-114">Object to processing of their personal data.</span></span>
+ <span data-ttu-id="8b534-115">個人データをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="8b534-115">Export their personal data.</span></span>

<span data-ttu-id="8b534-116">GDPR は、[規制](http://data.consilium.europa.eu/doc/document/ST-5419-2016-INIT/en/pdf)の第 4 項の次の方法で個人データを定義しています (組織は個人データを持っていない)。</span><span class="sxs-lookup"><span data-stu-id="8b534-116">The GDPR defines personal data in the following way in article 4 of [the regulation](http://data.consilium.europa.eu/doc/document/ST-5419-2016-INIT/en/pdf) (organizations do not have personal data):</span></span>

> <span data-ttu-id="8b534-117">(1) 「個人データ」とは、特定または識別可能な自然人 (「データ主体」) に関するすべての情報を意味します。識別可能な自然人とは、特に、名前、識別番号、位置データ、オンライン識別子のような識別子、または身体的、生理学的、遺伝的、精神的、経済的、文化的、社会的アイデンティティーなど、その自然人固有の 1 つ以上の要因を参照することによって、直接的または間接的に、識別できる人のことです。</span><span class="sxs-lookup"><span data-stu-id="8b534-117">(1) 'personal data' means any information relating to an identified or identifiable natural person ('data subject'); an identifiable natural person is one who can be identified, directly or indirectly, in particular by reference to an identifier such as a name, an identification number, location data, an online identifier or to one or more factors specific to the physical, physiological, genetic, mental, economic, cultural or social identity of that natural person;</span></span>

<span data-ttu-id="8b534-118">コンプライアンスの責任を決定するために、GDPR は次のロールを識別します。</span><span class="sxs-lookup"><span data-stu-id="8b534-118">To determine responsibilities for compliance, the GDPR identifies the following roles:</span></span>

+ <span data-ttu-id="8b534-119">**データ コントローラー** - コントローラーは個人データを管理し、その使用方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="8b534-119">**Data controller** – The controller controls personal data and determines how it's used.</span></span> <span data-ttu-id="8b534-120">コントローラーの責任には、個人データの収集、維持、指揮、保護、変更、削除が含まれますが、これらに限定されません。</span><span class="sxs-lookup"><span data-stu-id="8b534-120">The responsibilities of the controller include but are not limited to collecting, maintaining, directing actions, protecting, modifying and deleting personal data.</span></span> <span data-ttu-id="8b534-121">コントローラーは、ユーザーをシステムに追加し、システムへのアクセスを許可し、データサブジェクトからデータを収集するか、会社のためにこれらのタスクを完了する従業員を持っています。</span><span class="sxs-lookup"><span data-stu-id="8b534-121">The controller either adds users to the system, grants access to the system, and collects data from data subjects, or has employees who complete these tasks on the company's behalf.</span></span> <span data-ttu-id="8b534-122">GDPR 要求のプロセスを理解し、GDPR 要求を実行する負担は、コントローラーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b534-122">The burden of understanding the process for GDPR requests and carrying out a GDPR request rests with the controller.</span></span>
+ <span data-ttu-id="8b534-123">**データ プロセッサ** - プロセッサは、データ コントローラーにサービスを提供し、データ コントローラーに代わってデータを処理します。</span><span class="sxs-lookup"><span data-stu-id="8b534-123">**Data processor** – The processor provides services to, and processes data on behalf of, the data controller.</span></span> <span data-ttu-id="8b534-124">プロセッサは、コントローラーに代わってアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="8b534-124">The processor performs actions on behalf of the controller.</span></span> <span data-ttu-id="8b534-125">プロセッサにより、コントローラーは GDPR に準拠できるようになりますが、データの所有権はなく DSR 要求に直接応答しません。</span><span class="sxs-lookup"><span data-stu-id="8b534-125">The processor makes it possible for the controller to be GDPR compliant, but has no ownership of the data and does not respond directly to DSR requests.</span></span>
+ <span data-ttu-id="8b534-126">**データ主体** - データ主体は、個人情報が使用されている自然人です。</span><span class="sxs-lookup"><span data-stu-id="8b534-126">**Data subject** – A data subject is a natural person whose personal information is being used.</span></span>
+ <span data-ttu-id="8b534-127">**C1** - C1 は Microsoft の直接顧客 (エンタープライズ クラウドの IT 管理者) です。</span><span class="sxs-lookup"><span data-stu-id="8b534-127">**C1** – C1 is a Microsoft direct customer (IT Admin in the Enterprise Cloud).</span></span>
+ <span data-ttu-id="8b534-128">**C2** - C2 は C1 の顧客です。</span><span class="sxs-lookup"><span data-stu-id="8b534-128">**C2** – C2 is C1's customer.</span></span>

<span data-ttu-id="8b534-129">Microsoft Dynamics 365 for Finance and Operations で、Microsoft はプロセッサとして動作します。</span><span class="sxs-lookup"><span data-stu-id="8b534-129">For Microsoft Dynamics 365 for Finance and Operations, Microsoft acts as a processor.</span></span> <span data-ttu-id="8b534-130">データ プロセッサとして、 Finance and Operations はデータ コントローラとして GDPR 責務に適応するのに役立つプロセスと機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="8b534-130">As a data processor, Finance and Operations provides processes and features that help you comply with your GDPR obligations as a data controller.</span></span>

<span data-ttu-id="8b534-131">次の図は、顧客から Finance and Operations データベースへのデータの流れ、およびお客様と Microsoft がそのプロセスで果たすロールを示しています。</span><span class="sxs-lookup"><span data-stu-id="8b534-131">The following illustration shows the flow of data from your customer to the Finance and Operations database, and the roles that you and Microsoft play in that process.</span></span> <span data-ttu-id="8b534-132">Finance and Operations で、コントローラーはテナント管理者、Microsoft はプロセッサです。</span><span class="sxs-lookup"><span data-stu-id="8b534-132">For Finance and Operations, the controller is the tenant administrator, and Microsoft is the processor.</span></span> <span data-ttu-id="8b534-133">このシナリオでは、データを保管、取得、並べ替えなどを行うことでデータを処理するプロセッサ (Microsoft) にデータが送信されます。</span><span class="sxs-lookup"><span data-stu-id="8b534-133">In this scenario, the data is sent to the processor (Microsoft), who then processes the data by storing it, retrieving it, sorting it, and so on.</span></span>

![顧客からのデータ フロー](../media/gdpr-customers-controller-processor.jpg)

<span data-ttu-id="8b534-135">データ主体が DSR の送信を選択すると、そのデータ主体はコントローラーに要求を出します。</span><span class="sxs-lookup"><span data-stu-id="8b534-135">When a data subject chooses to submit a DSR, the data subject makes the request to the controller.</span></span> <span data-ttu-id="8b534-136">データ主体は、ビジネスで収集したデータに対する Microsoft の権限を行使することはありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-136">Data subjects won't approach Microsoft to exercise their rights for data that your business has collected.</span></span> <span data-ttu-id="8b534-137">プロセッサとして、Microsoft は機能を提供することによって、またはアクションが可能であることを確認することによってコントローラを支援します。</span><span class="sxs-lookup"><span data-stu-id="8b534-137">As the processor, Microsoft assists the controller by providing features, or just by making sure that the actions are possible.</span></span> <span data-ttu-id="8b534-138">つまり、コントローラーは DSR 要求の受け入れて応答し、プロセッサはコンプライアンス要求を扱ったり有効化したりします。</span><span class="sxs-lookup"><span data-stu-id="8b534-138">In other words, the controller accepts and responds to a DSR request, and the processor assists with or enables the compliance request.</span></span> <span data-ttu-id="8b534-139">以下のテーブルは、Finance and Operations に関連するいくつかのロールと職責の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="8b534-139">The following table outlines some of the roles and responsibilities that are relevant to Finance and Operations.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="45%" />
<col width="25%" />
<col width="10%" />
</colgroup>
<tbody>
<tr class="odd">
<td>
<h3><span data-ttu-id="8b534-140"><strong>役割</strong></span><span class="sxs-lookup"><span data-stu-id="8b534-140"><strong>Role</strong></span></span></h3>
</td>
<td>
<h3><span data-ttu-id="8b534-141"><strong>シナリオ</strong></span><span class="sxs-lookup"><span data-stu-id="8b534-141"><strong>Scenarios</strong></span></span></h3>
</td>
<td>
<h3><span data-ttu-id="8b534-142"><strong>実装</strong></span><span class="sxs-lookup"><span data-stu-id="8b534-142"><strong>Implementation</strong></span></span></h3>
</td>
<td>
<h3><span data-ttu-id="8b534-143"><strong>データ アクセスのレベル</strong></span><span class="sxs-lookup"><span data-stu-id="8b534-143"><strong>Level of data access</strong></span></span></h3>
</td>
</tr>
<tr class="even">
<td>
<p><span data-ttu-id="8b534-144"><strong>顧客 (2)</strong></span><span class="sxs-lookup"><span data-stu-id="8b534-144"><strong>Your customer (2)</strong></span></span></p>
</td>
<td>
<ul>
<li><span data-ttu-id="8b534-145">個人データの表示</span><span class="sxs-lookup"><span data-stu-id="8b534-145">View personal data</span></span> </li>
<li><span data-ttu-id="8b534-146">個人データの修正</span><span class="sxs-lookup"><span data-stu-id="8b534-146">Correct personal data</span></span></li>
<li><span data-ttu-id="8b534-147">個人データの消去</span><span class="sxs-lookup"><span data-stu-id="8b534-147">Erase personal data</span></span> </li>
<li><span data-ttu-id="8b534-148">処理するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="8b534-148">Object to processing</span></span></li>
<li><span data-ttu-id="8b534-149">個人データをエクスポート</span><span class="sxs-lookup"><span data-stu-id="8b534-149">Export personal data</span></span></li></ul>
</td>
<td>
<p><span data-ttu-id="8b534-150">顧客が DSR (プロセスまたはサービス) を実行するためのメカニズムを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-150">You must provide a mechanism for your customer to exercise a DSR (process or service).</span></span></p>
</td>
<td>
<p><span data-ttu-id="8b534-151">顧客には、自分たちのデータのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b534-151">Your customer sees only their personal data.</span></span></p>
</td>
</tr>
<tr class="odd">
<td>
<p><span data-ttu-id="8b534-152"><strong>従業員 - インフォメーション ワーカー</strong></span><span class="sxs-lookup"><span data-stu-id="8b534-152"><strong>Your employee – information worker</strong></span></span></p>
</td>
<td>
<ul>
<li><span data-ttu-id="8b534-153">個人データの表示</span><span class="sxs-lookup"><span data-stu-id="8b534-153">View personal data</span></span> </li>
<li><span data-ttu-id="8b534-154">個人データの修正</span><span class="sxs-lookup"><span data-stu-id="8b534-154">Correct personal data</span></span></li>
<li><span data-ttu-id="8b534-155">個人データの消去</span><span class="sxs-lookup"><span data-stu-id="8b534-155">Erase personal data</span></span> </li>
<li><span data-ttu-id="8b534-156">処理するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="8b534-156">Object to processing</span></span></li>
<li><span data-ttu-id="8b534-157">個人データをエクスポート</span><span class="sxs-lookup"><span data-stu-id="8b534-157">Export personal data</span></span></li></ul>
</td>
<td>
<p><span data-ttu-id="8b534-158">作業者が DSR (プロセスまたはサービス) を実行するためのメカニズムを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-158">You must provide a mechanism for your worker to exercise a DSR (process or service).</span></span> <span data-ttu-id="8b534-159">一部のアクティビティ情報は、Microsoft から入手できます</span><span class="sxs-lookup"><span data-stu-id="8b534-159">Some activity information may be obtained from Microsoft</span></span></p>
</td>
<td>
<p><span data-ttu-id="8b534-160">インフォメーション ワーカーには、自分たちのデータのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b534-160">Your information worker sees only their personal data.</span></span></p>
</td>
</tr>
<tr class="odd">
<td>
<p><span data-ttu-id="8b534-161"><strong>従業員 - GDPR 管理者</strong></span><span class="sxs-lookup"><span data-stu-id="8b534-161"><strong>Your employee – GDPR administrator</strong></span></span></p>
</td>
<td>
<ul>
<li><span data-ttu-id="8b534-162">ユーザー ID 要求の検証</span><span class="sxs-lookup"><span data-stu-id="8b534-162">Validates the user identity request</span></span>  </li>
<li><span data-ttu-id="8b534-163">システムでの個人データの検索</span><span class="sxs-lookup"><span data-stu-id="8b534-163">Locates the personal data across systems</span></span> </li>
<li><span data-ttu-id="8b534-164">ポリシーに基づいてデータを調整する</span><span class="sxs-lookup"><span data-stu-id="8b534-164">Curates the data based on your policy</span></span></li>
<li><span data-ttu-id="8b534-165">データ パッケージを作成するか、アクションを実行する</span><span class="sxs-lookup"><span data-stu-id="8b534-165">Creates a data package or executes an action</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="8b534-166">Dynamics 365 for Finance and Operations を使用して、データを特定し、要求を満たします。</span><span class="sxs-lookup"><span data-stu-id="8b534-166">Uses Dynamics 365 for Finance and Operations to locate the data and fulfill the request.</span></span> </li>
<li><span data-ttu-id="8b534-167">カスタマイズを記述します。</span><span class="sxs-lookup"><span data-stu-id="8b534-167">Writes a customization.</span></span></li>
<li><span data-ttu-id="8b534-168">サード パーティに共有コントローラー DSR を求めます。</span><span class="sxs-lookup"><span data-stu-id="8b534-168">Reaches out to third parties for shared-controller DSRs.</span></span></li>
<li><span data-ttu-id="8b534-169">Microsoft にアクティビティ データを求めます。</span><span class="sxs-lookup"><span data-stu-id="8b534-169">Reaches out to Microsoft for activity data.</span></span></li> 
</ul>
</td>
<td>
<p><span data-ttu-id="8b534-170">GDRP 管理者は、DSR 要求を満たすために取得したデータを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b534-170">Your GDRP administrator sees the data that has been obtained to fulfill the DSR request.</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="responding-to-requests-to-view-correct-erase-object-or-export-personal-data"></a><span data-ttu-id="8b534-171">個人データを表示、修正、消去、却下、またはエクスポートする要求に対応</span><span class="sxs-lookup"><span data-stu-id="8b534-171">Responding to requests to view, correct, erase, object, or export personal data</span></span>

<span data-ttu-id="8b534-172">顧客は、自分の個人データが組織によって管理されることを理解する必要があると判断したとします。</span><span class="sxs-lookup"><span data-stu-id="8b534-172">Suppose that a customer decides that he or she wants to understand what personal data of theirs is maintained by an organization.</span></span> <span data-ttu-id="8b534-173">その顧客は、その組織に近づき、自分の DSR を実行するよう求めます。</span><span class="sxs-lookup"><span data-stu-id="8b534-173">That customer approaches that organization and asks to exercise his or her DSR.</span></span> <span data-ttu-id="8b534-174">データ主体が自分たちの DSR 行使するとき、コント ローラーは次の各項目に具体的に対処する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-174">When data subjects exercise their DSRs, controllers must address each of the following items specifically:</span></span>

+ <span data-ttu-id="8b534-175">データ件名が自身の要求の一部として与えた情報を使用してユーザーとロール (ユーザーは従業員、顧客、仕入先ですか?) を適切に識別します。</span><span class="sxs-lookup"><span data-stu-id="8b534-175">Properly identify the person and role (is the person an employee, a customer, a vendor?) by using information that the data subject gave you as part of his or her request.</span></span> <span data-ttu-id="8b534-176">この情報は、名前、従業員 ID や顧客番号、または別の識別子である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-176">This information might be a name, an employee ID or customer number, or another identifier.</span></span>
+ <span data-ttu-id="8b534-177">データ主体が EU 国 (または英国 [UK]) の居住者または市民であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b534-177">Confirm that the data subject is a resident or citizen of an EU nation (or the United Kingdom [UK]).</span></span>
+ <span data-ttu-id="8b534-178">要求の日時を記録します。</span><span class="sxs-lookup"><span data-stu-id="8b534-178">Record the data and time of the request.</span></span> <span data-ttu-id="8b534-179">(要求を完了するまでに 30 日あります。)</span><span class="sxs-lookup"><span data-stu-id="8b534-179">(You have 30 days to complete the request.)</span></span>
+ <span data-ttu-id="8b534-180">DSR 要求が適切かつ有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b534-180">Affirm that the DSR request is proper and valid.</span></span> <span data-ttu-id="8b534-181">法律顧問と連携して、有効な内容を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-181">You will need to work with your legal counsel to determine what is valid.</span></span> <span data-ttu-id="8b534-182">たとえば、DSR 要求のコンプライアンスが、ユーザーのその他の法的義務と競合しないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-182">For example, you must make sure that compliance with a DSR request doesn't conflict with any other legal obligations that you have.</span></span>
+ <span data-ttu-id="8b534-183">要求に関連する情報があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b534-183">Verify that you have the information that is related to the request.</span></span>

### <a name="reasons-why-certain-personal-data-may-not-be-modified-or-deleted"></a><span data-ttu-id="8b534-184">特定の個人データを変更または削除できない理由</span><span class="sxs-lookup"><span data-stu-id="8b534-184">Reasons why certain personal data may not be modified or deleted</span></span>

<span data-ttu-id="8b534-185">次のテーブルは、特定のシナリオで個人データの変更または削除が制限される理由を示しています。</span><span class="sxs-lookup"><span data-stu-id="8b534-185">The following table lists several reasons why personal data modification or deletion is restricted in certain scenarios.</span></span>

| <span data-ttu-id="8b534-186">理由</span><span class="sxs-lookup"><span data-stu-id="8b534-186">Reason</span></span> | <span data-ttu-id="8b534-187">コメント</span><span class="sxs-lookup"><span data-stu-id="8b534-187">Comment</span></span> |
|--------|---------|
| <span data-ttu-id="8b534-188">財務、税金、一般会計原則 (GAAP)</span><span class="sxs-lookup"><span data-stu-id="8b534-188">Financial, tax, generally accepted accounting principles (GAAP)</span></span> | <span data-ttu-id="8b534-189">関係者を削除することはできませんが、関係者の名前は更新できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-189">A party can't be deleted, but the party's name can be updated.</span></span> |
| <span data-ttu-id="8b534-190">財務、税、GAAP</span><span class="sxs-lookup"><span data-stu-id="8b534-190">Financial, tax, GAAP</span></span> | <span data-ttu-id="8b534-191">現在の作業者のデータは削除できませんが、作業者の名前を更新することはできます。</span><span class="sxs-lookup"><span data-stu-id="8b534-191">A current worker's data can't be deleted, but the worker's name can be updated.</span></span> | 
| <span data-ttu-id="8b534-192">GAAP</span><span class="sxs-lookup"><span data-stu-id="8b534-192">GAAP</span></span> | <span data-ttu-id="8b534-193">転記済または完了済みトランザクションは変更できません。</span><span class="sxs-lookup"><span data-stu-id="8b534-193">Posted or completed transactions can't be modified.</span></span> |


### <a name="right-to-view"></a><span data-ttu-id="8b534-194">表示するには右</span><span class="sxs-lookup"><span data-stu-id="8b534-194">Right to view</span></span>

<span data-ttu-id="8b534-195">組織は、データを表示する DSR 要求に応じて、次のアクションのいずれかを決定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-195">An organization might decide to take any of the following actions in response to a DSR request to view data:</span></span>

+ <span data-ttu-id="8b534-196">担当者検索レポートを使用して、個人データを検索および収集します。</span><span class="sxs-lookup"><span data-stu-id="8b534-196">Use the Person search report to find and collect personal data.</span></span> <span data-ttu-id="8b534-197">このレポートは今後のリリースに使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-197">This report will be available in an upcoming release.</span></span>
+ <span data-ttu-id="8b534-198">新しいエンティティを作成または既存のエンティティを拡張して、担当者検索レポートを拡張します。</span><span class="sxs-lookup"><span data-stu-id="8b534-198">Extend the Person search report by authoring a new entity or extending an existing entity.</span></span>
+ <span data-ttu-id="8b534-199">検索機能とフィルター機能を使用して特定の個人データを検索し、そのデータを Microsoft Office のエクスポート機能を使用してエクスポートするか、ブラウザ拡張機能を使用して .pdf に印刷します。</span><span class="sxs-lookup"><span data-stu-id="8b534-199">Use search and filter features to find specific personal data and export that data by using the Microsoft Office Export functionality or print that information to a .pdf using browser extensions.</span></span>
+ <span data-ttu-id="8b534-200">提供されたドキュメントを使用して、コントローラーが個人データとして識別したデータを含むデータ テーブルを識別します。</span><span class="sxs-lookup"><span data-stu-id="8b534-200">Use provided documentation to identify data tables that contain data that the controller has identified as personal data.</span></span>
+ <span data-ttu-id="8b534-201">個人データを検索してエクスポートするカスタム フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b534-201">Author a custom form that locates and exports personal data.</span></span>
+ <span data-ttu-id="8b534-202">認証された顧客が個人データを見ることを可能にする外部ポータルまたは Web サイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b534-202">Author an external portal or website that allows an authenticated customer to see his or her personal data.</span></span>

<span data-ttu-id="8b534-203">Finance and Operations の将来のリリースで使用できる担当者検索レポートは、DSR 要求の対象となる個人データを検出するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8b534-203">The Person search report, which will be available in a future release of Finance and Operations, might help you discover personal data that is subject to a DSR request.</span></span> <span data-ttu-id="8b534-204">レポートに探している情報が含まれていない場合は、情報が載っている修正プログラムの Microsoft Dynamics Lifecycle Services (LCS) サイトを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b534-204">If the report doesn't include the information that you're looking for, check the Microsoft Dynamics Lifecycle Services (LCS) site for possible hotfixes that include the information.</span></span> <span data-ttu-id="8b534-205">また、追加エンティティを作成、または提供されたエンティティを拡張することにより、レポートを自分で拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-205">You can also extend the report yourself by creating additional entities, or extending the provided entities.</span></span>

<span data-ttu-id="8b534-206">担当者検索レポートに、データの件名を要求しているすべての情報が含まれていない場合、Microsoft が提供するツールを使用して拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-206">If the Person search report doesn't contain all the information that the data subject is requesting, you can extend it by using tools that Microsoft has provided.</span></span> <span data-ttu-id="8b534-207">個人検索レポートを拡張する方法の詳細については、[個人検索レポートを拡張](./gdpr-extend-person-search-report.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b534-207">For information about how to extend the Person search report, see [Extend the Person search report](./gdpr-extend-person-search-report.md).</span></span>

### <a name="right-to-correct-"></a><span data-ttu-id="8b534-208">修正するには右\* \*\*</span><span class="sxs-lookup"><span data-stu-id="8b534-208">Right to correct\* \*\*</span></span>

<span data-ttu-id="8b534-209">組織は、データを修正するための DSR 要求に応じて、次のいずれかのアクションを実行することを決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-209">An organization might decide to take any of the following actions in response to a DSR request to correct data:</span></span>

+ <span data-ttu-id="8b534-210">担当者検索レポートを使用して、個人データを検索および収集します。</span><span class="sxs-lookup"><span data-stu-id="8b534-210">Use the Person search report to find and collect personal data.</span></span> <span data-ttu-id="8b534-211">このレポートは今後のリリースに使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-211">This report will be available in an upcoming release.</span></span>
+ <span data-ttu-id="8b534-212">新しいエンティティを作成または既存のエンティティを拡張して、担当者検索レポートを拡張します。</span><span class="sxs-lookup"><span data-stu-id="8b534-212">Extend the Person search report by authoring a new entity or extending an existing entity.</span></span>
+ <span data-ttu-id="8b534-213">特定の個人データを検索するには、検索機能とフィルター機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b534-213">Use search and filter features to find specific personal data.</span></span>
+ <span data-ttu-id="8b534-214">個人データを検索するカスタム フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b534-214">Author a custom form that locates personal data.</span></span>
+ <span data-ttu-id="8b534-215">認証された顧客が個人データを修正することを可能にする外部ポータルまたは Web サイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b534-215">Author an external portal or website that allows an authenticated customer to correct his or her personal data.</span></span>

<span data-ttu-id="8b534-216">データが特定されたら、製品内機能を使用して、製品が実行するための機能を提供する場所でデータを修正します。</span><span class="sxs-lookup"><span data-stu-id="8b534-216">When data is located, use in-product features to correct the data where the product offers the ability to do so.</span></span>

<span data-ttu-id="8b534-217">\*個人データと見なされるデータの中には、直接変更することができないものもあります。</span><span class="sxs-lookup"><span data-stu-id="8b534-217">\*You might find that some data that qualifies as personal data can't be modified directly.</span></span> <span data-ttu-id="8b534-218">このデータは通常、財務法 (税法など)、詐欺防止 (セキュリティ監査証跡)、または業界認定への準拠のために「現状のまま」保たれる金融取引やその他の業務データの一部です 。</span><span class="sxs-lookup"><span data-stu-id="8b534-218">Typically, this data is part of a financial transaction or other business data that is kept "as is" for compliance with financial laws (for example, tax laws), prevention of fraud (such as security audit trail), or compliance with industry certifications.</span></span>

<span data-ttu-id="8b534-219">\** GDPR は他のすべての法律を排除する法律ではありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-219">\** GDPR is not a law exclusive of all other laws.</span></span> <span data-ttu-id="8b534-220">エンタープライズ リソース プラン システムとして、Finance and Operations は特定のビジネスまたはトランザクション データの変更を許可していません。他の法律や認証のコンプライアンスに必要なビジネス データの変更のための機能を提供しておらず一切保証もしません。</span><span class="sxs-lookup"><span data-stu-id="8b534-220">As an enterprise resource planning system, Finance and Operations does not allow for modification of certain business or transactional data, and will not endorse nor provide functionality for the modification of business data that is necessary for compliance with other laws or certifications.</span></span> <span data-ttu-id="8b534-221">Finance and Operations は、参照の破損またはビジネス データの整合性が生じる変更/カスタマイズまたはその他のアクションに対して、サポートを提供しません。</span><span class="sxs-lookup"><span data-stu-id="8b534-221">Finance and Operations will not provide support for modifications/customizations or other actions that result in the corruption of referential or business data integrity.</span></span>


### <a name="right-to-be-forgotten"></a><span data-ttu-id="8b534-222">消去するには右\*</span><span class="sxs-lookup"><span data-stu-id="8b534-222">Right to be forgotten\*</span></span>

<span data-ttu-id="8b534-223">組織は、消去データの DSR 要求に応じて、次のアクションのいずれかを決定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-223">An organization might decide to take any of the following actions in response to a DSR request to erase data:</span></span>

+ <span data-ttu-id="8b534-224">製品が直接アクションを有効にする場所では、個人データを削除するか消去してください。</span><span class="sxs-lookup"><span data-stu-id="8b534-224">Delete or otherwise erase personal data where the product enables that action directly.</span></span>
+ <span data-ttu-id="8b534-225">Finance and Operations が直接アクションを有効にする場合、個人データを匿名にします。</span><span class="sxs-lookup"><span data-stu-id="8b534-225">Anonymize the personal data where Finance and Operations enables that action directly.</span></span>
+ <span data-ttu-id="8b534-226">個人データを消去または変更するカスタマイズを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b534-226">Author a customization to erase/modify the personal data.</span></span>

<span data-ttu-id="8b534-227">\* GDPR は他のすべての法律を排除する法律ではありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-227">\* GDPR is not a law exclusive of all other laws.</span></span> <span data-ttu-id="8b534-228">エンタープライズ リソース プラン システムとして、Finance and Operations は特定のビジネスまたはトランザクション データの削除を許可していません。他の法律や認証のコンプライアンスのために必要なビジネス データの削除機能を提供しておらず一切保証もしません。</span><span class="sxs-lookup"><span data-stu-id="8b534-228">As an enterprise resource planning system, Finance and Operations does not allow for deletion of certain business or transactional data, and will not endorse nor provide functionality for the deletion of business data that is necessary for compliance with other laws or certifications.</span></span> <span data-ttu-id="8b534-229">Finance and Operations は、参照の破損またはビジネス データの整合性が生じる変更/カスタマイズまたはその他のアクションに対して、サポートを提供しません。</span><span class="sxs-lookup"><span data-stu-id="8b534-229">Finance and Operations will not provide support for modifications/customizations or other actions that result in the corruption of referential or business data integrity.</span></span>

### <a name="right-to-port"></a><span data-ttu-id="8b534-230">移植するには右</span><span class="sxs-lookup"><span data-stu-id="8b534-230">Right to port</span></span>

<span data-ttu-id="8b534-231">組織は、ポート データの DSR 要求に応じて、次のアクションのいずれかを決定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-231">An organization might decide to take any of the following actions in response to a DSR request to port data:</span></span>

+ <span data-ttu-id="8b534-232">Microsoft Office アドインを使用して、個人データをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="8b534-232">Use the Microsoft Office Add-in to export personal data.</span></span>
+ <span data-ttu-id="8b534-233">個人データのエクスポートを可能にするカスタム レポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b534-233">Author a custom report that enables the export of personal data.</span></span>
+ <span data-ttu-id="8b534-234">個人データをエクスポートするカスタマイズを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b534-234">Author a customization that exports personal data.</span></span>
+ <span data-ttu-id="8b534-235">人物検索レポートを使用または拡張して、データ対象者の個人情報のコピー要求に役立つ情報を収集します。</span><span class="sxs-lookup"><span data-stu-id="8b534-235">Use or extend the Person search report to gather information in support of a request for a copy of the data subject's personal information.</span></span>

<span data-ttu-id="8b534-236">担当者検索レポート。DSR 要求の対象となる個人データを検索および収集できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-236">The Person search report, which might help you discover personal data that is subject to a DSR request.</span></span> <span data-ttu-id="8b534-237">レポートに探している情報が含まれていない場合は、情報が載っている修正プログラムの LCS サイトを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b534-237">If the report doesn't include the information that you're looking for, check the LCS site for possible hotfixes that include the information.</span></span> <span data-ttu-id="8b534-238">また、追加エンティティを作成することにより自分でレポートを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-238">You can also extend the report yourself by creating additional entities.</span></span>

<span data-ttu-id="8b534-239">担当者検索レポートに、データの件名を要求しているすべての情報が含まれていない場合、Microsoft が提供するツールを使用して拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-239">If the Person search report doesn't contain all the information that the data subject is requesting, you can extend it by using tools that Microsoft has provided.</span></span> <span data-ttu-id="8b534-240">個人検索レポートを拡張する方法の詳細については、[個人検索レポートを拡張](./gdpr-extend-person-search-report.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b534-240">For information about how to extend the Person search report, see [Extend the Person search report](./gdpr-extend-person-search-report.md).</span></span>

<span data-ttu-id="8b534-241">コントローラは、GDPR 内で定義されているようにデータ主体に返されなければならないデータの範囲外にある特定の種類の情報を、独自の裁量で編集することを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-241">The controller may, at their sole discretion choose to redact certain types of information that may fall outside of the scope of data that must be returned to the data subject as defined within the GDPR.</span></span>

## <a name="right-to-restrict"></a><span data-ttu-id="8b534-242">制限するには右</span><span class="sxs-lookup"><span data-stu-id="8b534-242">Right to restrict</span></span>

<span data-ttu-id="8b534-243">組織は、オプションのデータ処理を制限する DSR 要求に応じて、次のアクションのいずれかを決定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-243">An organization might decide to take the following action in response to a DSR request to restrict optional data processing:</span></span>

+ <span data-ttu-id="8b534-244">たとえば、マーケティング キャンペーンから顧客を削除します。</span><span class="sxs-lookup"><span data-stu-id="8b534-244">Remove the customer from, for example, a marketing campaign.</span></span>

<span data-ttu-id="8b534-245">\* GDPR は他のすべての法律を排除する法律ではありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-245">\* GDPR is not a law exclusive of all other laws.</span></span> <span data-ttu-id="8b534-246">エンタープライズ リソース プラン システムとして、Finance and Operations は特定のビジネスまたはトランザクション データの制限された処理を許可していません。他の法律や認証のコンプライアンスに必要なビジネス データの処理の制限に関する機能を提供しておらず一切保証もしません。</span><span class="sxs-lookup"><span data-stu-id="8b534-246">As an enterprise resource planning system, Finance and Operations does not allow for restricted processing of certain business or transactional data, and will not endorse nor provide functionality for the restriction of processing of business data that is necessary for compliance with other laws or certifications.</span></span> <span data-ttu-id="8b534-247">Finance and Operations は、参照の破損またはビジネス データの整合性が生じる変更/カスタマイズまたはその他のアクションに対して、サポートを提供しません。</span><span class="sxs-lookup"><span data-stu-id="8b534-247">Finance and Operations will not provide support for modifications/customizations or other actions that result in the corruption of referential or business data integrity.</span></span>


## <a name="controller-considerations"></a><span data-ttu-id="8b534-248">コントローラーの考慮事項</span><span class="sxs-lookup"><span data-stu-id="8b534-248">Controller considerations</span></span>

<span data-ttu-id="8b534-249">コントローラは、以下の情報を使用して DSR 要求を完了できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-249">Controllers can use the following information to complete DSR requests.</span></span>

#### <a name="system-inventory"></a><span data-ttu-id="8b534-250">システム インベントリ</span><span class="sxs-lookup"><span data-stu-id="8b534-250">System inventory</span></span>

+ <span data-ttu-id="8b534-251">**データの在庫およびタグ付け** - Microsoft は、開発者と顧客が使用できるタグ付けインフラストラクチャを実現しました。</span><span class="sxs-lookup"><span data-stu-id="8b534-251">**Data inventory and tagging** – Microsoft has enabled a tagging infrastructure that developers and customers can use.</span></span> <span data-ttu-id="8b534-252">メタデータに定義されている各データ フィールドには、コントローラーが個人データの定義に適合すると判断したデータを識別するために選択した値または用語を、確認または変更できる推奨値を持つ分類プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b534-252">Each data field that is defined in metadata contains a classification property that has a suggested value that the controller can confirm or change to any value or term they choose in order to identify data that they deem fits within the definition of personal data.</span></span>
+ <span data-ttu-id="8b534-253">**データ フロー ダイアグラム** - Microsoft は、顧客の生産環境におけるシステム間のデータのフローを識別するデータ フロー ダイアグラムを公開します。</span><span class="sxs-lookup"><span data-stu-id="8b534-253">**Data flow diagram** – Microsoft will publish a data flow diagram that identifies flows of data between systems in the customers production environments.</span></span>
+ <span data-ttu-id="8b534-254">**個人検索レポート** – Finance and Operations には、要求者の個人情報のコピーの要求をサポートする情報を収集するために使用できる個人検索レポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b534-254">**Person search report** – Finance and Operations includes the Person search report, which can be used to gather information in support of a request for a copy of the requestor's personal information.</span></span> <span data-ttu-id="8b534-255">(個人検索レポートは、将来のリリースで使用可能になります。)</span><span class="sxs-lookup"><span data-stu-id="8b534-255">(The Person search report will available in a future release.)</span></span>

## <a name="activity-and-diagnostic-information"></a><span data-ttu-id="8b534-256">活動と診断情報</span><span class="sxs-lookup"><span data-stu-id="8b534-256">Activity and diagnostic information</span></span>

<span data-ttu-id="8b534-257">コントローラーは、[Microsoft Enterprise Privacy Portal](https://www.microsoft.com/en-us/trustcenter/privacy) を使用してテレメトリ データに関する DSR 要求を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-257">The controller can make DSR requests regarding telemetry data by using the [Microsoft Enterprise Privacy Portal](https://www.microsoft.com/en-us/trustcenter/privacy).</span></span> <span data-ttu-id="8b534-258">収集された一部のテレメトリ データは匿名化されます。</span><span class="sxs-lookup"><span data-stu-id="8b534-258">Some telemetry data that we collect is pseudonymized.</span></span> <span data-ttu-id="8b534-259">追加情報または支援なしでは、ユーザーの ID は匿名です。</span><span class="sxs-lookup"><span data-stu-id="8b534-259">Without additional information or your assistance, the user's identity is anonymous.</span></span>

## <a name="representation-of-a-person-in-finance-and-operations"></a><span data-ttu-id="8b534-260">Finance and Operations のユーザーの表示</span><span class="sxs-lookup"><span data-stu-id="8b534-260">Representation of a person in Finance and Operations</span></span>

<span data-ttu-id="8b534-261">Finance and Operations には共通の [グローバル アドレス帳](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/overview-global-address-book) があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-261">Finance and Operations has a common [Global address book](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/overview-global-address-book).</span></span> <span data-ttu-id="8b534-262">連絡先、顧客、ユーザー、作業者、または他の担当者をシステムに追加するたびに、通常はアドレス帳にその人物のエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b534-262">Typically, every time that you add a contact, customer, user, worker, or other person in your system, you first create an address book entry for that person.</span></span> <span data-ttu-id="8b534-263">アドレス帳の各ユーザーは関係者と呼ばれ、PartyID が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="8b534-263">Each person in the address book is referred to as a party and is assigned a PartyID.</span></span> <span data-ttu-id="8b534-264">担当者は、顧客、ユーザー、または作業者などのシステム内でのロールも保有して、CustID、UserID、WorkerID などの ロール ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="8b534-264">The person also takes on a role in the system, such as Customer, User, or Worker, and has a role ID: CustID, UserID, WorkerID, and so on.</span></span>

![グローバル アドレス帳のデータ モデル](../media/gdpr-address-data-model.jpg)

### <a name="each-person-is-a-type-of-party"></a><span data-ttu-id="8b534-266">各担当者は、関係者のタイプです。</span><span class="sxs-lookup"><span data-stu-id="8b534-266">Each person is a type of party</span></span>

<span data-ttu-id="8b534-267">関係者レコードに関連付けられているロールは、関係者ロールと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8b534-267">Roles that are associated with party records are referred to as party roles.</span></span> <span data-ttu-id="8b534-268">パーティーの役割はいくつかあり、パーティーの両方のタイプ (個人と組織) に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-268">There are several party roles, and they can be assigned to both party types (person and organization):</span></span>

+ <span data-ttu-id="8b534-269">**顧客** - 他の個人、会社、またはエンティティによって生産される商品やサービスを購入する個人、会社、または他のエンティティ。</span><span class="sxs-lookup"><span data-stu-id="8b534-269">**Customer** – An individual, company, or other entity that purchases goods and services that are produced by other individuals, companies, or entities.</span></span>
+ <span data-ttu-id="8b534-270">**見込顧客** – 組織が提供する商品やサービスに興味がある当事者。</span><span class="sxs-lookup"><span data-stu-id="8b534-270">**Prospect** – A party that might be interested in goods or services an organization provides.</span></span>
+ <span data-ttu-id="8b534-271">**作業者** – 従業員または契約社員のロールを引き受けるか、またはサービスと引き換えに給与が支払われる人。</span><span class="sxs-lookup"><span data-stu-id="8b534-271">**Worker** – A person who assumes the role of an employee or a contractor, or who is paid in exchange for services.</span></span>
+ <span data-ttu-id="8b534-272">**ユーザー** – システムのユーザーになっている人物。</span><span class="sxs-lookup"><span data-stu-id="8b534-272">**User** – A person who is a user of the system.</span></span> <span data-ttu-id="8b534-273">ユーザーは、グローバル アドレス帳で識別されません。</span><span class="sxs-lookup"><span data-stu-id="8b534-273">The user isn't identified in the Global address book.</span></span>
+ <span data-ttu-id="8b534-274">**仕入先** – 支払いと引き換えに、1 社かそれ以上の法人に製品を供給する関係者。</span><span class="sxs-lookup"><span data-stu-id="8b534-274">**Vendor** – A party that supplies products to one or more legal entities in exchange for payment.</span></span>
+ <span data-ttu-id="8b534-275">**競合他社** - 自社が提供する商品やサービスのような商品やサービスを提供する個人や組織。</span><span class="sxs-lookup"><span data-stu-id="8b534-275">**Competitor** – A person or organization that provides goods or services that are like the goods or services that your business provides.</span></span> <span data-ttu-id="8b534-276">すぐに使える Finance and Operations には、競合他社の特定の ID がありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-276">Out of the box, Finance and Operations has no particular identification for competitors.</span></span>
+ <span data-ttu-id="8b534-277">**申請者** - 組織の業務をしたり、組織内の空席の職務を埋めるための正式な書面または電子形式の要求を行う人。</span><span class="sxs-lookup"><span data-stu-id="8b534-277">**Applicant** – A person who makes a formal written or electronic request to work for an organization or fill an open position in it.</span></span>
+ <span data-ttu-id="8b534-278">**連絡先** - 組織の内部または外部のいずれかで、エントリーを作成した個人。</span><span class="sxs-lookup"><span data-stu-id="8b534-278">**Contact** – A person, either inside or outside your organization, that you've created an entry for.</span></span> <span data-ttu-id="8b534-279">このエントリでは、個人の住所、電子メール アドレス、電話や FAX 番号、および Web ページの URL などの情報を保存できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-279">In this entry, you can save information such as the person's street and email addresses, telephone and fax numbers, and webpage URLs.</span></span>

### <a name="the-right-to-view-and-port-its-all-about-the-party"></a><span data-ttu-id="8b534-280">表示する権限およびポート: 関係者に関するすべて</span><span class="sxs-lookup"><span data-stu-id="8b534-280">The right to view and port: It's all about the party</span></span>

<span data-ttu-id="8b534-281">データ主体がコントローラーに申し入れてユーザーの個人データのコピーを要求するとき、そのコントローラーは、個人を説明するデータを特定するためにグローバル アドレス帳情報を使用する選択をすることがあります。</span><span class="sxs-lookup"><span data-stu-id="8b534-281">When a data subject approaches the controller to request a copy of his or her personal data, the controller might choose to use the Global address book information to locate the data that describes the person.</span></span> <span data-ttu-id="8b534-282">このトピックの前の図で説明したように、**人物**は**ロール**を担う**関係者**のタイプです。</span><span class="sxs-lookup"><span data-stu-id="8b534-282">As noted in the illustration earlier in this topic, a **person** is a type of **party** that plays a **role**.</span></span>

<span data-ttu-id="8b534-283">組織によっては、企業間の関係を通じてのみその活動を実施しているため、DSR の義務がそれほど多くありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-283">Some organizations conduct their activities only through business-to-business relationships and will have modest DSR obligations.</span></span> <span data-ttu-id="8b534-284">対照的に、他の組織はビジネスと顧客関係を通じて活動を実施します。</span><span class="sxs-lookup"><span data-stu-id="8b534-284">By contrast, other organizations conduct their activities through business-to-customer relationships.</span></span> <span data-ttu-id="8b534-285">これらの組織は、グローバル アドレス帳や、拡張性、カスタマイズ機能、[Excel で開く](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-edit-excel)操作を使用して、カスタム レポート、カスタム フォーム、カスタム クエリ、カスタム データ エクスポート の各機能を書き込み、ビジネスが顧客から収集するデータなどの特殊なニーズに地対応する、この関連データ リレーションシップを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-285">These organization might choose to use the Global address book and its associative data relationship to write custom reports, custom forms, custom queries, and custom data export features by using the extensibility and customization capabilities and [Open in Excel](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-edit-excel) experiences to serve the specific needs of the kinds of data that their business collects from their customers.</span></span>

## <a name="the-person-search-report"></a><span data-ttu-id="8b534-286">個人検索レポート</span><span class="sxs-lookup"><span data-stu-id="8b534-286">The Person search report</span></span>

<span data-ttu-id="8b534-287">コントローラーをサポートするために、このレポートでは、**データ管理** 作業領域で利用可能な既存のエンティティ モデル レポート機能を改善しています。</span><span class="sxs-lookup"><span data-stu-id="8b534-287">To support the controller, this report offers a refinement of the existing entity model reporting functionality that is available in the **Data management** workspace.</span></span> <span data-ttu-id="8b534-288">**データ管理** ワークスペースは、ほとんどのロールの種類のパッケージ化された表現のコレクションを提供します。</span><span class="sxs-lookup"><span data-stu-id="8b534-288">The **Data management** workspace offers a collection of pre-packaged representations of most role types.</span></span> <span data-ttu-id="8b534-289">これらの表現はエンティティと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8b534-289">These representations are known as entities.</span></span>

> [!Note]
> <span data-ttu-id="8b534-290">担当者検索レポートは、将来のリリースの Finance and Operations、Microsoft Dynamics 365 for Retail、および Microsoft Dynamics 365 for Talent で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-290">The Person search report will be available for Finance and Operations, Microsoft Dynamics 365 for Retail and Microsoft Dynamics 365 for Talent, in a future release.</span></span> <span data-ttu-id="8b534-291">現在、このレポートは Microsoft Dynamics AX 2012 をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="8b534-291">Currently the report does not support Microsoft Dynamics AX 2012.</span></span> 

<span data-ttu-id="8b534-292">エンティティは特定のロールのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="8b534-292">An entity represents an instance of a specific role.</span></span> <span data-ttu-id="8b534-293">データ管理機能を使用すると、コントローラーはエンティティ データをコロン区切り値、コンマ区切り値 (CSV)、セミコロン区切り値、タブ区切り値、Microsoft Excel、XML などの複数の形式にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="8b534-293">The data management functionality lets the controller export entity data to several formats, such as colon-separated values, comma-separated values (CSV), semicolon-separated values, tab-separated values, Microsoft Excel, and XML.</span></span>

<span data-ttu-id="8b534-294">担当者検索レポートは、当事者と関連付けられた**すべて**のロール (および対応するエンティティ) を識別するために使用される当事者 ID を提供することにより、**データ管理**ワークスペースでエンティティ データをエクスポートする追加の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="8b534-294">The Person search report provides additional capabilities in the **Data management** workspace that export entity data by providing a party ID that is used to identify **all** roles (and corresponding entities) that are associated with the party.</span></span> <span data-ttu-id="8b534-295">この機能を使用すると、すべてのエンティティ データとトランザクション データを単一のアクションまたは単一の関係者または複数の関係者のいずれかでエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="8b534-295">This capability lets you export all entity and transaction data in a single action, for either a single party or a collection of parties.</span></span>

<span data-ttu-id="8b534-296">データ主体がコントローラーに申し入れてユーザーの個人データのコピーを要求するとき、そのコントローラーは、個人を説明するデータを特定するためにグローバル アドレス帳情報を使用する選択をすることがあります。</span><span class="sxs-lookup"><span data-stu-id="8b534-296">When a data subject approaches the controller to request a copy of his or her personal data, the controller might choose to use the Global address book information to locate the data that describes the person.</span></span> <span data-ttu-id="8b534-297">このトピックの前の図で説明したように、**人物**は**ロール**を担う**関係者**のタイプです。</span><span class="sxs-lookup"><span data-stu-id="8b534-297">As noted in the illustration earlier in this topic, a **person** is a type of **party** that plays a **role**.</span></span>

<span data-ttu-id="8b534-298">組織によっては、企業間の関係を通じてのみその活動を実施しているため、DSR の義務がそれほど多くありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-298">Some organizations conduct their activities only through business-to-business relationships and will have modest DSR obligations.</span></span> <span data-ttu-id="8b534-299">対照的に、他の組織はビジネスと顧客関係を通じて活動を実施します。</span><span class="sxs-lookup"><span data-stu-id="8b534-299">By contrast, other organizations conduct their activities through business-to-customer relationships.</span></span> <span data-ttu-id="8b534-300">これらの組織は、グローバル アドレス帳や、拡張性、カスタマイズ機能、[Excel で開く](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-edit-excel#how-do-i-add-an-explicit-button-for-a-template-open-in-excel-option)操作を使用して、カスタム レポート、カスタム フォーム、カスタム クエリ、カスタム データ エクスポート の各機能を書き込み、ビジネスが顧客から収集するデータなどの特殊なニーズに地対応する、この関連データ リレーションシップを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-300">These organization might choose to use the Global address book and its associative data relationship to write custom reports, custom forms, custom queries, and custom data export features by using the extensibility and customization capabilities and [Open in Excel](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-edit-excel#how-do-i-add-an-explicit-button-for-a-template-open-in-excel-option) experiences to serve the specific needs of the kinds of data that their business collects from their customers.</span></span>

## <a name="additional-notes-that-apply-to-requests-for-data"></a><span data-ttu-id="8b534-301">データの要求に適用される追加のメモ</span><span class="sxs-lookup"><span data-stu-id="8b534-301">Additional notes that apply to requests for data</span></span>

+ <span data-ttu-id="8b534-302">Management Reporter および Microsoft Power BI プレゼンテーションのデータは、さまざまな財務書類に入力された情報から生成され、レポート目的でそれらのアプリケーションに転送されます。</span><span class="sxs-lookup"><span data-stu-id="8b534-302">Data in Management Reporter and in Microsoft Power BI presentations is generated from the information that is entered in various financial documents and then transferred to those applications for reporting purposes.</span></span> <span data-ttu-id="8b534-303">レポート、Excel にエクスポートおよび個人検索レポートなどのツールを使用して Finance and Operations の財務書類からデータの要求を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-303">Any request for data should be fulfilled from the financial documents in Finance and Operations by using tools such as reports, Export to Excel, and the Person search report.</span></span> <span data-ttu-id="8b534-304">基本機能を変更するカスタマイズを行わなかった場合は、GDPR 要求を満たすために、Management Reporter や Power BI から追加の報告を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-304">You should not need to do additional reporting from Management Reporter or Power BI to fulfill a GDPR request unless you have made customizations that have altered the base functionality.</span></span>
+ <span data-ttu-id="8b534-305">ドキュメントや添付ファイルに含まれる個人用のデータは、レポートに依存しないデータ件名に返す必要もあります。</span><span class="sxs-lookup"><span data-stu-id="8b534-305">Personal data that is included in documents or attachments might also need to be returned to the data subject, independent of any reporting.</span></span>
+ <span data-ttu-id="8b534-306">マスター レコードに関連付けられているトランザクションのデータがある場合は削除できません。</span><span class="sxs-lookup"><span data-stu-id="8b534-306">If a master record has transactional data associated with it, it can't be deleted.</span></span>
+ <span data-ttu-id="8b534-307">同様に、転記済または完了済みのトランザクションは削除できません。</span><span class="sxs-lookup"><span data-stu-id="8b534-307">Similarly, transactions that have been posted or completed can't be deleted.</span></span>

### <a name="reasons-why-finance-and-operations-might-not-support-modifying-or-deleting-data-out-of-the-box"></a><span data-ttu-id="8b534-308">Finance and Operations がそのままではデータの変更と削除をサポートしない理由</span><span class="sxs-lookup"><span data-stu-id="8b534-308">Reasons why Finance and Operations might not support modifying or deleting data out of the box</span></span>

<span data-ttu-id="8b534-309">次のテーブルは、データの変更が制限される理由を示しています。</span><span class="sxs-lookup"><span data-stu-id="8b534-309">The following table lists several reasons why data modifications might be restricted.</span></span>

|<span data-ttu-id="8b534-310">理由</span><span class="sxs-lookup"><span data-stu-id="8b534-310">Reason</span></span> | <span data-ttu-id="8b534-311">コメント</span><span class="sxs-lookup"><span data-stu-id="8b534-311">Comment</span></span> |
|-------|---------|
| <span data-ttu-id="8b534-312">監査</span><span class="sxs-lookup"><span data-stu-id="8b534-312">Audit</span></span> | <span data-ttu-id="8b534-313">コンプライアンスと監査のためにデータを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-313">Data must be preserved for compliance and auditing.</span></span> |
| <span data-ttu-id="8b534-314">計算済</span><span class="sxs-lookup"><span data-stu-id="8b534-314">Calculated</span></span> | <span data-ttu-id="8b534-315">計算されたデータは、計算に含まれるデータを変更することによってのみ変更できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-315">Data that has been calculated can be changed only by changing the data that is included in the calculation.</span></span> |
| <span data-ttu-id="8b534-316">財務、税金、一般会計原則 (GAAP)</span><span class="sxs-lookup"><span data-stu-id="8b534-316">Financial, tax, generally accepted accounting principles (GAAP)</span></span> | <span data-ttu-id="8b534-317">転記済トランザクションは変更または削除できません。</span><span class="sxs-lookup"><span data-stu-id="8b534-317">Posted transactions can't be modified or deleted.</span></span> |
| <span data-ttu-id="8b534-318">インポート ログ</span><span class="sxs-lookup"><span data-stu-id="8b534-318">Import log</span></span> | <span data-ttu-id="8b534-319">コンプライアンスと監査のためにデータを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-319">Data must be preserved for compliance and auditing.</span></span> |

### <a name="what-types-of-personal-data-might-exist-in-the-product"></a><span data-ttu-id="8b534-320">製品に存在する可能性のある個人データの種類</span><span class="sxs-lookup"><span data-stu-id="8b534-320">What types of personal data might exist in the product</span></span>

<span data-ttu-id="8b534-321">会社にデータ要求が送られることを想定してください。</span><span class="sxs-lookup"><span data-stu-id="8b534-321">You should expect data requests to come to your company.</span></span> <span data-ttu-id="8b534-322">データを要求する人を、会社との 1 つまたは場合によっては複数のリレーションシップに分類することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-322">You can categorize the people who request data into one or, in some cases, more than one relationship with your company:</span></span>

+ <span data-ttu-id="8b534-323">顧客</span><span class="sxs-lookup"><span data-stu-id="8b534-323">Customers</span></span> 
+ <span data-ttu-id="8b534-324">仕入先</span><span class="sxs-lookup"><span data-stu-id="8b534-324">Vendors</span></span>
+ <span data-ttu-id="8b534-325">作業者</span><span class="sxs-lookup"><span data-stu-id="8b534-325">Workers</span></span>
+ <span data-ttu-id="8b534-326">ユーザー</span><span class="sxs-lookup"><span data-stu-id="8b534-326">Users</span></span>
+ <span data-ttu-id="8b534-327">倉庫作業者</span><span class="sxs-lookup"><span data-stu-id="8b534-327">Warehouse workers</span></span>
+ <span data-ttu-id="8b534-328">トラック運転手</span><span class="sxs-lookup"><span data-stu-id="8b534-328">Truck drivers</span></span>
+ <span data-ttu-id="8b534-329">見込顧客</span><span class="sxs-lookup"><span data-stu-id="8b534-329">Prospects</span></span>
+ <span data-ttu-id="8b534-330">連絡先</span><span class="sxs-lookup"><span data-stu-id="8b534-330">Contacts</span></span>
+ <span data-ttu-id="8b534-331">応募者</span><span class="sxs-lookup"><span data-stu-id="8b534-331">Applicants</span></span>
+ <span data-ttu-id="8b534-332">競合他社</span><span class="sxs-lookup"><span data-stu-id="8b534-332">Competitors</span></span>

<span data-ttu-id="8b534-333">個人データは、ここにリストされていない他のロールにも含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-333">Personal data might also be contained in other roles that aren't listed here.</span></span> <span data-ttu-id="8b534-334">個人データの入力、表示、編集するために使用される Finance and Operations 内のページは、上記の一覧のほとんどのロールのワークシートで提供されてきました。</span><span class="sxs-lookup"><span data-stu-id="8b534-334">Pages within Finance and Operations used to enter, view or edit personal data have been provided in worksheets for most roles in the preceding list.</span></span> <span data-ttu-id="8b534-335">CustomerSourceの [個人データの検索および管理の参照ドキュメント](https://mbs.microsoft.com/customersource/global/AX/learning/documentation/white-papers/referencedocumentspersonaldata) ページからスプレッドシートを表示したりダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="8b534-335">You can view or download the spreadsheets from the [Reference documents for finding and managing personal data](https://mbs.microsoft.com/customersource/global/AX/learning/documentation/white-papers/referencedocumentspersonaldata) page on CustomerSource.</span></span> 

## <a name="detailed-inventory"></a><span data-ttu-id="8b534-336">詳細な在庫</span><span class="sxs-lookup"><span data-stu-id="8b534-336">Detailed inventory</span></span>

<span data-ttu-id="8b534-337">Finance and Operations を使用する場合は、複数のデータ ストアに存在する大量のデータを生成または収集する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="8b534-337">As you use Finance and Operations, you might find that you generate or collect large amounts of data that resides in multiple data stores.</span></span> <span data-ttu-id="8b534-338">データの格納場所を理解するのに役立つように、データ ストア内のデータごとにデータ マーカーを導入しました。</span><span class="sxs-lookup"><span data-stu-id="8b534-338">To help you make sense of where your data resides, we've introduced a data marker for each piece of data in our data stores.</span></span> <span data-ttu-id="8b534-339">このマーカーは「資産分類」と呼ばれ、Finance and Operations における個人データの識別や追跡に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-339">This marker is called "Asset Classification," and it can be used to identify or track personal data in Finance and Operations.</span></span> <span data-ttu-id="8b534-340">収集するデータは「顧客コンテンツ」として説明されています。</span><span class="sxs-lookup"><span data-stu-id="8b534-340">Any data that you collect has been described as "customer content."</span></span> <span data-ttu-id="8b534-341">一部の顧客コンテンツには個人データが含まれていることがあり、一部の顧客コンテンツはビジネス データを含む場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-341">Some customer content might contain personal data, and some customer content might contain business data.</span></span> <span data-ttu-id="8b534-342">顧客のすべてのコンテンツを個人データとして処理することを選択、または「個人データ」であるとみなす任意のデータを識別して追跡できるように分類を自分で変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-342">You can choose to treat all customer content as personal data, or you can change the classification yourself, so that you can identify and track any data that you feel is considered "Personal Data."</span></span> <span data-ttu-id="8b534-343">Microsoft は既定の分類のセットで指定されてはいますが、選択した分類や識別子を自由に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-343">Although Microsoft has a supplied a set of default classifications, you're free to use any classification or identifiers that you choose.</span></span>

<Link to documentation on how to modify asset classifications>

<Asset Classification table>

<Link to form that prints the full inventory>

![プロパティに AssetClassification フィールドを示しているソリューション エクスプローラー](../media/gdpr-asset-classification-detail-invent-section.jpg)

## <a name="age-gating-preventing-minors-from-using-the-service"></a><span data-ttu-id="8b534-345">年齢ゲーティング: 未成年がサービスを利用できないようにします。</span><span class="sxs-lookup"><span data-stu-id="8b534-345">Age Gating: Preventing minors from using the service</span></span>

### <a name="overview"></a><span data-ttu-id="8b534-346">概要</span><span class="sxs-lookup"><span data-stu-id="8b534-346">Overview</span></span>

<span data-ttu-id="8b534-347">Microsoft は、個人データが収集される Microsoft ソフトウェアのすべてのユーザーが、認証に Microsoft アカウント (MSA) または Microsoft Azure Active Directory (Azure AD) アカウントを使用することを必須とします。</span><span class="sxs-lookup"><span data-stu-id="8b534-347">Microsoft mandates that all users of Microsoft software where personal data is collected must use a Microsoft account (MSA) or Microsoft Azure Active Directory (Azure AD) account for authentication.</span></span> <span data-ttu-id="8b534-348">また、これらのアカウントは、ソフトウェアまたはサービスを使用する未成年者が個人データを使用するためにサービスに対して保護者の同意を得ることを確認するように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-348">Additionally, those accounts must be configured to enable minors who use the software or service to affirm parental consent for the service to use their personal data.</span></span>

### <a name="what-is-this-feature"></a><span data-ttu-id="8b534-349">これはどういう機能ですか ?</span><span class="sxs-lookup"><span data-stu-id="8b534-349">What is this feature?</span></span>

<span data-ttu-id="8b534-350">サービスのテナント管理者としては、Azure AD 年齢ゲーティングまたは MSA 年齢ゲーティングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-350">As the tenant admin of the service, you will be required to set up Azure AD Age Gating and/or MSA age gating.</span></span> <link to azure doc>

<span data-ttu-id="8b534-351">Azure 年齢ゲーティングを使用して設定されていないユーザーは、ユーザーがマイナーでない場合でも、サービスの使用を制限されます。</span><span class="sxs-lookup"><span data-stu-id="8b534-351">Any user who isn't configured by using Azure Age Gating will be restricted from using the service, even if the user isn't a minor.</span></span> <span data-ttu-id="8b534-352">年齢ゲーティングをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b534-352">Age Gating must be configured.</span></span>

<span data-ttu-id="8b534-353">サインイン年齢ゲートを使用して、マイクロソフトのソフトウェアおよびシステムへのアクセスを制限します。</span><span class="sxs-lookup"><span data-stu-id="8b534-353">We will restrict access to our software and systems by using a sign-in age gate.</span></span>

### <a name="how-will-age-gating-work"></a><span data-ttu-id="8b534-354">年齢ゲーティングはどのように機能しますか。</span><span class="sxs-lookup"><span data-stu-id="8b534-354">How will age gating work?</span></span>

<span data-ttu-id="8b534-355">GDPR は、未成年者に保護者の同意がない場合、システムがその未成年者の個人データの処理を停止する必要があることを定めています。</span><span class="sxs-lookup"><span data-stu-id="8b534-355">The GDPR specifies that systems must stop processing a minor's personal data if that minor doesn't have parental consent.</span></span> <span data-ttu-id="8b534-356">同意を付与してから取り消しできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8b534-356">Note that consent can be given and then withdrawn.</span></span> <span data-ttu-id="8b534-357">したがって、ユーザーはシステムに 1 日しかアクセスできず、次の日にアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8b534-357">Therefore, a user might have access to the system one day but not the next.</span></span>

## <a name="privacy-notices-and-user-subject-rights"></a><span data-ttu-id="8b534-358">プライバシーに関する通知およびユーザー件名権限</span><span class="sxs-lookup"><span data-stu-id="8b534-358">Privacy notices and user subject rights</span></span>

### <a name="displaying-your-organizations-user-rights-and-privacy-notice"></a><span data-ttu-id="8b534-359">組織のユーザー権限およびプライバシー通知を表示</span><span class="sxs-lookup"><span data-stu-id="8b534-359">Displaying your organizations user rights and privacy notice</span></span>

<span data-ttu-id="8b534-360">Finance and Operation の**情報**ボックスに、Microsoft のユーザー権利のドキュメントおよび Microsoft のプライバシーと Cookie のドキュメントへのリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b534-360">In the **About** box in Finance and Operation, you will find links to the Microsoft user rights documentation, and to the Microsoft privacy and cookies documentation.</span></span> <span data-ttu-id="8b534-361">また、組織のプライバシーに関する声明にリンクを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-361">You can also add a link to your organization's privacy statement.</span></span>

![資産を示すソリューション エクスプローラー](../media/gdpr-privacy-01-w-note.jpg)

<span data-ttu-id="8b534-363">**システム パラメーター**ページの、Finance and Operations で、システム管理者は、組織のユーザー権限およびプライバシーに関する通知へのリンクを追加できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-363">On the **System parameters** page in Finance and Operations, system administrator can add links to the organization's user rights and privacy notices.</span></span> <span data-ttu-id="8b534-364">通知タイプのいずれかまたは両方に、有効な URL を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8b534-364">You can add a valid URL for one or both notice types.</span></span>

![組織のプライバシーに関する声明にリンクを追加するシステム パラメーター](../media/gdpr-privacy-02.jpg)

<span data-ttu-id="8b534-366">システム パラメーターへの入力が完了したら、次の図に示されているように、組織のプライバシー通知へのリンクが **情報** ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b534-366">When you've completed your entries in the system parameters, the link to your organization's privacy notice will appear in the **About** box, as show in the following illustration.</span></span>

![組織のプライバシーに関する通知へのリンクがある変更詳細ボックス](../media/gdpr-privacy-03-w-note.jpg)

## <a name="clarification-of-the-scope-of-this-content"></a><span data-ttu-id="8b534-368">このコンテンツのスコープの明確化</span><span class="sxs-lookup"><span data-stu-id="8b534-368">Clarification of the scope of this content</span></span>

+ <span data-ttu-id="8b534-369">このドキュメントは、公開日現在の Microsoft が解釈する GDPR の解説です。</span><span class="sxs-lookup"><span data-stu-id="8b534-369">This documentation is a commentary on the GDPR, as Microsoft interprets it, as of the publication date.</span></span> <span data-ttu-id="8b534-370">GDPR に多くの時間を費やしたことにより、その目的と意味について深い思慮を持っていると考えています。</span><span class="sxs-lookup"><span data-stu-id="8b534-370">We have spent a lot of time with the GDPR and believe that we have been thoughtful about its intent and meaning.</span></span> <span data-ttu-id="8b534-371">ただし、GDPR のアプリケーションは非常に個別に異なっており、GDPR のすべての側面および解釈が十分に解決されているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-371">But the application of the GDPR is highly fact-specific, and not all aspects and interpretations of the GDPR are well-settled.</span></span>
+ <span data-ttu-id="8b534-372">このドキュメントは、情報提供のみを目的としたものであり、法的なアドバイスとして、または GDPR がユーザーおよび組織にどのように適用されるかを判断するためには使用できません。</span><span class="sxs-lookup"><span data-stu-id="8b534-372">This documentation is provided for informational purposes only, and should not be relied upon as legal advice or to determine how the GDPR might apply to you and your organization.</span></span> <span data-ttu-id="8b534-373">法的に資格のある専門家と連携して、GDPR、組織への GDPR の具体的な適用方法、およびコンプライアンスをもっとも確実にする方法について検討されることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8b534-373">We encourage you to work with a legally qualified professional to discuss the GDPR, how it applies specifically to your organization, and how to best ensure compliance.</span></span>
+ <span data-ttu-id="8b534-374">Microsoft はこのプレゼンテーションに記載されている情報に関して一切保証せず、明示的、暗示的、または法的に保証することもありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-374">MICROSOFT MAKES NO WARRANTIES, EXPRESS, IMPLIED, OR STATUTORY AS TO THE INFORMATION PROVIDED IN THIS PRESENTATION.</span></span> <span data-ttu-id="8b534-375">このドキュメントは、「現状のまま」で提供されています。</span><span class="sxs-lookup"><span data-stu-id="8b534-375">This documentation is provided "as is."</span></span> <span data-ttu-id="8b534-376">URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="8b534-376">Information and views expressed in this documentation, including URL and other Internet website references, may change without notice.</span></span>
+ <span data-ttu-id="8b534-377">このドキュメントは、Microsoft 製品の知的財産に対する法的権利をお客様に提供するものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b534-377">This documentation does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="8b534-378">内部での参照目的のみの場合、このプレゼンテーションをコピーして使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b534-378">You may copy and use this presentation for your internal, reference purposes only.</span></span>
