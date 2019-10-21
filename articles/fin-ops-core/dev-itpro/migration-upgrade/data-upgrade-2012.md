---
title: AX 2012 からのアップグレード - 開発環境でのデータ アップグレード
description: このトピックでは、Microsoft Dynamics AX 2012 から最新の Finance and Operations 開発環境にアップグレードする詳細なプロセスについて説明します。
author: tariqbell
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: febcdc40cac7ff9afdf08702fac60e51f302c899
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191883"
---
# <a name="upgrade-from-ax-2012---data-upgrade-in-development-environments"></a>AX 2012 からのアップグレード - 開発環境でのデータ アップグレード

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

これは、アップグレード プロジェクトのエキサイティングな瞬間です。 このタスクの出力により、Microsoft Dynamics AX 2012 から最新の Finance and Operations 開発環境にアップグレードされた最初のデータセットが提供されます。

このプロセスを共有サンドボックス環境で実行する前に、開発環境で実行することをお勧めします。 このアプローチには 2 つの理由があります。

- 開発者がカスタム データ アップグレード スクリプトを書き込んでテストできるローカル データを提供します。
- これは、データ アップグレード プロセスの繰り返しに費やされる全体的な時間を短縮できます。 開発環境では、問題を即座にデバッグし、コードを調整し、アップグレードを数分以内に再実行することができます。 ただし、より規模の大きいサンドボックス環境ではこの機敏性のレベルが許可されていません。 それらの環境では、問題の修正やデバッグ、コードの更新、更新済コードの配置、およびアップグレードの再実行に少なくとも数時間を要します。

データのアップグレードを実行する前に、[アップグレード アナライザー](upgrade-analyzer-tool.md)を実行して、特定した問題に対応することを強くお勧めします。これは、データのアップグレードが迅速かつ容易になることを保証する手助けになります。

> [!NOTE]
> このプロセスを開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。[SQL Server Management Studio のダウンロード](/sql/ssms/download-sql-server-management-studio-ssms). 

## <a name="end-to-end-data-upgrade-process"></a>エンド ツー エンド データのアップグレード プロセス

![データ アップグレード プロセス](media/endToEndDataUpgradeProcess.png)

### <a name="back-up-your-ax-2012-database"></a>AX 2012 データベースをバックアップします

AX 2012 データベースをバックアップするには、標準の Microsoft SQL Server プロセスを使用して BAK ファイルを作成します。 バックアップを作成するときに圧縮オプションを使用すると、ファイル サイズが小さくなり、Microsoft Azure Storage にアップロードおよびダウンロードするために必要な時間が短縮されます。

### <a name="upload-the-backup-to-azure-storage"></a>Azure ストレージにバックアップをアップロード

