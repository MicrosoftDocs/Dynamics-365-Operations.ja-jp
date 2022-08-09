---
title: Finance and Operations バージョン 10.0.2 (2019 年 5 月) の新機能および変更点
description: この記事では、Dynamics 365 財務と運用バージョン 10.0.2 の新機能または変更された機能について説明します。 このバージョンは 5 月にリリースされます。
author: tonyafehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: a362a31d-44df-45c5-b698-64c5264c592e
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: e94b3ffadbcf5fb41b71f670559f7ed9ccb0a863
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124896"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-1002-may-2019"></a>Finance and Operations バージョン 10.0.2 (2019 年 5 月) の新機能および変更点

[!include [banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 財務と運用バージョン 10.0.2 の新機能または変更された機能について説明します。 このバージョンは 5 月にリリースされ、ビルド番号は 10.0.80 です。 バージョン 10.0.2 の詳細については [追加リソース](whats-new-changed-10-0-2.md#additional-resources) を参照してください。


Retail の最新のリリースの新機能と変更については、[Dynamics 365 for Retail バージョン 10.0.2 の新機能と変更](../../../commerce/get-started/whats-new-10-0-2.md) を参照してください。

  
## <a name="recovering-vendor-invoices-that-are-in-use"></a>使用中の仕入先請求書を回復します。

**仕入先請求書を回復** ページを使用して、4 時間以上使用されている仕入先請求書を回復またはリリースし、編集可能にします。 このページは、**定期処理タスク** ナビゲーション リンクまたは、**仕入先請求書の入力** ワークスペースのタイルから開くことができます。 請求書が復旧した後、**仕入先請求書** ページで編集可能になります。

詳細については [仕入先請求書の概要](../../../finance/accounts-payable/vendor-invoices-overview.md) を参照してください。
  
## <a name="bank-foreign-currency-revaluation"></a>銀行の外貨再評価

期間終了の一環として、いくつかの会計の慣行では、外貨建ての銀行口座残高は異なる為替レートの種類 (現在、過去、平均など) を使用して再評価が必要です。 銀行の外貨再評価の機能を使用して、ひとつ以上の銀行口座を再評価できます。 これはグローバルな機能でもあり、単一のページからアクセスできるすべての法人に対して銀行を再評価できます。
  
## <a name="create-project-based-sales-orders-for-projects-with-a-funding-source-of-type-grant"></a>交付タイプの資金調達ソースのプロジェクトに対して、プロジェクト ベースの販売注文を作成します。

この機能は、関連プロジェクト契約の交付によって出資される時間/実費払いプロジェクトのプロジェクト ベースの、販売注文の作成をサポートします。 交付の連絡先として割り当てられている顧客は、販売注文の顧客です。

## <a name="support-for-project-based-sales-orders-for-projects-with-multiple-funding-sources"></a>複数の資金調達ソースを持つプロジェクトに対するプロジェクト ベースの販売注文のサポート

この機能を使用すると、関連するプロジェクト契約に複数の資金調達ソースがある場合に、時間/実費払いプロジェクトの販売注文を作成できます。 **プロジェクト管理および会計パラメーター** ページの **一般** タブで **複数の資金調達ソースがあるプロジェクトの販売注文を許可する** オプションを選択して、この機能を有効にします。 このパラメータは削除され、今後のリリースでこの機能は常に有効になる予定です。 詳細については、[財務と運用の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) を参照してください。

## <a name="acceptance-test-library"></a>承認テストのライブラリ

この開発者向け機能を使用すると、販売注文、顧客、品目などの何百ものエンティティを含む豊富なドメイン固有言語を使用して、単体テストおよびコンポーネント テストを効率的に作成できます。 詳細については [承認テスト ライブラリのリソース](../../dev-itpro/perf-test/acceptance-test-library.md) を参照してください。  

## <a name="regulatory-updates"></a>規制の更新
Finance and Operations の規制の更新については、[ローカライズおよび規制機能 – 規制の更新](../../../finance/localizations/regulatory-updates.md) を参照してください。 また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。

## <a name="extensibility-enhancements"></a>拡張性の強化

このFinance and Operations のリリースでは、拡張性をサポートするために多くの機能拡張が行われています。 たとえば、列挙体、メタデータ、メソッドに拡張性の機能拡張が行われています。 詳しくは、[Dynamics 365 財務と運用バージョン 10.0.2 の拡張機能の変更](../../dev-itpro/extensibility/extensibility-changes-10-2.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
Finance and Operations 10.0.2 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=313841&dbType=3&qc=a4ba239cdec6f528657f529750b68845b75580e5fdb0ad6060c4bc33f8da67f8)を参照してください。

### <a name="platform-update-26"></a>プラットフォーム update 26

プラットフォーム更新プログラム 26 を含む Microsoft Dynamics 365 財務と運用バージョン10.0.2。 プラットフォーム更新プロフラム 26 の詳細ついては、[Dynamics 365 財務と運用プラットフォーム更新プログラム 26 の新機能や変更 (2019 年 5 月)](whats-new-platform-update-26.md) を参照してください。


### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[財務と運用の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) の記事では、Dynamics 365 Finance の削除済みまたは非推奨の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に[財務と運用の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

