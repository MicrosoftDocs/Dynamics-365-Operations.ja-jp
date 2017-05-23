---
title: "財務諸表デザイナーでの行の定義"
description: "行定義は、財務レポートの各行の内容を指定する、レポート コンポーネントまたは構成要素です。 行定義は、複数の会社が使用できる構成要素グループを作成するために、列定義、レポート ツリー定義およびレポートの定義と組み合わせることができます。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: aa9fcc4d0c122d2355362b75ca210af4c2ef4338
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="row-definitions-in-financial-report-designer"></a>財務諸表デザイナーでの行の定義

[!include[banner](../includes/banner.md)]


行定義は、財務レポートの各行の内容を指定する、レポート コンポーネントまたは構成要素です。 行定義は、複数の会社が使用できる構成要素グループを作成するために、列定義、レポート ツリー定義およびレポートの定義と組み合わせることができます。

<a name="create-a-row-definition"></a>行定義の作成
-----------------------

1.  レポート デザイナーのナビゲーション ウィンドウで、[**行の定義**] をクリックします。
2.  [**ファイル**] メニューの [**新規**] をクリックし、[**行定義**] をクリックします。 各セルの内容に関する詳細については、[行定義セルの変更](modify-row-definition-cells-financial-reporting.md)を参照してください。

## <a name="open-a-row-definition"></a>行定義を開く
1.  レポート デザイナーのナビゲーション ウィンドウで、[**行の定義**] をクリックします。
2.  行定義の名前をダブルクリックして開きます。
3.  行定義に関連付けられている構成要素を表示するには、行定義を右クリックし、[**関連**] を選択します。

## <a name="contents-of-a-row-definition"></a>行定義の内容
行定義は、最大 20,000 行の財務分析コードを保有することができ、次の情報を含むことができます:

-   [**現金**] または [**総収益**] などのセクションの見出し、明細行、およびスペースを作成することでレポートに意味を追加する説明用テキストです。
-   Microsoft Dynamics 365 for Operations の分析コード値を含めることができる財務データへのリンク [**注記:**] レポートが生成されるたびに財務分析コード システムからデータを取得するよう行定義を設定できます。
-   リンクされている財務データに基づく行の合計と式です

通常、行定義の各行には以下の情報タイプの 1 つが含まれています:

-   財務分析コード システムへの参照です
-   データに基づく合計または計算です
-   フォーマット

行定義に情報を入力するには 2 つの方法があります。

-   手動で新しい行定義に行情報を入力します。 詳細については、[行定義セルの変更](modify-row-definition-cells-financial-reporting.md)を参照してください。
-   財務分析コードから行情報を直接プルするには、レポート デザイナーを使用します。 詳細については、「[行定義セルの変更](modify-row-definition-cells-financial-reporting.md)」の「関連するフォーミュラ / 行 / 単位」を参照してください。

## <a name="add-dimensions-in-a-row-definition"></a>行定義への分析コードの追加
分析コードは、データおよび値の交差です。 レポート デザイナーでデータおよび値をグループ化することができます。 トランザクションをより詳細に分類および分析できます。 [**分析コードから行を挿入**] ダイアログ ボックスを使用して、行定義に複数の行を同時に追加できます。 ダイアログ ボックスは、分析コードごとに 1 つの列を表示します。 次の表では、各分析コードで指定する情報のタイプを示します。

