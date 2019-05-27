---
title: セキュリティとデータ エンティティ
description: このトピックでは、データ エンティティのセキュリティについて説明します。 データ エンティティはエントリ ポイント セキュリティをサポートするため、ロール ベースのセキュリティ フレームワークによって制御されます。 データ エンティティのエントリ ポイントを権限および職務にマッピングするモデルは、ターゲット シナリオによって異なります。 したがって、データ エンティティでは、統合モードごとに個別のセキュリティ構成が可能です。
author: Sunil-Garg
manager: AnnBe
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 17852
ms.assetid: a9ede141-56fa-4310-997d-aeef184f7a52
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 313cc68ae1622b44fec9aa17511c051613e27f22
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537098"
---
# <a name="security-and-data-entities"></a><span data-ttu-id="1264b-106">セキュリティとデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="1264b-106">Security and data entities</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1264b-107">データ エンティティは拡張可能なデータ セキュリティ (XDS) の概念をサポートしません。</span><span class="sxs-lookup"><span data-stu-id="1264b-107">Data entities do not support the Extensible Data Security (XDS) concepts.</span></span>

## <a name="entry-points"></a><span data-ttu-id="1264b-108">エントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="1264b-108">Entry points</span></span>
<span data-ttu-id="1264b-109">データ エンティティはエントリ ポイントのセキュリティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="1264b-109">Data entities support entry point security.</span></span> <span data-ttu-id="1264b-110">このサポートは、メニュー項目とページのサポートと似ています。</span><span class="sxs-lookup"><span data-stu-id="1264b-110">This support resembles the support that menu items and pages have.</span></span> <span data-ttu-id="1264b-111">セキュリティ モデルを定義する際の柔軟性を高めるため、データ エンティティでは統合モードごとに個別のセキュリティ設定が可能となっています。</span><span class="sxs-lookup"><span data-stu-id="1264b-111">To give you flexibility when you define a security model, data entities allow for a separate security configuration for each integration mode.</span></span> <span data-ttu-id="1264b-112">現在、データ エンティティに対して 2 つのエントリ ポイント/統合モードは識別されます。</span><span class="sxs-lookup"><span data-stu-id="1264b-112">Currently, two entry points/integration modes are identified for a data entity.</span></span>

| <span data-ttu-id="1264b-113">エントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="1264b-113">Entry point</span></span>     | <span data-ttu-id="1264b-114">説明</span><span class="sxs-lookup"><span data-stu-id="1264b-114">Description</span></span>                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1264b-115">データ サービス</span><span class="sxs-lookup"><span data-stu-id="1264b-115">Data services</span></span>   | <span data-ttu-id="1264b-116">エンティティ用の OData サービス (API) を使用できる機能。</span><span class="sxs-lookup"><span data-stu-id="1264b-116">The ability to use OData services (API) for the entity.</span></span>                                                              |
| <span data-ttu-id="1264b-117">データ管理</span><span class="sxs-lookup"><span data-stu-id="1264b-117">Data management</span></span> | <span data-ttu-id="1264b-118">インポート/エクスポートおよびコネクタの統合など、エンティティ用の非同期統合オプションを使用できる機能。</span><span class="sxs-lookup"><span data-stu-id="1264b-118">The ability to use asynchronous integration options for the entity, such as import/export and connector integration.</span></span> |

## <a name="target-scenarios"></a><span data-ttu-id="1264b-119">ターゲット シナリオ</span><span class="sxs-lookup"><span data-stu-id="1264b-119">Target scenarios</span></span>
<span data-ttu-id="1264b-120">データ エンティティは、シナリオの複数のカテゴリをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="1264b-120">Data entities can support multiple categories of scenarios.</span></span> <span data-ttu-id="1264b-121">各カテゴリでは、別々に確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-121">Each category might have to be secured separately.</span></span>

