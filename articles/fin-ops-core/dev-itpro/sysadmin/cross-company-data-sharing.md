---
title: 会社間データ共有
description: このトピックでは、配置において参照データおよびグループ データを会社間で共有するためのメカニズムである会社間データ共有について説明します。
author: peakerbl
ms.date: 06/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysDataSharingConfiguration
audience: IT Pro
ms.reviewer: kfend
ms.custom: 89071
ms.assetid: 0bbe7453-624f-4551-a1d0-842484067311
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 7a3d8d2ee6b16ffcba1192961b6074dcccbeb54e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189800"
---
# <a name="cross-company-data-sharing"></a><span data-ttu-id="1a8ff-103">会社間データ共有</span><span class="sxs-lookup"><span data-stu-id="1a8ff-103">Cross-company data sharing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a8ff-104">このトピックでは、企業間のデータ共有について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-104">This topic provides information about cross-company data sharing.</span></span> <span data-ttu-id="1a8ff-105">会社間共有は、Finance and Operations 展開で、参照およびグループ データを会社間で共有するためのメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-105">Cross-company sharing is a mechanism for sharing reference and group data among companies in a Finance and Operations deployment.</span></span> <span data-ttu-id="1a8ff-106">この機能は、Microsoft Dynamics AX 2012 の仮想会社機能に似ています。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-106">This feature resembles the virtual companies feature in Microsoft Dynamics AX 2012.</span></span>

## <a name="what-is-this-feature-and-how-does-it-work"></a><span data-ttu-id="1a8ff-107">これはどういう機能で、どのように動作しますか ?</span><span class="sxs-lookup"><span data-stu-id="1a8ff-107">What is this feature and how does it work?</span></span>

<span data-ttu-id="1a8ff-108">会社間のデータの共有を使用すると、会社間で参照およびグループのデータをレプリケート (共有) できます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-108">Cross-company data sharing lets you replicate (share) reference and group data among companies.</span></span> <span data-ttu-id="1a8ff-109">レプリケーションが行われる前にデータの整合性が確認されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-109">Data integrity is verified before replication occurs.</span></span> 

<span data-ttu-id="1a8ff-110">会社間のデータ共有と基本的なロジックの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-110">Here are some examples of cross-company data sharing and the basic logic:</span></span>

-   <span data-ttu-id="1a8ff-111">同じ支払条件と支払日定義が 15 の法人に使用されています。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-111">The same payment terms and payment day definitions are used across 15 legal entities.</span></span>
-   <span data-ttu-id="1a8ff-112">3 つの国/地域の 7 つの法人に、同じ配送条件が適用されています。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-112">The same terms of delivery are used across seven legal entities in three countries/regions.</span></span>
-   <span data-ttu-id="1a8ff-113">ポリシー内のいずれかの会社で作成、更新、削除されたレコードは、すべての会社で直ちにレプリケートされます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-113">Records created, updated, and deleted in any of the companies within the policy will be replicated immediately, across all the companies.</span></span>
-   <span data-ttu-id="1a8ff-114">共有対象として選択されていないフィールドは、各会社で保持され、レプリケーションはトリガーされません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-114">Fields that are not selected for sharing are maintained in each company and will not trigger any replication.</span></span>
-   <span data-ttu-id="1a8ff-115">ポリシーを有効にする際に、既存のレコードをコピーすることを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-115">As part of enabling a policy, it is optional to copy any existing records.</span></span>


<span data-ttu-id="1a8ff-116">会社間のデータの共有には、次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-116">Cross-company data sharing has the following limitations:</span></span>

