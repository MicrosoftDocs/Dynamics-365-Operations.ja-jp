---
title: Finance and Operations バージョン 10.0 (2019 年 4 月) の新機能および変更された機能
description: このトピックでは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 のプレビュー中の機能について説明します。 このバージョンは、2019 年 4 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: a362a31d-44df-45c5-b698-64c5264c592e
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: Release 10
ms.openlocfilehash: e469b9867ffc2d6d86e0449f81d5950073a6f12b
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863513"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-100-april-2019"></a><span data-ttu-id="8ab02-104">Finance and Operations バージョン 10.0 (2019 年 4 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="8ab02-104">What's new or changed in Finance and Operations version 10.0 (April 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ab02-105">このトピックでは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-105">This topic describes features that are new or changed in Microsoft Dynamics 365 for Finance and Operations version 10.0.</span></span> <span data-ttu-id="8ab02-106">このバージョンのビルド番号は 10.0.8 です。</span><span class="sxs-lookup"><span data-stu-id="8ab02-106">This version has a build number of 10.0.8.</span></span> <span data-ttu-id="8ab02-107">バージョン 10.0 の詳細については [追加リソース](whats-new-changed-10.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-107">For more information about version 10.0, see [Additional resources](whats-new-changed-10.md#additional-resources).</span></span>

<span data-ttu-id="8ab02-108">Microsoft Dynamics 365 for Retail の機能については [Dynamics 365 for Retail (2019 年 4 月) の新機能および変更された機能](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/april-whats-new) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-108">To learn about the features in Microsoft Dynamics 365 for Retail, see [What's new or changed in Dynamics 365 for Retail (April 2019)](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/april-whats-new).</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="8ab02-109">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="8ab02-109">Extensibility enhancements</span></span>

<span data-ttu-id="8ab02-110">Finance and Operations の今回のリリースでは、列挙、メタデータ、メソッドの強化など、拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-110">In this release of Finance and Operations, numerous extensibility enhancements have been made to support extensibility including enhancements to enumerations, metadata, and methods.</span></span> <span data-ttu-id="8ab02-111">詳細については、[Dynamics 365 for Finance and Operations バージョン 10.0 で変更された拡張機能](../../dev-itpro/extensibility/extensibility-changes-10.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-111">For detailed information, see [Extensibility changes in Dynamics 365 for Finance and Operations version 10.0](../../dev-itpro/extensibility/extensibility-changes-10.md).</span></span>

## <a name="catch-weight-product-processing-with-warehouse-management"></a><span data-ttu-id="8ab02-112">倉庫管理による CW 製品の処理</span><span class="sxs-lookup"><span data-stu-id="8ab02-112">Catch weight product processing with warehouse management</span></span>
<span data-ttu-id="8ab02-113">この機能を使用すると、倉庫管理プロセス内の CW 製品を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-113">This feature allows you to use catch weight products within warehouse management processes.</span></span> <span data-ttu-id="8ab02-114">この機能は、今回のリリースの制限対象者のみに提供できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-114">This feature is only available to a limited audience for this release.</span></span> 

<span data-ttu-id="8ab02-115">詳細については、[倉庫管理の CW 製品処理](../../supply-chain/warehousing/catch-weight-processing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-115">For more information, see [Catch weight product processing with warehouse management](../../supply-chain/warehousing/catch-weight-processing.md).</span></span>

## <a name="master-planning-stability-and-recovery-improvements"></a><span data-ttu-id="8ab02-116">マスター プランの安定性と復元性の改善</span><span class="sxs-lookup"><span data-stu-id="8ab02-116">Master planning stability and recovery improvements</span></span>

<span data-ttu-id="8ab02-117">マスター プランが、継続的な改善を行うことにより不具合や接続の問題に対してより柔軟な対応ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-117">Master planning will be made more resilient to failures and connectivity issues through multiple, incremental improvements.</span></span> <span data-ttu-id="8ab02-118">これにより、マスタープランの機能が強化され、例外処理により中断されることなく復旧できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-118">This will enhance the ability for master planning to recover from exceptions without being stopped.</span></span>

<span data-ttu-id="8ab02-119">以前はマスター プランが停止した場合は、マスター プランの再実行する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="8ab02-119">If master planning is stopped, it has been necessary to restart the master planning run.</span></span> <span data-ttu-id="8ab02-120">このプロセスが改善され、マスター プランが中断した場合は自動的に停止した地点から再開するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8ab02-120">This process has been improved so that master planning will now restart automatically from where it was stopped.</span></span> <span data-ttu-id="8ab02-121">これはマスタープランにおいて時間を重視するお客様にとって重要な改善点となります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-121">This will be a significant improvement for customers where master planning is a time-critical process.</span></span>

##  <a name="improved-removal-of-obsolete-planning-data"></a><span data-ttu-id="8ab02-122">使われていないプランデータの削除機能を改善しています</span><span class="sxs-lookup"><span data-stu-id="8ab02-122">Improved removal of obsolete planning data</span></span>

<span data-ttu-id="8ab02-123">マスター プランが正常に実行された後、不要になったプランデータをクリーンアップ ジョブが削除するよう設定されています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-123">After a successful master planning run, a clean-up job is scheduled to remove planning data that is no longer needed.</span></span> <span data-ttu-id="8ab02-124">マスター プランの実行時に不備があった際には、データのクリーンアップはされません。そのため不要なデータの収集をしてしまうリスクを回避できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-124">In some cases, such as a failed master planning run, the data would not be cleaned up thereby incurring risk of aggregating unnecessary data.</span></span>

<span data-ttu-id="8ab02-125">クリーンアップ ジョブは機能強化されており、以前に失敗したマスタープランの実行データを削除します、また他の処理スレッドをブロックすることなく、使用可能なすべてのヘルパーが実行されるようを最適化されています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-125">The clean-up job has now been enhanced to remove data from previously failed master planning runs, and the design has been optimized to never block other threads, leaving all helpers available for the master planning run.</span></span> <span data-ttu-id="8ab02-126">これらの機能強化は、会社間マスタ プランにも適用されています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-126">These improvements also apply to intercompany master planning.</span></span>

## <a name="realize-the-conditional-tax-when-postdated-checks-are-drawn"></a><span data-ttu-id="8ab02-127">先日付小切手が引き落とされたときに条件付税を現金化する</span><span class="sxs-lookup"><span data-stu-id="8ab02-127">Realize the conditional tax when postdated checks are drawn</span></span>

<span data-ttu-id="8ab02-128">条件付加税とは、一部の国/地域で必要とされる現金対象の付加価値税 (VAT) です。</span><span class="sxs-lookup"><span data-stu-id="8ab02-128">Conditional tax is cash basis value-added tax (VAT) that is required in some countries/regions.</span></span> <span data-ttu-id="8ab02-129">請求書の支払を行うまでは、この税を差し引くことができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-129">This tax can be deducted until you have paid the invoice.</span></span> <span data-ttu-id="8ab02-130">支払方法が先日付小切手の場合は、支払いの際、または先日付小切手が引き落とされる際に税金を現金化するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-130">If the payment method is posted checks, you now have the option to realize the tax during payment or when the posted checks are drawn.</span></span> <span data-ttu-id="8ab02-131">このオプションを有効にするには **現金および銀行管理パラメーター > 先日付小切手 > 先日付小切手が引き落とされるときに、条件付け税を現金化** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-131">To enable this option, go to **Cash and bank management parameters > Postdated checks > Realize the conditional tax when postdated checks are drawn**.</span></span> <span data-ttu-id="8ab02-132">詳細については、「 [条件付消費税](../../financials/general-ledger/indirect-taxes-overview.md#conditional-sales-tax) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-132">For more information, see [Conditional tax](../../financials/general-ledger/indirect-taxes-overview.md#conditional-sales-tax).</span></span> 

## <a name="non-gst-transactions-for-india"></a><span data-ttu-id="8ab02-133">インド向けの非販売税トランザクション</span><span class="sxs-lookup"><span data-stu-id="8ab02-133">Non-GST transactions for India</span></span> 
<span data-ttu-id="8ab02-134">この機能を使用すると、税エンジンを使用して非販売税トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-134">This feature allows you to create non-GST transactions with the Tax engine.</span></span> <span data-ttu-id="8ab02-135">非販売税トランザクションを作成するには、それぞれの課税対象トランザクション行の **税情報** で **非販売税** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-135">To create a non-GST transaction, select the **Non-GST** check box in the **Tax information** of each taxable transaction line.</span></span> <span data-ttu-id="8ab02-136">また、**参照番号順序グループ** に **供給の請求** の **番号順序コード** があることも確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-136">You also need to make sure that there is a **Number sequence code** for **Bill of supply** in the **Reference number sequence group**.</span></span> <span data-ttu-id="8ab02-137">これらのトランザクションは、販売税還付 (GSTR) で非販売税トランザクションとして識別されます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-137">These transactions will be identified as non-GST transactions in the GST return (GSTR).</span></span> 

## <a name="tax-engine"></a><span data-ttu-id="8ab02-138">税エンジン</span><span class="sxs-lookup"><span data-stu-id="8ab02-138">Tax engine</span></span>

> [!NOTE]
> <span data-ttu-id="8ab02-139">税エンジン (GTE) は、現在のみインドのみで使用可能となっています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-139">The tax engine (GTE) is currently only available for India.</span></span>

<span data-ttu-id="8ab02-140">今回のリリースには、税エンジンを対象とする次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-140">This release includes the following features for the Tax engine.</span></span>

### <a name="improving-tax-configuration-usability-with-reduced-number-of-lookups"></a><span data-ttu-id="8ab02-141">参照処理を削減することで、税コンフィギュレーションの操作性が向上しました</span><span class="sxs-lookup"><span data-stu-id="8ab02-141">Improving tax configuration usability with reduced number of lookups</span></span>

<span data-ttu-id="8ab02-142">税エンジン (GTE) を使用して税をコンフィギュレーションする際に、税率、非控除割合、税コンポーネント、税期間を参照する複数のテーブルを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-142">While configuring tax using the Tax engine (GTE), you can define multiple tables to look up tax rates, non-deductible percentages, tax components, tax periods, and more.</span></span> <span data-ttu-id="8ab02-143">この機能を使って組み合わせの設定をすることで、参照する テーブルの数を削減することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-143">This feature reduces the number of lookup tables by combining them.</span></span> <span data-ttu-id="8ab02-144">たとえば、 **原産国/地域** 、 **消費国/地域** 、および **製品タイプ** などの データ モデル プロパティは、いろいろな場所で流用することができる税トランザクションの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-144">For example, data model properties such as **Country/Region of Origin**, **Consumption of Country/Region**, and **Product type** determine the nature of the tax transaction, which can be reused in many places.</span></span> <span data-ttu-id="8ab02-145">今回のリリースでは、参照が可能な明細行レベルで文字列型の判定を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-145">In this release, you can add a string-type measure at the line level, which can be a lookup.</span></span> <span data-ttu-id="8ab02-146">この測定は、レポートやレートなど、他の参照でさらに使用できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-146">This measure can be further used in other lookups, such as reporting and rate.</span></span>

<span data-ttu-id="8ab02-147">この機能により、管理が必要な参照処理の件数を大幅に削減することができ、税コンフィギュレーションの操作性が向上します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-147">This feature will dramatically reduce the number of lookups that you need to maintain and will improve the tax configuration usability.</span></span> <span data-ttu-id="8ab02-148">この明細行レベルの文字列型の判定機能は、税ドキュメントのユーザー インターフェイスにも表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-148">This line-level string-type measure will also be shown in the tax document user interface.</span></span>

### <a name="simplifying-tax-setup-maintenance-with-excel-integration"></a><span data-ttu-id="8ab02-149">Excelとの機能統合により、税設定のメンテナンスが簡素化されます</span><span class="sxs-lookup"><span data-stu-id="8ab02-149">Simplifying tax setup maintenance with Excel integration</span></span>

<span data-ttu-id="8ab02-150">税コンフィギュレーションにて、税金の設定パラメーター(税率を設定および非控除割合 など) を管理することは、一部の国/地域や業種によってはこの作業に手間がかかってしまいます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-150">Maintaining tax setup parameters (such as tax rates and non-deductible percentages) for tax configurations can be an effort-intensive task for users in some countries/regions and for some types of businesses.</span></span> <span data-ttu-id="8ab02-151">今回は Microsoft Excel のファイルでこれらの管理を行うことができるようになっています。このファイルは税参照テーブルに基づいて自動生成され、税設定と機能統合されています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-151">Now you can maintain these parameters in Microsoft Excel files that are automatically generated based on tax lookup tables and are integrated with the tax setup.</span></span>

### <a name="enabling-tax-configuration-with-tax-currency-and-sales-tax-codes"></a><span data-ttu-id="8ab02-152">税通貨および消費税コードによる税コンフィギュレーションの有効化</span><span class="sxs-lookup"><span data-stu-id="8ab02-152">Enabling tax configuration with tax currency and sales tax codes</span></span>

<span data-ttu-id="8ab02-153">GTE における消費税コードはの設定は、Finance and Operationsと機能統合するうえで必須となります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-153">Sales tax code is a mandatory setup for GTE to integrate with Finance and Operations.</span></span> <span data-ttu-id="8ab02-154">これまでは、 GTE が税コンフィギュレーションを同期する際に税コンポーネントと同名の消費税コードを生成しており、この消費税コードの自動生成には通貨会計が使用されています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-154">Previously, GTE created the sales tax code with the same name as the tax component when synchronizing the tax configuration, and it used the accounting currency for the auto-create sales tax codes.</span></span>

<span data-ttu-id="8ab02-155">世界中の複数の税を登録する必要のある会社は、異なる国で使用されている税通貨を税コンポーネントで管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-155">Companies with multiple tax registration across the world need to maintain different tax currencies for tax components used in different countries.</span></span> <span data-ttu-id="8ab02-156">今回のリリースでは、次の機能をご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-156">With the release of this feature, users can do the following.</span></span>

- <span data-ttu-id="8ab02-157">税設定にて消費税コードを管理します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-157">Maintain the sales tax code in tax setup.</span></span>
- <span data-ttu-id="8ab02-158">参照テーブルの消費税コードに税コンポーネントを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-158">Map the tax component to the sales tax code in lookup tables.</span></span>
- <span data-ttu-id="8ab02-159">これらの消費税コードの税通貨と決済期間を管理します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-159">Maintain tax currency and settlement period of these sales tax codes.</span></span>

<span data-ttu-id="8ab02-160">税の設定にあたり、 GTE は税取引を記録するために、割り当てられた消費税コード、税の通貨および決済期間を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-160">With the tax setup, GTE will use the mapped sales tax code, tax currency, and settlement period for posting the tax transactions.</span></span>

## <a name="expanded-regional-coverage-for-regulatory-configuration-service-rcs-deployments"></a><span data-ttu-id="8ab02-161">Regulatory Configuration Service (RCS)が展開される対象地域の拡充</span><span class="sxs-lookup"><span data-stu-id="8ab02-161">Expanded regional coverage for Regulatory Configuration Service (RCS) deployments</span></span>
<span data-ttu-id="8ab02-162">RCSへの機能拡張を継続的に行っていく一環として、対象地域を拡大しており、ここではエンドユーザーがサービス環境を任意に配置することが可能です。</span><span class="sxs-lookup"><span data-stu-id="8ab02-162">As part of the ongoing enhancements to RCS, we are increasing the breadth of regional coverage where service environments can be deployed through end-user selection.</span></span> <span data-ttu-id="8ab02-163">今回のリリースの一部として、ユーザーは次の国または地域でRCS環境をホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-163">As part of this release, users can host their RCS environments in the following countries or regions:</span></span>

- <span data-ttu-id="8ab02-164">米国</span><span class="sxs-lookup"><span data-stu-id="8ab02-164">United States</span></span> 
- <span data-ttu-id="8ab02-165">インド</span><span class="sxs-lookup"><span data-stu-id="8ab02-165">India</span></span> 
- <span data-ttu-id="8ab02-166">ヨーロッパ (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="8ab02-166">Europe (Preview)</span></span>
- <span data-ttu-id="8ab02-167">中国 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="8ab02-167">China (Preview)</span></span>

## <a name="tax-functionality-updates-for-china"></a><span data-ttu-id="8ab02-168">中国に向けた税機能のアップデート</span><span class="sxs-lookup"><span data-stu-id="8ab02-168">Tax functionality updates for China</span></span>

<span data-ttu-id="8ab02-169">中国では、正式なタックスインボイスは政府が承認した2つのインボイスソフトウェア (AisinoとBaiWang) のみが発行することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-169">In China, official tax invoices can only be issued via two government-authorized invoicing software (Aisino and BaiWang).</span></span> <span data-ttu-id="8ab02-170">この機能では発行されたインボイスを、.TXTおよび. XMLファイル形式にエクスポートし、それらファイルを必要に応じて承認されたソフトである Aisino と BaiWang にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-170">This feature lets you export the issued invoices into the .TXT and .XML file formats so you can import the files into the authorized invoicing software of Aisino and BaiWang providers accordingly.</span></span> 

<span data-ttu-id="8ab02-171">Finance and Operations の税分類とコードを管理することも可能です。これは税統合インターフェイス3.0と整合性を保ちます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-171">You can also maintain the tax classification and codes in Finance and Operations, which is in alignment with tax integration interface 3.0.</span></span> <span data-ttu-id="8ab02-172">請求書をエクスポートしたファイルには、中国では必須となっている商品コード (商品やサービスの分類) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-172">The exported invoice file will include commodity codes (classification of goods and services) which is mandatory for China.</span></span> 

<span data-ttu-id="8ab02-173">標準カテゴリ階層の設定には、エクスポートしたファイル内にインボイスの明細行に商品コードを含める機能が実装されています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-173">The standard category hierarchy setting functionality is used to include the commodity codes in the invoice lines of the exported file.</span></span>

<span data-ttu-id="8ab02-174">このリリースでは次の更新が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-174">The following updates are included in this release:</span></span>

- <span data-ttu-id="8ab02-175">BaiWangが提供するソフトとの間に新たなインターフェイスが実装されており、BaiWangのソフトウェアから出力された .TXT形式と.XML形式のファイルをインポートでき、発行されたインボイスを .XML形式で出力することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-175">There is a new interface with BaiWang provider software that lets you export issued invoices in .XML format and you can import files from BaiWang software in .TXT and .XML formats.</span></span>
- <span data-ttu-id="8ab02-176">発行するインボイスの構成が更新されたため、Aisinoが提供するソフトウェアに .TXT ファイルをインポートして連携することが可能となりました。</span><span class="sxs-lookup"><span data-stu-id="8ab02-176">We updated the structure of the issued invoice that is exported and you can import .TXT file for interface with Aisino provider software.</span></span>

<span data-ttu-id="8ab02-177">詳細については、 [中国の税統合の構成](../../financials/localizations/apac-chn-tax-integration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-177">For more information, see [Configure tax integration for China](../../financials/localizations/apac-chn-tax-integration.md).</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="8ab02-178">電子申告 (ER)</span><span class="sxs-lookup"><span data-stu-id="8ab02-178">Electronic reporting (ER)</span></span>

<span data-ttu-id="8ab02-179">今回のリリースには、電子申告 (ER)に関する次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-179">This release includes the following features for Electronic reporting (ER).</span></span>

### <a name="performance-optimization-of-customer-built-configurations"></a><span data-ttu-id="8ab02-180">ユーザーが行ったコンフィギュレーションに対するパフォーマンスの最適化</span><span class="sxs-lookup"><span data-stu-id="8ab02-180">Performance optimization of customer-built configurations</span></span>
<span data-ttu-id="8ab02-181">機能コンサルタントである「ペルソナ」が、電子申告 コンフィギュレーションの実行を記録することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-181">A functional consultant persona can enable tracing of execution of electronic reporting configuration.</span></span> <span data-ttu-id="8ab02-182">このコンサルタントは生成された記録を分析し、使用頻度の高いノードをキャッシュすることで電子申告 コンフィギュレーションパフォーマンスの最適化します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-182">This consultant can also analyze a generated trace and optimize electronic reporting configuration performance by setting caching on frequently used nodes.</span></span>

<span data-ttu-id="8ab02-183">これまでは、キャッシュの対象となっていたものは一定のレコードのみであり、処理に関連するレコードはキャッシュされていませんでした。</span><span class="sxs-lookup"><span data-stu-id="8ab02-183">Before this release, caching supported only a flat list of records, which meant that any related records were not cached.</span></span> <span data-ttu-id="8ab02-184">この機能は、入れ子構造のレコードをキャッシュすることができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-184">This feature allows caching of nested records.</span></span> <span data-ttu-id="8ab02-185">また、本機能を使うことで 「ずる賢い」キャッシュを行うことができます。 参照されたレコードのみをキャッシュし、全体をキャッシュしません。</span><span class="sxs-lookup"><span data-stu-id="8ab02-185">It also allows users to enable “lazy” caching, when only referenced records are being cached, not the whole list.</span></span>

### <a name="setting-up-parameters-by-legal-entity"></a><span data-ttu-id="8ab02-186">法人別パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="8ab02-186">Setting up parameters by legal entity</span></span>

<span data-ttu-id="8ab02-187">この機能では、抽象データソースを含むER形式の構成をすることができ、法人ユーザーがどのようにデータ ソースを入力するか指定することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-187">This feature allows you to configure an ER format that includes an abstract data source and lets you specify how this data source can be filled in by a business user.</span></span> <span data-ttu-id="8ab02-188">ビジネス ユーザーは、Finance and Operationsのインターフェースを使って指定した法人のマスターデータをもとにERフォーマットを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-188">The business user can then use the Finance and Operations user interface to set up an ER format with master data from a specific legal entity.</span></span> <span data-ttu-id="8ab02-189">これは、対応するERフォーマットの実行を制御する可能性のある法人に対して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-189">This can be done for any legal entity that might control execution of the corresponding ER format.</span></span>

<span data-ttu-id="8ab02-190">この機能では、 ビジネス ユーザー が Finance and Operations インスタンスから特定の企業のERフォーマットをマスターデータとともにエクスポートし、もう一方へとインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-190">This feature also enables a business user to export an ER format with master data for a specific company from one Finance and Operations instance and import it to another one.</span></span>

### <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="8ab02-191">生成されたドキュメント用にカスタマイズされた保存先を指定します</span><span class="sxs-lookup"><span data-stu-id="8ab02-191">Specify a custom storage location for generated documents</span></span>

<span data-ttu-id="8ab02-192">新たなERの拡張点としては、コードを作成することができ、その中でERフォーマットが生成されるドキュメントにアクセスすることが可能なイベントに参加できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-192">A new ER extensibility point is introduced allowing you to write a custom code in which you can subscribe to an event giving you access to any of the documents that ER formats generate.</span></span> <span data-ttu-id="8ab02-193">ERフレームワークに対応したファイルの保存先を拡張することができ、ドキュメントを継続的に保存していくことが可能です。</span><span class="sxs-lookup"><span data-stu-id="8ab02-193">This feature lets you extend the list of storage locations that are supported by ER framework to keep generated documents.</span></span>

<span data-ttu-id="8ab02-194">詳細については、次の [生成されたドキュメントの保管場所を指定する](../../dev-itpro/analytics/er-custom-storage-generated-documents.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-194">For more information, see [Specify a custom storage location for generated documents](../../dev-itpro/analytics/er-custom-storage-generated-documents.md).</span></span>

### <a name="post-processing-of-imported-files"></a><span data-ttu-id="8ab02-195">ファイルをインポートした後の処理</span><span class="sxs-lookup"><span data-stu-id="8ab02-195">Post-processing of imported files</span></span>

<span data-ttu-id="8ab02-196">電子申告 (ER) のインポート機能は、処理大砲のファイルの取得先として SharePoint のフォルダを使用しています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-196">Import functionality in Electronic reporting (ER) uses SharePoint folders to get the next set of files for processing.</span></span> <span data-ttu-id="8ab02-197">前回までのリリースでは、処理されたファイルを管理する自動プロセスが実装されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="8ab02-197">In previous releasess there was no automatic process to manage processed files.</span></span> <span data-ttu-id="8ab02-198">たとえば、正常に処理されたファイルは SharePoint のソース フォルダーから自動的に削除され、他の場所に移動することができませんでした。</span><span class="sxs-lookup"><span data-stu-id="8ab02-198">For example, successfully processed files were automatically deleted from a SharePoint source folder and couldn't be moved to another location.</span></span> <span data-ttu-id="8ab02-199">結果として、さらなる手作業が必要となり誤操作の潜在的原因となっていました。</span><span class="sxs-lookup"><span data-stu-id="8ab02-199">This resulted in additional manual work and potential errors.</span></span> <span data-ttu-id="8ab02-200">この機能には処理済みのファイルを管理する機能が実装されており、処理終了後の動作を設定することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-200">With this feature, there is a process to automatically manage processed files, which allows you to configure the post-processing actions.</span></span> <span data-ttu-id="8ab02-201">ERフォーマットの読み込みの設定を変更することで、次の動作を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-201">By changing the source settings of an ER format, you can configure the following actions:</span></span>

<span data-ttu-id="8ab02-202">正常に処理されたファイルのフォルダー</span><span class="sxs-lookup"><span data-stu-id="8ab02-202">For successfully processed files:</span></span>
- <span data-ttu-id="8ab02-203">読み込み元の SharePoint フォルダからファイルを削除する。</span><span class="sxs-lookup"><span data-stu-id="8ab02-203">Delete files from the source SharePoint folder.</span></span>
- <span data-ttu-id="8ab02-204">処理済ファイルを別の SharePoint フォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="8ab02-204">Move files to another SharePoint folder.</span></span>
<span data-ttu-id="8ab02-205">警告で処理されるファイルの場合</span><span class="sxs-lookup"><span data-stu-id="8ab02-205">For files that are processed with warnings:</span></span>
- <span data-ttu-id="8ab02-206">読み込み元の SharePoint フォルダにファイルを保持する。</span><span class="sxs-lookup"><span data-stu-id="8ab02-206">Keep files in the source SharePoint folder.</span></span>
- <span data-ttu-id="8ab02-207">処理済ファイルを別の SharePoint フォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="8ab02-207">Move files to another SharePoint folder.</span></span>
<span data-ttu-id="8ab02-208">処理に失敗したファイル</span><span class="sxs-lookup"><span data-stu-id="8ab02-208">For files that failed to process:</span></span>
- <span data-ttu-id="8ab02-209">読み込み元の SharePoint フォルダにファイルを保持する。</span><span class="sxs-lookup"><span data-stu-id="8ab02-209">Keep files in the source SharePoint folder.</span></span>
- <span data-ttu-id="8ab02-210">処理済ファイルを別の SharePoint フォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="8ab02-210">Move files to another SharePoint folder.</span></span>

### <a name="generate-documents-in-pdf-format-by-filling-in-pdf-templates"></a><span data-ttu-id="8ab02-211">PDFのテンプレートに入力することにより、PDF形式でドキュメントを生成を可能にします。</span><span class="sxs-lookup"><span data-stu-id="8ab02-211">Generate documents in PDF format by filling in PDF templates</span></span>

<span data-ttu-id="8ab02-212">この機能では、レポートをPDF形式で生成するにあたって、入力可能なPDFドキュメントをテンプレートとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-212">This feature allows you to use a fillable PDF document as a template for generating reports in the PDF format.</span></span> <span data-ttu-id="8ab02-213">設計時に調整済みのERフォーマットにPDFをインポートすることで、入力が必要な項目が検出されERフォーマットに新たな要素が自動で生成されます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-213">You can import the PDF at design time to a configured ER format which automatically generates new elements of this ER format for discovered fields that need to be filled in.</span></span> <span data-ttu-id="8ab02-214">ERフォーマット上に生成された要素にバインドを追加することで、PDFテンプレート上の必要項目に入力をすることが可能となります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-214">By adding bindings to generated elements of an ER format, you can fill in necessary fields of the PDF template by running this ER format.</span></span> <span data-ttu-id="8ab02-215">この機能を使用することで、ERフォーマットを設定して複数のPDFドキュメントを生成したうえで、自動的にそれら複数のファイルを1つの最終版PDFドキュメントに統合することも可能です。</span><span class="sxs-lookup"><span data-stu-id="8ab02-215">With this feature, you can also configure an ER format generating multiple PDF documents and automatically merge them into a single, final PDF document.</span></span>

## <a name="russian-features"></a><span data-ttu-id="8ab02-216">ロシア用の機能</span><span class="sxs-lookup"><span data-stu-id="8ab02-216">Russian features</span></span>

### <a name="cash-flow-management"></a><span data-ttu-id="8ab02-217">キャッシュ フロー管理</span><span class="sxs-lookup"><span data-stu-id="8ab02-217">Cash flow management</span></span> 

<span data-ttu-id="8ab02-218">この機能によって、次のことが可能となります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-218">This functionality allows you to do the following:</span></span>
- <span data-ttu-id="8ab02-219">キャッシュ フローを予測し、分析を行う</span><span class="sxs-lookup"><span data-stu-id="8ab02-219">Obtain a cash flow forecast and perform an analysis.</span></span>
- <span data-ttu-id="8ab02-220">支払スケジュール仕訳帳を使用して支払を日次単位で管理する</span><span class="sxs-lookup"><span data-stu-id="8ab02-220">Manage payments on a daily basis using payment schedule journals.</span></span>
- <span data-ttu-id="8ab02-221">会社の現金持高を管理する</span><span class="sxs-lookup"><span data-stu-id="8ab02-221">Control the company’s cash position.</span></span>
- <span data-ttu-id="8ab02-222">集中管理方式で会社のキャッシュ フローを管理する</span><span class="sxs-lookup"><span data-stu-id="8ab02-222">Maintain the company’s cash flows with centralized control.</span></span>

<span data-ttu-id="8ab02-223">詳細については、「 [キャッシュ フローの管理 (ロシア) ](../../financials/localizations/rus-cash-flow.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-223">For more information, see [Cash flow management (Russia)](../../financials/localizations/rus-cash-flow.md).</span></span>

### <a name="other-incomes-and-expenses-profit-tax-registers"></a><span data-ttu-id="8ab02-224">その他の収入/支出 収益税 の登録</span><span class="sxs-lookup"><span data-stu-id="8ab02-224">Other incomes and expenses profit tax registers</span></span>

<span data-ttu-id="8ab02-225">次の税登録を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-225">The following tax registers are available:</span></span>

- <span data-ttu-id="8ab02-226">現在の期間の収入</span><span class="sxs-lookup"><span data-stu-id="8ab02-226">Current period incomes</span></span>
- <span data-ttu-id="8ab02-227">税経費</span><span class="sxs-lookup"><span data-stu-id="8ab02-227">Tax expenses</span></span>
- <span data-ttu-id="8ab02-228">現在の期間の他の経費</span><span class="sxs-lookup"><span data-stu-id="8ab02-228">Other expenses of current period</span></span>
- <span data-ttu-id="8ab02-229">現在の期間の未実現経費</span><span class="sxs-lookup"><span data-stu-id="8ab02-229">Unrealized expenses of current period</span></span>
- <span data-ttu-id="8ab02-230">その他の未実現経費</span><span class="sxs-lookup"><span data-stu-id="8ab02-230">Other unrealized expenses</span></span>

### <a name="localization-of-process-industries"></a><span data-ttu-id="8ab02-231">Process Industries のローカライズ</span><span class="sxs-lookup"><span data-stu-id="8ab02-231">Localization of process industries</span></span>

<span data-ttu-id="8ab02-232">以下2点での基本的なローカライズが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="8ab02-232">Basic localization in the following two areas is available:</span></span>
- <span data-ttu-id="8ab02-233">すべての新しい総勘定元帳の転記に対応しています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-233">Correspondence of accounts for all new general ledger postings.</span></span>
- <span data-ttu-id="8ab02-234">機能面においてプロセス産業とロシア国の関係性の共存を実現しています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-234">Functional coexistence of process industries features and Russian country context.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ab02-235">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8ab02-235">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8ab02-236">バグ修正</span><span class="sxs-lookup"><span data-stu-id="8ab02-236">Bug fixes</span></span>
<span data-ttu-id="8ab02-237">Finance and Operations 10.0 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2080156)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-237">For information about the bug fixes included in each of the updates that are part of Finance and Operations version 10.0, sign in to Lifecycle Services (LCS) and view the [KB article](https://go.microsoft.com/fwlink/?linkid=2080156).</span></span> 

## <a name="regulatory-updates"></a><span data-ttu-id="8ab02-238">規制の更新</span><span class="sxs-lookup"><span data-stu-id="8ab02-238">Regulatory updates</span></span>
<span data-ttu-id="8ab02-239">Finance and Operations の規制の更新については、[ローカライズおよび規制機能 – 規制の更新](../../financials/localizations/regulatory-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-239">For information about the regulatory updates for Finance and Operations, see [Localization and Regulatory features – Regulatory updates](../../financials/localizations/regulatory-updates.md).</span></span> <span data-ttu-id="8ab02-240">また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-240">Alternatively, you can sign in to Lifecycle Services (LCS) and view the planned regulatory updates using the issue search tool, where you can search by country, type of feature, and release.</span></span>

### <a name="platform-update-24"></a><span data-ttu-id="8ab02-241">プラットフォーム update 24</span><span class="sxs-lookup"><span data-stu-id="8ab02-241">Platform update 24</span></span>
<span data-ttu-id="8ab02-242">Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 には、プラットフォーム更新プログラム 24 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ab02-242">Microsoft Dynamics 365 for Finance and Operations version 10.0 includes Platform update 24.</span></span> <span data-ttu-id="8ab02-243">プラットフォーム更新プロフラム 24 については [Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能と変更された機能](whats-new-platform-update-24.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ab02-243">To learn more about Platform update 24, see [What's new and changed in Finance and Operations platform update 24 (March 2019)](whats-new-platform-update-24.md).</span></span>

### <a name="dynamics-365-april-19-release-notes"></a><span data-ttu-id="8ab02-244">Dynamics 365 2019 年 4 月 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="8ab02-244">Dynamics 365 April '19 release notes</span></span>
<span data-ttu-id="8ab02-245">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="8ab02-245">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="8ab02-246">[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/business-applications-release-notes/April19/index)。</span><span class="sxs-lookup"><span data-stu-id="8ab02-246">[Check out the April '19 release notes](https://docs.microsoft.com/business-applications-release-notes/April19/index).</span></span> <span data-ttu-id="8ab02-247">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-247">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="8ab02-248">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="8ab02-248">Removed and deprecated features</span></span>
<span data-ttu-id="8ab02-249">[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8ab02-249">The [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="8ab02-250">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="8ab02-250">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="8ab02-251">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-251">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="8ab02-252">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="8ab02-252">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="8ab02-253">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="8ab02-253">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="8ab02-254">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="8ab02-254">Typically these are functional updates that need to made to the compiler.</span></span>
