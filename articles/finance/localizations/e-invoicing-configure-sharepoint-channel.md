---
title: SharePoint チャネルの構成
description: この記事では、Microsoft SharePoint チャネルを構成して、受信する電子請求書を処理する方法について説明します。
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 92eaa357c6d72cc637d4ce353702e5d41ecf4338
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272307"
---
# <a name="configure-a-sharepoint-channel"></a>SharePoint チャネルの構成

[!include [banner](../includes/banner.md)]

Microsoft SharePoint チャネルを構成して受信するドキュメントを処理する前提条件として、[SharePoint の接続を構成する](e-invoicing-create-sharepoint-connection.md) で説明されている手順を完了する必要があります。

その後、SharePoint チャネルを使用して SharePoint フォルダーに保存されているファイルから仕入先電子請求書をインポートできます。

1. SharePoint サイトで、次のフォルダーを作成します。

    - **メイン フォルダー** – サービスが処理するファイルがあるフォルダー。
    - **アーカイブ フォルダー** – 処理されたファイルを保存するフォルダー。
    - **エラー フォルダー** – 処理が失敗した場合にシステムがファイルを移動するフォルダー。

2. Regulatory Configuration Service (RCS) で、作成した電子請求機能を選択します。 状態が **ドラフト** のバージョンを選択していることを確認してください。
3. **設定** タブで **追加** を選択します。
4. **機能設定の作成** ドロップダウン ダイアログ ボックスの **新規** フィールド グループで、**カスタム設定** オプションを選択します。
5. **設定タイプ** のフィールド グループで、**データ チャネル** オプションを選択します。
6. **データ チャネルの選択** フィールドで、**SharePoint フォルダー** を選択します。
7. **作成** を選択します。
8. 作成した行を選択し、**編集** を選択します。
9. **データ チャネル** タブの **パラメーター** セクションで、次の必須フィールドを設定します。

    | フィールド                 | Description |
    |-----------------------|-------------|
    | データ チャネル          | データ チャネルを識別する一意の名前を入力します。 名前は最大 10 文字使用できます。 これは、通信プロセス中に、適用ルールおよび接続されたアプリケーションで参照されます。 |
    | SharePoint アドレス    | SharePoint URL を入力します。 たとえば、「`<domain>.sharepoint.com`」を入力します。 |
    | アプリケーション ID        | SharePoint ユーザー アカウントの ID を含む Azure Key Vault シークレットの名前を入力します。 このシークレットは、Key Vault で作成し、サービス環境で設定する必要があります。 値は、[SharePoint 接続の構成](e-invoicing-create-sharepoint-connection.md) からの **アプリケーション (クライアント) ID** の値です。 |
    | アプリケーション シークレット    | SharePoint ユーザー アカウントのパスワードを含む Key Vault シークレットの名前を入力します。 値は、[SharePoint 接続の構成](e-invoicing-create-sharepoint-connection.md) からの **アプリ登録シークレット** 値です。 |
    | サイト名             | SharePoint サイトの名前を入力します。 |
    | ドキュメント ライブラリ名 | SharePoint ドキュメント ライブラリの名前を入力します。 |
    | タイムアウト               | システムが応答を待つ最大時間制限 (ミリ秒 (ms)) を入力します。 既定値は 10,000 ms (10 秒) です。 |
    | メイン フォルダー           | ファイルのインポート元、またはサービスがファイルを処理するフォルダーを指定します。 |
    | アーカイブ フォルダー        | 処理したファイルの保存先フォルダーを指定します。 |
    | エラー フォルダー          | 処理が失敗した場合にファイルを移動するフォルダーを指定します。 |
    | 最大ファイル サイズ         | 処理される 1 つのファイルの最大サイズ (バイト) を入力します。 既定値は 20,000,000 バイトです。 |
    | 最大ファイル数      | 単一のアクションで処理するファイルの最大数を入力します。 ファイルの数を制限しない場合は、値を **0** (ゼロ) に設定します。 |
    | ファイルのフィルター           | ファイル名でフィルター処理する文字列を入力します。 このフィールドはオプションです。 **\*smth\*.ext** などシンプルなマスクがサポートされており、各アスタリスク (\*) は 0 個以上の文字を表します。 たとえば、**\*.pdf** を入力して、PDF ファイルを読み取るチャネルを構成します。 |
    | カスタム ファイル名      | クライアントからのカスタム ファイル名を入力します。 |

10. 必要に応じて、**適用ルール** タブで基準の確認および更新を行います。 **チャネル** フィールドの値は、以前の手順の **データ チャネル** フィールドで入力した値と同じである必要があります。
11. **保存** を選択して、ページを閉じます。
