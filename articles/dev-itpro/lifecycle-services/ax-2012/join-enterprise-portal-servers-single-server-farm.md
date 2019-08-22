---
title: エンタープライズ ポータル サーバーの 1 つのサーバー ファームへの結合
description: この記事では、エンタープライズ ポータル サーバー (Microsoft Dynamics AX 2012 用) を単一のサーバー ファームに参加させる方法について説明します。
author: aneesmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 27431
ms.assetid: 05316e9d-818e-4f4b-901c-2e67fe8edfd1
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: f0f4e5ef01c11cb7da6dd944caa4a2aecf0fd5e7
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850545"
---
# <a name="join-enterprise-portal-servers-into-a-single-server-farm"></a>エンタープライズ ポータル サーバーの 1 つのサーバー ファームへの結合

[!include [banner](../../includes/banner.md)]

この記事では、エンタープライズ ポータル サーバー (Microsoft Dynamics AX 2012 用) を単一のサーバー ファームに参加させる方法について説明します。 

Microsoft Dynamics Lifecycle Services (LCS) でエンタープライズ ポータル (EP) サーバーが配置されると、各 EP サーバーは独自のサーバー ファームに配置されます。 この記事のステップでは、すべての EP サーバーを単一のサーバー ファームに参加させる方法を示します。 基本概念は、1 台の EP サーバー上にサーバー ファームを保持し、その他のすべての EP サーバーをそのファームに結合することです。 この記事の情報は、次の前提条件に基づいています。

-   *N* EP サーバーは、LCS によってが配置され、これらのサーバーは、EP-01、EP 02、EP-03...EP 0*N*とラベル付けされています。
-   ロード バランサを AzureILB01 と呼びます。
-   EP-01 を単一のサーバー ファームとして使用し、その他のすべての EP サーバーはそのファームに参加します。

## <a name="overview"></a>概要
次の図は、EP サーバーを単一のサーバー ファームに参加させるプロセスを示しています。 [![ProcessFlow\_ConfigureEPServersInFarm](./media/processflow_configureepserversinfarm.png)](./media/processflow_configureepserversinfarm.png)

## <a name="put-ep-servers-into-a-single-server-farm"></a>1 台のサーバー ファームに EP サーバーを配置
1.  Dynamics インストーラー ユーザー サービス アカウントを使用して EP-01 にログオンします。
2.  Microsoft SharePoint 2013 Central Administration を起動します。
3.  **システム設定** &gt; **代替アクセス マッピングのコンフィギュレーション**に移動します。
4.  **内部 URL を追加する**をクリックします。 次のスクリーン ショットは、EP サイトが作成されたポートである、ポート 81 に EP-02 のマッピングを追加する方法を示しています。 LCS によって展開されているすべての EP サーバーでこの手順を繰り返します。[![AddInternalURLs](./media/addinternalurls.png)](./media/addinternalurls.png)
5.  **公開 URL の編集**をクリックし、適切な値を入力します。
    -   **既定:** ロード バランサ URL + ポート 81 を使用します。
    -   **イントラネット:** EP-01 (SharePoint サーバー ファームの仮想マシン) とポート 81 を使用します。
    -   **インターネット:** 公的に登録された URL と ポート 81 を使用します。

    [![EditPublicZoneURLs](./media/editpubliczoneurls.png)](./media/editpubliczoneurls.png)
6.  レジストリ エディター (regedit) を開き、次のレジストリ キーを作成します。
    -   **パス:** HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Contro\\Lsa\\MSV1\_0
    -   **キーの詳細、キー値:** ロード バランサー名と完全修飾名

    [![EditMultiString](./media/editmultistring.png)](./media/editmultistring.png)
