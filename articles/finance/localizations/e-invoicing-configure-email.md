---
title: メール チャネルの構成
description: この記事では、電子請求書を受信するメール チャネルを構成する方法について説明します。
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 19339cbcc59e93289609690363b0dd9195a66f6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279873"
---
# <a name="configure-an-email-channel"></a>メール チャネルの構成

[!include [banner](../includes/banner.md)]

作成した電子請求機能が、電子メールで受信した添付ファイルから電子的な仕入の請求書をインポートする場合は、メール アカウント チャネルを構成します。

1. Regulatory Configuration Service (RCS) で、作成した電子請求機能を選択します。 状態が **ドラフト** のバージョンを選択していることを確認してください。
2. **設定** タブで **追加** を選択します。
3. **機能設定の作成** ドロップダウン ダイアログ ボックスの **新規** フィールド グループで、**カスタム設定** オプションを選択します。
4. **設定タイプ** のフィールド グループで、**データ チャネル** オプションを選択します。
5. **データ チャネルの選択** フィールドで、**受信メール** と入力します。
6. **作成** を選択します。
7. 作成した行を選択し、**編集** を選択します。
8. **データ チャネル** タブの **パラメーター** セクションで、次の必須フィールドを設定します。

    | フィールド                | Description |
    |----------------------|-------------|
    | データ チャネル         | データ チャネルを識別する一意の名前を入力します。 名前は最大 10 文字使用できます。 これは、通信プロセス中に、適用ルールおよび接続されたアプリケーションで参照されます。 |
    | サーバー アドレス       | メール アカウント プロバイダーのサーバー アドレスを入力します。 たとえば、`https://outlook.live.com` プロバイダーのサーバー アドレスは imap-mail.outlook.com です。 |
    | サーバー ポート          | メール アカウント プロバイダーが使用するポートの番号を入力します。 たとえば、`https://outlook.live.com` プロバイダーのサーバー ポートは 993 です。 |
    | ユーザー名シークレット     | メール ユーザー アカウントの ID を含む Microsoft Azure Key Vault シークレットの名前を入力します。 このシークレットは、Key Vault で作成し、サービス環境で設定する必要があります。 |
    | ユーザー パスワード シークレット | メール ユーザー アカウントのパスワードを含む Key Vault シークレットの名前を入力します。 |
    | タイムアウト              | システムが応答を待つ最大時間制限 (ミリ秒 (ms))。 既定値は 10,000 ms (10 秒) です。 |
    | メイン フォルダー          | メールのインポート元、またはサービスがメールを処理するフォルダーを指定します。 |
    | アーカイブ フォルダー       | 処理したメールの保存先フォルダーを指定します。 このフォルダーを指定しない場合、自動的に作成されます。 |
    | エラー フォルダー         | 処理が失敗した場合にメールを移動するフォルダーを指定します。 このフォルダーを指定しない場合、自動的に作成されます。 |
    | メッセージの最大サイズ     | 処理される 1 つのメッセージの最大サイズ (バイト) を入力します。 既定値は 20,000,000 バイトです。 |
    | 最大メッセージ番号   | 単一のアクションで処理するメッセージの最大数を入力します。 メッセージの数を制限しない場合は、値を **0** (ゼロ) に設定します。 |
    | フィルターから          | 送信者のアドレスでフィルター処理する文字列を入力します。 送信者のアドレスがフィルターに一致するメールだけが処理されます。 このフィールドはオプションです。 複数の送信者のアドレスを指定するには、セミコロン (;) を区切りとして使用します。 |
    | 件名フィルター       | 件名でフィルター処理する文字列を入力します。 件名がフィルターに一致するメールだけが処理されます。 このフィールドはオプションです。 **\*smth\*.ext** などシンプルなマスクがサポートされており、各アスタリスク (\*) は 0 個以上の文字を表します。 |
    | 日付フィルター          | 処理されるメッセージの最大期日経過日数 (日) を定義する日付を指定します。 このフィールドはオプションです。 既定の値は 30 日です。 |
    | 処理モード      | <p>メール内のすべての添付ファイルをまとめて処理できるか、または各添付ファイルを個別に処理するかを指定するには、次のいずれかのオプションを選択します。</p><ul><li><b>添付ファイル</b> – メールの各添付ファイルに新しい電子ドキュメントが作成されます。 たとえば、1 つのメールに電子請求書のデータを含む複数のファイルが含まれている場合、各ファイルはシステムで新しい電子請求書と見なされます。</li><li><b>メール</b> – 1 つの添付ファイルが基本添付ファイルと見なされ、1 つの電子請求書がシステムで作成されます。 他の添付ファイルは、サポート ファイルとして使用できます。</li></ul> |

9. **添付ファイル フィルター** セクションで、ファイル フィルター処理情報を追加します。 定義されているフィルターを満たす添付ファイルだけが処理されます。 たとえば、**\*.xml** は .xml ファイル名拡張子を持つ添付ファイルをフィルター処理します。 添付ファイルの名前は、設定中に Dynamics 365 Finance または Dynamics 365 Supply Chain Management で使用されます。

    - 以前の手順で **処理モード** フィールドを **メール** に設定した場合は、複数のフィルターをここに追加できます。 名前が特定のドキュメントを識別します。
    - **処理モード** フィールドを **添付ファイル** に設定した場合、追加できるフィルターは 1 つのみです。

10. 必要に応じて、**適用ルール** タブで基準の確認および更新を行います。 **チャネル** フィールドの値は、手順 8 の **データ チャネル** フィールドで入力した値と同じである必要があります。
11. **保存** を選択して、ページを閉じます。
