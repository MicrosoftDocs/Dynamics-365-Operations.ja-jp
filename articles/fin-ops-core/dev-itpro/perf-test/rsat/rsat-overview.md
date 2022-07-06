---
title: Regression suite automation tool (RSAT)
description: Regression Suite Automation Tool (RSAT) により、タスク レコーダーを使用してビジネス タスクを記録し、コードを記述することなく自動テストに変換することができます。
author: FrankDahl
ms.date: 03/29/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ae8e62ad44d9c01a5d0c8696a2f9e2728f34b5e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851904"
---
# <a name="regression-suite-automation-tool-rsat"></a>Regression suite automation tool (RSAT)

[!include [banner](../../includes/banner.md)]

Regression Suite Automation Tool (RSAT) を使用すると、財務と運用アプリのユーザー受け入れテスト (UAT) の時間と費用を大幅に縮小できます。 通常、UAT は Microsoft アプリケーションの更新プログラムを取得するか、カスタム コードおよび構成を運用環境に適用する前に必要です。 RSAT により、機能パワー ユーザーはタスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくてもタスク記録を一連の自動テストに変換できます。 タスク レコーダーの詳細については、 [タスク レコーダー のリソース](../../user-interface/task-recorder.md) を参照してください。

RSATは、テストの実行、報告、および調査のために Microsoft Azure DevOps と完全に統合されています。 テスト パラメーターは、テスト ステップから切り離され、Microsoft Excel ファイルに保存されます。

この記事に加えて、以下のトピックで RSAT の使用について説明します。

+ [Regression Suite Automation Tool (RSAT) のインストールと構成](rsat-install-configure.md)
+ [Regression Suite Automation Tool (RSAT) テスト ケースの実行](rsat-run.md)
+ [Regression Suite Automation Tool (RSAT) の並列実行の実行](rsat-parallel-execution.md)
+ [Regression Suite Automation Tool (RSAT) でのテスト ケースの管理](rsat-maintain-test-cases.md)
+ [Azure DevOps を使用しないトライアル モード](rsat-trial-without-devops.md)
+ [予測値の検証](rsat-validate-expected.md)
+ [チェーン テスト ケース](rsat-chain-test-cases.md)
+ [派生テスト ケース](rsat-derived-test-cases.md)
+ [管理者以外のユーザーが RSAT を使用するように構成する](rsat-configure-nonadmin.md)
+ [パラメーター ファイルのアップグレード](rsat-upgrade-parameter-files.md)
+ [Regression Suite Automation Tool (RSAT) のベスト プラクティス](rsat-best-practices.md)
+ [Regression Suite Automation Tool (RSAT) のトラブルシューティング](rsat-troubleshooting.md)
+ [Azure DevOps パイプラインと RSAT を統合する](rsat-devops-extension.md)

## <a name="getting-started-videos"></a>使用開始のビデオ

これらのビデオでは、RSAT が紹介されており、作業を開始することができます。

### <a name="use-task-recorder-to-create-a-test-case-for-rsat"></a>タスク レコーダーを使用して RSAT のテスト ケースを作成する

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4uM5U]

[タスク レコーダーを使用して、Regression Suite Automation Tool (RSAT) のテスト ケースを作成する方法](https://youtu.be/bBr4BXAxTNI) ビデオ (上記参照) は、YouTube で入手可能な [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。

### <a name="create-a-test-plan-in-azure-devops-to-use-with-rsat"></a>Azure DevOps でテスト プランを作成し、RSAT で使用する

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4vx0I]

[Azure DevOps でテスト プランを作成し、Regression Suite Automation Tool (RSAT) で使用する方法](https://youtu.be/3jIuBleAnQk) ビデオ (上記参照) は、YouTube で入手可能な [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。

### <a name="how-to-use-rsat"></a>RSAT の使用方法

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4vl8Z]

[Regression Suite Automation Tool (RSAT) の使用方法](https://youtu.be/uhN9JItzGAk) ビデオ (上記参照) は、YouTube で入手可能な [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。

### <a name="the-improved-excel-experience-in-rsat-20"></a>RSAT 2.0 での Excel エクスペリエンスの向上

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4Gi0V]

