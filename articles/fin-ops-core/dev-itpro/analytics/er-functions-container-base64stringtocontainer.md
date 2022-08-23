---
title: Base64StringToContainer ER 関数
description: この記事では、Base64StringToContainer 電子申告 (ER) 関数の使用方法について説明します。
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 96dfffc3d899f1106c6c931efb08c941f5b3c1a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291237"
---
# <a name="base64stringtocontainer-er-function"></a>Base64StringToContainer ER 関数

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [関数](er-formula-language.md#Functions) は、指定された *文字列* 型の入力を *[コンテナー](er-functions-category-container.md)* 型のデータ項目に変換します。

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

![ER モデル マッピング デザイナー ページのサンプル データ ソース。](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>追加リソース

[コンテナー関数](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
