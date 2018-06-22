---
title: "クラウドの工程とサービス"
description: "Finance and Operations は、管理されたサービスとしての Microsoft のクラウド ERP です。 つまり、Microsoft は実稼働環境の管理と運用を担当します。 Microsoft の Dynamics サービス エンジニアリング チームは、24 時間、週 7 日、年間 365 日お客様の生産システムを運用および管理します。"
author: manalidongre
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: 
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 68f09306be3b06fc1bcdcc8b703df93323485f8f
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="cloud-operations-and-servicing"></a>クラウドの工程とサービス

[!include [banner](../includes/banner.md)]

この試みで顧客、パートナー、および Microsoft が成功するには、例外を管理する Microsoft Dynamics サービス エンジニアリング (DSE) チームでアクションのほとんどがセルフ サービスとなるよう確認する必要があります。 このセルフサービス モードを実現するために、マイクロソフト製品チームは、環境の運用に必要なさまざまな機能の自動化を推し進めています。

## <a name="monitor-and-troubleshoot-the-health-of-your-environment"></a>環境の正常性の監視およびトラブルシューティング
Microsoft Dynamics 365 for Finance and Operations のクラウド バージョンにおいて、クラウド サービスに対する正常なオンボーディング体験で重要なことは、常に環境の正常性を把握して、必要に応じて正常性の問題をトラブルシューティングできることです。 Finance and Operations の管理者センターである Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。 詳細については、[モニタリングおよび診断](monitoring-diagnostics.md) を参照してください。

## <a name="update-your-environment"></a>環境の更新
Go-Live の後、実稼働環境は定期的に更新する必要があります。 Lifecycle Services (LCS) では、環境を継続的に更新するセルフ サービス エクスペリエンスが提供されます。

### <a name="update-types"></a>更新タイプ
- **プラットフォーム**
  - プラットフォームの修正プログラムは、Microsoft がプラットフォームの問題に対処するためにリリースする累積的なバイナリ修正プログラムです。
  - 新しいプラットフォームのリリースです。 Microsoft がプラットフォームに新しい更新プログラムをリリースしたときは、[最新のプラットフォーム更新プログラムへのアップグレード](../migration-upgrade/upgrade-latest-platform-update.md) に記載された情報を使用して新しいリリースを取り込みます。
- **アプリケーション**
  - アプリケーション修正プログラムはアプリケーションの問題を処理する X++ 修正プログラムです。
  - アプリケーションのカスタマイズは、パートナー/ISV が Microsoft により出荷する基本製品で開発するカスタマイズです。
  - アプリケーションの新規リリース。 このような更新プログラムの詳細については、[Microsoft Dynamics 365 for Finance and Operations の最新の更新への移動の概要](../migration-upgrade/upgrade-latest-update.md) を参照してください。

**クラウド インフラストラクチャ**
- Microsoft は環境のインフラストラクチャの管理について責任を負います。 このため、計画済みメンテナンス ウィンドウで月ごとに実行される必要のあるオペレーティング システムの更新などの特定の更新があります。 その他の種類の更新プログラムには、インフラストラクチャ コンポーネントへの変更が含まれます。 

### <a name="update-policy"></a>更新ポリシー
現在、サービスの更新には、生産テナント ダウンタイムが必要です。 プラットフォーム、アプリケーション、およびクラウド インフラストラクチャの更新プログラムは、2 種類のメンテナンス期間に適用されます。
- **Microsoft 予定された保守ウィンドウ** - Microsoft は、予定されているメンテナンスのダウンタイムについて、5 営業日以内に顧客に通知します。 既定のダウンタイム ウィンドウは地域ごとに定義され、ビジネスへの影響を最小限に抑えるため週末に発生するようスケジュールされます。 このウィンドウでクラウド インフラストラクチャの更新を行うことができます。 計画済みメンテナンスの詳細については、計画済みメンテナンス ウィンドウに関するよく寄せられる質問を参照してください。
- **顧客が開始するメンテナンス ウィンドウ** - 顧客は、パッケージ アプリケーション フローの一部として LCS を介してメンテナンス ウィンドウを選択します。 この保守ウィンドウでは、プラットフォームとアプリケーションの更新が行われます。

