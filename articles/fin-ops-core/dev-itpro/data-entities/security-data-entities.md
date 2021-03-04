---
title: セキュリティとデータ エンティティ
description: このトピックでは、データ エンティティのセキュリティについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 17852
ms.assetid: a9ede141-56fa-4310-997d-aeef184f7a52
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 222b18106e8af461f801097e49d8626c336dc01f
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127661"
---
# <a name="security-and-data-entities"></a><span data-ttu-id="30b20-103">セキュリティとデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="30b20-103">Security and data entities</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="30b20-104">データ エンティティは拡張可能なデータ セキュリティ (XDS) の概念をサポートしません。</span><span class="sxs-lookup"><span data-stu-id="30b20-104">Data entities do not support the Extensible Data Security (XDS) concepts.</span></span>

## <a name="entry-points"></a><span data-ttu-id="30b20-105">エントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="30b20-105">Entry points</span></span>
<span data-ttu-id="30b20-106">データ エンティティはエントリ ポイントのセキュリティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="30b20-106">Data entities support entry point security.</span></span> <span data-ttu-id="30b20-107">このサポートは、メニュー項目とページのサポートと似ています。</span><span class="sxs-lookup"><span data-stu-id="30b20-107">This support resembles the support that menu items and pages have.</span></span> <span data-ttu-id="30b20-108">セキュリティ モデルを定義する際の柔軟性を高めるため、データ エンティティでは統合モードごとに個別のセキュリティ設定が可能となっています。</span><span class="sxs-lookup"><span data-stu-id="30b20-108">To give you flexibility when you define a security model, data entities allow for a separate security configuration for each integration mode.</span></span> <span data-ttu-id="30b20-109">現在、データ エンティティに対して 2 つのエントリ ポイント/統合モードは識別されます。</span><span class="sxs-lookup"><span data-stu-id="30b20-109">Currently, two entry points/integration modes are identified for a data entity.</span></span>

| <span data-ttu-id="30b20-110">エントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="30b20-110">Entry point</span></span>     | <span data-ttu-id="30b20-111">説明</span><span class="sxs-lookup"><span data-stu-id="30b20-111">Description</span></span>                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b20-112">データ サービス</span><span class="sxs-lookup"><span data-stu-id="30b20-112">Data services</span></span>   | <span data-ttu-id="30b20-113">エンティティ用の OData サービス (API) を使用できる機能。</span><span class="sxs-lookup"><span data-stu-id="30b20-113">The ability to use OData services (API) for the entity.</span></span>                                                              |
| <span data-ttu-id="30b20-114">データ管理</span><span class="sxs-lookup"><span data-stu-id="30b20-114">Data management</span></span> | <span data-ttu-id="30b20-115">インポート/エクスポートおよびコネクタの統合など、エンティティ用の非同期統合オプションを使用できる機能。</span><span class="sxs-lookup"><span data-stu-id="30b20-115">The ability to use asynchronous integration options for the entity, such as import/export and connector integration.</span></span> |

## <a name="target-scenarios"></a><span data-ttu-id="30b20-116">ターゲット シナリオ</span><span class="sxs-lookup"><span data-stu-id="30b20-116">Target scenarios</span></span>
<span data-ttu-id="30b20-117">データ エンティティは、シナリオの複数のカテゴリをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="30b20-117">Data entities can support multiple categories of scenarios.</span></span> <span data-ttu-id="30b20-118">各カテゴリでは、別々に確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-118">Each category might have to be secured separately.</span></span>

