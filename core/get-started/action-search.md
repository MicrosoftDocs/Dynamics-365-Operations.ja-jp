---
title: "アクション検索"
description: "この記事では、Microsoft Dynamics 365 for Finance and Operations のアクション検索機能について説明します。 アクション検索でページのアクションを検索して実行できます。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: cd024f2bc06fca9c21ea41fbed44efbc519cee94
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017


---

# <a name="action-search"></a>アクション検索

[!include[banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 for Finance and Operations のアクション検索機能について説明します。 アクション検索でページのアクションを検索して実行できます。

<a name="introduction"></a>はじめに
------------

Microsoft Dynamics 365 for Finance and Operations のページでは、ページの上部に表示される標準アクション ウィンドウおよびページのさまざまなセクションに表示されるツール バーの両方のアクション ウィンドウでコマンドが主として公開されます。 以前のバージョンでは、キー ヒント機能は、Alt キーおよび一連の文字を押して、アクション ウィンドウのボタンをすばやくアクセスできました。 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) ただし、Finance and Operations の現在のバージョンでは、キー ヒントは使用できなくなり、アクション検索機能によって取り替えられました。 この新しい機能ですぐに検索でき、表示されているどのアクション ウィンドウのボタンからも実行できます。

## <a name="using-action-search"></a>アクション検索の使用
アクション検索機能を使用するには、次の手順に従います。

1.  アクション ウィンドウで、**アクション検索**フィールドをクリックします。 (**アクション検索**フィールドには、虫眼鏡アイコンが含まれます)。
2.  自分が実行するボタンの名前の全体または一部を入力します。 ボタンの「パス」の単語を使用しても検索できます。 (詳細については、この記事の次のセクションを参照してください)。通常、2 から 4 文字を入力するとボタンが結果一覧の先頭の近くに表示されます。
3.  検索して、結果リストのボタンを実行します (マウスまたはキーボードを使用して)。

ボタンの実行後、作業し続けることができるように、フォーカスはページの最後の位置に戻されます。 

[![アクション検索フィールド](./media/action-search-field.png)](./media/action-search-field.png)

Ctrl + /、または Alt + Q を押しても、アクション検索を開始できます。 ページの最後の位置にフォーカスを返すには、キーボード ショートカットを再度押します。

## <a name="understanding-the-results-list"></a>結果一覧の理解
多くの場合、Finance and Operations で、ボタンの目的を完全に理解するためには、ボタンの場所とコンテキストの両方を把握しておく必要があります。 したがって、リストに表示されるボタンを完全に理解するために、結果一覧の各項目に追加情報が表示されます。 特に、ボタンの「パス」が表示されます。 このパスは、必要に応じて、次の UI 要素のラベルを含む場合があります:

-   アクション ウィンドウ タブ
-   ボタン グループ
-   メニュー ボタン (ボタンがメニュー ボタンの中にある場合)
-   メニュー区切り (ボタンがメニュー ボタンの中の名前を付けられたグループの中にある場合)
-   ページのグループあるいはタブ (たとえば、クイック タブの名前)

たとえば、**tot**と**アクション検索**フィールドに入力し、現在結果一覧を確認します。 最初の入力で、[**合計**] と名付けられるボタンが強調表示されます。 [**販売注文**] &gt; [**ビュー**] のボタンのパスも表示されます。 [**販売注文**] の部分は、アクション ウィンドウの [**販売注文**] タブに対応し、[**ビュー**] の部分は、そのタブの [**ビュー**] グループに対応します。 同様に、[**割引合計**] ボタン ([**販売**] &gt; [**計算**]) は、このボタンがアクション ウィンドウの [**販売**] タブの [**計算**] グループに位置することを示します。 したがって、この情報はどのボタンがアクション検索にトリガされたかを理解するのに役立ちます (結果一覧でそのボタンを選択した場合)。 

[![データ付アクション検索フィールド](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

前の例では、アクション検索はページ上部の標準アクション ウィンドウから結果を表示しました。 ただし、アクション検索は、ページの他の領域に表示されるツール バーの結果も表示します。 たとえば、[**販売注文明細行**] クイック タブに位置する [**手持在庫**] ボタンを検索しているとします。 この場合、結果一覧のボタンのパス ([**販売注文明細行**] &gt; [**在庫**] &gt; [**ビュー**]) はそのボタンが [**販売注文明細行**] クイック タブの、[**在庫**] メニュー ボタンの、[**ビュー**] ヘッダーに位置することを示します。 

[![手持在庫](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>アクション検索対ナビゲーション検索
アクション検索がページで検索し実行するアクションであるのに対し、Finance and Operations の複数のページを検索し移動する別の検索メカニズムがあります。 この機能の詳細については、「[ナビゲーション検索](navigation-search.md)」の記事を参照してください。