-   <span data-ttu-id="1a8ff-117">会社間でトランザクション データを共有するために使用できません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-117">It can’t be used to share transactional data between companies.</span></span>
-   <span data-ttu-id="1a8ff-118">参照データとグループ データのみを共有するか、有効に設定されているテーブルのみを共有することができます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-118">Only reference and group data can be shared, or tables that have specifically been enabled.</span></span> <span data-ttu-id="1a8ff-119">たとえば、**データ共有タイプ** が **複製** に設定されているとします。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-119">For example, **Data Sharing Type** is set to **Duplicate**.</span></span>
-   <span data-ttu-id="1a8ff-120">ジョブごとに合計 100 万レコード未満のレプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-120">It supports replication of fewer than one million total records per job.</span></span> <span data-ttu-id="1a8ff-121">この合計は、共有レコードの数 × 共有会社の数として計算されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-121">This total is calculated as the number of shared records × the number of shared companies.</span></span> <span data-ttu-id="1a8ff-122">バージョン 10.0.10 のプラットフォーム更新から、制限が 200 万レコードまで拡張されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-122">The limit is increased to two million records from the Platform Update for version 10.0.10.</span></span>
-   <span data-ttu-id="1a8ff-123">ポリシーあたり最大で 100 社のレプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-123">It supports replication for up to 100 companies per policy.</span></span> <span data-ttu-id="1a8ff-124">バージョン 10.0.10 のプラットフォーム更新から、制限が 300 社まで拡張されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-124">The limit is increased to 300 companies from the Platform Update for version 10.0.10.</span></span>
-   <span data-ttu-id="1a8ff-125">子の関係の1 つのレベルだけが公開されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-125">Only one level of child relationships is exposed.</span></span> <span data-ttu-id="1a8ff-126">データの一貫性を保護するため、別のレベルが必要な場合、レプリケーションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-126">To protect data consistency, replication doesn't occur if another level is required.</span></span>
-   <span data-ttu-id="1a8ff-127">財務分析コードを参照するフィールド (たとえば、**元帳** または **既定** 分析コード) は、複数の会社間で共有することはできません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-127">Fields that reference Financial dimensions, for example **Ledger** or **Default** dimension, can't be shared across companies.</span></span> 
      <span data-ttu-id="1a8ff-128">分析コードには、背景の分析コード データに対する緩い外部キー参照が保持されます。これは、会社固有のデータと非会社固有のデータの両方を参照できます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-128">o Dimensions hold a loose foreign key reference to the backing dimension data, which can reference both company-specific and non-company specific data.</span></span> <span data-ttu-id="1a8ff-129">各分析コード値に適用される適切なアクションを決定することは本質的に複雑であり、現在の実装からの変更が必要です。これは、パフォーマンスに大幅な影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-129">Determining the appropriate action to be taken for each dimension value has inherent complexity and would require a change from the current implementation, which could dramatically impact performance.</span></span>
-   <span data-ttu-id="1a8ff-130">[二重書き込み](../data-entities/dual-write/dual-write-home-page.md) と共に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-130">It can’t be used with [dual-write](../data-entities/dual-write/dual-write-home-page.md).</span></span>


### <a name="policies"></a><span data-ttu-id="1a8ff-131">ポリシー</span><span class="sxs-lookup"><span data-stu-id="1a8ff-131">Policies</span></span>

<span data-ttu-id="1a8ff-132">データ共有は、データ パッケージに保存された定義済みポリシーによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-132">Data sharing is managed by defined policies that are saved in data packages.</span></span> <span data-ttu-id="1a8ff-133">Microsoft がテスト済みでサポートしているテンプレートは、Microsoft Dynamics Lifecycle Services (LCS) でダウンロード可能なデータ パッケージとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-133">Templates that Microsoft has tested and supports are available as downloadable data packages on Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="1a8ff-134">ポリシーでは、データ共有の次の側面を制御できます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-134">Policies let you control the following aspects of data sharing:</span></span>

-   <span data-ttu-id="1a8ff-135">複製されるフィールド</span><span class="sxs-lookup"><span data-stu-id="1a8ff-135">The fields that are replicated</span></span>
-   <span data-ttu-id="1a8ff-136">レプリケーションに参加するエンティティ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-136">The entities that participate in the replication</span></span>
-   <span data-ttu-id="1a8ff-137">共有に参加している会社</span><span class="sxs-lookup"><span data-stu-id="1a8ff-137">The companies that participates in the sharing</span></span>