- <span data-ttu-id="30b20-119">**データ管理 (ファイルに基づくインポート/エクスポートなど)** - 通常、データ マネージャーがこれらのシナリオを実行します。</span><span class="sxs-lookup"><span data-stu-id="30b20-119">**Data management (file-based import/export, and so on)** – Typically, a data manager performs these scenarios.</span></span> <span data-ttu-id="30b20-120">これらのシナリオでは、クライアントの UI から通常アクセスできないデータにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="30b20-120">These scenarios might provide access to data that isn't usually accessible through the UI for the client.</span></span> <span data-ttu-id="30b20-121">したがって、データ マネージャーがインポート/エクスポート操作のみを実行できるよう、関連ページへのアクセスとは独立してデータ管理シナリオを保護したいと考えることは多くあります。</span><span class="sxs-lookup"><span data-stu-id="30b20-121">Therefore, you will often want to secure data management scenarios independently of access to the related page, so that a data manager can perform only import/export operations.</span></span>
- <span data-ttu-id="30b20-122">**OData 経由の全般的な統合** – 多くの統合シナリオでは、データ エンティティをサービスとして公開する必要があるため、OData (オンライン ストアフロントや製品ライフサイクル管理 \[PLM\] システムなど) を介してデータにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="30b20-122">**General integration via OData** – Many integration scenarios require that data entities be exposed as services, so that data can be accessed via OData (for example, from an online storefront or a Process Lifetime Management \[PLM\] system).</span></span> <span data-ttu-id="30b20-123">多くの場合、この目的のためにページ アクセスとは別に作成されている、データ エンティティへのアクセスを制御する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-123">Often, you will want to control access to data entities that are built for this purpose independently of page access.</span></span> <span data-ttu-id="30b20-124">つまり、クライアントの UI を使用してアクセス許可を与えることなく、サービス インターフェイスへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="30b20-124">In other words, you will want to grant access to the service interface without granting access through the client UI.</span></span>
- <span data-ttu-id="30b20-125">**Microsoft Office 統合 (Excel での編集など)** – Office 統合シナリオでも、OData 経由でアクセスするデータ エンティティが必要です。</span><span class="sxs-lookup"><span data-stu-id="30b20-125">**Microsoft Office integration (Edit in Excel, and so on)** – Office integration scenarios also require that data entities be accessed via OData.</span></span> <span data-ttu-id="30b20-126">ただし、エンドユーザーの観点からは、これらのシナリオは、たとえば Microsoft Excel が一部の編集作業を簡略化するのに使用されるなど、クライアントの自然の拡張として見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="30b20-126">However, from an end-user perspective, these scenarios can be viewed as a natural extension of the client, where, for example, Microsoft Excel is used to simplify some editing tasks.</span></span> <span data-ttu-id="30b20-127">したがって、通常、ページ アクセスとは独立して Microsoft Office の統合を保護する理由はありません。</span><span class="sxs-lookup"><span data-stu-id="30b20-127">Therefore, there is usually no reason to secure the Microsoft Office integration independently of page access.</span></span>

## <a name="privilegeduty-mapping"></a><span data-ttu-id="30b20-128">権限/職務権限マッピング</span><span class="sxs-lookup"><span data-stu-id="30b20-128">Privilege/duty mapping</span></span>
<span data-ttu-id="30b20-129">データ エンティティの対象シナリオに応じて、1 つまたは複数の新しい特権を作成し、既存の職務を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-129">Depending on the target scenarios for a data entity, you should create one or more new privileges, and extend existing duties.</span></span> <span data-ttu-id="30b20-130">または、新しい権限をターゲット シナリオ用に特別に作成された職務にマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="30b20-130">Alternatively, you can map the new privileges to duties that are created specifically for the target scenario.</span></span> <span data-ttu-id="30b20-131">この方法は、シナリオに必要なアクセス権以上のアクセス権がユーザーに付与されないようにします。</span><span class="sxs-lookup"><span data-stu-id="30b20-131">This approach helps guarantee that no user is granted more access than the user requires for the scenario.</span></span>

