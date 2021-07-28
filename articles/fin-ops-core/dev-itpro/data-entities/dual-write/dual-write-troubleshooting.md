---
title: 一般的なトラブルシューティング
description: このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関する一般的なトラブルシューティングの情報を提供します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: ccad9c55c0200d008525c7d3fdaeeef99b7eecfb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350743"
---
# <a name="general-troubleshooting"></a>一般的なトラブルシューティング

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関する一般的なトラブルシューティングの情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Package Deployer ツールを使用してデュアル書書き込み込みパッケージをインストールしようとすると、使用可能なソリューションが表示されない

Package Deployer ツールの一部のバージョンは、デュアル書き込みソリューション パッケージと互換性がありません。 パッケージを正常にインストールするには、Package Deployer ツールの [バージョン 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) またはそれ以降を使用してください。

Package Deployer ツールをインストールした後、次の手順に従ってソリューション パッケージをインストールしてください。

1. Yammer.com から最新のソリューション パッケージ ファイルをダウンロードします。 パッケージのZIP ファイルをダウンロードした後、ファイルを右クリックして **プロパティ** を選択します。 **ブロックの解除** チェック ボックスを選択し、**適用** を選択します。 **ブロックの解除** チェックボックスが表示されない場合は、zip ファイルのブロック解除が既にされているため、この手順を省略できます。

    ![プロパティ ダイアログ ボックス。](media/unblock_option.png)

2. パッケージの zip ファイルを展開し、**Dynamics365FinanceAndOperationsCommon** フォルダのすべてのファイルをコピーします。

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 フォルダの内容。](media/extract_package.png)

3. コピーされたすべてのファイルを Package Deployer ツールの **Tools** フォルダーに貼り付けます。 
4. **PackageDeployer.exe** を実行して Dataverse の環境を選択し、ソリューションをインストールします。

    ![ツール フォルダのコンテンツ。](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Dataverse のプラグイン トレース ログを有効にして確認し、エラーの詳細を表示します

**トレース ログを有効にするために必要な役割とエラーの表示:** システム管理者

トレース ログを有効にするには、次の手順に従います。

1. Dynamics 365 のモデル駆動型アプリにサインインし、**システム** 配下の **設定** ページを開き、 **管理** を選択します。
2. **管理者** ページで、**システム管理** を選択します。
3. **カスタマイズ** タブの **プラグインおよびユーザー定義ワークフロー活動の追跡** 列で、**すべて** を選択してプラグインのトレース ログを有効にします。 例外が発生したときにのみトレースログを記録する場合は **例外** を選択します。


トレースログを確認にするには、次の手順に従います。

1. Dynamics 365 のモデル駆動型アプリにサインインし、**カスタマイズ** 配下の **設定** ページを開き、 **プラグイン トレース ログ** を選択します。
2. **タイプ名** 列が **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** に設定されているトレース ログを検索します。
3. 完全なログを表示するには、項目をダブルクリックし、**実行** ファストタブで **メッセージ ブロック** のテキストを確認します。

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>デバッグ モードを有効にして、アプリ Finance and Operations でのライブ同期に関する問題のトラブルシューティングを行います。

**エラーを表示するために必要な役割：** Dataverse で発生したシステム管理のデュアル書き込みエラーは、Finance and Operations アプリに表示される場合があります。 エラーメッセージの完全なテキストが表示されない場合がありますが、これはメッセージが長すぎるか個人の識別情報 (PII) が含まれていることが原因です。 エラーの詳細ログを有効にするには、次の手順を実行してください。

1. Finance and Operations アプリにおけるすべてのプロジェクトの構成は、**DualWriteProjectConfiguration** テーブル内に **IsDebugMode** プロパティが存在します。 Excel アドインを使用して **DualWriteProjectConfiguration** テーブルを開きます。

    > [!TIP]
    > テーブルを簡単に開くには、Excel アドインで **デザイン** モードを有効にしてから、ワークシートに **DualWriteProjectConfigurationEntity** を追加してください。 詳細については、[Excel でテーブル データを開き、Excel アドインを使用して更新する](../../office-integration/use-excel-add-in.md) を参照してください。

2. プロジェクトの **IsDebugMode** プロパティを **はい** に設定します。
3. エラーが発生するシナリオを実行します。
4. 詳細なログは、DualWriteErrorLog テーブルで確認できます。 テーブル ブラウザーでデータを参照するには、次のURLを使用してください（必要に応じて **XXX** を置き換えてください）：

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Finance and Operations アプリの仮想マシンの同期エラーを確認する

**エラーを表示するために必要な役割：** システム管理者

1. Microsoft Dynamics Lifecycle Services (LCS) にログインします。
2. デュアル書き込みテストを実行する、LCS プロジェクトを開きます。
3. **クラウド ホスト環境** のタイトルを選択します。
4. リモート デスクトップを使用して、Finance and Operations アプリの仮想マシン (VM) にログインします。 LCS に表示されるローカル アカウントを使用します。
5. イベント ビューアーを開きます。
6. **アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DualWriteSync \> オペレーション** を選択します。
7. 最近発生したエラーの一覧を確認します。

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Finance and Operations アプリの Dataverse 環境のリンクを解除し、他の環境をリンクする

**環境のリンクの解除に必要な役割：** Finance and Operations アプリ、または Dataverse のいずれかのシステム管理者。

1. Finance and Operations アプリにサインインします。
2. **ワークスペース \> データ管理** に移動して、**デュアル書き込み** のタイルを選択します。
3. 実行中のすべてのマッピングを選択し、**停止** を選択します。
4. **リンク解除の環境** を選択します。
5. **はい** を選択して操作を確認します。

環境に新たなリンクを設定することができるようになります。

## <a name="unable-to-view-the-sales-order-line-information-form"></a>販売注文明細行の情報フォームを表示できない 

Dynamics 365 Sales で販売注文を作成する際に、**+ 製品の追加** をクリックすると、Dynamics 365 Project Operations の注文明細行フォームにリダイレクトされる場合があります。 このフォームでは、販売注文明細行の **情報** フォームを表示することはできません。 **新規注文明細行** 配下のドロップダウン リストには、**情報** のオプションが表示されません。 これが発生するのは、プロジェクト オペレーションがご利用の環境にインストールされているためです。

**情報** フォームのオプションを再度有効にするには、次の手順を実行してください：
1. **注文明細行** テーブルに移動します。
2. フォーム ノード配下の **情報** フォームを確認します。 
3. **情報** フォームを選択し、**セキュリティロールの有効化** をクリックします。 
4. **すべてのユーザーに表示** されるようにセキュリティ設定を変更します。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]