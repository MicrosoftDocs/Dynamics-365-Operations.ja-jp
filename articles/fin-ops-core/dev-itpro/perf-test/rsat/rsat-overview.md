---
title: Regression Suite Automation Tool
description: Regression Suite Automation Tool では、機能パワー ユーザーがタスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくても自動テストのスイートに変換できるようにします。
author: robadawy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6ffd1f6261b8bf7d4d52497217df79f6cbdde6e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680446"
---
# <a name="regression-suite-automation-tool"></a>Regression Suite Automation Tool

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>概要
Regression Suite Automation Tool (RSAT) を使用すると、ユーザー受け入れテスト (UAT) の時間と費用を大幅に縮小できます。 通常、UAT は Microsoft アプリケーションの更新プログラムを取得するか、カスタム コードおよび構成を実稼働環境に適用する前に必要です。 RSAT により、機能パワー ユーザーはタスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくてもタスク記録を一連の自動テストに変換できます。 タスク レコーダーの詳細については、 [タスク レコーダー のリソース](../../user-interface/task-recorder.md) を参照してください。

RSATは、テストの実行、報告、および調査のために Microsoft Azure DevOps と完全に統合されています。 テスト パラメーターは、テスト ステップから切り離され、Microsoft Excel ファイルに保存されます。

RSAT の使用についての定義。

+ [Regression Suite Automation Tool (このトピック)](rsat-overview.md)
+ [Regression Suite Automation Tool インストールおよび構成](rsat-install-configure.md)
+ [Regression Suite Automation Tool テスト ケースの実行](rsat-run.md)
+ [予測値を検証する](rsat-validate-expected.md)
+ [テスト ケースのチェーン](rsat-chain-test-cases.md)
+ [派生テスト ケース](rsat-derived-test-cases.md)
+ [Regression Suite Automation Tool ベスト プラクティス](rsat-best-practices.md)
+ [Regression Suite Automation Tool のトラブルシューティング](rsat-troubleshooting.md)


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

上記の [RSAT 2.0 での Excel エクスペリエンスの向上](https://youtu.be/fcEkSIVQ1Bg)ビデオは、YouTube で視聴できる [Finance and Operations のプレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)に含まれています。 


## <a name="end-to-end-flow"></a>エンド ツー エンド フロー
このツールは、次に定義するエンド ツー エンド フローのパーツに含まれています。 このアプリケーションは、Microsoft Dynamics Lifecycle Services (LCS) および Azure DevOps と共に、テスト ケースの作成 (タスク レコーダーを使用)、構成、実行、調査、および報告に対する一連のツールを提供します。

![作成、構成、実行](media/end-to-end.png)

このプロセスの詳細については、[ユーザー受け入れテストを作成して自動化する](../../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)を参照してください。

## <a name="lcs-and-bpm"></a>LCS および BPM

LCS でビジネス プロセス モデラー (BPM) ツールを使用する必要はありません。 ただし、プロジェクトとテナント間でテスト ライブラリを管理および配布できるようにする場合、推奨されているツールは BPM です。 これらの機能は、Microsoft パートナーおよび独立系ソフトウェア ベンダー (ISV) にとって特に便利です。 BPM では、LCS ソリューションの一部としてテスト ライブラリを配布できるようにします。

BPM を使用していない場合は、Azure DevOps で手動でテスト ケースを作成し、開発者記録ファイルを Azure DevOps テスト ケースに添付できます。 開発者記録ファイルは、タスク レコーダー ウィンドウから直接作成できます。

![開発者としてタスク レコードを保存](media/save-as-developer.png)

開発者記録ファイルに **Recording.xml** という名前を付けてから、Azure DevOps テスト ケースに添付する必要があります。 または、記録ファイル **-テスト ケース タイトル-.xml** という名前を付けることもできます。これは、**-テスト ケース タイトル-** はテスト ケースの DevOps タイトルになります。

![添付ファイルの追加](media/attachments.png)

## <a name="intended-usage-and-test-classification"></a>使用目的およびテストの分類

### <a name="business-cycle-business-process-testing"></a>ビジネス サイクル (ビジネス プロセス) のテスト
Regression Suite Automation Tool は、ビジネス サイクル テストおよびシナリオ テスト (複数のコンポーネントのテスト) を使用目的としており、通常は開発ライフ サイクルの終了時に発生します。 これは、*ユーザー受け入れテスト* とも呼ばれます。 ビジネス サイクルのテストは、コンポーネントまたは単体テストよりも少ない数のテスト ケースで構成されます。 これを下の図に示します。

![単体テスト、コンポーネント テスト、複数のコンポーネントテスト、ビジネス サイクルテスト](media/business-cycle.png)

### <a name="warehouse-mobile-app"></a>Warehouse Mobile App
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
