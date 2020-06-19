---
title: 会社間データ共有
description: このトピックでは、企業間のデータ共有について説明します。 会社間共有は、Finance and Operations 展開で、参照およびグループ データを会社間で共有するためのメカニズムです。
author: peakerbl
manager: AnnBe
ms.date: 06/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysDataSharingConfiguration
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 89071
ms.assetid: 0bbe7453-624f-4551-a1d0-842484067311
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 8d8a217e4ff8cd70246b511e8b8458f69403d21d
ms.sourcegitcommit: c5d0bd90334e259e96df17a217b2eff03c265f07
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2020
ms.locfileid: "3423002"
---
# <a name="cross-company-data-sharing"></a><span data-ttu-id="362c1-104">会社間データ共有</span><span class="sxs-lookup"><span data-stu-id="362c1-104">Cross-company data sharing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="362c1-105">このトピックでは、企業間のデータ共有について説明します。</span><span class="sxs-lookup"><span data-stu-id="362c1-105">This topic provides information about cross-company data sharing.</span></span> <span data-ttu-id="362c1-106">会社間共有は、Finance and Operations 展開で、参照およびグループ データを会社間で共有するためのメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="362c1-106">Cross-company sharing is a mechanism for sharing reference and group data among companies in a Finance and Operations deployment.</span></span> <span data-ttu-id="362c1-107">この機能は、Microsoft Dynamics AX 2012 の仮想会社機能に似ています。</span><span class="sxs-lookup"><span data-stu-id="362c1-107">This feature resembles the virtual companies feature in Microsoft Dynamics AX 2012.</span></span>

<a name="what-is-this-feature-and-how-does-it-work"></a><span data-ttu-id="362c1-108">これはどういう機能で、どのように動作しますか ?</span><span class="sxs-lookup"><span data-stu-id="362c1-108">What is this feature and how does it work?</span></span>
------------------------------------------

<span data-ttu-id="362c1-109">会社間のデータの共有を使用すると、会社間で参照およびグループのデータをレプリケート (共有) できます。</span><span class="sxs-lookup"><span data-stu-id="362c1-109">Cross-company data sharing lets you replicate (share) reference and group data among companies.</span></span> <span data-ttu-id="362c1-110">レプリケーションが行われる前にデータの整合性が確認されます。</span><span class="sxs-lookup"><span data-stu-id="362c1-110">Data integrity is verified before replication occurs.</span></span> 

<span data-ttu-id="362c1-111">会社間のデータ共有と基本的なロジックの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="362c1-111">Here are some examples of cross-company data sharing and the basic logic:</span></span>

-   <span data-ttu-id="362c1-112">同じ支払条件と支払日定義が 15 の法人に使用されています。</span><span class="sxs-lookup"><span data-stu-id="362c1-112">The same payment terms and payment day definitions are used across 15 legal entities.</span></span>
-   <span data-ttu-id="362c1-113">3 つの国/地域の 7 つの法人に、同じ配送条件が適用されています。</span><span class="sxs-lookup"><span data-stu-id="362c1-113">The same terms of delivery are used across seven legal entities in three countries/regions.</span></span>
-   <span data-ttu-id="362c1-114">ポリシー内のいずれかの会社で作成、更新、削除されたレコードは、すべての会社で直ちにレプリケートされます。</span><span class="sxs-lookup"><span data-stu-id="362c1-114">Records created, updated, and deleted in any of the companies within the policy will be replicated immediately, across all the companies.</span></span>
-   <span data-ttu-id="362c1-115">共有対象として選択されていないフィールドは、各会社で保持され、レプリケーションはトリガーされません。</span><span class="sxs-lookup"><span data-stu-id="362c1-115">Fields that are not selected for sharing are maintained in each company and will not trigger any replication.</span></span>
-   <span data-ttu-id="362c1-116">ポリシーを有効にする際に、既存のレコードをコピーすることを選択できます。</span><span class="sxs-lookup"><span data-stu-id="362c1-116">As part of enabling a policy, it is optional to copy any existing records.</span></span>


<span data-ttu-id="362c1-117">会社間のデータの共有には、次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="362c1-117">Cross-company data sharing has the following limitations:</span></span>