<span data-ttu-id="30b20-132">次のテーブルに、作成する必要のある権限を示します。</span><span class="sxs-lookup"><span data-stu-id="30b20-132">The following table shows the privileges that you should create.</span></span> <span data-ttu-id="30b20-133">また、職務にこれらの特権をマップする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="30b20-133">It also explains how you should map these privileges to duties.</span></span> <span data-ttu-id="30b20-134">データ エンティティが複数のシナリオをサポートすることを意図している場合、権限と職務権限マッピングを組み合わせたセットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-134">If your data entity is intended to support more than one scenario, you should create the combined set of privileges and duty mappings.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="30b20-135">ターゲット シナリオ</span><span class="sxs-lookup"><span data-stu-id="30b20-135">Target scenario</span></span></th>
<th><span data-ttu-id="30b20-136">権限</span><span class="sxs-lookup"><span data-stu-id="30b20-136">Privileges</span></span></th>
<th><span data-ttu-id="30b20-137">職務マッピング</span><span class="sxs-lookup"><span data-stu-id="30b20-137">Duty mapping</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="30b20-138">データ エンティティは、データ管理を目的としています。</span><span class="sxs-lookup"><span data-stu-id="30b20-138">The data entity is intended for data management.</span></span></td>
<td><span data-ttu-id="30b20-139">次の新しい権限を作成します。</span><span class="sxs-lookup"><span data-stu-id="30b20-139">Create the following new privileges:</span></span>
<ul>
<li><span data-ttu-id="30b20-140"><em>&lt;DataEntity&gt;</em><strong>インポート</strong>
</span><span class="sxs-lookup"><span data-stu-id="30b20-140"><em>&lt;DataEntity&gt;</em><strong>Import</strong>
</span></span><ul>
<li><span data-ttu-id="30b20-141">交付 = 作成</span><span class="sxs-lookup"><span data-stu-id="30b20-141">Grant=Create</span></span></li>
<li><span data-ttu-id="30b20-142">IntegrationMode=DataManagement</span><span class="sxs-lookup"><span data-stu-id="30b20-142">IntegrationMode=DataManagement</span></span></li>
</ul>
</li>
<li><span data-ttu-id="30b20-143"><em>&lt;DataEntity&gt;</em><strong>エクスポート</strong>
</span><span class="sxs-lookup"><span data-stu-id="30b20-143"><em>&lt;DataEntity&gt;</em><strong>Export</strong>
</span></span><ul>
<li><span data-ttu-id="30b20-144">付与 = 読み取り</span><span class="sxs-lookup"><span data-stu-id="30b20-144">Grant=Read</span></span></li>
<li><span data-ttu-id="30b20-145">IntegrationMode=DataManagement</span><span class="sxs-lookup"><span data-stu-id="30b20-145">IntegrationMode=DataManagement</span></span></li>
</ul>
</li>
</ul>
</td>
<td><span data-ttu-id="30b20-146">新しい権限を持つ関連データの管理業務を拡張します。</span><span class="sxs-lookup"><span data-stu-id="30b20-146">Extend the relevant data management duties with the new privileges.</span></span> <span data-ttu-id="30b20-147">詳細については、このトピックで後述する「データ管理ロール」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="30b20-147">For more information, see the "Data administrator role" section later in this topic.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30b20-148">データ エンティティは、OData を介した一般的な統合を目的としています。</span><span class="sxs-lookup"><span data-stu-id="30b20-148">The data entity is intended for general integration via OData.</span></span></td>
<td><span data-ttu-id="30b20-149">次の新しい権限を作成します。</span><span class="sxs-lookup"><span data-stu-id="30b20-149">Create the following new privileges:</span></span>
<ul>
<li><span data-ttu-id="30b20-150"><em>&lt;DataEntity&gt;</em> <strong>ビュー</strong>
</span><span class="sxs-lookup"><span data-stu-id="30b20-150"><em>&lt;DataEntity&gt;</em><strong>View</strong>
</span></span><ul>
<li><span data-ttu-id="30b20-151">付与 = 読み取り</span><span class="sxs-lookup"><span data-stu-id="30b20-151">Grant=Read</span></span></li>
<li><span data-ttu-id="30b20-152">IntegrationMode=DataServices</span><span class="sxs-lookup"><span data-stu-id="30b20-152">IntegrationMode=DataServices</span></span></li>
</ul>
</li>
<li><span data-ttu-id="30b20-153"><em>&lt;DataEntity&gt;</em><strong>管理</strong>
</span><span class="sxs-lookup"><span data-stu-id="30b20-153"><em>&lt;DataEntity&gt;</em><strong>Maintain</strong>
</span></span><ul>
<li><span data-ttu-id="30b20-154">交付 = 削除</span><span class="sxs-lookup"><span data-stu-id="30b20-154">Grant=Delete</span></span></li>
<li><span data-ttu-id="30b20-155">IntegrationMode=DataServices</span><span class="sxs-lookup"><span data-stu-id="30b20-155">IntegrationMode=DataServices</span></span></li>
</ul>
</li>
</ul>
</td>
<td><span data-ttu-id="30b20-156">統合シナリオの新しい職務を作成し、関連する新しい特権をこれらの職務にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="30b20-156">Create new duties for the integration scenario, and map the relevant new privileges to these duties.</span></span> <span data-ttu-id="30b20-157">詳細については、このトピックで後述する「職務名のガイドライン」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="30b20-157">For more information, see the "Duty naming guidelines" section later in this topic.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30b20-158">データ エンティティは、Microsoft Office との統合を目的としています。</span><span class="sxs-lookup"><span data-stu-id="30b20-158">The data entity is intended for Microsoft Office integration.</span></span></td>
<td><span data-ttu-id="30b20-159">次の新しい権限を作成します。</span><span class="sxs-lookup"><span data-stu-id="30b20-159">Create the following new privileges:</span></span>
<ul>
<li><span data-ttu-id="30b20-160"><em>&lt;DataEntity&gt;</em> <strong>ビュー</strong>
</span><span class="sxs-lookup"><span data-stu-id="30b20-160"><em>&lt;DataEntity&gt;</em><strong>View</strong>
</span></span><ul>
<li><span data-ttu-id="30b20-161">付与 = 読み取り</span><span class="sxs-lookup"><span data-stu-id="30b20-161">Grant=Read</span></span></li>
<li><span data-ttu-id="30b20-162">IntegrationMode=DataServices</span><span class="sxs-lookup"><span data-stu-id="30b20-162">IntegrationMode=DataServices</span></span></li>
</ul>
</li>
<li><span data-ttu-id="30b20-163"><em>&lt;DataEntity&gt;</em><strong>管理</strong>
</span><span class="sxs-lookup"><span data-stu-id="30b20-163"><em>&lt;DataEntity&gt;</em><strong>Maintain</strong>
</span></span><ul>
<li><span data-ttu-id="30b20-164">交付 = 削除</span><span class="sxs-lookup"><span data-stu-id="30b20-164">Grant=Delete</span></span></li>
<li><span data-ttu-id="30b20-165">IntegrationMode=DataServices</span><span class="sxs-lookup"><span data-stu-id="30b20-165">IntegrationMode=DataServices</span></span></li>
</ul>
</li>
</ul>
</td>
<td><span data-ttu-id="30b20-166">新しい権限を持つ関連ページへのアクセスを提供する関連する既存の任務を拡張します。</span><span class="sxs-lookup"><span data-stu-id="30b20-166">Extend the relevant existing duties that provide access to the related pages with the new privileges.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="30b20-167">前のテーブルで説明されている方法は最小特権の原則に準拠しているため、それを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="30b20-167">Because the approach that is described in the preceding table complies with the principle of least privilege, we recommend that you use it.</span></span> <span data-ttu-id="30b20-168">ただし、場合によっては、次のより簡単な方法を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="30b20-168">Nevertheless, in some situations, you can use the following simpler approach.</span></span> <span data-ttu-id="30b20-169">ただし、この方法は安全性が低い場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="30b20-169">However, be aware that this approach might be less secure.</span></span> <span data-ttu-id="30b20-170">管理および拡張が少し困難になる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="30b20-170">It might also be slightly harder to maintain and extend.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="30b20-171">ターゲット シナリオ</span><span class="sxs-lookup"><span data-stu-id="30b20-171">Target scenario</span></span></th>
<th><span data-ttu-id="30b20-172">権限</span><span class="sxs-lookup"><span data-stu-id="30b20-172">Privileges</span></span></th>
<th><span data-ttu-id="30b20-173">職務マッピング</span><span class="sxs-lookup"><span data-stu-id="30b20-173">Duty mapping</span></span></th>
<th><span data-ttu-id="30b20-174">潜在的な問題</span><span class="sxs-lookup"><span data-stu-id="30b20-174">Potential issues</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="30b20-175">データ エンティティは、データ管理、OData による一般的な統合、および Microsoft Office との統合を目的としています。</span><span class="sxs-lookup"><span data-stu-id="30b20-175">The data entity is intended for data management, general integration via OData, and Microsoft Office integration.</span></span></td>
<td><span data-ttu-id="30b20-176">次の新しい権限を作成します。</span><span class="sxs-lookup"><span data-stu-id="30b20-176">Create the following new privileges:</span></span>
<ul>
<li><span data-ttu-id="30b20-177"><em>&lt;DataEntity&gt;</em> <strong>ビュー</strong>
</span><span class="sxs-lookup"><span data-stu-id="30b20-177"><em>&lt;DataEntity&gt;</em><strong>View</strong>
</span></span><ul>
<li><span data-ttu-id="30b20-178">付与 = 読み取り</span><span class="sxs-lookup"><span data-stu-id="30b20-178">Grant=Read</span></span></li>
<li><span data-ttu-id="30b20-179">IntegrationMode=All</span><span class="sxs-lookup"><span data-stu-id="30b20-179">IntegrationMode=All</span></span></li>
</ul>
</li>
<li><span data-ttu-id="30b20-180"><em>&lt;DataEntity&gt;</em><strong>管理</strong>
</span><span class="sxs-lookup"><span data-stu-id="30b20-180"><em>&lt;DataEntity&gt;</em><strong>Maintain</strong>
</span></span><ul>
<li><span data-ttu-id="30b20-181">交付 = 削除</span><span class="sxs-lookup"><span data-stu-id="30b20-181">Grant=Delete</span></span></li>
<li><span data-ttu-id="30b20-182">IntegrationMode=All</span><span class="sxs-lookup"><span data-stu-id="30b20-182">IntegrationMode=All</span></span></li>
</ul>
</li>
</ul>
</td>
<td>
<ol>
<li><span data-ttu-id="30b20-183">新しい権限を持つ関連データの管理業務を拡張します。</span><span class="sxs-lookup"><span data-stu-id="30b20-183">Extend the relevant data management duties with the new privileges.</span></span></li>
<li><span data-ttu-id="30b20-184">統合シナリオの新しい職務を作成し、関連する新しい特権をこれらの職務にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="30b20-184">Create new duties for the integration scenario, and map the relevant new privileges to these duties.</span></span></li>
<li><span data-ttu-id="30b20-185">新しい権限を持つ関連ページへのアクセスを提供する関連する既存の任務を拡張します。</span><span class="sxs-lookup"><span data-stu-id="30b20-185">Extend the relevant existing duties that provide access to the related page with the new privileges.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="30b20-186">この方法を使用するときは、データのインポート/エクスポートへのアクセス許可を付与されているデータ マネージャーは、システムに Web サービスからもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="30b20-186">When you use this approach, a data manager who is granted access to import/export data can also access the system from a web service.</span></span> <span data-ttu-id="30b20-187">同様に、データ エンティティに関連付けられているページへのアクセスを許可されているユーザーは、Web サービスからでもシステムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="30b20-187">Likewise, a user who is granted access to the page that is associated with a data entity can also access the system from a web service.</span></span> <span data-ttu-id="30b20-188">このユーザーは、関連するデータ管理職務権限を付与されていない場合にのみ、データのインポート/エクスポートを禁止されます。</span><span class="sxs-lookup"><span data-stu-id="30b20-188">This user will be prevented from data import/export only if the user hasn't been granted the related data management duty.</span></span></td>
</tr>
</tbody>
</table>

