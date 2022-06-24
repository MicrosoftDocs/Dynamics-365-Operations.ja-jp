---
title: robots.txt ファイルの管理
description: この記事では、Microsoft Dynamics 365 Commerce の robots.txt ファイルを管理する方法について説明します。
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ccb09cfce00ba838cb5358afef9b7acc5c61d8d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896982"
---
# <a name="manage-robotstxt-files"></a>robots.txt ファイルの管理

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の robots.txt ファイルを管理する方法について説明します。

ロボット除外標準または robots.txt は、Web サイトが Web ロボットと通信するために使用する標準です。 参照すべきではない Web サイトのすべての領域について、Web ロボットに指示します。 多くの場合、検索エンジンはロボットを使用して Web サイトをインデックス化します。

サーバーからロボットを除外するには、サーバー上にファイルを作成します。 このファイルでは、ロボットのアクセス ポリシーを指定します。 ファイルは、ローカル URL **/robots.txt** で HTTP 経由でアクセスできる必要があります。 robots.txt ファイルは、検索エンジンがサイトのコンテンツをインデックス化するのに役立ちます。

Dynamics 365 Commerce では、ドメインの robots.txt ファイルをアップロードできます。 コマース環境内のドメインごとに、robots.txt ファイルを 1 つアップロードして、そのドメインに関連付けることができます。

robots.txt ファイルの詳細については、[Web ロボット ページ](https://www.robotstxt.org/)を参照してください。

## <a name="upload-a-robotstxt-file"></a>robots.txt ファイルのアップロード

[ロボットの除外標準](https://www.robotstxt.org/orig.html)に従って robots.txt ファイルを作成しおよび編集した後に、コマース作成ツールを使用するコンピュータでそのファイルにアクセスできることを確認します。 ファイル名は、**robots.txt** である必要があります。 最適な結果を得るには、標準に記載されている形式にする必要があります。 各コマースの顧客は、robots.txt ファイルの内容を検証および維持する責任があります。 robots.txt ファイルをアップロードするには、システム管理者としてコマースにログインする必要があります。

コマースで robots.txt ファイルをアップロードするには、次の手順を実行します。

1. システム管理者として Commerce にサインインします。
2. 左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。
3. **テナントの設定** で、**robots.txt** を選択します。 環境に関連付けられているすべてのドメインのリストが、ウィンドウの主要部分に表示されます。
4. **管理** を選択して、環境内ドメインの robots.txt ファイルをアップロードします。
5. 右側のメニューで、robots.txt ファイルに関連づけられているドメインの横にある **アップロード** ボタン (上向き矢印) を選択します。 ファイル参照ダイアログ ボックスが表示されます。
6. ダイアログボックスで、関連付けられたドメインにアップロードする robots.txt ファイルを参照して選択し、**開く** を選択してアップロードを完了します。

> [!NOTE] 
> アップロード中に、コマースはファイルがテキスト ファイルであることを検証しますが、ファイルの内容は検証しません。

## <a name="download-a-robotstxt-file"></a>robots.txt ファイルのダウンロード

コマースで robots.txt ファイルをダウンロードするには、次の手順を実行します。

1. システム管理者として Commerce にサインインします。
2. 左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。
3. **テナントの設定** で、**robots.txt** を選択します。 環境に関連付けられているすべてのドメインのリストが、ウィンドウの主要部分に表示されます。
4. **管理** を選択して、環境内ドメインの robots.txt ファイルをダウンロードします。
5. 右側のメニューで、robots.txt ファイルに関連づけられているドメインの横にある **ダウンロード** ボタン (下向き矢印) を選択します。 ファイル参照ダイアログ ボックスが表示されます。
6. ダイアログ ボックスで、ローカル ドライブの目的の場所に移動し、ファイル名を確認するか入力して **保存** を選択してダウンロードを完了します。

> [!NOTE]
> この手順を使用して、コマース作成ツールを介して以前にアップロードされた robots.txt ファイルのみをダウンロードできます。

## <a name="delete-a-robotstxt-file"></a>robots.txt ファイルの削除

コマースで robots.txt ファイルを削除するには、次の手順を実行します。

1. システム管理者として Commerce にサインインします。
2. 左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。
3. **テナントの設定** で、**robots.txt** を選択します。 環境に関連付けられているすべてのドメインのリストが、ウィンドウの主要部分に表示されます。
4. **管理** を選択して、環境内ドメインの robots.txt ファイルを削除します。
5. 右側のメニューで、robots.txt ファイルに関連づけられているドメインの横にある **削除** ボタン (ごみ箱記号) を選択します。 ファイル ブラウザー ウィンドウが表示されます。
6. ファイル ブラウザー ウィンドウで、ドメインから削除する robots.txt ファイルを参照して選択し、**開く** を選択します。 警告のメッセージ ボックスが表示されます。
7. メッセージ ボックスで、**削除** を選択して robots.txt ファイルの削除を確認します。

> [!NOTE] 
> この手順を使用して、コマース作成ツールを介して以前にアップロードされた robots.txt ファイルのみを削除できます。

## <a name="additional-resources"></a>追加リソース

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[新しい eコマース テナントのデプロイ](deploy-ecommerce-site.md)

[eコマース サイトの作成](create-ecommerce-site.md)

[オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け](associate-site-online-store.md)

[URL リダイレクトの一括アップロード](upload-bulk-redirects.md)

[Commerce での B2C テナントの設定](set-up-B2C-tenant.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-B2C-tenants.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
