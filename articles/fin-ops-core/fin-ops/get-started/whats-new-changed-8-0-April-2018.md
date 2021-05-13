---
title: Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations バージョン 8.0 の新機能または変更された機能について説明します。 このバージョンは 2018 年 4 月にリリースされました。
author: tonyafehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: b265d51c-52d1-45c5-b578-64c5242c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: d92d4d8fda5ce473ffe4a28ac316d0da20297e75
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923428"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-version-80-april-2018"></a><span data-ttu-id="8bc54-104">Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="8bc54-104">What's new or changed in Dynamics 365 for Finance and Operations version 8.0 (April 2018)</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8bc54-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018).</span></span> <span data-ttu-id="8bc54-106">このバージョンは 2018 年 4 月にリリースされ、ビルド番号は 8.0.30 と 8.0.35 です。</span><span class="sxs-lookup"><span data-stu-id="8bc54-106">This version was released in April 2018 and has build numbers 8.0.30 and 8.0.35.</span></span>

<span data-ttu-id="8bc54-107">ビジネス アプリケーションの最新の更新プログラムや、独自のアプリケーションと拡張機能をプラットフォームにビルドするための新しい機能を見つけるには、[Dynamics 365 2018 年春リリース計画](/business-applications-release-notes/April18/release-overview)をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-107">To discover the latest updates to our business applications, as well as a host of new capabilities for building your own applications and extensions on top of our platform, download the [Dynamics 365 Spring '18 release plans](/business-applications-release-notes/April18/release-overview).</span></span> <span data-ttu-id="8bc54-108">リリース ノートでは、Dynamics 365 for Finance and Operations の新規または変更のいずれかの機能に関する詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-108">The release plans provide details about the features that are either new or changed in Dynamics 365 for Finance and Operations.</span></span>

### <a name="introducing-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="8bc54-109">Dynamics 365 for Finance and Operations の導入</span><span class="sxs-lookup"><span data-stu-id="8bc54-109">Introducing Dynamics 365 for Finance and Operations</span></span>

<span data-ttu-id="8bc54-110">ユーザーおよび開発者は、「Microsoft Dynamics 365 for Finance and Operations」という更新済の製品名を確認できます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-110">Users and developers will see an updated product name, "Microsoft Dynamics 365 for Finance and Operations."</span></span> <span data-ttu-id="8bc54-111">バージョン 8.0 では Dynamics 365 製品がさらに簡素化され、顧客とエコシステムの選択がさらに簡単になります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-111">With version 8.0, Microsoft is further simplifying our Dynamics 365 offerings and increasing ease of selection for our customers and ecosystem.</span></span> <span data-ttu-id="8bc54-112">今後 Microsoft は、個別エディション (Business Edition および Enterprise Edition) を提供しなくなるため、この Dynamics 365 アプリケーションの製品名は Microsoft Dynamics 365 for Finance and Operations になります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-112">Going forward, Microsoft is no longer offering separate editions (Business edition and Enterprise edition), so the product name for this Dynamics 365 application is Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="business-productivity"></a><span data-ttu-id="8bc54-113">業務の生産性</span><span class="sxs-lookup"><span data-stu-id="8bc54-113">Business productivity</span></span>

### <a name="alerts"></a><span data-ttu-id="8bc54-114">警告</span><span class="sxs-lookup"><span data-stu-id="8bc54-114">Alerts</span></span>

<span data-ttu-id="8bc54-115">クライアント ベースの警告機能により、請求書が支払われたときや顧客が住所を変更したときなど、ビジネス イベントに基づいて警告ルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-115">Client-based alert functionality enables a user to define alert rules based on business events, such as when an invoice is paid or a customer changes an address.</span></span> <span data-ttu-id="8bc54-116">警告およびその作成方法の詳細については、[警告の概要](alerts-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-116">For more information about alerts and how to create them, see [Alerts overview](alerts-overview.md).</span></span>