## <a name="duty-naming-guidelines"></a><span data-ttu-id="30b20-189">職務名のガイドライン</span><span class="sxs-lookup"><span data-stu-id="30b20-189">Duty naming guidelines</span></span>
<span data-ttu-id="30b20-190">特定の統合シナリオのデータ エンティティを作成するとき、個別の職務も作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-190">When you create data entities for specific integration scenarios, you should also create separate duties.</span></span> <span data-ttu-id="30b20-191">これらの任務は、外部アプリケーションまたはサービスに、データ エンティティへの必要なアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="30b20-191">These duties grant the external application or service the required access to the data entities.</span></span> <span data-ttu-id="30b20-192">作成する職務は、クライアント UI を介してアクセスするための対応する職務と同じ命名規則に従ってください。</span><span class="sxs-lookup"><span data-stu-id="30b20-192">The duties that you create should follow the same naming guidelines as the corresponding duties that provide access through the client UI.</span></span> <span data-ttu-id="30b20-193">ただし、「サービスを使用する」接尾辞を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-193">However, you should add a "using services" suffix.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="30b20-194">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="30b20-194">Duty type</span></span></th>
<th><span data-ttu-id="30b20-195">職務オブジェクト名の接尾語</span><span class="sxs-lookup"><span data-stu-id="30b20-195">Duty object name suffix</span></span></th>
<th><span data-ttu-id="30b20-196">職務名のテンプレート</span><span class="sxs-lookup"><span data-stu-id="30b20-196">Duty name template</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="30b20-197">有効化</span><span class="sxs-lookup"><span data-stu-id="30b20-197">Enable</span></span></td>
<td><span data-ttu-id="30b20-198">…IntegrationEnable</span><span class="sxs-lookup"><span data-stu-id="30b20-198">…IntegrationEnable</span></span></td>
<td><span data-ttu-id="30b20-199">有効化 …</span><span class="sxs-lookup"><span data-stu-id="30b20-199">Enable …</span></span> <span data-ttu-id="30b20-200">サービスの使用</span><span class="sxs-lookup"><span data-stu-id="30b20-200">using services</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30b20-201">レコード</span><span class="sxs-lookup"><span data-stu-id="30b20-201">Record</span></span></td>
<td><span data-ttu-id="30b20-202">…IntegrationMaintain</span><span class="sxs-lookup"><span data-stu-id="30b20-202">…IntegrationMaintain</span></span></td>
<td><span data-ttu-id="30b20-203">メンテナンス …</span><span class="sxs-lookup"><span data-stu-id="30b20-203">Maintain …</span></span> <span data-ttu-id="30b20-204">サービスの使用</span><span class="sxs-lookup"><span data-stu-id="30b20-204">using services</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30b20-205">認証する</span><span class="sxs-lookup"><span data-stu-id="30b20-205">Authorize</span></span></td>
<td><span data-ttu-id="30b20-206">…IntegrationApprove (リリース、確認、仕分入力)</span><span class="sxs-lookup"><span data-stu-id="30b20-206">…IntegrationApprove (Release, Confirm, Journalize)</span></span></td>
<td><span data-ttu-id="30b20-207">承認 (リリース、確認、仕訳入力) …</span><span class="sxs-lookup"><span data-stu-id="30b20-207">Approve (Release, Confirm, Journalize) …</span></span> <span data-ttu-id="30b20-208">サービスの使用</span><span class="sxs-lookup"><span data-stu-id="30b20-208">using services</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30b20-209">照会</span><span class="sxs-lookup"><span data-stu-id="30b20-209">Inquire</span></span></td>
<td><span data-ttu-id="30b20-210">…IntegrationInquire</span><span class="sxs-lookup"><span data-stu-id="30b20-210">…IntegrationInquire</span></span></td>
<td><span data-ttu-id="30b20-211">照会先 …</span><span class="sxs-lookup"><span data-stu-id="30b20-211">Inquire into …</span></span> <span data-ttu-id="30b20-212">サービスの使用</span><span class="sxs-lookup"><span data-stu-id="30b20-212">using services</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="30b20-213">これらのガイドラインに従う職務権限名の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="30b20-213">Here are some examples of duty names that follow these guidelines:</span></span>

