---
title: Finance and Operations バージョン 10.0.1 (2019 年 4 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations バージョン 10.0.1 の新機能または変更された機能について説明します。 このバージョンは 4 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 04/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: a362a31d-44df-45c5-b698-64c5264c592e
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 1504c33fd25158b4e52ba6035a3a406d07ff9d39
ms.sourcegitcommit: 3d1b0e7d0f165fbcbec9c92783e5e936b282d757
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2019
ms.locfileid: "1540139"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-1001-april-2019"></a><span data-ttu-id="2cc8e-104">Finance and Operations バージョン 10.0.1 (2019 年 4 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="2cc8e-104">What's new or changed in Finance and Operations version 10.0.1 (April 2019)</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2cc8e-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Finance and Operations version 10.0.1.</span></span> <span data-ttu-id="2cc8e-106">このバージョンは 4 月にリリースされ、ビルド番号は 10.0.51 です。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-106">This version will be released in April and has a build number of 10.0.51.</span></span> <span data-ttu-id="2cc8e-107">バージョン 10.0.1 の詳細については [追加リソース](whats-new-changed-10-0-1.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-107">For more information about version 10.0.1, see [Additional resources](whats-new-changed-10-0-1.md#additional-resources).</span></span>

<span data-ttu-id="2cc8e-108">最新のリリースの Microsoft Dynamics 365 for Retail の新機能と変更については、[Dynamics 365 for Retail バージョン 10.0.1 の新機能と変更](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/whats-new-10-0-1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-108">To learn about the new features and changes in the latest releases of Microsoft Dynamics 365 for Retail, see [What's new or changed in Dynamics 365 for Retail version 10.0.1](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/whats-new-10-0-1).</span></span>


## <a name="enable-edit-for-externally-maintained-fields"></a><span data-ttu-id="2cc8e-109">外部管理フィールドの編集を有効化</span><span class="sxs-lookup"><span data-stu-id="2cc8e-109">Enable edit for externally maintained fields</span></span>

<span data-ttu-id="2cc8e-110">見込顧客リストの現金化への統合など、外部システムとの統合シナリオのため、グローバル アドレス帳および顧客レコードの特定のフィールドは、外部システムで管理されることを予想して外部管理とマークされています。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-110">Due to integration scenarios with external systems, such as the Prospect to cash integration, certain fields on Global address book and customer records were marked as externally maintained with the expectation that these values would be maintained in an external system.</span></span> <span data-ttu-id="2cc8e-111">**外部管理フィールドの編集を有効化** オプションがグローバル アドレス帳パラメータ (**組織管理 > グローバル アドレス帳 > グローバル アドレス帳パラメータ**) に既定値の **いいえ** で追加されました。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-111">The **Enable edit for externally maintained fields** option has been added to the Global address book parameters (**Organization administration > Global address book > Global address book parameters**) with the default value of **No**.</span></span>  <span data-ttu-id="2cc8e-112">ユーザー シナリオでこれらのフィールドを外部管理の場合も編集可能にする必要がある場合は、値を **はい** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-112">If the user scenario requires these fields to be available for edit even though maintained externally, the value can be set to **Yes**.</span></span>

## <a name="russian-features"></a><span data-ttu-id="2cc8e-113">ロシア用の機能</span><span class="sxs-lookup"><span data-stu-id="2cc8e-113">Russian features</span></span>

### <a name="journal-of-alcohol-sales"></a><span data-ttu-id="2cc8e-114">アルコール販売の仕訳帳</span><span class="sxs-lookup"><span data-stu-id="2cc8e-114">Journal of alcohol sales</span></span>
<span data-ttu-id="2cc8e-115">この機能は法定形式のアルコール小売販売の仕訳帳の印刷を含みます。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-115">This functionality includes printing the journal of Alcohol retail sales in statutory format.</span></span>

### <a name="electronic-format-of-accounting-reporting"></a><span data-ttu-id="2cc8e-116">会計レポートの電子形式</span><span class="sxs-lookup"><span data-stu-id="2cc8e-116">Electronic format of accounting reporting</span></span>
<span data-ttu-id="2cc8e-117">電子申告コンフィギュレーションが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-117">Electronic reporting configuration is now available.</span></span> <span data-ttu-id="2cc8e-118">これを使用すると、電子形式で会計レポートを生成したり、構成された財務諸表に基づいて計算したデータを保持できます。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-118">It allows you to generate accounting reporting in electronic format, and contains data calculated based on the configured Financial report.</span></span> <span data-ttu-id="2cc8e-119">詳細については [電子形式の会計レポート (ロシア)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/rus-accounting-reporting) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-119">For more information, see [Accounting reporting in electronic format (Russia)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/rus-accounting-reporting)</span></span>

<span data-ttu-id="2cc8e-120">[財務諸表 (ロシア)](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/rus-financial-reports) で次の作業を行う方法に関する情報を見つけることができます:</span><span class="sxs-lookup"><span data-stu-id="2cc8e-120">You can find information about how to do the following tasks in [Financial reporting (Russia)](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/rus-financial-reports):</span></span>
- <span data-ttu-id="2cc8e-121">財務諸表を設定します。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-121">Set up financial reports.</span></span>
- <span data-ttu-id="2cc8e-122">財務諸表の計算結果を使用するように電子申告を構成します。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-122">Configure Electronic reporting to use the results of financial report calculations.</span></span>
- <span data-ttu-id="2cc8e-123">財務諸表を生成し結果を保存するように電子メッセージを構成します。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-123">Configure electronic messages to generate the financial report and store the results.</span></span>

<span data-ttu-id="2cc8e-124">Excel で財務諸表の印刷を構成する方法の詳細は [Excel での財務諸表のコンフィギュレーション (ロシア)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/rus-excel-financial-report) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-124">For more information about configuring printing for financial reports in Excel, see [Configure financial reports in Excel (Russia)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/rus-excel-financial-report)</span></span>

### <a name="assessed-tax-registers-and-electronic-format-of-declaration-version-505-2019"></a><span data-ttu-id="2cc8e-125">評価税登録および申告バージョン 5.05 (2019) の電子形式</span><span class="sxs-lookup"><span data-stu-id="2cc8e-125">Assessed tax registers and electronic format of declaration version 5.05 (2019)</span></span>
<span data-ttu-id="2cc8e-126">この機能を使用すると、2019 年の報告から適用可能な、不動産資産に関する技術情報および税務情報の保管、評価税登録の計算、および電子形式で評価税申告の生成が可能になります。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-126">This functionality allows you to keep technical and tax information for realty assets, calculate assessed tax registers, and generate assessed tax declaration in electronic format, applicable from the reporting for year 2019.</span></span> <span data-ttu-id="2cc8e-127">詳細については [評価税申告 (ロシア)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/rus-assessed-tax-declaration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-127">For more information, see [Assessed tax declaration (Russia)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/rus-assessed-tax-declaration)</span></span>

### <a name="transport-tax-registers-and-electronic-format-of-declaration"></a><span data-ttu-id="2cc8e-128">輸送税登録および申告の電子形式</span><span class="sxs-lookup"><span data-stu-id="2cc8e-128">Transport tax registers and electronic format of declaration</span></span>
<span data-ttu-id="2cc8e-129">この機能を使用して、車両の技術情報および税務情報を保持し、輸送税登録を計算し、電子形式で輸送税申告を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-129">This functionality allows you to keep technical and tax information for vehicles, calculate transport tax registers, and generate transport tax declaration in electronic format.</span></span>

### <a name="land-tax-registers-and-electronic-format-of-declaration-version-506-2018"></a><span data-ttu-id="2cc8e-130">土地税登録および申告バージョン 5.06 (2018) の電子形式</span><span class="sxs-lookup"><span data-stu-id="2cc8e-130">Land tax registers and electronic format of declaration version 5.06 (2018)</span></span>
<span data-ttu-id="2cc8e-131">この機能を使用すると、2018 年の年次報告から適用可能な、土地面積に関する技術情報および税務情報の保管、土地税登録の計算、および電子形式で土地税申告の生成が可能になります。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-131">This functionality allows you to keep technical and tax information for ground areas, calculate land tax registers, and generate land tax declaration in electronic format, applicable from the annual reporting for year 2018.</span></span>

### <a name="vat-declaration-in-electronic-format-version-506-2019"></a><span data-ttu-id="2cc8e-132">電子形式の VAT 申告バージョン 5.06 (2019)</span><span class="sxs-lookup"><span data-stu-id="2cc8e-132">VAT declaration in electronic format version 5.06 (2019)</span></span>
<span data-ttu-id="2cc8e-133">この機能によって 2019 年の報告から適用可能な XML 形式の VAT 明細書を生成できます。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-133">This functionality allows you to generate a VAT statement in XML format that is applicable from the reporting for year 2019.</span></span>
<span data-ttu-id="2cc8e-134">詳細については [VAT 申告 (ロシア)](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/rus-VAT-declaration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-134">For more information, see [VAT declaration (Russia)](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/rus-VAT-declaration).</span></span>

### <a name="sales-purchase-books-and-factures-journals-in-electronic-format-2019"></a><span data-ttu-id="2cc8e-135">販売、購買帳簿、Facture 仕訳帳の電子形式 (2019)</span><span class="sxs-lookup"><span data-stu-id="2cc8e-135">Sales, purchase books, and factures journals in electronic format (2019)</span></span>
<span data-ttu-id="2cc8e-136">この機能により、販売、購買帳簿、factures 仕訳帳を 2019 年から適用される電子形式で生成できます。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-136">This functionality allows you to generate sales, purchase books, and factures journals in electronic format applicable from the year 2019.</span></span> <span data-ttu-id="2cc8e-137">販売および購買帳簿の作業方法の詳細は [売上帳簿、購買帳簿、請求書 Facture 仕訳帳](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/rus-sales-books-purchase-books) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-137">For details about how to work with sales and purchase books, see [Sales books, purchase books, and invoice-factures journals](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/rus-sales-books-purchase-books).</span></span>

## <a name="regulatory-updates"></a><span data-ttu-id="2cc8e-138">規制の更新</span><span class="sxs-lookup"><span data-stu-id="2cc8e-138">Regulatory updates</span></span>
<span data-ttu-id="2cc8e-139">Finance and Operations の規制の更新については、[ローカライズおよび規制機能 – 規制の更新](../../financials/localizations/regulatory-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-139">For information about the regulatory updates for Finance and Operations, see [Localization and Regulatory features – Regulatory updates](../../financials/localizations/regulatory-updates.md).</span></span> <span data-ttu-id="2cc8e-140">また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-140">Alternatively, you can sign in to Lifecycle Services (LCS) and view the planned regulatory updates using the issue search tool, where you can search by country, type of feature, and release.</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="2cc8e-141">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="2cc8e-141">Extensibility enhancements</span></span>

<span data-ttu-id="2cc8e-142">このFinance and Operations のリリースでは、拡張性をサポートするために多くの機能拡張が行われています。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-142">In this release of Finance and Operations, numerous enhancements have been made to support extensibility.</span></span> <span data-ttu-id="2cc8e-143">たとえば、列挙体、メタデータ、メソッドに拡張性の機能拡張が行われています。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-143">For example, extensibility enhancements have been made to enumerations, metadata, and methods.</span></span> <span data-ttu-id="2cc8e-144">詳細については、[Dynamics 365 for Finance and Operations バージョン 10.0.1 で変更された拡張機能](../../dev-itpro/extensibility/extensibility-changes-10-1.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-144">For detailed information, see [Extensibility changes in Dynamics 365 for Finance and Operations version 10.0.1](../../dev-itpro/extensibility/extensibility-changes-10-1.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2cc8e-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2cc8e-145">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2cc8e-146">バグ修正</span><span class="sxs-lookup"><span data-stu-id="2cc8e-146">Bug fixes</span></span>
<span data-ttu-id="2cc8e-147">Finance and Operations 10.0.1 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=299640&dbType=3&qc=2da6de70aab0f4c61b0f920b3242211f5043697189d50a6e1fb1ac3d27ee5f78)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-147">For information about the bug fixes included in each of the updates that are part of Finance and Operations version 10.0.1, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=299640&dbType=3&qc=2da6de70aab0f4c61b0f920b3242211f5043697189d50a6e1fb1ac3d27ee5f78).</span></span>

### <a name="platform-update-25"></a><span data-ttu-id="2cc8e-148">プラットフォーム update 25</span><span class="sxs-lookup"><span data-stu-id="2cc8e-148">Platform update 25</span></span>
<span data-ttu-id="2cc8e-149">Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 には、プラットフォーム更新プログラム 25 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-149">Microsoft Dynamics 365 for Finance and Operations version 10.0.1 includes Platform update 25.</span></span> <span data-ttu-id="2cc8e-150">プラットフォーム更新プロフラム 25 の詳細ついては [Finance and Operations プラットフォーム更新プログラム 25 (2019 年 4 月) の新機能や変更](whats-new-platform-25.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-150">To learn more about Platform update 25, see [What's new or changed in Finance and Operations platform update 25 (April 2019)](whats-new-platform-25.md).</span></span>

### <a name="dynamics-365-april-19-release-notes"></a><span data-ttu-id="2cc8e-151">Dynamics 365 2019 年 4 月 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="2cc8e-151">Dynamics 365 April '19 release notes</span></span>
<span data-ttu-id="2cc8e-152">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="2cc8e-152">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="2cc8e-153">[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index)。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-153">[Check out the April '19 release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index).</span></span> <span data-ttu-id="2cc8e-154">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-154">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="2cc8e-155">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="2cc8e-155">Removed and deprecated features</span></span>
<span data-ttu-id="2cc8e-156">[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-156">The [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="2cc8e-157">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-157">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="2cc8e-158">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-158">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="2cc8e-159">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-159">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="2cc8e-160">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-160">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="2cc8e-161">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="2cc8e-161">Typically these are functional updates that need to made to the compiler.</span></span>

