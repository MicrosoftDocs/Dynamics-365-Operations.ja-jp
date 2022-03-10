---
title: 一般的なトラブルシューティング
description: このトピックでは、財務と運用アプリと Dataverse 間のデュアル書き込み統合に関する一般的なトラブル シューティングの情報を提供します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6f5b9f26990e2f4db9bf69040a6c4be31400b40
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062341"
---
# <a name="general-troubleshooting"></a>一般的なトラブルシューティング

[!include [banner](../../includes/banner.md)]



このトピックでは、財務と運用アプリと Dataverse 間のデュアル書き込み統合に関する一般的なトラブル シューティングの情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Dataverse のプラグイン トレース ログを有効にして確認し、エラーの詳細を表示します

**トレース ログを有効にするために必要な役割とエラーの表示:** システム管理者

トレース ログを有効にするには、次の手順に従います。

1. Customer Engagement アプリにログインし、**設定** ページを開いてから、**システム** で **管理者** を選択します。
2. **管理者** ページで、**システム管理** を選択します。
3. **カスタマイズ** タブの **プラグインおよびユーザー定義ワークフロー活動の追跡** 列で、**すべて** を選択してプラグインのトレース ログを有効にします。 例外が発生したときにのみトレースログを記録する場合は **例外** を選択します。


トレースログを確認にするには、次の手順に従います。

1. Customer Engagement アプリにログインし **設定** ページを開いてから、**カスタマイズ** で **プラグイン トレース ログ** を選択します。
2. **タイプ名** 列が **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** に設定されているトレース ログを検索します。
3. 完全なログを表示するには、項目をダブルクリックし、**実行** ファストタブで **メッセージ ブロック** のテキストを確認します。

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>デバッグ モードを有効にして、財務と運用アプリでのライブ同期に関する問題のトラブルシューティングを行います

**エラーを表示するために必要な役割：** システム管理者

Dataverse で発生するデュアル書き込みエラーは、財務と運用アプリでも発生する場合があります。 エラーの詳細ログを有効にするには、次の手順を実行します。

1. 財務と運用アプリのすべてのプロジェクトの構成には、**DualWriteProjectConfiguration** テーブル内に **IsDebugMode** フラグがあります。
2. Excel アドインを使用して **DualWriteProjectConfiguration** を開きます。 アドインを使用するには、Finance and Operations の Excel アドインでデザイン モードを有効にし、シートに **DualWriteProjectConfiguration** を追加します。 詳細については、[Excel でのエンティティ データの表示と更新](../../office-integration/use-excel-add-in.md) を参照してください。
3. プロジェクトで、**IsDebugMode** を **はい** に設定します。
4. エラーが発生するシナリオを実行します。
5. 詳細なログは、**DualWriteErrorLog** テーブルに保存されます。
6. テーブル ブラウザでデータをルックアップするには、次のリンクを使用します。`https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`、必要に応じて `999` と置き換えます。
7. プラットフォーム 更新プログラム 37 およびそれ以降のバージョンで使用可能な [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe) の後に再度更新します。 この修正プログラムがインストールされている場合、デバッグ モードでさらに多くのログをキャプチャします。  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>財務と運用アプリの仮想マシンの同期エラーを確認する

**エラーを表示するために必要な役割：** システム管理者

1. Microsoft Dynamics Lifecycle Services (LCS) にログインします。
2. デュアル書き込みテストを実行する、LCS プロジェクトを開きます。
3. **クラウド ホスト環境** のタイトルを選択します。
4. リモート デスクトップを使用して、財務と運用アプリの仮想マシン (VM) にログインします。 LCS に表示されるローカル アカウントを使用します。
5. イベント ビューアーを開きます。
6. **アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DualWriteSync \> オペレーション** を選択します。
7. 最近発生したエラーの一覧を確認します。

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>財務と運用アプリから、別の Dataverse 環境をリンク/リンク解除する方法

**環境のリンクの解除に必要な役割:** 財務と運用アプリ、または Dataverse のいずれかのシステム管理者。

1. 財務と運用アプリにログインします。
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

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>ネットワーク トレースを有効にして保存し、サポート チケットにトレースを関連付けできるようにする方法

サポート チームは、いくつかの問題をトラブルシューティングするために、ネットワーク トレースを確認する必要がある場合があります。 ネットワーク トラックを作成するには、次の手順を実行します。

### <a name="chrome"></a>Chrome

1. 開いたタブで **F12 キー** を押すか **開発者ツール** を選択して開発者ツールを開きます。
2. **ネットワーク** タブを開き、フィルターのテキスト ボックスに **integ** と入力します。
3. シナリオを実行し、ログに記録されている要求を遵守します。
4. エントリを右クリックし、**すべてをコンテンツ付きの HAR として保存** を選択します。

### <a name="microsoft-edge"></a>Microsoft Edge

1. 開いたタブで **F12 キー** を押すか **開発者ツール** を選択して開発者ツールを開きます。
2. **ネットワーク** タブを開きます。
3. シナリオを実行します。
4. 結果を HAR としてエクスポートするには、**保存** を選択します。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
