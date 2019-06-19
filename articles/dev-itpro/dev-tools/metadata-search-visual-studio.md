---
title: Visual Studio でのメタデータの検索
description: この記事では、メタデータ検索を使用して、任意のパターンやコンテンツのコードとメタデータを検索する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 83303
ms.assetid: 4d686948-a78d-48fa-bbf8-28da7880eec7
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05e4f558cb72c3fca162ce0c0a6325e5905a3cc5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544133"
---
# <a name="metadata-search-in-visual-studio"></a>Visual Studio でのメタデータの検索

[!include [banner](../includes/banner.md)]

この記事では、メタデータ検索を使用して、任意のパターンやコンテンツのコードとメタデータを検索する方法について説明します。 

大量のコード ベースおよびメタデータを考えると、多くの場合特定の基準を満たすコード内のものを検索する必要があります。 パターンを含んでいるまたは基準を満たしているメタデータ要素の名前が分からない場合がよくあります。 メタデータ検索は、メタデータ検索ツール ウィンドウと移動先ウィンドウの 2 つのユーザー インターフェイスを通じて Visual Studio で公開されます。

## <a name="metadata-search-tool-window"></a>メタデータ検索ツール ウィンドウ
メタデータ検索ツール ウィンドウには **Dynamics 365 &gt; メタデータ検索** メニュー コマンドからアクセスすることができます。 検索クエリを入力して検索を開始します。 結果は、入力と同時にウィンドウへの入力が非同期で開始されます。 任意の結果行をダブルクリックして、検索クエリに一致する、対応する X++ コードまたはメタデータに移動することができます。   

[![Posted\_MetaSearch](./media/posted_metasearch.png)](./media/posted_metasearch.png) 

また、1 つまたは複数の結果を選択して、右クリックし、これらの要素をプロジェクトに追加することができます。 検索結果とやりとりを開始するまで、検索の完了を待機する必要はありません。 

[![AddNewProject\_MetaSearch](./media/addnewproject_metasearch.png)](./media/addnewproject_metasearch.png)

## <a name="navigate-to-window"></a>ウィンドウへの移動
**移動先** ウィンドウは、**Ctrl + ','** (コンマ区切り記号) ショートカット キーを使用して呼び出されます。 **Ctrl+‘,’** キーを押すと、Visual Studio の主要なドキュメント ウィンドウの右上隅にクエリ エントリ ボックスが表示されます。 また、Visual Studio の **編集** メニューから **移動先** ウィンドウにアクセスすることができます。 クエリを検索し、入力時に結果が表示されることを確認します。 検索が完了したら、進行状況インジケーターが停止します。 結果とやりとりを開始するために、検索の完了を待機する必要はありません。 

[![TypeForm\_MetaSearch](./media/typeform_metasearch.png)](./media/typeform_metasearch.png)

## <a name="search-query-syntax"></a>クエリ構文を検索
ここでは、検索クエリの構文について説明し、クエリの例を示します。

### <a name="syntax"></a>構文

検索クエリは、この一般的な形式の一連のフィルターで構成される検索文字列です。*&lt;filter\_1&gt;:&lt;filter\_1\_value&gt; \[&lt;filter\_2&gt;:&lt;filter\_2\_value&gt;… \[ &lt;filter\_N&gt;:&lt;filter\_N\_value&gt;\]\]*、ここで *&lt;filter\_i&gt;* は許容されるフィルター名の 1 つで、*&lt;filter\_i\_value&gt;* はカンマ区切り (クォーテーションの場合もあり) のフィルタリング値です。

### <a name="filter-names"></a>フィルター名

-   **名前**: 要素名ごとのフィルター処理。 これは既定のフィルターです。つまり、フィルター値を入力するだけで要素名とみなされます。 各コンマ区切り値は、許容可能な要素名です。
-   **タイプ**: 要素タイプでフィルター処理してください。 各コンマ区切り値は、要素またはサブ要素タイプ (ルート タイプまたはサブタイプ) (テーブル、クラス、フィールドなど) にする必要があります。 フィルター処理のロジックは次のとおりです。

<!-- -->

