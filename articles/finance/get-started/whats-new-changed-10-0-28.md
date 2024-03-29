---
title: Dynamics 365 Finance 10.0.28 (2022 年 8 月) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Finance バージョン 10.0.28 プレビュー リリースの新機能または変更された機能について説明します。
author: kfend
ms.date: 05/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 13dc259b641e435fcf43a0e40aa5479cb825e47d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070618"
---
# <a name="whats-new-or-changed-in-dynamics-365-finance-10028-august-2022"></a>Dynamics 365 Finance 10.0.28 (2022 年 8 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Finance バージョン 10.0.28 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 10.0.1264 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 5 月
- **リリースの一般提供 (手動更新):** 2022 年 7 月
- **リリースの一般提供 (自動更新):** 2022 年 7 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|----|----|----|----|
| 買掛金 | 発注書の前払機能を有効にする | **顧客\仕入先決済トランザクションの仕訳** 機能を使用しているかどうかに関係なく、前払請求書機能を使用できます。 前払請求書機能を使用するには、**買掛金勘定パラメーター** \> **元帳と消費税** に移動し、**前払請求書** クイックタブで、**前払請求書** オプションを **はい** に設定します。 | パラメーター |
| 予算管理 | 予算管理ドキュメント フィルター処理の強化 | この機能により、予算管理に含まれる各ドキュメントにクエリ ベースのフィルター オプションを提供され、予算チェックする予算管理ドキュメントを指定できます。 したがって、ドキュメント タイプのサブセットのみをチェックするように指定できます (たとえば、**プール** フィールドが **01** に設定されている発注書のみ)。 | 機能管理 |
| 固定資産 (ロシア) | 減価償却の開始日と終了日 | **減価償却開始日** フィールドで、**処理の開始日** を選択できます。 次に、システムは、資産が運用開始された日から減価償却の計算を開始し、処分日に減価償却を完了します。 | パラメーター |
| 一般会計 | 元帳決済内のすべての元帳トランザクションのマークの解除 | 決済できない元帳トランザクションは、トランザクションが決済されたとシステムが判断するため、元帳決済のマークが付けられることがあります。 この問題を回避するには、システム内のすべてのユーザーおよび法人の、すべての元帳トランザクションのマークを解除します。 この機能を有効にすると、**すべてのトランザクションのマークを解除** という名前の新しいボタンが **元帳決済** ページに追加されます。 このボタンを選択し、システム内のすべてのユーザーおよび法人の、すべての元帳トランザクションのマークを解除します。 このボタンは管理者だけが使用できます。 | 既定 |
| 一般会計 | 試算表に主勘定カテゴリを表示するオプション | この機能を使用すると、**試算表** リスト ページで主勘定カテゴリを列として追加できます。 試算表の **表示する列** ボタンの下のメニューに **主勘定カテゴリの表示** オプションが追加されました。 | 既定 |
| 税額の計算 | 一般仕訳帳との統合 | [財務と運用アプリとの税計算の統合](../localizations/global-tax-calcuation-service-overview.md) | パラメーター |
| 税額の計算 | 仕入先請求仕訳帳との統合 | [財務と運用アプリとの税計算の統合](../localizations/global-tax-calcuation-service-overview.md) | パラメーター |
| グローバリゼーション | (ER) 派生形式の親データ モデルのラベルを使用する | このモデルから派生した形式の親[電子レポート (ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) データ モデルのラベルを使用することができます。 **優位 ER データ モデルのラベルへの拡張アクセス** 機能を有効にすると、その形式を別の形式から派生した場合に選択式の ER データ モデルのラベルにアクセスし、このプロセス中で代替データ モデルを選択することもできます。 詳細については、[ライフサイクル](../../fin-ops-core/dev-itpro/analytics/er-design-multilingual-reports.md#lifecycle)を参照してください。 | 機能管理 |
| グローバリゼーション | (ER) 生成された ER ドキュメントに言語を指定する | ファイルとして受信された生成済みのドキュメントに優先言語を指定することができます。 既定では、生成されたファイルの名前を生成するように設計されている式では、この言語は無視されます。 **'言語の基本設定' パラメーターを 'ファイル名' 式に適用する** 機能を有効にすると、生成されたドキュメントに対して指定した優先言語に応じ、この式を作成することができます。 詳細については、[形式](../../fin-ops-core/dev-itpro/analytics/er-design-multilingual-reports.md#format)を参照してください。 | 機能管理 |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) には記載されません。

| 機能領域 | 機能名 | 詳細 |
|--------------|--------------|------------------|
| 与信および回収 | 支払いが手動で決済されるときに回収状態を更新 | この機能拡張により、支払いが支払い仕訳帳の外部で手動で決済された場合に、回収状態が更新されます。 以前は、請求書が顧客支払仕訳帳で決済されている場合にのみ回収状態が更新されました。 支払を手動で決済すると、回収状態が適切な状態に更新されます。 |
| グローバリゼーション | (ER) Excel テンプレートを再適用して ER 形式を変更する | ER により、更新された Excel テンプレートを ER 形式に[再適用](../../fin-ops-core/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md)することができます。 更新されたテンプレートに準拠できるように、ER 形式が更新されます。 最初は、更新したヘッダーとフッターのあるテンプレートを再適用しても、ER 形式は更新されません。 リリースされた機能の改善により、更新したヘッダーとフッターを含むテンプレートを再適用すると、ER 形式を更新することができます。 詳細については、[テンプレートの更新](../../fin-ops-core/dev-itpro/analytics/er-fillable-excel.md#update-a-template)を参照してください。 |
| グローバリゼーション | (ER) 構成された ER の出力先が実行時に適用できるかどうかをデザイン時にユーザーに通知する | 選択した ER 形式の [ER 送信先](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-destinations.md)を構成することができます。 構成済み ER の出力先の適用性は、形式のバージョン管理と ER ユーザー パラメーターによって[異なります](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-destinations.md#applicability)。 したがって、構成された ER の出力先が実行時に使用されるかどうかを設計時に予測することはできません。 リリースされた機能の改善により、ER のユーザー パラメーターと選択した形式のバージョン管理が分析され、構成された ER の出力先が実行時に適用できない場合に警告します。 この改善により、問題を修正して、構成された ER の出力先を実行時に適用できるようにする 2 つのオプションも提供されます。 |
| グローバリゼーション | (ER) アプリケーション テーブルのレコードをフェッチする | *テーブル レコード* タイプの ER データ ソースを使用して、アプリケーション テーブル、エンティティ、ビューなどからレコードをフェッチすることができます。 既定では、指定したテーブルのすべてのフィールドは、実行時にフェッチされます。 実行パフォーマンスを改善し、メモリ消費を最適化するために、データ ソース設定を変更して、フェッチされるフィールドの数を減らすることができます。 詳細については、[I実行時にフェッチされたテーブル フィール尾の数を削減することで ER ソリューションのパフォーマンスを改善する](../../fin-ops-core/dev-itpro/analytics/er-reduce-fetched-fields-number.md)をご覧ください。 |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Finance 10.0.28 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.28 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) を参照してください。

### <a name="regulatory-updates"></a>規制の更新

財務と運用アプリの規制の更新については、[規制の更新](../localizations/regulatory-updates.md) を参照してください。 規制の更新を調べるもう 1 つの方法は、LCS にログインして、問題検索ツールを使用して予定されている規制更新を表示することです。 問題検索では、国、機能の種類、およびリリースを使用して検索を実行できます。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界のクラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界のクラウド: 2022 年リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-finance)をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際にそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md)の記事では、Dynamics 365 Finance の削除または非推奨の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

