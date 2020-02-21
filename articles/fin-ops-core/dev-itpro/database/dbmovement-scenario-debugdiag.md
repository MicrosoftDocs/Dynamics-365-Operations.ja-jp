---
title: 生産データベースのコピーのデバッグ
description: このトピックでは、Finance and Operations のデバッグや診断シナリオについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 4e5238ede5477e29df2ce92d106de9945c90ea2d
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029434"
---
# <a name="debug-a-copy-of-the-production-database"></a>生産データベースのコピーのデバッグ

[!include [banner](../includes/banner.md)]

データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。 このチュートリアルでは、生産データの最新のコピーの特定のデータとトランザクションをデバッグする方法を示します。

このチュートリアルでは、次の方法について説明します。

> [!div class="checklist"]
> * ユーザー受け入れテスト (UAT) 環境を更新します。
> * 承認済リスト (「ホワイトリスト」) には、開発者の環境の IP アドレスを追加します。
> * UAT データベースに接続できるように、開発者環境を更新します。
> * ブレークポイントを設定し、データのデバッグを開始します。

このシナリオの例として、既に稼働している顧客が、開発環境から生産トランザクションの最新のコピーをデバッグしようとしているということがあります。 これにより、顧客は止まっている特定のトランザクションをデバッグしたり、または実際的なデータセットを使用して新しい機能とレポートを開発できます。

## <a name="prerequisites"></a>必要条件

更新操作を行うには、実稼働環境を配置している必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。 このチュートリアルを完了するには、開発者環境が配置されている必要があります。

> [!IMPORTANT]
> デバッグの場合、UAT 環境で使用できるのと同じコードとビジネス ロジックを実行する DevTest 環境を使用することを強くお勧めします。 バージョン コントロールで複数のブランチを使用する場合は、最新の UAT または生産トランザクションをデバッグするために使用される DevTest 環境を、UAT のパッケージを構築するために使用する同じブランチに接続した後、生産に使用することをお勧めします。 これにより、互換性のあるスキーマになるため、DevTest 環境と UAT データベースの間でデータベースの同期を実行する必要がありません。 これまで、このような環境は、修正プログラム/サポート環境と呼ばれてきました。通常のコード プロモーション パス外となっているためです。

## <a name="refresh-the-uat-environment"></a>UAT 環境を更新 

この更新操作は、生産データベースの最新のコピーで UAT 環境を上書きします。 この手順を完了するには、[トレーニング目的での更新](dbmovement-scenario-general-refresh.md)の手順に従います。

## <a name="add-your-ip-address-to-a-whitelist"></a>IP アドレスをホワイトリストに追加します。

既定では、すべてのサンドボックス標準受け入れテスト環境で Microsoft Azure データベース プラットフォームとして SQL データベースを使用します。 このような環境のデータベースは、最初に配置された Application Object Server (AOS) へのアクセスを制限するファイアウォールで保護されています。

ただし、UAT データベースに直接開発環境 (クラウドにホストされているか、または Microsoft が管理) を接続できるように、例外を作ることができます。 開発者環境を UAT データベースに直接接続するには、開発者仮想マシン (VM) で IP アドレスを取得する必要があります。

サンドボックス AOS VM で、Microsoft SQL Server Management Studio (SSMS) を開き、Microsoft Dynamics Lifecycle Services (LCS) で環境の詳細のページから使用できる情報を使用してデータベースに接続します。 ユーザー名レコードで **axdbadmin** を検索し、**{sqlServer\\sqlDatabase}** 形式のサーバーとデータベースに注目します。

SSMS で、SQL Server、ユーザー名、およびパスワードを入力します。 **接続のプロパティ** タブで、LCS の **axdbadmin** レコードから明示的にデータベース名を入力します。

接続したら、データベースに対してクエリを開き、次の Transact-SQL (T-SQL) コマンドで IP アドレスを入力します。

```sql
-- Create database-level firewall setting for IP a.b.c.d 
EXECUTE sp_set_database_firewall_rule N'Debugging rule for DevTest environment', 'a.b.c.d', 'a.b.c.d'; 
```

開発環境に戻って SSMS を開き、UAT データベースに対して同じ **axdbadmin** 資格情報を使用して接続を試みます。 次の手順に進む前に接続できることを確認します。

> [!NOTE]
> 更新を実行するたびにファイアウォール ホワイトリストはリセットされます。 将来の必要なときに、このデータベースに DevTest 環境を追加する必要があります。

## <a name="update-a-onebox-devtest-environment-to-connect-to-the-uat-database"></a>UAT データベースに接続する OneBox DevTest 環境を更新する

開発者環境で、データベース接続を変更するために web.config ファイルを更新する必要があります。 この手順を使用すると、データベースに対して UAT からコンフィギュレーションされたローカル コードとバイナリを実行できます。

サービス ドライブで **AoSService\\WebRoot** ディレクトリに移動します。 (通常は、サービス ドライブはドライブ J または K です)。web.config という名前のファイルを検索し、*バックアップを作成*します。 次に、メモ帳などのエディターで **web.config** ファイルを開き、次の構成を見つけます。

- DataAccess.Database
- DataAccess.DBServer
- DataAccess.SqlPwd
- DataAccess.SqlUser

LCS で UAT 環境の環境詳細ページから値を使用するように、これらのコンフィギュレーションを更新します。

```xml
<add key="DataAccess.Database" value="<example_axdb_fromAzure>" />
<add key="DataAccess.DbServer" value="<example_axdb_server.database.windows.net>" />
<add key="DataAccess.SqlPwd" value="<axdbadmin_password_from_LCS>" />
<add key="DataAccess.SqlUser" value="axdbadmin" />
```
ファイル保存します。 クラウドにホストされている環境で操作している場合は、IISRESET を実行します。 Microsoft が管理する開発者向けのコンピューターを使用していてアクセス許可が制限されている場合、必ず Microsoft Visual Studio を閉じてください。

最後に、Web ブラウザーを開き、DevTest 環境の URL に移動して、UAT データベースからデータを取得することを確認します。

## <a name="debug-transactions-in-the-devtest-environment"></a>DevTest 環境でトランザクションをデバッグする

これで、環境が正しく再構成され、Visual Studio を開いてニーズを最も満たすアプリケーション コードでブレークポイントを設定できるようになりました。 UAT 環境のユーザーは、DevTest 環境でのデバッグ中に影響を受けないことに注意してください。

## <a name="best-practices"></a>ベスト プラクティス

デバッグ エクスペリエンスがすばやく、信頼性の高いものになり、組織内の他のユーザーに影響しないことを保証するのに役立ついくつかの一般的なベスト プラクティスを以下に示します。

- DevTest 環境のコードとバイナリのバージョンが、UAT 環境のバージョンと正確に一致することを確認します。 展開用のパッケージを作成したのと同じブランチに DevTest 環境を接続します。 または、リリースされている最新のカスタマイズで最新の状態になっている "HotfixSupport" ブランチに接続します。
- Visual Studio からデータベースの同期を実行しないでください。 そうしないと、UAT データベース内のスキーマの可用性に影響を与え、UAT 環境のユーザーに影響を与える可能性があります。