<span data-ttu-id="1a8ff-138">会社とテーブルは、1 つのポリシーのみで使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-138">The same company and table can only be in one policy.</span></span> <span data-ttu-id="1a8ff-139">同じテーブルを複数のポリシーで共有することもできます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-139">It is possible to share the same table in more than policy.</span></span> <span data-ttu-id="1a8ff-140">これは、レコードまたは会社の制限に達した場合や、異なる国や地域に対して共有する必要があるテーブルに対してポリシーを作成する場合に当てはまる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-140">This can happen when the limits of records or companies are reached, or to create policies for tables that need to be shared differently for different country/regions.</span></span> 

> [!NOTE]
> <span data-ttu-id="1a8ff-141">既定では、必要な外部キー フィールドのみが選択されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-141">Only required foreign key fields are selected by default.</span></span> <span data-ttu-id="1a8ff-142">オプションの外部キーを手動で選択して追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-142">Optional foreign keys need to be selected manually to be included.</span></span> <span data-ttu-id="1a8ff-143">テーブルが追加されていない場合は、外部キー フィールドを選択するときに 1 つ以上のテーブルを追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-143">The best practice is to add one or more tables when selecting a foreign key field, unless the table has already been added.</span></span>

<span data-ttu-id="1a8ff-144">Microsoft がテスト済みでサポートしているポリシー テンプレートは、Lifecycle Services (LCS) でダウンロード可能なデータ パッケージとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-144">Policy templates that Microsoft has tested and supports are available as downloadable data packages on Lifecycle Services (LCS).</span></span> 


> [!IMPORTANT]
> <span data-ttu-id="1a8ff-145">顧客は、LCS から使用可能な Microsoft データ テンプレートを変更できますが、このシナリオには対応していません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-145">Although customers can modify the Microsoft data templates that are available from LCS, this scenario isn't supported.</span></span>

### <a name="conflict-resolution"></a><span data-ttu-id="1a8ff-146">競合の解決</span><span class="sxs-lookup"><span data-stu-id="1a8ff-146">Conflict resolution</span></span>

<span data-ttu-id="1a8ff-147">検証ポリシーは、共有ポリシーが有効な場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-147">Validation rules are run when a sharing policy is enabled.</span></span> <span data-ttu-id="1a8ff-148">不整合が検出された場合、システムを実装するユーザーがどの会社のレコードが優先されるかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-148">If inconsistencies are detected, the user who implements the system can choose which records from which company should win.</span></span>

### <a name="considerations-for-successful-data-sharing"></a><span data-ttu-id="1a8ff-149">データ共有を成功させるための注意事項</span><span class="sxs-lookup"><span data-stu-id="1a8ff-149">Considerations for successful data sharing</span></span>

<span data-ttu-id="1a8ff-150">Microsoft データ パッケージの複数のエンティティに、エンティティを有効にするときに考慮する必要があるリファレンスがあります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-150">Several entities in the Microsoft data packages have references that you must consider when you enable the entities.</span></span> <span data-ttu-id="1a8ff-151">参照が一致しない場合、ポリシーを共有する一部のデータを有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-151">Some data sharing policies can't be enabled if references don't match.</span></span> <span data-ttu-id="1a8ff-152">他のポリシーを有効にすることができますが、不整合検出チェック ツールを使用して、データが一貫していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-152">Other policies can be enabled, but you should use the Find inconsistency checker tool to verify that your data is consistent.</span></span> <span data-ttu-id="1a8ff-153">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-153">Here are some examples:</span></span>

