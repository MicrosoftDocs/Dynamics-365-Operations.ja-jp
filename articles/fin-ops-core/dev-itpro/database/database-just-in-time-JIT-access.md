---
title: ジャストインタイム データベース アクセスの有効化
description: このトピックでは、ジャストインタイム (JIT) 方式でデータベース アクセスを有効にするために必要な手順を示します。
author: laneswenka
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 7d5465ebca2cdda260ac68020db7839d6a76a2b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753050"
---
# <a name="enable-just-in-time-database-access"></a>ジャストインタイム データベース アクセスの有効化

[!include [banner](../includes/banner.md)]

このトピックでは、ジャストインタイム (JIT) 方式を使用してデータベース アクセスを有効にするために必要な手順を示します。 さまざまなトラブルシューティング作業、予定外のクエリの実行、またはデータ アップグレードの問題解決に、データベースへのアクセスが必要な場合に役立ちます。 このプロセスは、セルフサービスおよび Microsoft が管理するサンドボックス承認テスト環境の両方に対して使用できます。 使用可能な環境のタイプの詳細については、[配置の概要](../deployment/cloud-deployment-overview.md) を参照してください。

## <a name="microsoft-managed-environments-without-rdp-access"></a>RDP へのアクセスがない Microsoft が管理する環境

サンドボックスへのリモート デスクトップ プロトコル (RDP) アクセスがない場合は、ご利用の IP アドレスを Lifecycle Services (LCS) からセルフサービス方式で許可リストに追加できます。 環境から RDP が削除されると、環境の詳細ページのマシン資格情報セクションが削除されます。  この場合、次のスクリーンショットに示すように、データベース アカウント セクションのみが残ります。 
![データベース アカウント セクション](media/sql-jit1.png)

サンドボックス環境の環境の詳細ページを開いて、**管理** > **アクセスの有効化** を選択してから、ダイアログ ボックスでソース環境の IP アドレスを追加します。 このエントリは期限切れになり、入力した IP アドレスの横に有効期限が表示されます。 また、データベースの更新やデータベースのインポートなど、データベースの移動操作によってデータベースが置き換えられた後にも失われます。

LCS のアカウントおよび有効にした IP アドレスを使用して、データベースに接続する SQL Server Management Studio (SSMS) のようなツールを使用することができるようになります。 LCS はサーバーとデータベースを次の形式で表示することに注意してください: **serverName\databaseName**。  SSMS で接続するには、Azure パブリック クラウドの場合、**serverName.database.windows.net** などのドメイン名の接尾語を追加する必要があります。 SSMS 接続ウィンドウの **オプション** タブでは、正常に接続するために **データベース** フィールドの databaseName 値も明示的に入力する必要があります。

## <a name="self-service-environments"></a>セルフサービス環境

セルフサービス環境のタイプには、リモート デスクトップ プロトコル (RDP) アクセスまたは静的データベース アカウントはありませんでした。 ただし、この場合もデータベースにアクセスすることができます。

サンドボックス環境の環境の詳細ページを開いて、**管理** > **アクセスの有効化** を選択してから、ダイアログ ボックスでソース環境の IP アドレスを追加します。 エントリの有効期限は設定されていませんが、データベースの更新やデータベースのインポートなど、データベースの移動操作によってデータベースが置き換えられた後に失われます。

また、**データベース アカウント** セクションで必要なアクセスのタイプを入力する必要があります。 使用可能なオプションには、読み取りまたは読み取り-書き込みのアクセスが含まれます。 簡単な理由の説明を入力し、**アクセスの要求** を選択します。
![アクセスの要求オプション](media/sql-jit2.png)

ページが更新されると、有効期限の時間とともにデータベース アカウントが表示されます。
![有効期限の時間とともに表示されるデータベース アカウント](media/sql-jit3.png)

LCS のアカウントおよび有効にした IP アドレスを使用して、データベースに接続する SQL Server Management Studio (SSMS) のようなツールを使用することができるようになります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]