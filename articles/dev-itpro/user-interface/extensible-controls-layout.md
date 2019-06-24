---
title: 拡張可能なコントロール レイアウトのガイドライン
description: この記事では、拡張可能なコントロールのレイアウトとサイズを指定するときに従うガイドラインについて説明します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 11354
ms.assetid: 53d1f66a-1e69-4548-9fd2-a87a3b370882
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d04dd393685d4e4a69cee6a3b4983b1dc7bdeca
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548636"
---
# <a name="extensible-control-layout-guidelines"></a>拡張可能なコントロール レイアウトのガイドライン

[!include [banner](../includes/banner.md)]

この記事では、拡張可能なコントロールのレイアウトとサイズを指定するときに従うガイドラインについて説明します。

<a name="dos-and-donts-for-achieving-the-desired-layout"></a>目的のレイアウトを実現するための注意事項
-----------------------------------------------

-   コントロールのレイアウト クラスを直接使用しないでください。 (たとえば、**layout-container** および **layout-horizontal** は、DOM のコントロールに表示されるクラスです。) 代わりに、レイアウト バインディング ハンドラーを使用して、これらのクラスを適用します。 Internet Explorer は異なるレイアウト フレームワークを使用しており、要素にいくつかのインライン スタイルを追加するには、このフレームワークにハンドラーが提供する予備のバインディング情報が必要です。 したがって、クラスがコントロールにハードコードされて**いない**ことを確認してください。
-   レイアウト バインディング ハンドラーを使うコンテナーの子である要素に、絶対配置 (**position: absolute** and **top**/**bottom**/**left**/**right** positions) を使用しないでください。 これらの要素の絶対配置は、正しく物事をレイアウトすることに適用される CSS クラスを妨げます。
-   **幅: 100%** と**高さ: 100%** の使用には注意が必要です。 これらの設定は、レイアウト CSS クラスと組み合わせて使用すると、必ずしも機能しない場合があります。 塗りつぶし動作を使用する場合、代わりにサイズ変更バインディング ハンドラーの **$dyn.layout.Size.available** オプションを使用することをお勧めします。

## <a name="layout-binding-handlers"></a>レイアウト バインディング ハンドラー
### <a name="layout"></a>レイアウト

**ArrangeMethod** 属性と **Columns** 属性をコンテナーの **arrangeMethod**、**Columns**、**Children** オプションに適用するのに使用されます。

#### <a name="arrangemethod"></a>ArrangeMethod

-   $dyn.layout.ArrangeMethod.vertical
-   $dyn.layout.ArrangeMethod.horizontalLeft
-   $dyn.layout.ArrangeMethod.horizontalWrap
-   $dyn.layout.ArrangeMethod.horizontalRight
-   $dyn.layout.ArrangeMethod.none (レイアウト CSS クラスは要素に適用されません。)

#### <a name="columns"></a>列

-   **$dyn.layout.Columns.fill** - この定数を使用します。 コントロールに応じて、「塗りつぶし」と「バランス」のいずれかの列が使用されます。
-   **$dyn.layout.Columns.fixed** - **1**、**2**、**3** のような固定値を使用します。

#### <a name="children"></a>子

-   このコンテナを介して子を追加するためにコンテンツ ハンドラー (追加、置換) を使用する場合は、**$ data.Children** を使用します。 このコントロールがコンテナーである場合にのみ使用する必要があります。

**使用例:**

    <div data-dyn-bind="layout: { arrangeMethod: $dyn.layout.ArrangeMethod.vertical, columns: '1' }"> </div>

### <a name="sizing"></a>サイズ変更

#### <a name="heightwidth"></a>高さ/幅

-   **$dyn.layout.Size.available (SizeToAvailable)** - その方向に使用可能領域を入力します。
-   **$dyn.layout.Size.content (SizeToContent)** - その方向のコンテンツへのサイズ。
-   **$dyn.layout.Size.fixed (手動)** - 固定ピクセル値。

**使用例:**

    <div data-dyn-bind="sizing: { height: $dyn.layout.Size.available, width: $dyn.layout.Size.content }"> </div>

**サイズ変更バインディング ハンドラーに関する注意事項:**

-   サイジング バインディング ハンドラーを **SizeToAvailable** オプション (**$dyn.layout.Size.available**) と組み合わせて使用するとき、レイアウト バインディング ハンドラーを親の **&lt;div&gt;**/DOM 要素使用する必要があります。 これにより、どの軸 (水平または垂直方向) に沿って満たされるかがわかります。

**レイアウト/サイズ ハンドラーを使用すべきですか、または直接プロパティを設定する必要がありますか。**

-   拡張可能コントロールがクライアント コントロール (グループまたは PivotItem など) から継承している場合、バインディングが既に存在するため、直接そのコントロールに関連付けられている **&lt;div&gt;** でバインディング ハンドラーを使用しません。 ただし、**data-dyn-bind** 属性にプロパティが直接入れるように、プロパティを設定する必要がある場合があります。

**例 :**

    <div data-dyn-role="Group" data-dyn-bind="ArrangeMethod: $dyn.layout.ArrangeMethod.vertical, Columns: $dyn.layout.Columns.fill, Height: $dyn.layout.Size.available"></div>

<a name="faq"></a>よく寄せられる質問
---

#### <a name="is-my-control-being-laid-out-as-expected"></a>自分のコントロールが期待どおりにレイアウトされているか。

指示に適した方法は、要素を検査し、目的のクラスを探すことです。

-   適用されるオプションに応じて検索するレイアウト クラス:
    -   layout-container
    -   layout-vertical
    -   layout-horizontal
-   検索するクラスのサイズ設定:
    -   **$dyn.layout.Size.available** で、**入力幅**または**入力高さ**のいずれかを表示する必要があります。
    -   手動サイズについては、**固定高さ**または**固定幅**のいずれかを表示する必要があります。
    -   **$dyn.layout.Size.content** では、追加のクラスは存在すべきでなく、手動の高さと幅は要素で特定されたインラインである必要があります。

これらのクラスが予期したとおりに表示されない場合、拘束力のあるハンドラーの使用状況を確認し、このページの注意事項の一覧を読んだことを確認します。



