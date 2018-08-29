---
title: "会社間データ共有"
description: "このトピックでは、企業間のデータ共有について説明します。 会社間の共有は、Microsoft Dynamics 365 for Finance and Operations 展開において、会社間で参照データとグループ データを共有するためのメカニズムです。"
author: aprilolson
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysDataSharingConfiguration
audience: IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 89071
ms.assetid: 0bbe7453-624f-4551-a1d0-842484067311
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: d0fd3a3bc73919f990bafd81688d14750a1b288b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="cross-company-data-sharing"></a><span data-ttu-id="0f166-104">会社間データ共有</span><span class="sxs-lookup"><span data-stu-id="0f166-104">Cross-company data sharing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f166-105">このトピックでは、企業間のデータ共有について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f166-105">This topic provides information about cross-company data sharing.</span></span> <span data-ttu-id="0f166-106">会社間の共有は、Microsoft Dynamics 365 for Finance and Operations 展開において、会社間で参照データとグループ データを共有するためのメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="0f166-106">Cross-company sharing is a mechanism for sharing reference and group data among companies in a Microsoft Dynamics 365 for Finance and Operations deployment.</span></span> <span data-ttu-id="0f166-107">この機能は、Microsoft Dynamics AX 2012 の仮想会社機能に似ています。</span><span class="sxs-lookup"><span data-stu-id="0f166-107">This feature resembles the virtual companies feature in Microsoft Dynamics AX 2012.</span></span>

<a name="what-is-this-feature-and-how-does-it-work"></a><span data-ttu-id="0f166-108">これはどういう機能で、どのように動作しますか ?</span><span class="sxs-lookup"><span data-stu-id="0f166-108">What is this feature and how does it work?</span></span>
------------------------------------------

<span data-ttu-id="0f166-109">会社間のデータの共有を使用すると、Finance and Operations の展開において会社間で参照データおよびグループのデータをレプリケート (共有) できます。</span><span class="sxs-lookup"><span data-stu-id="0f166-109">Cross-company data sharing lets you replicate (share) reference and group data among companies in a Finance and Operations deployment.</span></span> <span data-ttu-id="0f166-110">レプリケーションが行われる前にデータの整合性が確認されます。</span><span class="sxs-lookup"><span data-stu-id="0f166-110">Data integrity is verified before replication occurs.</span></span> 

<span data-ttu-id="0f166-111">会社間のデータ共有の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0f166-111">Here are some examples of cross-company data sharing:</span></span>

-   <span data-ttu-id="0f166-112">同じ支払条件と支払日定義が 15 の法人に使用されています。</span><span class="sxs-lookup"><span data-stu-id="0f166-112">The same payment terms and payment day definitions are used across 15 legal entities.</span></span>
-   <span data-ttu-id="0f166-113">3 つの国/地域の 7 つの法人に、同じ配送条件が適用されています。</span><span class="sxs-lookup"><span data-stu-id="0f166-113">The same terms of delivery are used across seven legal entities in three countries/regions.</span></span>

<span data-ttu-id="0f166-114">会社間のデータの共有には、次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="0f166-114">Cross-company data sharing has the following limitations:</span></span>

-   <span data-ttu-id="0f166-115">会社間でトランザクション データを共有するために使用できません。</span><span class="sxs-lookup"><span data-stu-id="0f166-115">It can’t be used to share transactional data between companies.</span></span>
-   <span data-ttu-id="0f166-116">参照データおよびグループ データだけが共有されます。</span><span class="sxs-lookup"><span data-stu-id="0f166-116">Only reference and group data can be shared.</span></span>
-   <span data-ttu-id="0f166-117">ジョブごとに合計 100 万レコード未満のレプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0f166-117">It supports replication of fewer than one million total records per job.</span></span> <span data-ttu-id="0f166-118">(この合計は、共有レコードの数 × 共有会社の数として計算されます。)</span><span class="sxs-lookup"><span data-stu-id="0f166-118">(This total is calculated as the number of shared records × the number of shared companies.)</span></span>
-   <span data-ttu-id="0f166-119">子の関係の1 つのレベルだけが公開されます。</span><span class="sxs-lookup"><span data-stu-id="0f166-119">Only one level of child relationships is exposed.</span></span> <span data-ttu-id="0f166-120">データの一貫性を保護するため、別のレベルが必要な場合、レプリケーションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="0f166-120">To protect data consistency, replication doesn't occur if another level is required.</span></span>

