---
title: システム要件と前提条件
description: このトピックでは、Finance and Operations アプリで二重書き込みを有効にする前に設定する必要があるシステム要件と前提条件について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a022230c65b4c05ff6aeb4a6a50f28def17ae01c
ms.sourcegitcommit: e69cfc74e9dbce64ae0e1ab7cd441e5ae6efd4c9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/08/2020
ms.locfileid: "3353676"
---
# <a name="system-requirements-and-prerequisites"></a>システム要件と前提条件

[!include [banner](../../includes/banner.md)]



## <a name="verify-requirements-and-grant-access"></a>要件を確認し、アクセスを許可する

二重書き込みを有効にする前に、次の手順に従って、最小システム要件を満たしていることを確認し、相互に接続する必要があるアプリへのアクセスを許可します。 二重書き込み正常性チェックは、Finance and Operations アプリ環境と Common Data Service 環境をリンクする二重書き込みウィザードを完了すると、前提条件を検証します。

1. プラットフォーム更新プログラムとアプリのバージョンを検証します。

    Finance and Operations アプリ環境で、Platform update 33 (アプリ バージョン 10.0.9) 以降が実行されていることを確認します。

    **関連する正常性チェックの結果:**

    *アプリのバージョンが最新です*

    *二重書き込みは、Platform Update PU 33 (アプリ バージョン 10.0.9) 以上の Finance and Operationsアプリ環境でサポートされています*

2. 二重書き込みコア ソリューションをインストールします。

    二重書き込みコア ソリューションには、エンティティ マップのメタデータが含まれており、環境にインストールする必要があります。

    1. Power Apps の左ウィンドウで、**ソリューション** を選択します。
    2. **AppSource を開く** を選択します。
    3. **二重書き込みコア** ソリューションを選択します。
    4. プロンプトに従ってソリューションをインポートします。

    ![二重書き込みコア ソリューションのインストール](media/dual-write-core-solution.png)

    **関連する正常性チェックの結果:**

    *二重書き込みコア ソリューションが見つかりました*

    *二重書き込みコア ソリューションには、エンティティ マップのメタデータが含まれており、環境にインストールする必要があります*

3. Finance and Operations アプリに接続できるように Common Data Service アクセスを許可します。

    1. 次の URL を使用して Finance and Operations アプリのインスタンスを開きます。 **\<BaseFinanceandOperationsappsURL\>** をインスタンスに置き換えます。

        `https://<BaseFinanceandOperationsappsURL>/?cmp=DAT&mi=SysAADClientTable`

    2. 新しいクライアント ID レコード: **33976c19-1db5-4c02-810e-c243db79efde** を追加するには、**新規** を選択します。 このレコードは、Common Data Service から Finance and Operations アプリへの接続に使用されるアプリのアプリケーション ID です。
    3. 前の2つの手順を繰り返して、別のクライアント ID レコード: **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** を追加します。

        ![別のクライアント ID レコードの追加](media/another-client-id-record.png)

    完了したら、次の手順に従ってエンティティの一覧を更新します:

    1. **ワークスペース \> データ管理** に移動し、**データ エンティティ** タイルを選択して、エンティティ リストが入力されていることを確認します。
    2. **ワークスペース \> データ管理** に移動して、**フレームワーク パラメーター** タイルを選択します。 次に、**エンティティ** タブ (`https://<BaseFinanceandOperationsappsURL>/?cmp=USMF&mi=DM_DataManagementWorkspaceMenuItem&TableName=DMFDefinitionGroupEntity`) で、**エンティティ リストの更新** を選択します。

    **関連する正常性チェックの結果:**

    *Common Data Service は Finance and Operations アプリに接続できます*

    *二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID 33976c19-1db5-4c02-810e-c243db79efde が存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b が存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 33976c19-1db5-4c02-810e-c243db79efde のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*

