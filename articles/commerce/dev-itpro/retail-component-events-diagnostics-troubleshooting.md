---
title: 診断とトラブルシューティングの Commerce コンポーネント イベント
description: この記事では、コマース固有のコンポーネントからイベントを検索する場所について説明します。
author: ShalabhjainMSFT
ms.date: 08/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 85493
ms.assetid: a22c9493-c000-4514-bb0d-b3cc674439d9
ms.search.industry: Retail
ms.openlocfilehash: 42060c4accf4f5ee0a594ead64f7e56d9b7516fc
ms.sourcegitcommit: 14a27b776befbc6793390f97e8fb0279c0ea18c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/15/2022
ms.locfileid: "9295913"
---
# <a name="commerce-component-events-for-diagnostics-and-troubleshooting"></a>診断とトラブルシューティングの Commerce コンポーネント イベント

[!include [banner](../includes/banner.md)]

この記事では、コマース固有のコンポーネントからイベントを検索する場所について説明します。 診断とトラブルシューティングを有効にするには、Retail Modern POS などのセルフホスト型のコンポーネントを含むすべての Commerce コンポーネントと Commerce Scale Unit や e コマース モジュールなどのクラウド ホスト型コンポーネントは、それらのイベントにイベント ビューアー (または Retail Cloud F12 などのブラウザー開発ツール コンソール) にローカルでログします。 イベントは、Microsoft Dynamics Lifecycle Services (LCS) ログ検索エクスペリエンスにも記録されます。

## <a name="viewing-events-in-event-viewer"></a>イベント ビューアーでのイベントの表示

イベントがログされるコンピューターに対して物理的にアクセスできる場合、イベント ビューアーを使用して、Microsoft Windows を実行するコンピューター上にインストールされたコンポーネント用イベントを表示することができます。 イベント ビューアーの詳細については、TechNet の [イベント ビューアー](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)) を参照してください。 また、イベント ビューアーを使用して、ユーザーがアクセス権を持つコンピューターからリモートでイベントを表示することができます。 イベント ビューアーを使用して、リモートでイベントを表示する方法の詳細については、TechNet の [リモート コンピューターでイベント ログを使用](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766438(v=ws.11)) を参照してください。 イベント ビューアは通常、次の使用例でのトラブルシューティングに使用されます。

- 開発者トポロジまたはイベント ビューアーへのアクセスを提供するダウンロード可能な仮想ハードディスク (VHD) での開発。
- 会議室パイロットを実行していて、そのコンピューターのイベント ビューアにアクセスできるときのクライアント コンポーネント。

ただし、ほとんどの場合、特にコンピューターのイベント ビューアーへのアクセスがない場合、LCS でログ検索を使用できます。 E コマース モジュールに対しては、イベントは現在のところ、ブラウザ開発者ツール (F12キーなど) でのみ使用できます。 ログ検索については、この記事の後半で説明します。 このセクションは、次のコンポーネントに適用されます。

- コマース スケール ユニット
- Retail Modern POS
- Retail ハードウェア ステーション

### <a name="find-commerce-specific-events-in-event-viewer"></a>イベント ビューアーで、コマース固有のイベントを検索する

コンピューターでイベント ビューアを起動するには、**開始** ボタンをクリックし、**イベント ビューア** をクリックします。

[![スタート ボタンのショートカット メニューのイベント ビューアー コマンド。](./media/launch-event-viewer.png)](./media/launch-event-viewer.png)

すべてのコマース固有イベント ログにはイベント ビューアーで次のパスを確認できます。アプリケーションおよびサービス ログ \\Microsoft\\Dynamics 以下のコマース固有のイベント ログを提供します。

- **Commerce-RetailServer** – このログには、Commerce Scale Unit コンポーネントによって記録されるイベントが含まれます。
- **Commerce-ModernPos** - このログには、Retail Modern POS によって記録されるイベントが含まれます。 これらのイベントには、TypeScript および C\# (CRT) レイヤーからのイベントが含まれます。
- **Commerce-LoggingProvider** – このログには、この記事の前半で一覧に含まれていない他のすべてのコマース コンポーネントによって記録されるイベントが含まれています。

### <a name="enable-debug-event-logs"></a>デバッグ イベント ログの有効化

現在、さまざまなコンポーネントによって記録されたイベントの一部がデバッグ イベント ログに送信されます。 これらのイベントは非常に高いレートで記録され、詳細なデバッグ シナリオでのみ有用な詳細イベントです。 イベント ビューアーでのデバッグ イベント ログを有効にするには、この手順を実行します。

- デバッグ ログを右クリックし、**ログの有効化** をクリックします。