-   <span data-ttu-id="362c1-118">会社間でトランザクション データを共有するために使用できません。</span><span class="sxs-lookup"><span data-stu-id="362c1-118">It can’t be used to share transactional data between companies.</span></span>
-   <span data-ttu-id="362c1-119">参照データとグループ データのみを共有するか、有効に設定されているテーブルのみを共有することができます。</span><span class="sxs-lookup"><span data-stu-id="362c1-119">Only reference and group data can be shared, or tables that have specifically been enabled.</span></span> <span data-ttu-id="362c1-120">たとえば、**データ共有タイプ**が **複製** に設定されているとします。</span><span class="sxs-lookup"><span data-stu-id="362c1-120">For example, **Data Sharing Type** is set to **Duplicate**.</span></span>
-   <span data-ttu-id="362c1-121">ジョブごとに合計 100 万レコード未満のレプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="362c1-121">It supports replication of fewer than one million total records per job.</span></span> <span data-ttu-id="362c1-122">この合計は、共有レコードの数 × 共有会社の数として計算されます。</span><span class="sxs-lookup"><span data-stu-id="362c1-122">This total is calculated as the number of shared records × the number of shared companies.</span></span> <span data-ttu-id="362c1-123">バージョン 10.0.10 のプラットフォーム更新から、制限が 200 万レコードまで拡張されます。</span><span class="sxs-lookup"><span data-stu-id="362c1-123">The limit is increased to two million records from the Platform Update for version 10.0.10.</span></span>
-   <span data-ttu-id="362c1-124">ポリシーあたり最大で 100 社のレプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="362c1-124">It supports replication for up to 100 companies per policy.</span></span> <span data-ttu-id="362c1-125">バージョン 10.0.10 のプラットフォーム更新から、制限が 300 社まで拡張されます。</span><span class="sxs-lookup"><span data-stu-id="362c1-125">The limit is increased to 300 companies from the Platform Update for version 10.0.10.</span></span>
-   <span data-ttu-id="362c1-126">子の関係の1 つのレベルだけが公開されます。</span><span class="sxs-lookup"><span data-stu-id="362c1-126">Only one level of child relationships is exposed.</span></span> <span data-ttu-id="362c1-127">データの一貫性を保護するため、別のレベルが必要な場合、レプリケーションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="362c1-127">To protect data consistency, replication doesn't occur if another level is required.</span></span>
-   <span data-ttu-id="362c1-128">財務分析コードを参照するフィールド (たとえば、**元帳** または **既定** 分析コード) は、複数の会社間で共有することはできません。</span><span class="sxs-lookup"><span data-stu-id="362c1-128">Fields that reference Financial dimension, for example **Ledger** or **Default** dimension, can't be shared across companies.</span></span> 
      <span data-ttu-id="362c1-129">分析コードには、背景の分析コード データに対する緩い外部キー参照が保持されます。これは、会社固有のデータと非会社固有のデータの両方を参照できます。</span><span class="sxs-lookup"><span data-stu-id="362c1-129">o Dimensions hold a loose foreign key reference to the backing dimension data, which can reference both company-specific and non-company specific data.</span></span> <span data-ttu-id="362c1-130">各分析コード値に適用される適切なアクションを決定することは本質的に複雑であり、現在の実装からの変更が必要です。これは、パフォーマンスに大幅な影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="362c1-130">Determining the appropriate action to be taken for each dimension value has inherent complexity and would require a change from the current implementation, which could dramatically impact performance.</span></span>


### <a name="policies"></a><span data-ttu-id="362c1-131">ポリシー</span><span class="sxs-lookup"><span data-stu-id="362c1-131">Policies</span></span>

<span data-ttu-id="362c1-132">データ共有は、データ パッケージに保存された定義済みポリシーによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="362c1-132">Data sharing is managed by defined policies that are saved in data packages.</span></span> <span data-ttu-id="362c1-133">Microsoft がテスト済みでサポートしているテンプレートは、Microsoft Dynamics Lifecycle Services (LCS) でダウンロード可能なデータ パッケージとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="362c1-133">Templates that Microsoft has tested and supports are available as downloadable data packages on Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="362c1-134">ポリシーでは、データ共有の次の側面を制御できます。</span><span class="sxs-lookup"><span data-stu-id="362c1-134">Policies let you control the following aspects of data sharing:</span></span>

-   <span data-ttu-id="362c1-135">複製されるフィールド</span><span class="sxs-lookup"><span data-stu-id="362c1-135">The fields that are replicated</span></span>
-   <span data-ttu-id="362c1-136">レプリケーションに参加するエンティティ</span><span class="sxs-lookup"><span data-stu-id="362c1-136">The entities that participate in the replication</span></span>
-   <span data-ttu-id="362c1-137">共有に参加している会社</span><span class="sxs-lookup"><span data-stu-id="362c1-137">The companies that participates in the sharing</span></span>

