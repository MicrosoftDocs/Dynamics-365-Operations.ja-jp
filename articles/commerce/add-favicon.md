---
title: お気に入りの追加
description: このトピックでは、サイトにお気に入りを追加する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 18e12cbe46650fcf024a56b6de9a8cb2903d2bf8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914580"
---
# <a name="add-a-favicon"></a>お気に入りの追加

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、サイトにお気に入りを追加する方法について説明します。

## <a name="overview"></a>概要

お気に入りは小さなグラフィック ファイルで、Web ブラウザー タブ、アドレス バー、閲覧の履歴、およびブックマークやお気に入りなど、その他の場所内に表示されます。 サイトにお気に入りを追加することをお勧めします。それによりブランドを代表して強化し、顧客が閲覧する他のサイトと区別するのに役立ちます。

サイトにはさまざまなサイズとファイル タイプのお気に入りを追加できますが、このトピックでは、単一のお気に入りを追加する方法について説明します。 ただし、同じプロセスと場所を使用して、お気に入りをさらに追加することができます。

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>サイトのアセット コレクションにお気に入りをアップロードする

お気に入りをサイトのアセット コレクションにアップロードするには、次の手順に従います。

1. **アセット \> アップロード \> アセットのアップロード**の順に移動します。
1. ローカル ファイル システムでお気に入りを検索して選択します。
1. タイトルを入力し、**OK** を選択します。 
1. 右側のプロパティ ウィンドウで、お気に入りのパブリック URL をコピーします。

> [!NOTE]
> **アップロード後にアセットを公開**オプションを選択しない場合、**アセット** ページに戻り、後でお気に入りを手動で公開する必要があります。

## <a name="create-the-html-for-the-favicon"></a>お気に入りの HTML を作成する

お気に入りの HTML を作成するには、次の HTML スニペットを使用します。 **href** 属性に関しては、**"Public\_URL\_for\_your\_favicon"** を以前にコピーしたパブリック URL に置き換えます。

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>お気に入りの HTML をページの \<head\> 要素に追加する

サイトにお気に入りを追加するには、サイト ページの **\<head\>** 要素に任意のタイプの HTML またはスクリプトを追加するのと同じ手順を使用します。

## <a name="additional-resources"></a>追加リソース

[ロゴの追加](add-logo.md)

[サイト テーマの選択](select-site-theme.md)

[CSS 上書きファイルの作業](css-override-files.md)

[ようこそメッセージの追加](add-welcome-message.md)

[著作権に関する注意事項の追加](add-copyright-notice.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