4. Common Data Service に接続できるように Finance and Operations アプリへのアクセスを許可します。

    1. Power Apps で、右上隅にある **設定** ボタン (ギヤ記号) を選択し、**詳細設定 \> セキュリティ** に移動して、**ユーザー** を選択します。

        ![ユーザー](media/selecting-users.png)

    2. ドロップダウン メニューを使用して、ビューを **有効なユーザー** から **アプリケーション ユーザー** に変更します。

        ![アプリケーション ユーザー ビューへの切り替え](media/selecting-application-users.png)

    3. 新しいユーザーを作成し、**ユーザー** メニューで **アプリケーション ユーザー** を選択します。

        ![アプリケーション ユーザーへの切り替え](media/create-new-user.png)

    4. **アプリケーション ID** フィールドに、**00000015-0000-0000-c000-000000000000** と入力します。 このアプリケーション ID は Finance and Operations アプリ用で、アプリを Common Data Service に接続できるようにします。 完了したら、プロンプトに従って他のフィールドに入力し、ユーザー アカウントを保存します。

        ![アプリケーション ID の入力](media/add-application-id.png)

    5. 基本電子メール アドレスを入力します。
    6. **ロールの管理** を選択し、**ユーザー ロールの管理** ダイアログ ボックスで **システム管理者** チェック ボックスを選択して、選択したアプリケーション ユーザーにシステム管理者権限を付与します。

        ![システム管理者ロールの割り当て](media/manage-user-roles.png)

    7. **Dynamics 365 \> 設定 \> セキュリティ**に移動し、**チーム** を選択して、**すべてのチーム** にビューを変更します。
    8. ルートの事業単位/組織を選択して、**ロールの管理** を選択し、**チームロールの管理** ダイアログ ボックスで **システム管理者** チェック ボックスを選択して、必要なシステム管理者権限を割り当てます。

        ![システム管理者ロールの割り当て](media/assign-system-admin-role.png)

    9. アプリケーションID **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** について前の 5 つの手順を繰り返します。

        ![アプリケーション ID の割り当て](media/assign-application-id.png)

    **関連する正常性チェックの結果:**

    *Finance and Operations アプリは Common Data Service に接続できます*

    *二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 00000015-0000-0000-c000-000000000000 のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*

5. テナントでアプリへの同意をします。

    必要なアプリの同意をしてください。

    1. 次のURLを開き、管理者の資格情報を使用してサインインします。 同意を求めるメッセージが表示されます。

        [https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent](https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent)

    2. **受け入れる** を選択します。

        **承認** を選択することで、テナントにアプリケーション ID **33976c19-1db5-4c02-810e-c243db79efde** を持つアプリのインストールに同意したことになります。 Common Data Service は、Finance and Operations アプリと通信するためにこのアプリが必要です。

    3. アプリケーション ID **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** について前の 2 つの手順を繰り返します。

    **関連する正常性チェックの結果:**

    *テナントのアプリ*

    *必要な二重書き込みアプリケーションを、テナントにインストールする必要があります。<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 33976c19-1db5-4c02-810e-c243db79efde<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*

6. 二重書き込みプラグインが有効になっていることを確認します。

    二重書き込みコア ソリューションのインストール プロセスの一部としてプラグインを有効にする必要があるため、通常この手順は必要ありません。 ただし、正常性チェックが失敗した場合は、次の手順に従って手動で二重書き込みプラグインを有効にします:

    1. [Plugin Registration Tool](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool) をダウンロードします。

        Plugin Registration Tool には、二重書き込みに関連付けられている 2 つのプラグイン アセンブリが必要です: **DualWriteRegistration.Plugins** と **DualWriteRuntime.Plugins**。 これらのアセンブリには、二重書き込みを使用する前に、順番に有効にする必要があるプラグイン ステップがあります。 プラグイン ステップを表示するには、プラグイン アセンブリとそのプラグイン タイプを展開します。 二重書き込みプラグイン アセンブリに属するすべてのステップを有効にする必要があります。

    2. ステップを有効にするには、ステップを選択したまま (または右クリック) にし、**有効** を選択します。 **有効** オプションがなく、**無効** オプションのみの場合、ステップは既に有効になっており、変更する必要はありません。

        ![Plugin Registration Tool の使用](media/plugin-registration-tool.png)

    > [!NOTE]
    > 二重書き込みプラグイン アセンブリが見つからない場合は、二重書き込みコア ソリューションの最新バージョンをインポートします。

    **関連する正常性チェックの結果:**

    *二重書き込み登録とランタイム プラグインが有効です*

    *Common Data Service で CRUD 操作を確実に行うには、二重書き込みプラグインを有効にする必要があります*

7. 見込顧客を現金化 (P2C) するソリューションをインストールします。

    P2C ソリューションは、二重書き込みと同時には機能しません。 したがって、P2C ソリューションをインストールしないでください。 既にインストールされている場合は、二重書き込みを有効にする前にアンインストールする必要があります。

8. サポートされているテナント コンフィギュレーションを指定します。

    Finance and Operations アプリと Common Data Service が同じテナントにインストールされていることを確認します。 テナント間シナリオは現在サポートされていません。


## <a name="next-steps"></a>次のステップ

[二重書き込みウィザードを使用して環境をリンクする](link-your-environment.md)