<span data-ttu-id="362c1-138">会社とテーブルは、1 つのポリシーのみで使用できます。</span><span class="sxs-lookup"><span data-stu-id="362c1-138">The same company and table can only be in one policy.</span></span> <span data-ttu-id="362c1-139">同じテーブルを複数のポリシーで共有することもできます。</span><span class="sxs-lookup"><span data-stu-id="362c1-139">It is possible to share the same table in more than policy.</span></span> <span data-ttu-id="362c1-140">これは、レコードまたは会社の制限に達した場合や、異なる国や地域に対して共有する必要があるテーブルに対してポリシーを作成する場合に当てはまる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="362c1-140">This can happen when the limits of records or companies are reached, or to create policies for tables that need to be shared differently for different country/regions.</span></span> 

> [!NOTE]
> <span data-ttu-id="362c1-141">既定では、必要な外部キー フィールドのみが選択されます。</span><span class="sxs-lookup"><span data-stu-id="362c1-141">Only required foreign key fields are selected by default.</span></span> <span data-ttu-id="362c1-142">オプションの外部キーを手動で選択して追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="362c1-142">Optional foreign keys need to be selected manually to be included.</span></span> <span data-ttu-id="362c1-143">テーブルが追加されていない場合は、外部キー フィールドを選択するときに 1 つ以上のテーブルを追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="362c1-143">The best practice is to add one or more tables when selecting a foreign key field, unless the table has already been added.</span></span>

<span data-ttu-id="362c1-144">Microsoft がテスト済みでサポートしているポリシー テンプレートは、Lifecycle Services (LCS) でダウンロード可能なデータ パッケージとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="362c1-144">Policy templates that Microsoft has tested and supports are available as downloadable data packages on Lifecycle Services (LCS).</span></span> 


> [!IMPORTANT]
> <span data-ttu-id="362c1-145">顧客は、LCS から使用可能な Microsoft データ テンプレートを変更できますが、このシナリオには対応していません。</span><span class="sxs-lookup"><span data-stu-id="362c1-145">Although customers can modify the Microsoft data templates that are available from LCS, this scenario isn't supported.</span></span>

### <a name="conflict-resolution"></a><span data-ttu-id="362c1-146">競合の解決</span><span class="sxs-lookup"><span data-stu-id="362c1-146">Conflict resolution</span></span>

<span data-ttu-id="362c1-147">検証ポリシーは、共有ポリシーが有効な場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="362c1-147">Validation rules are run when a sharing policy is enabled.</span></span> <span data-ttu-id="362c1-148">不整合が検出された場合、システムを実装するユーザーがどの会社のレコードが優先されるかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="362c1-148">If inconsistencies are detected, the user who implements the system can choose which records from which company should win.</span></span>

### <a name="considerations-for-successful-data-sharing"></a><span data-ttu-id="362c1-149">データ共有を成功させるための注意事項</span><span class="sxs-lookup"><span data-stu-id="362c1-149">Considerations for successful data sharing</span></span>

<span data-ttu-id="362c1-150">Microsoft データ パッケージの複数のエンティティに、エンティティを有効にするときに考慮する必要があるリファレンスがあります。</span><span class="sxs-lookup"><span data-stu-id="362c1-150">Several entities in the Microsoft data packages have references that you must consider when you enable the entities.</span></span> <span data-ttu-id="362c1-151">参照が一致しない場合、ポリシーを共有する一部のデータを有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="362c1-151">Some data sharing policies can't be enabled if references don't match.</span></span> <span data-ttu-id="362c1-152">他のポリシーを有効にすることができますが、不整合検出チェック ツールを使用して、データが一貫していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="362c1-152">Other policies can be enabled, but you should use the Find inconsistency checker tool to verify that your data is consistent.</span></span> <span data-ttu-id="362c1-153">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="362c1-153">Here are some examples:</span></span>

