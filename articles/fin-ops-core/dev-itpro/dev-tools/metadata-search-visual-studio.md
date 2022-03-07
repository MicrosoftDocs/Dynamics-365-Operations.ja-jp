---
title: Visual Studio でのメタデータの検索
description: この記事では、メタデータ検索を使用して、任意のパターンやコンテンツのコードとメタデータを検索する方法について説明します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: 83303
ms.assetid: 4d686948-a78d-48fa-bbf8-28da7880eec7
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dca75c96b74cc73c770f6a0653ec06796193591
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783036"
---
# <a name="metadata-search-in-visual-studio"></a>Visual Studio でのメタデータの検索

[!include [banner](../includes/banner.md)]

この記事では、メタデータ検索を使用して、任意のパターンやコンテンツのコードとメタデータを検索する方法について説明します。

大量のコード ベースおよびメタデータを考えると、多くの場合特定の基準を満たすコード内のものを検索する必要があります。 たとえば、パターンを含む、または基準を満たしているメタデータ要素の名前が分からない場合があります。 メタデータ検索は、メタデータ検索ツール ウィンドウと移動先ウィンドウの 2 つのユーザー インターフェイスを通じて Visual Studio で公開されます。

## <a name="metadata-search-tool-window"></a>メタデータ検索ツール ウィンドウ

メタデータ検索ツール ウィンドウには **Dynamics 365 &gt; メタデータ検索** メニュー コマンドからアクセスすることができます。 検索クエリを入力して検索を開始します。 結果は、入力と同時にウィンドウへの入力が非同期で開始されます。 任意の結果行をダブルクリックして、検索クエリに一致する、対応する X++ コードまたはメタデータに移動することができます。

[![メタデータ検索ツール ウィンドウ。](./media/posted_metasearch.png)](./media/posted_metasearch.png)

また、1 つまたは複数の結果を選択して、右クリックし、これらの要素をプロジェクトに追加することができます。 検索結果とやりとりを開始するまで、検索の完了を待機する必要はありません。

[![メタデータ検索から新しいプロジェクトに追加します。](./media/addnewproject_metasearch.png)](./media/addnewproject_metasearch.png)

## <a name="navigate-to-window"></a>ウィンドウへの移動

**移動先** ウィンドウは、**Ctrl + ','** (コンマ区切り記号) ショートカット キーを使用して呼び出されます。 **Ctrl+‘,’** キーを押すと、Visual Studio の主要なドキュメント ウィンドウの右上隅にクエリ エントリ ボックスが表示されます。 また、Visual Studio の **編集** メニューから **移動先** ウィンドウにアクセスすることができます。 クエリを検索し、入力時に結果が表示されることを確認します。 検索が完了したら、進行状況インジケーターが停止します。 結果とやりとりを開始するために、検索の完了を待機する必要はありません。

[![ウィンドウに移動します。](./media/typeform_metasearch.png)](./media/typeform_metasearch.png)

## <a name="search-query-syntax"></a>クエリ構文を検索

ここでは、検索クエリの構文について説明し、クエリの例を示します。

### <a name="syntax"></a>構文

検索クエリは、この一般的なフォームの一連のフィルターで構成される検索文字列です。

```xml
<filter_1>:<filter_1_value> [<filter_2>:<filter_2_value> … [ <filter_N>:<filter_N\_value>]]
```

`<filter_i>` は、許容されるフィルター名の 1 つであり、<`filter_i_value>` はコンマで区切られた (場合によっては引用符で括られた) フィルター値です。

### <a name="filter-names"></a>フィルター名

- **名前**: 要素名ごとのフィルター処理。 これは既定のフィルターです。つまり、フィルター値を入力するだけで要素名とみなされます。 各コンマ区切り値は、許容可能な要素名です。
- **タイプ**: 要素タイプでフィルター処理してください。 各コンマ区切り値は、要素またはサブ要素タイプ (ルート タイプまたはサブタイプ) (つまりテーブル、クラス、フィールドなど) の名前にする必要があります。 フィルター処理のロジックは次のとおりです。

    `(roottype_1 OR roottype_2 OR … OR roottype_N) AND (subtype_1 OR subtype_2 OR … OR subtype_N)`

