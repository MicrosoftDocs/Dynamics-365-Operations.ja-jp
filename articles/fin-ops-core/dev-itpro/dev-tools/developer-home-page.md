---
title: ホームページの開発とカスタマイズ
description: このトピックでは、開発に関するトピックへのリンクを提供します。
author: RobinARH
manager: AnnBe
ms.date: 10/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.assetid: 06e26767-6056-4755-b47e-0bda71833581
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2264d919325972639ac09149cd20aa7f729b119
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811720"
---
# <a name="develop-and-customize-home-page"></a>ホームページの開発とカスタマイズ

[!include [banner](../includes/banner.md)]

このトピックでは、開発に関するトピックへのリンクを提供します。

## <a name="overview"></a>概要

Finance and Operations アプリケーションは、Microsoft から提供されている次世代エンタープライズ リソース プランニング (ERP) を表します。 これは、パブリック クラウドとプライベート クラウド両方のクラウド ベースのソリューションおよびオンプレミスとして、全体の ERP アプリケーション スイートを有効にするために設計されています。 これは、Microsoft からの最新テクノロジーで構築時に、クラウドでの操作の速度、わかりやすさ、およびコスト効率性を利用します。 このリリースでは、開発環境が大幅に変更されています。 これらの変更の内容は以下の通りです。

- 実行環境から切り離された開発ツール。 オンライン データベースではなく、ローカルの XML ベースのファイルに対して作成します。
- Microsoft Visual Studio が開発環境です。 Visual Studio 環境は、円滑で慣れ親しんだエクスペリエンスを提供するようにカスタマイズされています。
- X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。 CIL は C\# プログラミング言語などの他の .NET ベース (マネージド) の言語で使用されるものと同じ中間言語です。
- ブラウザー ベースのクライアントおよびフォームのデザイン パターンを活用して、改善されたエンド ユーザー エクスペリエンスを提供することができます。
- Application Lifecycle Model (ALM) は、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。

## <a name="architecture"></a>アーキテクチャ
-   [アプリケーション スタックおよびサーバーのアーキテクチャ](application-stack-server-architecture.md)