### <a name="policies"></a><span data-ttu-id="0f166-121">ポリシー</span><span class="sxs-lookup"><span data-stu-id="0f166-121">Policies</span></span>

<span data-ttu-id="0f166-122">データ共有は、データ パッケージに保存された定義済みポリシーによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="0f166-122">Data sharing is managed by defined policies that are saved in data packages.</span></span> <span data-ttu-id="0f166-123">Microsoft がテスト済みでサポートしているテンプレートは、Microsoft Dynamics Lifecycle Services (LCS) でダウンロード可能なデータ パッケージとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f166-123">Templates that Microsoft has tested and supports are available as downloadable data packages on Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0f166-124">ポリシーでは、データ共有の次の側面を制御できます。</span><span class="sxs-lookup"><span data-stu-id="0f166-124">Policies let you control the following aspects of data sharing:</span></span>

-   <span data-ttu-id="0f166-125">複製されるフィールド</span><span class="sxs-lookup"><span data-stu-id="0f166-125">The fields that are replicated</span></span>
-   <span data-ttu-id="0f166-126">レプリケーションに参加するエンティティ</span><span class="sxs-lookup"><span data-stu-id="0f166-126">The entities that participate in the replication</span></span>

<span data-ttu-id="0f166-127">**重要:** 顧客は、LCS から使用可能な Microsoft データ テンプレートを変更できますが、このシナリオはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0f166-127">**Important:** Although customers can modify the Microsoft data templates that are available from LCS, this scenario isn't supported.</span></span>

### <a name="conflict-resolution"></a><span data-ttu-id="0f166-128">競合の解決</span><span class="sxs-lookup"><span data-stu-id="0f166-128">Conflict resolution</span></span>

<span data-ttu-id="0f166-129">検証ポリシーは、共有ポリシーが有効な場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="0f166-129">Validation rules are run when a sharing policy is enabled.</span></span> <span data-ttu-id="0f166-130">不整合が検出された場合、システムを実装するユーザーがどの会社のレコードが優先されるかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="0f166-130">If inconsistencies are detected, the user who implements the system can choose which records from which company should win.</span></span>

### <a name="considerations-for-successful-data-sharing"></a><span data-ttu-id="0f166-131">データ共有を成功させるための注意事項</span><span class="sxs-lookup"><span data-stu-id="0f166-131">Considerations for successful data sharing</span></span>

<span data-ttu-id="0f166-132">Microsoft データ パッケージの複数のエンティティに、エンティティを有効にするときに考慮する必要があるリファレンスがあります。</span><span class="sxs-lookup"><span data-stu-id="0f166-132">Several entities in the Microsoft data packages have references that you must consider when you enable the entities.</span></span> <span data-ttu-id="0f166-133">参照が一致しない場合、ポリシーを共有する一部のデータを有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0f166-133">Some data sharing policies can't be enabled if references don't match.</span></span> <span data-ttu-id="0f166-134">他のポリシーを有効にすることができますが、不整合検出チェック ツールを使用して、データが一貫していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f166-134">Other policies can be enabled, but you should use the Find inconsistency checker tool to verify that your data is consistent.</span></span> <span data-ttu-id="0f166-135">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="0f166-135">Here are some examples:</span></span>

-   <span data-ttu-id="0f166-136">生産グループ共有ポリシーには、会社の勘定科目表への参照があります。</span><span class="sxs-lookup"><span data-stu-id="0f166-136">The Production group sharing policy has a reference to a company's chart of accounts.</span></span> <span data-ttu-id="0f166-137">したがって、この共有ポリシーに追加されたすべての企業は、同じ勘定科目表を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f166-137">Therefore, all companies that are added to this sharing policy must use the same chart of accounts.</span></span>
-   <span data-ttu-id="0f166-138">番号シーケンスを使用するエンティティを有効にする場合、番号シーケンス タイプは、それらのエンティティの共有ポリシーにおいて、すべての企業で同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f166-138">If you want to enable entities that use number sequences, the number sequence types must be the same across all companies in a sharing policy for those entities.</span></span>
-   <span data-ttu-id="0f166-139">設定オプションは、共有ポリシーに関連する会社間で同じでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0f166-139">Setup options must be the same across the companies that are involved in the sharing policy.</span></span> <span data-ttu-id="0f166-140">設定オプションの例には、税金が既定で含まれるかどうかを指定する設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0f166-140">Examples of setup options include the setting that specifies whether tax is included by default.</span></span>