-   <span data-ttu-id="362c1-154">生産グループ共有ポリシーには、会社の勘定科目表への参照があります。</span><span class="sxs-lookup"><span data-stu-id="362c1-154">The Production group sharing policy has a reference to a company's chart of accounts.</span></span> <span data-ttu-id="362c1-155">したがって、この共有ポリシーに追加されたすべての企業は、同じ勘定科目表を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="362c1-155">Therefore, all companies that are added to this sharing policy must use the same chart of accounts.</span></span>
-   <span data-ttu-id="362c1-156">番号シーケンスを使用するエンティティを有効にする場合、番号シーケンス タイプは、それらのエンティティの共有ポリシーにおいて、すべての企業で同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="362c1-156">If you want to enable entities that use number sequences, the number sequence types must be the same across all companies in a sharing policy for those entities.</span></span>
-   <span data-ttu-id="362c1-157">設定オプションは、共有ポリシーに関連する会社間で同じでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="362c1-157">Setup options must be the same across the companies that are involved in the sharing policy.</span></span> <span data-ttu-id="362c1-158">設定オプションの例には、税金が既定で含まれるかどうかを指定する設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="362c1-158">Examples of setup options include the setting that specifies whether tax is included by default.</span></span>

## <a name="when-should-i-use-cross-company-data-sharing"></a><span data-ttu-id="362c1-159">会社間のデータ共有をいつ使用すればよいでしょうか ?</span><span class="sxs-lookup"><span data-stu-id="362c1-159">When should I use cross-company data sharing?</span></span>
<span data-ttu-id="362c1-160">次の業務シナリオでは、会社間データ共有を使用します。</span><span class="sxs-lookup"><span data-stu-id="362c1-160">Use cross-company data sharing for the following business scenarios:</span></span>

-   <span data-ttu-id="362c1-161">1 つの配置の単純な参照とグループのデータの共有</span><span class="sxs-lookup"><span data-stu-id="362c1-161">Sharing of simple reference and group data in a single deployment</span></span>
-   <span data-ttu-id="362c1-162">構成が非常に似ている会社間で共有</span><span class="sxs-lookup"><span data-stu-id="362c1-162">Sharing among companies that have very similar configurations</span></span>
-   <span data-ttu-id="362c1-163">Microsoft が明示的にテスト済みのシナリオを共有</span><span class="sxs-lookup"><span data-stu-id="362c1-163">Sharing scenarios that have been explicitly tested by Microsoft</span></span>

<span data-ttu-id="362c1-164">会社間のデータの共有は、次のシナリオではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="362c1-164">Cross-company data sharing isn't supported for the following scenarios:</span></span>

-   <span data-ttu-id="362c1-165">多くの会社間で共有される多くのレコードのある、ソリューションのフランチャイズ化。</span><span class="sxs-lookup"><span data-stu-id="362c1-165">Franchising solutions, where thousands of records are shared across thousands of companies.</span></span>
-   <span data-ttu-id="362c1-166">連結など、レポートまたは管理目的のトランザクション レコードの共有。</span><span class="sxs-lookup"><span data-stu-id="362c1-166">Sharing of transactional records for reporting or management purposes, such as consolidations.</span></span>
-   <span data-ttu-id="362c1-167">配置間で共有。</span><span class="sxs-lookup"><span data-stu-id="362c1-167">Sharing across deployments.</span></span>
-   <span data-ttu-id="362c1-168">サブタイプ/スーパータイプ テーブルまたは日付の有効性ルールを持つテーブルの複製などの複雑なシナリオ。</span><span class="sxs-lookup"><span data-stu-id="362c1-168">Complex scenarios, such as replication of subtype/supertype tables or tables that have date effectivity rules.</span></span>
-   <span data-ttu-id="362c1-169">一意なインデックスを持たないテーブル。</span><span class="sxs-lookup"><span data-stu-id="362c1-169">Tables that do not have a unique index.</span></span> 


