---
title: システム要件と前提条件
description: この記事では、財務と運用アプリで二重書き込みを有効にする前に設定する必要があるシステム要件と前提条件について説明します。
author: NHelgren
ms.date: 02/09/2022
ms.topic: article
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: nhelgren
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8f3b6e32ee7f25d659e4cf8b489b0cfe968b935
ms.sourcegitcommit: 43a0fb019bc67c00c39c2778343ba89924c3322c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2022
ms.locfileid: "9671441"
---
# <a name="system-requirements-and-prerequisites"></a>システム要件と前提条件

[!include [banner](../../includes/banner.md)]



## <a name="what-regions-are-available"></a>どの地域で使用できますか?

現時点では、次の地域におけるデュアル書き込みをサポートしています。

+ アジア
+ オーストラリア
+ ブラジル
+ カナダ
+ ヨーロッパ
+ フランス
+ ドイツ
+ インド
+ 日本
+ 南アフリカ
+ スイス
+ アラブ首長国連邦
+ イギリス
+ 米国


> [!NOTE]
> 現在、追加の地域をサポートする計画はありません。

## <a name="verify-requirements-and-grant-access"></a>要件を確認し、アクセスを許可する

二重書き込みを有効にする前に、次の手順に従って、最小システム要件を満たしていることを確認し、相互に接続する必要があるアプリへのアクセスを許可します。 二重書き込み正常性チェックは、財務と運用アプリ環境と Dataverse 環境をリンクする二重書き込みウィザードを完了すると、前提条件を検証します。

次の図に示すように、環境の設定時に **Dynamics 365 アプリ** を **はい** に設定する必要があります。 または、Dataverse に付属し、**Dynamics 365 アプリを有効化する** が **はい** に設定されている Customer Engagement アプリを選択することもできます。

:::image type="content" source="media/add_database_expanded2.png" alt-text="アプリの切り替えを有効にします。":::

1. プラットフォーム更新プログラムとアプリのバージョンを検証します。

    財務と運用アプリ環境で、プラットフォーム更新プログラム 33 (アプリ バージョン 10.0.9) 以降が実行されていることを確認します。

    **関連する正常性チェックの結果:**

    *アプリのバージョンが最新です*

    *二重書き込みは、プラットフォーム更新プログラム PU 33 (アプリ バージョン 10.0.9) 以上の財務と運用アプリ環境でサポートされています*

2. 二重書き込みコア ソリューションをインストールします。

    二重書き込みコア ソリューションには、テーブル マップのメタデータが含まれており、環境にインストールする必要があります。

    1. Power Apps の左ウィンドウで、**Solutions** を選択します。
    2. **AppSource を開く** を選択します。
    3. **二重書き込みコア** ソリューションを選択します。
    4. プロンプトに従ってソリューションをインポートします。

    ![二重書き込みコア ソリューションのインストール。](media/dual-write-core-solution.png)

    **関連する正常性チェックの結果:**

    *二重書き込みコア ソリューションが見つかりました*

    *二重書き込みコア ソリューションには、テーブル マップのメタデータが含まれており、環境にインストールする必要があります*

3. 財務と運用アプリに接続できるように Dataverse アクセスを許可します。

    1. 財務と運用アプリのインスタンスを開き、Azure Active Directory アプリケーションを検索して移動します。

    2. 新しいクライアント ID 行 **6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452** を追加するには、**新規** を選択します。 この行は、Dataverse から財務と運用アプリへの接続に使用されるアプリのアプリケーション ID です。
    3. 前の2つの手順を繰り返して、別のクライアント ID 行 **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** を追加します。

    完了したら、次の手順に従ってテーブルの一覧を更新します:

    1. **ワークスペース \> データ管理** に移動し、**データ エンティティ** タイルを選択して、エンティティ リストが入力されていることを確認します。
    2. **ワークスペース \> データ管理** に移動して、**フレームワーク パラメーター** タイルを選択します。 次に、**エンティティ設定** タブ (`https://<BaseFinanceandOperationsappsURL>/?cmp=USMF&mi=DM_DataManagementWorkspaceMenuItem&TableName=DMFDefinitionGroupEntity`) で、**エンティティ リストの更新** を選択します。

    **関連する正常性チェックの結果:**<br>
    *Dataverse は財務と運用アプリに接続可能*<br>
    *二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452 のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*

