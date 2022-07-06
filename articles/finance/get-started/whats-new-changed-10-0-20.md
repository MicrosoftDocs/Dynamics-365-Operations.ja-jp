---
title: Dynamics 365 Finance 10.0.20 (2021 年 8 月) の新機能および変更された機能
description: この記事では、Dynamics 365 Finance バージョン 10.0.20 プレビュー リリースの新機能または変更された機能について説明します。
author: kfend
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: dd30fc1d68232084b2fc8c55ff62edbd0c8be3b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855386"
---
# <a name="preview-features-in-dynamics-365-finance-10020-august-2021"></a>Dynamics 365 Finance 10.0.20 (2021 年 8 月) のプレビュー機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Finance バージョン 10.0.20 の新機能または変更された機能について説明します。 このバージョンには 10.0.886 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 5 月
- **リリースの一般提供 (手動更新):** 2021 年 7 月
- **リリースの一般提供 (自動更新):** 2021 年 7 月


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365/release-plans/) を参照してください。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |
|----|----|----|
| 財務分析情報 | [顧客支払予測](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/customer-payment-predictions) | [顧客支払予測](../finance-insights/payment-insights-overview.md) |
| 財務分析情報 | [キャッシュ フロー予測の外部データ](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/external-data-cash-forecasting) | [キャッシュ フロー予測に外部データを使用する](../finance-insights/external-data-in-cash-flow.md) |
| 財務分析情報 | [予測銀行残高](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/forecast-bank-balance) | [キャッシュ フロー予測](../finance-insights/cash-flow-forecast-intro.md) |
| 財務分析情報 | [インテリジェントな予算案](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/intelligent-budget-proposal) | [予算案](../finance-insights/budget-proposals.md) |
| Finance Insights | [会計登録者ワークスペース](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/treasurer-workspace) | [現金持高](../finance-insights/cash-position.md) |

> [!Note]
> **機能管理** ワークスペースで Finance Insights を有効にする前に、Lifecycle Services (LCS) から Finance Insights アドインをインストールする必要があります。 

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。 これらの機能を使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で明示的にそれらを有効にする必要があります。

| 機能領域 | 機能 &nbsp; 名 &nbsp; 機能 &nbsp; 管理 | 詳細 |
|---|---|---|
| 原価管理 | 在庫決算の取り消しに対してユーザー定義のバッチ番号設定を有効にする|在庫決算の取り消しを実行すると、影響を受ける各品目に対してバッチ ジョブが作成され、品目が多すぎるとバッチ サーバーが調整される可能性があります。 この機能により、現在在庫決算の取り消しで使用されている 「追加のバッチ ヘルパー」 を使用するプロセスを有効にします。 環境を考慮してパフォーマンスを最適化するために設定を調整できます。 |
| 一般会計 | 現金持高の照会のフィルター処理の強化 | この機能により、現金持高の照会に対する財務分析コードのフィルター処理が強化されます。 有効にした場合、入力されたすべての区分基準に一致するレコードだけが照会で返されます。 有効にしない場合は、入力した任意の区分基準に一致するレコードが返されます。  |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム
Dynamics 365 Finance 10.0.20 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.20 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md) を参照してください。 

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にログインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8) を参照してください。

### <a name="regulatory-updates"></a>規制の更新
財務と運用アプリの規制の更新については、[規制の更新](../localizations/regulatory-updates.md) を参照してください。 規制の更新を調べるもう 1 つの方法は、LCS にログインして、問題検索ツールを使用して予定されている規制更新を表示することです。 問題検索では、国、機能の種類、およびリリースを使用して検索を実行できます。 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2021wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md)の記事では、Dynamics 365 Finance の削除または非推奨の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
