---
title: robots.txt ファイルの管理
description: このトピックでは、Microsoft Dynamics 365 Commerce の robots.txt ファイルを管理する方法について説明します。
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: e472f3612bd6860e7262bb128035f2aed3b39372
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946040"
---
# <a name="manage-robotstxt-files"></a>robots.txt ファイルの管理

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の robots.txt ファイルを管理する方法について説明します。

## <a name="overview"></a>概要

ロボット除外標準または robots.txt は、Web サイトが Web ロボットと通信するために使用する標準です。 参照すべきではない Web サイトのすべての領域について、Web ロボットに指示します。 多くの場合、検索エンジンはロボットを使用して Web サイトをインデックス化します。

サーバーからロボットを除外するには、サーバー上にファイルを作成します。 このファイルでは、ロボットのアクセス ポリシーを指定します。 ファイルは、ローカル URL **/robots.txt** で HTTP 経由でアクセスできる必要があります。 robots.txt ファイルは、検索エンジンがサイトのコンテンツをインデックス化するのに役立ちます。

Dynamics 365 Commerce では、ドメインの robots.txt ファイルをアップロードできます。 コマース環境内のドメインごとに、robots.txt ファイルを 1 つアップロードして、そのドメインに関連付けることができます。

robots.txt ファイルの詳細については、[Web ロボット ページ](https://www.robotstxt.org/)を参照してください。

## <a name="upload-a-robotstxt-file"></a>robots.txt ファイルのアップロード

[ロボットの除外標準](https://www.robotstxt.org/orig.html)に従って robots.txt ファイルを作成しおよび編集した後に、コマース作成ツールを使用するコンピュータでそのファイルにアクセスできることを確認します。 ファイル名は、**robots.txt** である必要があります。 最適な結果を得るには、標準に記載されている形式にする必要があります。 各コマースの顧客は、robots.txt ファイルの内容を検証および維持する責任があります。 robots.txt ファイルをアップロードするには、システム管理者としてコマースにログインする必要があります。

コマースで robots.txt ファイルをアップロードするには、次の手順を実行します。

1. システム管理者として Commerce にサインインします。
2. 左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。
3. **テナントの設定**で、**robots.txt** を選択します。 環境に関連付けられているすべてのドメインのリストが、ウィンドウの主要部分に表示されます。
4. **管理**を選択して、環境内ドメインの robots.txt ファイルをアップロードします。
5. 右側のメニューで、robots.txt ファイルに関連づけられているドメインの横にある**アップロード** ボタン (上向き矢印) を選択します。 ファイル参照ダイアログ ボックスが表示されます。
6. ダイアログボックスで、関連付けられたドメインにアップロードする robots.txt ファイルを参照して選択し、**開く**を選択してアップロードを完了します。

> [!NOTE] 
> アップロード中に、コマースはファイルがテキスト ファイルであることを検証しますが、ファイルの内容は検証しません。

## <a name="download-a-robotstxt-file"></a>robots.txt ファイルのダウンロード

コマースで robots.txt ファイルをダウンロードするには、次の手順を実行します。

1. システム管理者として Commerce にサインインします。
2. 左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。
3. **テナントの設定**で、**robots.txt** を選択します。 環境に関連付けられているすべてのドメインのリストが、ウィンドウの主要部分に表示されます。
4. **管理**を選択して、環境内ドメインの robots.txt ファイルをダウンロードします。
5. 右側のメニューで、robots.txt ファイルに関連づけられているドメインの横にある**ダウンロード** ボタン (下向き矢印) を選択します。 ファイル参照ダイアログ ボックスが表示されます。
6. ダイアログ ボックスで、ローカル ドライブの目的の場所に移動し、ファイル名を確認するか入力して**保存**を選択してダウンロードを完了します。

> [!NOTE]
> この手順を使用して、コマース作成ツールを介して以前にアップロードされた robots.txt ファイルのみをダウンロードできます。

## <a name="delete-a-robotstxt-file"></a>robots.txt ファイルの削除

コマースで robots.txt ファイルを削除するには、次の手順を実行します。

1. システム管理者として Commerce にサインインします。
2. 左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。
3. **テナントの設定**で、**robots.txt** を選択します。 環境に関連付けられているすべてのドメインのリストが、ウィンドウの主要部分に表示されます。
4. **管理**を選択して、環境内ドメインの robots.txt ファイルを削除します。
5. 右側のメニューで、robots.txt ファイルに関連づけられているドメインの横にある**削除** ボタン (ごみ箱記号) を選択します。 ファイル ブラウザー ウィンドウが表示されます。
6. ファイル ブラウザー ウィンドウで、ドメインから削除する robots.txt ファイルを参照して選択し、**開く**を選択します。 警告のメッセージ ボックスが表示されます。
7. メッセージ ボックスで、**削除**を選択して robots.txt ファイルの削除を確認します。

> [!NOTE] 
> この手順を使用して、コマース作成ツールを介して以前にアップロードされた robots.txt ファイルのみを削除できます。

## <a name="additional-resources"></a>追加リソース

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[新しい E コマース サイトの配置](deploy-ecommerce-site.md)

[E コマース サイトの作成](create-ecommerce-site.md)

[チャンネルとオンライン サイトの関連付け](associate-site-online-store.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)