- <span data-ttu-id="1264b-122">**データ管理 (ファイルに基づくインポート/エクスポートなど)** - 通常、データ マネージャーがこれらのシナリオを実行します。</span><span class="sxs-lookup"><span data-stu-id="1264b-122">**Data management (file-based import/export, and so on)** – Typically, a data manager performs these scenarios.</span></span> <span data-ttu-id="1264b-123">これらのシナリオでは、Finance and Operations クライアントの UI から通常アクセスできないデータにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="1264b-123">These scenarios might provide access to data that isn't usually accessible through the UI for the Finance and Operations client.</span></span> <span data-ttu-id="1264b-124">したがって、データ マネージャーがインポート/エクスポート操作のみを実行できるよう、関連ページへのアクセスとは独立してデータ管理シナリオを保護したいと考えることは多くあります。</span><span class="sxs-lookup"><span data-stu-id="1264b-124">Therefore, you will often want to secure data management scenarios independently of access to the related page, so that a data manager can perform only import/export operations.</span></span>
- <span data-ttu-id="1264b-125">**OData 経由の全般的な統合** – 多くの統合シナリオでは、データ エンティティをサービスとして公開する必要があるため、OData (オンライン ストアフロントや製品ライフサイクル管理 \[PLM\] システムなど) を介してデータにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="1264b-125">**General integration via OData** – Many integration scenarios require that data entities be exposed as services, so that data can be accessed via OData (for example, from an online storefront or a Process Lifetime Management \[PLM\] system).</span></span> <span data-ttu-id="1264b-126">多くの場合、この目的のためにページ アクセスとは別に作成されている、データ エンティティへのアクセスを制御する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-126">Often, you will want to control access to data entities that are built for this purpose independently of page access.</span></span> <span data-ttu-id="1264b-127">つまり、Finance and Operations クライアントの UI を使用してアクセス許可を与えることなく、サービス インターフェイスへのアクセスを許可したいとします。</span><span class="sxs-lookup"><span data-stu-id="1264b-127">In other words, you will want to grant access to the service interface without granting access through the Finance and Operations client UI.</span></span>
- <span data-ttu-id="1264b-128">**Microsoft Office 統合 (Excel での編集など)** – Office 統合シナリオでも、OData 経由でアクセスするデータ エンティティが必要です。</span><span class="sxs-lookup"><span data-stu-id="1264b-128">**Microsoft Office integration (Edit in Excel, and so on)** – Office integration scenarios also require that data entities be accessed via OData.</span></span> <span data-ttu-id="1264b-129">ただし、エンドユーザーの観点からは、これらのシナリオは、たとえば Microsoft Excel が一部の編集作業を簡略化するのに使用されるなど、Finance and Operations クライアントの自然の拡張として見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="1264b-129">However, from an end-user perspective, these scenarios can be viewed as a natural extension of the Finance and Operations client, where, for example, Microsoft Excel is used to simplify some editing tasks.</span></span> <span data-ttu-id="1264b-130">したがって、通常、ページ アクセスとは独立して Microsoft Office の統合を保護する理由はありません。</span><span class="sxs-lookup"><span data-stu-id="1264b-130">Therefore, there is usually no reason to secure the Microsoft Office integration independently of page access.</span></span>

## <a name="privilegeduty-mapping"></a><span data-ttu-id="1264b-131">権限/職務権限マッピング</span><span class="sxs-lookup"><span data-stu-id="1264b-131">Privilege/duty mapping</span></span>
<span data-ttu-id="1264b-132">データ エンティティの対象シナリオに応じて、1 つまたは複数の新しい特権を作成し、既存の職務を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-132">Depending on the target scenarios for a data entity, you should create one or more new privileges, and extend existing duties.</span></span> <span data-ttu-id="1264b-133">または、新しい権限をターゲット シナリオ用に特別に作成された職務にマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="1264b-133">Alternatively, you can map the new privileges to duties that are created specifically for the target scenario.</span></span> <span data-ttu-id="1264b-134">この方法は、シナリオに必要なアクセス権以上のアクセス権がユーザーに付与されないようにします。 </span><span class="sxs-lookup"><span data-stu-id="1264b-134">This approach helps guarantee that no user is granted more access than he or she requires for the scenario.</span></span>

