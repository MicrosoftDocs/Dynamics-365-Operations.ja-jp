---
title: 一般的なトラブルシューティング
description: この記事では、財務と運用アプリと Dataverse 間の二重書き込み統合に関する一般的なトラブル シューティングの情報を提供します。
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f263e331d23ce0ddf60a4abc2467513aa342445
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112367"
---
# <a name="general-troubleshooting"></a>一般的なトラブルシューティング

[!include [banner](../../includes/banner.md)]



この記事では、財務と運用アプリと Dataverse 間の二重書き込み統合に関する一般的なトラブル シューティングの情報を提供します。

> [!IMPORTANT]
> この記事で説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Dataverse のプラグイン トレース ログを有効にして確認し、エラーの詳細を表示します

追跡ログは、Finance + Operations と Dataverse の間のデュアル書き込みライブ同期の問題をトラブルシューティングする場合に便利です 。 ログは、Dynamics 365 の技術およびエンジニアリング サポートを提供するチームに具体的な詳細を提供できます。 この記事では、追跡ログを有効にする方法と、追跡ログを表示する方法について説明します。 追跡ログは、Dynamics 365 設定ページで管理され、変更および表示するには管理者レベルの特権が必要です。 

**トレース ログを有効にするために必要な役割とエラーの表示:** システム管理者

### <a name="turn-on-the-trace-log"></a>追跡ログを有効にする
トレース ログを有効にするには、次の手順に従います。

1.  Dynamics 365 にログオンし、トップ ナビゲーションバーで **設定** を選択します。 システム ページで、**管理** をクリックします。
2.  管理ページで、**システム設定** をクリックします。
3.  **カスタマイズ** タブとプラグインを選択し、カスタム作業フロー活動追跡セクションで、ドロップダウンを **すべて** に変更します。 これにより、すべての活動が追跡され、潜在的な問題を確認する必要があるチームに包括的なデータ セットが提供されます。

> [!NOTE]
> ドロップダウンを **例外** に設定すると、例外 (エラー) が発生したときにのみ追跡情報が提供されます。

有効にすると、この場所に戻って **オフ** を選択することにより手動でオフにするまで、プラグイン追跡ログが収集され続けます。

### <a name="view-the-trace-log"></a>トレース ログの表示
トレースログを確認にするには、次の手順に従います。

1. Dynamics 365 設定ページのトップ ナビゲーションバーで **設定** を選択します。 
2. ページの **カスタマイズ** セクションで **プラグイン トレース ログ** を選択します。
3. 追跡ログの一覧には、名前のタイプやメッセージ名に基づくエントリが表示されます。
4. 目的のエントリを開き、ログ全体を表示します。 実行セクションのメッセージ ブロックには、プラグインに関する情報が表示されます。 可能な場合は、例外の詳細も提供されます。 

追跡ログの内容をコピーしてメモ帳などの別のアプリケーションに貼り付け、ログやテキスト ファイルを表示すると、すべてのコンテンツを簡単に把握できます。 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>デバッグ モードを有効にして、財務と運用アプリ間のライブ同期に関する問題のトラブルシューティングを行う

**エラーを表示するために必要な役割：** システム管理者

Dataverse で発生する二重書き込みエラーは、財務と運用アプリでも発生する場合があります。 エラーの詳細ログを有効にするには、次の手順を実行します。

1. 財務と運用アプリのすべてのプロジェクトの構成には、**DualWriteProjectConfiguration** テーブル内に **IsDebugMode** フラグがあります。
2. Excel アドインを使用して **DualWriteProjectConfiguration** を開きます。 アドインを使用するには、財務と運用の Excel アドインでデザイン モードを有効にし、シートに **DualWriteProjectConfiguration** を追加します。 詳細については、[Excel でのエンティティ データの表示と更新](../../office-integration/use-excel-add-in.md) を参照してください。
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

## <a name="dual-write-ui-landing-page-showing-blank"></a>空白が表示されたデュアル書き込み UI ランディング ページ
Microsoft Edge または Google Chrome ブラウザーでデュアル 書き込みページを開くと、ホーム ページが読み込まれず、空白のページや "問題が発生しました" などのエラーが表示されます。
開発者ツールのコンソール ログにエラーが表示されます。

>bundle.eed39124e62c58ef34d2.js:37 DOMException: 'Window' から 'sessionStorage' プロパティを読み取れません: このドキュメントへのアクセスが拒否されました。 at t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 ) at new t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103 ) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 ) at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728 ) at jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191 ) at Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692 ) at Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076 ) at Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 ) at vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 ) at hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151 )

UI では、ブラウザーのセッション記憶域を使用して、ホーム ページを読み込む一部のプロパティ値が格納されます。 これが機能するには、サイトのブラウザーでサード パーティの Cookie を許可する必要があります。 このエラーは、UI がセッション記憶域にアクセスできないことを示しています。 この問題が発生するシナリオは次の 2 つです。