### <a name="optimization-advisor"></a><span data-ttu-id="8bc54-117">最適化アドバイザー</span><span class="sxs-lookup"><span data-stu-id="8bc54-117">Optimization advisor</span></span>

<span data-ttu-id="8bc54-118">テレメトリを使用して、お客様のビジネス プロセスを分析し、最適化の可能性を探し、アプリケーション データを使用してその可能性を定量化し、ソリューションを推奨します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-118">Uses telemetry to analyze customers' business processes, finds optimization opportunities, uses application data to quantify the opportunities, and then recommends solutions.</span></span>

### <a name="project-timesheet-mobile"></a><span data-ttu-id="8bc54-119">プロジェクト タイムシート モバイル</span><span class="sxs-lookup"><span data-stu-id="8bc54-119">Project timesheet mobile</span></span>

<span data-ttu-id="8bc54-120">従業員は、プロジェクト タイムシートを作成して送信できます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-120">Employees can create and submit project timesheets.</span></span> <span data-ttu-id="8bc54-121">保存したお気に入りの使用機能と、以前のタイムシートからのコピー機能により、迅速で正確な時間の入力が容易になります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-121">The use of saved favorites and the ability to copy from a previous timesheet facilitates rapid, accurate time entry.</span></span>

### <a name="edit-default-project-fulfillment-hours"></a><span data-ttu-id="8bc54-122">既定のプロジェクトのフルフィルメント時間を編集</span><span class="sxs-lookup"><span data-stu-id="8bc54-122">Edit default project fulfillment hours</span></span>

<span data-ttu-id="8bc54-123">プロジェクト リソース管理者は、プロジェクトの予約調達のためのプロセスの一部として、既定の時間を編集できます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-123">Project resource managers can edit the default hours as part of the project booking fulfillment process.</span></span>

### <a name="reserve-project-resources-past-the-task-end-date"></a><span data-ttu-id="8bc54-124">タスクの終了日が過ぎてからプロジェクト リソースを予約</span><span class="sxs-lookup"><span data-stu-id="8bc54-124">Reserve project resources past the task end date</span></span>

<span data-ttu-id="8bc54-125">プロジェクト リソースの管理者は、タスクの現在の計画終了日を過ぎたタスクでリソースをフルフィルメントすることができます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-125">Project resource managers can fulfill resources on tasks past the current planned end date for the task.</span></span>

### <a name="person-search-report"></a><span data-ttu-id="8bc54-126">個人検索レポート</span><span class="sxs-lookup"><span data-stu-id="8bc54-126">Person search report</span></span>

<span data-ttu-id="8bc54-127">Finance and Operations 内で担当者および個人データを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-127">You can find a person and their personal data in Finance and Operations.</span></span>

### <a name="data-sharing-for-customer-and-vendor-tables"></a><span data-ttu-id="8bc54-128">顧客および仕入先のテーブルのデータ共有</span><span class="sxs-lookup"><span data-stu-id="8bc54-128">Data sharing for customer and vendor tables</span></span>

<span data-ttu-id="8bc54-129">データは、顧客テーブルと仕入先テーブル、および複数の法人の多くの関連テーブルで共有することができます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-129">Data can be shared across customer and vendor tables and many related tables across multiple legal entities.</span></span>

### <a name="one-voucher-deprecation"></a><span data-ttu-id="8bc54-130">1 つの伝票の廃止</span><span class="sxs-lookup"><span data-stu-id="8bc54-130">One voucher deprecation</span></span>

