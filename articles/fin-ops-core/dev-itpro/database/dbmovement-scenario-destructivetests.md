---
title: 破壊試験
description: この記事では、財務と運用の破壊テスト シナリオについて説明します。
author: LaneSwenka
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: c42b58cf64c36a8f90b94007650527a0982143ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867551"
---
# <a name="destructive-testing"></a>破壊試験 

[!include [banner](../includes/banner.md)]

データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。 場合によっては、環境で破壊試験を実行する必要があります。 このコンテキストでは、破壊試験は、環境を継続的なテストに使用できなくなったと宣言することを意味します。 破壊試験は、会議室パイロット中の実装ライフ サイクルでは一般的です。 このチュートリアルでは、破壊試験を容易にするデータベース移動操作の使用方法を示します。

このチュートリアルでは、2 つの操作について説明します。

> [!div class="checklist"]
> * データベース バックアップ資産を使用します。
> * ポイントインタイム復元を使用します。

このシナリオの例として、顧客は会議室パイロットを実行しようとしており、トランザクションがない (つまり、販売注文や発注書がない) 環境で開始します。 顧客は、同じパイロットを行うために、地理的な環境地域間で物理的な倉庫から物理的な倉庫に移動し、各パイロットが行われる前に、環境を「リセット」することを希望しています。

## <a name="prerequisites"></a>必要条件

このチュートリアルを完了するには、プロジェクトに標準ユーザー受け入れテスト (UAT) 環境が展開されている必要があります。

## <a name="using-a-database-backup"></a>データベースのバックアップの使用

すでにテストの準備ができているデータベース バックアップ (.bacpac) ファイルがある場合、最も簡単な方法は、バックアップ ファイルを LCS プロジェクトの資産ライブラリ内の **データベース バックアップ** セクションにアップロードすることです。 その後、ここで説明するように、対象となる環境にインポートすることができます。

[!include [dbmovement-import](../includes/dbmovement-import.md)]

### <a name="database-backup-pros-and-cons"></a>データベース バックアップの長所と短所

バックアップ ファイル資産を使用する利点は、テストの開始点に戻るために、同じファイルのインポートを保持できることです。

デメリットは、インポートが完了する前かつユーザーが開始できるようになった後に多くの構成 (バッチ ジョブなど) を設定する必要がある場合、各破壊テスト セッションの前により多くの作業が必要になる点です。

## <a name="using-point-in-time-restore"></a>ポイントインタイム復元の使用

データベース バックアップ (.bacpac) ファイルで開始しなかった場合に、正常な状態であることがわかっている UAT 環境がある場合、自分のタイムゾーンの日時を記録できます。 その後、破壊試験を開始できます。 次に、テストが完了したら、、次の手順を使用して、前の時点の環境を復元できます。

[!include [dbmovement-import](../includes/dbmovement-pitr.md)]

### <a name="point-in-time-restore-pros-and-cons"></a>ポイントインタイム復元のメリットとデメリット

ポイントタイム復元を使用する利点は、データベース バックアップ (.bacpac) ファイルの処理を回避できるため、破壊テスト セッションの間の時間を短縮できることです。

デメリットは、ポイントインタイム復元の現在の制限により、復元が完了した後に新しい復元の日時を記録する必要があることです。 ポイントインタイム復元では常に新しいデータベースが作成されるため、使用された元の日時は新しいデータベースの復元ポイントとして使用できません。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]