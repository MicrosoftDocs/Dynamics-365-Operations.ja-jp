---
title: Base64StringToContainer ER 関数
description: このトピックでは、Base64StringToContainer 電子申告 (ER) 関数の使用方法について説明します。
author: NickSelin
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6fd08d9a2522bdf497b1926c884a4583065d9f19
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754377"
---
# <a name="base64stringtocontainer-er-function"></a>Base64StringToContainer ER 関数

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [関数](er-formula-language.md#functions) は、指定された *文字列* 型の入力を *[コンテナー](er-functions-category-container.md)* 型のデータ項目に変換します。

## <a name="syntax"></a>構文

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>引数

`input`: *文字列*

*文字列* 型のデータ ソースの有効なパス。

## <a name="return-values"></a>戻り値

*コンテナー*

バイナリ ラージ オブジェクト (BLOB) 形式の結果バイナリ値。

## <a name="usage-notes"></a>使用上の注意

入力文字列が、バイナリからテキストへのエンコード スキームの正しい Base64 グループを提供しない場合、"パラメーターが無効です" という例外がスローされます。

## <a name="example"></a>例

モデル マッピングでは、次のデータ ソースを定義します。

- **DocuTypeGroup** アプリケーションの列挙を参照する *Dynamics 365 for Operations / 列挙型* タイプのルート **DocuTypeGroupEnum** データ ソース
- **CustTable** アプリケーション テーブルを参照する *Dynamics 365 for Operations / テーブル レコード* タイプのルート **Customer** データ ソース
- 次のように構成された の 方法で構成 された *計算フィールド* 型の **\#Media** データ ソース:

    - **Customer** データ ソースの子データ ソースとして追加されます。
    - 式 `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)` を含みます。

- 次のように構成された *計算フィールド* 型の **\#MediaAsBase64String** データ ソース:

    - **Customer.'\#Media'** データ ソースの子データ ソースとして追加されます。
    - 式 `Customer.'#Media'.'getFileContentAsBase64String()'` を含みます。

- 次のように構成された *計算フィールド* 型の **\#BlobFomBase64** データ ソース:

    - **Customer.'\#Media'** データ ソースの子データ ソースとして追加されます。
    - 式 `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'` を含みます。

この例では、**\#MediaAsBase64String** データ ソースは、現在のメディア添付ファイルのバイナリ コンテンツを、バイナリからテキストへのエンコード スキームの Base64 グループを表すテキストとしてエンコードします。 **\#BlobFomBase64** データ ソースは、Base64 文字列をデコードし、BLOB 形式のバイナリ値を返します。

![ER モデル マッピング デザイナー ページのサンプル データ ソース](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>追加リソース

[コンテナー関数](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]