<span data-ttu-id="1264b-135">次のテーブルに、作成する必要のある権限を示します。</span><span class="sxs-lookup"><span data-stu-id="1264b-135">The following table shows the privileges that you should create.</span></span> <span data-ttu-id="1264b-136">また、職務にこれらの特権をマップする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="1264b-136">It also explains how you should map these privileges to duties.</span></span> <span data-ttu-id="1264b-137">データ エンティティが複数のシナリオをサポートすることを意図している場合、権限と職務権限マッピングを組み合わせたセットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-137">If your data entity is intended to support more than one scenario, you should create the combined set of privileges and duty mappings.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1264b-138">ターゲット シナリオ</span><span class="sxs-lookup"><span data-stu-id="1264b-138">Target scenario</span></span></th>
<th><span data-ttu-id="1264b-139">権限</span><span class="sxs-lookup"><span data-stu-id="1264b-139">Privileges</span></span></th>
<th><span data-ttu-id="1264b-140">職務マッピング</span><span class="sxs-lookup"><span data-stu-id="1264b-140">Duty mapping</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1264b-141">データ エンティティは、データ管理を目的としています。</span><span class="sxs-lookup"><span data-stu-id="1264b-141">The data entity is intended for data management.</span></span></td>
<td><span data-ttu-id="1264b-142">次の新しい権限を作成します。</span><span class="sxs-lookup"><span data-stu-id="1264b-142">Create the following new privileges:</span></span>
<ul>
<li><span data-ttu-id="1264b-143"><em>&lt;DataEntity&gt;</em><strong>インポート</strong>
</span><span class="sxs-lookup"><span data-stu-id="1264b-143"><em>&lt;DataEntity&gt;</em><strong>Import</strong>
</span></span><ul>
<li><span data-ttu-id="1264b-144">交付 = 作成</span><span class="sxs-lookup"><span data-stu-id="1264b-144">Grant=Create</span></span></li>
<li><span data-ttu-id="1264b-145">IntegrationMode=DataManagement</span><span class="sxs-lookup"><span data-stu-id="1264b-145">IntegrationMode=DataManagement</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1264b-146"><em>&lt;DataEntity&gt;</em><strong>エクスポート</strong>
</span><span class="sxs-lookup"><span data-stu-id="1264b-146"><em>&lt;DataEntity&gt;</em><strong>Export</strong>
</span></span><ul>
<li><span data-ttu-id="1264b-147">付与 = 読み取り</span><span class="sxs-lookup"><span data-stu-id="1264b-147">Grant=Read</span></span></li>
<li><span data-ttu-id="1264b-148">IntegrationMode=DataManagement</span><span class="sxs-lookup"><span data-stu-id="1264b-148">IntegrationMode=DataManagement</span></span></li>
</ul>
</li>
</ul>
</td>
<td><span data-ttu-id="1264b-149">新しい権限を持つ関連データの管理業務を拡張します。</span><span class="sxs-lookup"><span data-stu-id="1264b-149">Extend the relevant data management duties with the new privileges.</span></span> <span data-ttu-id="1264b-150">詳細については、このトピックで後述する「データ管理ロール」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1264b-150">For more information, see the "Data administrator role" section later in this topic.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1264b-151">データ エンティティは、OData を介した一般的な統合を目的としています。</span><span class="sxs-lookup"><span data-stu-id="1264b-151">The data entity is intended for general integration via OData.</span></span></td>
<td><span data-ttu-id="1264b-152">次の新しい権限を作成します。</span><span class="sxs-lookup"><span data-stu-id="1264b-152">Create the following new privileges:</span></span>
<ul>
<li><span data-ttu-id="1264b-153"><em>&lt;DataEntity&gt;</em> <strong>ビュー</strong>
</span><span class="sxs-lookup"><span data-stu-id="1264b-153"><em>&lt;DataEntity&gt;</em><strong>View</strong>
</span></span><ul>
<li><span data-ttu-id="1264b-154">付与 = 読み取り</span><span class="sxs-lookup"><span data-stu-id="1264b-154">Grant=Read</span></span></li>
<li><span data-ttu-id="1264b-155">IntegrationMode=DataServices</span><span class="sxs-lookup"><span data-stu-id="1264b-155">IntegrationMode=DataServices</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1264b-156"><em>&lt;DataEntity&gt;</em><strong>管理</strong>
</span><span class="sxs-lookup"><span data-stu-id="1264b-156"><em>&lt;DataEntity&gt;</em><strong>Maintain</strong>
</span></span><ul>
<li><span data-ttu-id="1264b-157">交付 = 削除</span><span class="sxs-lookup"><span data-stu-id="1264b-157">Grant=Delete</span></span></li>
<li><span data-ttu-id="1264b-158">IntegrationMode=DataServices</span><span class="sxs-lookup"><span data-stu-id="1264b-158">IntegrationMode=DataServices</span></span></li>
</ul>
</li>
</ul>
</td>
<td><span data-ttu-id="1264b-159">統合シナリオの新しい職務を作成し、関連する新しい特権をこれらの職務にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="1264b-159">Create new duties for the integration scenario, and map the relevant new privileges to these duties.</span></span> <span data-ttu-id="1264b-160">詳細については、このトピックで後述する「職務名のガイドライン」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1264b-160">For more information, see the "Duty naming guidelines" section later in this topic.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1264b-161">データ エンティティは、Microsoft Office との統合を目的としています。</span><span class="sxs-lookup"><span data-stu-id="1264b-161">The data entity is intended for Microsoft Office integration.</span></span></td>
<td><span data-ttu-id="1264b-162">次の新しい権限を作成します。</span><span class="sxs-lookup"><span data-stu-id="1264b-162">Create the following new privileges:</span></span>
<ul>
<li><span data-ttu-id="1264b-163"><em>&lt;DataEntity&gt;</em> <strong>ビュー</strong>
</span><span class="sxs-lookup"><span data-stu-id="1264b-163"><em>&lt;DataEntity&gt;</em><strong>View</strong>
</span></span><ul>
<li><span data-ttu-id="1264b-164">付与 = 読み取り</span><span class="sxs-lookup"><span data-stu-id="1264b-164">Grant=Read</span></span></li>
<li><span data-ttu-id="1264b-165">IntegrationMode=DataServices</span><span class="sxs-lookup"><span data-stu-id="1264b-165">IntegrationMode=DataServices</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1264b-166"><em>&lt;DataEntity&gt;</em><strong>管理</strong>
</span><span class="sxs-lookup"><span data-stu-id="1264b-166"><em>&lt;DataEntity&gt;</em><strong>Maintain</strong>
</span></span><ul>
<li><span data-ttu-id="1264b-167">交付 = 削除</span><span class="sxs-lookup"><span data-stu-id="1264b-167">Grant=Delete</span></span></li>
<li><span data-ttu-id="1264b-168">IntegrationMode=DataServices</span><span class="sxs-lookup"><span data-stu-id="1264b-168">IntegrationMode=DataServices</span></span></li>
</ul>
</li>
</ul>
</td>
<td><span data-ttu-id="1264b-169">新しい権限を持つ関連ページへのアクセスを提供する関連する既存の任務を拡張します。</span><span class="sxs-lookup"><span data-stu-id="1264b-169">Extend the relevant existing duties that provide access to the related pages with the new privileges.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1264b-170">前のテーブルで説明されている方法は最小特権の原則に準拠しているため、それを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1264b-170">Because the approach that is described in the preceding table complies with the principle of least privilege, we recommend that you use it.</span></span> <span data-ttu-id="1264b-171">ただし、場合によっては、次のより簡単な方法を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1264b-171">Nevertheless, in some situations, you can use the following simpler approach.</span></span> <span data-ttu-id="1264b-172">ただし、この方法は安全性が低い場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1264b-172">However, be aware that this approach might be less secure.</span></span> <span data-ttu-id="1264b-173">管理および拡張が少し困難になる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="1264b-173">It might also be slightly harder to maintain and extend.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1264b-174">ターゲット シナリオ</span><span class="sxs-lookup"><span data-stu-id="1264b-174">Target scenario</span></span></th>
<th><span data-ttu-id="1264b-175">権限</span><span class="sxs-lookup"><span data-stu-id="1264b-175">Privileges</span></span></th>
<th><span data-ttu-id="1264b-176">職務マッピング</span><span class="sxs-lookup"><span data-stu-id="1264b-176">Duty mapping</span></span></th>
<th><span data-ttu-id="1264b-177">潜在的な問題</span><span class="sxs-lookup"><span data-stu-id="1264b-177">Potential issues</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1264b-178">データ エンティティは、データ管理、OData による一般的な統合、および Microsoft Office との統合を目的としています。</span><span class="sxs-lookup"><span data-stu-id="1264b-178">The data entity is intended for data management, general integration via OData, and Microsoft Office integration.</span></span></td>
<td><span data-ttu-id="1264b-179">次の新しい権限を作成します。</span><span class="sxs-lookup"><span data-stu-id="1264b-179">Create the following new privileges:</span></span>
<ul>
<li><span data-ttu-id="1264b-180"><em>&lt;DataEntity&gt;</em> <strong>ビュー</strong>
</span><span class="sxs-lookup"><span data-stu-id="1264b-180"><em>&lt;DataEntity&gt;</em><strong>View</strong>
</span></span><ul>
<li><span data-ttu-id="1264b-181">付与 = 読み取り</span><span class="sxs-lookup"><span data-stu-id="1264b-181">Grant=Read</span></span></li>
<li><span data-ttu-id="1264b-182">IntegrationMode=All</span><span class="sxs-lookup"><span data-stu-id="1264b-182">IntegrationMode=All</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1264b-183"><em>&lt;DataEntity&gt;</em><strong>管理</strong>
</span><span class="sxs-lookup"><span data-stu-id="1264b-183"><em>&lt;DataEntity&gt;</em><strong>Maintain</strong>
</span></span><ul>
<li><span data-ttu-id="1264b-184">交付 = 削除</span><span class="sxs-lookup"><span data-stu-id="1264b-184">Grant=Delete</span></span></li>
<li><span data-ttu-id="1264b-185">IntegrationMode=All</span><span class="sxs-lookup"><span data-stu-id="1264b-185">IntegrationMode=All</span></span></li>
</ul>
</li>
</ul>
</td>
<td>
<ol>
<li><span data-ttu-id="1264b-186">新しい権限を持つ関連データの管理業務を拡張します。</span><span class="sxs-lookup"><span data-stu-id="1264b-186">Extend the relevant data management duties with the new privileges.</span></span></li>
<li><span data-ttu-id="1264b-187">統合シナリオの新しい職務を作成し、関連する新しい特権をこれらの職務にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="1264b-187">Create new duties for the integration scenario, and map the relevant new privileges to these duties.</span></span></li>
<li><span data-ttu-id="1264b-188">新しい権限を持つ関連ページへのアクセスを提供する関連する既存の任務を拡張します。</span><span class="sxs-lookup"><span data-stu-id="1264b-188">Extend the relevant existing duties that provide access to the related page with the new privileges.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1264b-189">この方法を使用するときは、データのインポート/エクスポートへのアクセス許可を付与されているデータ マネージャーは、システムに Web サービスからもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="1264b-189">When you use this approach, a data manager who is granted access to import/export data can also access the system from a web service.</span></span> <span data-ttu-id="1264b-190">同様に、データ エンティティに関連付けられているページへのアクセスを許可されているユーザーは、Web サービスからでもシステムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="1264b-190">Likewise, a user who is granted access to the page that is associated with a data entity can also access the system from a web service.</span></span> <span data-ttu-id="1264b-191">このユーザーは、関連するデータ管理職務権限が与えられていない場合にのみ、データのインポート/エクスポートが禁止されます。</span><span class="sxs-lookup"><span data-stu-id="1264b-191">This user will be prevented from data import/export only if he or she hasn't been granted the related data management duty.</span></span></td>
</tr>
</tbody>
</table>