- <span data-ttu-id="30b20-214">サービスを使用した工順マスターの管理</span><span class="sxs-lookup"><span data-stu-id="30b20-214">Maintain route master using service</span></span>
- <span data-ttu-id="30b20-215">サービスを使用しているケース進捗状況の照会</span><span class="sxs-lookup"><span data-stu-id="30b20-215">Inquire into case progress using services</span></span>

## <a name="data-administrator-role"></a><span data-ttu-id="30b20-216">データ管理者ロール</span><span class="sxs-lookup"><span data-stu-id="30b20-216">Data administrator role</span></span>
<span data-ttu-id="30b20-217">**DataManagementApplicationAdministrator** セキュリティ ロールによって、関連したユーザーが **データ管理** ワークスペースでフル インポート/エクスポート機能を実行できます。</span><span class="sxs-lookup"><span data-stu-id="30b20-217">The **DataManagementApplicationAdministrator** security role enables an associated user to have full import/export capabilities in the **Data management** workspace.</span></span> <span data-ttu-id="30b20-218">このセキュリティ ロールには、5 つのデータ エンティティ カテゴリに割り当てられた 2 つのセキュリティ職務があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-218">This security role has two security duties for each of the five data entity categories that are assigned to it.</span></span> <span data-ttu-id="30b20-219">1 つの関税は、関連するカテゴリのデータ エンティティを介してデータをインポートすることであり、1 つは関連するカテゴリのデータ エンティティを介してデータをエクスポートすることです。</span><span class="sxs-lookup"><span data-stu-id="30b20-219">One duty is for importing data via data entities of the associated category, and one for exporting data via data entities of the associated category.</span></span> <span data-ttu-id="30b20-220">したがって、このセキュリティ ロールには合計 10 のセキュリティ義務が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="30b20-220">Therefore, a total of 10 security duties are assigned to this security role:</span></span>