<span data-ttu-id="8bc54-131">財務仕訳帳 (一般仕訳帳、固定資産仕訳帳、仕入先支払仕訳帳など) の既存の機能を使用して、1 つの伝票のコンテキストで複数の補助元帳トランザクションを入力できます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-131">The existing functionality for financial journals (general journal, fixed asset journal, vendor payment journal, and so on) lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="8bc54-132">この機能を「1 つの伝票」と呼びます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-132">This functionality is referred to as "One voucher."</span></span> <span data-ttu-id="8bc54-133">1 つの伝票機能により、決済、税計算、補助元帳の一般会計への調整、財務報告などの間に問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-133">The One voucher functionality causes issues during settlement, tax calculation, reconciliation of a subledger to the general ledger, financial reporting, and more.</span></span> <span data-ttu-id="8bc54-134">これらの問題のため、1 つの伝票機能は廃止されます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-134">Because of these issues, the One voucher functionality will be made obsolete.</span></span> <span data-ttu-id="8bc54-135">ただし、この機能に依存する機能的なギャップがあるため、機能が一度に無効になることはありません。</span><span class="sxs-lookup"><span data-stu-id="8bc54-135">However, because there are functional gaps that depend on this functionality, the functionality won't become obsolete all at once.</span></span> <span data-ttu-id="8bc54-136">代わりに、次のスケジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-136">Instead, we will use the following schedule:</span></span>

- <span data-ttu-id="8bc54-137">**18 年春リリース** – 機能は、一般会計パラメーターによって既定で、オフになります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-137">**Spring '18 release** – The functionality will be turned off by default, through a General ledger parameter.</span></span> <span data-ttu-id="8bc54-138">ただし、組織が単一伝票文書に記載されているビジネス シナリオ ギャップの範囲内にシナリオがある場合、機能をオンにできます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-138">However, you can turn the functionality on if your organization has a scenario that falls in the business scenario gaps that are listed in the One voucher documentation.</span></span>

    - <span data-ttu-id="8bc54-139">顧客が 1 つの伝票を必要としないビジネス シナリオがある場合、機能をオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-139">If a customer has a business scenario that doesn't require One voucher, don't turn the functionality on.</span></span> <span data-ttu-id="8bc54-140">この機能が使用される場合、単一伝票文書に記載されている領域の「不具合」は修正されません。</span><span class="sxs-lookup"><span data-stu-id="8bc54-140">We won't fix "bugs" in the areas that are identified in the One voucher documentation if this functionality is used.</span></span>
    - <span data-ttu-id="8bc54-141">機能的なギャップのいずれかに必要な機能でない限り、 Microsoft Dynamics 365 Finance and Operations への統合に 1 つの伝票を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-141">Stop using One voucher for integrations into Microsoft Dynamics 365 Finance and Operations, unless the functionality is required for one of the functional gaps.</span></span>

- <span data-ttu-id="8bc54-142">**18 年秋およびそれ以降のリリース** – 機能的なギャップが埋まります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-142">**Fall '18 and later releases** – The functional gaps will be filled.</span></span> <span data-ttu-id="8bc54-143">機能的なギャップが埋められた後、1 つの伝票の機能が完全にオフになります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-143">After the functional gaps are filled, the One voucher functionality will be permanently turned off.</span></span>

