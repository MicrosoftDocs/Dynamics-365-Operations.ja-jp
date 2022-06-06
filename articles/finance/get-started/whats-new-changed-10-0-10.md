---
title: Dynamics 365 Finance 10.0.10 (2020 年 5 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 Finance 10.0.10 の新機能または変更された機能について説明します。
author: kfend
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-05
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 88b9cb9996ce4b49265f0f8d2665428f5242970b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724827"
---
# <a name="whats-new-or-changed-in-dynamics-365-finance-10010-may-2020"></a>Dynamics 365 Finance 10.0.10 (2020 年 5 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance 10.0.10 の新機能または変更された機能について説明します。 このバージョンには 10.0.420 のビルド番号が含まれており、次のように使用できます。

- **プレビュー リリース :** 2020 年 3 月
- **一般提供 (自己更新) :**  2020 年 4 月
- **自動更新 :** 2020 年 5 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能
このリリースでは次の機能が含まれています。 機能タイトルは、[リリース計画](/dynamics365/release-plans/)のサイトに関する追加情報にリンクします。 

- [パフォーマンスを高める予算計画クエリの最適化](/dynamics365-release-plan/2020wave1/dynamics365-finance/budget-planning-query-optimization-performance)

 - [仕訳帳別転記済トランザクションの日付範囲](/dynamics365-release-plan/2020wave1/dynamics365-finance/date-range-posted-transactions-journals-report)
 
 - [伝票トランザクション リストページへの仕入先 ID、顧客 ID、仕入先名、および顧客名の追加](/dynamics365-release-plan/2020wave1/dynamics365-finance/add-vendor-id-customer-id-vendor-name-customer-name-voucher-transactions-list-page)
 
 - [請求書の合計と登録済請求書の合計が一致しない場合に、ワークフローへの送信を禁止します](/dynamics365-release-plan/2020wave1/dynamics365-finance/prohibit-submission-workflow-when-invoice-total-registered-invoice-total-are-not-equal)
 
 - [利息の配送と使用の確認 機能を有効にする – 詳細な元帳エントリの転記時に銀行残高を更新できます](/dynamics365-release-plan/2020wave1/dynamics365-finance/allow-interest-distribution-escheatment-use-feature--lets-update-bank-balances-when-posting-advanced-ledger-entries)
 
 - [レポート年別の税 1099 詳細レポートのフィルター処理が可能です](/dynamics365-release-plan/2020wave1/dynamics365-finance/allow-filtering-tax-1099-detail-report-reporting-year)

 - [拡張されたイタリアのローカリゼーション : 支払時のコミッション決済](/dynamics365-release-plan/2020wave1/dynamics365-finance/extended-italian-localization-commission-settlement-payments)
 
 - [拡張されたイタリアのローカリゼーション : 銀行と送金タイプのコンフィギュレーション可能な転記プロファイル](/dynamics365-release-plan/2020wave1/dynamics365-finance/extended-italian-localization-configurable-posting-profiles-banks-remittance-types)
 
 - [拡張されたイタリアのローカリゼーション : 受取手形の受取拒否の対応](/dynamics365-release-plan/2020wave1/dynamics365-finance/extended-italian-localization-protest-handling-bills-exchange)

### <a name="additional-enhancements"></a>追加の機能強化

#### <a name="add-vendor-id-and-vendor-name-to-the-posted-projects-list-page"></a>仕入先 ID と仕入先名を転記済プロジェクトのリスト ページに追加します
この機能を有効にすると、プロジェクト関連の発注書の経費について **転記されたプロジェクト リストページ** に仕入先 ID と仕入先名が表示されます。

#### <a name="enable-default-accounting-setup-for-project"></a>プロジェクトの既定の会計設定の有効化
この機能を使用すると、既定の会計設定データを表示、編集できます。 このデータには、プロジェクト リスト ページまたは プロジェクト契約 リストページの既定の財務分析コードと売上税グループが含まれます。 有効にすると、**すべてのプロジェクト リスト ページ** の **プロジェクト** タブに **既定の会計を表示する表示** メニューが表示されます。 このメニューは、**プロジェクト契約 リストページ** の **プロジェクト契約** タブにも表示されます。 **既定の会計を表示する** をクリックすると、情報ボックスが開き、特定の会計設定情報を表示、管理できます。 この機能を使うと、詳細ページを開いてアクションを完了させる代わりに、リスト ページからアクションを完了させることができます。
 
## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム
Dynamics 365 Finance 10.0.10 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.10 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=424137&dbType=3&qc=bf63d49dcc96e51eb42ac1dd66c6c5e5d7548f1e176f729e324ea3353b9860cb) を参照してください。

### <a name="regulatory-updates"></a>規制の更新
Dynamics 365 財務と運用アプリの規制の更新については、[規制の更新](../localizations/regulatory-updates.md) を参照してください。 規制の更新を調べるもう 1 つの方法は、LCS にログインして、問題検索ツールを使用して予定されている規制更新を表示することです。 問題検索では、国、機能の種類、およびリリースを使用して検索を実行できます。 

### <a name="dynamics-365-2020-release-wave-1-plan"></a>Dynamics 365: 2020 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2020 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2020wave1/index) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Finance の削除済みまたは推奨されない機能](removed-deprecated-features-finance.md) のトピックでは、Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