## <a name="duty-naming-guidelines"></a><span data-ttu-id="1264b-192">職務名のガイドライン</span><span class="sxs-lookup"><span data-stu-id="1264b-192">Duty naming guidelines</span></span>
<span data-ttu-id="1264b-193">特定の統合シナリオのデータ エンティティを作成するとき、個別の職務も作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-193">When you create data entities for specific integration scenarios, you should also create separate duties.</span></span> <span data-ttu-id="1264b-194">これらの任務は、外部アプリケーションまたはサービスに、データ エンティティへの必要なアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="1264b-194">These duties grant the external application or service the required access to the data entities.</span></span> <span data-ttu-id="1264b-195">作成する職務は、Dynamics 365 for Finance and Operations クライアント UI を介してアクセスするための対応する職務と同じ命名規則に従ってください。</span><span class="sxs-lookup"><span data-stu-id="1264b-195">The duties that you create should follow the same naming guidelines as the corresponding duties that provide access through the Dynamics 365 for Finance and Operations client UI.</span></span> <span data-ttu-id="1264b-196">ただし、「サービスを使用する」接尾辞を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-196">However, you should add a "using services" suffix.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1264b-197">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="1264b-197">Duty type</span></span></th>
<th><span data-ttu-id="1264b-198">職務オブジェクト名の接尾語</span><span class="sxs-lookup"><span data-stu-id="1264b-198">Duty object name suffix</span></span></th>
<th><span data-ttu-id="1264b-199">職務名のテンプレート</span><span class="sxs-lookup"><span data-stu-id="1264b-199">Duty name template</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1264b-200">有効化</span><span class="sxs-lookup"><span data-stu-id="1264b-200">Enable</span></span></td>
<td><span data-ttu-id="1264b-201">…IntegrationEnable</span><span class="sxs-lookup"><span data-stu-id="1264b-201">…IntegrationEnable</span></span></td>
<td><span data-ttu-id="1264b-202">有効化 …</span><span class="sxs-lookup"><span data-stu-id="1264b-202">Enable …</span></span> <span data-ttu-id="1264b-203">サービスの使用</span><span class="sxs-lookup"><span data-stu-id="1264b-203">using services</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1264b-204">レコード</span><span class="sxs-lookup"><span data-stu-id="1264b-204">Record</span></span></td>
<td><span data-ttu-id="1264b-205">…IntegrationMaintain</span><span class="sxs-lookup"><span data-stu-id="1264b-205">…IntegrationMaintain</span></span></td>
<td><span data-ttu-id="1264b-206">メンテナンス …</span><span class="sxs-lookup"><span data-stu-id="1264b-206">Maintain …</span></span> <span data-ttu-id="1264b-207">サービスの使用</span><span class="sxs-lookup"><span data-stu-id="1264b-207">using services</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1264b-208">認証する</span><span class="sxs-lookup"><span data-stu-id="1264b-208">Authorize</span></span></td>
<td><span data-ttu-id="1264b-209">…IntegrationApprove (リリース、確認、仕分入力)</span><span class="sxs-lookup"><span data-stu-id="1264b-209">…IntegrationApprove (Release, Confirm, Journalize)</span></span></td>
<td><span data-ttu-id="1264b-210">承認 (リリース、確認、仕訳入力) …</span><span class="sxs-lookup"><span data-stu-id="1264b-210">Approve (Release, Confirm, Journalize) …</span></span> <span data-ttu-id="1264b-211">サービスの使用</span><span class="sxs-lookup"><span data-stu-id="1264b-211">using services</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1264b-212">照会</span><span class="sxs-lookup"><span data-stu-id="1264b-212">Inquire</span></span></td>
<td><span data-ttu-id="1264b-213">…IntegrationInquire</span><span class="sxs-lookup"><span data-stu-id="1264b-213">…IntegrationInquire</span></span></td>
<td><span data-ttu-id="1264b-214">照会先 …</span><span class="sxs-lookup"><span data-stu-id="1264b-214">Inquire into …</span></span> <span data-ttu-id="1264b-215">サービスの使用</span><span class="sxs-lookup"><span data-stu-id="1264b-215">using services</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1264b-216">これらのガイドラインに従う職務権限名の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1264b-216">Here are some examples of duty names that follow these guidelines:</span></span>