7.  **コマンド プロンプト** ウィンドウを開き、**ipconfig** コマンドを実行してローカル コンピューターの IP アドレスを取得します。
8.  メモ帳で C:\\Windows\\System32\\drivers\\etc\\hosts ファイルを開き、ロード バランサー名をローカル コンピューターの IP アドレスにマップします。 このマッピングは、ローカル EP サーバーが動作していることをテストするために使用されます。[![NotePad](./media/notepad.png)](./media/notepad.png)。
9.  LCS によって展開されているすべての EP サーバー上で手順 6 ～ 8 を繰り返します。
10. Dynamics インストーラー ユーザー サービス アカウントを使用して EP-02 サーバーにログオンします。
11. Dynamics インストーラが格納されているドライブに移動します (このドライブはたいていドライブ F です)。 **セットアップ** を右クリックし、**管理者として実行** をクリックして以下の手順に従います。
    1.  **Install Microsoft Dynamics AX コンポーネントのインストール**をクリックします。
    2.  **ようこそ**ページで、**次へ**をクリックします。
    3.  **コンポーネントの追加または変更**をクリックし、次に**次へ**をクリックします。
    4.  **Webサーバー コンポーネント** で、**エンタープライズ ポータル** チェック ボックスをオンにします。 **OK** をクリックして EP をインストールすることを同意し、**次へ**をクリックします。
    5.  検証エラーがないことを確認し、**次へ**をクリックします。
    6.  BC プロキシ ユーザーのパスワードを入力し、**次**を入力します。
    7.  **エンタープライズ ポータル用の Web サイトの構成**ページで、Web アプリケーションを選択します。
    8.  **Windows SharePoint Services を構成する**チェック ボックスをオンにします。
    9.  **インストールの完了後に IIS を再起動** チェック ボックスをオンにし、**次へ** をクリックします。

    [![EP 用の Web サイトの構成](./media/configure-a-web-site-for-ep.png)](./media/configure-a-web-site-for-ep.png)
12. インストールが完了するまで**次へ**をクリックします。
13. サーバー EP-03 から EP-0*N* で手順 10 ～ 12 を繰り返します。 (ファームがコンフィギュレーションされている単一のサーバーを除くすべての EP サーバーに EP を再インストールする必要があります。 ここでは、このサーバーは EP-01 です。)
14. 各 EP サーバー、EP-01 ～ EP-0*N* でこれらの手順に従います。
    1.  インターネット インフォメーション サービス (IIS) の管理コンソール (inetmgr) を開きます。
    2.  **サイト** &gt; **SharePoint – 81**に移動します。
    3.  右クリックして **バインドの編集** をクリックします。
    4.  バインディングをダブルクリックして、**Edit Site Binding** ダイアログ ボックスを開きます。
    5.   **ホスト名**フィールドに、ロード バランサー名を入力します。

    [![編集サイト バインディング](./media/edit-site-binding.png)](./media/edit-site-binding.png)
15. 各 EP サーバーで、これらの検証手順に従います。
    1.  **コマンド プロンプト** ウィンドウで、**iisreset** コマンドを実行します。
    2.  Internet Explorer を起動し、**http://AzureILB01:81/sites/DynamicsAx** に移動します。
    3.  ロール センター ページがエラーなく表示されることを確認します。

## <a name="configure-appfabric-cache"></a>AppFabric キャッシュのコンフィギュレーション。
1.  Dynamics インストール ユーザー サービス アカウントを使用して EP-01 サーバーにログオンします。
2.  Microsoft Windows PowerShell **コマンド プロンプト** ウィンドウを管理者として開きます。
3.  **Use-CacheCluster** コマンドを実行し、Windows PowerShell セッションのコンテキストを特定のキャッシュ クラスターに設定します。
4.  **New-Cache** コマンドを実行して新しい名前のキャッシュを作成します。 指定する名前をメモします。 (このキャッシュ名は、次の手順で入力します。)
5.  **Grant-CacheAllowedClientAccount** コマンドを実行し、.NET Business Connector プロキシを指定します。 (これは、EP アプリケーション プールで使用される口座です。)
6.  次のコマンドを実行します: **Set-CacheConfig -Secondaries 1**
    1.  キャッシュ名の入力を要求するメッセージが表示されたら、ステップ 4 から名前を入力します。
    2.  続行するかどうかを問われたときは、**Y** を入力します。

7.  手順 6 では、エラーが発生する場合は、次の順序でコマンドを実行します。
    1.  stop-cachecluster
    2.  Set-CacheConfig -Secondaries 1

8.  **Export-CacheClusterConfig** コマンドを実行してコンフィギュレーションをエキスポートします。 ファイルの名前を入力します。 このファイルは、ローカル コンピューターの任意の場所に保存できます。
9.  先ほど作成したファイルを開き、**&lt;advancedProperties&gt;** セクションに次のコンフィギュレーションを追加します。

        <transportProperties maxBufferSize="1000000000" />

