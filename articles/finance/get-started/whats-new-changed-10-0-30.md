---
title: Dynamics 365 Finance 10.0.30 (2022 年 11 月) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Finance バージョン 10.0.30 プレビュー リリースの新機能または変更された機能について説明します。
author: kfend
ms.date: 09/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f30c9896b5711adaeeccef31b0d4db87a0807c43
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405525"
---
# <a name="whats-new-or-changed-in-dynamics-365-finance-10030-november-2022"></a>Dynamics 365 Finance 10.0.30 (2022 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Finance バージョン 10.0.30 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 10.0.1362 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 9 月
- **リリースの一般提供 (手動更新):** 2022 年 10 月
- **リリースの一般提供 (自動更新):** 2022 年 11 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|----|----|----|----|
| 売掛金管理 | 自由書式の請求書転記における合計計算の改善 | パフォーマンスの向上が自由形式の請求書転記に追加され、より効率的に実行できます。 この拡張機能では、転記プロセス中に合計を複数回再計算するのではなく、計算された合計を保存します。 したがって、転記プロセスは短くなります。 | 機能管理 |
| 一般会計 | 元伝票会計フレームワークの強化されたパフォーマンス | パフォーマンスの向上が元伝票のバッチ転記に追加され、より効率的に実行できます。 この機能は、最初は自由形式請求書のバッチ転記にのみ影響します。 ただし、元伝票は将来のリリースでサポートされる予定です。 この機能を有効にすると、バッチの転記が小さな作業単位に分割され、システムが無効になるのを防ぎ、データベースの接続切断が原因で発生する問題が減らされます。 | 機能管理 |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) には記載されません。

| 機能領域 | フィーチャー名 | 詳細 |
|--------------|--------------|------------------|
| 与信および回収 | [すべての顧客] ページに [呼称] フィールドを表示します | この機能を使用すると、**一般** クイック タブのすべてのフィールドを **表示フィールドを増やす** ボタンを選択せずに表示できます。 **呼称** および **ふりがな** フィールド は常に表示されます。 これで、これらのフィールドを **全顧客リスト** ビュー ページに追加し、リスト ビューに残すことができるようになりました。 |
| グローバリゼーション | (ER) Excel ドキュメントに画像を埋め込む | [電子レポーティング (ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) 構成では、カスタム拡大縮小とカスタム縦横比を持つ埋め込み画像を含む Excel テンプレートに基づいて、Excel 形式でビジネス ドキュメントを生成するように設計できます。 実行時に、この画像は、生成されるビジネス ドキュメントの画像のプレースホルダーとして使用されます。 この改善により、生成されるドキュメント に追加された実行時に使用される画像の実際の拡大縮小と縦横比を[考慮](../../fin-ops-core/dev-itpro/analytics/er-fillable-excel.md#cell-component)することができます。 |
| グローバリゼーション | (ER) 構成された ER コンポーネントの調査 | すべての構成済み ER 形式 と モデル マッピング コンポーネントは、設計時に [検証](../../fin-ops-core/dev-itpro/analytics/er-components-inspections.md) できます。 この検証では、発生する可能性のある実行時の問題を防ぐために、整合性チェックが実行されます。 この改善により、アプリケーション コードで古い形式としてマークされ、評価された ER コンポーネントで参照されているアプリケーション コンポーネント (テーブル、クラス、メソッドなど) を検出できます。 この情報を使用すると、評価される ER コンポーネントの設計を変更し、アプリケーション コードからこれらのコンポーネントが削除される前に古いコンポーネントへの参照を削除することができます。 これにより、実行時の問題を防ぐのに役立ちます。 |
| グローバリゼーション | (ER) フォーミュラ デザイナー | ER フォーミュラ [エディタ](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting-formula-designer.md)を 使用すると、データバインドの説明、プロセス フローの制御、データ形式の指定、さまざまなデータ ソースを使用したその他のタスクの実行を実行できます。 このエディターは[相対パス](../../fin-ops-core/dev-itpro/analytics/er-formula-language.md#relative-path)を 使用して、構造化されたデータ ソースの任意の式の場所を記述します。 この改善により、すべての使用可能なデータ ソースの中から、データ ソース ウィンドウ内の編集可能な式を 1 回のクリックで明らかにできます。 したがって、編集可能な式の基本要素をすばやく視覚化し、その兄弟要素を観察し、必要に応じて式でこのすべての情報を使用することができます。 |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Finance 10.0.30 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.30 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) を参照してください。

### <a name="regulatory-updates"></a>規制の更新

財務と運用アプリの規制の更新については、[規制の更新](../localizations/regulatory-updates.md) を参照してください。 規制の更新を調べるもう 1 つの方法は、LCS にログインして、問題検索ツールを使用して予定されている規制更新を表示することです。 問題検索では、国、機能の種類、およびリリースを使用して検索を実行できます。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界のクラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界のクラウド: 2022 年リリース ウェーブ 2 プラン](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-finance)をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際にそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md)の記事では、Dynamics 365 Finance の削除または非推奨の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