- <span data-ttu-id="30b20-221">DataManagementApplicationDocumentEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="30b20-221">DataManagementApplicationDocumentEntitiesMaintain</span></span>
- <span data-ttu-id="30b20-222">DataManagementApplicationDocumentEntitiesView</span><span class="sxs-lookup"><span data-stu-id="30b20-222">DataManagementApplicationDocumentEntitiesView</span></span>
- <span data-ttu-id="30b20-223">DataManagementApplicationMasterEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="30b20-223">DataManagementApplicationMasterEntitiesMaintain</span></span>
- <span data-ttu-id="30b20-224">DataManagementApplicationMasterEntitiesView</span><span class="sxs-lookup"><span data-stu-id="30b20-224">DataManagementApplicationMasterEntitiesView</span></span>
- <span data-ttu-id="30b20-225">DataManagementApplicationParametersEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="30b20-225">DataManagementApplicationParametersEntitiesMaintain</span></span>
- <span data-ttu-id="30b20-226">DataManagementApplicationParametersEntitiesView</span><span class="sxs-lookup"><span data-stu-id="30b20-226">DataManagementApplicationParametersEntitiesView</span></span>
- <span data-ttu-id="30b20-227">DataManagementApplicationReferenceEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="30b20-227">DataManagementApplicationReferenceEntitiesMaintain</span></span>
- <span data-ttu-id="30b20-228">DataManagementApplicationReferenceEntitiesView</span><span class="sxs-lookup"><span data-stu-id="30b20-228">DataManagementApplicationReferenceEntitiesView</span></span>
- <span data-ttu-id="30b20-229">DataManagementApplicationTransactionEntitiesMaintain</span><span class="sxs-lookup"><span data-stu-id="30b20-229">DataManagementApplicationTransactionEntitiesMaintain</span></span>
- <span data-ttu-id="30b20-230">DataManagementApplicationTransactionEntitiesView</span><span class="sxs-lookup"><span data-stu-id="30b20-230">DataManagementApplicationTransactionEntitiesView</span></span>

