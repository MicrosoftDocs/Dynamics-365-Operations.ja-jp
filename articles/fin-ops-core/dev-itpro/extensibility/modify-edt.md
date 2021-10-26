---
title: 拡張機能を通じて拡張データ型 (EDT) を変更する
description: 拡張機能を使用して、拡張データ型 (EDT) で複数のプロパティをカスタマイズすることができます。
author: ivanv-microsoft
ms.date: 04/30/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 598c3678ec25c1e0995ac21eef162c89b28bde30
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594998"
---
# <a name="modify-extended-data-types-edts-through-extension"></a>拡張機能を通じて拡張データ型 (EDT) を変更する

[!include [banner](../includes/banner.md)]

既存の拡張データ型 (EDT) で拡張機能を使用してカスタマイズできるプロパティがいくつかあります。
- ラベル
- ヘルプ テキスト
- フォーム ヘルプ
- 国地域コード
- 文字列サイズ 
    + EDT が別の EDT から拡張されない場合、値のみを修正することができます。
    + 新しい文字列のサイズは、基準 EDT 値に等しい値または超える値にのみセットすることができます。
- 小数点以下の桁数 (NoOfDecimalsプロパティ)
    + 詳細については、 [選択したデータ型の小数点以下の精度の拡張](decimal-point-precision.md) を参照してください。

プロパティ シートを使用して、新たに追加された要素のと同様にプロパティを変更します。

![拡張プロパティ。](media/EDT01.jpg) 
 
コードをコンパイルした後、アプリケーションで変更を確認できます。

![テスト フォーム。](media/EDT02.jpg) 

Visual Studio のアプリケーション エクスプローラーでは作成された拡張機能を表示できます。

![アプリケーション エクスプローラー。](media/EDT03.jpg) 

## <a name="if-the-edt-is-modified-in-more-than-one-model"></a>1 つ以上のモデルで EDT が変更される場合

複数の ISV が同じ拡張データ型を拡張した場合は、モデル ID が最も高い (USR に最も近い) モデルの EDT のプロパティが使用されます。 同じレイヤーに変更を加えた複数のモデルがある場合は、モデル ID の最も高いモデルからの変更が使用されます。 たとえば、ISV 1 が モデル AwesomeModel (USR レイヤー) with ID 15 で「Awesome 品目番号」に ItemId のラベルを変更し、ISV 2 がモデル SuperModel (USR レイヤー) with ID 12 で「Super 品目番号」に ItemId のラベルを変更した場合、エンドユーザーにはユーザー インターフェイスで「品目番号」の代わりに「Awesome 品目番号」と表示されます。

> [!NOTE]
> 既存の EDT を拡張する代わりに、既存の EDT を基にして新たなEDTを作成できます。 これにより、拡張方法を使用して編集するよりも多くのプロパティを編集できます。 つまり、新しい EDT を使用するには、この EDT を使用してフィールドを変更する必要があります。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]