### <a name="search-for-and-apply-an-update-in-lifecycle-services"></a>Lifecycle Services で更新プログラムを検索して適用
プラットフォームとアプリケーションの更新は、環境に導入可能なパッケージとして適用されます。 デプロイ可能なパッケージは、プロジェクトのすべての環境への更新を適用するために使用される形式です。 実稼動環境で問題が発生したときは、修正プログラムをすばやく検索して、すべての環境 (開発/サンド ボックス、および実稼働) にそれを適用できます。
- **検索および更新プログラムをダウンロード** LCS で、[問題検索](issue-search-lcs.md) または [更新ポータル](../migration-upgrade/download-hotfix-lcs.md) を使用して更新を検索することができます。 更新プログラムを準備する手順は更新タイプによって異なるため、更新プログラムがダウンロードされた後、次のリストを使用して準備を続行する方法を決定してください。
  - プラットフォーム更新プログラム: プラットフォーム更新プログラムは累積的かつバイナリです。 つまり、プラットフォームの更新を環境に直接適用できます。 プラットフォームの更新プログラムがダウンロードされた後、アセット ライブラリを自動的に環境に適用させアップロードすることができます。
  - アプリケーションの修正プログラム: アプリケーションの修正プログラムはコードの変更です。 アプリケーションの修正プログラムをダウンロードした後、開発環境に適用して、配置可能なパッケージを生成する必要があります。 詳細については、[配置可能なパッケージの作成と適用](../deployment/create-apply-deployable-package.md) および [メタデータ修正プログラムのインストール](../migration-upgrade/install-metadata-hotfix-package.md) を参照してください。
  - アプリケーションのカスタマイズ: ISV またはパートナーが作成するカスタマイズです。 これらは展開可能なパッケージで、アセット ライブラリにアップロードされ、そこから適用することができます。
- **更新の適用** Finance and Operations システムの配置可能パッケージを適用する手順については、[Finance and Operations 環境用の Microsoft Dynamics 365 で配置可能パッケージを適用する](../deployment/apply-deployable-package-system.md) トピック内の情報を使用してください。 更新パッケージは、アプリケーション オブジェクト サーバー (AOS) のバイナリ修正プログラムまたは開発環境で作成された展開可能パッケージです。
- **更新の検証**更新の適用後、アプリケーションを検証する必要があります。
  - 更新プログラムが適用された問題を解決することを確認します。
  - 更新プログラムの適用によって回帰が発生していないことを確認します。
  - バイナリの更新を反映するようにビルド情報が更新されたことを確認します。
    - プラットフォーム更新プログラムで、AOS サービス モデルのバージョンが Microsoft の下で更新されることを確認します。
    - アプリケーションの更新プログラムで、修正プログラムを含むモデルのバージョンを確認します。 たとえば、アプリケーション スイートで修正があった場合、アプリケーション スイートのバージョンが更新されます。

## <a name="upgrade-your-environment"></a>環境のアップグレード
Dynamics 365 for Operation インスタンスを最新バージョンにアップグレードする方法の詳細については、[Finance and Operations の最新更新への移行の概要](../migration-upgrade/upgrade-latest-update.md) および [新機能および変更された機能](../../fin-and-ops/get-started/whats-new-changed.md) を参照してください。

## <a name="environment-data-management"></a>環境データ管理
これらは、ある環境から別の環境にデータベースをコピーする機能や、データベースを以前の状態に復元する機能など、データベースを管理するためのオプションです。
- データベースの更新: 生産データベースのコピーを使用して、サンドボックス環境を更新します (Prod から Sandbox へのデータベース復元)。 データベースを Azure SQL データベース環境から他の場所にコピーするため、LCS でデータベースの更新要求を送信することができます。
- ポイントインタイム復元: 非実稼働データベースを、リクエストから 35 日前までの特定の時点に復元するリクエストを送信できます。 データベース ポイントインタイム復元の詳細については、[非実稼働環境でのポイントインタイム データベース復元の要求](../database/request-point-in-time-restore.md) を参照してください。
- データベースを Azure SQL データベースから SQL Server へ、またはその逆にエキスポートします。 詳細については、[Microsoft Dynamics 365 for Finance and Operations を SQL Server から Azure SQL データベース環境へのコピー](../database/copy-database-from-sql-server-to-azure-sql.md) および [Microsoft Dynamics 365 for Finance and Operations を Azure SQL データベースから SQL Server 環境へのコピー](../database/copy-database-from-azure-sql-to-sql-server.md) を参照してください。

## <a name="sign-up-for-cloud-operations-notifications"></a>クラウド操作通知にサインアップします。
パッケージ アプリケーションのステータスが変更されると、LCS はプロジェクト内のすべてのユーザーに通知を送信します。 通知される追加の利害関係者は、通知リストに指定する必要があります。
1. 利害関係者を追加するには、LCS の [環境詳細] ビューで [通知一覧] をクリックします。
2. 通知する必要がある各ユーザーの電子メール アドレスを追加して、保存をクリックします。