- <span data-ttu-id="1264b-217">サービスを使用した工順マスターの管理</span><span class="sxs-lookup"><span data-stu-id="1264b-217">Maintain route master using service</span></span>
- <span data-ttu-id="1264b-218">サービスを使用しているケース進捗状況の照会</span><span class="sxs-lookup"><span data-stu-id="1264b-218">Inquire into case progress using services</span></span>

## <a name="data-administrator-role"></a><span data-ttu-id="1264b-219">データ管理者ロール</span><span class="sxs-lookup"><span data-stu-id="1264b-219">Data administrator role</span></span>
<span data-ttu-id="1264b-220">**DataManagementApplicationAdministrator** セキュリティ ロールによって、関連したユーザーが **データ管理** ワークスペースでフル インポート/エクスポート機能を実行できます。</span><span class="sxs-lookup"><span data-stu-id="1264b-220">The **DataManagementApplicationAdministrator** security role enables an associated user to have full import/export capabilities in the **Data management** workspace.</span></span> <span data-ttu-id="1264b-221">このセキュリティ ロールには、5 つのデータ エンティティ カテゴリに割り当てられた 2 つのセキュリティ職務があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-221">This security role has two security duties for each of the five data entity categories that are assigned to it.</span></span> <span data-ttu-id="1264b-222">1 つの関税は、関連するカテゴリのデータ エンティティを介してデータをインポートすることであり、1 つは関連するカテゴリのデータ エンティティを介してデータをエクスポートすることです。</span><span class="sxs-lookup"><span data-stu-id="1264b-222">One duty is for importing data via data entities of the associated category, and one for exporting data via data entities of the associated category.</span></span> <span data-ttu-id="1264b-223">したがって、このセキュリティ ロールには合計 10 のセキュリティ義務が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1264b-223">Therefore, a total of 10 security duties are assigned to this security role:</span></span>