<span data-ttu-id="30b20-231">**データ管理** ワークスペースで使用できるデータ エンティティを作成するとき、データ エンティティで指定される **エンティティ カテゴリ** プロパティに基づいて、新しいセキュリティ権限を持つこれらの職務を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-231">When you create data entities that can be used in the **Data management** workspace, you must extend these duties with the new security privileges, based on the **Entity Category** property that is specified on the data entity.</span></span> <span data-ttu-id="30b20-232">(新しいセキュリティ権限を使用して職務を拡張する方法については、このトピックの前半の「特権/職務マッピング」セクションを参照してください。)また、職務を使用して、特定のデータ管理シナリオ用の新しいロールを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="30b20-232">(For information about how to extend duties with the new security privileges, see the "Privilege/duty mapping" section earlier in this topic.) You can also use the duties to create new roles for specific data management scenarios.</span></span>

## <a name="modeling-new-entry-point-security-in-the-application-explorer"></a><span data-ttu-id="30b20-233">アプリケーション エクスプローラーでの新しいエントリ ポイント セキュリティのモデリング</span><span class="sxs-lookup"><span data-stu-id="30b20-233">Modeling new entry point security in the Application Explorer</span></span>
<span data-ttu-id="30b20-234">セキュリティのモデリングのパターンは、エントリ ポイントに対する権限を持つセキュリティのモデリングのパターンと似ています。</span><span class="sxs-lookup"><span data-stu-id="30b20-234">The pattern for modeling security resembles the pattern for modeling security with privileges on an entry point.</span></span> <span data-ttu-id="30b20-235">セキュリティをモデル化するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="30b20-235">To model security, follow these steps.</span></span>

1. <span data-ttu-id="30b20-236">新しい権限の作成を作成します。</span><span class="sxs-lookup"><span data-stu-id="30b20-236">Create a new privilege.</span></span>
2. <span data-ttu-id="30b20-237">新しいデータ エンティティのアクセス許可を作成します。</span><span class="sxs-lookup"><span data-stu-id="30b20-237">Create new data entity permissions.</span></span>
3. <span data-ttu-id="30b20-238">**名前** を **データ エンティティ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="30b20-238">Set the **Name** to **Data Entity**.</span></span>
4. <span data-ttu-id="30b20-239">**アクセス レベル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="30b20-239">Select the **Access Level**.</span></span>
5. <span data-ttu-id="30b20-240">**統合モード** を選択します (すべて &gt; Data Services &gt; データ管理)。</span><span class="sxs-lookup"><span data-stu-id="30b20-240">Select **Integration Mode** (All &gt; Data Services &gt; Data Management).</span></span> <span data-ttu-id="30b20-241">これは、オブジェクトの種類のデータ エンティティに固有です。</span><span class="sxs-lookup"><span data-stu-id="30b20-241">This is specific to Object Type: Data Entity.</span></span>

    - <span data-ttu-id="30b20-242">**すべて** - OData とデータのインポート/エクスポートの両方に適用される同じセキュリティ設定を適用します。</span><span class="sxs-lookup"><span data-stu-id="30b20-242">**All** – Applies same security settings to be applied to both OData and data import/export.</span></span>
    - <span data-ttu-id="30b20-243">**データ管理** - データのインポート/エクスポートおよびコネクタの統合のみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="30b20-243">**Data Management** – Applies only to data import/export and connector integration.</span></span>
    - <span data-ttu-id="30b20-244">**データ サービス** - OData サービスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="30b20-244">**Data Services** – Only applies to OData Services.</span></span>

<span data-ttu-id="30b20-245">[![RolebasedSecurity](./media/rolebasedsecurity.png)](./media/rolebasedsecurity.png)</span><span class="sxs-lookup"><span data-stu-id="30b20-245">[![RolebasedSecurity](./media/rolebasedsecurity.png)](./media/rolebasedsecurity.png)</span></span>

## <a name="sensitive-data"></a><span data-ttu-id="30b20-246">機密データ</span><span class="sxs-lookup"><span data-stu-id="30b20-246">Sensitive data</span></span>
<span data-ttu-id="30b20-247">テーブル保護フレームワーク (TPF) は、Finance and Operations に格納されているデータへの厳密なアクセス制御を使用できます。</span><span class="sxs-lookup"><span data-stu-id="30b20-247">The Table Protection Framework (TPF) enables strict access control to data that is stored in Finance and Operations.</span></span> <span data-ttu-id="30b20-248">この機能は、テーブルおよびテーブルのフィールドの AOSAuthorization プロパティを介して公開されます。</span><span class="sxs-lookup"><span data-stu-id="30b20-248">This feature is exposed through the AOSAuthorization property on tables and table fields.</span></span> <span data-ttu-id="30b20-249">AOSAuthorization を使用してテーブルまたはフィールドにマークを付ける場合、セキュリティ フレームワークでは、そのリソースへの明示的なアクセス権がユーザーに付与されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-249">If you mark a table or field by using AOSAuthorization, the security framework now requires that a user be granted explicit access to that resource.</span></span> <span data-ttu-id="30b20-250">この要件は、テーブルまたはフィールドにデータエンティティでアクセスする場合にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="30b20-250">This requirement also applies when the table or field is accessed through data entities.</span></span> <span data-ttu-id="30b20-251">この項では、データ エンティティの TPF アクセス許可を付与するためのガイドラインについて説明します。</span><span class="sxs-lookup"><span data-stu-id="30b20-251">This section describes the guidelines for granting TPF permissions for data entities.</span></span>