![デバッグ ログのショートカット メニューでログ コマンドを有効にします。](./media/enable-debugging-log.png)

## <a name="viewing-events-by-using-the-f12-browser-developer-tools-console"></a>(F12) ブラウザー開発者ツール コンソールを使用してイベントを表示

Retail Cloud POS と e コマース モジュールはブラウザー ベースのコンポーネントなので、ブラウザー開発者ツール コンソールを使用してそのイベントを表示できます。 Microsoft ブラウザ開発者ツール コンソールの詳細については、[コンソールを使用してエラーとデバッグを表示する](/microsoft-edge/devtools-guide/console) を参照してください。 Retail Cloud POS または e コマース モジュールのブラウザー開発者ツールを使用するには、サポートされているバージョンのブラウザを使用する必要があります。

### <a name="view-events-in-the-browser-developer-tools-console"></a>ブラウザー開発者ツール コンソールでのイベントの表示

1. ブラウザーを起動し、Retail Cloud POS または e コマースの Web サイトに移動します。
2. F12 キーを押し、**コンソール** タブをクリックします。
3. Retail Cloud POS または e コマース Web サイトの操作を実行する際に、イベントはコンソールに記録されます。 イベント重要度でフィルター処理して、異なる重要度レベルのイベントを表示することができます。

[![ブラウザー開発者ツールのコンソール タブ。](./media/browser-console-1024x522.png)](./media/browser-console.png)

## <a name="correlating-events"></a>関連のイベント

このセクションでは、さまざまなコマース コンポーネントからイベントを関連付ける方法について説明します。

### <a name="data-flow-between-a-pos-client-and-commerce-scale-unit"></a>POS クライアントと Commerce Scale Unit 間のデータ フロー

以下の図は、販売時点管理 (POS) クライアントと Commerce Scale Unit 間のデータ フローを示しています。

#### <a name="pos-client-startup"></a>POS クライアントの起動

ユーザーが POS クライアントを起動すると、新しい AppSessionID が生成されます。 AppSessionID は、POS クライアントで計測されるすべてのイベントのログを作成するために使用されます。 イベント ビューアおよびアプリ インサイトに記録したすべてのイベントはこの ID を持っています。

#### <a name="user-sign-in"></a>ユーザー サインイン

ユーザーが POS クライアントにサインインすると、新しい UserSessionID が生成されます。 UserSessionID は、POS クライアントで計測されるすべてのイベントのログを作成するために使用されます。 イベント ビューアーに記録されたすべてのユーザー イベントはこの ID を持ちます。 この ID は、ユーザーがログインしている間維持されます。 現在のユーザーがサインアウトして、新しいユーザーがサインインすると、新しい UserSessionID が生成されます。

#### <a name="pos-client-calls-to-commerce-scale-unit"></a>POS クライアントによる Commerce Scale Unit への呼び出し

POS クライアントが Commerce Scale Unit を呼び出すときはいつでも、AppSessionID と UserSessionID がヘッダーとして送信されます。 次に、Commerce Scale Unit は、受信要求 (イベント ID 5000) のイベントを記録します。 このイベントには、2 つの ID と ActivityID が含まれます。 その後、ActivityID はすべての関連するイベントにも使用されます。 AppSessionID、UserSessionID、ActivityID は、Commerce Scale Unit がホストされているイベント ログで使用可能です。 LCS ログ検索でも利用できます。

#### <a name="request-activity-on-commerce-scale-unit"></a>Commerce Scale Unit での要求の活動

Commerce Scale Unit 要求の一部として記録されるすべてのイベントは、最初の受信要求イベント用に記録された初期イベントと同じ ActivityID を持ちます (イベント ID 5000)。 これらのイベントは、イベント ビューアーと LCS ログ検索の両方で利用できます。

[![POS クライアントと Commerce Scale Unit 間のデータ フロー。](./media/event-log-data-flow1-1018x1024.png)](./media/event-log-data-flow1.png)

### <a name="finding-retail-modern-pos-events-in-event-viewer"></a>イベント ビューアーでの Retail Modern POS イベントの検索

Retail Modern POS によってが記録されたすべてのイベントには、次のデータ点が含まれています。

- **AppSessionID** - アプリケーションが最初に起動されたときに生成される一意の ID。 これは記録されるすべてのイベントに含まれています。
- **UserSessionID** – ユーザーが Retail Modern POS にサインインするときに生成される固有の ID。 これはユーザーがサインインしている限り、記録されるすべてのイベントに含まれています。 新しいユーザーがサインインするとき、新しい UserSessionID が作成されます。

