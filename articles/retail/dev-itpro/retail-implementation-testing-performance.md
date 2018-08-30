---
title: "テストおよびパフォーマンスの問題"
description: "このトピックでは、Microsoft Dynamics 365 for Retail 実装プロジェクトのテスト、およびパフォーマンスの推奨事項について説明します。"
author: Andreash1
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: andreash
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: Retail 7.3
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 1208d888bb19f1d298a37c10e9c34bde4580f88d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---


# <a name="testing-and-performance-issues"></a>テストおよびパフォーマンスの問題

このドキュメントでは、機能テスト、パフォーマンス テスト、およびパフォーマンスのトラブルシューティングに関連するプラクティスとツールについて説明します。

## <a name="user-acceptance-testing"></a>ユーザー受け入れテスト

ユーザー受け入れテスト (UAT) の主な目的は、特定のビジネス シナリオが期待どおりに動作するかを確認することです。 テストはカスタマイズだけでなく、最初から用意されている Microsoft の機能と、non-happy-path テストを含める必要があります。 実稼働環境に移動する前に正しく動作しないものは、すべてキャッチすることが目標です。

最良の結果を得るには、UAT 環境が、開発環境 (階層 1) ではなく、階層 2 〜階層 5 環境である必要があります。

開発環境が使用される場合、開発者がエラーを引き起こす可能性がある同じ環境を使用するシナリオがあります (例えば、未確定のソース変更またはデバッガーの添付エラーなど)。 Microsoft Internet Information Services (IIS) Express と IIS の間のスイッチは、問題を引き起こす可能性もあります。 さらに、開発マシンの何が起こったかを正確に知る方法がないため、レベル 1 環境での Microsoft のサポートは非常に限られたものとなります。

UAT (たとえば、「ドライ ラン」の準備) で使用できる運用環境。 ただし、何らかの理由でデータベースへのアクセスを必要とする場合は、配置サポート エンジニア (DSE) サービスの要求を通す必要があります。 したがって、この方法は効率的ではない場合があります。 さらに、実稼動環境は、計画された稼動日以前には、長期間使用することはできません。

UAT は、正式にビルド展開可能なパッケージを配置した後に、実行してください。 Microsoft Visual Studio で手動でビルドされたパッケージでは実行できません。 理由として、どのコード変更が手動でビルドされたパッケージに含まれていたかを証明する手段が無いからです。 公式のビルド システムだけが、特定のビルド内にある正確な変更の保証と監査証跡を提供します。

Retail Modern POS/クラウド POS を使用する場合は、正しいユーザー ロールを使用することを確認してください。 マネージャー、およびより低い権限を持つレジ担当者としてログインすることにより、テストする必要があります。

## <a name="performance"></a>パフォーマンス
### <a name="channel-performance"></a>チャネルの実績

場合によっては、チャネルのパフォーマンスが期待したほど良くないことがあります。 パフォーマンスの低下は、多くの場合次の要因によって発生します。 このリストは、影響の高い順に並べられています。

- Retail サーバーへの追加カスタム呼び出し。 追加の Retail サーバーの呼び出しを使用して製品を拡張すると、多くの場合パフォーマンスが大幅に低下します。 追加処理の可能性だけでなく、ネットワーク待機時間も考慮する必要があります。 Retail サーバーの追加の呼び出しを回避することをお勧めします。 多くの場合、拡張機能のプロパティを使用して、既存の Commerce Runtime (CRT) のハンドラーやトリガーの拡張によって、同じタスクを実行できます。
- 追加のチャネル データベース拡張機能。 カスタム SQL が効率的で、正しいインデックスを使用していることを確認してください。
- 同じカスタムまたは組み込みの CRT SQL クエリを複数回実行します。 この方法ではコストがかかりすぎる場合は、CRT 要求ハンドラーでキャッシュを適切に適用することができます。

詳細については、[IT プロおよび開発者向けの Microsoft Dynamics 365 for Retail](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page) トピックを参照してください。

