---
title: ワークスペース タイル用のアイコンの作成
description: このトピックでは、アイコンを作成してカスタム ワークスペース タイルに割り当てるためのガイドラインと推奨事項について説明します。
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
ms.custom: 141853
ms.assetid: 4f78c3a4-011f-4ebd-bada-98e77d43821e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 3b39ef02313db27ac6661baa02e0215e741835e4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537198"
---
# <a name="create-icons-for-workspace-tiles"></a>ワークスペース タイル用のアイコンの作成

[!include [banner](../includes/banner.md)]

このトピックでは、アイコンを作成してカスタム ワークスペース タイルに割り当てるためのガイドラインと推奨事項について説明します。  

ダッシュボードには、ユーザーがアクセスできる一連のワークスペース タイルが含まれています。 これらのタイルにはそれぞれ、ワークスペースに固有のアイコンが含まれます。 Microsoft により提供された追加設定なしのワークスペースについては、ワークスペースタイルで使用されるアイコンは一般的に [記号フォント](symbol-font.md) からの記号に対応します。 この記事では、マイクロソフト認定パートナーまたは個人のお客様が作成したワークスペースのアイコンを作成してタイルに割り当てるためのガイドラインと推奨事項について説明します。

## <a name="implementation-details"></a>実装詳細
### <a name="icon-creation"></a>アイコン作成

ワークスペース アイコンについては、アイコンの AOT リソースを使用することをお勧めします。 既成のシンボルは機能しますが、複数のワークスペースが同じアイコンを使用することがないように、独自のシンボルを作成することをお勧めします。 アイコンが必要な各ワークスペースについては、以下のガイドラインに準拠している新しい画像ファイルを作成します。

-   イメージ ファイルは、縦横比が 1:1 の PNG ファイルである必要があります。
-   アイコンは白いコンテンツの透明な背景にする必要があります。 このフレームワークはテーマに合わせて既定の背景色を設定します。
-   推奨画像サイズは、アイコンが中央の 21 x 21 ピクセルの正方形内に配置されている、50 x 50 ピクセルです (下図参照)。
    -   推奨される画像とアイコンのサイズは、すぐに使用できるワークスペースに対応しています。 大きいイメージは使用できません。ただし、フル イメージに関連するアイコンのサイズと配置はイメージのサイズに関係なく保持する必要があります。
    -   この推奨に従うことにより、以下の点ができるようになります。
        -   ワークスペース アイコンは、他のワークスペース アイコンのサイズと一致します。
        -   ワークスペースのアイコンのコンテンツは、画像を円としてレンダリングする CSS によってトリミングされません。

![workspaceIconSizing](./media/workspaceiconsizing.png)

### <a name="modeling-details"></a>モデリングの詳細

ワークスペース タイルを作成するときは、次のガイドラインに準拠する必要があります。

-   新しいアイコンごとに AOTResource を追加します。
-   ワークスペースに対応するタイルで、次のプロパティを設定します。
    -   ImageLocation=AOTResource
    -   NormalImage=&lt;AOTResource の名前&gt;

## <a name="example"></a>例
新しいワークスペースに使用される次のイメージ/アイコンを検討します。 

[![newLogo3](./media/newlogo3.png)](./media/newlogo3.png) 

このアイコンは透明な背景を持つイメージに変換され、アイコンの白いコンテンツは大きなイメージ キャンバスの中央に配置されます。 

![newIcon](./media/newicon.png) 

ワークスペース アイコンのイメージ

![newIcon\_guides](./media/newicon_guides.png) 

ワークスペース アイコンのイメージは、アイコンのために取り分けられた領域とともに、タイル上の可視の循環部分を表示するために重ねて表示されます。

この画像をワークスペース タイルで使用すると、ダッシュ ボードには次の結果が得られます。 

[![newWorkspaceIcon](./media/newworkspaceicon.png)](./media/newworkspaceicon.png)                



