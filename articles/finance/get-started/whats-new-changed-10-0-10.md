---
title: Dynamics 365 Finance バージョン 10.0 (2020 年 4 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 Finance バージョン 10.0.10 プレビュー リリースの新機能または変更された機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-05
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 70310c0f9ba547d8d0cbedba48eb641a26079dba
ms.sourcegitcommit: 794cbfee6077e75747cfcc4a977b7ab01cbc1a2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3165042"
---
# <a name="preview-features-in-dynamics-365-finance-version-10010-march-2020"></a>Dynamics 365 Finance バージョン 10.0.10 (2020 年 3 月) の機能をプレビューする

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance プレビュー バージョン 10.0.10 の新機能または変更された機能について説明します。 このバージョンには 10.0.420 のビルド番号が含まれており、次のように使用できます。

- **プレビュー リリース :** 2020 年 3 月
- **一般提供 (自己更新) :**  2020 年 4 月
- **自動更新 :** 2020 年 5 月

このリリースでは次の機能が含まれています。 機能タイトルは、[リリース計画](https://docs.microsoft.com/dynamics365/release-plans/)のサイトに関する追加情報にリンクします。 

- [パフォーマンスを高める予算計画クエリの最適化](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/budget-planning-query-optimization-performance)

 - [仕訳帳別転記済トランザクションの日付範囲](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/date-range-posted-transactions-journals-report)
 
 - [伝票トランザクション リストページへの仕入先 ID、顧客 ID、仕入先名、および顧客名の追加](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/add-vendor-id-customer-id-vendor-name-customer-name-voucher-transactions-list-page)
 
 - [請求書の合計と登録済請求書の合計が一致しない場合に、ワークフローへの送信を禁止します](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/prohibit-submission-workflow-when-invoice-total-registered-invoice-total-are-not-equal)
 
 - [利息の配送と使用の確認 機能を有効にする – 詳細な元帳エントリの転記時に銀行残高を更新できます](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/allow-interest-distribution-escheatment-use-feature--lets-update-bank-balances-when-posting-advanced-ledger-entries)
 
 - [レポート年別の税 1099 詳細レポートのフィルター処理が可能です](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/allow-filtering-tax-1099-detail-report-reporting-year)

 - [拡張されたイタリアのローカリゼーション : 支払時のコミッション決済](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/extended-italian-localization-commission-settlement-payments)
 
 - [拡張されたイタリアのローカリゼーション : 銀行と送金タイプのコンフィギュレーション可能な転記プロファイル](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/extended-italian-localization-configurable-posting-profiles-banks-remittance-types)
 
 - [拡張されたイタリアのローカリゼーション : 受取手形の受取拒否の対応](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/extended-italian-localization-protest-handling-bills-exchange)


 
## <a name="additional-resources"></a>追加リソース

### <a name="platform-update-34"></a>プラットフォーム update 34

Microsoft Dynamics 365 Finance 10.0.10 プレビューには、プラットフォーム更新 34 が含まれています。 詳細については、[プラットフォームアップデート 34 のプレビュー機能](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md)を参照してください。


### <a name="bug-fixes-and-additional-enhancements"></a>バグ修正およびその他の機能強化
10.0.10 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=424137&dbType=3&qc=bf63d49dcc96e51eb42ac1dd66c6c5e5d7548f1e176f729e324ea3353b9860cb) を参照してください。

#### <a name="add-vendor-id-and-vendor-name-to-the-posted-projects-list-page"></a>仕入先 ID と仕入先名を転記済プロジェクトのリスト ページに追加します
この機能を有効にすると、プロジェクト関連の発注書の経費について **転記されたプロジェクト リストページ** に仕入先 ID と仕入先名が表示されます。

#### <a name="enable-default-accounting-setup-for-project"></a>プロジェクトの既定の会計設定の有効化
この機能を使用すると、既定の財務分析コードや消費税グループなどの既定の会計設定データを、プロジェクト リスト ページまたはプロジェクト契約リスト ページから表示して編集することができます。 有効にすると、**すべてのプロジェクト リスト ページ** の **プロジェクト** タブ 上と **プロジェクト契約リスト ページ** の **プロジェクト契約** タブから  **既定の会計を表示** メニューがあります。 **既定の会計の表示** をクリックすると、詳細 フォームを開くのではなく、リスト ページから特定の会計設定情報を表示および管理できる サイド ファクト ボックス フォームが開きます。

### <a name="dynamics-365-2020-release-wave-1-plan"></a>Dynamics 365: 2020 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2020 リリース ウェーブ 1 プラン](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/index) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[削除済みまたは非推奨の機能](removed-deprecated-features-finance.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。
