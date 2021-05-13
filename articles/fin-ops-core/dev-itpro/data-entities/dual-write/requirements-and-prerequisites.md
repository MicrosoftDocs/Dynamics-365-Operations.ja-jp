---
title: システム要件と前提条件
description: このトピックでは、Finance and Operations アプリで二重書き込みを有効にする前に設定する必要があるシステム要件と前提条件について説明します。
author: sabinn-msft
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b60665c5cfa1589853b48f6727b7972c2036191a
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941123"
---
# <a name="system-requirements-and-prerequisites"></a>システム要件と前提条件

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


## <a name="what-regions-are-available"></a>どの地域で使用できますか?

現時点では、次の地域におけるデュアル書き込みをサポートしています。
    
   + アジア
   + オーストラリア
   + カナダ
   + ヨーロッパ
   + インド
   + 日本
   + 南アフリカ
   + 英国
   + 米国


## <a name="verify-requirements-and-grant-access"></a>要件を確認し、アクセスを許可する

二重書き込みを有効にする前に、次の手順に従って、最小システム要件を満たしていることを確認し、相互に接続する必要があるアプリへのアクセスを許可します。 二重書き込み正常性チェックは、Finance and Operations アプリ環境と Dataverse 環境をリンクする二重書き込みウィザードを完了すると、前提条件を検証します。

次の図に示すように、環境の設定時に **Dynamics 365 アプリ** を **はい** に設定する必要があります。 または、Dataverse に付属している Dynamics 365 環境で、すでに **Dynamics 365 アプリを有効化する** が **はい** に設定されているモデル駆動型アプリを選択することもできます。

:::image type="content" source="media/add_database.png" alt-text="アプリ切り替えの有効化" lightbox="media/add_database_expanded.png":::

1. プラットフォーム更新プログラムとアプリのバージョンを検証します。

    Finance and Operations アプリ環境で、Platform update 33 (アプリ バージョン 10.0.9) 以降が実行されていることを確認します。

    **関連する正常性チェックの結果:**

    *アプリのバージョンが最新です*

    *二重書き込みは、Platform Update PU 33 (アプリ バージョン 10.0.9) 以上の Finance and Operations アプリ環境でサポートされています*

2. 二重書き込みコア ソリューションをインストールします。

    二重書き込みコア ソリューションには、テーブル マップのメタデータが含まれており、環境にインストールする必要があります。

    1. Power Apps の左ウィンドウで、**Solutions** を選択します。
    2. **AppSource を開く** を選択します。
    3. **二重書き込みコア** ソリューションを選択します。
    4. プロンプトに従ってソリューションをインポートします。

    ![二重書き込みコア ソリューションのインストール](media/dual-write-core-solution.png)

    **関連する正常性チェックの結果:**

    *二重書き込みコア ソリューションが見つかりました*

    *二重書き込みコア ソリューションには、テーブル マップのメタデータが含まれており、環境にインストールする必要があります*

3. Finance and Operations アプリに接続できるように Dataverse アクセスを許可します。

    1. Finance and Operations アプリのインスタンスを開き 、Azure Active Directory アプリケーションを検索して移動します。

    2. 新しいクライアント ID 行 **6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452** を追加するには、**新規** を選択します。 この行は、Dataverse から Finance and Operations アプリへの接続に使用されるアプリのアプリケーション ID です。
    3. 前の2つの手順を繰り返して、別のクライアント ID 行 **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** を追加します。

    完了したら、次の手順に従ってテーブルの一覧を更新します:

    1. **ワークスペース \> データ管理** に移動し、**データ テーブル** タイルを選択して、テーブル リストが入力されていることを確認します。
    2. **ワークスペース \> データ管理** に移動して、**フレームワーク パラメーター** タイルを選択します。 次に、**エンティティ** タブ (`https://<BaseFinanceandOperationsappsURL>/?cmp=USMF&mi=DM_DataManagementWorkspaceMenuItem&TableName=DMFDefinitionGroupEntity`) で、**テーブル リストの更新** を選択します。

    **関連する正常性チェックの結果:**<br>
    *Dataverse は Finance and Operations アプリに接続できます*<br>
    *二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452 のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*