10. **Import-CacheClusterConfig c:\\newConfig.xml** のコマンドを実行して、コンフィギュレーションをインポートします。続行するか確認された場合、**Y** を入力します。
11. **Start-CacheCluster** コマンドを実行してキャッシュを開始します。
12. メモ帳で web.config ファイル (C:\\inetpub\\wwwroot\\wss\\VirtualDirectories\\81\\web.config) を管理者モードで開きます。
13. **&lt;configSections&gt;** セクションを検索します。 次の**セクション**要素を追加します。

    ```
    <section name="dataCacheClient" type="Microsoft.ApplicationServer.Caching.DataCacheClientSection, Microsoft.ApplicationServer.Caching.Core, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" allowLocation="true" allowDefinition="Everywhere" />
    ```

14. **&lt;/configSections&gt;** タグの後の web.config ファイルに、次の **dataCacheClient** 要素を追加します。

    1.  “Host\_server\_name” のすべてのインスタンスを EP サーバーの名前に置き換えます。
    2.  "既定値" を **New-Cache** コマンドを実行したときに指定した名前に置き換えます。

    <!-- -->

        <!-- velocity -->
        <dataCacheClient dataCacheServiceAccountType="DomainAccount">
        <localCache isEnabled="false" />
        <hosts>
        <!--List of hosts -->
        <!-- Replace highlighted with your own EP server name -->
        <host name="EP-01" cachePort="22233" /> 
        <host name="EP-02" cachePort="22233" />  
        <host name="EP-03" cachePort="22233" /> 
        <host name="EP-0N" cachePort="22233" /> 
        </hosts>
        </dataCacheClient>
        <Microsoft.Dynamics>
        <AppFabricCaching CacheName="default" />
        </Microsoft.Dynamics>
        <!-- velocity -->

15. LCS によって展開されているすべての EP サーバー上で手順 12 ～ 14 を繰り返します。
16. EP-01 サーバーの、Windows PowerShell ウィンドウで、**stop-cachecluster** コマンドを実行します。
17. **start-cachecluster** コマンドを実行します。

## <a name="validate-appfabric"></a>AppFabric の検証
1.  EP サーバーのいずれかの Windows サービス コンソールで、AppFabric キャッシュ サービスが実行されていることを確認します。
2.  Windows PowerShell **コマンド プロンプト** ウィンドウを管理者として開きます。
3.  既定の **Get-CacheStatistics** コマンドを実行します。 結果にはすべてゼロが表示されます。
4.  **iisereset** コマンドを実行することで、EP サーバーで Web サービスを再起動します。
5.  EP を開き、**販売**に移動します。
6.  既定の **Get-CacheStatistics** コマンドをもう一度を実行し、キャッシュにより値が表示されることを確認します。 この結果は、キャッシュの配分が機能していることを示しています。

## <a name="clean-up"></a>クリーンアップ
すべての EP サーバーが独自のサーバー ファームに配置されているため、すべてのサーバーを単一のファームに結合させた後、他の EP サーバー ファーム用に作成されたデータベースを SQL から削除する必要があります。

-   Spfarm\_admincontent\_ep-02
-   Spfarm\_admincontent\_ep-03
-   …
-   Spfarm\_admincontent\_ep-0*N*
-   Spfarm\_config\_ep-02
-   Spfarm\_config\_ ep-03
-   …
-   Spfarm\_config\_ep-0*N*
-   WSS\_コンテンツ\_\*

特定のサイトの WSS \_コンテンツ\_\* データベースの名前を知るには、次の手順に従います。

1.  SharePoint サーバーの管理を起動します。
2.  **アプリケーション管理** &gt; **サイト コレクションの表示**に移動します。
3.  右上隅で、ポート 81 でホストされているサイトを選択します。 結果画面には、選択したサイトに使用されているデータベースが示されます。
4.  サイト 81 が作成されたサーバーで使用されていない WSS \_コンテンツ\_\* データベースをすべて削除します。 この場合は、EP-01 によって使用される WSS\_Content\_\* データベースを保持し、WSS\_Content\_\* で始まる名前の他のデータベースをすべて削除します。