- **モデル**: モデル名ごとのフィルター。 各コンマ区切り値は、アプリケーションのモデル名にする必要があります。
- **プロパティ**: プロパティ フィルターを適用します。 各コンマ区切り値は、フォーム `property_name=property_value` に含まれている必要があります。
- **コード**: コード スニペットを使用してフィルタ処理し、コード スニペットを引用符で囲みます。 一致するソース コードは、指定されたコード スニペットを含む要素です。

検索ボックスで使用可能なドロップダウンリスト メニューを開いて、フィルターおよびフィルター構文の使用に関するヘルプを取得することができます。

[![メタデータ検索フィルター ボタン。](./media/metadatasearchfilter.jpg)]

## <a name="examples"></a>例

| クエリ文字列   | 目的       |
|--------------------------------|--------------------------------|
|`TrvExpTable` | トークンが単独である場合は、それは名前と見なされます。 したがって、名前に 「TrvExpTable」 を持つアプリケーションのすべてのものが検出されます。 |
|`type:form ccount`  | その名前に 「ccount」 を持つすべてのフォームを検索します。   |
|`type:form property:formtemplate=listpage` | 「ListPage」 に等しいプロパティ 「FormTemplate」 を含む、すべてのフォームを検索します。       |
|`type:table,formDesign property:"WorkflowDataSource=TrvExpTable"`              | テーブルの下で formDesign ノードを検索しますが、何も見つかりません。  |
|`type:form,formmenufunctionbuttoncontrol property:Text=@SYS311998` | (ラベル) 「@SYS311998」に等しいテキスト プロパティを含むすべてのメニュー機能ボタン コントロールを検索します。                        |
|`type:table,method name:insert` | メソッドの名前に 「insert」 を含むメソッドで、テーブルを検索します。 |
|`type:table,tableindex name:Export` | 「Export」 の単語を含むインデックス名で、テーブルを検索します。 |
|`type:table,tableindexfield name:xpNum` | インデックス フィールド名の 「xpNum」 で、テーブル インデックスを検索します。 |
|`type:table,tablefieldgroup name:EPNew`  |その名前内で「EPNew」を含む FieldGroups (テーブル内) を検索します。 |
|`type:form,formgridcontrol property:allowedit=no,heightmode=column` | 「いいえ」に等しいプロパティ **allowedit** および「列」に等しい heightmode を持つ、グリッド コントロールのフォームを検索します。 |
|`type:form,formtabcontrol property:arrangeMethod=Vertical,ViewEditMode=view,WidthMode=Auto` |  「垂直」に等しい arrangeMethod、「ビュー」に等しい ViewEditMode および「自動」に等しい WidthMode のプロパティを持つ、タブ コントロールのフォームを検索します。  |
|`type:form,formDesign property:"WorkflowDataSource=TrvExpTable"` |「TrvExpTable」の値に設定する FormDesign ノードで、「WorkflowDataSource」 プロパティを持つすべてのフォームを検索します。                 |
|`model:”Application Suite” type:formdesign property:style=simplelistdetail` | FormDesign ノードで simpleListDetail に設定するスタイル プロパティを持つ、アプリケーション スイート モデル内のすべてのフォームを検索します。             |
|`code:"return null"` | 「null を返す」を含むソース コード内で、すべての場所を検索します。 |
|`code:"element.lock()" type:form`   | スニペット 「element.lock()」 を含むソース コードのフォームで、すべての場所を検索します。   |
|`code:"insert" type:table,form`    | 「挿入」を含むフォームまたはテーブルのいずれかのソース コード内で、すべての場所を検索します。   |
|`code:"public display" type:form,method`  | 「公開表示」のコードを含む、すべてのフォーム メソッドを検索します。 |
|`type:formbuttoncontrol property:text=` | **空** テキスト プロパティを持つ、すべてのフォームのボタン コントロールを検索します。 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]