[RSAT 2.0 での Excel エクスペリエンスの向上](https://youtu.be/fcEkSIVQ1Bg) ビデオ (上記参照) は、YouTube で試聴できる [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。

## <a name="end-to-end-flow"></a>エンド ツー エンド フロー

RSAT は、次に定義するエンド ツー エンド フローのパーツに含まれています。 RSAT、Microsoft Dynamics Lifecycle Services (LCS) および Azure DevOps は、テスト ケースの作成 (タスク レコーダーを使用)、配布、構成、実行、調査、および報告に対する一連のツールを提供します。

![作成し、構成し、実行します。](media/end-to-end.png)

このプロセスの詳細については、[ユーザー受け入れテストを作成して自動化する](../../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)を参照してください。

## <a name="lcs-bpm-and-task-recordings"></a>LCS、BPM、およびタスクの記録

LCS でビジネス プロセス モデラー (BPM) ツールを使用する必要はありません。 プロジェクトとテナント間でテスト ライブラリを管理および配布できるようにする場合、BPM が推奨されています。 これらの機能は、Microsoft パートナーおよび独立系ソフトウェア ベンダー (ISV) にとって特に便利です。 BPM では、LCS ソリューションの一部としてテスト ライブラリを配布できるようにします。

BPM を使用していない場合は、Azure DevOps で手動でテスト ケースを作成し、開発者記録ファイルを Azure DevOps テスト ケースに添付できます。 開発者記録ファイルは、タスク レコーダー ウィンドウから直接作成できます。

![開発者としてタスク レコードを保存します。](media/save-as-developer.png)

開発者記録ファイルに **Recording.xml** という名前を付けてから、Azure DevOps テスト ケースに添付する必要があります。 または、記録ファイル **-テスト ケース タイトル-.xml** という名前を付けることもできます。これは、**-テスト ケース タイトル-** はテスト ケースの DevOps タイトルになります。

![添付ファイルを追加します。](media/attachments.png)

## <a name="intended-usage-and-test-classification"></a>使用目的およびテストの分類

### <a name="business-cycle-business-process-testing"></a>ビジネス サイクル (ビジネス プロセス) のテスト

RSAT は、開発ライフサイクルの最後に通常行われるビジネス サイクル テストおよびシナリオ テスト (複数のコンポーネント テスト) で使用するためのものです。 このテストは、*ユーザー受け入れテスト* とも呼ばれます。 次の図に示すように、ビジネス サイクル テストは、コンポーネント テストまたは単体テストよりも少ないテスト ケースで構成されています。

![単体テスト、コンポーネント テスト、複数のコンポーネントテスト、ビジネス サイクル テスト。](media/business-cycle.png)

### <a name="cloud-pos"></a>クラウド POS

Finance and Operations タスク レコーダーを使用して記録されたプロセスのテストに加えて、RSAT は Dynamics 365 Commerce の Cloud POS プロセスのテストもサポートしています。 RSAT と Cloud POS の詳細については、[Cloud POS 用のレコーダーおよび Regression Suite Automation Tool のテスト](../../../../commerce/dev-itpro/pos-rsat.md) を参照してください。

### <a name="warehouse-mobile-app"></a>Warehouse mobile app

RSAT をウェアハウス アプリ タスク検証フレームワークと組み合わせて使用することにより、ウェアハウス プロセスのテストを自動化することができます。 この[技術解説](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-warehouse-app-task-validation-framework-october-23-2019)は、開始するための優れた参考資料です。

### <a name="unit-and-component-testing"></a>ユニットおよびコンポーネント テスト

単体テストの場合は、RSAT を使用しないことを推奨します。 代わりに、SysTest フレームワークとビルド / テスト自動化ツールを使用します。 コンポーネント テストでは、[受け入れテスト ライブラリ リソース](../acceptance-test-library.md) (ATL) を活用します。 ATL は、 X++ テスト ヘルパーのライブラリです。 SysTest フレームワークを使用すると、次の利点があります。

+ 一貫したテスト データを作成できます。
+ テスト コードが読みやすくなります。
+ テスト データの作成に使用されているメソッドの発見可能性が向上します。
+ 前提条件の設定の複雑さを隠します。
+ パフォーマンスの高いテスト ケースをサポートします。

詳細については、[継続的デリバリー ホーム ページ](../../dev-tools/continuous-delivery-home-page.md) を参照してください。

### <a name="data-integration-testing"></a>データ統合テスト

統合テストで RSAT を使用するのではなく、データ管理フレームワーク (DIXF として知られます) に頼ります。 [データ タスクの自動化](../../data-entities/data-task-automation.md)フレームワークを使用すると、データ統合シナリオのテストを構成したり自動化したりすることができます。

## <a name="rsat-user-interface-overview"></a>RSAT ユーザー インターフェイスの概要

RSAT 2.1 により、**クイック リンク** タブおよび DevOps のテスト スイーツとテスト実行にすばやく移動する機能を含め、アプリの主要なコンポーネントを通じたナビゲーションを簡略化する最新のユーザー インターフェイスが導入されています。

左のナビゲーション ウィンドウを使用して、テスト計画、設定、Cloud POS 設定、およびクイック リンクのページ間を移動します。

### <a name="test-plan"></a>テスト計画

**テスト計画** タブは、テスト ケースを操作し、実行するメインのタブです。

![UI テスト計画 タブ。](media/UI-test-plans-tab.png)

### <a name="settings"></a>設定

**設定** タブを選択して、RSAT の設定を構成します。 トップ バーを使用して、一般、オプション、およびプロセス設定の間を移動します。 設定を保存する必要はありません。 設定は、設定ページから移動するとすぐに自動的に保存されます。 設定を RSAT 設定ファイルに保存したり、既存の設定ファイルを開いたりすることもできます。

![UI 設定タブ。](media/UI-settings-tab.png)

### <a name="cloud-pos-settings"></a>Cloud POS の設定

**Cloud POS 設定** タブを選択し、Cloud POS のテスト ケースを実行する RSAT を構成します。 設定を保存する必要はありません。 設定は、設定ページから移動するとすぐに自動的に保存されます。

![UI Cloud POS タブ。](media/UI-cloud-POS-tab.png)

### <a name="useful-links"></a>役に立つリンク

**リンク** タブで、新しい機能が提供されます。 **リンク** タブを選択すると、Finance and Operations 環境にすばやく移動するか、最近のテスト実行、最後のテスト実行、および現在のテスト計画を表示するのに役立つ Azure DevOps ページに移動することができます。 RSAT ドキュメント ページへのリンクもあります。

![UI リンク タブ。](media/UI-links-tab.png)

### <a name="quick-navigation-to-azure-devops"></a>Azure DevOps にすばやく移動する機能

テスト計画の作業をしている場合は、**開く** ボタンに 3 つのオプションが表示されるようになりました。

+ Azure DevOps で選択したテスト ケースを開きます。
+ 選択したテスト スイートを開きます。
+ 最近のテスト実行を開きます。

このタブで、Azure DevOps で最も関連性の高いページへのクイック アクセスが提供されます。

![UI DevOps の移動。](media/UI-DevOps-navigate.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