## <a name="getting-started"></a>はじめに
-   [ベータ評価版の入手](get-evaluation-copy.md)
-   [プレビュー サブスクリプションのサインアップ](sign-up-preview-subscription.md)
-   [開発環境の配置とアクセス](../dev-tools/access-instances.md)
-   [開発システム要件](development-system-requirements.md)
-   [削除済みまたは非推奨の機能](../migration-upgrade/deprecated-features.md)
-   [非推奨 API](../migration-upgrade/deprecated-apis.md)
-   [ローカル開発 (VHD) 環境の名前変更](../migration-upgrade/vso-machine-renaming.md)
-   [Azure DevOps の概要 (ビデオ)](https://channel9.msdn.com/Events/Build/2014/2-575)
<!-- [Learn about packages, models and Visual Studio (Office Mix)](https://mix.office.com/watch/ies6lyit6773)-->
<!-- [Development tools performance tips (Office Mix)](https://mix.office.com/watch/rnp6ng9wu8kx)-->
<!-- [Feedback and support (Office Mix)](https://mix.office.com/watch/92azzna59jj6)-->

## <a name="fleet-management"></a>フリート管理
-   [フリート管理のサンプル アプリケーション](introduction-fleet-management-sample.md)
-   [フリート管理のサンプル アプリケーションのためのエンド ツー エンドのシナリオ](fleet-management-sample.md)

## <a name="development-tools"></a>開発ツール
### <a name="tutorials"></a>チュートリアル

-   [開発ツールのチュートリアル](introduction-visual-studio.md)
-   [モデルとデータ モデル要素の作成の概要](create-data-model-elements.md)
-   [プロジェクトのビルドおよびデバッグ](build-debug-project.md)
-   [バージョン コントロール、メタデータ検索、およびナビゲーション](version-control-metadata-navigation.md)

### <a name="tools-models-and-vms"></a>ツール、モデル、VM

-   [Visual Studioの開発ツール](development-tools-overview.md)
<!-- [Introduction to the development environment (Office Mix)](https://mix.office.com/watch/1tz7194y62m3s)-->
-   [アプリケーション エクスプローラー](application-explorer.md)
-   [Visual Studioの Finance and Operations の プロジェクト タイプ](projects.md)
-   [要素デザイナー](element-designers.md)
-   [要素の使用方法を決定するためのコマンド](element-usage.md)
-   [モデルとパッケージ](models.md)
-   [ビルド操作](build-operations.md)
-   [コード エディター機能](code-editor.md)
-   [Visual Studioのツールアドイン](developer-tools-add-ins.md)
-   [モデルのエクスポートとインポート](models-export-import.md)
-   [Visual Studio でのメタデータの検索](metadata-search-visual-studio.md)
-   [開発マシンでの新しいユーザーの作成](enable-development-machine.md)
-   [ Visual Studio の開発ツールを更新する](update-development-tools.md)
-   [管理者アクセスを許可しない開発用 VM および ビルド用 VM に関するよく寄せられる質問](../sysadmin/VMs-no-admin-access.md)
<!--  [Configure version control with Azure DevOps (Office Mix)](https://mix.office.com/watch/1ftubtqzp3xxl)-->

## <a name="x-programming-language"></a>X++ プログラミング言語
### <a name="tutorials"></a>チュートリアル

-   [X++ およびデバッガーの機能](new-x-debugger-features.md)
-   [C\# と X++ ソース コードを使用してビジネス ロジックを記述する](write-business-logic.md)

### <a name="language-support"></a>言語サポート

-   [X++ と X++ コンパイラの変更](programming-language-support.md)
-   [要求または応答シナリオの EventHandlerResult クラス](event-handler-result-class.md)
-   [Visual Studioのデバッガーを使用して  X++ コードをデバッグする](debug-xpp.md)
-   C\#(linq-provider-c.md) 用の統合言語 クエリ (LINQ) プロバイダ
-   [ベスト プラクティス ルールの記述](author-best-practice-rules.md)

### <a name="reference"></a>参照

-   [X++ 言語リファレンス](../dev-ref/xpp-language-reference.md)

## <a name="customize-with-extensions-and-overlayering"></a>拡張機能およびオーバーレイによってカスタマイズする
- [拡張機能のホーム ページ](../extensibility/extensibility-home-page.md)
- [拡張機能を使用してアプリケーション スイート レポートをカスタマイズする](../analytics/customize-app-suite-reports-with-extensions.md)

## <a name="code-migration"></a>コードの移行
- [Visual Studio  での競合を解決する方法 (ビデオ)](https://youtu.be/4rxO0zUN2zU)
- [コードの移行とホーム ページのアップグレード](../migration-upgrade/code-migration-home-page.md)

## <a name="move-packages-between-environments"></a>環境間でパッケージを移動する
- [配置可能なモデル パッケージの作成](../deployment/create-apply-deployable-package.md)

## <a name="performance"></a>パフォーマンス
- [Trace Parser を使用してトレースを実行](../perf-test/trace-trace-tutorial.md)
- [Trace Parser を使用した問題点の診断およびパフォーマンスの分析](../perf-test/trace-parser.md)
- [パフォーマンス タイマー](../perf-test/performance-timer.md)
<!-- [Expanding data with the Data Expansion tool (Office Mix)](https://mix.office.com/watch/11cet1u4nmn64)
- [Analyzing performance Issues with Trace Parser (Office Mix)](https://mix.office.com/watch/17d76cll0npyw)
- [The performance timer and other tools (Office Mix)](https://mix.office.com/watch/ij5cqidra5q3)
- [Using Task Recorder to create a single user performance test (Office Mix)](https://mix.office.com/watch/qtdlasy2rcf3)
- [The performance timer and other tools (Office Mix)](https://mix.office.com/watch/ij5cqidra5q3)
- [Analyzing performance Issues with Trace Parser (Office Mix)](https://mix.office.com/watch/17d76cll0npyw)-->

## <a name="user-interface-concepts"></a>ユーザー インターフェイスのコンセプト
クライアントは、すべての主要なブラウザーで動作する HTML Web クライアントです。 ユーザー インターフェイスの開発およびカスタマイズの詳細ついては、[ユーザー インターフェイス開発ホーム ページ](../user-interface/user-interface-development-home-page.md) を参照してください。

## <a name="analytics"></a>分析
- [分析、集計の測定、および KPI モデリング](../analytics/analytics.md)

## <a name="reporting-services"></a>Reporting Services
- [電子申告 (ER) の概要](../analytics/general-electronic-reporting.md)
<!-- [Introduction to Advanced Reporting Solutions (Office Mix)](https://mix.office.com/watch/wdl1dquy2tve)
- [Demo of Advanced Reporting Solutions (Office Mix)](https://mix.office.com/watch/1hkvtnc8sc7l6)-->

## <a name="data-entities-and-odata"></a>データ エンティティおよび OData
- [データ エンティティの概要](../data-entities/data-entities.md)
- [データ プロトコル (OData) を開く](../data-entities/odata.md)

## <a name="testing-support-in-visual-studio"></a>Visual Studio でのテストのサポート
- [テストと検証](../perf-test/testing-validation.md)
- [Visual Studio のプロジェクトをテストする](../perf-test/testing-support.md)
- [継続的ビルドとテストの自動化を使用した開発者トポロジの展開](../perf-test/continuous-build-test-automation.md)
- [タスク レコーダー リソース](../user-interface/task-recorder.md)

## <a name="office-integration"></a>Office 統合
- [Office 統合の概要](../office-integration/office-integration.md)

## <a name="intelligence"></a>インテリジェンス
- [ビジネス インテリジェンス (BI) およびレポート作成のホーム ページ](../analytics/bi-reporting-home-page.md)
<!-- [Overview of aggregate data (Office Mix)](https://mix.office.com/watch/16yvvnw45kzhf)-->

## <a name="mobile-platform"></a>モバイル プラットフォーム
- [モバイル プラットフォームのリソース](../mobile-apps/platform/mobile-platform-home-page.md)

## <a name="global-finance-management"></a>グローバル財務管理
- [財務開発のホーム ページ](../financial/financial-dev-home-page.md)

## <a name="licensing"></a>ライセンス
- [独立系ソフトウェア ベンダー (ISV) ライセンス](isv-licensing.md)

## <a name="supply-chain-management"></a>サプライ チェーン マネジメント
- [ガント コントロール作成ガイド](../user-interface/gantt-development-guide.md)
- [新しい輸送管理エンジンの作成](../../../supply-chain/transportation/create-new-transportation-management-engine.md)

## <a name="additional-resources"></a>その他のリソース
[開発のための内部者向けヒント](https://community.dynamics.com/ax/b/newdynamicsax)



