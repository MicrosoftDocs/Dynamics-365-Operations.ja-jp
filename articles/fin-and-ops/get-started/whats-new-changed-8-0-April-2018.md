---
title: "Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations バージョン 8.0 の新機能または変更された機能について説明します。 このバージョンは 2018 年 4 月にリリースされました。"
author: tonyafehr
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: 
ms.assetid: b265d51c-52d1-45c5-b578-64c5242c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: c8ccd77263b32266ef28395183bff453cb411aff
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-version-80-april-2018"></a><span data-ttu-id="69169-104">Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="69169-104">What's new or changed in Dynamics 365 for Finance and Operations version 8.0 (April 2018)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="69169-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="69169-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018).</span></span> <span data-ttu-id="69169-106">このバージョンは 2018 年 4 月にリリースされ、ビルド番号は 8.0.30 です。</span><span class="sxs-lookup"><span data-stu-id="69169-106">This version was released in April 2018 and has a build number of 8.0.30.</span></span>

<span data-ttu-id="69169-107">ビジネス アプリケーションの最新の更新プログラムや、独自のアプリケーションと拡張機能をプラットフォームにビルドするための新しい機能を見つけるには、[[Dynamics 365 2018 年春リリース ノート](https://aka.ms/businessappsreleasenotes)] をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="69169-107">To discover the latest updates to our business applications, as well as a host of new capabilities for building your own applications and extensions on top of our platform, download the [Dynamics 365 Spring ’18 release notes](https://aka.ms/businessappsreleasenotes).</span></span> <span data-ttu-id="69169-108">リリース ノートでは、Dynamics 365 for Finance and Operations に含まれる新機能または変更された機能について詳細に説明します。</span><span class="sxs-lookup"><span data-stu-id="69169-108">The Release Notes provide details about the features that are either new or changed in Dynamics 365 for Finance and Operations.</span></span>

### <a name="introducing-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="69169-109">Dynamics 365 for Finance and Operations の導入</span><span class="sxs-lookup"><span data-stu-id="69169-109">Introducing Dynamics 365 for Finance and Operations</span></span>

<span data-ttu-id="69169-110">ユーザーと開発者に対して、更新された製品名、「Microsoft Dynamics 365 for Finance and Operations」が表示されます。</span><span class="sxs-lookup"><span data-stu-id="69169-110">Users and developers will see an updated product name, "Microsoft Dynamics 365 for Finance and Operations."</span></span> <span data-ttu-id="69169-111">バージョン 8.0 では Dynamics 365 製品がさらに簡素化され、顧客とエコシステムの選択がさらに簡単になります。</span><span class="sxs-lookup"><span data-stu-id="69169-111">With version 8.0, Microsoft is further simplifying our Dynamics 365 offerings and increasing ease of selection for our customers and ecosystem.</span></span> <span data-ttu-id="69169-112">今後、Microsoft は、個別エディション (Business edition および Enterprise edition) を提供しなくなるため、この Dynamics 365 アプリケーションの製品名は Microsoft Dynamics 365 for Finance and Operations になります。</span><span class="sxs-lookup"><span data-stu-id="69169-112">Going forward, Microsoft is no longer offering separate editions (Business edition and Enterprise edition), so the product name for this Dynamics 365 application is Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="business-productivity"></a><span data-ttu-id="69169-113">業務の生産性</span><span class="sxs-lookup"><span data-stu-id="69169-113">Business productivity</span></span> 

### <a name="alerts"></a><span data-ttu-id="69169-114">警告</span><span class="sxs-lookup"><span data-stu-id="69169-114">Alerts</span></span>

<span data-ttu-id="69169-115">クライアント ベースの警告機能により、請求書が支払われたときや顧客が住所を変更したときなど、ビジネス イベントに基づいて警告ルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="69169-115">Client-based alert functionality enables a user to define alert rules based on business events, such as when an invoice is paid or a customer changes an address.</span></span> <span data-ttu-id="69169-116">警告およびその作成方法の詳細については、[警告の概要](alerts-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-116">For more information about alerts and how to create them, see [Alerts overview](alerts-overview.md).</span></span>

### <a name="optimization-advisor"></a><span data-ttu-id="69169-117">最適化アドバイザー</span><span class="sxs-lookup"><span data-stu-id="69169-117">Optimization advisor</span></span>

<span data-ttu-id="69169-118">テレメトリを使用して、お客様のビジネス プロセスを分析し、最適化の可能性を探し、アプリケーション データを使用してその可能性を定量化し、ソリューションを推奨します。</span><span class="sxs-lookup"><span data-stu-id="69169-118">Uses telemetry to analyze customers’ business processes, finds optimization opportunities, uses application data to quantify the opportunities, and then recommends solutions.</span></span>

### <a name="project-timesheet-mobile"></a><span data-ttu-id="69169-119">プロジェクト タイムシート モバイル</span><span class="sxs-lookup"><span data-stu-id="69169-119">Project timesheet mobile</span></span>

<span data-ttu-id="69169-120">従業員は、プロジェクト タイムシートを作成して送信できます。</span><span class="sxs-lookup"><span data-stu-id="69169-120">Employees can create and submit project timesheets.</span></span> <span data-ttu-id="69169-121">保存したお気に入りの使用機能と、以前のタイムシートからのコピー機能により、迅速で正確な時間の入力が容易になります。</span><span class="sxs-lookup"><span data-stu-id="69169-121">The use of saved favorites and the ability to copy from a previous timesheet facilitates rapid, accurate time entry.</span></span>

### <a name="edit-default-project-fulfillment-hours"></a><span data-ttu-id="69169-122">既定のプロジェクトのフルフィルメント時間を編集</span><span class="sxs-lookup"><span data-stu-id="69169-122">Edit default project fulfillment hours</span></span>

<span data-ttu-id="69169-123">プロジェクト リソース管理者は、プロジェクトの予約調達のためのプロセスの一部として、既定の時間を編集できます。</span><span class="sxs-lookup"><span data-stu-id="69169-123">Project resource managers can edit the default hours as part of the project booking fulfillment process.</span></span>

### <a name="reserve-project-resources-past-the-task-end-date"></a><span data-ttu-id="69169-124">タスクの終了日が過ぎてからプロジェクト リソースを予約</span><span class="sxs-lookup"><span data-stu-id="69169-124">Reserve project resources past the task end date</span></span>

<span data-ttu-id="69169-125">プロジェクト リソースの管理者は、タスクの現在の計画終了日を過ぎたタスクでリソースをフルフィルメントすることができます。</span><span class="sxs-lookup"><span data-stu-id="69169-125">Project resource managers can fulfill resources on tasks past the current planned end date for the task.</span></span>

### <a name="person-search-report"></a><span data-ttu-id="69169-126">個人検索レポート</span><span class="sxs-lookup"><span data-stu-id="69169-126">Person search report</span></span>

<span data-ttu-id="69169-127">Finance and Operations 内で担当者および個人データを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="69169-127">You can find a person and their personal data in Finance and Operations.</span></span>

### <a name="data-sharing-for-customer-and-vendor-tables"></a><span data-ttu-id="69169-128">顧客および仕入先のテーブルのデータ共有</span><span class="sxs-lookup"><span data-stu-id="69169-128">Data sharing for customer and vendor tables</span></span>

<span data-ttu-id="69169-129">データは、顧客テーブルと仕入先テーブル、および複数の法人の多くの関連テーブルで共有することができます。</span><span class="sxs-lookup"><span data-stu-id="69169-129">Data can be shared across customer and vendor tables and many related tables across multiple legal entities.</span></span>

### <a name="one-voucher-deprecation"></a><span data-ttu-id="69169-130">1 つの伝票の廃止</span><span class="sxs-lookup"><span data-stu-id="69169-130">One voucher deprecation</span></span>

<span data-ttu-id="69169-131">既定で 1 つの伝票が一般会計パラメーターによってオフになります。</span><span class="sxs-lookup"><span data-stu-id="69169-131">One voucher is turned off by default, through a General ledger parameter.</span></span>

## <a name="extensibility-and-customization"></a><span data-ttu-id="69169-132">拡張性およびカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="69169-132">Extensibility and customization</span></span> 

### <a name="customizations-through-extensions-only"></a><span data-ttu-id="69169-133">拡張機能のみによるカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="69169-133">Customizations through extensions only</span></span>

<span data-ttu-id="69169-134">1 つのリリースから次へのカスタマイズの移行が、オーバーレイから拡張機能の使用に移動したことにより簡素化されています。</span><span class="sxs-lookup"><span data-stu-id="69169-134">Migrating customizations from one release to the next has been simplified by moving away from over-layering to the use of extensions.</span></span>

### <a name="extensibility-requests"></a><span data-ttu-id="69169-135">拡張機能の要求</span><span class="sxs-lookup"><span data-stu-id="69169-135">Extensibility requests</span></span>

<span data-ttu-id="69169-136">お客様は、必要なシナリオのために製品に拡張サポートを追加するよう Microsoft に依頼することができます。</span><span class="sxs-lookup"><span data-stu-id="69169-136">Customers can submit a request to Microsoft for extension support to be added to the product for a needed scenario.</span></span> <span data-ttu-id="69169-137">今回のリリースでは、この機能は Lifecycle Services (LCS) に移動されています。</span><span class="sxs-lookup"><span data-stu-id="69169-137">In this release, this feature is moved to Lifecycle Services (LCS).</span></span>

### <a name="extensible-project-work-breakdown-structure"></a><span data-ttu-id="69169-138">拡張可能なプロジェクトの作業分解構造</span><span class="sxs-lookup"><span data-stu-id="69169-138">Extensible project work breakdown structure</span></span>

<span data-ttu-id="69169-139">拡張子を使用して、プロジェクト作業分解構造のカスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="69169-139">Enables customization of the project work breakdown structure using extensions.</span></span>
<span data-ttu-id="69169-140">これにより、プロジェクト作業分解構造に使用される階層グリッド コントロールが、階層データをサポートする標準グリッドに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="69169-140">This replaces the hierarchical grid control used for the project work breakdown structure with a standard grid that supports hierarchical data.</span></span>

### <a name="embedding-powerapps-in-workspaces-and-forms"></a><span data-ttu-id="69169-141">ワークスペースおよびフォームに PowerApps を埋め込む</span><span class="sxs-lookup"><span data-stu-id="69169-141">Embedding PowerApps in workspaces and forms</span></span>

<span data-ttu-id="69169-142">PowerApps を使用して、外部ソースからのデータを Finance and Operations のデータに埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="69169-142">Use PowerApps to embed data from external sources into Finance and Operations data.</span></span> <span data-ttu-id="69169-143">Finance and Operations ページで PowerApp を埋め込む方法の詳細については、[PowerApps の埋め込み](embed-power-apps.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-143">For information about how to embed a PowerApp on a Finance and Operations page, see [Embed PowerApps](embed-power-apps.md).</span></span>

### <a name="custom-fields"></a><span data-ttu-id="69169-144">カスタム フィールド</span><span class="sxs-lookup"><span data-stu-id="69169-144">Custom fields</span></span>

<span data-ttu-id="69169-145">組織は、コードなしの機能拡張経験を使用し、カスタム フィールドを追加してビジネス要件に合わせて自社アプリケーションをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="69169-145">Organizations can add custom fields to tailor their application to their business requirements, using a no-code extensibility experience.</span></span> <span data-ttu-id="69169-146">カスタム フィールドを追加する方法の詳細については、[カスタム フィールド](user-defined-fields.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-146">For information about how to add a custom field, see [Custom fields](user-defined-fields.md).</span></span>

## <a name="integration"></a><span data-ttu-id="69169-147">統合</span><span class="sxs-lookup"><span data-stu-id="69169-147">Integration</span></span> 

### <a name="integration-with-common-data-service-cds"></a><span data-ttu-id="69169-148">Common Data Service (CDS) との統合</span><span class="sxs-lookup"><span data-stu-id="69169-148">Integration with Common Data Service (CDS)</span></span> 

<span data-ttu-id="69169-149">Dynamics 365 for Finance and Operations は、Finance and Operations と Dynamics 365 for Field Service の間、および Finance and Operations と Dynamics 365 for Project Service Automation の間のアプリケーション間のビジネス プロセスを可能にしました。</span><span class="sxs-lookup"><span data-stu-id="69169-149">Dynamics 365 for Finance and Operations has enabled cross-application business processes between Finance and Operations and Dynamics 365 for Field Service and between Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>
<span data-ttu-id="69169-150">これらのシナリオは、拡張可能なデータ インテグレーター テンプレートと CDS を使用して構成され、クロス アプリケーション シナリオを実現します。</span><span class="sxs-lookup"><span data-stu-id="69169-150">These scenarios are configured using extensible Data integrator templates and CDS to enable the cross-application scenarios.</span></span>

### <a name="integration-with-dynamics-365-for-field-service"></a><span data-ttu-id="69169-151">Dynamics 365 for Field Service との統合</span><span class="sxs-lookup"><span data-stu-id="69169-151">Integration with Dynamics 365 for Field Service</span></span>

<span data-ttu-id="69169-152">データ統合を活用して、Field Service アクティビティが Finance and Operations の外で行われるシナリオをサポートするためのデータ統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="69169-152">Provides data integration to support scenarios where Field Service activities are done outside Finance and Operations, leveraging the data integrator.</span></span>

### <a name="integration-with-dynamics-365-for-project-service-automation"></a><span data-ttu-id="69169-153">Dynamics 365 for Project Service Automation との統合</span><span class="sxs-lookup"><span data-stu-id="69169-153">Integration with Dynamics 365 for Project Service Automation</span></span>

<span data-ttu-id="69169-154">データ インテグレーターを活用することで、プロジェクトおよびリソース管理アクティビティが Finance and Operations の外で行われ、プロジェクト会計アクティビティが Finance and Operations で行われるシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="69169-154">Supports scenarios where project and resource management activities are done outside Finance and Operations, and the project accounting activities are done in Finance and Operations, leveraging the data integrator.</span></span>

## <a name="improved-support-experiences"></a><span data-ttu-id="69169-155">サポート エクスペリエンスの強化</span><span class="sxs-lookup"><span data-stu-id="69169-155">Improved support experiences</span></span> 

### <a name="telemetry-based-kb-recommendation"></a><span data-ttu-id="69169-156">テレメトリに基づく KB の推奨事項</span><span class="sxs-lookup"><span data-stu-id="69169-156">Telemetry-based KB recommendation</span></span>

<span data-ttu-id="69169-157">実稼働環境からのテレメトリは、テナントに適用されるアプリケーション修正プログラムを識別するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="69169-157">Telemetry from a production environment can be used to identify the application hotfixes that apply to a tenant.</span></span>

### <a name="kb-recommendations-when-entering-a-support-case"></a><span data-ttu-id="69169-158">サポート案件を入力する際の KB の推奨事項</span><span class="sxs-lookup"><span data-stu-id="69169-158">KB recommendations when entering a support case</span></span>

<span data-ttu-id="69169-159">LCS では、テレメトリ駆動の KB の推奨事項を提供します。</span><span class="sxs-lookup"><span data-stu-id="69169-159">LCS provides telemetry-driven KB recommendations.</span></span>

### <a name="report-production-outage"></a><span data-ttu-id="69169-160">稼働停止のレポート</span><span class="sxs-lookup"><span data-stu-id="69169-160">Report production outage</span></span>

<span data-ttu-id="69169-161">実稼動環境のサービスが低下または使用不可能になった場合、Microsoft サポートに問題をエスカレートを迅速かつ有効なチャンネルを提供します。</span><span class="sxs-lookup"><span data-stu-id="69169-161">Provides a quick and effective channel to escalate issues to Microsoft Support if the services in a production environment are degraded or become unavailable.</span></span>

## <a name="supply-chain-management"></a><span data-ttu-id="69169-162">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="69169-162">Supply chain management</span></span> 

### <a name="vendor-collaboration--rfq-process"></a><span data-ttu-id="69169-163">仕入先コラボレーション - RFQ プロセス</span><span class="sxs-lookup"><span data-stu-id="69169-163">Vendor collaboration – RFQ process</span></span>

<span data-ttu-id="69169-164">機能強化により、誰が入札したかを容易に把握できます (仕入先または調達部門)。</span><span class="sxs-lookup"><span data-stu-id="69169-164">Enhancements make it easy to tell who entered a bid (a vendor or a procurement department).</span></span> <span data-ttu-id="69169-165">詳細については、「[見積依頼 (RFQ)](../../supply-chain/procurement/request-quotations.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-165">For more information, see [Requests for quotation (RFQs)](../../supply-chain/procurement/request-quotations.md).</span></span>

### <a name="partial-shipment-of-a-load-split-load"></a><span data-ttu-id="69169-166">積荷の部分的出荷 (分割積荷)</span><span class="sxs-lookup"><span data-stu-id="69169-166">Partial shipment of a load (split load)</span></span>

<span data-ttu-id="69169-167">1 つの積荷または複数の積荷を完全に、または部分的に読み込めるように許可します。</span><span class="sxs-lookup"><span data-stu-id="69169-167">Allows single loads or multiple loads to be fully or partially loaded.</span></span>

### <a name="immediate-replenishment-of-locations"></a><span data-ttu-id="69169-168">場所の即時補充</span><span class="sxs-lookup"><span data-stu-id="69169-168">Immediate replenishment of locations</span></span>

<span data-ttu-id="69169-169">補充テンプレートのある場所ディレクティブの明細行の配賦に失敗した場合、ウェーブ実行中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="69169-169">Used during wave execution if allocation fails for a location directive line that has a replenishment template.</span></span> <span data-ttu-id="69169-170">即時補充の詳細については、[即時補充](../../supply-chain/warehousing/immediate-replenishment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-170">For more information about immediate replenishment, see [Immediate replenishment](../../supply-chain/warehousing/immediate-replenishment.md).</span></span>

### <a name="reason-codes-added-to-warehouse-counting-and-adjustment"></a><span data-ttu-id="69169-171">倉庫の棚卸と調整に追加された理由コード</span><span class="sxs-lookup"><span data-stu-id="69169-171">Reason codes added to warehouse counting and adjustment</span></span>

<span data-ttu-id="69169-172">棚卸を実行するとき、および調整を行うときに理由コードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="69169-172">Users can add a reason code when performing counts and when making an adjustment.</span></span> <span data-ttu-id="69169-173">理由コードの詳細については、[在庫棚卸の理由コード](../../supply-chain/warehousing/reason-codes-for-counting-journals.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-173">For more information about reason codes, see [Reason codes for inventory counting](../../supply-chain/warehousing/reason-codes-for-counting-journals.md).</span></span>

### <a name="batch-balancing-enabled-for-advanced-warehousing-processes"></a><span data-ttu-id="69169-174">高度な倉庫管理プロセスが有効になっているバッチ バランシング</span><span class="sxs-lookup"><span data-stu-id="69169-174">Batch balancing enabled for advanced warehousing processes</span></span> 

<span data-ttu-id="69169-175">倉庫管理プロセスに対して設定されている製品にバッチ バランシング プロセスを利用できるようになりました (以前のリリースでは、倉庫管理プロセスに対して設定されていない製品にのみバッチ バランシング プロセスが有効になっていました)。</span><span class="sxs-lookup"><span data-stu-id="69169-175">The batch balancing process is now available for products that are set up for warehouse management processes (in earlier releases, the batch balancing process was enabled only for products that were not set up for warehouse management processes).</span></span> <span data-ttu-id="69169-176">この機能拡張により、バッチ バランシング プロセスが完了した後に、ユーザーがピッキングに原料をリリースすることが可能になります。</span><span class="sxs-lookup"><span data-stu-id="69169-176">This enhancement makes it possible for the user to release ingredients to picking after the batch balancing process has been completed.</span></span> <span data-ttu-id="69169-177">バッチ バランシングの詳細については、「[バッチ バランシング](../../supply-chain/production-control/batch-balancing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-177">For more information about batch balancing, see [Batch balancing](../../supply-chain/production-control/batch-balancing.md).</span></span>

### <a name="analytical-workspaces-with-embedded-power-bi-for-cost-management"></a><span data-ttu-id="69169-178">原価管理のための Power BI が埋め込まれた分析ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="69169-178">Analytical workspaces with embedded Power BI for Cost management</span></span>

<span data-ttu-id="69169-179">原価管理のための新しい分析ワークスペースは、原価管理およびコスト分析のワークスペースに埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="69169-179">New Analytical workspaces for Cost management are embedded in the Cost administration and Cost Analysis workspaces.</span></span> <span data-ttu-id="69169-180">コンテンツ パックには、期首残高、期末残高、正味調達および正味使用量などの措置が含まれています。</span><span class="sxs-lookup"><span data-stu-id="69169-180">The content pack includes measures such as beginning balance, ending balance, net sourcing and net usage.</span></span> <span data-ttu-id="69169-181">在庫回転率、手持在庫日数、在庫の精度などの一連の計算メジャーも含まれています。</span><span class="sxs-lookup"><span data-stu-id="69169-181">A set of calculated measures, such as inventory turn ratio, days inventory on-hand, and inventory accuracy are also included.</span></span> <span data-ttu-id="69169-182">**原価管理** Power BI コンテンツは、**原価管理**および**コスト分析**ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="69169-182">The **Cost management** Power BI content is shown in the **Cost administration** and **Cost analysis** workspaces.</span></span> <span data-ttu-id="69169-183">詳細については、[原価管理の Power BI コンテンツ](../../dev-itpro/analytics/cost-management-content-pack.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-183">For more information, see [Cost management Power BI content](../../dev-itpro/analytics/cost-management-content-pack.md).</span></span>

## <a name="globalization"></a><span data-ttu-id="69169-184">グローバリゼーション</span><span class="sxs-lookup"><span data-stu-id="69169-184">Globalization</span></span> 

### <a name="india-localization--project-and-upgrade"></a><span data-ttu-id="69169-185">インド ローカライズ – プロジェクトとアップグレード</span><span class="sxs-lookup"><span data-stu-id="69169-185">India localization – project and upgrade</span></span>

<span data-ttu-id="69169-186">ユーザーはプロジェクト管理および会計モジュールでインドの商品及びサービス税 (GST) を管理でき、AX 2012 の顧客は Dynamics 365 for Finance and Operations にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="69169-186">Users can manage India Goods and Services Tax (GST) for the Project management and accounting module, and AX 2012 customers can upgrade to Dynamics 365 for Finance and Operations.</span></span>

### <a name="enhanced-configurability"></a><span data-ttu-id="69169-187">拡張されたコンフィギュレーションの可能性</span><span class="sxs-lookup"><span data-stu-id="69169-187">Enhanced configurability</span></span>

<span data-ttu-id="69169-188">新機能にはインポートとテスト シナリオが含まれており、コーディングなしでコンフィギュレーションが可能になるより広範なサポートも含まれます。</span><span class="sxs-lookup"><span data-stu-id="69169-188">New features include import and testing scenarios, and also broader support for configurability without coding.</span></span>

## <a name="servicing-performance-and-deployment"></a><span data-ttu-id="69169-189">保守、パフォーマンス、展開</span><span class="sxs-lookup"><span data-stu-id="69169-189">Servicing, performance, and deployment</span></span> 

### <a name="improved-delivery-of-platform-and-financial-reporting-updates"></a><span data-ttu-id="69169-190">プラットフォームおよび財務レポート更新のデリバリーの強化</span><span class="sxs-lookup"><span data-stu-id="69169-190">Improved delivery of platform and financial reporting updates</span></span>

<span data-ttu-id="69169-191">プラットフォームおよび財務レポートの更新は、オプションの更新プログラムではなく、Microsoft によって管理される継続的な更新になります。</span><span class="sxs-lookup"><span data-stu-id="69169-191">Platform and financial reporting updates will be continual updates managed by Microsoft rather than optional updates.</span></span> <span data-ttu-id="69169-192">この変更は、サービスの信頼性と可用性を向上させるとともに、最新の改善と修正を顧客に確実に提供することを目的としています。 </span><span class="sxs-lookup"><span data-stu-id="69169-192">This change is intended to improve service reliability and availability, and also to ensure that customers have the latest improvements and fixes.</span></span> <span data-ttu-id="69169-193">プラットフォームと財務レポートの更新には、下位互換性があります。</span><span class="sxs-lookup"><span data-stu-id="69169-193">Platform and financial reporting updates are backward-compatible.</span></span>  <span data-ttu-id="69169-194">詳細については、[Finance and Operations クラウド プラットフォームの毎月の更新に関するよく寄せられる質問](../../dev-itpro/sysadmin/faq-platform-monthly-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-194">For more information, see [Finance and Operations cloud platform monthly updates FAQ](../../dev-itpro/sysadmin/faq-platform-monthly-updates.md).</span></span>

### <a name="upgrade-automation"></a><span data-ttu-id="69169-195">自動アップグレード</span><span class="sxs-lookup"><span data-stu-id="69169-195">Upgrade automation</span></span>

<span data-ttu-id="69169-196">アップグレードの自動化により、非運用環境で LCS を使用して、顧客に対しメジャー バージョンのアップグレードをセルフ サービス操作として提供します。</span><span class="sxs-lookup"><span data-stu-id="69169-196">Upgrade automation makes major version upgrades a self-service operation for the customer, using LCS for non-production environments.</span></span>

### <a name="service-hardening"></a><span data-ttu-id="69169-197">サービスの強化</span><span class="sxs-lookup"><span data-stu-id="69169-197">Service hardening</span></span>

<span data-ttu-id="69169-198">主要な業務プロセスの監視と警告を追加し、最も使用頻度の高いフォームのフォーム負荷パフォーマンスを改善します。</span><span class="sxs-lookup"><span data-stu-id="69169-198">Added service monitoring and alerting for core business processes, and improved form load performance of the most commonly used forms.</span></span>

### <a name="lifecycle-services-sandbox-self-service-automation-and-rdp-lockdown"></a><span data-ttu-id="69169-199">Lifecycle Services サンドボックス セルフサービス自動化および RDP ロックダウン</span><span class="sxs-lookup"><span data-stu-id="69169-199">Lifecycle Services sandbox self-service automation and RDP lockdown</span></span>

<span data-ttu-id="69169-200">サンドボックス セルフサービスの自動化では、リモート デスクトップを介したサンドボックス環境へのアクセスがなくても、データの移動、デバッグ工程、監視、および診断がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="69169-200">Sandbox self-service automation supports data movement, debugging operations, monitoring, and diagnostics without requiring access to the sandbox environments through Remote Desktop.</span></span> <span data-ttu-id="69169-201">サンドボックス環境のリモート デスクトップ機能は使用されなくなります。</span><span class="sxs-lookup"><span data-stu-id="69169-201">Remote Desktop capabilities for sandbox environments will be deprecated.</span></span> <span data-ttu-id="69169-202">つまり、顧客は VM にアクセスするためにリモート デスクトップを使用する必要がなくなり、信頼性とセキュリティが向上します。</span><span class="sxs-lookup"><span data-stu-id="69169-202">This means that customers won’t be required to use Remote Desktop to access the VM, which improves reliability and security.</span></span>

## <a name="compliance"></a><span data-ttu-id="69169-203">コンプライアンス</span><span class="sxs-lookup"><span data-stu-id="69169-203">Compliance</span></span> 

### <a name="general-data-protection-regulation-gdpr"></a><span data-ttu-id="69169-204">一般的なデータ保護規制 (GDPR)</span><span class="sxs-lookup"><span data-stu-id="69169-204">General Data Protection Regulation (GDPR)</span></span>

<span data-ttu-id="69169-205">投資は、欧州のプライバシーに関する法律の要件に対応します。</span><span class="sxs-lookup"><span data-stu-id="69169-205">Investments address the European privacy law’s requirements.</span></span> <span data-ttu-id="69169-206">準拠に役立つリソースを検索するには [Trust Center](https://www.microsoft.com/en-us/trustcenter/compliance/accessibility) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-206">Go to the [Trust Center](https://www.microsoft.com/en-us/trustcenter/compliance/accessibility) to learn more and find resources to help you comply.</span></span>

### <a name="accessibility-enhancements"></a><span data-ttu-id="69169-207">アクセシビリティの拡張機能</span><span class="sxs-lookup"><span data-stu-id="69169-207">Accessibility enhancements</span></span>

<span data-ttu-id="69169-208">業界をリードするアクセシビリティ標準については [Trust Center](https://www.microsoft.com/en-us/trustcenter/compliance/accessibility) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69169-208">Go to the [Trust Center](https://www.microsoft.com/en-us/trustcenter/compliance/accessibility) to learn about our industry-leading accessibility standards.</span></span>