店舗のパフォーマンスを調査するときは、[小売チャンネル実績調査](https://dynamicsnotes.com/retail-channel-performance-investigations/)にある提案に従ってください。

### <a name="using-telemetry-data-to-find-performance-issues"></a>テレメトリ データを使用してパフォーマンスの問題を検索する
Microsoft Dynamics 365 for Retail および Microsoft Dynamics 365 for Finance and Operations (特に低速の SQL クエリまたは SQL デッドロック)、でパフォーマンスのトラブルシューティングを行う必要がある場合には Microsoft Dynamics Lifecycle Services (LCS) の環境の診断のページで、重要なテレメトリ データを表示します。 このデータを使用して、コード、構成、またはデザインの潜在的なパフォーマンスの問題を見つけることができます。 詳細については、[環境監視未加工ログの使用方法](https://blogs.msdn.microsoft.com/axsa/2018/06/05/how-to-use-environment-monitoring-view-raw-logs/)を参照してください。 その情報により、いくつかのバッチ処理またはフォームの読み込みが遅い理由が明らかになります。

### <a name="performance-testing"></a>パフォーマンス テスト

通常、システムのパフォーマンスをテストするときは、多くの共有リソースが競合するコンポーネントに焦点を絞る必要があります。 これらのリソースは、さまざまなプロジェクト、顧客、または要件ごとに異なる場合があります。

ボトルネックが発生するいくつかの理由は以下の通りです。

- Finance and Operations でのリソース集中型の計算は、明細書の転記、チャネル データ同期の計算変更など、大規模な製品品揃えを含む倉庫管理の操作、および MRP (Material Requirements Planning) の実行
- いくつかの Retail サーバー (クラウド内または Retail Store Scale Unit のいずれか) で実行する、複数の端末またはストア用の複雑な小売ビジネス ロジック
- 統合されたサード パーティ システム (Finance and Operations または Retail サーバーのいずれかから統合)
- Retail サーバーから頻繁に呼び出されるリアル タイム トランザクション サービス。
- 非標準または拡張された標準機能 (たとえば、カスタム WHS コードを使用する拡張明細書転記)

一般的に、既定および非リアルタイム POS 操作は、専用のリソース (POS がインストールまたは実行されているコンピューター) を持っているため、ボトルネックとはみなされません。 パフォーマンスの問題は、通常、ビジネス ロジックまたは Retail サーバーへの「Chatty」呼び出しによって発生します。

パフォーマンス テストはこのトピックで前述した情報を使用して、既にいくつかの初期最適化を完了した後に行う方が理想的です。 単一のユーザーまたはプロセスでシステムが正常に動作しない場合、同時ユーザーまたはプロセスでは正常に動作しません。 詳細については、[Retail Channel Performance](https://dynamicsnotes.com/retail-channel-performance-investigations/) を参照してください。 さらに、Finance and Operations ドキュメントで、「PerfSdk」または「Trace parser」を検索します。

すべてのプロジェクトは異なっているため、実行する必要のある正確なパフォーマンス テストについての一般的な回答は困難です。 たとえば、トランザクションの販売明細行が少ない (すべての店舗で 1 日あたり 10 万未満) 場合、および明細書転記にカスタム拡張コードが追加されていない場合は、転記にパフォーマンス テストを行う必要はありません。 ただし、販売明細行が大幅に高い場合、または主要なカスタム変更が加えられた場合は、パフォーマンス テストを転記することをお勧めします。

通常、すべての環境でハードウェア機能は異なります。 ただし、コードおよびデータが類似している場合、通常他の環境でもパフォーマンスの問題は起こり得ます。 パフォーマンス テストに実稼働環境を使用することをお勧めしません。 開発、テスト、および運用環境で同じデータを使用することをお勧めします。 開発環境は、修正プログラムの作成と検証に使用されます。 多数のパフォーマンス クリティカル コード パスはデータ依存のため、 Contoso サンプル データベースでは同じ問題が発生しないことがあります。

パフォーマンスの修正を完了した後は、テスト環境で修正プログラムを確認してください。 公式に構築されたパッケージをテスト環境に展開し、問題が解決した場合は、パッケージをリリース パッケージとしてマークします。 

さらにパフォーマンスの問題を大きく修正するには、新しいパフォーマンステストを行う必要があります。 多くの場合、大きな問題は、他のより小さな問題をマスクします。 上記の問題が解決された後、次の問題を検出し、パフォーマンスが顧客の期待に達するまで処理されます。

## <a name="additional-resources"></a>その他のリソース
[新しい環境、Visual Studio Team Services、および小売プロジェクトの分岐を設定します。](./new-environments-visual-studio-teams-branch-retail-projects.md)

[コードおよび小売プロジェクトの環境の更新](./updating-environments.md)