4. 財務と運用アプリに接続できるように Dataverse アクセスを許可します。 アプリケーション ID およびセキュリティ ロールに関する次の情報を使用して、[アプリケーション ユーザーの作成](/power-platform/admin/manage-application-users#create-an-application-user)の手順に従います。

    + **アプリケーション**: これらのアプリケーションにユーザーを追加します:

        + 00000015-0000-0000-c000-000000000000
        + 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b

    + **セキュリティ ロール**: コンフィギュレーション済み **セキュリティ ロール** を選択して、二重書き込みによって統合された各テーブルに対して **ユーザー** スコープのある **読み取り** 権限を付与します。

        >[!NOTE]
        > 会社と通貨為替テーブルは本質的にグローバルであり、すべての二重書き込みユーザーにはこれら 2 つのテーブルへの読み取りアクセスが必要です。
        > すべての二重書き込みユーザーを、**二重書き込みアプリ ユーザー** セキュリティ ロールに追加する必要があります。
        > 管理者以外のユーザーが二重書き込みが有効なテーブルに行を作成できるようにするには、ユーザーに **二重書き込みランタイム ユーザー** セキュリティ ロールを割り当てる必要があります。

        セキュリティ ロールの作成方法に関する説明については、[カスタム セキュリティ ロールの作成またはコンフィギュレーション](/power-platform/admin/database-security#create-or-configure-a-custom-security-role)を参照してください。

        > [!NOTE]
        > ルートの事業単位の既定チームは、二重書き込みを通して統合されたすべての行の既定の所有者になります。
        > そのチームにはセキュリティ ロールが割り当てられている必要があるので、ルートの事業単位のユーザーすべてがセキュリティ ロールを継承します。
        > 少なくとも、**事業単位のユーザーは、そのチームが所有しているすべての行に対する読み取りアクセスを持つ** ことになります。 これが必要な動作でない場合、ユーザーがルートの事業単位のメンバーでないことを確認します。

    **関連する正常性チェックの結果:**<br>
    *財務と運用アプリは Dataverse に接続可能*<br>
    *二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 00000015-0000-0000-c000-000000000000 のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*

    > [!NOTE]
    > レコードが財務と運用アプリで作成された場合、**所有者** フィールドは、一致するレコードが Dataverse に存在する場合でも、データが Dataverse に対してデュアル書き込みされます。 デュアル書き込みでは、ID **00000015-0000-0000-c000-000000000000 を持つアプリ ユーザーを使用して、** Dataverse、と通信して、**変更者** フィールドは、アプリケーション ユーザーに設定されます。

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

        ![Plugin Registration Tool の使用。](media/plugin-registration-tool.png)

    > [!NOTE]
    > 二重書き込みプラグイン アセンブリが見つからない場合は、二重書き込みコア ソリューションの最新バージョンをインポートします。

    **関連する正常性チェックの結果:**<br>
    *二重書き込み登録とランタイム プラグインが有効です*<br>
    *Dataverse で CRUD 操作を確実に行うには、二重書き込みプラグインを有効にする必要があります*

7. **二重書き込みアプリケーション オーケストレーション ソリューション** をインストールします。

    Power Apps の左ウィンドウで、**Solutions** を選択します。 **AppSource を開く** を選択し、パッケージ、具体的には、[二重書き込みアプリケーション コア ソリューション](https://appsource.microsoft.com/product/dynamics-365/mscrm.dwappcore?tab=Overview)、[二重書き込み人事ソリューション](https://appsource.microsoft.com/product/dynamics-365/mscrm.hcm_dualwrite?tab=Overview)、[二重書き込みサプライ チェーン ソリューション](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.dwscm?tab=Overview)、[二重書き込み財務ソリューション](https://appsource.microsoft.com/dynamics-365/mscrm.dwfne?tab=Overview)、[二重書き込みメモ ソリューション](https://appsource.microsoft.com/product/dynamics-365/mscrm.dwnotessln?tab=Overview)、[二重書き込み資産管理ソリューション](https://appsource.microsoft.com/product/dynamics-365/mscrm.dwassetmanagement?tab=Overview)、および[二重書き込み当事者およびグローバル アドレス帳ソリューション](https://appsource.microsoft.com/product/dynamics-365/mscrm.dwgabsln?tab=Overview)を検索します。 これらのソリューションは、次のようなマスター データ シナリオに対応しています
    
    + 顧客、製品、仕入先。
    + 見積もりから現金などのエンド ツー エンド プロセス フロー。
    + 価格、在庫、ATP 日付などのオンデマンド機能。
    + 元帳、税、支払条件、およびスケジュールなどの参照データ。

[前提条件の指示に従って](/dev-itpro/data-entities/dual-write/separated-solutions)、探しているソリューションを見つけてください。 ソリューションを選択し、プロンプトに従ってインポートします。 
     
二重書き込みフレームワークは拡張可能で、数回の追加クリックで顧客中心のビジネス データ交換にも対応します。
    
> [!NOTE]
> 二重書き込みウィザードを使用して環境をリンクする場合は、次の手順の一部として **ソリューションの適用** を選択する必要があります。 Power Apps ソリューション セクションでソリューション パッケージが作成されるまでに数分かかる場合があります。 表示されるまで待ってから、次のステップに進みます。

8. 見込顧客を現金化 (P2C) するソリューションをインストールします。

    P2C ソリューションは、二重書き込みと同時には機能しません。 したがって、P2C ソリューションをインストールしないでください。 既にインストールされている場合は、二重書き込みを有効にする前にアンインストールする必要があります。

9. サポートされているテナント コンフィギュレーションを指定します。

    財務と運用アプリと Dataverse が同じテナントにインストールされていることを確認します。 テナント間シナリオは現在サポートされていません。

    > [!NOTE]
    > バージョン 1.0.16.0 より前の二重書き込みコア ソリューションについては、変更および追加の手順の次のセクションを参照してください。 

**バージョン 1.0.16.0 より前の二重書き込みコア ソリューションのみ**

1. 上記の手順 3b で、新しいクライアント ID 行: **33976c19-1db5-4c02-810e-c243db79efde** (および 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452) を作成します。
2. テナントでアプリへの同意を追加します。

    1. 次のURLを開き、管理者の資格情報を使用してサインインします。 同意を求めるメッセージが表示されます。

        [https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent](https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent)

    2. **受け入れる** を選択します。

        **承認** を選択することで、テナントにアプリケーション ID **33976c19-1db5-4c02-810e-c243db79efde** を持つアプリのインストールに同意したことになります。 Dataverse には、財務と運用アプリと通信するためにこのアプリが必要です。

    
    **関連する正常性チェックの結果:**<br>
    *テナントのアプリ*<br>
    *必要な二重書き込みアプリケーションを、テナントにインストールする必要があります。<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 33976c19-1db5-4c02-810e-c243db79efde<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*

## <a name="next-steps"></a>次のステップ

[二重書き込みウィザードを使用して環境をリンクする](link-your-environment.md)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