## <a name="when-should-i-use-cross-company-data-sharing"></a><span data-ttu-id="0f166-141">会社間のデータ共有をいつ使用すればよいでしょうか ?</span><span class="sxs-lookup"><span data-stu-id="0f166-141">When should I use cross-company data sharing?</span></span>
<span data-ttu-id="0f166-142">次の業務シナリオでは、会社間データ共有を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f166-142">Use cross-company data sharing for the following business scenarios:</span></span>

-   <span data-ttu-id="0f166-143">1 つの配置の単純な参照とグループのデータの共有</span><span class="sxs-lookup"><span data-stu-id="0f166-143">Sharing of simple reference and group data in a single deployment</span></span>
-   <span data-ttu-id="0f166-144">構成が非常に似ている会社間で共有</span><span class="sxs-lookup"><span data-stu-id="0f166-144">Sharing among companies that have very similar configurations</span></span>
-   <span data-ttu-id="0f166-145">Microsoft が明示的にテスト済みのシナリオを共有</span><span class="sxs-lookup"><span data-stu-id="0f166-145">Sharing scenarios that have been explicitly tested by Microsoft</span></span>

<span data-ttu-id="0f166-146">会社間のデータの共有は、次のシナリオではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0f166-146">Cross-company data sharing isn't supported for the following scenarios:</span></span>

-   <span data-ttu-id="0f166-147">多くの会社間で共有される多くのレコードのある、ソリューションのフランチャイズ化。</span><span class="sxs-lookup"><span data-stu-id="0f166-147">Franchising solutions, where thousands of records are shared across thousands of companies.</span></span>
-   <span data-ttu-id="0f166-148">連結など、レポートまたは管理目的のトランザクション レコードの共有</span><span class="sxs-lookup"><span data-stu-id="0f166-148">Sharing of transactional records for reporting or management purposes, such as consolidations</span></span>
-   <span data-ttu-id="0f166-149">配置間で共有</span><span class="sxs-lookup"><span data-stu-id="0f166-149">Sharing across deployments</span></span>
-   <span data-ttu-id="0f166-150">サブタイプ/スーパータイプ テーブルまたは日付の有効性ルールを持つテーブルの複製などの複雑なシナリオ</span><span class="sxs-lookup"><span data-stu-id="0f166-150">Complex scenarios, such as replication of subtype/supertype tables or tables that have date effectivity rules</span></span>
-   <span data-ttu-id="0f166-151">マスター データの管理</span><span class="sxs-lookup"><span data-stu-id="0f166-151">Master data management</span></span>

## <a name="download-a-cross-company-data-sharing-template-from-lcs"></a><span data-ttu-id="0f166-152">会社間データ 供給テンプレートを LCS からダウンロード</span><span class="sxs-lookup"><span data-stu-id="0f166-152">Download a cross-company data sharing template from LCS</span></span>
1.  <span data-ttu-id="0f166-153">LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="0f166-153">Sign in to LCS.</span></span>
2.  <span data-ttu-id="0f166-154">ホーム ページで、**共有アセット ライブラリ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f166-154">On the home page, click **Shared asset library**.</span></span>
3.  <span data-ttu-id="0f166-155">**資産タイプ** リストで、**データ パッケージ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f166-155">In the **Asset type** list, click **Data package**.</span></span>
4.  <span data-ttu-id="0f166-156">使用可能なデータ パッケージ ファイルのいずれかをクリックしてダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0f166-156">Click any of the available data package files to download them.</span></span>

