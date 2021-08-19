---
title: タイル リスト モジュール
description: このトピックでは、タイル リスト モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 10bf7139ba89f5089d288e78fab9e3d63249aac9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638907"
---
# <a name="tile-list-module"></a>タイル リスト モジュール

[!include [banner](includes/banner.md)]

このトピックでは、タイル リスト モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

タイル リスト モジュールは、カルーセル内ののタイルのコレクションです。 画像とテキストを使用して、製品カテゴリや製品ブランドのマーケティングを行うために使用されます。 たとえば、小売業者が eコマース サイトのホーム ページにタイル リスト モジュールを追加して、売れ筋のカテゴリをすべて販売促進することができます。

タイル リスト モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動します。 他のモジュールや Commerce 本社のデータには依存しません。 タイル リスト モジュールは、小売業者がマーケティングまたは販売促進を行う (製品、カテゴリ、ブランドなど) サイト ページに追加することができます。

次の図は、Adventure Works のホーム ページの中の、タイル リスト モジュールと、タイル モジュールの例を示しています。

![Adventure Works のホーム ページの中の、タイル リスト モジュールと、タイル モジュールの例](./media/Tile_list.PNG)

> [!IMPORTANT]
> タイル リスト モジュールは、Dynamics 365 Commerce バージョン 10.0.20 リリース時点で使用できます。
> タイル リスト モジュールは Adventure Works のテーマで示されています。

## <a name="tile-list-modules-and-themes"></a>タイル リスト モジュールとテーマ

タイル リスト モジュールは、テーマに基づく各種レイアウトおよびスタイルをサポートできます。 たとえば、Adventure Works のテーマでは、サイト ユーザーがタイルの上にカーソルを置くと、タイルはアニメーション効果を表示します。 各テーマには、タイル リストとタイル モジュールの追加プロパティを含めることができます。 また、テーマ開発者は、タイル リストやタイル モジュールの追加レイアウトを構築することもできます。

## <a name="tile-list-module-properties"></a>タイル リスト モジュールのプロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| ヘッダー       | ヘッダー テキストとヘッダー タグ | タイル リスト モジュールのテキスト ヘッダーです。 |

## <a name="tile-module-properties"></a>タイル モジュール プロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| 画像         | イメージ ファイル | 画像を使用して製品またはプロパティを紹介できます。 画像は Commerce サイト ビルダのメディア ライブラリーにアップロードするか、既存の画像を使用できます。 |
| ヘッダー       | ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**) | 既定では、**H2** ヘッダー タグがヘッダーに使用されますが、アクセシビリティ要件を満たすようにヘッダー タグを変更できます。 |
| 段落     | 段落のテキスト | モジュールは、リッチ テキスト形式の段落テキストをサポートします。 ハイパーリンク、太字、下線付き、および斜体など、基本的なリッチ テキスト機能がいくつかサポートされます。 これらの機能の一部は、モジュールに適用されるページ テーマによって上書きされる場合があります。 |
| リンク          | リンク テキスト、リンク URL、アクセス可能リッチ インターネット アプリケーション (ARIA) ラベル、および **新しいタブでリンクを開く** | モジュールは、1 つ以上の "アクションの呼び出し" リンクをサポートします。 リンクを追加すると、リンク テキスト、URL、および ARIA ラベルが必要になります。 ARIA ラベルは、アクセシビリティ要件を満たしていることを説明する必要があります。 リンクをコンフィギュレーションして、新しいタブで開くことができます。 |
| タイル リンク     | リンク テキスト、リンク URL、ARIA ラベル、および **新しいタブでリンクを開く** セレクター | このプロパティを使用して、"アクションへの呼び出し" リンクを定義します。 リンクを追加すると、リンク テキスト、URL、および ARIA ラベルが必要になります。 ARIA ラベルは、アクセシビリティ要件を満たしていることを説明する必要があります。 リンクをコンフィギュレーションして、新しいタブで開くことができます。|
| アイコン          | 画像 | 製品またはカテゴリ画像に加えて、アイコン記号を追加することもできます。 アイコン記号の画像は、製品またはカテゴリの画像の上に表示されます。 |

## <a name="add-a-tile-list-module-to-a-new-page"></a>タイル リンク モジュールを新しいページに追加する

新しいページにタイル リスト モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。

1. **テンプレート** に移動し、サイトのホーム ページのマーケティング テンプレートを開きます (または、新しいマーケティング テンプレートを作成します)。
1. 既定のページの **メイン** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**タイル リスト** モジュールを選択して、**OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。
1. **ページ** に移動し、サイトのホーム ページを開きます (または、マーケティング テンプレートを使用して新しいホーム ページを作成します)。
1. 既定のページの **メイン** スロットで、省略記号ボタン (**...**) を選択してから、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**タイル リスト** モジュールを選択して、**OK** を選択します。
1. タイル リスト モジュールのプロパティ ウィンドウで、ヘッダーを追加します。
1. **タイル リスト** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**タイル モジュール** モジュールを選択して、**OK** を選択します。
1. タイル モジュールのプロパティ ウィンドウで、画像、ヘッダー、およびアイコン記号画像を追加します。
1. 必要に応じて、タイル モジュールを追加および構成します。
1. **保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。
1. **編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[Adventure Works テーマ](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]