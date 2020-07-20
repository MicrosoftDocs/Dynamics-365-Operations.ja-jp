---
title: DocNode クラス
description: このトピックでは、DocNode クラスについて説明します。
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
ms.openlocfilehash: a663a384aab5c07a24dbfa66b70a2c80e47f1e66
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502672"
---
# <a name="class-docnode"></a>クラス DocNode

[!include [banner](../../includes/banner.md)]

```xpp
class DocNode extends TreeNode
```

DocNode クラスは、ドキュメント ノードの情報や機能を提供します。

## <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                            | 説明                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                                                                                                                                                         | ノードのソース コードを返します。                                                                                                   |
| public str changedBy(\[str value\])                                                                                                                                                               | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                              |
| public Date changedDate(\[Date value\])                                                                                                                                                           | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                      |
| public str changedTime(\[str value\])                                                                                                                                                             | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                      |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                                                                                                          | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public str createdBy(\[str value\])                                                                                                                                                               | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                   |
| public Date creationDate(\[Date value\])                                                                                                                                                          | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                           |
| public str creationTime(\[str value\])                                                                                                                                                            |                                                                                                                                         |
| public str description(\[str value\])                                                                                                                                                             | ドキュメント ノードの説明を設定するか返します。                                                                              |
| public str name(\[str value\])                                                                                                                                                                    | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededAccessLevel(\[int value\])                                                                                                                                                       | MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。                                                                 |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                                                                                                         | ドキュメント ノードのセキュリティ キーを設定するか返します。                                                                            |
| public str title(\[str value\])                                                                                                                                                                   | ドキュメント ノードのタイトルを設定するか返します。                                                                                    |
| ::public static DocNode findAOTElementDocNode(ApplCodeDocType HelpType, str Name, \[str ParentName\], \[int Mode\])                                                                               | アプリケーション オブジェクト ツリー (AOT) で要素ドキュメント ノードの検索を実行します。                         |
| ::public static DocNode findApplicationDocNode(ApplHelpType HelpType, str Name, \[str ParentName\], \[int Mode\])                                                                                 | アプリケーション要素ドキュメント ノードの検索を実行します。                                                                        |
| ::public static DocNode findKernelDocNode(KernelHelpType HelpType, str Name, \[str ParentName\], \[int Mode\])                                                                                    | カーネル要素ドキュメント ノードの検索を実行します。                                                                              |
| ::public static DocNode getNodeDetached(UtilFileType helpType, int UtilType, str Name, \[int ParentId\], \[int Type\], \[UtilEntryLevel Utillevel\], \[boolean Forcelevel\], \[boolean OldUtil\]) | 指定したドキュメントのノードを返します。                                                                                               |
| public void AOTsetSource(str source, \[boolean isStatic\])                                                                                                                                        | ノードのソース コードを設定します。                                                                                                      |
| public void AOTedit(\[int Line\], \[int Column\])                                                                                                                                                 | このノードの適切なエディタを開きます。                                                                                             |

## <a name="method-aotgetsource"></a>メソッド AOTgetSource

ノードのソース コードを返します。

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a>戻り値 - AOTgetSource

文字列としてのノードのソースコード。ノードのソース コードがない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  
ドキュメント ノードを変更したユーザーとして割り当てられている値。

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  
ドキュメント ノードの変更日として割り当てられている値。

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  
ドキュメント ノードの変更時刻として割り当てられている値。

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  
構成キー ID に割り当てられている値。

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

コントロールに割り当てられるコンフィギュレーションの ID。

### <a name="remarks---configurationkey"></a>備考 - configurationKey

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  
ドキュメント ノードを作成したユーザーとして割り当てられている値。

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  
ドキュメント ノードの作成日として割り当てられている値。

### <a name="return-value---creationdate"></a>戻り値 - creationDate

アプリケーション オブジェクトが作成された日付。

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-description"></a>メソッドの説明

ドキュメント ノードの説明を設定するか返します。

```xpp
public str description([str value])
```

### <a name="parameters---description"></a>パラメーター - description

値  
ドキュメント ノードの説明として割り当てられている値。

### <a name="return-value---description"></a>戻り値 - description

ドキュメント ノードの説明の入力

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - 名前

値  
ドキュメント ノードに割り当てられている名前。

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - 名前

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-neededaccesslevel"></a>メソッド neededAccessLevel

MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。

```xpp
public int neededAccessLevel([int value])
```

### <a name="parameters---neededaccesslevel"></a>パラメーター - neededAccessLevel

値  

### <a name="return-value---neededaccesslevel"></a>戻り値 - neededAccessLevel

neededAccessLevel プロパティの現在の値。

### <a name="remarks---neededaccesslevel"></a>備考 - neededAccessLevel

AccessType システム列挙値の使用可能な値は次のとおりです。

-   AccessType::NoAccess。
-   AccessType::View。
-   AccessType::Edit。
-   AccessType::Add。
-   AccessType::Delete。

