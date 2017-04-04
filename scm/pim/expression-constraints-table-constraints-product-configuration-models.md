---
title: "製品コンフィギュレーション モデルでの式の制約とテーブルの制約"
description: "このトピックでは、式の制約およびテーブル制約の使用について説明します。 制約は、販売注文、販売見積、発注書、または製造オーダーのための製品をコンフィギュレーションするときに選択できる属性値を制御します。 制約の作成方法に基づいて、式の制約またはテーブル制約を使用できます。"
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 08 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 1fe8a0d90a3f707fa7b0fea0310c819ce5040a42
ms.lasthandoff: 03/30/2017


---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>製品コンフィギュレーション モデルでの式の制約とテーブルの制約

このトピックでは、式の制約およびテーブル制約の使用について説明します。 制約は、販売注文、販売見積、発注書、または製造オーダーのための製品をコンフィギュレーションするときに選択できる属性値を制御します。 制約の作成方法に基づいて、式の制約またはテーブル制約を使用できます。 

制約は、販売注文、販売見積、発注書、または製造オーダーのための製品をコンフィギュレーションするときに選択できる属性値の制御に使用します。 制約の作成方法に基づいて、式の制約またはテーブル制約を使用できます。

## <a name="what-are-expression-constraints"></a>式の制約とは
式の制約の特徴は、式が算術演算子およびブール演算子と関数を使用することです。 式の制約は、製品コンフィギュレーション モデルの特定のコンポーネントに書き込まれます。 他のコンポーネントで再利用することも、また他のコンポーネントと共有することもできません。 ただし、コンポーネントの式の制約は、コンポーネントのサブコンポーネントの属性を参照できます。

## <a name="what-are-table-constraints"></a>テーブル制約とは
テーブル制約では、製品のコンフィギュレーション時に属性として許される値の組み合わせをリストします。 テーブル制約の定義は、総称的に使用できます。 製品コンフィギュレーション モデルのコンポーネントのテーブル制約を作成する場合、テーブル制約定義を選択します。 許される組み合わせを作成するには、特定のタイプの属性をコンポーネントに追加します。 各属性タイプは特定の値を所有します。

### <a name="example-of-a-table-constraint"></a>テーブル制約の例

この例では、スピーカーのコンフィギュレーションを特定のキャビネットの仕上げと前グリルに限定する方法を示します。 最初の表には、コンフィギュレーションで一般に使用できるキャビネットの仕上げと前グリルを示します。 値は**キャビネットの完了**と**グリルに向かって。**属性の型に対して定義されます。

| 属性タイプ | 値                      |
|----------------|-----------------------------|
| キャビネットの仕上げ | 黒、カシ、シタン、白 |
| 前グリル    | 黒、メタル、白         |

次の表には、**色と仕上げ**テーブルの制約によって定義される組み合わせを示します。 このテーブルの制約を使用すると、カシの仕上げと黒いグリルのスピーカー、シタンの仕上げと白いグリルのスピーカーなどをコンフィギュレーションできます。

| 完了         | グリル                       |
|----------------|-----------------------------|
| カシ            | 黒                       |
| シタン       | 白                       |
| 白          | 黒                       |
| 白          | 白                       |
| 黒          | 黒                       |
| 黒          | メタル                       | 

システム定義テーブル制約とユーザー定義テーブル制約を作成できます。 詳細については、[システム定義およびユーザー定義のテーブル制約](system-defined-user-defined-table-constraints.md)を参照してください。

