---
title: 警告モジュール
description: このトピックでは、警告モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785355"
---
# <a name="alert-module"></a>警告モジュール

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、警告モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

## <a name="overview"></a>概要

警告モジュールは、ページにインライン情報メッセージを表示するために使用されます。 警告モジュールは、テキストメッセージおよびリンクをサポートします。 電子商取引サイトのすべてのページに表示される、サイト全体のプロモーションを表示するために使用できます。 

警告モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。

## <a name="examples-of-alert-modules-in-e-commerce"></a>電子商取引サイトの警告モジュールの例

警告モジュールをサイト ヘッダーで使用して、サイト全体のプロモーションまたはメッセージを示すことができます。 次にいくつか例を挙げます。

"年間販売は残り 10 日間"

"新学期割引でお買い得。 今がチャンス。"

## <a name="alert-module-properties"></a>警告モジュール プロパティ

| プロパティ名  | 金額                              | 説明 |
|----------------|------------------------------------|-------------|
| テキスト           | テキスト                               | 警告モジュールに表示されるテキスト メッセージ。 |
| テキスト配置 | **右**、**左**、または**中央** | 警告モジュールでテキストをどのように合わせるかを定義する値。 |
| 警告を無視  | **True** または **False**              | 値が **True** に設定されている場合、顧客は警告を閉じることができます。 |
| リンク           | URL                                | オプション リンクの URL |

## <a name="add-an-alert-module-to-a-page"></a>警告モジュールをページに追加 

ページに警告モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。

1. **警告テンプレート**という名前のページ テンプレートを作成します。
1. 既定ページの**メイン** スロットで、警告モジュールを追加します。
1. テンプレートをチェックインし、公開します。 
1. 作成した警告テンプレートを使用して、**警告ページ**という名前のページを作成します。 
1. 新しいページの**メイン** スロットで、警告モジュールを追加します。
1. 警告モジュールの設定で、警告テキストを入力します。 警告モジュールをさらにカスタマイズする場合は、他のプロパティを編集できます。
1. ページを保存してプレビューします。 ページの上部に、追加したテキストを含む警告が表示される必要があります。
1. ページをチェックインしてから公開します。 

## <a name="additional-resources"></a>追加リソース

[スタート キットの概要](starter-kit-overview.md)

[カルーセル モジュール](add-carousel.md)

[コンテンツ リッチ ブロック モジュール](add-content-rich-block.md)

[コンテンツ配置モジュール](add-content-placement-modules.md)

[機能モジュール](add-feature-module.md)

[ヒーロー モジュール](add-hero-module.md)

[ビデオ プレーヤー モジュール](add-video-player.md)