-   <span data-ttu-id="1a8ff-154">生産グループ共有ポリシーには、会社の勘定科目表への参照があります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-154">The Production group sharing policy has a reference to a company's chart of accounts.</span></span> <span data-ttu-id="1a8ff-155">したがって、この共有ポリシーに追加されたすべての企業は、同じ勘定科目表を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-155">Therefore, all companies that are added to this sharing policy must use the same chart of accounts.</span></span>
-   <span data-ttu-id="1a8ff-156">番号シーケンスを使用するエンティティを有効にする場合、番号シーケンス タイプは、それらのエンティティの共有ポリシーにおいて、すべての企業で同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-156">If you want to enable entities that use number sequences, the number sequence types must be the same across all companies in a sharing policy for those entities.</span></span>
-   <span data-ttu-id="1a8ff-157">設定オプションは、共有ポリシーに関連する会社間で同じでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-157">Setup options must be the same across the companies that are involved in the sharing policy.</span></span> <span data-ttu-id="1a8ff-158">設定オプションの例には、税金が既定で含まれるかどうかを指定する設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-158">Examples of setup options include the setting that specifies whether tax is included by default.</span></span>

## <a name="when-should-i-use-cross-company-data-sharing"></a><span data-ttu-id="1a8ff-159">会社間のデータ共有をいつ使用すればよいでしょうか ?</span><span class="sxs-lookup"><span data-stu-id="1a8ff-159">When should I use cross-company data sharing?</span></span>
<span data-ttu-id="1a8ff-160">次の業務シナリオでは、会社間データ共有を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-160">Use cross-company data sharing for the following business scenarios:</span></span>

-   <span data-ttu-id="1a8ff-161">1 つの配置の単純な参照とグループのデータの共有</span><span class="sxs-lookup"><span data-stu-id="1a8ff-161">Sharing of simple reference and group data in a single deployment</span></span>
-   <span data-ttu-id="1a8ff-162">構成が非常に似ている会社間で共有</span><span class="sxs-lookup"><span data-stu-id="1a8ff-162">Sharing among companies that have very similar configurations</span></span>
-   <span data-ttu-id="1a8ff-163">Microsoft が明示的にテスト済みのシナリオを共有</span><span class="sxs-lookup"><span data-stu-id="1a8ff-163">Sharing scenarios that have been explicitly tested by Microsoft</span></span>

<span data-ttu-id="1a8ff-164">会社間のデータの共有は、次のシナリオではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-164">Cross-company data sharing isn't supported for the following scenarios:</span></span>

-   <span data-ttu-id="1a8ff-165">多くの会社間で共有される多くのレコードのある、ソリューションのフランチャイズ化。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-165">Franchising solutions, where thousands of records are shared across thousands of companies.</span></span>
-   <span data-ttu-id="1a8ff-166">連結など、レポートまたは管理目的のトランザクション レコードの共有。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-166">Sharing of transactional records for reporting or management purposes, such as consolidations.</span></span>
-   <span data-ttu-id="1a8ff-167">配置間で共有。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-167">Sharing across deployments.</span></span>
-   <span data-ttu-id="1a8ff-168">サブタイプ/スーパータイプ テーブルまたは日付の有効性ルールを持つテーブルの複製などの複雑なシナリオ。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-168">Complex scenarios, such as replication of subtype/supertype tables or tables that have date effectivity rules.</span></span>
-   <span data-ttu-id="1a8ff-169">一意なインデックスを持たないテーブル。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-169">Tables that do not have a unique index.</span></span> 


