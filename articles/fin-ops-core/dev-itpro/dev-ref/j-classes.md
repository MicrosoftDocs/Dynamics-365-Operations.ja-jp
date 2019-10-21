---
title: J クラス
description: 文字 J で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 58702
ms.assetid: e932e25e-b72a-428a-830a-20160e81e334
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 189bed51c39009dc3d112f9a49a9bdd5afb751aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191614"
---
# <a name="j-classes"></a>J クラス

[!include [banner](../includes/banner.md)]

文字 J で始まるシステム API クラス。

<a name="class-job"></a>クラス ジョブ
---------

    class Job extends TreeNode

Job クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | このノードのソース コードを返します。                                                                                                         |
| public str changedBy(\[str value\])                        | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])                    | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                            |
| public str changedTime(\[str value\])                      | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                            |
| public str createdBy(\[str value\])                        | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])                   | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                 |
| public str creationTime(\[str value\])                     |                                                                                                                                               |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                         |                                                                                                                                               |
| public void AOTsetSource(str source, \[boolean isStatic\]) | このノードのソース コードを設定します。                                                                                                            |
| public void AOTrun()                                       | アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。                                                |
| public void AOTedit(\[int Line\], \[int Column\])          | このノードの適切なエディタを開きます。                                                                                                   |

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null を参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
メソッドが静的かどうかを指定する値、オプション。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値、オプション。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

### <a name="method-aotrun"></a>メソッド AOTrun

アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。

    public void AOTrun()

### <a name="method-aotedit"></a>メソッド AOTedit

このノードの適切なエディタを開きます。

    public void AOTedit([int Line], [int Column])

#### <a name="parameters"></a>パラメーター

明細行  
カーソル位置の列 (オプション)。

<!-- -->

円柱  
カーソル位置の列 (オプション)。

#### <a name="remarks"></a>備考

ノードがメソッドである場合は、コード エディタが開きます。 ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。



