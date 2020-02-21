---
title: クライアント側の設計 API
description: このトピックでは、クライアント側での設計のための API の概要と、それらの使用に関する推奨事項について説明します。
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 8ca156f601135c68de5d2a0e7f80d0e19b1669c4
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029392"
---
# <a name="client-side-design-apis"></a>クライアント側の設計 API

[!include [banner](../../../includes/banner.md)]

このトピックでは、クライアント側での設計のためのプリケーション プログラミング インターフェイス (API) の概要と、それらの使用に関する推奨事項について説明します。

## <a name="terminology"></a>用語
次のリストには、クライアント側の設計 API に適用される用語がいくつか含まれています。

- **デザイン** - 既定デザインを上書きするためにページ、アクション、またはその他のコンポーネント オブジェクトで必要に応じて指定できるプロパティ。
- **コンポーネント** - コンポーネントには、次の 4 つのタイプがあります。

  - **ブロック コンテナー** (既定) - CSS ブロック動作を持つコンテナーです。 (つまり、コンテナーは、CSS **display: block** スタイル申告を持つ要素に相当します。)
  - **フレックス コンテナー** – CSS フレックス動作のあるコンテナー。 (つまり、コンテナーは、CSS **display: flex** スタイル申告を持つ要素に相当します。)
  - **コントロール参照** - ページまたはアクションの静的メタデータ (XML) に存在するコントロールを参照するコンポーネント。
  - **新しいコントロール** – 新しいコントロールをインスタンス化するコンポーネント。 (つまり、コントロールは、ページまたはアクションの静的メタデータ [XML] にはまだ存在しません。)

    コンポーネントは JavaScript Object Notation (JSON) オブジェクトによってデザイン内に表され、この JSON オブジェクトのプロパティは、コンポーネントのプロパティを表します。 デザイン プロパティ階層のほとんどすべての JSON オブジェクトはコンポーネントです。

- **項目** – コンテナーに入れ子にされたコンポーネント。
- **プロパティ** – コンポーネントで複数のタイプのプロパティを設定することができます。

  - コンテナー固有
  - 品目固有
  - コントロール固有
  - リスト固有
  - 一般 (不特定)

    プロパティは、コンポーネントの JSON オブジェクトのキーと値のペアとして指定されます。 適用可能なプロパティは、プロパティが適用されるコンポーネントのタイプによって異なります。

    使用可能な値の定義済リストを持つプロパティについては、ドキュメントで示されている最初の値がプロパティの既定値です。 ほとんどの場合、プロパティをまったく指定していない (つまり、JSON オブジェクトからのプロパティを省略する) 場合、プロパティは既定値を設定していた場合と同じように動作します。

    一般的なプロパティは、すべてのコンポーネントのタイプに適用できます。

    プロパティを指定するときは、次のガイドラインに従います。

  - プロパティ名は引用符で囲まないでください。
  - ドキュメントでそれ以外が指定されない限り、すべてのプロパティ値を二重引用符で囲む必要があります。

- **継承** – コントロールに色、フォントサイズ、またはフォントの太さが適用されている場合、すべての子孫コントロールは再割り当てされない限り、同じプロパティを継承します。 コントロールにスペースを適用する場合は、コントロールの品目 (非コンテナー) 子孫によって継承されます。 その他のプロパティは継承されません。

## <a name="using-design-apis"></a>設計 API の使用
次のコードは、予約管理の例のビジネス ロジック コードの変更されたセグメントです。 具体的には、このコードは、引当の詳細ページのデザインを指定する変数から取得されます。 コメントはコードに含まれており、いくつかの可能性を強調します。

> [!NOTE]
> コントロールに適用される色、フォント サイズ、またはフォントの太さはコントロールのすべての子にも適用されます。 埋め込みは、コンテナー以外の子によって継承されます。 その他のプロパティは継承されません。 コンテナーにはリスト、ページ、グループ、およびパーツが含まれます。

子または品目を持たないコントロールを作成した後、コントロール名は引用符で囲む必要があります (次のコードの **FMCustomer\_FullName** を参照してください)。 ただし、任意のカスタマイズがコントロールに適用される場合、コードはブロックされる必要があり、**名前**ラベルを使用する必要があります (次のコードで **FMCustomer\_画像**を参照してください)。

```json
// Page root container
"flexFlow":"column nowrap",
"items":[
    // Upper third of page, contains 4 rows
    {
        "flexFlow":"column nowrap",
        "background":"theme", // set background color to the theme color
        "color":"light",      // set the foreground (e.g. font) color to light
        "fontSize":"small",
        "border": "none",
        "padding":"small",
        "items":[
            // Row 1/4 with customer image and name
            {
                "flexFlow":"row nowrap",
                "alignItems":"center",
                "justifyItems":"center",
                "labelStyle":"hidden", // don't show label for field
                "fontSize":"large",
                "fontWeight":"bold",
                "items":[
                    {
                    // Customer image – since we're modifying the imageStyle, etc., this
                    // code must be blocked and the "FMCustomer_Image" must be labeled
                    // with "name".
                        "name":"FMCustomer_Image",
                        "imageStyle":"circular",
                        height:3,
                        width:3
                    },
                    // don't need to create a new object or use the "name" label if
                    // there is no customization
                    "FMCustomer_FullName",
                ]
            },
            // Row 2/4 with vehicle description
            . . .
        }
    }
```

次の図は、前のコードで生成された顧客画像、顧客名、フォント、背景色などを示しています。

![前のコードにより生成された情報を示す画像](media/detail-page.png)