### <a name="data-management"></a><span data-ttu-id="30b20-252">データ管理</span><span class="sxs-lookup"><span data-stu-id="30b20-252">Data management</span></span> 
<span data-ttu-id="30b20-253">データ移行で対象となるデータ エンティティについては、TPF アクセス許可を対応するインポート/エクスポート権限に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-253">For data entities that are targeted at data migration, you should assign TPF permissions to the corresponding import/export privileges.</span></span> <span data-ttu-id="30b20-254">この方法で、すべてのデータがインポート/エクスポートできることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="30b20-254">In this way, you help guarantee that all data can be imported and exported.</span></span>

### <a name="integration-by-using-odata"></a><span data-ttu-id="30b20-255">OData を使用する統合</span><span class="sxs-lookup"><span data-stu-id="30b20-255">Integration by using OData</span></span>
<span data-ttu-id="30b20-256">統合シナリオで対象とされるデータ エンティティについては、割り当てる必要がある TPF アクセス許可は、作業する全体としてのデータ エンティティに対して TPF で保護されたフィールドが必須かどうかに依存します。</span><span class="sxs-lookup"><span data-stu-id="30b20-256">For data entities that are targeted at integration scenarios, the TPF permissions that you should assign depend on whether the TPF-protected field is essential for the data entity as a whole to work:</span></span>

- <span data-ttu-id="30b20-257">**TPF で保護されたフィールドが必須の場合**: 必須のフィールドは、常に読み取り/書き込みとなるフィールドです。</span><span class="sxs-lookup"><span data-stu-id="30b20-257">**If the TPF-protected field is essential**: An essential field is a field that will always be read/written.</span></span> <span data-ttu-id="30b20-258">この場合、TPF のアクセス許可は、データ エンティティへのアクセスを許可する同じ権限に対して付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-258">In this case, TPF permissions should be granted to the same privileges that grant access to the data entity.</span></span>
- <span data-ttu-id="30b20-259">**TPF で保護されたフィールドが必須ではない場合**: 必須ではないフィールドの例としては、作業者の社会保障番号のフィールドおよび仕入先の銀行口座番号のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="30b20-259">**If the TPF-protected field isn't essential**: Examples of nonessential fields include the field for a worker's Social Security number and the field for a vendor's bank account number.</span></span> <span data-ttu-id="30b20-260">この場合、このフィールドにアクセスするための TPF アクセス許可は別の権限を通じて付与する必要があり、その権限は TPF で保護されたフィールドへのアクセスを必要とするロールに直接割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-260">In this case, TPF permissions for accessing the field should be granted through a separate privilege, and that privilege should be assigned directly to the roles that require access to the TPF-protected field.</span></span> <span data-ttu-id="30b20-261">ただし、フィールドがエンティティのマップ済フィールドである場合、そのロールはクライアント UI のページを通してフィールドへアクセスできるなら、ロールへのそのアクセスが既に許可された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-261">However, if the field is a mapped field on the entity, that access has probably already been granted to the role, if that role also has access to the field through pages in the client UI.</span></span>

<span data-ttu-id="30b20-262">エンティティにとって必須ではない TPF で保護されたフィールドへの明示的なアクセスを許可することには、いくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="30b20-262">There are several advantages to granting explicit access to TPF-protected fields that aren't considered essential for the entity:</span></span>

- <span data-ttu-id="30b20-263">だれが機密データへのアクセス権を持つかをより簡単に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="30b20-263">You can more easily discover who has access to sensitive data.</span></span>
- <span data-ttu-id="30b20-264">ロールに職務権限と特権の両方を割り当てる場合にのみにロールがアクセス権を取得するので、だれかが誤って機密データへのアクセスできるリスクを軽減できます。</span><span class="sxs-lookup"><span data-stu-id="30b20-264">You help reduce the risk that someone will gain access to sensitive data by accident, because a role gains access only if you assign both a duty and a privilege to it.</span></span>