## <a name="customer-and-vendor-master-data-sharing"></a><span data-ttu-id="1a8ff-170">顧客および仕入先のマスター データの共有</span><span class="sxs-lookup"><span data-stu-id="1a8ff-170">Customer and vendor master data sharing</span></span>
<span data-ttu-id="1a8ff-171">顧客および仕入先のマスタ データ共有により、複数の会社間で顧客および仕入先のデータを共有することができます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-171">Customer and vendor master data sharing allows you to share customer and vendor data across multiple companies.</span></span> <span data-ttu-id="1a8ff-172">この機能に関してご検討されている場合は、[データ共有申請](https://aka.ms/MSDYN365FODataSharing)に記入して、サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-172">If you would like to be considered for this feature, complete the [Data sharing application](https://aka.ms/MSDYN365FODataSharing) and contact Support.</span></span>

<span data-ttu-id="1a8ff-173">バージョン 10.0.12 のプラットフォーム更新プログラムがリリースされたため、**機能管理** モジュールの **顧客および仕入先のマスター データ共有** 機能を使用して、顧客および仕入先のマスター データ共有を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-173">With the release of Platform update for version 10.0.12, customer and vendor master data sharing can be enabled using the **Customer and vendor master data sharing** feature in the **Feature management** module.</span></span> <span data-ttu-id="1a8ff-174">最初にアンケートを記入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-174">There is no need to complete a survey first.</span></span> <span data-ttu-id="1a8ff-175">上で述べたレコードおよび会社の数の制限を考慮することが重要です。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-175">It is important to consider limits in the number of records and companies stated above.</span></span>

> [!NOTE]
> <span data-ttu-id="1a8ff-176">顧客または仕入先に対する既定の分析コードの設定は、会社間で共有することはできません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-176">Default dimensions set up against a customer or vendor cannot be shared across companies.</span></span> <span data-ttu-id="1a8ff-177">会社間のデータ共有用に顧客または仕入先レコードの構成すると、**DefaultDimension** フィールドが無効になり、データ共有ポリシーに含まれることができません。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-177">When configuring the customer or vendor record for cross-company data sharing, the **DefaultDimension** field is disabled, and cannot be included in the data sharing policy.</span></span>

> <span data-ttu-id="1a8ff-178">既定の分析コードには、背景の分析コード データに対する緩い外部キー参照が保持されます。これは、会社固有のデータと非会社固有のデータの両方を参照できます。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-178">Default dimensions hold a loose foreign key reference to the backing dimension data, which can reference both company-specific and non-company specific data.</span></span> <span data-ttu-id="1a8ff-179">各分析コード値に適用される適切なアクションを決定することは本質的に複雑であり、現在の実装からの変更が必要です。これは、パフォーマンスに大幅な影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-179">Determining the appropriate action to be taken for each dimension value has inherent complexity and would require a change from the current implementation, which could dramatically impact performance.</span></span>

## <a name="download-a-cross-company-data-sharing-template-from-lcs"></a><span data-ttu-id="1a8ff-180">会社間データ 供給テンプレートを LCS からダウンロード</span><span class="sxs-lookup"><span data-stu-id="1a8ff-180">Download a cross-company data sharing template from LCS</span></span>
1.  <span data-ttu-id="1a8ff-181">LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-181">Sign in to LCS.</span></span>
2.  <span data-ttu-id="1a8ff-182">ホーム ページで、**共有アセット ライブラリ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-182">On the home page, click **Shared asset library**.</span></span>
3.  <span data-ttu-id="1a8ff-183">**資産タイプ** リストで、**データ パッケージ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-183">In the **Asset type** list, click **Data package**.</span></span>
4.  <span data-ttu-id="1a8ff-184">使用可能なデータ パッケージ ファイルのいずれかをクリックしてダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-184">Click any of the available data package files to download them.</span></span>

<span data-ttu-id="1a8ff-185">テンプレートの使用方法の詳細については、 [会社間で財務データの共有を構成する](../data-entities/tasks/configure-financial-cross-company-data-sharing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1a8ff-185">For details about how to use a template, see [Configure financial cross-company data sharing](../data-entities/tasks/configure-financial-cross-company-data-sharing.md).</span></span>

## <a name="currently-supported-cross-company-data-sharing-templates"></a><span data-ttu-id="1a8ff-186">現時点では、会社間のデータ共有テンプレートがサポートされています</span><span class="sxs-lookup"><span data-stu-id="1a8ff-186">Currently supported cross-company data sharing templates</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1a8ff-187">LCS でのパッケージ名</span><span class="sxs-lookup"><span data-stu-id="1a8ff-187">Package name on LCS</span></span></th>
<th><span data-ttu-id="1a8ff-188">データ共有ポリシー</span><span class="sxs-lookup"><span data-stu-id="1a8ff-188">Data sharing policies</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a8ff-189">テンプレートを共有する財務データ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-189">Financial data sharing templates</span></span></td>
<td><ul>
<li><span data-ttu-id="1a8ff-190">銀行パラメーター</span><span class="sxs-lookup"><span data-stu-id="1a8ff-190">Bank parameters</span></span></li>
<li><span data-ttu-id="1a8ff-191">仕訳元帳の名前</span><span class="sxs-lookup"><span data-stu-id="1a8ff-191">Ledger journal names</span></span></li>
<li><span data-ttu-id="1a8ff-192">支払期日</span><span class="sxs-lookup"><span data-stu-id="1a8ff-192">Payment days</span></span></li>
<li><span data-ttu-id="1a8ff-193">支払スケジュール</span><span class="sxs-lookup"><span data-stu-id="1a8ff-193">Payment schedules</span></span></li>
<li><span data-ttu-id="1a8ff-194">支払条件</span><span class="sxs-lookup"><span data-stu-id="1a8ff-194">Payment terms</span></span></li>
<li><span data-ttu-id="1a8ff-195">非課税コード</span><span class="sxs-lookup"><span data-stu-id="1a8ff-195">Tax exempt codes</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a8ff-196">サプライ チェーン データ共有テンプレート</span><span class="sxs-lookup"><span data-stu-id="1a8ff-196">Supply chain data sharing templates</span></span></td>
<td><ul>
<li><span data-ttu-id="1a8ff-197">バーコード パラメーター</span><span class="sxs-lookup"><span data-stu-id="1a8ff-197">Barcode parameters</span></span></li>
<li><span data-ttu-id="1a8ff-198">バーコード設定</span><span class="sxs-lookup"><span data-stu-id="1a8ff-198">Barcode setup</span></span></li>
<li><span data-ttu-id="1a8ff-199">購入担当グループ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-199">Buyer group</span></span></li>
<li><span data-ttu-id="1a8ff-200">諸掛グループ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-200">Charges group</span></span></li>
<li><span data-ttu-id="1a8ff-201">コミッション</span><span class="sxs-lookup"><span data-stu-id="1a8ff-201">Commission</span></span></li>
<li><span data-ttu-id="1a8ff-202">出荷先コード</span><span class="sxs-lookup"><span data-stu-id="1a8ff-202">Destination code</span></span></li>
<li><span data-ttu-id="1a8ff-203">不適合タイプ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-203">Non-conformance type</span></span></li>
<li><span data-ttu-id="1a8ff-204">注文入力期限グループ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-204">Order entry deadline group</span></span></li>
<li><span data-ttu-id="1a8ff-205">発注元コード</span><span class="sxs-lookup"><span data-stu-id="1a8ff-205">Order origin code</span></span></li>
<li><span data-ttu-id="1a8ff-206">注文管理グループ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-206">Order pool</span></span></li>
<li><span data-ttu-id="1a8ff-207">生産グループ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-207">Production group</span></span></li>
<li><span data-ttu-id="1a8ff-208">生産管理グループ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-208">Production pool</span></span></li>
<li><span data-ttu-id="1a8ff-209">配送の理由</span><span class="sxs-lookup"><span data-stu-id="1a8ff-209">Reason for delivery</span></span></li>
<li><span data-ttu-id="1a8ff-210">提供品グループ</span><span class="sxs-lookup"><span data-stu-id="1a8ff-210">Supplementary item group</span></span></li>
<li><span data-ttu-id="1a8ff-211">配送条件</span><span class="sxs-lookup"><span data-stu-id="1a8ff-211">Terms of delivery</span></span></li>
<li><span data-ttu-id="1a8ff-212">作業時間カレンダー</span><span class="sxs-lookup"><span data-stu-id="1a8ff-212">Work time calendar</span></span></li>
</ul></td>
</tr>
</tbody>
</table>


## <a name="additional-resources"></a><span data-ttu-id="1a8ff-213">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="1a8ff-213">Additional resources</span></span>

[<span data-ttu-id="1a8ff-214">会社間財務データ共有を構成する (タスクガイド)</span><span class="sxs-lookup"><span data-stu-id="1a8ff-214">Configure financial cross-company data sharing (Task guide)</span></span>](../data-entities/tasks/configure-financial-cross-company-data-sharing.md)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]