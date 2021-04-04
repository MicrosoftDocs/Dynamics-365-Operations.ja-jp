---
title: QRCODE ER 機能
description: このトピックでは、QRCODE 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92665936decc87b29f2fabb346f4d16745d0a30b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562664"
---
# <a name="qrcode-er-function"></a>QRCODE ER 機能

[!include [banner](../includes/banner.md)]

`QRCODE` 関数は、バイナリ形式の指定された文字列に対して、クイック応答コード (QRコード) イメージを表示する *コンテナー* 値を返します。

## <a name="syntax"></a>構文

```vb
QRCODE (text)
```

## <a name="arguments"></a>引数

`text`: *文字列*

オリジナルのテキストを表す *文字列* 値。

## <a name="return-values"></a>戻り値

*コンテナー*

結果のバイナリ ストリーム。

## <a name="example"></a>例

定義済みのテンプレートを使用して、電子報告 (ER) 形式をコンフィギュレーションし、Microsoft Office 形式 (Excel ブックまたは Word 文書) の送信ドキュメントを生成することができます。 このテンプレートには、QR コード画像のプレースホルダーとして **画像** オブジェクト (Excel ブック) または **画像コンテンツ コントロール** (Word 文書) を含めることができます。 コンフィギュレーションされた ER 形式に、このプレースホルダーを塗りつぶすために使用する **セル** 要素を追加する必要があります。 QR コードにどの情報を格納するかを指定するには、この **セル** 要素に対してバインドを定義する必要があります。 たとえば、次の式を含むようにバインドをコンフィギュレーションできます。

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

コンフィギュレーションされた ER 形式を実行すると、**model.ListOfShelfLabels** データ ソースの **LabelText** フィールドは QR コード画像を生成するために使用されます。 この画像は、送信ドキュメントを生成するために使用するドキュメント テンプレートの QR コード画像のプレースホルダーを置き換えます。 生成されたドキュメントの画像がスキャンされると、**model.ListOfShelfLabels** データ ソースの **LabelText** フィールドから取得されたテキストを返します。 詳細については、[ER を使用して生成されるドキュメントへの画像や図形の埋め込み](electronic-reporting-embed-images-shapes.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]