AppSessionID 値および UserSessionID 値は、Retail Modern POS がインストールされているマシン上のイベント ビューアーの **詳細** タブで見つけることができます。

[![イベント ビューアーの詳細タブ。](./media/correlation-1024x672.png)](./media/correlation.png)

### <a name="finding-incoming-commerce-scale-unit-request-events-in-event-viewer"></a>イベント ビューアーで、受信する Commerce Scale Unit 要求のイベントを検索

イベント ビューアで受信する Commerce Scale Unit 要求のデータを関連付けるには、最初に **Analytic** チャネルを有効にする必要があります。 分析チャネルを有効にするには、次の手順を実行します。

1. イベント ビューアーの左ウィンドウで、**Commerce RetailServer** を選択します。
2. **表示** &gt; **分析とデバッグ ログを有効にします** をクリックします。 分析チャネルの新しいノードは、**Commerce-RetailServer** ログ プロバイダーの下に表示されます。
3. **分析** ノードを右クリックし、**ログの有効化** をクリックします。

イベント ビューアーでは、受信しているすべての Commerce Scale Unit の要求がイベント 5000 として Commerce-RetailServer ソースの分析チャネルに記録されます。 これらのイベントには、前述した AppSessionID と UserSessionID もあります。 すべてのイベントには、同じ要求のログに記録されたイベントごとに、固有の ActivityID も用意されています。

## <a name="using-lcs-log-search"></a>LCS ログ検索の使用

LCS ログ検索で、1 つのポータルからすべてのコンポーネントのデータを表示できます。 イベントは、(Commerce Scale Unit などの) クラウドでホストされたコンポーネントと (Retail Modern POS および Retail Hardware Station などの) 店舗内コンポーネントの両方からアクセスすることができます。 すべてのクラウドホストおよびストア内コンポーネントからのイベント データは、索引付けされ検索可能になる LCS ログ検索に流れます。 データは通常、記録されてから 5 分以内に利用可能です。 POS クライアントおよび Retail Hardware Station では、すべてのイベントが永続ストレージにローカルでキュー格納され、キューがいっぱいになった後にバッチでアップロードされます。 この動作により、ネットワーク トラフィックを最適化できます。  また、インターネット接続がない場合でもイベントを保存することができます。 接続が回復した後、すべての保留中のイベントがアップロードされます。

LCS ログ検索は、HA 運用トポロジに使用できます。 次のコマースのコンポーネントに使用することができます。

- Retail Modern POS
- Retail Cloud POS
- Commerce Scale Unit (Retail Cloud Scale Unit で実行中)

LCS ログ検索に、次のコマース コンポーネントからのログは **含まれません**。

- コマース レイアウト デザイナー
- コマース受領書デザイナー
- Retail Modern POS のセルフ サービス インストーラー
- 小売ハードウェア ステーション用のセルフ サービス インストーラー
- Commerce Scale Unit (Retail Store Scale Unit で実行中)
- Retail ハードウェア ステーション

### <a name="access-lcs-log-search"></a>LCS ログ検索にアクセス

LCS ログ検索にアクセスするには、次の手順を実行します。