1.  Edge/Chrome の Incognito モードで UI を開いており、Incognito でサード パーティ Cookie がブロックされている。
2.  Edge/Chromeでサード パーティの Cookie を完全にブロックしている。

### <a name="mitigation"></a>軽減策
ブラウザーの設定で、サード パーティ Cookie を許可する必要があります。

### <a name="google-chrome-browser"></a>Google Chrome ブラウザー
1 つ目のオプション:
1.  アドレス バーに chrome://settings/ と入力することで設定に移動し、[プライバシーとセキュリティ] -> [Cookie と他のサイトのデータ] に移動します。
2.  [すべての Cookie を許可する] を選択します。 この操作を実行しない場合、2 つ目のオプションに進みます。

2 つ目のオプション:
1.  アドレス バーに chrome://settings/ と入力することで設定に移動し、[プライバシーとセキュリティ] -> [Cookie と他のサイトのデータ] に移動します。
2.  [Incognito でサード パーティの Cookie をブロックする] または [サード パーティの Cookie をブロックする] を選択した場合、[Cookie を常に使用するサイト] に移動し、**追加** をクリックします。 
3.  財務と運用アプリのサイト名 (https://<your_FinOp_instance>.cloudax.dynamics.com) を追加します。 必ず、[すべての Cookie。このサイトでのみ] チェック ボックスをオンにしてください。 

### <a name="microsoft-edge-browser"></a>Microsoft Edge ブラウザー
1.  [設定] -> [サイトのアクセス許可] -> [Cookie とサイトのデータ] に移動します。
2.  [サード パーティの Cookie をブロックする] をオフにします。  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>財務と運用アプリから、別の Dataverse 環境のリンク解除およびリンクを行う方法

**環境のリンク解除に必要な役割:** 財務と運用アプリ、または Dataverse のいずれかのシステム管理者。

1. 財務と運用アプリにサインインします。
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

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>データ統合が最新の財務と運用スキーマを使用していることを確認する方法

最新のスキーマが使用されていない場合、データ統合でデータの問題が発生する可能性があります。 次の手順は、財務と運用アプリのエンティティ リストと、データ インテグレーターのエンティティを更新するのに役立ちます。

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>財務と運用環境のエンティティ リストの更新
1.  財務と運用環境にログオンします。
2.  **データ管理** を選択します。
3.  データ管理内で、**フレームワーク パラメータ** を選択します。
4.  **データのインポート/エクスポート フレームワークのパラメータ** ページで、**エンティティ設定** タブを選択し、**エンティティ リストの更新** を選択します。 関連するエンティティの数によっては、更新に 30 分以上かかる場合があります。
5.  **データ管理** に移動し、**データ エンティティ** を選択して、予期されるエンティティが一覧表示されていることを検証します。 予想されるエンティティが表示されない場合、エンティティが財務と運用環境に表示されていることを確認し、必要に応じて欠落しているエンティティを復元します。

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>更新で問題が解決しない場合は、エンティティを削除して再追加する

> [!NOTE]
> 削除する前に、エンティティを有効に使用している処理グループを停止する必要がある場合があります。

1.  財務と運用の環境で **データ管理** を選択し、**データ エンティティ** を選択します。
2.  問題のあるエンティティを検索し、対象のエンティティ、ステージング テーブル、エンティティ名、およびその他の設定をメモします。 一覧から 1 つまたは複数のエンティティを削除します。
3.  **新規** を選択し、手順 2 のデータを使用して 1 つまたは複数のエンティティを再追加します。 

#### <a name="refresh-entities-in-data-integrator"></a>データ インテグレーターでエンティティの更新
Power Platform 管理センターにログオン し、**データ統合を** を選択します。 問題が発生しているプロジェクトを開き、**エンティティの更新** を選択します。

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>ネットワーク トレースを有効にして保存し、サポート チケットにトレースを関連付けできるようにする方法

サポート チームは、いくつかの問題をトラブルシューティングするために、ネットワーク トレースを確認する必要がある場合があります。 ネットワーク トラックを作成するには、次の手順を実行します。

### <a name="google-chrome-browser"></a>Google Chrome ブラウザー

1. 開いたタブで **F12 キー** を押すか **開発者ツール** を選択して開発者ツールを開きます。
2. **ネットワーク** タブを開き、フィルターのテキスト ボックスに **integ** と入力します。
3. シナリオを実行し、ログに記録されている要求を遵守します。
4. エントリを右クリックし、**すべてをコンテンツ付きの HAR として保存** を選択します。

### <a name="microsoft-edge-browser"></a>Microsoft Edge ブラウザー

1. 開いたタブで **F12 キー** を押すか **開発者ツール** を選択して開発者ツールを開きます。
2. **ネットワーク** タブを開きます。
3. シナリオを実行します。
4. 結果を HAR としてエクスポートするには、**保存** を選択します。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