4. Dataverse に接続できるように Finance and Operations アプリへのアクセスを許可します。

    1. Power Apps で、右上隅にある **設定** ボタン (ギヤ記号) を選択し、**詳細設定 \> セキュリティ** に移動して、**ユーザー** を選択します。

        ![ユーザー](media/selecting-users.png)

    2. ドロップダウン メニューを使用して、ビューを **有効なユーザー** から **アプリケーション ユーザー** に変更します。

        ![アプリケーション ユーザー ビューへの切り替え](media/selecting-application-users.png)

    3. 新しいユーザーを作成し、**ユーザー** メニューで **アプリケーション ユーザー** を選択します。

        ![アプリケーション ユーザーへの切り替え](media/create-new-user.png)

    4. **アプリケーション ID** 列に、**00000015-0000-0000-c000-000000000000** と入力します。 このアプリケーション ID は Finance and Operations アプリ用で、アプリを Dataverse に接続できるようにします。 完了したら、プロンプトに従って他の列に入力し、ユーザー アカウントを保存します。

        ![アプリケーション ID の入力](media/add-application-id.png)

    5. 基本電子メール アドレスを入力します。
    6. **ロールの管理** を選択し、**ユーザー ロールの管理** ダイアログ ボックスで **システム管理者** チェック ボックスを選択して、選択したアプリケーション ユーザーにシステム管理者権限を付与します。

        ![システム管理者ロールの割り当て](media/manage-user-roles.png)

    7. **Dynamics 365 \> 設定 \> セキュリティ** に移動し、**チーム** を選択して、**すべての所有者チーム** にビューを変更します。
    8. **ルートの事業単位の既定のチーム** を選択し、**ロールの管理** を選択して、**チーム ロールの管理** ダイアログ ボックスで事前にコンフィギュレーションされた **セキュリティ ロール** を選択し、二重書き込みを通して統合された各テーブルの **ユーザー** スコープに対して **読み取り** 権限を付与します。 
    
      セキュリティ ロールの作成方法に関する説明については、[カスタム セキュリティ ロールの作成またはコンフィギュレーション](/power-platform/admin/database-security#create-or-configure-a-custom-security-role)を参照してください。
      
      > [!NOTE]
      > ルートの事業単位の既定チームは、二重書き込みを通して統合されたすべての行の既定の所有者になります。
      > そのチームにはセキュリティ ロールが割り当てられている必要があるので、ルートの事業単位のユーザーすべてがセキュリティ ロールを継承します。
      > 少なくとも、**事業単位のユーザーは、そのチームが所有しているすべての行に対する読み取りアクセスを持つ** ことになります。 これが必要な動作でない場合、ユーザーがルートの事業単位のメンバーでないことを確認します。

    9. アプリケーションID **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** について前の 5 つの手順を繰り返します。

        ![アプリケーション ID の割り当て](media/assign-application-id.png)

    **関連する正常性チェックの結果:**<br>
    *Finance and Operations アプリは Dataverse に接続できます*<br>
    *二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 00000015-0000-0000-c000-000000000000 のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*

5. テナントでアプリへの同意をします。
   バージョン 1.0.16.0 以上の二重書き込みコア ソリューションの場合、この手順は不要になりました。
        
    **関連する正常性チェックの結果:**<br>
    *テナントのアプリ*<br>
    *必要な二重書き込みアプリケーションを、テナントにインストールする必要があります。<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*

6. 二重書き込みプラグインが有効になっていることを確認します。

    二重書き込みコア ソリューションのインストール プロセスの一部としてプラグインを有効にする必要があるため、通常この手順は必要ありません。 ただし、正常性チェックが失敗した場合は、次の手順に従って手動で二重書き込みプラグインを有効にします:

    1. [Plugin Registration Tool](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool) をダウンロードします。

        Plugin Registration Tool には、二重書き込みに関連付けられている 2 つのプラグイン アセンブリが必要です: **DualWriteRegistration.Plugins** と **DualWriteRuntime.Plugins**。 これらのアセンブリには、二重書き込みを使用する前に、順番に有効にする必要があるプラグイン ステップがあります。 プラグイン ステップを表示するには、プラグイン アセンブリとそのプラグイン タイプを展開します。 二重書き込みプラグイン アセンブリに属するすべてのステップを有効にする必要があります。

    2. ステップを有効にするには、ステップを選択したまま (または右クリック) にし、**有効** を選択します。 **有効** オプションがなく、**無効** オプションのみの場合、ステップは既に有効になっており、変更する必要はありません。

        ![Plugin Registration Tool の使用](media/plugin-registration-tool.png)

    > [!NOTE]
    > 二重書き込みプラグイン アセンブリが見つからない場合は、二重書き込みコア ソリューションの最新バージョンをインポートします。

    **関連する正常性チェックの結果:**<br>
    *二重書き込み登録とランタイム プラグインが有効です*<br>
    *Dataverse で CRUD 操作を確実に行うには、二重書き込みプラグインを有効にする必要があります*

7. **二重書き込みアプリケーション オーケストレーション ソリューション** マップ ソリューションをインストールします。

    Power Apps の左ウィンドウで、**ソリューション** を選択します。 **AppSource を開く** を選択し、**二重書き込みアプリケーション オーケストレーション ソリューション** という名前のソリューションを検索します。 ソリューションを選択し、プロンプトに従ってインポートします。 インストール後、**ソリューション** の下に新しいソリューションがいくつか表示されます。 詳細については、[ソリューションの概要](/powerapps/maker/common-data-service/solutions-overview)を参照してください。 
 
    二重書き込みコア ソリューションには、テーブル マップのメタデータが含まれていますが、二重書き込みアプリケーション オーケストレーション ソリューションには、次の追加のマスタ データ シナリオが含まれます:
    
    + 顧客、製品、仕入先。
    + 見込顧客から現金などのエンド ツー エンド プロセス フロー。
    + 価格設定などのオンデマンド機能。
    + 元帳、税、支払条件、およびスケジュールの参照データ。 
    
    二重の書き込みは今後も拡大し続け、関係者、プロジェクト、手持在庫など、より多くのシナリオをサポートします。 フレームワークは拡張可能で、数回の追加クリックで顧客中心のビジネス データ交換にも対応します。
    
    > [!NOTE]
    > 二重書き込みウィザードを使用して環境をリンクする場合は、次の手順の一部として **ソリューションの適用** を選択する必要があります。 Power Apps ソリューション セクションでソリューション パッケージが作成されるまでに数分かかる場合があります。 表示されるまで待ってから、次のステップに進みます。

8. 見込顧客を現金化 (P2C) するソリューションをインストールします。

    P2C ソリューションは、二重書き込みと同時には機能しません。 したがって、P2C ソリューションをインストールしないでください。 既にインストールされている場合は、二重書き込みを有効にする前にアンインストールする必要があります。

9. サポートされているテナント コンフィギュレーションを指定します。

    Finance and Operations アプリと Dataverse が同じテナントにインストールされていることを確認します。 テナント間シナリオは現在サポートされていません。

    > [!NOTE]
    > バージョン 1.0.16.0 より前の二重書き込みコア ソリューションについては、変更および追加の手順の次のセクションを参照してください。 

**バージョン 1.0.16.0 より前の二重書き込みコア ソリューションのみ**

1. 上記の手順 3b で、新しいクライアント ID 行 **33976c19-1db5-4c02-810e-c243db79efde** (および 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452) を作成します。
2. テナントでアプリへの同意を追加します。

    1. 次のURLを開き、管理者の資格情報を使用してサインインします。 同意を求めるメッセージが表示されます。

        [https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent](https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent)

    2. **受け入れる** を選択します。

        **承認** を選択することで、テナントにアプリケーション ID **33976c19-1db5-4c02-810e-c243db79efde** を持つアプリのインストールに同意したことになります。 Dataverse は、Finance and Operations アプリと通信するためにこのアプリが必要です。

    
    **関連する正常性チェックの結果:**<br>
    *テナントのアプリ*<br>
    *必要な二重書き込みアプリケーションを、テナントにインストールする必要があります。<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 33976c19-1db5-4c02-810e-c243db79efde<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*

## <a name="next-steps"></a>次のステップ

[二重書き込みウィザードを使用して環境をリンクする](link-your-environment.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]