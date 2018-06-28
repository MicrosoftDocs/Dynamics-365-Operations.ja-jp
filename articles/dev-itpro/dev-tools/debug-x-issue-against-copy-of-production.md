---
title: "生産データベースのコピーに対する X++ のデバッグ"
description: "このトピックでは、実稼働環境で問題を調査できるように X++ デバッグを構成する方法について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 199063
ms.assetid: 3c0551f3-6c96-4518-8acd-82d4638f9323
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 20b6f72200eab79c9032bc3e9abd1e7f4ef49ce6
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="debug-x-against-a-copy-of-a-production-database"></a>生産データベースのコピーに対する X++ のデバッグ

[!include [banner](../includes/banner.md)]

このトピックでは、実稼働環境で問題を調査できるように X++ デバッグを構成する方法について説明します。 この手順では、生産データベースのコピーを作成し、コピーに接続するための開発環境をコンフィギュレーションします。

## <a name="solution-overview"></a>ソリューションの概要

実稼働環境で X++ のデバッグが必要な問題が発生したときは、システム管理者と開発者は連携して、デバッグを構成してから問題をデバッグします。 次の図は、プロセスの概要を表示します。

[![デバッグ プロセス](./media/debugxpp.jpg)](./media/debugxpp.jpg)

1. Microsoft Dynamics Lifecycle Services (LCS) では、システム管理者がデータベースのコピーをサンドボックス ユーザー受け入れテスト (UAT) 環境に接続するよう要求します。 (つまり、データベース更新を要求します。)
2. Microsoft Visual Studio Team Services (VSTS) では、開発者が実稼働環境で実行されている同じビルドにローカル コードを同期します。
3. Microsoft Azure SQL データベースのサンドボックス インスタンスでは、システム管理者が開発者に一時的な SQL サインインを作成します。 開発者は、サンドボックス データベースに接続するための環境を設定します。
4. 開発環境がサンドボックスのデータベースに接続できるように、ファイアウォールに例外が追加されています。
5. 開発者は問題をデバッグします。

> [!NOTE]
> デバッグが完了したら、システム管理者は、一時的なサインインをサンド ボックスの SQL データベースから削除できます。

## <a name="before-you-begin"></a>準備

実稼働環境で X++ デバッグ を構成する前に、次の点に注意してください。

- デバッグためにデータの破損が発生する可能性がありますので、実稼働環境を直接デバッグできません。 ただし、開発者は実行時に値を操作できます。 あるいは、独自のインスタンスでは、開発者はデータを変更するコード変更を行うことができます。

    > [!NOTE] 
    > デバッグに使用される開発環境は、サンドボックス環境と同じ LCS プロジェクトに存在する必要があります。 この要件は、サンドボックス データベースのセキュリティを強化するのに役立ちます。 既定では、サンドボックスと生産 SQL データベースの両方にファイアウォールの制限があります。 この制限により、これらの環境内のサーバーのみがデータベースに接続できます。 デバッグを有効にするため、開発環境がサンドボックスのデータベースに接続できるように、ファイアウォールに例外が追加されています。

- 環境の IP アドレスがサンドボックス データベースに接続できるようにするため、開発者環境への 1 回限りの手動変更が必要です。 IP アドレスを許可するために Microsoft サービス エンジニア リング チーム (DSE) に要求を送信します。
- デバッグにビルド環境を使用しないことをお勧めします。 それ以外の場合、コンピュータで開発者の活動が自動ビルド プロセスを中断するリスクがあります。

## <a name="solution-details"></a>ソリューションの詳細

実稼動環境で問題が発生する場合は、システム管理者は LCS にサインインして、データベースのコピーをサンド ボックス環境に追加するように要求できます。 データベースのコピーの実行中、システム管理者は開発者に問題について通知することができます。 開発者は、コードの正しいビルドに同期して、実稼働環境に合わせることができます。

1. Microsoft Visual Studio のソース管理エクスプローラーで、同期するブランチのルート ノードを右クリックしてから、**詳細** &gt; **特定のバージョンを取得**を選択します。
2. ダイアログ ボックスで、**Type=Label** を選択してから省略記号 (**...**) を選択します。
3. ダイアログ ボックスで**検索**を選択します。 ビルド サーバーからのすべてのビルドがリストに記載されます。
4. 実稼動環境に現在配置されているビルドを選択し、フル ビルドの実行を選択します。 データベースをコピーすると、システム管理者のみがサンド ボックス データベースにアクセスできます。 システム管理者は、次のタスクを完了する必要があります。

    - 従業員の給与など、サンドボックス データベースに不要なデータを削除します。
    - ユーザーとして、開発者を有効または追加にします。
    - 開発者が使用できる新しい SQL サインインを作成します。 このステップにより、システム管理者はサンドボックス環境のセキュリティを維持できます。 開発者は限られた時間だけ 1 つのデータベースにアクセスできます。 新しい SQL サインインを作成するには、次のコードを使用します。

        ```
        CREATE USER devtempuser WITH PASSWORD = ''
        EXEC sp_addrolemember 'db_owner', 'devtempuser'
        ```

次に、開発者は、Application Object Server (AOS) の web.config ファイルを編集します。

1. **J:\\AosService\\WebRoot\\web.config** に移動します。
2. 後で切り替えることができるように、元の web.config ファイルのコピーを保存します。
3. web.config ファイルの次のセクションを編集します。

    **変更前**

    ```
    <add key="DataAccess.Database" value="sandboxDatabaseName" />
    <add key="DataAccess.DbServer" value="sandboxDbServerName.database.windows.net" />
    <add key="DataAccess.SqlPwd" value="password" />
    <add key="DataAccess.SqlUser" value="devtempuser" />
    ```

    **変更後**

    ```
    <add key="DataAccess.Database" value="TariqRTW_axdb_dd78f8aadbc6c481" />
    <add key="DataAccess.DbServer" value="vyxx2dflyo.database.windows.net" />
    <add key="DataAccess.SqlPwd" value="P@ssw0rd" />
    <add key="DataAccess.SqlUser" value="devtempuser" />
    ```

4. 問題をデバッグします。

開発者が終了すると、 システム管理者はサンドボックス データベースから devtempuser を削除できます。 このステップにより、開発者はサンドボックス データベースに永続的にアクセスできなくなります。

