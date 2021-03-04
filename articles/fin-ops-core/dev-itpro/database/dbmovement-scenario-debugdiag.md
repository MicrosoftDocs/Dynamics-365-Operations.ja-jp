---
title: 生産データベースのコピーのデバッグ
description: このトピックでは、Finance and Operations のデバッグや診断シナリオについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: e89dfaf7997379eb8419f0dd03ba21221e99a1f1
ms.sourcegitcommit: 9f9045ad1fc4062a5d112cf312ba691c632aec96
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/26/2021
ms.locfileid: "5068486"
---
# <a name="debug-a-copy-of-the-production-database"></a>生産データベースのコピーのデバッグ

[!include [banner](../includes/banner.md)]

データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。 このチュートリアルでは、生産データの最新のコピーの特定のデータとトランザクションをデバッグする方法を示します。

このチュートリアルでは、次の方法について説明します。

> [!div class="checklist"]
> * ユーザー受け入れテスト (UAT) 環境を更新します。
> * 承認済リスト (セーフ リスト) に開発者環境の IP アドレスを追加します。
> * UAT データベースに接続できるように、開発者環境を更新します。
> * ブレークポイントを設定し、データのデバッグを開始します。

このシナリオの例として、既に稼働している顧客が、開発環境から生産トランザクションの最新のコピーをデバッグしようとしていることがあります。 これにより、顧客は止まっている特定のトランザクションをデバッグしたり、または実際的なデータセットを使用して新しい機能とレポートを開発できます。

## <a name="prerequisites"></a>必要条件

更新操作を行うには、実稼働環境を配置している必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。 このチュートリアルを完了するには、開発者環境が配置されている必要があります。

> [!IMPORTANT]
> デバッグの場合、UAT 環境で使用できるのと同じコードとビジネス ロジックを実行する DevTest 環境を使用することを強くお勧めします。 バージョン コントロールで複数のブランチを使用する場合は、最新の UAT または生産トランザクションをデバッグするために使用される DevTest 環境を、UAT のパッケージを構築するために使用する同じブランチに接続した後、生産に使用することをお勧めします。 これにより、互換性のあるスキーマになるため、DevTest 環境と UAT データベースの間でデータベースの同期を実行する必要がありません。 これまで、このような環境は、修正プログラム/サポート環境と呼ばれてきました。通常のコード プロモーション パス外となっているためです。

## <a name="refresh-the-uat-environment"></a>UAT 環境を更新 

この更新操作は、生産データベースの最新のコピーで UAT 環境を上書きします。 この手順を完了するには、[トレーニング目的での更新](dbmovement-scenario-general-refresh.md)の手順に従います。

## <a name="enable-database-access"></a>データベース アクセスの有効化

既定では、すべてのサンドボックス標準受け入れテスト環境で Microsoft Azure データベース プラットフォームとして SQL データベースを使用します。 このような環境のデータベースは、最初に配置された Application Object Server (AOS) へのアクセスを制限するファイアウォールで保護されています。

データベースに接続するには、[ジャストインタイム アクセスの有効化](database-just-in-time-JIT-access.md) の手順に従います。

> [!NOTE]
> 更新を実行するたびにファイアウォールのセーフ リストはリセットされます。 将来の必要なときに、このデータベースに DevTest 環境を追加する必要があります。

## <a name="update-a-onebox-devtest-environment-to-connect-to-the-uat-database"></a>UAT データベースに接続する OneBox DevTest 環境を更新する

開発者環境で、データベース接続を変更するために web.config ファイルを更新する必要があります。 この手順を使用すると、データベースに対して UAT からコンフィギュレーションされたローカル コードとバイナリを実行できます。

サービス ドライブで **AoSService\\WebRoot** ディレクトリに移動します。 (通常は、サービス ドライブはドライブ J または K です)。web.config という名前のファイルを検索し、*バックアップを作成* します。 次に、メモ帳などのエディターで **web.config** ファイルを開き、次の構成を見つけます。

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

### <a name="debugging-batch"></a>バッチのデバッグ

バッチ・ジョブをデバッグする必要があるシナリオでは、デバッグ DevTest マシン上で、Visual Studio からデバッガーを関連付けるオプションとして表示される前にバッチ・サービスを再起動する必要があります。 さらに、この DevTest マシンを独自のバッチ グループに分離して、デバッグするジョブが DevTest マシンで実行されるようにしておくと便利です。

## <a name="best-practices"></a>ベスト プラクティス

デバッグ エクスペリエンスがすばやく、信頼性の高いものになり、組織内の他のユーザーに影響しないことを保証するのに役立ついくつかの一般的なベスト プラクティスを以下に示します。

- DevTest 環境のコードとバイナリのバージョンが、UAT 環境のバージョンと正確に一致することを確認します。 展開用のパッケージを作成したのと同じブランチに DevTest 環境を接続します。 または、リリースされている最新のカスタマイズで最新の状態になっている "HotfixSupport" ブランチに接続します。
- Visual Studio からデータベースの同期を実行しないでください。 そうしないと、UAT データベース内のスキーマの可用性に影響を与え、UAT 環境のユーザーに影響を与える可能性があります。
- 最適なエクスペリエンスのため、UAT 環境として同じデータセンターに配置された開発者環境を使用してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]