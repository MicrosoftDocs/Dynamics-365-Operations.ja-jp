---
title: 一般的なトラブルシューティング
description: このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関する一般的なトラブルシューティングの情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172694"
---
# <a name="general-troubleshooting"></a>一般的なトラブルシューティング

[!include [banner](../../includes/banner.md)]



このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関する一般的なトラブルシューティングの情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Package Deployer ツールを使用してデュアル書書き込み込みパッケージをインストールしようとすると、使用可能なソリューションが表示されない

Package Deployer ツールの一部のバージョンは、デュアル書き込みソリューション パッケージと互換性がありません。 パッケージを正常にインストールするには、Package Deployer ツールの [バージョン 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) またはそれ以降を使用してください。

Package Deployer ツールをインストールした後、次の手順に従ってソリューション パッケージをインストールしてください。

1. Yammer.com から最新のソリューション パッケージ ファイルをダウンロードします。 パッケージのZIP ファイルをダウンロードした後、ファイルを右クリックして **プロパティ**を選択します。 **ブロックの解除** チェック ボックスを選択し、**適用** を選択します。 **ブロックの解除** チェックボックスが表示されない場合は、zip ファイルのブロック解除が既にされているため、この手順を省略できます。

    ![プロパティ ダイアログ ボックス](media/unblock_option.png)

2. パッケージの zip ファイルを展開し、**Dynamics365FinanceAndOperationsCommon** フォルダのすべてのファイルをコピーします。

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 フォルダの内容](media/extract_package.png)

3. コピーされたすべてのファイルを Package Deployer ツールの**Tools** フォルダーに貼り付けます。 
4. **PackageDeployer.exe** を実行して Common Data Service の環境を選択し、ソリューションをインストールします。

    ![ツール フォルダのコンテンツ](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>Common Data Service のプラグイン トレース ログを有効にして確認し、エラーの詳細を表示します。

**トレース ログを有効にするために必要な役割とエラーの表示:** システム管理者

トレース ログを有効にするには、次の手順に従います。

1. Finance and Operations アプリにログインし、**設定** ページを開いて、**システム** 配下の**管理** を選択します。
2. **管理者** ページで、**システム管理**を選択します。
3. **カスタマイズ** タブの **プラグインおよびユーザー定義ワークフロー活動の追跡** フィールドで、**すべて** を選択してプラグインのトレース ログを有効にします。 例外が発生したときにのみトレースログを記録する場合は **例外** を選択します。


トレースログを確認にするには、次の手順に従います。

1. Finance and Operations アプリにログインし、**設定** ページを開いて、**カスタマイズ** 配下の**プラグイン トレース ログ** を選択します。
2. **タイプ名** フィールドが **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**に設定されているトレース ログを検索します。
3. 完全なログを表示するには、項目をダブルクリックし、**実行**ファストタブで **メッセージ ブロック** のテキストを確認します。

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>デバッグ モードを有効にして、アプリ Finance and Operations でのライブ同期に関する問題のトラブルシューティングを行います。

**エラーを表示するために必要な役割：** システム管理者

Common Data Serviceで発生するデュアル書き込みエラーは、Finance and Operationsアプリでも発生する場合があります。 エラーメッセージの完全なテキストが表示されない場合がありますが、これはメッセージが長すぎるか個人の識別情報 (PII) が含まれていることが原因です。 エラーの詳細ログを有効にするには、次の手順を実行してください。

1. Finance and Operations アプリにおけるすべてのプロジェクトの構成は、**DualWriteProjectConfiguration** エンティティ内に **IsDebugMode** プロパティが存在します。 Excel アドインを使用して **DualWriteProjectConfiguration** エンティティを開きます。

    > [!TIP]
    > エンティティを簡単に開くには、Excelアドインで **デザイン** モードを有効にしてから、ワークシートに**DualWriteProjectConfigurationEntity** を追加してください。 詳細については、[Excel でエンティティ データを開き、Excel アドインを使用して更新する](../../office-integration/use-excel-add-in.md)を参照してください。

2. プロジェクトの **IsDebugMode**プロパティを **はい** に設定します。
3. エラーが発生するシナリオを実行します。
4. 詳細なログは、DualWriteErrorLog テーブルで確認できます。 テーブル ブラウザーでデータを参照するには、次のURLを使用してください（必要に応じて**XXX**を置き換えてください）：

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Finance and Operations アプリの仮想マシンの同期エラーを確認する

**エラーを表示するために必要な役割：** システム管理者

1. Microsoft Dynamics Lifecycle Services (LCS) にログインします。
2. デュアル書き込みテストを実行する、LCS プロジェクトを開きます。
3. **クラウド ホスト環境**のタイトルを選択します。
4. リモート デスクトップを使用して、Finance and Operations アプリの仮想マシン (VM) にログインします。 LCS に表示されるローカル アカウントを使用します。
5. イベント ビューアーを開きます。
6. **アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DualWriteSync \> オペレーション**を選択します。
7. 最近発生したエラーの一覧を確認します。

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>Finance and Operations アプリの Common Data Service 環境のリンクを解除し、他の環境をリンクする

**環境のリンクの解除に必要な資格情報：** Azure ADテナント管理者

1. Finance and Operations アプリにサインインします。
2. **ワークスペース \> データ管理**に移動して、**デュアル書き込み**のタイルを選択します。
3. 実行中のすべてのマッピングを選択し、**停止**を選択します。
4. **リンク解除の環境**を選択します。
5. **はい**を選択して操作を確認します。

環境に新たなリンクを設定することができるようになります。