## <a name="customer-and-vendor-master-data-sharing"></a><span data-ttu-id="362c1-170">顧客および仕入先のマスター データの共有</span><span class="sxs-lookup"><span data-stu-id="362c1-170">Customer and vendor master data sharing</span></span>
<span data-ttu-id="362c1-171">顧客および仕入先のマスタ データ共有により、複数の会社間で顧客および仕入先のデータを共有することができます。</span><span class="sxs-lookup"><span data-stu-id="362c1-171">Customer and vendor master data sharing allows you to share customer and vendor data across multiple companies.</span></span> <span data-ttu-id="362c1-172">この機能に関してご検討されている場合は、[データ共有申請](https://aka.ms/MSDYN365FODataSharing)に記入して、サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="362c1-172">If you would like to be considered for this feature, complete the [Data sharing application](https://aka.ms/MSDYN365FODataSharing) and contact Support.</span></span>

<span data-ttu-id="362c1-173">バージョン 10.0.12 のプラットフォーム更新プログラムがリリースされたため、**機能管理**モジュールの**マスター会社共有**機能を使用して、顧客および仕入先のマスター データ共有を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="362c1-173">With the release of Platform update for version 10.0.12, customer and vendor master data sharing can be enabled using the **Master company sharing** feature in the **Feature management** module.</span></span> <span data-ttu-id="362c1-174">最初にアンケートを記入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="362c1-174">There is no need to complete a survey first.</span></span> <span data-ttu-id="362c1-175">上で述べたレコードおよび会社の数の制限を考慮することが重要です。</span><span class="sxs-lookup"><span data-stu-id="362c1-175">It is important to consider limits in the number of records and companies stated above.</span></span>

> [!NOTE]
> <span data-ttu-id="362c1-176">顧客または仕入先に対する既定の分析コードの設定は、会社間で共有することはできません。</span><span class="sxs-lookup"><span data-stu-id="362c1-176">Default dimensions set up against a customer or vendor cannot be shared across companies.</span></span> <span data-ttu-id="362c1-177">会社間のデータ共有用に顧客または仕入先レコードの構成すると、**DefaultDimension**フィールドが無効になり、データ共有ポリシーに含まれることができません。</span><span class="sxs-lookup"><span data-stu-id="362c1-177">When configuring the customer or vendor record for cross-company data sharing, the **DefaultDimension** field is disabled, and cannot be included in the data sharing policy.</span></span>

> <span data-ttu-id="362c1-178">既定の分析コードには、背景の分析コード データに対する緩い外部キー参照が保持されます。これは、会社固有のデータと非会社固有のデータの両方を参照できます。</span><span class="sxs-lookup"><span data-stu-id="362c1-178">Default dimensions hold a loose foreign key reference to the backing dimension data, which can reference both company-specific and non-company specific data.</span></span> <span data-ttu-id="362c1-179">各分析コード値に適用される適切なアクションを決定することは本質的に複雑であり、現在の実装からの変更が必要です。これは、パフォーマンスに大幅な影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="362c1-179">Determining the appropriate action to be taken for each dimension value has inherent complexity and would require a change from the current implementation, which could dramatically impact performance.</span></span>

## <a name="download-a-cross-company-data-sharing-template-from-lcs"></a><span data-ttu-id="362c1-180">会社間データ 供給テンプレートを LCS からダウンロード</span><span class="sxs-lookup"><span data-stu-id="362c1-180">Download a cross-company data sharing template from LCS</span></span>
1.  <span data-ttu-id="362c1-181">LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="362c1-181">Sign in to LCS.</span></span>
2.  <span data-ttu-id="362c1-182">ホーム ページで、**共有アセット ライブラリ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="362c1-182">On the home page, click **Shared asset library**.</span></span>
3.  <span data-ttu-id="362c1-183">**資産タイプ** リストで、**データ パッケージ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="362c1-183">In the **Asset type** list, click **Data package**.</span></span>
4.  <span data-ttu-id="362c1-184">使用可能なデータ パッケージ ファイルのいずれかをクリックしてダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="362c1-184">Click any of the available data package files to download them.</span></span>

<span data-ttu-id="362c1-185">テンプレートの使用方法の詳細については、 [会社間で財務データの共有を構成する](../data-entities/tasks/configure-financial-cross-company-data-sharing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="362c1-185">For details about how to use a template, see [Configure financial cross-company data sharing](../data-entities/tasks/configure-financial-cross-company-data-sharing.md).</span></span>

## <a name="currently-supported-cross-company-data-sharing-templates"></a><span data-ttu-id="362c1-186">現時点では、会社間のデータ共有テンプレートがサポートされています</span><span class="sxs-lookup"><span data-stu-id="362c1-186">Currently supported cross-company data sharing templates</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="362c1-187">LCS でのパッケージ名</span><span class="sxs-lookup"><span data-stu-id="362c1-187">Package name on LCS</span></span></th>
<th><span data-ttu-id="362c1-188">データ共有ポリシー</span><span class="sxs-lookup"><span data-stu-id="362c1-188">Data sharing policies</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="362c1-189">テンプレートを共有する財務データ</span><span class="sxs-lookup"><span data-stu-id="362c1-189">Financial data sharing templates</span></span></td>
<td><ul>
<li><span data-ttu-id="362c1-190">銀行パラメーター</span><span class="sxs-lookup"><span data-stu-id="362c1-190">Bank parameters</span></span></li>
<li><span data-ttu-id="362c1-191">仕訳元帳の名前</span><span class="sxs-lookup"><span data-stu-id="362c1-191">Ledger journal names</span></span></li>
<li><span data-ttu-id="362c1-192">支払期日</span><span class="sxs-lookup"><span data-stu-id="362c1-192">Payment days</span></span></li>
<li><span data-ttu-id="362c1-193">支払スケジュール</span><span class="sxs-lookup"><span data-stu-id="362c1-193">Payment schedules</span></span></li>
<li><span data-ttu-id="362c1-194">支払条件</span><span class="sxs-lookup"><span data-stu-id="362c1-194">Payment terms</span></span></li>
<li><span data-ttu-id="362c1-195">非課税コード</span><span class="sxs-lookup"><span data-stu-id="362c1-195">Tax exempt codes</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="362c1-196">サプライ チェーン データ共有テンプレート</span><span class="sxs-lookup"><span data-stu-id="362c1-196">Supply chain data sharing templates</span></span></td>
<td><ul>
<li><span data-ttu-id="362c1-197">バーコード パラメーター</span><span class="sxs-lookup"><span data-stu-id="362c1-197">Barcode parameters</span></span></li>
<li><span data-ttu-id="362c1-198">バーコード設定</span><span class="sxs-lookup"><span data-stu-id="362c1-198">Barcode setup</span></span></li>
<li><span data-ttu-id="362c1-199">購入担当グループ</span><span class="sxs-lookup"><span data-stu-id="362c1-199">Buyer group</span></span></li>
<li><span data-ttu-id="362c1-200">諸掛グループ</span><span class="sxs-lookup"><span data-stu-id="362c1-200">Charges group</span></span></li>
<li><span data-ttu-id="362c1-201">コミッション</span><span class="sxs-lookup"><span data-stu-id="362c1-201">Commission</span></span></li>
<li><span data-ttu-id="362c1-202">出荷先コード</span><span class="sxs-lookup"><span data-stu-id="362c1-202">Destination code</span></span></li>
<li><span data-ttu-id="362c1-203">不適合タイプ</span><span class="sxs-lookup"><span data-stu-id="362c1-203">Non-conformance type</span></span></li>
<li><span data-ttu-id="362c1-204">注文入力期限グループ</span><span class="sxs-lookup"><span data-stu-id="362c1-204">Order entry deadline group</span></span></li>
<li><span data-ttu-id="362c1-205">発注元コード</span><span class="sxs-lookup"><span data-stu-id="362c1-205">Order origin code</span></span></li>
<li><span data-ttu-id="362c1-206">注文管理グループ</span><span class="sxs-lookup"><span data-stu-id="362c1-206">Order pool</span></span></li>
<li><span data-ttu-id="362c1-207">生産グループ</span><span class="sxs-lookup"><span data-stu-id="362c1-207">Production group</span></span></li>
<li><span data-ttu-id="362c1-208">生産管理グループ</span><span class="sxs-lookup"><span data-stu-id="362c1-208">Production pool</span></span></li>
<li><span data-ttu-id="362c1-209">配送の理由</span><span class="sxs-lookup"><span data-stu-id="362c1-209">Reason for delivery</span></span></li>
<li><span data-ttu-id="362c1-210">提供品グループ</span><span class="sxs-lookup"><span data-stu-id="362c1-210">Supplementary item group</span></span></li>
<li><span data-ttu-id="362c1-211">配送条件</span><span class="sxs-lookup"><span data-stu-id="362c1-211">Terms of delivery</span></span></li>
<li><span data-ttu-id="362c1-212">作業時間カレンダー</span><span class="sxs-lookup"><span data-stu-id="362c1-212">Work time calendar</span></span></li>
</ul></td>
</tr>
</tbody>
</table>


<a name="additional-resources"></a><span data-ttu-id="362c1-213">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="362c1-213">Additional resources</span></span>
--------

[<span data-ttu-id="362c1-214">会社間財務データ共有を構成する (タスクガイド)</span><span class="sxs-lookup"><span data-stu-id="362c1-214">Configure financial cross-company data sharing (Task guide)</span></span>](../data-entities/tasks/configure-financial-cross-company-data-sharing.md)



