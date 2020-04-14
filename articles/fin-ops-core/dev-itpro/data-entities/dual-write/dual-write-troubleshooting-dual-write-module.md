---
title: Finance and Operations アプリのデュアル書き込みモジュールに関する問題のトラブルシューティング
description: このトピックでは、アプリの Finance and Operations デュアル書き込みモジュールの問題修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172763"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Finance and Operations アプリのデュアル書き込みモジュールに関する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]



このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、Finance and Operations アプリの **デュアル書き込み** モジュールの問題修正に特化したトラブルシューティング情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Finance and Operations アプリでデュアル書き込みのモジュールを読み込むことができない

**データ管理** ワークスペースで **デュアル書き込み** タイルを選択しても**デュアル書き込み** のページを開くことができない場合は、データ統合サービスがダウンしている可能性があります。 サポートチケットを作成して、データ統合サービスの再起動を要求してください。

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>新しいエンティティのマッピングを作成しようとするとエラーが発生する

**問題の解決に必要な資格情報：** Azure ADテナント管理者

新しいエンティティをデュアル書き込み用で構成する場合に、次のエラーメッセージが表示される場合があります。

*応答状態コードが成功とならない: 401 (権限なし)*

このエラーが発生する原因は、新しいエンティティのマッピングを追加できるのが、Azure AD テナント管理者のみであるためです。

この問題を解決するには、Finance and Operations アプリに Azure AD 管理テナントでログインしてください。 また、web.PowerApps.com にアクセスし、接続の再検証をする必要があります。

## <a name="error-when-you-open-the-dual-write-user-interface"></a>デュアル書き込みのユーザー インターフェイスを開くとエラーが発生する

**データ管理**ワークスペースからデュアル書き込みにアクセスすると、次のエラーメッセージが表示される場合があります。

*login.microsoftonline.com が接続を拒否しました。*

この問題を修正するには、Microsoft Edge の InPrivate を使用してサインインするか、Chromium の incognito ウィンドウを使用するか、Google Chrome のincognitoウィンドウを使用してください。 また、サードパーティの cookie のブロックを解除、クリアする必要があります。

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>環境をデュアル書き込みにリンクする際、または新しいエンティティのマッピングを追加する際にエラーが発生する

**問題の解決に必要な資格情報：** Azure ADテナント管理者

マッピングをリンクまたは作成する際に、次のエラーが表示される場合があります。

*応答状態コードが成功とならない: 403 (tokenexchange) 。<br>セッション ID: \<セッション ID\><br>ルート アクティビティ ID: \<ご利用のルート アクティビティ ID\>*

このエラーは、デュアル書き込みへのリンクと、マッピングを作成する十分なアクセス権限がない場合に発生する可能性があります。 Azure AD のテナントの管理者アカウントを作成して環境をリンクし、エンティティのマッピングを追加する必要があります。 この設定後は、非管理者のアカウントを使用してステータスを監視し、マッピングを編集することができます。

## <a name="error-when-you-stop-the-entity-mapping"></a>エンティティ マッピングを停止した際のエラー

エンティティのマッピングを停止した際に、次のエラー メッセージが表示される場合があります。

*\[禁止されています\]、\[{状態: 403、"ソース": ""、"メッセージ": "トークン変換エラー: ユーザーに dynamicscrmonline/xxxxxx-xxxx-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx への接続許可がありません"}\]、リモート サーバーがエラーを返しました：(403) 許可されていません。*

このエラーは、リンクされた Common Data Service 環境が使用できない場合に発生します。

この問題を修正するには、チケットを作成してデータ統合チームに問い合わせてください。 データ統合チームがマッピンがバックエンドで **実行されていない** ことを識別できるように、ネットワークのトレースを添付してください。
