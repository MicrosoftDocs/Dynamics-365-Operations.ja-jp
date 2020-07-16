---
title: ProjectGroupNode クラス
description: このトピックでは、ProjectGroupNode クラスについて説明します。
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
ms.openlocfilehash: 3edba6caab410d9687bbbea89ea59d0453539fc3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502873"
---
# <a name="class-projectgroupnode"></a>クラス ProjectGroupNode

[!include [banner](../../includes/banner.md)]

```xpp
class ProjectGroupNode extends TreeNode
```

ProjectGroupNode クラスは、プロジェクト内のグループ ノードを表します。

## <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\]) | 特定の要素の projectGroup を検索します。 特定のグループまたはプロジェクト全体を検索するために使用できます。                             |
| public str groupMask(\[str value\])                                                          |                                                                                                                                               |
| public str name(\[str value\])                                                               | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public boolean preventEditProperties(\[boolean value\])                                      |                                                                                                                                               |
| public GroupNodeType projectGroupType(\[GroupNodeType value\])                               |                                                                                                                                               |
| public void addUtilNode(UtilElementType type, str name)                                      | projectGroup にノードを追加します。                                                                                                              |
| public void addNode(TreeNode node)                                                           | ProjectGroup に既存のノードを追加します。                                                                                                    |

## <a name="method-findgroupmember"></a>メソッド findGroupMember

特定の要素の projectGroup を検索します。 特定のグループまたはプロジェクト全体を検索するために使用できます。

```xpp
public TreeNode findGroupMember(str name, UtilElementType type, [boolean searchSubgroups])
```

### <a name="parameters---findgroupmember"></a>パラメーター - findGroupMember

名前  
検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。

<!-- -->

タイプ  
検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。

<!-- -->

searchSubgroups  
検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。

### <a name="return-value---findgroupmember"></a>戻り値 - findGroupMember

オブジェクトが見つからない場合は、条件を満たす最初のオブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic にはなし) を返します。

### <a name="remarks---findgroupmember"></a>備考 - findGroupMember

このメソッドは ProjectNode にもあります。

## <a name="method-groupmask"></a>メソッド groupMask

```xpp
public str groupMask([str value])
```

### <a name="parameters---groupmask"></a>パラメーター - groupMask

値  

### <a name="return-value---groupmask"></a>戻り値 - groupMask

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

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

## <a name="method-preventeditproperties"></a>メソッド preventEditProperties

```xpp
public boolean preventEditProperties([boolean value])
```

### <a name="parameters---preventeditproperties"></a>パラメーター - preventEditProperties

値  

### <a name="return-value---preventeditproperties"></a>戻り値 - preventEditProperties

## <a name="method-projectgrouptype"></a>メソッド projectGroupType

```xpp
public GroupNodeType projectGroupType([GroupNodeType value])
```

### <a name="parameters---projectgrouptype"></a>パラメーター - projectGroupType

値  

### <a name="return-value---projectgrouptype"></a>戻り値 - projectGroupType

## <a name="method-addutilnode"></a>メソッド addUtilNode

projectGroup にノードを追加します。

```xpp
public void addUtilNode(UtilElementType type, str name)
```

### <a name="parameters---addutilnode"></a>パラメーター - addUtilNode

タイプ  
ノードの名前。

<!-- -->

名前  
ノードの名前。

### <a name="remarks---addutilnode"></a>備考 - addUtilNode

このメソッドは、ProjectNode クラスにもあります。

## <a name="method-addnode"></a>メソッド addNode

ProjectGroup に既存のノードを追加します。

```xpp
public void addNode(TreeNode node)
```

### <a name="parameters---addnode"></a>パラメーター - addNode

node  
追加するノード。