開発環境がローカルまたは Azure で VM としてホストされている場合、2012 データベースのバックアップをそれに転送する必要があります。 ローカル VM では、ネットワーク全体でファイルを直接転送することができますが (それを許可するように仮想ネットワークを構成済みの場合)、Azure でホストされた VM の場合バックアップを Azure Storage にアップロードすることをお勧めします (自分のセキュアな転送サービスまたは SFTP の使用も有効なオプションです)。 これに対して、独自の Azure ストレージ アカウントを指定する必要があります。 Azure ストレージ間でファイルを移動するのに役立つ無料のツールがあります。コマンド ラインからは [Azcopy](/azure/storage/storage-use-azcopy) を、GUI 操作からは [Microsoft Azure ストレージ エクスプローラー](https://storageexplorer.com/) を使用できます。 これらのツールのいずれかを使用して、オンプレミス環境から Azure ストレージにバックアップをアップロードしてから、開発環境にダウンロードしてください。

### <a name="download-and-restore-the-backup-to-the-development-environment"></a>開発環境へのバックアップのダウンロードと復元

新しい開発環境にバックアップを復元する場合、既存の AXDB データベースを上書きしないでください。 代わりに、元のデータベースの横にある AX 2012 データベースを復元します。 パフォーマンスを向上させるために、データおよびログ ファイルの D ドライブの使用も考慮する場合があります。 ただし、D ドライブを使用することには潜在的な問題点があります。基になる仮想マシン (VM) が Azure で割り当て解除され、次に再割り当てされると、D ドライブが消去されます。 実際、このシナリオが発生ことはほとんどありません。 したがって、そのリスクは容認できる可能性があります。 ドライブ D の使用方法の詳細については、[[Windows Azure 仮想マシンでのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)] を参照してください。

データベースの復元プロセスをスピードアップするには、SQL Server サービスアカウントを **axlocaladmin** に変更します。 復元プロセスでは、インスタント ファイルの初期化を使用できます。 詳細については、[データベース インスタント ファイルの初期化](/sql/relational-databases/databases/database-instant-file-initialization) を参照してください。

データベースを復元した後、次のサービスを停止します。

- World Wide Web 公開サービス
- Dynamics 365 for Finance and Operations バッチ管理サービス
- Management Reporter 2012 処理サービス

次に、元の AXDB データベースを **AXDB_orig** に名前を変更します。 このデータベースは、後でコードを開発する際に参照する場合があります。

最後に、新しく復元された AX 2012 データベース **AXDB** の名前を変更します。

### <a name="run-the-data-upgrade-deployable-package"></a>データ アップグレード展開可能なパッケージを実行 

最新の更新プログラムを実行しているターゲット環境用に最新のデータ アップグレード展開可能パッケージを入手するには、Microsoft Dynamics Lifecycle Services (LCS) 共用資産ライブラリから最新のバイナリ更新プログラムをダウンロードします。

1. [LCS](https://lcs.dynamics.com/) にサインインします。
2. **共有資産ライブラリ** タイルを選択します。
3. **共有アセット** ライブラリの**アセット タイプの選択**で、**ソフトウェア配置可能パッケージ**を選択します。
4. 配置可能パッケージ ファイルの一覧で、アップグレードに対応するデータ アップグレード パッケージを検索します。 たとえば、AX 2012 からアップグレードする場合、パッケージ名は AX2012DataUpgrade から始まります。 アップグレードするリリースに対応するパッケージを選択します。 例: AX2012DataUpgrade-July2017。

詳細については、[開発、デモ、またはサンドボックス環境でのデータのアップグレード](upgrade-data-to-latest-update.md) を参照してください。 

## <a name="troubleshooting-data-upgrade-script-errors"></a>アップグレード スクリプト エラーのトラブルシューティング データ

最後に停止した場所で、データのアップグレードを再開できるようにするオプションがあります。 また、データベース内のテーブルに、コール スタック付きでデータ アップグレード スクリプト エラーを記録することができます。 開発のシナリオでは、失敗したスクリプトをスキップし、継続してアップグレードを実行できます。

詳細については、[主要データのアップグレード トピック](upgrade-data-to-latest-update.md#troubleshoot-upgrade-script-errors) を参照してください。

### <a name="recommendation-for-the-first-data-upgrade-run"></a>最初のデータ アップグレードを実行するための推奨事項

初めてデータセットのデータのアップグレードを実行するとき、特に多くのカスタマイズまたは多くのカスタム データのアップグレード スクリプトが存在するとき、[失敗したスクリプトをスキップする機能](upgrade-data-to-latest-update.md) が役に立つ場合があります。 この機能を使用すると、1 回の実行で可能な限り多くのエラーを可視化できます。 それ以外の場合、実行あたり 1 つだけの重要な問題が検出されます。 スクリプト間には依存関係が存在するため、親スクリプトをスキップすると関連する子スクリプトにエラーが発生することがあります。 これらのエラーは、親が正しく実行されなかったためにのみ発生します。 親スクリプト内の問題が解決されると、解決されます。