## <a name="what-syntax-should-be-used-to-write-constraints"></a>これらの構文が制約を作成するのに使用する必要がありますか。
制約を記述するには、OML (Optimization Modeling Language) の構文を使用する必要があります。 [制約を決済する場合でも、Microsoftの解答者の基準の制約解答者を使用します。

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>テーブル制約または式の制約の使用
制約を作成する方法に基づいて、式の制約またはテーブル制約のいずれかを使用できます。 テーブル制約はマトリックスとして構築しますが、式の制約は個別の文です。 製品をコンフィギュレーションするとき、使用する制約の種類は重要ではありません。 2 つのメソッドの違いを次に示します。  

次の制約設定を使用して製品をコンフィギュレーションする場合、以下の組み合わせを使用できますます。

-   色が黒、サイズが 30 または 50 の製品
-   色が赤、サイズが 20 の製品

### <a name="table-constraint-setup"></a>テーブル制約の設定

| 色 | サイズ |
|-------|------|
| 黒 | 30   |
| 黒 | 50   |
| 赤   | 20   |

### <a name="expression-constraint-setup"></a>式の制約設定

(色 == "黒" & (サイズ == "30" | サイズ == "50")) | (色 == "赤" & サイズ = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>式の制約の記述時に使用するのは演算子かまたはインフィックス表記法か
式の制約の記述には、使用可能なプレフィックス演算子か、またはインフィックス表記法のいずれかを使用できます。 演算子 **Min**、**Max**、および **Abs ** については、インフィックス表記法を使用できません。 これらの演算子は、ほとんどのプログラム言語に標準の演算子として含まれています。

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>式の制約の記述には、どんな演算子やインフィックス表記法を使用できますか。
次の表は、製品コンフィギュレーション モデル内のコンポーネントの式の制約を記述するときに使用できる演算子とインフィックス表記法を示します。 この最初のテーブルの例では、インフィックス表記法または演算子のいずれかを使用して式を記述する方法を示します。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>オペレーター</th>
<th>説明</th>
<th>構文</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>です。</td>
<td>これは最初の条件が false、2 番目の条件が true、または両方とも true の場合に true です。</td>
<td>[開始日]、b、挿入辞意味します: 終了]: b</td>
<td><ul>
<li><strong>オペレータ:</strong> [X意味します。= 0、Y &gt;= 0]</li>
<li><strong>インフィックス表記法:</strong> X。= 0 ]: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>かつ</td>
<td>これは、すべての条件が true の場合にのみ true です。 条件数が 0 の場合、<strong>True</strong> になります。</td>
<td>引数]、および[挿入辞: &amp; b &amp; (&amp; z</td>
<td><ul>
<li><strong>オペレータ:</strong> [との==、Y &lt;x 2 = 2]</li>
<li><strong>インフィックス表記法:</strong> == y &lt;x 2 &amp; = 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>又は</td>
<td>これは、任意の条件が true の場合に true です。 条件数が 0 の場合、<strong>False</strong> になります。</td>
<td>引数]、または[挿入辞:。~ b ~ " ~ z</td>
<td><ul>
<li><strong>オペレータ:</strong> [一部の==、Y &lt;x 2 = 2]</li>
<li><strong>インフィックス表記法:</strong> X 2 == ~ y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>プラス</td>
<td>これにより要件が合計されます。 条件数が 0 の場合、<strong>0</strong> になります。</td>
<td>プラス引数]、[挿入辞: 終了+ b + + (z</td>
<td><ul>
<li><strong>オペレーター:</strong> Plus[x, y, 2] == z</li>
<li><strong>インフィックス表記法:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>マイナス</td>
<td>これは引数を無効にします。 これは条件がきっかり 1 つの場合に限ります。</td>
<td>在庫]、[expr挿入辞: [expr</td>
<td><ul>
<li><strong>オペレーター:</strong> Minus[x] == y</li>
<li><strong>インフィックス表記法:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>ABS</td>
<td>これは、条件の絶対値を取ります。 これは条件がきっかり 1 つの場合に限ります。</td>
<td>ABS [expr]</td>
<td><strong>オペレーター:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>時間</td>
<td>これは、条件の製品を取ります。 条件数が 0 の場合、<strong>1</strong> になります。</td>
<td>[引数と、挿入]:辞 開始日* b * * (z</td>
<td><ul>
<li><strong>オペレーター:</strong> Times[x, y, 2] == z</li>
<li><strong>インフィックス表記法:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>パワー</td>
<td>これは、指数関数を取ります。 これはべき乗を右から左に適用します。  (つまり、アクセス許可連想です)。したがって、<strong>[能力の、b)、c</strong> 同等物になります <strong>[能力の[bの能力、c) ]</strong>。 <strong>Power</strong> は、指数が正の定数の場合にのみ使用できます。</td>
<td>[能力]:辞引数、挿入 ^ b払^の^ z</td>
<td><ul>
<li><strong>オペレーター:</strong> Power[x, 2] == y</li>
<li><strong>インフィックス表記法:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>最大</td>
<td>これにより、最大条件が作成されます。 条件数が 0 の場合、<strong>Infinity</strong> (無限) になります。</td>
<td>[最大値引数]</td>
<td><strong>オペレーター: </strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>最小</td>
<td>これにより、最小条件が作成されます。 条件数が 0 の場合、<strong>Infinity</strong> (無限) になります。</td>
<td>[最小値引数]</td>
<td><strong>オペレーター:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>ない</td>
<td>これにより、条件の論理逆数が作成されます。 これは条件がきっかり 1 つの場合に限ります。</td>
<td>ない]、[expr挿入辞:。expr</td>
<td><ul>
<li><strong>オペレータ:</strong> ない[X] &amp;、[Yの== 3]</li>
<li><strong>インフィックス表記法:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

次の表の例は、インフィックス表記法を記述する方法を示します。

| インフィックス表記法    | 説明                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| X " Y + z         | 追加                                                                                      |
| X \* y \* z       | 乗算                                                                                |
| x - y             | バイナリ減算は、2 番目の値が負であるバイナリ加算と同様に変換されます。 |
| X ^ z Yの^         | 右結合の累乗法                                                   |
| 。X                | ブール値の not                                                                                   |
| X ]: y            | Boolean の意味                                                                           |
|  x | y | z         | ブール値 or                                                                                    |
| X (Y (z         | ブール値 and                                                                                   |
| X == Yの== z       | 等式                                                                                      |
| X。" Y。= z       | 明確                                                                                      |
| X &lt; y &lt; z   | 次の値より小さい                                                                                     |
| X &gt; y &gt; z   | 次の値より大きい                                                                                  |
| X &lt;" Y &lt;= z | 以下                                                                         |
| X &gt;" Y &gt;= z | 以上                                                                      |
|  (x)                | かっこは既定の優先順位より優先されます。                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>式の制約がなぜ正しく検証されないのですか。
製品コンフィギュレーション モデルの属性、コンポーネント、またはサブコンポーネントのソルバー名として予約済みのキーワードは使用できません。 使用できる引当済キーワードの一覧を挙げます。:

-   シーリング
-   要素
-   等しい
-   フロア
-   次の場合
-   未満
-   大きい
-   です。
-   ログ
-   最大
-   最小
-   マイナス
-   プラス
-   パワー
-   時間
-   スロット
-   モデル
-   意思決定
-   目標


<a name="see-also"></a>参照
--------

[式の制約 (作業ガイドを作成する) ] (http://ax.help.dynamics.com/en/wiki/create-an-expression-constraint/)

[製品モデル コンフィギュレーション (作業ガイド追加する) に計算を] (http://ax.help.dynamics.com/en/wiki/add-a-calculation-to-a-product-configuration-model/)