- <span data-ttu-id="1264b-224">DataManagementApplicationDocumentEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="1264b-224">DataManagementApplicationDocumentEntitiesMaintain</span></span>
- <span data-ttu-id="1264b-225">DataManagementApplicationDocumentEntitiesView</span><span class="sxs-lookup"><span data-stu-id="1264b-225">DataManagementApplicationDocumentEntitiesView</span></span>
- <span data-ttu-id="1264b-226">DataManagementApplicationMasterEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="1264b-226">DataManagementApplicationMasterEntitiesMaintain</span></span>
- <span data-ttu-id="1264b-227">DataManagementApplicationMasterEntitiesView</span><span class="sxs-lookup"><span data-stu-id="1264b-227">DataManagementApplicationMasterEntitiesView</span></span>
- <span data-ttu-id="1264b-228">DataManagementApplicationParametersEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="1264b-228">DataManagementApplicationParametersEntitiesMaintain</span></span>
- <span data-ttu-id="1264b-229">DataManagementApplicationParametersEntitiesView</span><span class="sxs-lookup"><span data-stu-id="1264b-229">DataManagementApplicationParametersEntitiesView</span></span>
- <span data-ttu-id="1264b-230">DataManagementApplicationReferenceEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="1264b-230">DataManagementApplicationReferenceEntitiesMaintain</span></span>
- <span data-ttu-id="1264b-231">DataManagementApplicationReferenceEntitiesView</span><span class="sxs-lookup"><span data-stu-id="1264b-231">DataManagementApplicationReferenceEntitiesView</span></span>
- <span data-ttu-id="1264b-232">DataManagementApplicationTransactionEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="1264b-232">DataManagementApplicationTransactionEntitiesMaintain</span></span>
- <span data-ttu-id="1264b-233">DataManagementApplicationTransactionEntitiesView</span><span class="sxs-lookup"><span data-stu-id="1264b-233">DataManagementApplicationTransactionEntitiesView</span></span>

