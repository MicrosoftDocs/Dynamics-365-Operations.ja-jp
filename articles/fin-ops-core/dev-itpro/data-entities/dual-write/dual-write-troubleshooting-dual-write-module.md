---
title: Finance and Operations アプリでのデュアル書き込み問題のトラブルシューティング
description: このトピックでは、アプリの Finance and Operations デュアル書き込みモジュールの問題修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 90ff55540c153ef4f3ac07bf5316a3abb4755f2c
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380143"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Finance and Operations アプリでのデュアル書き込み問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、Finance and Operations アプリの **デュアル書き込み** モジュールの問題修正に特化したトラブルシューティング情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Finance and Operations アプリでデュアル書き込みのモジュールを読み込むことができない

**データ管理** ワークスペースで **デュアル書き込み** タイルを選択しても **デュアル書き込み** のページを開くことができない場合は、データ統合サービスがダウンしている可能性があります。 サポートチケットを作成して、データ統合サービスの再起動を要求してください。

## <a name="error-when-you-try-to-create-a-new-table-map"></a>新規テーブル マップを作成しようとするとエラーが発生する

**問題の修正に必要な資格情報：** デュアル書き込みを設定したのと同じユーザー。

新しいテーブルをデュアル書き込みで構成する場合に、次のエラー メッセージが表示される場合があります。 マッピングを作成できるのは、デュアル書き込み接続を設定したユーザーだけです。

*応答状態コードが成功とならない: 401 (権限なし)*。

## <a name="error-when-you-open-the-dual-write-user-interface"></a>デュアル書き込みのユーザー インターフェイスを開くとエラーが発生する

**データ管理** ワークスペースからデュアル書き込みにアクセスすると、次のエラーメッセージが表示される場合があります。

*login.microsoftonline.com が接続を拒否しました。*

この問題を修正するには、Microsoft Edge の InPrivate を使用してサインインするか、Chromium の incognito ウィンドウを使用するか、Google Chrome のincognitoウィンドウを使用してください。 また、サードパーティの cookie のブロックを解除、クリアする必要があります。

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>環境をデュアル書き込みにリンクする際、または新しいテーブルのマッピングを追加する際にエラーが発生する

**問題の修正に必要なロール:** Finance and Operations アプリと Dataverse 両方のシステム管理者権限。

マッピングをリンクまたは作成する際に、次のエラーが表示される場合があります。

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

このエラーは、デュアル書き込みへのリンクと、マッピングを作成する十分なアクセス権限がない場合に発生する可能性があります。 このエラーは、リンク解除によるデュアル書き込みを行わずに Dataverse 環境をリセットした場合にも発生する可能性があります。 Finance and Operations アプリと Dataverse の両方でシステム管理者ロールを持つすべてのユーザーが、環境をリンクできます。 デュアル書き込み接続を設定したユーザーだけが、新しいテーブル マップを追加できます。 設定後、システム管理者のロールを持つユーザーはステータスを監視し、マッピングを編集できます。

## <a name="error-when-you-stop-the-table-mapping"></a>テーブル マッピングを停止した際のエラー

テーブルのマッピングを停止した際に、次のエラー メッセージが表示される場合があります:

*\[禁止されています\]、\[{状態: 403、"ソース": ""、"メッセージ": "トークン変換エラー: ユーザーに dynamicscrmonline/xxxxxx-xxxx-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx への接続許可がありません"}\]、リモート サーバーがエラーを返しました：(403) 許可されていません。*

このエラーは、リンクされた Dataverse 環境が使用できない場合に発生します。

この問題を修正するには、チケットを作成してデータ統合チームに問い合わせてください。 データ統合チームがマッピンがバックエンドで **実行されていない** ことを識別できるように、ネットワークのトレースを添付してください。

## <a name="errors-while-trying-to-start-a-table-mapping"></a>テーブル マッピングの開始中に発生するエラー

### <a name="unable-to-complete-initial-data-sync"></a>初期データの同期を完了できません

初期データの同期実行時に、次のようなエラーが表示される場合があります。

*初期データの同期を完了できません。エラー: デュアル書き込みエラー ― プラグインの登録に失敗しました: デュアル書き込みルックアップのメタデータをビルドできません。エラーオブジェクト参照がオブジェクトのインスタンスに設定されていません。*

マッピングの状態を **実行中** に設定しようとすると、次のエラーが表示される場合があります。 エラーの原因によって修正方法は異なります。

+ マッピングに依存マッピングが含まれている場合は、このテーブル マッピングの依存マッピングを有効にする必要があります。
+ マッピングにソース列、または出力先の列がない可能性があります。 Finance and Operations アプリの列が存在しない場合は、[マップに存在しないテーブル列の問題](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) のセクションに記載されている手順を実行します。 Dataverse で列が表示されていない場合は、マッピングの **テーブルの更新** ボタンをクリックして、列が自動的にマッピングに反映されるようにします。

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>バージョンの不一致エラーとデュアル書き込みソリューションのアップグレード

テーブルのマッピングを実行しようとすると、次のエラー メッセージが表示される場合があります。

+ *顧客グループ (msdyn_customergroups) : デュアル書き込みエラー - Dynamics 365 for Sales のソリューション 'Dynamics365Company' にはバージョンの不一致があります。バージョン: '2.0.2.10' 必須バージョン: '2.0.133'*
+ *Dynamics 365 for Sales のソリューション 'Dynamics365FinanceExtended' にはバージョンの不一致があります。バージョン: '1.0.0.0' 必須バージョン: '2.0.227'*
+ *Dynamics 365 for Sales のソリューション 'Dynamics365FinanceAndOperationsCommon' にはバージョンの不一致があります。バージョン: '1.0.0.0' 必須バージョン: '2.0.133'*
+ *Dynamics 365 for Sales のソリューション 'CurrencyExchangeRates' にはバージョンの不一致があります。バージョン: '1.0.0.0' 必須バージョン: '2.0.133'*
+ *Dynamics 365 for Sales のソリューション 'Dynamics365SupplyChainExtended' にはバージョンの不一致があります。バージョン: '1.0.0.0' 必須バージョン: '2.0.227'*

この問題を修正するには、Dataverse でデュアル書き込みソリューションを更新します。 必要なソリューション バージョンに一致する最新のソリューションにアップグレードしてください。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
