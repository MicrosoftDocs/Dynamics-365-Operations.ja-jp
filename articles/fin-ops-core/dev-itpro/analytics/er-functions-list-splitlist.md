---
title: SPLITLIST ER 関数
description: このトピックでは、SPLITLIST 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: ef0b548173a01cc5a15fcfb743dfb29397c1349b3c2926fa6401399459d07026
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776125"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER 関数

[!include [banner](../includes/banner.md)]

`SPLITLIST` 関数は、指定されたリストをサブリスト (またはバッチ) に分割します。各サブリストには指定されたレコード数が含まれます。 その後、結果をバッチで構成された新しい *レコード リスト* 値として返します。

## <a name="syntax-1"></a>構文 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>構文 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`number`: *整数*

バッチごとのレコードの最大数

`on-demand reading flag`: *ブール値*

サブリストの要素をオンデマンドで生成すべきかどうかを指定する *ブール* 値。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

返されるバッチのリストには、次の要素が含まれます。

 - **値:** *リスト*

    現在のバッチに属するレコードのリスト。

- **Batchnumber:** *整数*

    返されたリスト内の現在のバッチ数。

需要の読み取りフラグが **True** に設定されている場合、サブリストは要求時に生成され、メモリ消費の減少が可能になりますが、要素が順番に使用されていないと、パフォーマンスが低下する可能性があります。

## <a name="example"></a>例

次の図では、**明細行** データ ソースが、3 つのレコードがあるレコード リストとして作成されます。 このリストは、それぞれ最大 2 つのレコードを含むバッチに分割されます。

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

次の図は、設計された形式レイアウトを示します。 この形式のレイアウトでは、XML 形式で出力を生成するために作成される **明細行** データ ソースにバインディングされます。 この出力は、各バッチとその中のレコードに対する個々のノードを表示します。

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

次の図は、設計された形式が実行される際の結果を示します。

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