<span data-ttu-id="1264b-234">**データ管理** ワークスペースで使用できるデータ エンティティを作成するとき、データ エンティティで指定される **エンティティ カテゴリ** プロパティに基づいて、新しいセキュリティ権限を持つこれらの職務を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-234">When you create data entities that can be used in the **Data management** workspace, you must extend these duties with the new security privileges, based on the **Entity Category** property that is specified on the data entity.</span></span> <span data-ttu-id="1264b-235">(新しいセキュリティ権限を使用して職務を拡張する方法については、このトピックの前半の「特権/職務マッピング」セクションを参照してください。)また、職務を使用して、特定のデータ管理シナリオ用の新しいロールを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="1264b-235">(For information about how to extend duties with the new security privileges, see the "Privilege/duty mapping" section earlier in this topic.) You can also use the duties to create new roles for specific data management scenarios.</span></span>

## <a name="modeling-new-entry-point-security-in-the-application-explorer"></a><span data-ttu-id="1264b-236">アプリケーション エクスプローラーでの新しいエントリ ポイント セキュリティのモデリング</span><span class="sxs-lookup"><span data-stu-id="1264b-236">Modeling new entry point security in the Application Explorer</span></span>
<span data-ttu-id="1264b-237">セキュリティのモデリングのパターンは、エントリ ポイントに対する権限を持つセキュリティのモデリングのパターンと似ています。</span><span class="sxs-lookup"><span data-stu-id="1264b-237">The pattern for modeling security resembles the pattern for modeling security with privileges on an entry point.</span></span> <span data-ttu-id="1264b-238">セキュリティをモデル化するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1264b-238">To model security, follow these steps.</span></span>

1. <span data-ttu-id="1264b-239">新しい権限の作成を作成します。</span><span class="sxs-lookup"><span data-stu-id="1264b-239">Create a new privilege.</span></span>
2. <span data-ttu-id="1264b-240">新しいデータ エンティティのアクセス許可を作成します。</span><span class="sxs-lookup"><span data-stu-id="1264b-240">Create new data entity permissions.</span></span>
3. <span data-ttu-id="1264b-241">**名前** を **データ エンティティ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1264b-241">Set the **Name** to **Data Entity**.</span></span>
4. <span data-ttu-id="1264b-242">**アクセス レベル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1264b-242">Select the **Access Level**.</span></span>
5. <span data-ttu-id="1264b-243">**統合モード**を選択します (すべて &gt; データ サービス &gt; データ管理)。</span><span class="sxs-lookup"><span data-stu-id="1264b-243">Select **Integration Mode** (All &gt; Data Services &gt; Data Management).</span></span> <span data-ttu-id="1264b-244">これは、オブジェクトの種類のデータ エンティティに固有です。</span><span class="sxs-lookup"><span data-stu-id="1264b-244">This is specific to Object Type: Data Entity.</span></span>

    - <span data-ttu-id="1264b-245">**すべて** - OData とデータのインポート/エクスポートの両方に適用される同じセキュリティ設定を適用します。</span><span class="sxs-lookup"><span data-stu-id="1264b-245">**All** – Applies same security settings to be applied to both OData and data import/export.</span></span>
    - <span data-ttu-id="1264b-246">**データ管理** - データのインポート/エクスポートおよびコネクタの統合のみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1264b-246">**Data Management** – Applies only to data import/export and connector integration.</span></span>
    - <span data-ttu-id="1264b-247">**データ サービス** - OData サービスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="1264b-247">**Data Services** – Only applies to OData Services.</span></span>

<span data-ttu-id="1264b-248">[![RolebasedSecurity](./media/rolebasedsecurity.png)](./media/rolebasedsecurity.png)</span><span class="sxs-lookup"><span data-stu-id="1264b-248">[![RolebasedSecurity](./media/rolebasedsecurity.png)](./media/rolebasedsecurity.png)</span></span>

## <a name="sensitive-data"></a><span data-ttu-id="1264b-249">機密データ</span><span class="sxs-lookup"><span data-stu-id="1264b-249">Sensitive data</span></span>
<span data-ttu-id="1264b-250">テーブル保護フレームワーク (TPF) は、Finance and Operations に格納されているデータへの厳密なアクセス制御を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1264b-250">The Table Protection Framework (TPF) enables strict access control to data that is stored in Finance and Operations.</span></span> <span data-ttu-id="1264b-251">この機能は、テーブルおよびテーブルのフィールドの AOSAuthorization プロパティを介して公開されます。</span><span class="sxs-lookup"><span data-stu-id="1264b-251">This feature is exposed through the AOSAuthorization property on tables and table fields.</span></span> <span data-ttu-id="1264b-252">AOSAuthorization を使用してテーブルまたはフィールドにマークを付ける場合、セキュリティ フレームワークでは、そのリソースへの明示的なアクセス権がユーザーに付与されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-252">If you mark a table or field by using AOSAuthorization, the security framework now requires that a user be granted explicit access to that resource.</span></span> <span data-ttu-id="1264b-253">この要件は、テーブルまたはフィールドにデータエンティティでアクセスする場合にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="1264b-253">This requirement also applies when the table or field is accessed through data entities.</span></span> <span data-ttu-id="1264b-254">この項では、データ エンティティの TPF アクセス許可を付与するためのガイドラインについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1264b-254">This section describes the guidelines for granting TPF permissions for data entities.</span></span>

