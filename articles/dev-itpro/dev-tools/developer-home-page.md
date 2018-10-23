---
title: "開発およびカスタマイズ"
description: "このトピックでは、開発に関するトピックへのリンクを提供します。"
author: RobinARH
manager: AnnBe
ms.date: 04/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21631
ms.assetid: 06e26767-6056-4755-b47e-0bda71833581
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 84ae968e4f0e309c6cb841c4d63ee92c7676bfab
ms.openlocfilehash: 0de1e48aa9fbabdcd711aabded726066f9e341b1
ms.contentlocale: ja-jp
ms.lasthandoff: 10/05/2018

---

# <a name="develop-and-customize"></a>開発およびカスタマイズ 

[!include [banner](../includes/banner.md)]

このトピックでは、開発に関するトピックへのリンクを提供します。

## <a name="overview"></a>概要

Microsoft Dynamics 365 for Finance and Operations は、Microsoft から提供されている次世代エンタープライズ リソース プランニング (ERP) を表します。 これは、パブリック クラウドとプライベート クラウド両方のクラウド ベースのソリューションおよびオンプレミスとして、全体の ERP アプリケーション スイートを有効にするために設計されています。 これは、Microsoft からの最新テクノロジーで構築時に、クラウドでの操作の速度、わかりやすさ、およびコスト効率性を利用します。 このリリースでは、開発環境が大幅に変更されています。 これらの変更の内容は以下の通りです。

- 実行環境から切り離された開発ツール。 オンライン データベースではなく、ローカルの XML ベースのファイルに対して作成します。
- Microsoft Visual Studio は開発環境です。 Visual Studio 環境は、円滑で慣れ親しんだエクスペリエンスを提供するようにカスタマイズされています。
- X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。 CIL は C\# プログラミング言語などの他の .NET ベース (マネージド) の言語で使用されるものと同じ中間言語です。
- ブラウザー ベースのクライアントおよびフォームのデザイン パターンを活用して、改善されたエンド ユーザー エクスペリエンスを提供することができます。
- Application Lifecycle Model (ALM) は、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。

## <a name="architecture"></a>アーキテクチャ
-   [アプリケーション スタックおよびサーバーのアーキテクチャ](application-stack-server-architecture.md)