| オプション                | 説明                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 分析コード             | 行定義に追加する分析コードを識別するパターンです。 このパターンには、分析コードの各位置に対応する 1 つのアンパサンド (&) または番号記号 (\#) が含まれます。 通常、[主勘定分析コード] にはすべてアンパサンドを、他の分析コードにはすべて番号記号を使用します。 |
| 分析コード範囲の開始 | 行定義に追加するこの分析コードの最初の値です。                                                                                                                                                                                                                 |
| 分析コード範囲の終了   | 行定義に追加するこの分析コードの最後の値です。                                                                                                                                                                                                                  |

行定義に分析コードを追加するには、次のステップを実行します。

1.  レポート デザイナーで [**列定義**] をクリックして変更する行定義を開きます。
2.  [**編集**] メニューで [**分析コードから行を挿入**] をクリックします。
3.  [**分析コードから行を挿入**] ダイアログ ボックスの [**分析コード**] 行で、行定義に転送する分析コードのセルを選択し、[**すべて &&&**] をクリックします。
4.  行定義を特定の範囲の分析コード値に限定するには、[**分析コード範囲の開始**] セルに開始分析コード値を、[**分析コード範囲の終了**] セルに終了分析コード値を入力します。 選択した分析コードのすべての値を対象とする場合は、これらのセルは空白のままにします。 [**メモ:**] 分析コードの範囲にワイルドカード (\* または ?) を使用すると、ERP データベースのデータの照合方法によっては意図した結果が返されない場合があります。
5.  [**開始行コード**] フィールドで、行定義に追加する最初の分析コード値の行コードを指定します。
6.  [**行の増分**] フィールドで、連続する行コード間の間隔を指定します。 たとえば、最初の行コードが 100 で増分値が 30 の場合、最初の新しい行コードは 100、130、160、190、および 220 になります。 新しいフォーマットおよぶ式のフォーミュラを挿入するための十分なスペースを提供する増分値を使用します。
7.  [**OK**] をクリックします 選択した分析コード値ごとに 1 つの行が行定義に追加されます。

## <a name="adjust-rounding-in-a-row-definition"></a>行定義の丸めの調整
金額が丸められた貸借対照表がある場合は、合計が不均衡になる場合があります。 この問題は、たとえば、貸借対照表レポートに丸めオプションを使用して、レポート定義が丸め処理を指定した場合でも発生することがあります。 行定義のオプションの [**丸め調整行**] オプションを使用して、貸借対照表の金額を調整できます。 レポート定義の [**設定**] タブで丸めのオフまたは変更ができます。 次の表に、金額の丸め方法を示します。 次の表では、丸めがオフになっている場合、行 100 と行 200 の合計が異なります。

| 行コード | 丸めを使用しない金額 | 千の単位に丸められた金額 |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| 小計    | 7,300                    | 8                                       |

貸借対照表の丸めを調整するには、次のステップを実行します。

1.  レポート デザイナーで [**列定義**] をクリックして変更する行定義を開きます。
2.  [**編集**] メニューで、[**丸め調整**] をクリックします。
3.  [**丸め調整**] ダイアログ ボックスに次の値を入力します:
    -   [**丸め調整行**] – 貸借対照表の収支を合わせるために調整される行の行コードです。
    -   [**総資産の行**] – 総資産を含む貸借対照表の行の行コードです。
    -   [[**負債合計および資本の行**] – 負債合計および資本を含む貸借対照表の行の行コードです。
    -   [**調整金額の制限**] – 自動調整での制限に指定する正の整数です。 この金額は、実際の丸め誤差の絶対値と比較されます。

    **注記:**これらの行コードは、財務データとリンクしている必要があります。 つまり、行の [**財務分析コードへのリンク**] セルには分析コード値が必要です。 説明 (**DESC**)、計算 (**CALC**)、または合計 (**TOT**) の行を参照**しない**でください。

丸めがオンの場合は、貸借対照表の金額が均等に釣り合います。 **注記:**調整の制限は、レポート定義に対して指定されている [**丸め精度**] オプションに基づいて適用されます。 たとえば、レポートで千の位で丸めるよう選択し [**調整金額の制限**] フィールドに「**2**」を入力すると、[**丸め調整行**] フィールドで識別された値が $2,000 単位で増加または減少した場合に警告メッセージが表示されます。

## <a name="format-row-and-column-text"></a>行および列のテキストの書式設定
フォントを変更しテキストの書式を設定することにより、レポートの外観をカスタマイズできます。 次のセクションでは、レポートの行および列の外観の書式を設定する方法を説明します。

### <a name="manage-font-styles"></a>フォント スタイルの管理

レポートのフォント スタイルを作成し、変更できます。 ドキュメント、またはレポートの特定の行または列に、それらのスタイルを適用できます。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>フォント スタイルの作成</td>
<td><ol>
<li>レポート デザイナーの [<strong>書式設定</strong>] メニューで [<strong>スタイルおよびフォーマット</strong>] をクリックします。</li>
<li>[<strong>スタイルおよびフォーマット</strong>] ダイアログ ボックスの [<strong>新規</strong>] をクリックして、新しいスタイル用の一意の名前を入力します。</li>
<li>フォントを選択して [<strong>OK</strong>] をクリックします。</li>
</ol></td>
</tr>
<tr class="even">
<td>フォント スタイルの変更</td>
<td><ol>
<li>レポート デザイナーの [<strong>書式設定</strong>] メニューで [<strong>スタイルおよびフォーマット</strong>] をクリックします。</li>
<li>[<strong>スタイルおよびフォーマット</strong>] ダイアログ ボックスで、変更するスタイルを選択し、[<strong>変更</strong>] をクリックします。</li>
<li>フォントを選択して [<strong>OK</strong>] をクリックします。</li>
</ol></td>
</tr>
<tr class="odd">
<td>フォント スタイルの適用</td>
<td><ol>
<li>レポート デザイナーの、定義または列定義、あるいはフッターとヘッダーで、1 つ以上のセルを選択します。</li>
<li>ツール バー上の [<strong>スタイル</strong>] 一覧で、フォント スタイルを選択します。</li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>行のテキストの書式設定

列定義で指定された書式は、レポート定義で指定された書式を上書きします。 テキスト形式を変更するには、書式設定ツールバーのコントロールを使用します。 これらのコントロールは Microsoft Windows の標準コントロールです。

1.  レポート デザイナーで、変更する列定義を開きます。
2.  書式を設定するセルを選択します。 複数のセルを選択する場合は、Ctrl キーを押しながらセルを選択します。
3.  適用するフォーマットのツール バーのボタンをクリックします。 たとえば行をインデントにするには、行を選択し、ツール バーの **インデントの増加** ![インデントの増加](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "インデントの増加") をクリックします。

### <a name="adjust-columns-while-you-design-reports"></a>レポートのデザイン中に列を調整

行定義内の作業中の列を見やすくするには、ビュー ウィンドウ内の列の幅を調整し、列を表示または非表示にすることもできます。 加えた変更は、画面に表示される列の外観にだけ影響を与えます。 レポートの書式設定列には影響しません。

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>ビュー ウィンドウ内の列の幅の変更

1.  レポート デザイナーで、変更する列定義を開きます。
2.  [**書式設定**] メニューで、[**列の幅**] を選択します。
3.  [**列の幅**]ダイアログ ボックスで、ファイル名を入力し、次に [**OK**] をクリックします。 または、列の見出しの右側の境界をドラッグして列の幅を変更することもできます。

### <a name="hide-columns-in-the-view-pane"></a>ビュー ウィンドウ内の列の非表示

1.  レポート デザイナーで、変更する列定義を開きます。
2.  最小化する列を選択します。
3.  右クリックしてから、[**非表示**] をクリックします。

### <a name="show-all-hidden-columns-in-the-view-pane"></a>ビュー ウィンドウ内のすべての非表示の列を表示

1.  レポート デザイナーで、変更する列定義を開きます。
2.  表示する最小化された列を右クリックし、[**非表示解除**] をクリックします。


<a name="see-also"></a>参照
--------

[財務報告](financial-reporting-intro.md)



