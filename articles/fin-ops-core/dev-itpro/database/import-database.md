---
title: データベースのインポート
description: この記事では、財務と運用アプリのデータベースをインポートする方法について説明します。
author: LaneSwenka
ms.date: 11/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 45d7f7a976498cace05942940c372d0c4bfe87e5
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103492"
---
# <a name="import-a-database"></a>データベースのインポート

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) は、ゴールデン コンフィギュレーション データベースをサンドボックス ユーザー受入テスト (UAT) の環境にインポートするために使用できます。

## <a name="prerequisites"></a>必要条件

Dynamics AX 2012 アップグレード用に構成された LCS プロジェクトには、データベース インポートは適用できません。 したがって、**プロジェクト オンボーディング** \> **プロジェクト概要** で、**レガシ システム** フィールドが **AX2012 アップグレード** に設定された場合、インポートはブロックされます。

## <a name="self-service-import-database"></a>セルフ サービス インポート データベース

[!include [dbmovement-import](../includes/dbmovement-import.md)]

### <a name="import-operation-failure"></a>インポート操作失敗

インポート操作が正常に行われない場合は、*ロールバック* できます。 操作が最初に失敗した後に **ロールバック** オプションをクリックすると、対象となるサンドボックス環境がインポートの開始前の状態に戻されます。 ロールバック操作は、データベースを復元するための Microsoft Azure SQL データベース ポイントインタイム復元機能により使用可能になります。 ターゲット サンドボックスに存在するカスタマイズが、新しくインポートされたデータでデータベースの同期を完了できない場合、ロールバックがよく必要になります。

### <a name="data-elements-that-require-attention-after-import"></a>インポート後に注意が必要なデータの要素

データベースのバックアップをサンド ボックスUAT環境にインポートするときは、特定の活動を実行する必要があります。 次にいくつか例を挙げます。

* ソース データベースに、パーティション テーブルのレコードが 1 つしか含まれていないことを確認します。
* お客様の要件に従って、電子メール機能が正しく再設定または無効になっていることを確認してください。
* お客様の要件に従って、統合設定がオンまたはオフになっていることを確認してください。
* Application Object Server (AOS) サーバーが必要なバッチ グループに追加されたことを確認します。
* システム ヘルプとタスク ガイドに再接続されていることを確認します。
* バッチ ジョブのステータスが **待機中** に設定されていることを確認します。
* ユーザーが再度有効化されたことを確認します。
* 必要に応じて、二重書き込みが再リンクされていることを確認します。
* 必要に応じて、二重書き込みが再リンクされていることを確認します。  この操作に成功した後にターゲット環境に新しいリンクを設定するには、[二重書き込み環境リンク](../data-entities/dual-write/link-your-environment.md)を参照してください。

### <a name="environment-admin"></a>環境管理者

対象となる環境のシステム管理者アカウント (**管理者** ユーザーID) が、その環境内の web.config ファイルに含まれる値にリセットされます。 このアカウントは、LCS からの管理者アカウントと同じである必要があります。 このアカウントがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの **環境の詳細** ページにアクセスします。 環境が最初に展開されたときに **環境管理者** フィールドで選択された値は、トランザクション データベース内のシステム管理者となるように更新されます。 これにより、環境のテナントが環境管理者のテナントになります。

web.config ファイルを変更するために環境に管理者ユーザー プロビジョニング ツールを使用した場合、値が LCS の値と一致しない可能性があります。 別のアカウントを使用することを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。 その後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。

## <a name="steps-to-complete-after-a-database-import-for-environments-that-use-commerce-functionality"></a>コマース機能を使用する環境のデータベース インポート後に実行する手順

[!include [environment-reprovision](../includes/environment-reprovision.md)]


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

