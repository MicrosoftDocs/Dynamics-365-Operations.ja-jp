---
title: Commerce チャット モジュールのプロアクティブなチャット パラメータ
description: この記事では、Microsoft Dynamics 365 Commerce の Commerce チャット モジュールのプロアクティブなチャットマラメーターについて説明します。
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691073"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Commerce チャット モジュールのプロアクティブなチャット パラメータ

[!include [banner](includes/banner.md)]

この記事では、Customer Service オムニチャネルを使用した Commerce チャットと、Microsoft Dynamics 365 Commerce の Power Virtual Agents を使った Commerce チャットモジュールのプロアクティブなチャット パラメータについて説明します。

## <a name="proactive-chat-properties"></a>プロアクティブなチャット プロパティ

プロアクティブなチャット プロパティは、Customer Service 用オムニチャネルを使った Commerce チャットと Commerce サイトビルダーの Power Virtual Agents を使った Commerce チャットのプロパティ ウィンドウにあります。

> [!NOTE]
> 既定では、ここに表示されるプロアクティブな活動のプロパティはすべて空白です。 これらのプロパティの詳細を確認し、必要に応じてのみ設定することをお勧めします。 この方法は、誤ったプロアクティブなアクションをトリガから減らすのに役立ちます。

### <a name="proactive-chat"></a>プロアクティブ チャット

| フレンドリ名 | Description | 既定値 |
|---------------|-------------|---------------|
| 有効 | さまざまなトリガに基づいて、顧客にプロアクティブに関与します。 | 無効 |
| チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 | 空白 |

### <a name="wait-time-proactive-chat"></a>待ち時間 (プロアクティブ チャット)

| フレンドリ名 | Description |
|---------------|-------------|
| 待ち時間 (秒) | プロアクティブなチャットがトリガされる前にサイト ユーザーがサイト ページに費やす時間 (秒)。 |
| チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 |

### <a name="number-of-page-visits-proactive-chat"></a>ページ訪問数 (プロアクティブ チャット)

| フレンドリ名 | Description |
|---------------|-------------|
| ページ訪問の数 | プロアクティブなシステムがトリガされる前のページ訪問の数。 サイトユーザーは、まずクッキーの同意のバナーのプロンプトに同意する必要があります。 |
| チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 |

### <a name="specific-pages-proactive-chat"></a>特定のページ (プロアクティブ チャット)

| フレンドリ名 | Description |
|---------------|-------------|
| ページ | ページにアクセスした際にプロアクティブな活動をトリガするページの一覧。 |
| チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 |

### <a name="from-specific-pages-proactive-chat"></a>特定のページから (プロアクティブ チャット)

| フレンドリ名 | Description |
|---------------|-------------|
| ページ | ユーザーが去って行った際に、プロアクティブ チャットをトリガするページの一覧。 |
| チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 |

### <a name="specific-countryregion-proactive-chat"></a>特定の国/地域 (プロアクティブ チャット)

| フレンドリ名 | Description |
|---------------|-------------|
| 国コード | 指定した国や地域から移動するユーザーは、プロアクティブなチャットを開始します。 国/地域コードは、大文字で 2 文字 (**米国** など) で指定する必要があります。 |
| チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 |

### <a name="date-range-proactive-chat"></a>日付範囲 (プロアクティブ チャット)

| フレンドリ名 | Description |
|---------------|-------------|
| 開始日 (dd/mm/yyyy) | その日かその日の後にプロアクティブなチャットがトリガーされる日付。 |
| 終了日 (dd/mm/yyyy) | その日かその日の前にプロアクティブなチャットがトリガーされる日付。 |
| チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 |

### <a name="total-amount-in-cart-proactive-chat"></a>チャットの合計金額 (プロアクティブ チャット)

| フレンドリ名 | Description |
|---------------|-------------|
| 最小 | ユーザーが買い物カゴページに移動するときにプロアクティブな活動をトリガーする買い物カゴの最小金額 (その金額を含む)。 |
| 最大 | ユーザーが買い物カゴページに移動するときにプロアクティブな活動をトリガーする買い物カゴの最大金額 (その金額を含む)。 |
|チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>カートに入る品目の総数 (プロアクティブ チャット)

| フレンドリ名 | Description |
|---------------|-------------|
| 最小 | ユーザーが買い物カゴページに移動するときにプロアクティブな活動をトリガーする買い物カゴの最小商品数 (その商品を含む)。 |
| 最大 | ユーザーが買い物カゴページに移動するときにプロアクティブな活動をトリガーする買い物カゴの最大商品数 (その商品を含む)。 |
| チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 |

### <a name="specific-products-in-cart-proactive-chat"></a>特定の製品をカートに入れる (プロアクティブ チャット)

| フレンドリ名 | Description |
|---------------|-------------|
| 製品 ID/SKU | ユーザーが買い物カゴ ページに移動するときにプロアクティブ な活動をトリガする製品の ID/在庫管理単位 (SKU) 番号の一覧。 |
| チャットのあいさつ | プロアクティブ なオブジェクトがトリガされた場合に使用されるあいさつメッセージ。 |

## <a name="additional-resources"></a>追加リソース

[Commerce チャット機能の概要](commerce-chat-overview.md)

[Customer Service 用オムニチャネルを使った Commerce チャット モジュール](commerce-chat-module.md)

[Power Virtual Agents モジュールを使った Commerce チャット](chat-module-pva.md)