## <a name="getting-started"></a>はじめに
-   [ベータ評価版の入手](get-evaluation-copy.md)
-   [LCS101 – サブスクリプションのサインアップ](sign-up-preview-subscription.md)
-   [開発インスタンスにアクセス](../dev-tools/access-instances.md)
-   [開発システム要件](development-system-requirements.md)
-   [削除予定の機能](../migration-upgrade/deprecated-features.md)
-   [非推奨 API's](../migration-upgrade/deprecated-apis.md)
-   [Azure DevOps の名前を変更し、コンピューターを再起動する](../migration-upgrade/vso-machine-renaming.md)
-   [Azure DevOps の概要 (ビデオ)](http://channel9.msdn.com/Events/Build/2014/2-575)
<!-- [Learn about packages, models and Visual Studio (Office Mix)](https://mix.office.com/watch/ies6lyit6773)-->
<!-- [Development tools performance tips (Office Mix)](https://mix.office.com/watch/rnp6ng9wu8kx)-->
<!-- [Feedback and support (Office Mix)](https://mix.office.com/watch/92azzna59jj6)-->

## <a name="fleet-management"></a>フリート管理
-   [フリート管理のサンプル](introduction-fleet-management-sample.md)
-   [INT101: フリート管理の概要](fleet-management-sample.md)

## <a name="development-tools"></a>開発ツール
### <a name="tutorials"></a>チュートリアル

-   [Visual Studio 開発の概要](introduction-visual-studio.md)
-   [簡易データモデルを作成する](create-data-model-elements.md)
-   [プロジェクトの構築およびデバッグ](build-debug-project.md)
-   [バージョン コントロール、メタデータ、検索、ナビゲーション、およびその他の機能](version-control-metadata-navigation.md)

### <a name="tools-models-and-vms"></a>ツール、モデル、VM

-   [開発ツール](development-tools-overview.md)
<!-- [Introduction to the development environment (Office Mix)](https://mix.office.com/watch/1tz7194y62m3s)-->
-   [アプリケーション エクスプローラー](application-explorer.md)
-   [プロジェクト](projects.md)
-   [要素デザイナー](element-designers.md)
-   [要素の利用状況](element-usage.md)
-   [モデル](models.md)
-   [ビルド操作](build-operations.md)
-   [Visual Studio コード エディター](code-editor.md)
-   [開発者ツールのアドイン](developer-tools-add-ins.md)
-   [モデルの配分: モデルをエクスポートおよびインポートする方法](models-export-import.md)
-   [Visual Studio でのメタデータの検索](metadata-search-visual-studio.md)
-   [Visual Studio を使用して競合を解決する](https://mix.office.com/watch/1rl75ei2cs6d7)
-   [新しいユーザー アカウントを開発 VM で開発できるようにする](enable-development-machine.md)
-   [Visual Studio 開発ツールの更新](update-development-tools.md)
-   [管理者のアクセスを許可しない仮想マシンに関するよく寄せられる質問](../sysadmin/VMs-no-admin-access.md)
<!--  [Configure version control with Azure DevOps (Office Mix)](https://mix.office.com/watch/1ftubtqzp3xxl)-->

## <a name="x-programming-language"></a>X++ プログラミング言語
### <a name="tutorials"></a>チュートリアル

-   [新しい X++ およびデバッガーの機能](new-x-debugger-features.md)
-   [C\#、X++ 相互運用性およびLINQ](write-business-logic.md)

### <a name="language-support"></a>言語サポート

-   [プログラミング言語のサポート](programming-language-support.md)
-   [要求または応答シナリオの EventHandlerResult クラス](event-handler-result-class.md)
-   [X++ コードのデバッグ](debug-xpp.md)
-   [C で使用する LINQ プロバイダー\#](linq-provider-c.md)
-   [ベスト プラクティス ルールの作成](author-best-practice-rules.md)

### <a name="reference"></a>参照

-   [X++ 言語リファレンス](../dev-ref/xpp-language-reference.md)

## <a name="customize-with-extensions-and-overlayering"></a>拡張機能およびオーバーレイによってカスタマイズする
- [拡張機能のホーム ページ](../extensibility/extensibility-home-page.md)
- [拡張機能を使用してアプリケーション スイート レポートをカスタマイズする](../analytics/customize-app-suite-reports-with-extensions.md)

## <a name="code-migration"></a>コードの移行
- [コードの移行とホーム ページのアップグレード](../migration-upgrade/code-migration-home-page.md)

## <a name="move-packages-between-environments"></a>環境間でパッケージを移動する
- [配置可能なパッケージの作成と適用](../deployment/create-apply-deployable-package.md)

## <a name="performance"></a>パフォーマンス
- [Trace Parser でトレースを実行し、分析する](../perf-test/trace-trace-tutorial.md)
- [Visual Studio Online を使用した PerfSDK およびマルチユーザー テストの概要](../perf-test/perfsdk-tutorial.md)
- [問題点の診断およびパフォーマンス問題の分析にTrace Parser のデスクトップ バージョンを使用する](../perf-test/trace-parser.md)
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
- [分析](../analytics/analytics.md)

## <a name="reporting-services"></a>Reporting Services
- [電子申告の概要](../analytics/general-electronic-reporting.md)
<!-- [Introduction to Advanced Reporting Solutions (Office Mix)](https://mix.office.com/watch/wdl1dquy2tve)
- [Demo of Advanced Reporting Solutions (Office Mix)](https://mix.office.com/watch/1hkvtnc8sc7l6)-->

## <a name="data-entities-and-odata"></a>データ エンティティおよび OData
- [データ エンティティのホーム ページ](../data-entities/data-entities.md)
- [OData](../data-entities/odata.md)

## <a name="testing-support-in-visual-studio"></a>Visual Studio でのテストのサポート
- [テストと検証](../perf-test/testing-validation.md)
- [Visual Studio でのテストのサポート](../perf-test/testing-support.md)
- [継続的なビルドとテストの自動化による開発者トポロジの配置](../perf-test/continuous-build-test-automation.md)
- [タスク レコーダー](../user-interface/task-recorder.md)

## <a name="office-integration"></a>Office 統合
- [Office 統合](../office-integration/office-integration.md)

## <a name="intelligence"></a>インテリジェンス
- [インテリジェンス](../analytics/bi-reporting-home-page.md)
<!-- [Overview of aggregate data (Office Mix)](https://mix.office.com/watch/16yvvnw45kzhf)-->

## <a name="mobile-platform"></a>モバイル プラットフォーム
- [モバイル プラットフォームのホーム ページ](../mobile-apps/platform/mobile-platform-home-page.md)

## <a name="global-finance-management"></a>グローバル財務管理
- [財務開発ホーム ページ](../financial/financial-dev-home-page.md)

## <a name="licensing"></a>ライセンス
- [ISV ライセンス](isv-licensing.md)

## <a name="supply-chain-management"></a>サプライ チェーン マネジメント
- [ガント作成ガイド](../user-interface/gantt-development-guide.md)
- [新しい輸送管理エンジンの作成](../../supply-chain/transportation/create-new-transportation-management-engine.md)

## <a name="additional-resources"></a>その他のリソース
[開発のための内部者向けヒント](https://community.dynamics.com/ax/b/newdynamicsax)