### <a name="data-management"></a><span data-ttu-id="1264b-255">データ管理</span><span class="sxs-lookup"><span data-stu-id="1264b-255">Data management</span></span> 
<span data-ttu-id="1264b-256">データ移行で対象となるデータ エンティティについては、TPF アクセス許可を対応するインポート/エクスポート権限に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-256">For data entities that are targeted at data migration, you should assign TPF permissions to the corresponding import/export privileges.</span></span> <span data-ttu-id="1264b-257">この方法で、すべてのデータがインポート/エクスポートできることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="1264b-257">In this way, you help guarantee that all data can be imported and exported.</span></span>

### <a name="integration-by-using-odata"></a><span data-ttu-id="1264b-258">OData を使用する統合</span><span class="sxs-lookup"><span data-stu-id="1264b-258">Integration by using OData</span></span>
<span data-ttu-id="1264b-259">統合シナリオで対象とされるデータ エンティティについては、割り当てる必要がある TPF アクセス許可は、作業する全体としてのデータ エンティティに対して TPF で保護されたフィールドが必須かどうかに依存します。</span><span class="sxs-lookup"><span data-stu-id="1264b-259">For data entities that are targeted at integration scenarios, the TPF permissions that you should assign depend on whether the TPF-protected field is essential for the data entity as a whole to work:</span></span>

- <span data-ttu-id="1264b-260">**TPF で保護されたフィールドが必須の場合**: 必須のフィールドは、常に読み取り/書き込みとなるフィールドです。</span><span class="sxs-lookup"><span data-stu-id="1264b-260">**If the TPF-protected field is essential**: An essential field is a field that will always be read/written.</span></span> <span data-ttu-id="1264b-261">この場合、TPF のアクセス許可は、データ エンティティへのアクセスを許可する同じ権限に対して付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-261">In this case, TPF permissions should be granted to the same privileges that grant access to the data entity.</span></span>
- <span data-ttu-id="1264b-262">**TPF で保護されたフィールドが必須ではない場合**: 必須ではないフィールドの例としては、作業者の社会保障番号のフィールドおよび仕入先の銀行口座番号のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="1264b-262">**If the TPF-protected field isn't essential**: Examples of nonessential fields include the field for a worker's Social Security number and the field for a vendor's bank account number.</span></span> <span data-ttu-id="1264b-263">この場合、このフィールドにアクセスするための TPF アクセス許可は別の権限を通じて付与する必要があり、その権限は TPF で保護されたフィールドへのアクセスを必要とするロールに直接割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-263">In this case, TPF permissions for accessing the field should be granted through a separate privilege, and that privilege should be assigned directly to the roles that require access to the TPF-protected field.</span></span> <span data-ttu-id="1264b-264">ただし、フィールドがエンティティのマップ済フィールドである場合、そのロールは Finance and Operations クライアント UI のページを通してフィールドへアクセスできるなら、ロールへのそのアクセスが既に許可された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-264">However, if the field is a mapped field on the entity, that access has probably already been granted to the role, if that role also has access to the field through pages in the Finance and Operations client UI.</span></span>

<span data-ttu-id="1264b-265">エンティティにとって必須ではない TPF で保護されたフィールドへの明示的なアクセスを許可することには、いくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="1264b-265">There are several advantages to granting explicit access to TPF-protected fields that aren't considered essential for the entity:</span></span>

- <span data-ttu-id="1264b-266">だれが機密データへのアクセス権を持つかをより簡単に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="1264b-266">You can more easily discover who has access to sensitive data.</span></span>
- <span data-ttu-id="1264b-267">ロールに職務権限と特権の両方を割り当てる場合にのみにロールがアクセス権を取得するので、だれかが誤って機密データへのアクセスできるリスクを軽減できます。</span><span class="sxs-lookup"><span data-stu-id="1264b-267">You help reduce the risk that someone will gain access to sensitive data by accident, because a role gains access only if you assign both a duty and a privilege to it.</span></span>