<span data-ttu-id="8bc54-144">この機能の使用と廃止に関する詳細については、[1 つの伝票ドキュメント](../../../finance/general-ledger/one-voucher.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-144">See the [One voucher documentation](../../../finance/general-ledger/one-voucher.md) for detailed information about the use and deprecation of this functionality.</span></span>

## <a name="extensibility-and-customization"></a><span data-ttu-id="8bc54-145">拡張性およびカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="8bc54-145">Extensibility and customization</span></span>

### <a name="customizations-through-extensions-only"></a><span data-ttu-id="8bc54-146">拡張機能のみによるカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="8bc54-146">Customizations through extensions only</span></span>

<span data-ttu-id="8bc54-147">1 つのリリースから次へのカスタマイズの移行が、オーバーレイから拡張機能の使用に移動したことにより簡素化されています。</span><span class="sxs-lookup"><span data-stu-id="8bc54-147">Migrating customizations from one release to the next has been simplified by moving away from over-layering to the use of extensions.</span></span>

### <a name="extensibility-requests"></a><span data-ttu-id="8bc54-148">拡張機能の要求</span><span class="sxs-lookup"><span data-stu-id="8bc54-148">Extensibility requests</span></span>

<span data-ttu-id="8bc54-149">お客様は、必要なシナリオのために製品に拡張サポートを追加するよう Microsoft に依頼することができます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-149">Customers can submit a request to Microsoft for extension support to be added to the product for a needed scenario.</span></span> <span data-ttu-id="8bc54-150">今回のリリースでは、この機能は Lifecycle Services (LCS) に移動されています。</span><span class="sxs-lookup"><span data-stu-id="8bc54-150">In this release, this feature is moved to Lifecycle Services (LCS).</span></span>

### <a name="embedding-microsoft-power-apps-in-workspaces-and-forms"></a><span data-ttu-id="8bc54-151">ワークスペースおよびフォームに Microsoft Power Apps を埋め込む</span><span class="sxs-lookup"><span data-stu-id="8bc54-151">Embedding Microsoft Power Apps in workspaces and forms</span></span>

<span data-ttu-id="8bc54-152">Microsoft Power Apps を使用して、外部ソースからのデータを Finance and Operations のデータに埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-152">Use Microsoft Power Apps to embed data from external sources into Finance and Operations data.</span></span> <span data-ttu-id="8bc54-153">Finance and Operations ページで PowerApp を埋め込む方法の詳細については、[PowerApps の埋め込み](embed-power-apps.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-153">For information about how to embed a PowerApp on a Finance and Operations page, see [Embed PowerApps](embed-power-apps.md).</span></span>

### <a name="custom-fields"></a><span data-ttu-id="8bc54-154">カスタム フィールド</span><span class="sxs-lookup"><span data-stu-id="8bc54-154">Custom fields</span></span>

<span data-ttu-id="8bc54-155">組織は、コードなしの機能拡張経験を使用し、カスタム フィールドを追加してビジネス要件に合わせて自社アプリケーションをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-155">Organizations can add custom fields to tailor their application to their business requirements, using a no-code extensibility experience.</span></span> <span data-ttu-id="8bc54-156">カスタム フィールドを作成および管理する方法の詳細については、[カスタム フィールドの作成と操作](user-defined-fields.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-156">For information about how to add a custom field, see [Create and work with custom fields](user-defined-fields.md).</span></span>

## <a name="integration"></a><span data-ttu-id="8bc54-157">統合</span><span class="sxs-lookup"><span data-stu-id="8bc54-157">Integration</span></span> 

### <a name="integration-with-dataverse"></a><span data-ttu-id="8bc54-158">Dataverse との統合</span><span class="sxs-lookup"><span data-stu-id="8bc54-158">Integration with Dataverse</span></span>

<span data-ttu-id="8bc54-159">Dynamics 365 for Finance and Operations では、Finance and Operations と Dynamics 365 for Field Service の間、および Finance and Operations と Dynamics 365 for Project Service Automation の間のクロス アプリケーションの業務プロセスを有効にしました。</span><span class="sxs-lookup"><span data-stu-id="8bc54-159">Dynamics 365 for Finance and Operations has enabled cross-application business processes between Finance and Operations and Dynamics 365 for Field Service and between Finance and Operations and Dynamics 365 for Project Service Automation.</span></span> <span data-ttu-id="8bc54-160">これらのシナリオは、拡張可能なデータ インテグレーター テンプレートと Dataverse を使用して構成され、クロス アプリケーション シナリオを実現します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-160">These scenarios are configured using extensible Data integrator templates and Dataverse to enable the cross-application scenarios.</span></span>

### <a name="integration-with-dynamics-365-for-field-service"></a><span data-ttu-id="8bc54-161">Dynamics 365 for Field Service との統合</span><span class="sxs-lookup"><span data-stu-id="8bc54-161">Integration with Dynamics 365 for Field Service</span></span>

<span data-ttu-id="8bc54-162">データ インテグレーターを活用して、Field Service アクティビティが Finance and Operations の外で行われるシナリオをサポートするためのデータ統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-162">Provides data integration to support scenarios where Field Service activities are done outside Finance and Operations, leveraging the data integrator.</span></span>

### <a name="integration-with-dynamics-365-for-project-service-automation"></a><span data-ttu-id="8bc54-163">Dynamics 365 for Project Service Automation との統合</span><span class="sxs-lookup"><span data-stu-id="8bc54-163">Integration with Dynamics 365 for Project Service Automation</span></span>

<span data-ttu-id="8bc54-164">データ インテグレーターを活用することで、プロジェクトおよびリソース管理アクティビティが Finance and Operations の外で行われ、プロジェクト会計アクティビティが Finance and Operations で行われるシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="8bc54-164">Supports scenarios where project and resource management activities are done outside Finance and Operations, and the project accounting activities are done in Finance and Operations, leveraging the data integrator.</span></span>

## <a name="improved-support-experiences"></a><span data-ttu-id="8bc54-165">サポート エクスペリエンスの強化</span><span class="sxs-lookup"><span data-stu-id="8bc54-165">Improved support experiences</span></span>

### <a name="telemetry-based-kb-recommendation"></a><span data-ttu-id="8bc54-166">テレメトリに基づく KB の推奨事項</span><span class="sxs-lookup"><span data-stu-id="8bc54-166">Telemetry-based KB recommendation</span></span>

<span data-ttu-id="8bc54-167">実稼働環境からのテレメトリは、テナントに適用されるアプリケーション修正プログラムを識別するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-167">Telemetry from a production environment can be used to identify the application hotfixes that apply to a tenant.</span></span>

### <a name="kb-recommendations-when-entering-a-support-case"></a><span data-ttu-id="8bc54-168">サポート案件を入力する際の KB の推奨事項</span><span class="sxs-lookup"><span data-stu-id="8bc54-168">KB recommendations when entering a support case</span></span>

<span data-ttu-id="8bc54-169">LCS では、テレメトリ駆動の KB の推奨事項を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-169">LCS provides telemetry-driven KB recommendations.</span></span>

### <a name="report-production-outage"></a><span data-ttu-id="8bc54-170">稼働停止のレポート</span><span class="sxs-lookup"><span data-stu-id="8bc54-170">Report production outage</span></span>

<span data-ttu-id="8bc54-171">実稼動環境のサービスが低下または使用不可能になった場合、Microsoft サポートに問題をエスカレートを迅速かつ有効なチャンネルを提供します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-171">Provides a quick and effective channel to escalate issues to Microsoft Support if the services in a production environment are degraded or become unavailable.</span></span>

## <a name="supply-chain-management"></a><span data-ttu-id="8bc54-172">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="8bc54-172">Supply chain management</span></span>

### <a name="vendor-collaboration--rfq-process"></a><span data-ttu-id="8bc54-173">仕入先コラボレーション - RFQ プロセス</span><span class="sxs-lookup"><span data-stu-id="8bc54-173">Vendor collaboration – RFQ process</span></span>

<span data-ttu-id="8bc54-174">機能強化により、誰が入札したかを容易に把握できます (仕入先または調達部門)。</span><span class="sxs-lookup"><span data-stu-id="8bc54-174">Enhancements make it easy to tell who entered a bid (a vendor or a procurement department).</span></span> <span data-ttu-id="8bc54-175">詳細については、「[見積依頼 (RFQ)](../../../supply-chain/procurement/request-quotations.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-175">For more information, see [Requests for quotation (RFQs)](../../../supply-chain/procurement/request-quotations.md).</span></span>

### <a name="partial-shipment-of-a-load-split-load"></a><span data-ttu-id="8bc54-176">積荷の部分的出荷 (分割積荷)</span><span class="sxs-lookup"><span data-stu-id="8bc54-176">Partial shipment of a load (split load)</span></span>

<span data-ttu-id="8bc54-177">1 つの積荷または複数の積荷を完全に、または部分的に読み込めるように許可します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-177">Allows single loads or multiple loads to be fully or partially loaded.</span></span>

### <a name="immediate-replenishment-of-locations"></a><span data-ttu-id="8bc54-178">場所の即時補充</span><span class="sxs-lookup"><span data-stu-id="8bc54-178">Immediate replenishment of locations</span></span>

<span data-ttu-id="8bc54-179">補充テンプレートのある場所ディレクティブの明細行の配賦に失敗した場合、ウェーブ実行中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-179">Used during wave execution if allocation fails for a location directive line that has a replenishment template.</span></span> <span data-ttu-id="8bc54-180">即時補充の詳細については、[即時補充](../../../supply-chain/warehousing/immediate-replenishment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-180">For more information about immediate replenishment, see [Immediate replenishment](../../../supply-chain/warehousing/immediate-replenishment.md).</span></span>

### <a name="reason-codes-added-to-warehouse-counting-and-adjustment"></a><span data-ttu-id="8bc54-181">倉庫の棚卸と調整に追加された理由コード</span><span class="sxs-lookup"><span data-stu-id="8bc54-181">Reason codes added to warehouse counting and adjustment</span></span>

<span data-ttu-id="8bc54-182">棚卸を実行するとき、および調整を行うときに理由コードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-182">Users can add a reason code when performing counts and when making an adjustment.</span></span> <span data-ttu-id="8bc54-183">理由コードの詳細については、[在庫棚卸の理由コード](../../../supply-chain/warehousing/reason-codes-for-counting-journals.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-183">For more information about reason codes, see [Reason codes for inventory counting](../../../supply-chain/warehousing/reason-codes-for-counting-journals.md).</span></span>

### <a name="batch-balancing-enabled-for-advanced-warehousing-processes"></a><span data-ttu-id="8bc54-184">高度な倉庫管理プロセスが有効になっているバッチ バランシング</span><span class="sxs-lookup"><span data-stu-id="8bc54-184">Batch balancing enabled for advanced warehousing processes</span></span>

<span data-ttu-id="8bc54-185">倉庫管理プロセスに対して設定されている製品にバッチ バランシング プロセスを利用できるようになりました (以前のリリースでは、倉庫管理プロセスに対して設定されていない製品にのみバッチ バランシング プロセスが有効になっていました)。</span><span class="sxs-lookup"><span data-stu-id="8bc54-185">The batch balancing process is now available for products that are set up for warehouse management processes (in earlier releases, the batch balancing process was enabled only for products that were not set up for warehouse management processes).</span></span> <span data-ttu-id="8bc54-186">この機能拡張により、バッチ バランシング プロセスが完了した後に、ユーザーがピッキングに原料をリリースすることが可能になります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-186">This enhancement makes it possible for the user to release ingredients to picking after the batch balancing process has been completed.</span></span> <span data-ttu-id="8bc54-187">バッチ バランシングの詳細については、「[バッチ バランシング](../../../supply-chain/production-control/batch-balancing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-187">For more information about batch balancing, see [Batch balancing](../../../supply-chain/production-control/batch-balancing.md).</span></span>

### <a name="analytical-workspaces-with-embedded-power-bi-for-cost-management"></a><span data-ttu-id="8bc54-188">原価管理のための Power BI が埋め込まれた分析ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="8bc54-188">Analytical workspaces with embedded Power BI for Cost management</span></span>

<span data-ttu-id="8bc54-189">原価管理のための新しい分析ワークスペースは、原価管理およびコスト分析のワークスペースに埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-189">New Analytical workspaces for Cost management are embedded in the Cost administration and Cost Analysis workspaces.</span></span> <span data-ttu-id="8bc54-190">コンテンツ パックには、期首残高、期末残高、正味調達および正味使用量などの措置が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8bc54-190">The content pack includes measures such as beginning balance, ending balance, net sourcing and net usage.</span></span> <span data-ttu-id="8bc54-191">在庫回転率、手持在庫日数、在庫の精度などの一連の計算メジャーも含まれています。</span><span class="sxs-lookup"><span data-stu-id="8bc54-191">A set of calculated measures, such as inventory turn ratio, days inventory on-hand, and inventory accuracy are also included.</span></span> <span data-ttu-id="8bc54-192">**原価管理** Power BI コンテンツは、**原価管理** および **コスト分析** ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-192">The **Cost management** Power BI content is shown in the **Cost administration** and **Cost analysis** workspaces.</span></span> <span data-ttu-id="8bc54-193">詳細については、[原価管理 Power BI コンテンツ](../../dev-itpro/analytics/cost-management-content-pack.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-193">For more information, see [Cost management Power BI content](../../dev-itpro/analytics/cost-management-content-pack.md).</span></span>

## <a name="globalization"></a><span data-ttu-id="8bc54-194">グローバリゼーション</span><span class="sxs-lookup"><span data-stu-id="8bc54-194">Globalization</span></span>

### <a name="india-localization--project-and-upgrade"></a><span data-ttu-id="8bc54-195">インド ローカライズ – プロジェクトとアップグレード</span><span class="sxs-lookup"><span data-stu-id="8bc54-195">India localization – project and upgrade</span></span>

<span data-ttu-id="8bc54-196">ユーザーはプロジェクト管理および会計モジュールでインドの商品及びサービス税 (GST) を管理でき、AX 2012 の顧客は Dynamics 365 for Finance and Operations にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-196">Users can manage India Goods and Services Tax (GST) for the Project management and accounting module, and AX 2012 customers can upgrade to Dynamics 365 for Finance and Operations.</span></span>

### <a name="enhanced-configurability"></a><span data-ttu-id="8bc54-197">拡張されたコンフィギュレーションの可能性</span><span class="sxs-lookup"><span data-stu-id="8bc54-197">Enhanced configurability</span></span>

<span data-ttu-id="8bc54-198">新機能にはインポートとテスト シナリオが含まれており、コーディングなしでコンフィギュレーションが可能になるより広範なサポートも含まれます。</span><span class="sxs-lookup"><span data-stu-id="8bc54-198">New features include import and testing scenarios, and also broader support for configurability without coding.</span></span>

## <a name="servicing-performance-and-deployment"></a><span data-ttu-id="8bc54-199">保守、パフォーマンス、展開</span><span class="sxs-lookup"><span data-stu-id="8bc54-199">Servicing, performance, and deployment</span></span>

### <a name="improved-delivery-of-platform-and-financial-reporting-updates"></a><span data-ttu-id="8bc54-200">プラットフォームおよび財務レポート更新のデリバリーの強化</span><span class="sxs-lookup"><span data-stu-id="8bc54-200">Improved delivery of platform and financial reporting updates</span></span>

<span data-ttu-id="8bc54-201">プラットフォームおよび財務レポートの更新は、オプションの更新プログラムではなく、Microsoft によって管理される継続的な更新になります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-201">Platform and financial reporting updates will be continual updates managed by Microsoft rather than optional updates.</span></span> <span data-ttu-id="8bc54-202">この変更は、サービスの信頼性と可用性を向上させるとともに、最新の改善と修正を顧客に確実に提供することを目的としています。 </span><span class="sxs-lookup"><span data-stu-id="8bc54-202">This change is intended to improve service reliability and availability, and also to ensure that customers have the latest improvements and fixes.</span></span> <span data-ttu-id="8bc54-203">プラットフォームと財務レポートの更新には、下位互換性があります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-203">Platform and financial reporting updates are backward-compatible.</span></span> <span data-ttu-id="8bc54-204">詳細については、[1 つのバージョン サービスに関してよく寄せられる質問](./one-version.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-204">For more information, see [One Version service updates FAQ](./one-version.md).</span></span>

### <a name="upgrade-automation"></a><span data-ttu-id="8bc54-205">自動アップグレード</span><span class="sxs-lookup"><span data-stu-id="8bc54-205">Upgrade automation</span></span>

<span data-ttu-id="8bc54-206">アップグレードの自動化により、非運用環境で LCS を使用して、顧客に対しメジャー バージョンのアップグレードをセルフ サービス操作として提供します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-206">Upgrade automation makes major version upgrades a self-service operation for the customer, using LCS for non-production environments.</span></span>

### <a name="service-hardening"></a><span data-ttu-id="8bc54-207">サービスの強化</span><span class="sxs-lookup"><span data-stu-id="8bc54-207">Service hardening</span></span>

<span data-ttu-id="8bc54-208">主要な業務プロセスの監視と警告を追加し、最も使用頻度の高いフォームのフォーム負荷パフォーマンスを改善します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-208">Added service monitoring and alerting for core business processes, and improved form load performance of the most commonly used forms.</span></span>

### <a name="lifecycle-services-sandbox-self-service-automation-and-rdp-lockdown"></a><span data-ttu-id="8bc54-209">Lifecycle Services サンドボックス セルフサービス自動化および RDP ロックダウン</span><span class="sxs-lookup"><span data-stu-id="8bc54-209">Lifecycle Services sandbox self-service automation and RDP lockdown</span></span>

<span data-ttu-id="8bc54-210">サンドボックス セルフサービスの自動化では、リモート デスクトップを介したサンドボックス環境へのアクセスがなくても、データの移動、デバッグ工程、監視、および診断がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8bc54-210">Sandbox self-service automation supports data movement, debugging operations, monitoring, and diagnostics without requiring access to the sandbox environments through Remote Desktop.</span></span> <span data-ttu-id="8bc54-211">サンドボックス環境のリモート デスクトップ機能は使用されなくなります。</span><span class="sxs-lookup"><span data-stu-id="8bc54-211">Remote Desktop capabilities for sandbox environments will be deprecated.</span></span> <span data-ttu-id="8bc54-212">つまり、顧客は VM にアクセスするためにリモート デスクトップを使用する必要がなくなり、信頼性とセキュリティが向上します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-212">This means that customers won't be required to use Remote Desktop to access the VM, which improves reliability and security.</span></span>

## <a name="compliance"></a><span data-ttu-id="8bc54-213">コンプライアンス</span><span class="sxs-lookup"><span data-stu-id="8bc54-213">Compliance</span></span>

### <a name="general-data-protection-regulation-gdpr"></a><span data-ttu-id="8bc54-214">一般データ保護規則 (GDPR)</span><span class="sxs-lookup"><span data-stu-id="8bc54-214">General Data Protection Regulation (GDPR)</span></span>

<span data-ttu-id="8bc54-215">投資は、欧州のプライバシーに関する法律の要件に対応します。</span><span class="sxs-lookup"><span data-stu-id="8bc54-215">Investments address the European privacy law's requirements.</span></span> <span data-ttu-id="8bc54-216">準拠に役立つリソースを検索するには [Trust Center](https://www.microsoft.com/trustcenter/compliance/accessibility) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-216">Go to the [Trust Center](https://www.microsoft.com/trustcenter/compliance/accessibility) to learn more and find resources to help you comply.</span></span>

### <a name="accessibility-enhancements"></a><span data-ttu-id="8bc54-217">アクセシビリティの拡張機能</span><span class="sxs-lookup"><span data-stu-id="8bc54-217">Accessibility enhancements</span></span>

<span data-ttu-id="8bc54-218">業界をリードするアクセシビリティ標準については [Trust Center](https://www.microsoft.com/trustcenter/compliance/accessibility) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc54-218">Go to the [Trust Center](https://www.microsoft.com/trustcenter/compliance/accessibility) to learn about our industry-leading accessibility standards.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
