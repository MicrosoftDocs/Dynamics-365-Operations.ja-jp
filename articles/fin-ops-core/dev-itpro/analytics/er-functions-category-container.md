---
title: コンテナー カテゴリ内の ER 関数のリスト
description: この記事では、電子申告 (ER) でサポートされるコンテナー関数について説明します。
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
ms.openlocfilehash: f07c3645f824fc2fe8ca156c8cf06840e993a9a5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282654"
---
# <a name="list-of-er-functions-in-the-container-category"></a>コンテナー カテゴリ内の ER 関数のリスト

[!include [banner](../includes/banner.md)]

[電子申告 (ER)](general-electronic-reporting.md) コンテナー [関数](er-formula-language.md#Functions) を使用して、*コンテナー* データ型のデータ ソースを含む操作を実行するために使用できます。 これらの操作は、処理データがバイナリ ラージ オブジェクト (BLOB) 形式でバイナリ データのコレクションを表す場合に発生します。 この記事では、これらの関数の概要を示します。

## <a name="list-of-supported-functions"></a>サポートされている関数のリスト

| 関数 | 説明 |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | この関数は、バイナリからテキストへのエンコード スキームの Base64 グループを表す、指定された ASCII 文字列からデコードされるバイナリ コンテンツで構成される *コンテナー* 値を返します。 |

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子報告のフォーミュラ言語](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