## <a name="method-securitykey"></a>メソッド securityKey

ドキュメント ノードのセキュリティ キーを設定するか返します。

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  
セキュリティ キー ID に割り当てられている値。

### <a name="return-value---securitykey"></a>戻り値 - securityKey

ドキュメント ノードのセキュリティ キー ID。ドキュメント ノードにセキュリティ キーが関連付けられていない場合は 0 (ゼロ)。

## <a name="method-title"></a>メソッド title

ドキュメント ノードのタイトルを設定するか返します。

```xpp
public str title([str value])
```

### <a name="parameters---title"></a>パラメーター - title

値  
ドキュメント ノードに割り当てられているタイトル。

### <a name="return-value---title"></a>戻り値 - title

ドキュメント ノードのタイトル。

## <a name="method-findaotelementdocnode"></a>メソッド findAOTElementDocNode

アプリケーション オブジェクト ツリー (AOT) で要素ドキュメント ノードの検索を実行します。

```xpp
public static DocNode findAOTElementDocNode(ApplCodeDocType HelpType, str Name, [str ParentName], [int Mode])
```

### <a name="parameters---findaotelementdocnode"></a>パラメーター - findAOTElementDocNode

HelpType  
検索に使用するモード (オプション)。

<!-- -->

氏名  
検索に使用するモード (オプション)。

<!-- -->

ParentName  
検索に使用するモード (オプション)。

<!-- -->

モード  
検索に使用するモード (オプション)。

### <a name="return-value---findaotelementdocnode"></a>戻り値 - findAOTElementDocNode

検出されたノード。それ以外の場合は、null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

## <a name="method-findapplicationdocnode"></a>メソッド findApplicationDocNode

アプリケーション要素ドキュメント ノードの検索を実行します。

```xpp
public static DocNode findApplicationDocNode(ApplHelpType HelpType, str Name, [str ParentName], [int Mode])
```

### <a name="parameters---findapplicationdocnode"></a>パラメーター - findApplicationDocNode

HelpType  
検索に使用するモード (オプション)。

<!-- -->

氏名  
検索に使用するモード (オプション)。

<!-- -->

ParentName  
検索に使用するモード (オプション)。

<!-- -->

モード  
検索に使用するモード (オプション)。

### <a name="return-value---findapplicationdocnode"></a>戻り値 - findApplicationDocNode

検出されたノード。ノードが検出されなかった場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

## <a name="method-findkerneldocnode"></a>メソッド findKernelDocNode

カーネル要素ドキュメント ノードの検索を実行します。

```xpp
public static DocNode findKernelDocNode(KernelHelpType HelpType, str Name, [str ParentName], [int Mode])
```

### <a name="parameters---findkerneldocnode"></a>パラメーター - findKernelDocNode

HelpType  
検索に使用するモード (オプション)。

<!-- -->

氏名  
検索に使用するモード (オプション)。

<!-- -->

ParentName  
検索に使用するモード (オプション)。

<!-- -->

モード  
検索に使用するモード (オプション)。

### <a name="return-value---findkerneldocnode"></a>戻り値 - findKernelDocNode

検出されたノード。それ以外の場合は、null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

## <a name="method-getnodedetached"></a>メソッド getNodeDetached

指定したドキュメントのノードを返します。

```xpp
public static DocNode getNodeDetached(UtilFileType helpType, int UtilType, str Name, [int ParentId], [int Type], [UtilEntryLevel Utillevel], [boolean Forcelevel], [boolean OldUtil])
```

### <a name="parameters---getnodedetached"></a>パラメーター - getNodeDetached

helpType  
引当済。省略可能です。

<!-- -->

UtilType  
引当済。省略可能です。

<!-- -->

氏名  
引当済。省略可能です。

<!-- -->

ParentId  
引当済。省略可能です。

<!-- -->

種類  
引当済。省略可能です。

<!-- -->

Utillevel  
引当済。省略可能です。

<!-- -->

Forcelevel  
引当済。省略可能です。

<!-- -->

OldUtil  
引当済。省略可能です。

### <a name="return-value---getnodedetached"></a>戻り値 - getNodeDetached

指定したドキュメントのノードです。

## <a name="method-aotsetsource"></a>メソッド AOTsetSource

ノードのソース コードを設定します。

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a>パラメーター - AOTsetSource

ソース  
メソッドが静的かどうかを示すブール値。

<!-- -->

isStatic  
メソッドが静的かどうかを示すブール値。

## <a name="method-aotedit"></a>メソッド AOTedit

このノードの適切なエディタを開きます。

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a>パラメーター - AOTedit

折れ線  
カーソル位置の列 (オプション)。

<!-- -->

円柱  
カーソル位置の列 (オプション)。

### <a name="remarks---aotedit"></a>備考 - AOTedit

ノードがメソッドである場合は、コード エディタが開きます。 ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。

