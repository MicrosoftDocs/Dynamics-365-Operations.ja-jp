---
title: "拡張データ型の変更"
description: "拡張機能を使用して、拡張データ型 (EDT) で複数のプロパティをカスタマイズすることができます。"
author: ivanv-microsoft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 78195aa952f5aea85f141623e2dfb4e24c2cd785
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="modify-an-extended-data-type"></a>拡張データ型の変更

[!include [banner](../includes/banner.md)]

既存の拡張データ型 (EDT) で拡張機能を使用してカスタマイズできるプロパティがいくつかあります。
- ラベル
- ヘルプ テキスト
- フォーム ヘルプ
- 国地域コード
- 文字列サイズ 
    + EDT が別の EDT から拡張されない場合、値のみを修正することができます。
    + 新しい文字列のサイズは、基準 EDT 値に等しい値または超える値にのみセットすることができます。

プロパティ シートを使用して、新たに追加された要素のと同様にプロパティを変更します。

![EDT の変更](media/EDT01.jpg) 
 
コードをコンパイルした後、アプリケーションで変更を確認できます。

![EDT の変更](media/EDT02.jpg) 

Visual Studio のアプリケーション エクスプ ローラーでは作成された拡張機能を表示できます。

![EDT の変更](media/EDT03.jpg) 

## <a name="if-the-edt-is-modified-in-more-than-one-model"></a>1 つ以上のモデルで EDT が変更される場合
複数の ISV に同じ拡張データ型がある場合、最上位モデル ID を持つモデルから EDT のプロパティが使用されます。 たとえば、ISV 1 が モデル AwesomeModel with ID 12 で「Awesome 品目番号」に ItemId のラベルを変更し、ISV 2 がモデル SuperModel with ID 15 で「Super 品目番号」に ItemId のラベルを変更した場合、エンドユーザーはユーザー インターフェイスで「品目番号」の代わりに「Awesome 品目番号」を表示します。

> [!TIP]
> 既存の EDT を拡張する代わりに、既存の EDT から派生する新しいものを作成できます。 これにより、拡張方法を使用して編集するよりも多くのプロパティを編集できます。 つまり、新しい EDT を使用するには、この EDT を使用してフィールドを変更する必要があります。