<span data-ttu-id="0f166-157">テンプレートを使用して、Finance and Operations をコンフィギュレーションする方法の詳細については、[会社間財務データ共有のコンフィギュレーション (タスク ガイド)](../data-entities/tasks/configure-financial-cross-company-data-sharing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f166-157">For details about how to configure Finance and Operations to use a template, see [Configure financial cross-company data sharing (Task guide)](../data-entities/tasks/configure-financial-cross-company-data-sharing.md).</span></span>

## <a name="currently-supported-cross-company-data-sharing-templates"></a><span data-ttu-id="0f166-158">現時点では、会社間のデータ共有テンプレートがサポートされています</span><span class="sxs-lookup"><span data-stu-id="0f166-158">Currently supported cross-company data sharing templates</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0f166-159">LCS でのパッケージ名</span><span class="sxs-lookup"><span data-stu-id="0f166-159">Package name on LCS</span></span></th>
<th><span data-ttu-id="0f166-160">データ共有ポリシー</span><span class="sxs-lookup"><span data-stu-id="0f166-160">Data sharing policies</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f166-161">テンプレートを共有する財務データ</span><span class="sxs-lookup"><span data-stu-id="0f166-161">Financial data sharing templates</span></span></td>
<td><ul>
<li><span data-ttu-id="0f166-162">銀行パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f166-162">Bank parameters</span></span></li>
<li><span data-ttu-id="0f166-163">仕訳元帳の名前</span><span class="sxs-lookup"><span data-stu-id="0f166-163">Ledger journal names</span></span></li>
<li><span data-ttu-id="0f166-164">支払期日</span><span class="sxs-lookup"><span data-stu-id="0f166-164">Payment days</span></span></li>
<li><span data-ttu-id="0f166-165">支払スケジュール</span><span class="sxs-lookup"><span data-stu-id="0f166-165">Payment schedules</span></span></li>
<li><span data-ttu-id="0f166-166">支払条件</span><span class="sxs-lookup"><span data-stu-id="0f166-166">Payment terms</span></span></li>
<li><span data-ttu-id="0f166-167">非課税コード</span><span class="sxs-lookup"><span data-stu-id="0f166-167">Tax exempt codes</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f166-168">サプライ チェーン データ共有テンプレート</span><span class="sxs-lookup"><span data-stu-id="0f166-168">Supply chain data sharing templates</span></span></td>
<td><ul>
<li><span data-ttu-id="0f166-169">バーコード パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f166-169">Barcode parameters</span></span></li>
<li><span data-ttu-id="0f166-170">バーコード設定</span><span class="sxs-lookup"><span data-stu-id="0f166-170">Barcode setup</span></span></li>
<li><span data-ttu-id="0f166-171">購入担当グループ</span><span class="sxs-lookup"><span data-stu-id="0f166-171">Buyer group</span></span></li>
<li><span data-ttu-id="0f166-172">諸掛グループ</span><span class="sxs-lookup"><span data-stu-id="0f166-172">Charges group</span></span></li>
<li><span data-ttu-id="0f166-173">コミッション</span><span class="sxs-lookup"><span data-stu-id="0f166-173">Commission</span></span></li>
<li><span data-ttu-id="0f166-174">出荷先コード</span><span class="sxs-lookup"><span data-stu-id="0f166-174">Destination code</span></span></li>
<li><span data-ttu-id="0f166-175">不適合タイプ</span><span class="sxs-lookup"><span data-stu-id="0f166-175">Non-conformance type</span></span></li>
<li><span data-ttu-id="0f166-176">注文入力期限グループ</span><span class="sxs-lookup"><span data-stu-id="0f166-176">Order entry deadline group</span></span></li>
<li><span data-ttu-id="0f166-177">発注元コード</span><span class="sxs-lookup"><span data-stu-id="0f166-177">Order origin code</span></span></li>
<li><span data-ttu-id="0f166-178">注文管理グループ</span><span class="sxs-lookup"><span data-stu-id="0f166-178">Order pool</span></span></li>
<li><span data-ttu-id="0f166-179">生産グループ</span><span class="sxs-lookup"><span data-stu-id="0f166-179">Production group</span></span></li>
<li><span data-ttu-id="0f166-180">生産管理グループ</span><span class="sxs-lookup"><span data-stu-id="0f166-180">Production pool</span></span></li>
<li><span data-ttu-id="0f166-181">配送の理由</span><span class="sxs-lookup"><span data-stu-id="0f166-181">Reason for delivery</span></span></li>
<li><span data-ttu-id="0f166-182">提供品グループ</span><span class="sxs-lookup"><span data-stu-id="0f166-182">Supplementary item group</span></span></li>
<li><span data-ttu-id="0f166-183">配送条件</span><span class="sxs-lookup"><span data-stu-id="0f166-183">Terms of delivery</span></span></li>
<li><span data-ttu-id="0f166-184">作業時間カレンダー</span><span class="sxs-lookup"><span data-stu-id="0f166-184">Work time calendar</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="0f166-185">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="0f166-185">Additional resources</span></span>
--------

[<span data-ttu-id="0f166-186">会社間財務データ共有を構成する (タスクガイド)</span><span class="sxs-lookup"><span data-stu-id="0f166-186">Configure financial cross-company data sharing (Task guide)</span></span>](../data-entities/tasks/configure-financial-cross-company-data-sharing.md)




