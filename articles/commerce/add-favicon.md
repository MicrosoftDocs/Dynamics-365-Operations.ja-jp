---
title: お気に入りの追加
description: このトピックでは、サイトにお気に入りを追加する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f249348fac526fc7814045b1b1b71c898430c0f2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980434"
---
# <a name="add-a-favicon"></a>お気に入りの追加

[!include [banner](includes/banner.md)]

このトピックでは、サイトにお気に入りを追加する方法について説明します。

## <a name="overview"></a>概要

お気に入りは小さなグラフィック ファイルで、Web ブラウザー タブ、アドレス バー、閲覧の履歴、およびブックマークやお気に入りなど、その他の場所内に表示されます。 サイトにお気に入りを追加することをお勧めします。それによりブランドを代表して強化し、顧客が閲覧する他のサイトと区別するのに役立ちます。

サイトにはさまざまなサイズとファイル タイプのお気に入りを追加できますが、このトピックでは、単一のお気に入りを追加する方法について説明します。 ただし、同じプロセスと場所を使用して、お気に入りをさらに追加することができます。

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>サイトのアセット コレクションにお気に入りをアップロードする

お気に入りをサイトのアセット コレクションにアップロードするには、次の手順に従います。

1. 左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。
1. コマンド バーで、**アップロード \> メディア項目のアップロード** を選択します。
1. [ファイル エクスプローラー] ウィンドウで、アップロードするお気に入り画像ファイルを選択し、**開く** を選択します。
1. **メディア項目のアップロード** ダイアログ ボックスで、必要なタイトルと代替テキストを入力します。
1. 画像をアップロードしてすぐに公開する場合は、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。

    > [!NOTE]
    > **アップロード後にメディア項目を公開する** オプションを選択しない場合は、後で **メディア項目** ページからお気に入りを手動で公開する必要があります。

1. **OK** を選択します。
1. 右側のプロパティ ウィンドウで、お気に入りのパブリック URL をコピーします。 この URL は後続の手順で使用します。

## <a name="create-the-html-for-your-favicon"></a>お気に入りの HTML を作成する

お気に入りの HTML を作成するには、次の HTML 文字列を使用します。 **href** 属性に関しては、**Public\_URL\_for\_your\_favicon** を前述のコピーしたパブリック URL に置き換えます。

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>お気に入りのメタタグを含むフラグメントを作成する

お気に入りのメタタグを含むフラグメントを作成するには、次の手順に従ってください。

1. **フラグメント** に移動し、**新規** を選択します。
1. **新規ページ フラグメント** ダイアログボ ックスで、ページ フラグメントの基になるモジュールに **メタタグ** を選択します。
1. フラグメントの名前を入力し、**OK** を選択します。
1. フラグメント階層ツリーで、**既定のメタタグ** 子を選択し ます。
1. 右側のウィンドウで、 **Metaタグ** 配下の **追加** を選択、前述の作成済みの HTML 文字列を入力します。 
1. **編集の完了** を選択し、 **発行** を選択してフラグメントを公開します。

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>ページの HTML 内の head セクションにメタタグのページ フラグメントを追加する

ページの HTML 内の **head** セクションにメタタグのページ フラグメントを追加するには、次の手順に従ってください。

1. **テンプレート** に移動して、お気に入りを追加するページのテンプレートを開き、続いて **編集** を開きます。
1. テンプレート階層ツリーで、**HTML head** コンテナーの右にある省略符号 (**...**) ボタンを選択し、 **フラグメントの追加** を選択します。
1. **フラグメントの選択** ダイアログ ボックスで、以前に作成した メタタグ フラグメントを選択し、**OK** を選択します。
1. **編集の完了** を選択し、 **発行** を選択してテンプレートを公開します。

> [!NOTE]
> サイトで複数のテンプレートを使用している場合は、メタタグのラグメントをすべてのテンプレートに追加する必要があります。

メタタグ フラグメントを追加したテンプレートに基づくページをプレビューすると、[ブラウザー] タブにお気に入りが表示されます。

## <a name="additional-resources"></a>追加リソース

[ロゴの追加](add-logo.md)

[サイト テーマの選択](select-site-theme.md)

[CSS 上書きファイルの作業](css-override-files.md)

[ようこそメッセージの追加](add-welcome-message.md)

[著作権に関する注意事項の追加](add-copyright-notice.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

