---
title: X++ 構文
description: このトピックには、X++ の構文リファレンスが含まれています。
author: RobinARH
manager: AnnBe
ms.date: 07/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 72211
ms.assetid: bb238a46-3a43-4f3c-a9b6-86b26e988881
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e931d3681f34772d137c5a2ae3e672e55ef2891f
ms.sourcegitcommit: 7eae20185944ff7394531173490a286a61092323
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2019
ms.locfileid: "2872651"
---
# <a name="x-syntax"></a>X++ 構文

[!include [banner](../includes/banner.md)]

このトピックには、X++ の構文リファレンスが含まれています。 

<a name="x-keywords"></a>X++ キーワード
------------

次の表に示す X++ キーワードは予約されています。 これらのキーワードは、他の目的に使用することはできません。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>予約語</th>
<th>説明</th>
<th>詳細情報</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>!</strong></td>
<td>ありません。</td>
<td>リレーショナル演算子</td>
</tr>
<tr class="even">
<td><strong>!=</strong></td>
<td>非等値演算子 (等しくない)。</td>
<td>リレーショナル演算子</td>
</tr>
<tr class="odd">
<td><strong>#</strong></td>
<td>マクロ名に接頭語を付けます。</td>
<td>方法: #define および #if を使用してマクロをテストする</td>
</tr>
<tr class="even">
<td><strong>&amp;</strong></td>
<td>バイナリ AND。</td>
<td>算術演算子</td>
</tr>
<tr class="odd">
<td><strong>&amp;&amp;</strong></td>
<td>論理 AND。</td>
<td>リレーショナル演算子</td>
</tr>
<tr class="even">
<td><strong>(</strong></td>
<td>関数呼び出し演算子は、関数呼び出しの開始を示します。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>)</strong></td>
<td>関数呼び出し演算子は、関数呼び出しの終了を示します。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><em></strong></td>
<td>乗算します。 アスタリスク (<span class="code"></em></span>) は、X++ SQL でも使用されます。 1 つの使用方法は、<code>select</code> ステートメントにおいてテーブルのすべてのフィールドを示すことです。 もう 1 つの使用法は、<code>like</code>演算子を持つワイルドカードとして、あらゆる種類の 0 から複数の文字表すことです。 <code>like</code> 演算子は、<span class="code">?</span> も使用します 文字。</td>
<td>算術演算子</td>
</tr>
<tr class="odd">
<td><strong>^</strong></td>
<td>バイナリ XOR。</td>
<td>算術演算子</td>
</tr>
<tr class="even">
<td><strong>|</strong></td>
<td>バイナリ OR。</td>
<td>算術演算子</td>
</tr>
<tr class="odd">
<td><strong>||</strong></td>
<td>論理 OR。</td>
<td>リレーショナル演算子</td>
</tr>
<tr class="even">
<td><strong>~</strong></td>
<td>ありません。</td>
<td>算術演算子</td>
</tr>
<tr class="odd">
<td><strong>+</strong></td>
<td>プラス。</td>
<td>算術演算子</td>
</tr>
<tr class="even">
<td><strong>++</strong></td>
<td>増分。</td>
<td>代入演算子</td>
</tr>
<tr class="odd">
<td><strong>+=</strong></td>
<td>割り当ての追加。</td>
<td>代入演算子</td>
</tr>
<tr class="even">
<td><strong>、</strong></td>
<td>コンマ演算子。 コンマで区切られた式は、左から右に評価されます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>-</strong></td>
<td>マイナス。</td>
<td>算術演算子</td>
</tr>
<tr class="even">
<td><strong>--</strong></td>
<td>デクリメント演算子。</td>
<td>代入演算子</td>
</tr>
<tr class="odd">
<td><strong>-=</strong></td>
<td>減算する割り当て。</td>
<td>代入演算子</td>
</tr>
<tr class="even">
<td><strong>。</strong></td>
<td>クラス メンバー アクセス演算子、たとえば、<code>formRun.run</code> は、クラス型 <code>FormRun</code> のオブジェクトの <code>run</code> メソッドにアクセスします。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>/</strong></td>
<td>分割。</td>
<td>算術演算子</td>
</tr>
<tr class="even">
<td><strong>&lt;/strong&gt;</td>
<td>文字列でエスケープします。 余分な引用符およびタブの <span class="code">\t</span> などの特定の文字をエスケープします。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>@</strong></td>
<td>キーワードのエスケープです。 たとえば、<span class="code">str<xref href="abstract" data-throw-if-not-resolved="False" data-raw-source="@abstract"></xref>;</span> は <strong>@</strong> 記号なしではコンパイルに失敗します 。 また \ エスケープ文字の効果を否定すること、およびソース コード内の 1 つ以上の明細行にまたがる文字列を有効にすることによってリテラル文字列にも影響を及ぼします。 新しい行は 16 進数 0x0A の 1 文字で表され、これは一般に改行と呼ばれます。 0x0D0A のように 16 進数 0x0D のキャリッジ リターン文字は含まれません。</td>
<td></td>
</tr>
<tr class="even">
<td><strong>: </strong></td>
<td>フィールド申告またはラベル指定子。 コロン (<span class="code">:</span>) 文字も <code>switch</code> 明細書で使用されます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>::</strong></td>
<td>静的 (class) メソッド <span class="code">ClassName::methodName</span> を呼び出すときに使用します。</td>
<td></td>
</tr>
<tr class="even">
<td><strong>;</strong></td>
<td>ステートメントを終了します。 <code>for</code> ループまたは文の区切り記号として使用されます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>&lt;</strong></td>
<td>より小さい。</td>
<td>リレーショナル演算子</td>
</tr>
<tr class="even">
<td><strong>&lt;&lt;</strong></td>
<td>左 Shift。</td>
<td>算術演算子</td>
</tr>
<tr class="odd">
<td><strong>&lt;=</strong></td>
<td>以下。</td>
<td>算術演算子</td>
</tr>
<tr class="even">
<td><strong>=</strong></td>
<td>代入演算子。 &quot;<strong>=</strong>&quot; の左側の引数は、右側の引数の値に設定されます。</td>
<td>代入演算子</td>
</tr>
<tr class="odd">
<td><strong>==</strong></td>
<td>両方の式が等しい場合は、true を返します。</td>
<td>リレーショナル演算子</td>
</tr>
<tr class="even">
<td><strong>&gt;</strong></td>
<td>より大きい。</td>
<td>リレーショナル演算子</td>
</tr>
<tr class="odd">
<td><strong>&gt;=</strong></td>
<td>以上。</td>
<td>リレーショナル演算子</td>
</tr>
<tr class="even">
<td><strong>&gt;&gt;</strong></td>
<td>右 Shift</td>
<td>算術演算子</td>
</tr>
<tr class="odd">
<td><strong>?</strong></td>
<td>三項演算子。 疑問符 (<span class="code">?</span>) 文字は、<code>like</code> 演算子がどのような種類の文字でも正確に表すために使用されます。 <code>like</code> 演算子は、<span class="code"><em></span> 文字も使用します。</td>
<td>三項演算子 (?)</td>
</tr>
<tr class="even">
<td><strong>[</strong></td>
<td>配列宣言子、開きます。 &quot;<strong>]</strong>&quot; とともに使用する必要があります。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>]</strong></td>
<td>配列宣言子、閉じます。 &quot;<strong>[</strong>&quot; とともに使用する必要があります。</td>
<td></td>
</tr>
<tr class="even">
<td><strong>{</strong></td>
<td>ステートメントの番号の先頭を示します。 これらのステートメントの最後には、&quot;<strong>}</strong>&quot; が続かなければなりません。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>}</strong></td>
<td>ステートメントの番号の最後を示します。 &quot;<strong>{</strong>&quot; は、これらのステートメントの最初よりも前にある必要があります。</td>
<td></td>
</tr>
<tr class="even">
<td><strong>抽象</strong></td>
<td>クラスとメソッドのモディファイア。 <strong>抽象</strong>クラスは<strong>新規</strong>キーワードで構築することはできません。 <strong>抽象</strong>メソッドを呼び出すことはできません。 テーブルは、AOT で<span class="ui">抽象</span>プロパティを<span class="ui">はい</span>に設定するか、<code>DictTable</code> クラスを使用して、抽象として変更することもできます。 <span class="ui">抽象</span> プロパティの既定値は <span class="ui">いいえ</span> であり、別のテーブルによりテーブルが拡張されない限り設定することはできません。 抽象テーブルの各行は、派生テーブルに依存する行が必要です。 これは、抽象テーブルの各行が <span class="ui">InstanceRelationType</span> プロパティ フィールドで 0 より大きい値を持つことを意味します。 マーキングを抽象としてマークすることによる他の効果はありません。 非公式に、プログラマは <span class="term">concrete</span> という用語を使用して<strong>抽象</strong>ではないクラスを記述します。</td>
<td>メソッド モディファイアー テーブル継承の概要</td>
</tr>
<tr class="odd">
<td><strong>anytype</strong></td>
<td>このメソッドは任意のデータ型を返すことができます。</td>
<td>Anytype</td>
</tr>
<tr class="even">
<td><strong>利用品目</strong></td>
<td>派生クラス変数に基本クラス変数を割り当てるときに必要です。 たとえば、<code>Base</code>クラスを<strong>拡張</strong>する指定された <code>Derived</code> クラスでは、明細書の<code>myDerived = myBase as Derived;</code> は <strong>as</strong> キーワードを使用して、コンパイラ エラーを避けます。 このキーワードは、ベース テーブル変数を派生テーブル変数に割り当てるときにも適用されます。</td>
<td>式の演算子: 継承の Is および As</td>
</tr>
<tr class="odd">
<td><strong>asc</strong></td>
<td><code>select</code>ステートメント <code>order</code> <code>by</code> または <code>group</code> <code>by</code> 句のオプション。 並べ替えは昇順です。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>時刻</strong></td>
<td>印刷ウィンドウの位置を指定します。</td>
<td>ステートメントの印刷</td>
</tr>
<tr class="odd">
<td><strong>平均</strong></td>
<td><code>select</code> ステートメント内の <code>group by</code> 句により指定された行からフィールドの平均を返します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>分割</strong></td>
<td>コード ブロックをすぐに終了します。</td>
<td>Break ステートメント</td>
</tr>
<tr class="odd">
<td><strong>ブレークポイント</strong></td>
<td>デバッグのために設定されているブレークポイントを表します。 コードにブレークポイントを設定するには、次のように記述します。<code>breakpoint;</code></td>
<td></td>
</tr>
<tr class="even">
<td><strong>作成者</strong></td>
<td>グループ化と並べ替えの基準となる予約語の一部。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>byref</strong></td>
<td>呼び出されたメソッドに渡されるパラメーターが、値ではなく参照 (アドレス) により渡されることを指定します。 <strong>Byref</strong> は、参照によってパラメータをとる .NET メソッドを呼び出すときに X++ で使用されます (C# のキーワード <strong>out</strong> or <strong>ref</strong> など)。</td>
<td>方法: CLR Interop に byref キーワードを使用します。</td>
</tr>
<tr class="even">
<td><strong>Case など</strong></td>
<td><code>switch</code> ステートメント内の選択。</td>
<td>Switch ステートメント</td>
</tr>
<tr class="odd">
<td><strong>catch</strong></td>
<td>例外処理で使用されます。</td>
<td>トライおよびキャッチ キーワードの例外処理</td>
</tr>
<tr class="even">
<td><strong>changeCompany</strong></td>
<td>データベース設定を別の会社に変更します。</td>
<td>会社の設計パターンを変更する</td>
</tr>
<tr class="odd">
<td><strong>クラス</strong></td>
<td>クラスを宣言します。</td>
<td>X++ のクラス</td>
</tr>
<tr class="even">
<td><strong>クライアント</strong></td>
<td>メソッド モディファイアー｡</td>
<td>メソッド モディファイアー</td>
</tr>
<tr class="odd">
<td><strong>コンテナー</strong></td>
<td>型 <code>container</code> の変数を指定します。</td>
<td>コンテナー</td>
</tr>
<tr class="even">
<td><strong>続行</strong></td>
<td>ループの次の繰り返しを強制します。</td>
<td>明細書の続行</td>
</tr>
<tr class="odd">
<td><strong>カウント</strong></td>
<td><code>select</code> ステートメント内の <code>group by</code> 句により指定された行からレコードの数を返します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>crossCompany</strong></td>
<td><code>select</code> 明細書は、ユーザーが読み取りを承認されているすべての会社のデータを戻します。</td>
<td>会社間の X++ Code の基礎</td>
</tr>
<tr class="odd">
<td><strong>日付</strong></td>
<td>型 <code>date</code> の変数を指定します。</td>
<td>日付</td>
</tr>
<tr class="even">
<td><strong>既定</strong></td>
<td><code>switch</code>明細書内の既定ケース</td>
<td>Switch ステートメント</td>
</tr>
<tr class="odd">
<td><strong>デリゲート</strong></td>
<td>他のクラスのメソッドへの複数の参照を格納し、これを行うように求められる場合にメソッドを呼び出すことができるクラス メンバー。 デリゲートは、次のようなさまざまな種類のメソッドへの参照を保存できます。
<ul>
<li>X++ クラスの静的メソッド</li>
<li>X++ クラスのインスタンス メソッド</li>
<li>.NET Framework クラスのメソッド</li>
</ul></td>
<td>イベント用語およびキーワード X++、C# 比較: イベント</td>
</tr>
<tr class="even">
<td><strong>delete_from</strong></td>
<td>同時に複数のレコードをデータベースから削除できます。</td>
<td>delete_from</td>
</tr>
<tr class="odd">
<td><strong>desc</strong></td>
<td><code>select</code> ステートメント <code>order by</code> または <code>group by</code> 句のオプション。 並べ替えは降順です。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>表示</strong></td>
<td>メソッド モディファイアー｡</td>
<td>メソッド モディファイアー</td>
</tr>
<tr class="odd">
<td><strong>div</strong></td>
<td>整数除算。</td>
<td>算術演算子</td>
</tr>
<tr class="even">
<td><strong>実行</strong></td>
<td>ループ<code>do...while</code>の開始</td>
<td>while Loops を実行</td>
</tr>
<tr class="odd">
<td><strong>編集</strong></td>
<td>メソッド モディファイアー｡</td>
<td>メソッド モディファイアー</td>
</tr>
<tr class="even">
<td><strong>その他</strong></td>
<td>条件付き実行 (<code>if...else</code>)。</td>
<td>if および if ... else ステートメント</td>
</tr>
<tr class="odd">
<td><strong>eventHandler</strong></td>
<td><span class="code">+=</span> or <span class="code">-=</span> 演算子を使用して、デリゲートのメソッドの参照を追加または削除するたびに使用する必要があります。 例: <span class="code">myDelegate += eventHandler(OtherClass::myStaticMethod);</span></td>
<td>イベント用語およびキーワード X++、C# 比較: イベント</td>
</tr>
<tr class="even">
<td><strong>あり</strong></td>
<td><code>select</code> 文の <code>join</code> 句で使用されます。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>拡張</strong></td>
<td>クラスまたはインターフェイス申告句。 クラスが明示的に別のクラスを拡張しない場合、クラスは <code>Object</code> クラスの拡張を検討します (&quot;オブジェクトを拡張&quot; と記述した場合のように)。</td>
<td>サブクラスを作成しています</td>
</tr>
<tr class="even">
<td><strong>いいえ</strong></td>
<td>ブール型リテラル。</td>
<td>ブール型</td>
</tr>
<tr class="odd">
<td><strong>最終</strong></td>
<td>クラスとメソッドのモディファイア。</td>
<td>メソッド モディファイアー</td>
</tr>
<tr class="even">
<td><strong>firstFast</strong></td>
<td><code>select</code> 文で使用され、最初の行のフェッチを高速化します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>firstOnly</strong></td>
<td>最初のレコードだけをフェッチするために <code>select</code> 文で使用されます。 <code>firstOnly</code> キーワードは、X++ SQL <code>select</code> ステートメントによって最大 1 つのレコードの取得されることを保証しません。 AOS が <code>EntireTable</code> キャッシュを使用し、<code>select</code> ステートメントのデータ要求を満たすことができる場合は、<code>firstOnly</code> キーワードは無視されます。</td>
<td>ステートメント構文セットに基づくキャッシュを選択</td>
</tr>
<tr class="even">
<td><strong>firstOnly10</strong></td>
<td><strong>firstOnly</strong> と同じ。ただし、1 行ではなく 10 行を返します。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>firstOnly100</strong></td>
<td><strong>firstOnly</strong> と同じ。ただし、1 行ではなく 100 行を返します。</td>
<td></td>
</tr>
<tr class="even">
<td><strong>firstOnly1000</strong></td>
<td><strong>firstOnly</strong> と同じ。ただし、1 行ではなく 1000 行を返します。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>フラッシュ</strong></td>
<td>テーブル キャッシュ全体をクリアします。 <code>flush</code> ステートメントの構文を次に示します: <code>YourTable ytBuffer;</code>  <code>flush ytBuffer;</code></td>
<td>セット ベースのキャッシュ</td>
</tr>
<tr class="even">
<td><strong>の</strong></td>
<td>ループの繰り返し用。</td>
<td>ループ用</td>
</tr>
<tr class="odd">
<td><strong>forceLiterals</strong></td>
<td><code>select</code> 文で使用され、最適化時に <code>where</code> 句で使用される実際の値を Microsoft SQL Server データベースに公開しないようにカーネルに指示します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>forceNestedLoop</strong></td>
<td>SQL Server データベースがネストループ アルゴリズムを使用して、<code>join</code> を含む特定の SQL ステートメントを処理するよう強制します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>forcePlaceholders</strong></td>
<td><code>select</code>  文で使用され、最適化時に <code>where</code> 句で使用される実際の値を Microsoft SQL Server データベースに公開しないようにカーネルに指示します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>forceSelectOrder</strong></td>
<td>SQL Server データベースが指定した順序で結合内のテーブルにアクセスするよう強制します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>forUpdate</strong></td>
<td>更新専用のレコードを選択します。 フェッチされたレコードに対して実行される操作は更新です。 基になるデータベースによっては、レコードが他のユーザーのためにロックされることがあります。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>開始</strong></td>
<td><code>select</code> ステートメントの部分。 <code>from</code> 句は、列が存在するテーブルを指定します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>グループ</strong></td>
<td><code>select</code> ステートメントの <code>group by</code> 句の一部。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>次の場合</strong></td>
<td>条件付き実行。</td>
<td>if および if ... else ステートメント</td>
</tr>
<tr class="odd">
<td><strong>実装</strong></td>
<td>インターフェイスを実装します。</td>
<td>インターフェイスの概要</td>
</tr>
<tr class="even">
<td><strong>insert_recordset</strong></td>
<td>単一のサーバー トリップで、1 つ以上のテーブルのデータを 1 つの行先テーブルにコピーします。</td>
<td>insert_recordset</td>
</tr>
<tr class="odd">
<td><strong>int</strong></td>
<td>型 <code>integer</code> の変数を指定します (32 ビット)。</td>
<td>整数</td>
</tr>
<tr class="even">
<td><strong>int64</strong></td>
<td>型 <code>integer</code> の変数を指定します (64 ビット)。</td>
<td>整数</td>
</tr>
<tr class="odd">
<td><strong>インターフェイス</strong></td>
<td>インターフェイスの宣言。</td>
<td>インターフェイスの概要</td>
</tr>
<tr class="even">
<td><strong>は</strong></td>
<td>クラス変数によって照会されるオブジェクトが指定されたクラスから継承するか、または指定されたクラスのものであるかを確認します。 たとえば、<code>Base</code>クラスを<strong>拡張</strong>する指定された <code>Derived</code> クラスでは、式の <code>(myDerived is Base)</code> は <strong>true</strong> を返します。 このキーワードは、クラスの継承とテーブルの継承に適用されます。</td>
<td>式の演算子: 継承の Is および As</td>
</tr>
<tr class="odd">
<td><strong>結合</strong></td>
<td>テーブルは、両方のテーブルに共通の列に結合されます。 結合を使用することにより複数のテーブルに基づく単一の結果セットを生成することができます。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>等号</strong></td>
<td>ワイルドカード文字 * および ? を使って、パターンにより一致をテストします。 <code>like</code> 演算子の右側の文字列は、バックスラッシュを表すのに 4 つのバックスラッシュ文字を使用する必要があります。 例は以下に:
<ul>
<li><span class="code">(&quot;&amp;quot; like &quot;</em>&lt;em&gt;&quot; )</span> // false に解決されています。</li>
<li><span class="code">(&quot;&amp;quot; like &quot;</em>\*&quot;)</span> // true に解決されています。</li>
</ul></td>
<td>リレーショナル演算子</td>
</tr>
<tr class="odd">
<td><strong>maxof</strong></td>
<td><code>group by</code> 句により指定された行からフィールドの最大値を返します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>minof</strong></td>
<td><code>group by</code> 句により指定された行からフィールドの最小値を返します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>mod</strong></td>
<td>左側の expression1 の整数剰余を右側の expression2 で除算したものを返します。 非公式に、これは剰余演算子と呼ばれることもあります。 <code>((12 mod 7) == 5)</code> は true。</td>
<td></td>
</tr>
<tr class="even">
<td><strong>新規</strong></td>
<td>演算子。 指定されたクラス/インタフェース参照変数と割り当て互換性のある匿名クラスのインスタンスを作成するか、配列のメモリを割り当てます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>次へ</strong></td>
<td>テーブルの次のレコードをフェッチします。</td>
<td></td>
</tr>
<tr class="even">
<td><strong>noFetch</strong></td>
<td>現時点でフェッチされるレコードがないことを示します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>notExists</strong></td>
<td><code>select</code> 文の <code>join</code> 句で使用されます。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>記号定数。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>optimisticLock</strong></td>
<td>テーブルに異なる値が設定されていても、オプティミスティック同時実行制御でステートメントを実行するよう強制します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>注文</strong></td>
<td><code>select</code> ステートメントの <code>order by</code> 句の一部。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>外部</strong></td>
<td><span class="keyword">外部結合</span>。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>一時停止</strong></td>
<td>ジョブの実行を停止させます。 実行を続行する必要があるかどうかを確認するメッセージが表示されます。</td>
<td>ステートメントの選択</td>
</tr>
<tr class="odd">
<td><strong>pessimisticLock</strong></td>
<td>テーブルに異なる値が設定されていても、ペシミスティック同時実行制御でステートメントを実行するよう強制します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="even">
<td><strong>印刷</strong></td>
<td>スクリーン上にディスプレイ出力を表示できます。</td>
<td>ステートメントの印刷</td>
</tr>
<tr class="odd">
<td><strong>プライベート</strong></td>
<td>メソッドのアクセス修飾子。</td>
<td>メソッド アクセス制御</td>
</tr>
<tr class="even">
<td><strong>保護</strong></td>
<td>メソッドのアクセス修飾子。</td>
<td>メソッド アクセス制御</td>
</tr>
<tr class="odd">
<td><strong>パブリック</strong></td>
<td>メソッドのアクセス修飾子。</td>
<td>メソッド アクセス制御</td>
</tr>
<tr class="even">
<td><strong>実質</strong></td>
<td>型 <code>real</code> の変数を指定します。</td>
<td>Reals</td>
</tr>
<tr class="odd">
<td><strong>repeatableRead</strong></td>
<td>現在の取引が完了するまで、現在の取引内のロジックによって読み取られたデータを変更できる他の取引がないことを指定します。 明示的なトランザクションは <strong>ttsAbort</strong> または最も外側の <strong>ttsCommit</strong> で完了します。 スタンドアロンの <strong>select</strong> 明細書では、トランザクション期間は <strong>select</strong> コマンドの期間です。 ただし、X++ コードで表示されるこのキーワードなしでも (データベースがテーブルをどのようにスキャンするかに応じて)、データベースは時に、個々の<strong>選択</strong>ステートメントの <strong>repeatableRead</strong> と同等のものを実施します。</td>
<td>詳細については、「基になるリレーショナル データベース製品のドキュメント」を参照してください。</td>
</tr>
<tr class="even">
<td><strong>再試行</strong></td>
<td>例外処理で使用されます。</td>
<td>トライおよびキャッチ キーワードの例外処理</td>
</tr>
<tr class="odd">
<td><strong>戻る</strong></td>
<td>メソッドから終了します。</td>
<td>メソッドの宣言</td>
</tr>
<tr class="even">
<td><strong>リバース</strong></td>
<td>レコードが逆の順序で返されます。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>選択</strong></td>
<td><code>select</code> 句は、結果セットに表示される列またはビューを指定します。</td>
<td>ステートメントの選択</td>
</tr>
<tr class="even">
<td><strong>サーバー</strong></td>
<td>メソッド モディファイアー｡</td>
<td>メソッド モディファイアー</td>
</tr>
<tr class="odd">
<td><strong>設定</strong></td>
<td><span class="code">update_recordset</span> コマンドで使用されます。</td>
<td>update_recordset</td>
</tr>
<tr class="even">
<td><strong>静的</strong></td>
<td>静的メソッドはインスタンス変数を参照できません (静的変数のみ)。クラスのインスタンスではなく、クラス名を使用して呼び出すことができます (&quot;<code>MyClass.aStaticProcedure</code>&quot;)。</td>
<td>メソッド モディファイアー</td>
</tr>
<tr class="odd">
<td><strong>str</strong></td>
<td>型 <code>string</code> の変数を指定します。</td>
<td>文字列</td>
</tr>
<tr class="even">
<td><strong>合計</strong></td>
<td><code>select</code> ステートメント内の <code>group by</code> 句により指定された行からフィールドの合計を返します。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>スーパー</strong></td>
<td>現在のメソッドによって上書きされたメソッドを呼び出します。</td>
<td>テーブル メソッド</td>
</tr>
<tr class="even">
<td><strong>切り替え</strong></td>
<td>選択ステートメントを切り替えます。</td>
<td>Switch ステートメント</td>
</tr>
<tr class="odd">
<td><strong>tableLock</strong></td>
<td>Obsolete; <strong>tableLock</strong> はクエリで使用できなくなりました。</td>
<td></td>
</tr>
<tr class="even">
<td><strong>この</strong></td>
<td>クラスの現在のインスタンスへの参照。 クラスのメソッド内の X++ コードで使用されます。 Usクラスの<em>メソッド</em> メンバーを参照するのに使用されますが、クラスの<em>フィールド</em> メンバーは参照されません。<code>public str getFullName()</code>  <span class="code">{</span>  <span class="code">    // 次のステートメントは 「this」 なしではコンパイルできません。</span>  <code>    return this.concatenateFirstAndLastNames();</code>  <span class="code">}</span></td>
<td><code>element</code> という名前のシステム変数とほぼ同様です。 フォーム コントロール メソッドの <code>element</code> を使用して、格納フォームを参照します。 詳細については、「フォームの変数を使用」を参照してください。</td>
</tr>
<tr class="odd">
<td><strong>スロー</strong></td>
<td>例外処理で使用されます。</td>
<td>トライおよびキャッチ キーワードの例外処理</td>
</tr>
<tr class="even">
<td><strong>はい</strong></td>
<td>ブール型リテラル。</td>
<td>ブール型</td>
</tr>
<tr class="odd">
<td><strong>実行</strong></td>
<td>例外処理で使用されます。</td>
<td>トライおよびキャッチ キーワードの例外処理</td>
</tr>
<tr class="even">
<td><strong>ttsAbort</strong></td>
<td>現在のトランザクションのすべての変更を破棄します。</td>
<td>トランザクションの整合性</td>
</tr>
<tr class="odd">
<td><strong>ttsBegin</strong></td>
<td>トランザクションの開始をマークします。</td>
<td>トランザクションの整合性</td>
</tr>
<tr class="even">
<td><strong>ttsCommit</strong></td>
<td>トランザクションの終了をマークします。</td>
<td>トランザクションの整合性</td>
</tr>
<tr class="odd">
<td><strong>update_recordset</strong></td>
<td>1 回の工程内で行セットの操作を許可します。</td>
<td>update_recordset</td>
</tr>
<tr class="even">
<td><strong>validTimeState</strong></td>
<td>X++ SQL <code>select</code> 明細書により有効時間状態テーブルから取得される行をフィルター処理します。 例: <span class="code">xMyTable; から validTimeState(myDateEffective) *を選択</span> ... または ...  <span class="code">xMyTable; から validTimeState(myDateFrom, myDateTo)* を選択</span></td>
<td>有効時間状態テーブルが読み取りおよび書き込み操作に及ぼす影響</td>
</tr>
<tr class="odd">
<td><strong>無効</strong></td>
<td>値を返さないメソッドを示します。</td>
<td>メソッドの宣言</td>
</tr>
<tr class="even">
<td><strong>WHERE</strong></td>
<td><code>select</code> ステートメントの部分。 <code>where</code> 句は、満たす必要がある条件を指定します。つまり、その結果に含める行です。</td>
<td>ステートメント構文の選択</td>
</tr>
<tr class="odd">
<td><strong>中に</strong></td>
<td>繰り返しのステートメント。 テスト条件が該当する時は、明細書またはブロックを繰り返し実行します。</td>
<td>While Loop while select ステートメント</td>
</tr>
<tr class="even">
<td><strong>ウィンドウ</strong></td>
<td>出力ウィンドウのサイズを変更できます。</td>
<td>ステートメントの印刷</td>
</tr>
</tbody>
</table>

## <a name="expressions-syntax"></a>式の構文
X++ の式は数学的または論理的ないずれかの方法で使用されます。 式は、言語のデータ型に基づいて作成されます。つまり、ある式はある型の値を返します。 この値は、計算、代入、条件文などで使用できます。

### <a name="ebnf-description-of-expressions-in-x"></a>EBNF Description of Expressions in X++

|                    |   |                                                             |
|--------------------|---|-------------------------------------------------------------|
|     式     | = | 簡易式  \[RelationalOperator Simple-expression \] |
| RelationalOperator | = |                              =                              |
| 簡易式  | = |                   簡易式 \[ +                    |
|        相談        | = |           Compfactor { 複数演算子 CompFactor }           |
|   複数演算子    | = |                             \*                              |
|     CompFactor     | = |                        \[ ! \] \[ -                         |
|       係数       | = |                           リテラル                           |
|        列挙        | = |                     EnumName :: リテラル                     |
|      変数      | = |    識別子 \[ \[ 式 \] \] \[ . 式 \]     |
|    FunctionCall    | = |                      \[ 式 (.                       |
|   If 式    | = |            Expression ? 式 : 式             |

意味の制限が前述の構文に適用されます。 :: 演算子を使用するメソッドを呼び出すことはできません。 同様に、アーカイブ オブジェクトなしで、つまりメソッドなどの中でなければ、**this** キーワードを使用することはできません。

### <a name="examples"></a>例

| 式の例                                       | 説明                                                                                                                                    |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `1`                                                         | 整数リテラル。                                                                                                                            |
| NoYes::No                                                   | 列挙参照。                                                                                                                             |
| `A`                                                         | 変数の参照。                                                                                                                          |
| Debtor::Find("1")                                           | 静的メソッドの呼び出し (顧客変数を返す)。                                                                                            |
| (A &gt; 3 ? true : false)                                   | **true** または **false** を返す if 式です。                                                                                           |
| (CustTable.Account == 「100」の CustTable を選択します)。NameRef | 選択式。 顧客テーブルで nameref フィールドを返します。 これは文字列です                                                        |
| A &gt;= B                                                   | 論理式。 **true** または **false** を返します。                                                                                           |
| A + B                                                       | 算術式です。 合計 A と B。                                                                                                        |
| A + B / C                                                   | B/C を計算し、これを A に追加します。                                                                                                       |
| ~A + this.Value()                                           | A 以外のバイナリと、スコープ (this) 内のオブジェクトのメソッド呼び出し値の結果を合計します。                                                       |
| Debtor::Find("1").NameRef                                   | 検出された顧客レコードの NameRef フィールドを返します。                                                                                        |
| Debtor::Find("1").Balance()                                 | 顧客テーブルの `Balance` へのメソッド呼び出し (Debtor::Find は、顧客を返す)。 口座番号 1 の顧客の残高を返します。 |

## <a name="ebnf-overview"></a>EBNF 概要
Extended Backus Naur Form (EBNF) は metalanguage あり、このガイドでは言語構文を説明するために使用されています。 EBNF 定義は生産ルール、非ターミナル、およびターミナルで構成されます。 重要な用語は次のテーブルに表示されます。


|    重要な用語     |       例        |                                                                                                          説明                                                                                                          |
|------------------|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    ターミナル     |      Work\_Team      |                                                                           ターミナルは、変更しない 1 文字または文字の文字列です。                                                                            |
|   非ターミナル   |      `Employee`      | 非ターミナルは、生産ルールまたはテキストの説明のいずれかによって定義された言語の有効な文の一部の説明です。 非ターミナル記号は、1 つまたは複数のターミナル記号にいつでも展開できます。 |
| 生産ルール | 従業員 = 開発者 |                                                                                                            テスト担当者                                                                                                             |

### <a name="example"></a>例

Work\_Team = Manager Employee {, Employee}  Employee = Developer | Tester この例は Work\_Team を `Manager` および一人またはそれ以上の `Employees` で構成されるように定義します。 `Employee` は、`Developer`、または `Tester` として定義されています。 この例で使用されているシンボルについては、次の表で説明します。

### <a name="special-symbols-in-ebnf"></a>EBNF の特殊記号

|         記号          |                                                               説明                                                               |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
|  (<em>式</em>)  | かっこには、記号 (ターミナルおよび非ターミナル) がまとめて保持されます。 生産ルールの右側の任意の場所に配置できます。 |
|  <em>Expression1</em>   |                                                          <em>Expression2</em>                                                           |
| \[<em>式</em>\] |               オプション: \[ と \] の間の項目はオプションです。 すべてまたはいずれかの項目に括弧が含まれます。                |
|      {Expression}       |                     繰り返し: { と } の間の項目はオプションですが、必要な回数繰り返し実行できます。                     |

たとえば、自転車のために購入するアクセサリがサドル、飲料水ボトル ホルダー、ベル、およびクラクションから成る場合、ベルまたはクラクションのいずれか、および 0 個、1 個、または複数の飲料水ボトル ホルダー、さらにちょうど 1 つのサドルを持つことができ、この場合以下のように表されます: \_自転車アクセサリ = サドル\[ベル | クラクション\] {飲料水\_ボトル\_ホルダー} この文法は次の選択を定義します。`saddle`  `saddle bell`  `saddle horn`  サドル 飲料水\_ボトル\_ホルダー  サドル ベル 飲料水\_ボトル\_ホルダー  サドル ベル 飲料水\_ボトル\_ホルダー 飲料水\_ボトル\_ホルダーなど。

## <a name="x-grammar"></a>X++ 文法
このトピックでは、X++ 言語の正式な文法を示します。

### <a name="how-to-interpret-the-formal-bnf-grammar"></a>正式な BNF 文法を解釈する方法

このセクションでは、Backus Naur Form (BNF) の X++ の文法について説明します。 次に、BNF の小さな例について説明します。

```xpp
AA ::= BB  CC_SYM
BB ::= JJ_SYM
   ::= KK_SYM
```

`AA` は生産ルールの名前です。 `AA` は `BB` が必要で、続いて CC\_SYM となります。 `BB` も生産ルールです。 したがって、`BB` はターミナルではありません。 `BB` は、JJ\_SYM または KK\_SYM のいずれかである必要があります。 JJ\_SYM と KK\_SYM の両方は他の生産ルールの名前ではないためターミナルです。 CC\_SYM もターミナルです。

X++ の文法の BNF で、ターミナルのほとんどに名前の接尾語として \_SYM があります。

### <a name="the-formal-x-grammar-in-bnf"></a>BNF での正式な X++ 文法

このセクションには、X++文法を定義する BNF が含まれています。

```xpp
    CMPL_UNIT ::= RETTYPEID  FUNC_HDR  FUNC_HEAD  BODY
              ::= RETTYPEID  DATA_HDR  CLASS_DECL
              ::= EXPR_HDR  IF_EXPR  SEMIOPT
              ::= RETTYPEID  FUNC_HDR  EVENT_DECL  BODY
    SEMIOPT ::= SEMICOLON_SYM
            ::= 
    CLASS_DECL ::= CLASS_HEADER  LEFTBR_SYM  DCL_EVENTMAP  DCL_LIST  RIGHTBR_SYM
    CLASS_HEADER ::= ATTRIBUTE_DEF  CLASS_MODIFIERS  CLASSORINTERFACE  STD_ID  EXTENDS  IMPLEMENTS
    ATTRIBUTE_DEF ::= LEFT_BRKT_SYM  ATTRIBUTE_INIT  ATTRIBUTE_LIST  RETTYPEID  RGHT_BRKT_SYM
                  ::= 
    ATTRIBUTE_INIT ::= 
                   .
    ATTRIBUTE_LIST ::= ATTRIBUTE
                   ::= ATTRIBUTE_LIST  LIST_SEP_SYM  ATTRIBUTE
    ATTRIBUTE ::= STD_ID
              ::= ATTRIBUTE_WITH_ARGS_BEGINS  ATTRIBUTE_WITH_ARGS_ENDS
    ATTRIBUTE_WITH_ARGS_BEGINS ::= STD_ID  LEFT_PAR_SYM
    ATTRIBUTE_WITH_ARGS_ENDS ::= ATTRIBUTE_ARGS  RGHT_PAR_SYM
    ATTRIBUTE_ARGS ::= ATTRIBUTE_CONSTANT
                   ::= ATTRIBUTE_ARGS  LIST_SEP_SYM  ATTRIBUTE_CONSTANT
    ATTRIBUTE_CONSTANT ::= INT_SYM
                       ::= DBL_SYM
                       ::= STR_SYM
                       ::= DATE_SYM
                       ::= DATETIME_SYM
                       ::= STD_ID  DBLCOLON_SYM  STD_ID
                       ::= TRUE_SYM
                       ::= FALSE_SYM
                       ::= INT64_SYM
                       ::= ATTRIBUTE_INTRINSIC
    ATTRIBUTE_INTRINSIC ::= INTRI_ID  LEFT_PAR_SYM  IARGS  RGHT_PAR_SYM
    CLASSORINTERFACE ::= CLASS_SYM
                     ::= INTERFACE_SYM
    CLASS_MODIFIERS ::= CLASS_MODS
                    ::= 
    CLASS_MODS ::= CLASS_MODIFIER
               ::= CLASS_MODS  RETTYPEID  CLASS_MODIFIER
    CLASS_MODIFIER ::= PUBLIC_SYM
                   ::= FINAL_SYM
                   ::= STATIC_SYM
                   ::= ABSTRACT_SYM
                   ::= PRIVATE_SYM
    EXTENDS ::= EXTENDS_SYM  STD_ID
            ::= 
    IMPLEMENTS ::= IMPLEMENTS_SYM  IMPLEMENTLIST
               ::= 
    IMPLEMENTLIST ::= STD_ID
                  ::= IMPLEMENTLIST  LIST_SEP_SYM  STD_ID
    DCL_EVENTMAP ::= 
    EVENT_DECL ::= ATTRIBUTE_DEF  EVENT_HEADER  PARM_DCL_LIST
    EVENT_HEADER ::= EVENT_MODIFIER  VOID_TYPE_SYM  STD_ID
    EVENT_MODIFIER ::= EVENT_SYM
    FUNC_HEAD ::= ATTRIBUTE_DEF  FUNCNAME  PARM_DCL_LIST
    FUNCNAME ::= FUNCTYPE  STD_ID
    FUNCTYPE ::= FUNC_MODIFIERS  DECL_TYPE
    FUNC_MODIFIERS ::= FUNC_MODS
                   ::= 
    FUNC_MODS ::= RETTYPEID  FUNC_MODIFIER
              ::= FUNC_MODS  RETTYPEID  FUNC_MODIFIER
    FUNC_MODIFIER ::= PUBLIC_SYM
                  ::= PRIVATE_SYM
                  ::= PROTECTED_SYM
                  ::= FINAL_SYM
                  ::= STATIC_SYM
                  ::= ABSTRACT_SYM
                  ::= DISPLAY_SYM
                  ::= EDIT_SYM
                  ::= SERVER_SYM
                  ::= CLIENT_SYM
    BODY ::= LEFTBR_SYM  DCL_FUNC_LIST  SEMIOPT  SECAUTHZCHECK  STMTLIST  SECAUTHZEND  RIGHTBR_SYM
    SECAUTHZCHECK ::= 
    SECAUTHZEND ::= 
    RETTYPEID ::= 
    FUNCTION_DEF ::= FUNC_HEADER  PARM_DCL_LIST  LOCAL_BODY
    FUNC_HEADER ::= DECL_TYPE  STD_ID
    PARM_DCL_LIST ::= RETTYPEID  PARM_START  PARM_LIST_OPT  RGHT_PAR_SYM  RETTYPEID
    PARM_START ::= LEFT_PAR_SYM
    PARM_LIST_OPT ::= PARM_LIST
                  ::= 
    PARM_LIST ::= DCL_INIT
              ::= PARM_LIST  LIST_SEP_SYM  DCL_INIT
    LOCAL_BODY ::= LEFTBR_SYM  DCL_LIST  SEMIOPT  STMTLIST  RETTYPEID  RIGHTBR_SYM
    DCL_LIST ::= DCL_LIST2
             ::= 
    DCL_LIST2 ::= DCL_STMT
              ::= DCL_LIST2  DCL_STMT
    DCL_FUNC_LIST ::= DCL_FUNC_LIST2
                  ::= 
    DCL_FUNC_LIST2 ::= DCL_STMT
                   ::= FUNCTION_DEF
                   ::= DCL_FUNC_LIST2  DCL_STMT
                   ::= DCL_FUNC_LIST2  FUNCTION_DEF
    DCL_STMT ::= DCL_INIT_LIST  RETTYPEID  SEMICOLON_SYM
    DCL_INIT_LIST ::= DCL_INIT
                  ::= DCL_CLIST  ASG_CLAUSE
    DCL_CLIST ::= DCL_INIT_LIST  LIST_SEP_SYM  STD_ID  ARR_DCL_IDX
    DCL_INIT ::= DECL  ASG_CLAUSE
    DECL ::= DECL_TYPE  STD_ID  ARR_DCL_IDX
    DECL_TYPE ::= STR_TYPE_SYM  STR_LEN
              ::= INT_TYPE_SYM
              ::= DBL_TYPE_SYM
              ::= DATE_TYPE_SYM
              ::= DATETIME_TYPE_SYM
              ::= TYPE_ID
              ::= QUEUE_TYPE_SYM
              ::= VOID_TYPE_SYM
              ::= ANY_TYPE_SYM
              ::= GUID_TYPE_SYM
              ::= INT64_TYPE_SYM
              ::= CLR_TYPE
    CLR_TYPE ::= CLR_NAMESPACE  TYPE_ID  CLR_ARRAY_TYPE_EXT
             ::= CLR_NAMESPACE  CLR_TYPE
    CLR_NAMESPACE ::= TYPE_ID  PERIOD_SYM
    CLR_ARRAY_TYPE_EXT ::= CLR_ARRAY_SPEC
                       ::= 
    CLR_ARRAY_SPEC ::= CLR_ARRAY_PART
                   ::= CLR_ARRAY_SPEC  CLR_ARRAY_PART
    CLR_ARRAY_PART ::= CLR_ARRAY_LEFT_PART  CLR_RECTANGULAR_LIST  RGHT_BRKT_SYM
    CLR_ARRAY_LEFT_PART ::= LEFT_BRKT_SYM
    CLR_RECTANGULAR_LIST ::= CLR_COMMA_LIST
                         ::= 
    CLR_COMMA_LIST ::= LIST_SEP_SYM
                   ::= CLR_COMMA_LIST  LIST_SEP_SYM
    STR_LEN ::= INT_SYM
            ::= 
    ARR_DCL_IDX ::= LEFT_BRKT_SYM  RANGE  ARRAY_MEM  RGHT_BRKT_SYM
                ::= 
    RANGE ::= IF_EXPR
          ::= 
    ARRAY_MEM ::= LIST_SEP_SYM  IF_EXPR
              ::= 
    ASG_CLAUSE ::= INIT_START  IF_EXPR
               ::= 
    INIT_START ::= ASG_SYM
    ASG_STMT ::= LVAL_FLD  ASSIGN  IF_EXPR
             ::= LVAL_LIST  ASG_SYM  IF_EXPR
             ::= LVAL_FLD  ASG_INC_DEC
             ::= ASG_INC_DEC  LVAL_FLD
             ::= LVAL_FLD  ASG_EVENT_HANDLER
    ASSIGN ::= ASG_SYM
           ::= ASGINC_SYM
           ::= ASGDEC_SYM
    ASG_INCDEC ::= ASGINC_SYM
               ::= ASGDEC_SYM
    ASG_EVENT_HANDLER ::= ASG_INCDEC  EVENTHANDLER_SYM  LEFT_PAR_SYM  QUALIFIER  STD_ID  RGHT_PAR_SYM
      ::= ASG_INCDEC  EVENTHANDLER_SYM  LEFT_PAR_SYM  STD_ID  DBLCOLON_SYM  STD_ID  RGHT_PAR_SYM
      ::= ASG_INCDEC  EVENTHANDLER_SYM  LEFT_PAR_SYM  QUALIFIER  EVAL_CLR_TYPE  DBLCOLON_SYM  STD_ID  RGHT_PAR_SYM
    ASG_INC_DEC ::= INC_SYM
                ::= DEC_SYM
    LVAL_FLD ::= FIELD
    LVAL_START ::= LEFT_BRKT_SYM
    LVAL_LIST ::= LVAL_START  LVALUES  RGHT_BRKT_SYM
    LVALUE ::= FIELD
    LVALUES ::= LVALUE
            ::= LVALUES  NEXTLVAL  LVALUE
    NEXTLVAL ::= LIST_SEP_SYM
    IF_EXPR ::= COND_TRUE  IF_EXPR
            ::= BOOL_EXPR
    COND_TRUE ::= COND_TEST  IF_EXPR  COLON_SYM
    COND_TEST ::= BOOL_EXPR  QUEST_SYM
    BOOL_EXPR ::= BOOL_EXPR  LOGOP  EXPR
              ::= EXPR
    LOGOP ::= AND_SYM
          ::= OR_SYM
    EXPR ::= SMPL_EXPR  RELOP  SMPL_EXPR
         ::= SMPL_EXPR  AS_SYM  STD_ID
         ::= SMPL_EXPR  IS_SYM  STD_ID
         ::= SMPL_EXPR  AS_SYM  EVAL_CLR_TYPE
         ::= SMPL_EXPR  IS_SYM  EVAL_CLR_TYPE
         ::= SMPL_EXPR
    RELOP ::= LT_SYM
          ::= LE_SYM
          ::= EQ_SYM
          ::= NE_SYM
          ::= GT_SYM
          ::= GE_SYM
          ::= LIKE_SYM
    SMPL_EXPR ::= SMPL_EXPR  ADDOP  TERM
              ::= TERM
    ADDOP ::= PLUS_SYM
          ::= MINUS_SYM
          ::= PHYSOR_SYM
    TERM ::= TERM  MULOP  CMPL_FACT
         ::= CMPL_FACT
    MULOP ::= MULT_SYM
          ::= DIV_SYM
          ::= MOD_SYM
          ::= INTDIV_SYM
          ::= SHIFTL_SYM
          ::= SHIFTR_SYM
          ::= PHYSAND_SYM
          ::= PHYSXOR_SYM
    CMPL_FACT ::= NOT_SYM  SGND_FACT
              ::= SGND_FACT
    SGND_FACT ::= SIGNOP  FACTOR
              ::= FACTOR
    SIGNOP ::= UMINUS_SYM
           ::= PHYSNOT_SYM
    FACTOR ::= LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
           ::= CONSTANT
           ::= FIELD
           ::= DIRSEARCH
           ::= FUNCTION
           ::= INTRINSICS
           ::= EVAL
           ::= CONLITTERAL
           ::= NEW_CLR_ARRAY
    NEW_CLR_ARRAY ::= NEW_SYM  EVAL_CLR_TYPE  NEW_CLR_ARRAY_PART  LEFT_PAR_SYM  RGHT_PAR_SYM
    NEW_CLR_ARRAY_PART ::= CLR_SIZED_ARRAY  CLR_NOSIZED_ARRAY_SPEC
    CLR_SIZED_ARRAY ::= LEFT_BRKT_SYM  CLR_SMPL_EXPR_COMMA_LIST  RGHT_BRKT_SYM
    CLR_SMPL_EXPR_COMMA_LIST ::= SMPL_EXPR
      ::= CLR_SMPL_EXPR_COMMA_LIST  LIST_SEP_SYM  SMPL_EXPR
    CLR_NOSIZED_ARRAY_SPEC ::= CLR_NOSIZED_ARRAY_LIST
                           ::= 
    CLR_NOSIZED_ARRAY_LIST ::= CLR_NOSIZED_ARRAY
                           ::= CLR_NOSIZED_ARRAY_LIST  CLR_NOSIZED_ARRAY
    CLR_NOSIZED_ARRAY ::= LEFT_BRKT_SYM  CLR_EMPTY_COMMA_LIST  RGHT_BRKT_SYM
    CLR_EMPTY_COMMA_LIST ::= CLR_EMPTY_RECT_COMMA_LIST
                         ::= 
    CLR_EMPTY_RECT_COMMA_LIST ::= LIST_SEP_SYM
                              ::= CLR_EMPTY_RECT_COMMA_LIST  LIST_SEP_SYM
    CONLITTERAL ::= LEFT_BRKT_SYM  IF_EXPR  EXPR_LIST  RGHT_BRKT_SYM
    CONSTANT ::= INT_SYM
             ::= DBL_SYM
             ::= STR_SYM
             ::= DATE_SYM
             ::= DATETIME_SYM
             ::= STD_ID  DBLCOLON_SYM  STD_ID
             ::= TRUE_SYM
             ::= FALSE_SYM
             ::= NULL_SYM
             ::= INT64_SYM
             ::= QUALIFIER  EVAL_CLR_TYPE  DBLCOLON_SYM  STD_ID
             ::= QUALIFIER  STD_ID  DBLCOLON_SYM  STD_ID
    DIRSEARCH ::= DIRS_HEADER  PERIOD_SYM  STD_ID  ARR_IDX
              ::= DIRS_HEADER  PERIOD_SYM  FLD_NUM  ARR_IDX
    DIRS_HEADER ::= LEFT_PAR_SYM  SET_DIRS  FIND_JOIN  RGHT_PAR_SYM
    SET_DIRS ::= 
    FIELD ::= QUALIFIER  STD_ID  ARR_IDX
          ::= QUALIFIER  FLD_NUM  ARR_IDX
          ::= STD_ID  ARR_IDX
    QUALIFIER ::= EVAL  PERIOD_SYM
              ::= STD_ID  PERIOD_SYM
    FLD_NUM ::= LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    ARR_IDX ::= LEFT_BRKT_SYM  SMPL_EXPR  RGHT_BRKT_SYM
            ::= 
    EXPR_LIST ::= EXPR_LIST2
              ::= 
    EXPR_LIST2 ::= LIST_SEP_SYM  IF_EXPR
               ::= EXPR_LIST2  LIST_SEP_SYM  IF_EXPR
    FUNCTION ::= FUNC_ID  LEFT_PAR_SYM  EVAL_FUNCTION_NAME  PAR_LIST  RGHT_PAR_SYM
    EVAL_FUNCTION_NAME ::= 
    EVAL_NAME ::= EVAL_ID  LEFT_PAR_SYM
              ::= STD_ID  LEFT_PAR_SYM
              ::= STD_ID  DBLCOLON_SYM  STD_ID  LEFT_PAR_SYM
              ::= SUPER_SYM  LEFT_PAR_SYM
              ::= NEW_SYM  STD_ID  LEFT_PAR_SYM
              ::= NEW_SYM  EVAL_CLR_TYPE  LEFT_PAR_SYM
              ::= QUALIFIER  EVAL_CLR_TYPE  DBLCOLON_SYM  STD_ID  LEFT_PAR_SYM
              ::= QUALIFIER  STD_ID  LEFT_PAR_SYM
              ::= QUALIFIER  STD_ID  DBLCOLON_SYM  STD_ID  LEFT_PAR_SYM
    EVAL_CLR_TYPE ::= NAMESPACE  STD_ID
                  ::= NAMESPACE  EVAL_CLR_TYPE
    NAMESPACE ::= STD_ID  PERIOD_SYM
    EVAL ::= EVAL_NAME  PAR_LIST  RGHT_PAR_SYM
    PAR_LIST ::= PRM_LIST
             ::= 
    PRM_LIST ::= PAR_ELEM
             ::= PRM_LIST  LIST_SEP_SYM  PAR_ELEM
    PAR_ELEM ::= IF_EXPR
             ::= BYREF_SYM  FIELD
    INTRINSICS ::= INTRI_ID  LEFT_PAR_SYM  IARGS  RGHT_PAR_SYM
    IARGS ::= STD_ID
          ::= STR_SYM
          ::= STD_ID  LIST_SEP_SYM  STD_ID
          ::= 
    STMTLIST ::= STATEMENTS
             ::= 
    STATEMENTS ::= STATEMENT
               ::= STATEMENTS  STATEMENT
    STATEMENT ::= COMPOUND_STMT
              ::= WHILE_STMT
              ::= FOR_STMT
              ::= DO_STMT
              ::= SEARCH_STMT
              ::= FIND_STMT
              ::= PRINT_STMT
              ::= WINDOW_STMT
              ::= IF_STMT
              ::= SWITCH_STMT
              ::= EXPR_STMT
              ::= PAUSE_STMT
              ::= BP_CLAUSE
              ::= BREAK_STMT
              ::= CONTINUE_STMT
              ::= RETURN_CLAUSE
              ::= MOVE_REC_STMT
              ::= THROW_STMT
              ::= TRY_STMT
              ::= RETRY_STMT
              ::= TTS_STMT
              ::= FLUSH_STMT
              ::= TBLLOCK_STMT
              ::= CHANGE_STMT
              ::= UPDATE_STMT
              ::= INSERT_STMT
              ::= UNCHECKED_STMT
    COMPOUND_STMT ::= LEFTBR_SYM  STMTLIST  RIGHTBR_SYM
    THROW_STMT ::= THROW_SYM  IF_EXPR  SEMICOLON_SYM
    TRY_STMT ::= TRY_BLOCK  CATCH_LIST
    TRY_BLOCK ::= TRY_START  STATEMENT
    TRY_START ::= TRY_SYM
    CATCH_LIST ::= CATCH_STMT
               ::= CATCH_LIST  CATCH_STMT
    CATCH_STMT ::= CATCH_EXPR  PRE_CATCH  STATEMENT  POST_CATCH
    CATCH_EXPR ::= CATCH_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
      ::= CATCH_SYM  LEFT_PAR_SYM  IF_EXPR  LIST_SEP_SYM  TABLEINSTANCE  RGHT_PAR_SYM
      ::= CATCH_SYM
    PRE_CATCH ::= 
    POST_CATCH ::= 
    TABLEINSTANCE ::= INSTANCENAME
    INSTANCENAME ::= QUALIFIER  STD_ID  ARR_IDX
                 ::= STD_ID  ARR_IDX
    RETRY_STMT ::= RETRY_SYM  SEMICOLON_SYM
    WHILE_STMT ::= WHILE_TEST  STATEMENT
    WHILE_TEST ::= WHILE  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    WHILE ::= WHILE_SYM
    DO_STMT ::= DO_BODY  DO_TEST  SEMICOLON_SYM
    DO_BODY ::= DO_HEADER  STATEMENT
    DO_HEADER ::= DO_SYM
    DO_TEST ::= WHILE_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    FOR_STMT ::= FOR_HEADER  STATEMENT
    FOR_HEADER ::= FOR_TEST  SEMICOLON_SYM  FOR_ASG  RGHT_PAR_SYM
    FOR_TEST ::= FOR_INIT  SEMICOLON_SYM  IF_EXPR
    FOR_INIT ::= FOR_SYM  LEFT_PAR_SYM  FOR_ASG
    FOR_ASG ::= LVAL_FLD  ASSIGN  IF_EXPR
            ::= LVAL_FLD  ASG_INC_DEC
            ::= ASG_INC_DEC  LVAL_FLD
    JOIN_LIST ::= JOIN_SPECS
              ::= 
    JOIN_SPECS ::= JOIN_SPEC
               ::= JOIN_SPECS  JOIN_SPEC
    JOIN_SPEC ::= JOIN_ORDER  WHERE  IF_EXPR
              ::= JOIN_ORDER
    JOIN_ORDER ::= JOIN_USING
               ::= JOIN_USING  ORDER_GROUP
    JOIN_USING ::= JOIN_CLAUSE  USING_INDEX  STD_ID
               ::= JOIN_CLAUSE  USING_INDEX  HINT_SYM  STD_ID
               ::= JOIN_CLAUSE
    JOIN_CLAUSE ::= OUTER  JOIN_SYM  SELECTOPT  TABLE
    OUTER ::= OUTER_SYM
          ::= EXISTS_SYM
          ::= NOTEXISTS_SYM
          ::= 
    SEARCH_STMT ::= SEARCH_JOIN  STATEMENT
    SEARCH_JOIN ::= SEARCH_WHERE  JOIN_LIST
    SEARCH_WHERE ::= SEARCH_ORDER  WHERE  IF_EXPR
                 ::= SEARCH_ORDER
    WHERE ::= WHERE_SYM
    SUM_ELEM ::= SUM_FUNC  LEFT_PAR_SYM  STD_ID  RGHT_PAR_SYM
    SUM_FUNC ::= SUM_SYM
             ::= AVG_SYM
             ::= CNT_SYM
             ::= MINOF_SYM
             ::= MAXOF_SYM
    SEARCH_ORDER ::= SEARCH_USING
                 ::= SEARCH_USING  ORDER_GROUP
    ORDER_GROUP ::= ORDERBY_CLAUSE  OPT_GROUPBY
                ::= GROUPBY_CLAUSE  OPT_ORDERBY
    OPT_GROUPBY ::= GROUPBY_CLAUSE
                ::= 
    OPT_ORDERBY ::= ORDERBY_CLAUSE
                ::= 
    ORDERBY_CLAUSE ::= ORDER_SYM  OPT_BY  ORDER_ELEM
                   ::= ORDERBY_CLAUSE  LIST_SEP_SYM  ORDER_ELEM
    GROUPBY_CLAUSE ::= GROUP_SYM  OPT_BY  ORDER_ELEM
                   ::= GROUPBY_CLAUSE  LIST_SEP_SYM  ORDER_ELEM
    ORDER_ELEM ::= STD_ID  INDEX  DIRECTION
               ::= ORDER_QUALIFIER  STD_ID  INDEX  DIRECTION
    ORDER_QUALIFIER ::= STD_ID  PERIOD_SYM
    INDEX ::= LEFT_BRKT_SYM  INT_SYM  RGHT_BRKT_SYM
          ::= 
    DIRECTION ::= ASCEND_SYM
              ::= DESCEND_SYM
              ::= 
    OPT_BY ::= BY_SYM
           ::= 
    SEARCH_USING ::= SEARCH_CLAUSE  USING_INDEX  STD_ID
                 ::= SEARCH_CLAUSE  USING_INDEX  HINT_SYM  STD_ID
                 ::= SEARCH_CLAUSE
    USING_INDEX ::= INDEX_SYM
    SEARCH_CLAUSE ::= WHILE_SYM  SELECT_SYM  SELECTOPT  CROSSCOMPANY_CLAUSE  VALIDTIMESTATE_CLAUSE  TABLE
    CROSSCOMPANY_CLAUSE ::= CROSSCOMPANY_SYM
                        ::= CROSSCOMPANY_SYM  COLON_SYM  STD_ID
                        ::= 
    VALIDTIMESTATE_CLAUSE ::= VALIDTIMESTATE_SYM  LEFT_PAR_SYM  STD_ID  LIST_SEP_SYM  STD_ID  RGHT_PAR_SYM
      ::= VALIDTIMESTATE_SYM  LEFT_PAR_SYM  STD_ID  RGHT_PAR_SYM
      ::= 
    SELECTOPT ::= 
              ::= SELECTOPT  REVERSE_SYM
              ::= SELECTOPT  FIRSTFAST_SYM
              ::= SELECTOPT  FIRSTONLY_SYM
              ::= SELECTOPT  FIRSTONLY_SYM1
              ::= SELECTOPT  FIRSTONLY_SYM10
              ::= SELECTOPT  FIRSTONLY_SYM100
              ::= SELECTOPT  FIRSTONLY_SYM1000
              ::= SELECTOPT  FORUPDATE_SYM
              ::= SELECTOPT  NOFETCH_SYM
              ::= SELECTOPT  FORCE_SELECT_ORDER_SYM
              ::= SELECTOPT  FORCE_NESTED_LOOP_SYM
              ::= SELECTOPT  FORCE_LITERALS_SYM
              ::= SELECTOPT  FORCE_PLACEHOLDERS_SYM
              ::= SELECTOPT  REPEATABLEREAD_SYM
              ::= SELECTOPT  OPTIMISTICLOCK_SYM
              ::= SELECTOPT  PESSIMISTICLOCK_SYM
              ::= SELECTOPT  GENERATEONLY_SYM
    FIND_STMT ::= FIND_JOIN  SEMICOLON_SYM
    FIND_JOIN ::= FIND_WHERE  JOIN_LIST
    FIND_WHERE ::= FIND_ORDER  WHERE  IF_EXPR
               ::= FIND_ORDER
    FIND_ORDER ::= FIND_USING
               ::= FIND_USING  ORDER_GROUP
    FIND_USING ::= FIND_TABLE  USING_INDEX  STD_ID
               ::= FIND_TABLE  USING_INDEX  HINT_SYM  STD_ID
               ::= FIND_TABLE
    FIND_TABLE ::= SELECT_SYM  SELECTOPT  CROSSCOMPANY_CLAUSE  VALIDTIMESTATE_CLAUSE  TABLE
      ::= DELETE_SYM  SELECTOPT  CROSSCOMPANY_CLAUSE  VALIDTIMESTATE_CLAUSE  TABLE
    TABLE ::= FLD_LIST  OPT_FROM
    FLD_LIST ::= MULT_SYM
             ::= FIELD_LIST
    FIELD_LIST ::= FIELD_SPEC
               ::= FIELD_LIST  LIST_SEP_SYM  FIELD_SPEC
    FIELD_SPEC ::= STD_ID  INDEX
               ::= SUM_ELEM
    OPT_FROM ::= FROM_SYM  STD_ID
             ::= 
    SETFIELDSMODE ::= 
    UPDATE_STMT ::= UPDATETABLE  SET_SYM  SETFIELDSMODE  FIELDASSIGNMENTS  OPT_WHERE  JOIN_LIST  SEMICOLON_SYM
    UPDATETABLE ::= UPDATE_SYM  SELECTOPT  CROSSCOMPANY_CLAUSE  STD_ID
    OPT_WHERE ::= WHERE  IF_EXPR
              ::= 
    FIELDASSIGNMENTS ::= FIELDASSIGNMENTS  LIST_SEP_SYM  FIELDASSIGNMENT
                     ::= FIELDASSIGNMENT
    FIELDASSIGNMENT ::= STD_ID  INDEX  ASG_SYM  IF_EXPR
    INSERT_PART ::= INSERT_SYM  CROSSCOMPANY_CLAUSE  INSERT_NAME  LEFT_PAR_SYM  INSERTFIELDLIST  RGHT_PAR_SYM
    INSERT_NAME ::= STD_ID
    INSERT_STMT ::= INSERT_PART  FIND_JOIN  SEMICOLON_SYM
    INSERTFIELDLIST ::= INSERTFIELD
                    ::= INSERTFIELDLIST  LIST_SEP_SYM  INSERTFIELD
    INSERTFIELD ::= STD_ID  INDEX
    PRINT_STMT ::= PRINT_CLAUSE  AT_CLAUSE  SEMICOLON_SYM
    PRINT_CLAUSE ::= PRINT  IF_EXPR  EXPR_LIST
    PRINT ::= PRINT_SYM
    AT_CLAUSE ::= AT_SYM  IF_EXPR  LIST_SEP_SYM  IF_EXPR
              ::= 
    WINDOW_STMT ::= WINDOW_SYM  IF_EXPR  LIST_SEP_SYM  IF_EXPR  AT_CLAUSE  SEMICOLON_SYM
    IF_STMT ::= ELSE_STMT
            ::= IF_CONDS
    IF_CONDS ::= IF_COND  STATEMENT
    IF_COND ::= IF_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    ELSE_STMT ::= ELSE  STATEMENT
    ELSE ::= IF_CONDS  ELSE_SYM
    SWITCH_STMT ::= CASE_LIST  RIGHTBR_SYM
    CASE_LIST ::= SWITCH_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM  LEFTBR_SYM
              ::= CASE_TESTS  STMTLIST
    CASE_TESTS ::= CASE_HEADER  COLON_SYM
               ::= CASE_LIST  DEFAULT_SYM  COLON_SYM
    CASE_HEADER ::= CASE  IF_EXPR
                ::= CASEALT  IF_EXPR
    CASE ::= CASE_LIST  CASE_SYM
    CASEALT ::= CASE_HEADER  LIST_SEP_SYM
    EXPR_STMT ::= ASG_STMT  SEMICOLON_SYM
              ::= FUNCTION  SEMICOLON_SYM
              ::= INTRINSICS  SEMICOLON_SYM
              ::= EVAL  SEMICOLON_SYM
    PAUSE_STMT ::= PAUSE_SYM  SEMICOLON_SYM
    BP_CLAUSE ::= BP_SYM  SEMICOLON_SYM
    BREAK_STMT ::= BREAK_SYM  SEMICOLON_SYM
    CONTINUE_STMT ::= CONTINUE_SYM  SEMICOLON_SYM
    RETURN_CLAUSE ::= RETURN_SYM  SEMICOLON_SYM
                  ::= RETURN_SYM  IF_EXPR  SEMICOLON_SYM
    TTS_STMT ::= TTSABORT_SYM  SEMICOLON_SYM
             ::= TTSBEGIN_SYM  SEMICOLON_SYM
             ::= TTSEND_SYM  SEMICOLON_SYM
    FLUSH_STMT ::= FLUSH  ID_LIST  SEMICOLON_SYM
    FLUSH ::= FLUSH_SYM
    TBLLOCK_STMT ::= TABLELOCK  ID_LIST  SEMICOLON_SYM
    TABLELOCK ::= TABLELOCK_SYM
    ID_LIST ::= STD_ID
            ::= ID_LIST  LIST_SEP_SYM  STD_ID
    MOVE_REC_STMT ::= NEXT_SYM  TABLE  SEMICOLON_SYM
    CHANGE_STMT ::= CHANGE_HEADER  STATEMENT
    CHANGE_HEADER ::= CHANGE  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    CHANGE ::= CHANGECOMP_SYM
           ::= CHANGESITE_SYM
    UNCHECKED_STMT ::= UNCHECKED_HEADER  STATEMENT
    UNCHECKED_HEADER ::= UNCHECKED_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
```
 

## <a name="x-language-syntax-is-stricter-in-microsoft-dynamics-ax-2012"></a>X++ 言語の構文は Microsoft Dynamics AX 2012 では厳密です
Microsoft Dynamics AX 2012 以降では、X++ の構文ルールが以前のバージョンの製品より厳しくなっています。 このトピックでは、構文の変更について説明します。

### <a name="table-of-x-syntax-changes"></a>X++ 構文変更のテーブル

次のテーブルに、Microsoft Dynamics AX 2012 で始まる構文の変更の一覧を示します。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>エリア</th>
<th>構文ルール</th>
<th>Microsoft Dynamics AX 2012 以前</th>
<th>Microsoft Dynamics AX 2012 で始まる</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>エスケープ</td>
<td>バックスラッシュ文字 <span class="code">&lt;/span&gt; は、認識されないエスケープとしてコンパイラで拒否されます</td>
<td>コンパイラは、&quot;31\12\2002&quot; を受け付けていましたが、実行時にリテラル文字列は異なる値として解釈されました。</td>
<td>現在、次の X++ ステートメントはコンパイラによって拒否されます: <span class="code">str myDateString = &quot;31\12\2002&quot;;</span>。正しい構文は、<span class="code">&quot;31\12\2002&quot;</span>です。</td>
</tr>
<tr class="even">
<td>例外</td>
<td>再試行は、catch ブロックの外部で使用できなくなった</td>
<td><strong>catch</strong> ブロックの外に <strong>retry</strong> キーワードを書き込むことができました。 これにより、実行時に<strong>再試行</strong>に達したときにプログラムが終了しました。</td>
<td>現在は、<strong>再試行</strong>が <strong>catch</strong> ブロック内部でのみ発生するようになりました。 詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。</td>
</tr>
<tr class="odd">
<td>例外</td>
<td><code>int</code> 値だけをスローおよび取得できるようになります</td>
<td><code>throw &quot;hello world&quot;;</code> などの文字列および日付のようなスカラー式をスローでき、コンパイル エラーが発生しませんでした。 実行時には、<span class="code">catch {print(&quot;Catch worked.&quot;);}</span> などの特定の値で装飾されていない <code>catch</code> ブロックによって捉えることが可能です。</td>
<td>現在、<strong>throw</strong> キーワードで配置できる唯一の式は、<code>int</code> です。 多くの場合、スローするための最もよい方法は、<span class="code">Global::error(&quot;説明&quot;);</span> です。 多くの場合、見つけるための最もよい方法は、<code>Exception</code> 列挙の要素です。 詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。</td>
</tr>
<tr class="even">
<td>継承</td>
<td>ダウン キャストは明示的にできるようになりました。
<table>
<thead>
<tr class="header">
<th><strong>メモ</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>暗黙的なダウンキャストを回避することがプログラミングのベスト プラクティスです。</td>
</tr>
</tbody>
</table></td>
<td>単純な代入演算子である等号記号 (<code>=</code>) で派生オブジェクトに基本オブジェクトを代入することができました。 コンパイラはこれらの割り当てを受け入れましたが、実行時に不適切なダウンキャスト割り当てを誤って使用するとエラーが発生しました。</td>
<td>現在は、ダウンキャストは明示的にできるようになりました。 これは、演算子と<strong>して</strong>新しく実行されます。 <strong>as</strong> キーワードによる明示的なダウンキャストは、<code>ThingClass</code> が <code>Object</code> で拡張する次のコード例で示されています。<code>ThingClass myThing = new ThingClass();</code>  <code>Object myObject = myThing;</code>  <code>myThing = myObject as ThingClass; // Explicit downcast, good.</code> 詳細については、式の演算子: 継承の Is および As を参照してください。</td>
</tr>
<tr class="odd">
<td>継承</td>
<td>基本メソッドの上書きへのアクセスを、基本メソッドより減らすことはできません。</td>
<td>基本メソッドを <strong>protected</strong> で修飾して、メソッドのオーバーライドを <strong>private</strong> とすることができました。</td>
<td>現在は、基本メソッドが<strong>保護されている</strong>場合、オーバーライド メソッドは<strong>保護</strong>または<strong>パブリック</strong>のいずれかでなければならず、<strong>プライベート</strong>にできません。 この方法の詳細については、「メソッド アクセス コントロール」を参照してください。</td>
</tr>
<tr class="even">
<td>継承</td>
<td>基本メソッドのオーバーライドは、基本メソッドとまったく同じ戻り値の型とパラメータ署名にする必要があります。</td>
<td>基本クラスに、すべてのテーブルの基準となっている <code>Common</code> テーブルのパラメーターを入力するメソッドがあったと仮定します。 派生クラスでは、代わりに <code>MyTable</code> を入力するメソッドをオーバーライド可能でした。</td>
<td>現在、基本メソッドとそのオーバーライド メソッドのパラメーター署名は、正確に一致する必要があります。 また、戻り値の型が正確に一致する必要があります。 詳細については、「メソッドの上書き」を参照してください。</td>
</tr>
<tr class="odd">
<td>インターフェイス</td>
<td>インターフェイス メソッドの実装はパラメーター署名と完全に一致する必要があります。</td>
<td>インターフェイスに、<code>int</code> のパラメーターを入力するメソッドがあると仮定します。 インターフェイスを実装するクラスでは、メソッドを <code>str</code> のパラメーターで記述可能でした。</td>
<td>現在、メソッドのパラメーター署名は、インターフェイスとクラスのメソッドの実装の間で正確に一致する必要があります。 また、戻り値の型が正確に一致する必要があります。 詳細については、「インターフェイスの概要」を参照してください。</td>
</tr>
<tr class="even">
<td>インターフェイス</td>
<td>インターフェイスを実装する非抽象基本クラスは、実装の派生クラスに依存できません。</td>
<td>基本クラスでインターフェイスを実装するとき、インターフェイスのメソッドが派生クラスによって実装された場合、基本クラスでそのメソッドを実装しないことが可能でした。 唯一の制限は、クラスで、<code>new</code> コンストラクター メソッドを呼び出せないことでした。</td>
<td>現在は、コンパイラによって、インターフェイスを実装するすべてのクラスは、インターフェイスのすべてのメソッドの完全な実装を持つまたは継承することが必須とされています。 詳細については、X++、C# の比較: オブジェクト指向プログラミングを参照してください。</td>
</tr>
<tr class="odd">
<td>モディファイア</td>
<td><strong>静的</strong>修飾子をインターフェイスに適用しないでください</td>
<td><span class="code">静的インターフェイス</span> IMyInterface {} を書き込むことができましたが、このコンテキストでは意味がないため、<strong>static</strong> モディファイアーに影響はありませんでした。</td>
<td>Dynamics AX 2009 以降、X++ コンパイラがインターフェイス宣言上で<strong>静的</strong>モディファイアーの許可をやめることがあります。 詳細については、「インターフェイスの概要」を参照してください。</td>
</tr>
<tr class="even">
<td>モディファイア</td>
<td><strong>静的</strong>修飾子を <code>new</code> コンストラクターに適用する必要があります</td>
<td><strong>静的</strong>モディファイアーを <code>new</code> コンストラクター メソッドの宣言に適用することができました。 これにより、<code>new MyClass();</code> が NULL 操作として動作するようになりました。 代わりに、ステートメント <span class="code">MyClass::new();</span> が静的な <code>new</code> メソッドを呼び出しますが、オブジェクトを構築しません。</td>
<td>現在は、<strong>静的</strong>モディファイアーが <code>new</code> メソッドに適用されるときにコンパイラはエラーを発行します。 詳細については、「コンストラクター」を参照してください。</td>
</tr>
<tr class="odd">
<td>モディファイア</td>
<td>各メソッドで明示的なアクセス修飾子を使用</td>
<td>過去には、<span class="ui">AOT</span> &gt; <span class="ui">クラス</span> &gt; <em>MyClass</em> &gt; <span class="ui">新しいメソッド</span>のメニュー項目で、アクセス修飾子のないメソッドを作成していました。 これは、メソッドが暗黙的に<strong>パブリック </strong>であることを意味しましたが、一部の X++ 開発者は既定を完全に認識していない可能性があります。 開発者がメソッドが呼び出される可能性のあるあらゆる場所を調べる必要があり、メソッドのコードを修正しなければならなかったときに、これにより余分な作業が後で発生しました。</td>
<td>現在は、<span class="ui">新しいメソッド</span>のメニュー項目において新しいメソッドの自動宣言に <strong>private</strong> キーワードが明示的に含まれています。 開発者は、必要に応じて別のモディファイアーを入力することができます。 詳細については、「メソッド モディファイア」を参照してください。</td>
</tr>
<tr class="even">
<td>パラメーター</td>
<td><code>new</code> コンストラクターの呼び出しで指定されるパラメーターは、<code>new</code> コンストラクター メソッドのパラメーターと一致する必要があります</td>
<td><code>new</code> メソッドがパラメーターを入力しないために宣言された場合でも、<code>new</code> コンストラクター メソッドの呼び出しで複数のパラメーターを渡すことができました。</td>
<td>現在は、<code>new</code> メソッドへの呼び出しは、宣言された <code>new</code> メソッドのパラメーター署名と正確に一致する必要があります。 詳細については、「サブクラスの作成」を参照してください。</td>
</tr>
<tr class="odd">
<td>パラメーター</td>
<td>既定値を持つパラメーターは、既定値がないすべてのパラメーターの後でなければなりません</td>
<td>2 つのパラメーターで取得するメソッドを宣言して、最初のパラメーターのみに既定値を提供させるようにできました。 この目的はありませんでした。 呼び出しが 2 番目のパラメーターの値を指定する必要があり、1 番目のパラメーターを省略できないため、最初のパラメーターの既定値を受け入れる方法はありませんでした。</td>
<td>現在は、メソッドの宣言において、既定値を提供するパラメーターは提供しないすべてのパラメーターの後に配置する必要があります。 詳細については、次のトピックを参照してください。
<ul>
<li>オプションのパラメーターの使用</li>
<li>パラメーターのベスト プラクティス</li>
</ul></td>
</tr>
<tr class="even">
<td>パラメーター</td>
<td>メソッドのオーバーライドには、オーバーライドされたメソッドとして同じ既定のパラメータが必要です。</td>
<td>メソッドを <span class="code">public void myMethod(int i=22){}</span> として、オーバーライドを <span class="code">public void myMethod(){}</span> として宣言することができました。 ただし、オーバーライド メソッドが <code>derivedObject(333);</code> として呼び出された場合はエラーが発生しました。</td>
<td>現在、オーバーライド メソッドは、オーバーライドされたメソッドで宣言されている順序と同じ順序で同じパラメーターの型を一覧表示する必要があります。 詳細については、「メソッドの上書き」を参照してください。</td>
</tr>
<tr class="odd">
<td>プリプロセッサ</td>
<td>コメント内の <strong>TODO</strong> は、コメントの最初の行で、最初の空白ではない文字にする必要があります。</td>
<td>複数行 <span class="code">/* ... */</span> タスク コメントで、最初のコメント行の後の他のテキストの後に <strong>TODO</strong> キーワードが出現した場合でも、<strong>TODO</strong> を検出するために使用する X++ プリプロセッサ。</td>
<td>現在は、<strong>TODO</strong> がコメントの最初の行に表示される場合、およびコメントの最初の空白ではない文字として表示される場合のみ、X++ プリプロセッサが <strong>TODO</strong> キーワードを検出します。 詳細については、「X++ 開発者タスクに対する TODO コメント」を参照してください。</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>その他のリソース
--------

[X++ 言語リファレンス](xpp-language-reference.md)


