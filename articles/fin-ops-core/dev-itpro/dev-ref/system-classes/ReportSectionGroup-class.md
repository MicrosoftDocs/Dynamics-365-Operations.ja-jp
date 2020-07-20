---
title: ReportSectionGroup クラス
description: このトピックでは、ReportSectionGroup クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e19e72ab3ef5b66b2001a2f5c052232b591f9e74
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502829"
---
# <a name="class-reportsectiongroup"></a>クラス ReportSectionGroup

[!include [banner](../../includes/banner.md)]

```xpp
class ReportSectionGroup extends TreeNode
```

ReportSectionGroup クラスは、レポート セクションのコレクションを定義します。

## <a name="remarks"></a>備考

レポート セクション グループは、ヘッダー セクション、本文セクション、フッター セクションを含めることができます。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスする必要があります。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                       | 説明                                                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public ReportSection addSection(ReportBlockType sectionType) |                                                                                                                           |
| public FieldId dataField(\[FieldId value\])                  |                                                                                                                           |
| public int delete()                                          |                                                                                                                           |
| public str name(\[str value\])                               | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public ReportSection section(ReportBlockType sectionType)    |                                                                                                                           |
| public TableId table(\[TableId value\])                      | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                     |

## <a name="method-addsection"></a>メソッド addSection

```xpp
public ReportSection addSection(ReportBlockType sectionType)
```

### <a name="parameters---addsection"></a>パラメーター - addSection

sectionType  

### <a name="return-value---addsection"></a>戻り値 - addSection

## <a name="method-datafield"></a>メソッド dataField

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a>パラメーター - dataField

値  

### <a name="return-value---datafield"></a>戻り値 - dataField

## <a name="method-delete"></a>メソッド delete

```xpp
public int delete()
```

### <a name="return-value---delete"></a>戻り値 - delete

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-section"></a>メソッド section

```xpp
public ReportSection section(ReportBlockType sectionType)
```

### <a name="parameters---section"></a>パラメーター - section

sectionType  

### <a name="return-value---section"></a>戻り値 - section

## <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a>パラメーター - table

値  

### <a name="return-value---table"></a>戻り値 - toBlob

オブジェクトに関連付けられたテーブル ID の現在の値。