1. [Lifecycle Services](https://lcs.dynamics.com/) に移動します。
2. プロジェクトに関連付けられている資格情報を使用してログインします。
3. プロジェクト ページで、正しいプロジェクトを選択します。
4. **プロジェクトの詳細** ページで、正しい環境を選択します。
5. **環境の詳細** ページで、**環境の監視** をクリックします。
6. **環境の監視** ページで、**未加工ログの表示** をクリックします。
7. **ログ検索** ページで、次のいずれかのクエリを選択します。

    - **コマース クライアント イベント** クエリには、Retail Modern POS、Retail Cloud POS、および Commerce Scale Unit (Retail Cloud Scale Unit で実行中) からのイベントが含まれます
    - **すべてのログ** クエリには、Commerce Scale Unit、Commerce Data Exchange、および Commerce Data Exchange: リアルタイム サービスからのデータが含まれます

以下の条件でフィルター処理してクエリを調整することができます。

- 開始および終了日時 (協定世界時 \[UTC\])
- デバイス ID
- POS ユーザー
- POS アプリケーション セッション ID
- POS ユーザー セッション ID
- 重大度


![環境監視ページの検索結果。](./media/log-search-results.png)

### <a name="access-logs-in-application-insights"></a>Application Insights のログへのアクセス

Commerce コンポーネントの診断イベントは、Application Insights からアクセスすることもできます。

#### <a name="commerce-scale-unit-minimum-version-requirements"></a>Commerce Scale Unit 最小バージョン要件

Commerce Scale Unit には、次の最小バージョン要件があります。

- 10.0.23 (Retail Server バージョン 9.33.22062.15 およびそれ以降)
- 10.0.24 (Retail Server バージョン 9.34.22062.14 およびそれ以降)
- 10.0.25 (Retail Server バージョン 9.35.22062.13 およびそれ以降)
- 10.0.26 およびそれ以降 (すべてのバージョン)

#### <a name="enable-diagnostic-events-in-application-insights"></a>Application Insights の診断イベントを有効にする

> [!IMPORTANT]
> システム オペレーション インサイト プレビューを使用した場合、次の手順を実行してシステム オペレーション インサイトを有効にする必要があります。 このようにして、イベントに対し信頼性があり安全なアクセスを継続することができます。

Commerce コンポーネントの診断イベントを有効にするには、Application Insights アカウントが必要です。 既存のアカウントを使用するか、または[新しいアカウントを作成](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource)できます。 データ プライバシーの理由から、運用、サンドボックス、および開発環境とで個別の Application Insights アカウントを使用することをお勧めします。 アカウントを作成した後、Commerce 本部で **オペレーション インサイト** 機能を有効にする必要があります。

Commerce 本部で Application Insights の診断イベントを有効にするには、以下の手順に従います。

1. **機能管理** ワークスペースで、**オペレーション インサイト** 機能を有効にします。
1. **システム管理 \> オペレーション インサイト** に移動します。
1. **構成** タブで、**Commerce チャネル イベント** オプション を **はい** に設定します。
1. **環境** タブで、Application Insights を使用する計画があるすべての環境に対して **LCS 環境 ID** と **環境モード** の値を入力します。 各環境の LCS 環境 ID は、LCS の環境の **環境の詳細** ページで見つけることができます。 データベースのコピー操作が実行されるときに診断イベントが正しくない環境に誤って送信されるのを防ぐために、この手順が必要です。
1. **Application Insights レジストリ** タブで、各 Application Insights アカウントを使用する環境の Application Insights インストルメンテーション キーおよび対応する環境モードを指定します。
1. 前の構成が完了した後、**CDX ジョブ 1110** ジョブを実行する必要があります。 このジョブが独自のスケジュールで実行されるのを待つか、手動で実行することができます。
1. 各 Commerce Scale Unit を再起動します。 LCS で、**環境の詳細 \> Commerce \> 管理** に移動して Commerce Scale Unit のインスタンスを選択し、**再起動** を選択します。
1. Application Insights を使用にする環境ごとに前の手順を繰り返します。

> [!NOTE]
> Commerce バージョン 10.0.29 以降では、このセクションの手順により、販売時点管理 (POS) の運用イベントのストリーミングを Application Insights アカウントに対して有効化することもできます。
>
> 構成ファイルを使用して POS の運用情報イベントを制御するには、次の手順を実行します。
>
>1. テキスト エディタを使用して、“C:\Program Files (x86)\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker”にある "DLLHost.exe.config" ファイルを開きます。
>
>1. diagnosticsSection” からクラス名 "Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger" を持つシンク XML 要素を削除します。 

#### <a name="disable-diagnostic-events-in-application-insights"></a>Application Insights の診断イベントを無効にする

Application Insights へ診断イベントを送信する必要がなくなった場合は、機能を無効にする必要があります。

> [!IMPORTANT]
> 診断イベントを無効にする場合、**機能管理** で機能を無効にするだけでは不十分です。

Commerce 本部で Application Insights の診断イベントを無効にするには、以下の手順に従います。

1. **システム管理 \> オペレーション インサイト** に移動します。
1. **構成** タブで、**Commerce チャネル イベント** オプション を **いいえ** に設定します。
1. 前の構成が完了した後、**CDX ジョブ 1110** ジョブを実行する必要があります。 このジョブが独自のスケジュールで実行されるのを待つか、手動で実行することができます。
1. 各 Commerce Scale Unit を再起動します。 LCS で、**環境の詳細 \> Commerce \> 管理** に移動して Commerce Scale Unit のインスタンスを選択し、**再起動** を選択します。
1. Application Insights を無効にする環境ごとに前の手順を繰り返します。

単一の環境に対して診断イベントを無効にするには、**オペレーション インサイト** ページの **Application Insights レジストリ** タブにあるインストルメンテーション キーを削除します。 前の手順の手順 3 と 4 を実行します。

> [!NOTE]
> Commerce バージョン 10.0.29 以降では、このセクションのステップにより、POS の運用インサイト イベントのストリーミングを Application Insights アカウントに対して無効化することもできます。 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