-   **(roottype\_1 OR roottype\_2 OR … OR roottype\_N) および (subtype\_1 OR subtype\_2 OR … OR subtype\_N)**



-   **モデル**: モデル名ごとのフィルター。 各コンマ区切り値は、アプリケーションのモデル名にする必要があります。
-   **プロパティ**: プロパティ フィルターを適用します。 各コンマ区切り値は、フォームの *property\_name=property\_value* にする必要があります。
-   **コード**: コード スニペットを使用してフィルタ処理し、コード スニペットを引用符で囲みます。 一致するソース コードは、指定されたコード スニペットを含む要素です。

検索ボックスで使用可能なドロップダウンリスト メニューを開いて、フィルターおよびフィルター構文の使用に関するヘルプを取得することができます。

[metadatasearchfilter](./media/metadatasearchfilter.jpg)

## <a name="examples"></a>例

|                               <strong>クエリ文字列</strong>                               |                                                        <strong>目的</strong>                                                         |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
|                                        TrvExpTable                                        | トークンが単独である場合は、それは名前と見なされます。 したがって、名前に 'TrvExpTable' を持つアプリケーションのすべてのものが検出されます。 |
|                                     type:form ccount                                      |                                              その名前の「アカウント」を持つすべてのフォームを検索します。                                              |
|                         type:form property:formtemplate=listpage                          |                                「ListPage」に等しい「FormTemplate」のプロパティを含む、すべてのフォームを検索します。                                 |
|              type:table,formDesign property:"WorkflowDataSource=TrvExpTable"              |                                         テーブルの下で formDesign ノードを検索しますが、何も見つかりません。                                         |
|             type:form,formmenufunctionbuttoncontrol property:Text=@SYS311998              |                       (ラベル) 「@SYS311998」に等しいテキスト プロパティを含むすべてのメニュー機能ボタン コントロールを検索します。                        |
|                               type:table,method name:insert                               |                                      メソッドの名前に「挿入」を含むメソッドで、テーブルを検索します。                                      |
|                             type:table,tableindex name:Export                             |                                        「エクスポート」の単語を含むインデックス名で、テーブルを検索します。                                         |
|                           type:table,tableindexfield name:xpNum                           |                                          インデックス フィールド名の「xpNum」で、テーブル インデックスを検索します。                                           |
|                           type:table,tablefieldgroup name:EPNew                           |                                       その名前内で「EPNew」を含む FieldGroups (テーブル内) を検索します。                                       |
|             type:form,formgridcontrol property:allowedit=no,heightmode=column             |                     「いいえ」に等しい allowedit のプロパティおよび「列」に等しい heightmode を持つ、グリッド コントロールのフォームを検索します。                      |
| type:form,formtabcontrol property:arrangeMethod=Vertical,ViewEditMode=view,WidthMode=Auto |  「垂直」に等しい arrangeMethod、「ビュー」に等しい ViewEditMode および「自動」に等しい WidthMode のプロパティを持つ、タブ コントロールのフォームを検索します。  |
|              type:form,formDesign property:"WorkflowDataSource=TrvExpTable"               |                「TrvExpTable」の値に設定する FormDesign ノードで「WorkflowDataSource」プロパティを持つ、すべてのフォームを検索します。                 |
|         model:”Application Suite” type:formdesign property:style=simplelistdetail         |            FormDesign ノードで simpleListDetail に設定するスタイル プロパティを持つ、アプリケーション スイート モデル内のすべてのフォームを検索します。             |
|                                    code:”return null”                                     |                                       「Null を返す」を含むソース コード内で、すべての場所を検索します。                                       |
|                              code:"element.lock()" type:form                              |                             スニペット 「element.lock()」を含むソース コードのフォームで、すべての場所を検索します。                             |
|                               code:"insert" type:table,form                               |                             「挿入」を含むフォームまたはテーブルのいずれかのソース コード内で、すべての場所を検索します。                             |
|                          code:"public display" type:form,method                           |                                        「公開表示」のコードを含む、すべてのフォーム メソッドを検索します。                                        |
|                           type:formbuttoncontrol property:text=                           |                               <strong>空</strong>テキスト プロパティを持つ、すべてのフォームのボタン コントロールを検索します。                               |

