---
title: "電子申告 (ER) のフォーミュラ デザイナー"
description: "このトピックでは、電子申告 (ER) でのフォーミュラ デザイナーの使用方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f0ded563ecf0b6d0ce67f046f631d8c4dcfc7802
ms.openlocfilehash: 1dc584355c8992ee701169fd5d29ad7b0300a498
ms.contentlocale: ja-jp
ms.lasthandoff: 10/22/2018

---

# <a name="formula-designer-in-electronic-reporting-er"></a>電子申告 (ER) のフォーミュラ デザイナー

[!include [banner](../includes/banner.md)]

このトピックでは、電子申告 (ER) でのフォーミュラ デザイナーの使用方法を説明します。 ER の特定の電子ドキュメントの形式を設計する場合、データを変換する式を使用して、ドキュメントのフルフィルメントおよび書式設定の要件を満たすことができます。 これらの式は、Microsoft Excel の式と類似しています。 テキスト、日時、算術、論理、情報、データ型変換、およびその他 (ビジネス ドメインの特定の関数) といったさまざまなタイプの関数が式でサポートされています。

## <a name="formula-designer-overview"></a>フォーミュラ デザイナーの概要

ER はフォーミュラ デザイナーをサポートします。 したがって、設計時に次のタスクに使用できる式を実行時にコンフィギュレーションできます。

- ER フォーマットのデータ ソースとして設計された ER データ モデルに入力する必要のある Microsoft Dynamics 365 for Finance and Operations データベースから受け取るデータの変換。 (たとえば、これらの変換にはフィルタ処理、グループ化、およびデータ型の変換が含まれる可能性があります。)
- 特定の ER フォーマットのレイアウトや条件に従って電子ドキュメントを生成するため、フォーマット データを送信する必要があります。 (たとえば、書式設定は、要求された言語またはカルチャ、またはエンコードに従って行われる可能性があります)。
- 電子ドキュメントを作成するプロセスを制御します。 (たとえば、式は、実行しているデータによってフォーマットの特定の要素の出力を有効または無効にできます。 これらはドキュメントの作成プロセスを中断したり、またはユーザーにメッセージをスローすることもできます。)

次のいずれかのアクションを実行する際 **フォーミュラ デザイナー** ページを開くことができます。

- データ モデルのコンポーネントへのデータ ソース項目のバインド。
- 形式コンポーネントへのデータ ソース項目のバインド。
- データ ソースの一部である計算済フィールドのメンテナンス完了。
- ユーザー入力パラメーターの表示条件の定義。
- 形式の変換の設計。
- 形式のコンポーネントに有効にする条件の定義。
- 形式のファイル コンポーネントに対するファイル名の定義。
- プロセス制御検証の条件の定義。
- プロセス制御検証のメッセージ テキストの定義。

## <a name="designing-er-formulas"></a>ER フォーミュラ デザイナー

### <a name="data-binding"></a>データ バインディング

ER フォーミュラ デザイナーは、実行時にデータ消費者に入力できるよう、データ ソースから受信されたデータを変換する式を定義するのに使用できます。

- Finance and Operations データ ソースとランタイム パラメーターから ER データ モデルへ
- ER データ モデルから ER 形式へ
- Finance and Operations データ ソースとランタイム パラメーターから ER 形式へ

次の図は、このタイプの式の設計を示しています。 この例では、式は、Finance and Operations のイントラスタット テーブルの **Intrastat.AmountMST** フィールドの値を小数点以下 2 桁に丸め、その丸めた値を返します。

[![データ バインディング](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

次の図は、このタイプの式を使用できる方法を示しています。 この例では、入力された式の結果が、**税申告モデル** データ モデルの **Transaction.InvoicedAmount** コンポーネントに反映されます。

[![使用されているデータ バインディング](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

実行時に、デザイン式 **ROUND (Intrastat.AmountMST, 2)** は、イントラスタット テーブルの各レコードに対する **AmountMST** フィールドの値を小数点以下 2 桁に丸めます。 **税レポート** データ モデルの **Transaction.InvoicedAmount** コンポーネントで丸めの値を入力します。

### <a name="data-formatting"></a>データの書式設定

ER フォーミュラ デザイナーは、電子ドキュメント生成の一部として送信できるよう、データ ソースから受信されたデータを書式設定する式を定義するのに使用できます。 フォーマットに対して再使用すべき、標準的なルールとして適用されるはずの書式設定があります。 この場合、フォーマット式を持つ名前付きの変換として、書式設定のコンフィギュレーションで 1 度の書式設定を導入することができます。 この名前付き変換は、作成したフォーマット式に従って出力を書式設定する必要がある多くの形式コンポーネントに後でリンクできます。

次の図は、このタイプの変換の設計を示しています。 この例では、**TrimmedString** 変換は、先頭および末尾にあるスペースを削除することにより **文字列** データ型の受信データを切り詰めます。 その後、切り詰めた文字列を返します。

[![変換](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

次の図は、このタイプの変換を使用できる方法を示しています。 この例では、いくつかの形式のコンポーネントは、実行時に生成する電子ドキュメントにテキストを出力として送信します。 これらすべての形式のコンポーネントは、名前で **TrimmedString** 変換へと参照します。

[![使用されている変換](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

前の図の**partyName** コンポーネントなどの形式コンポーネントが **TrimmedString**変換を参照する場合、変換は生成する電子ドキュメントへの出力としてテキストを送信します。 このテキストには、先頭および末尾にあるスペースは含まれません。

個別に適用する必要のある形式の場合、特定形式コンポーネントのバインディングの個別の式として導入できます。 次の図は、このタイプの式を示しています。 この例では、**partyType** の形式コンポーネントは、データ ソースの **Model.Company.RegistrationType** フィールドからの受信データを大文字テキストに変換する式を介してデータ ソースにバインドされます。 式は、そのテキストを出力として、電子ドキュメントに送信します。

[![個々のコンポーネントに書式設定を適用](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>プロセス フローの制御

ER フォーミュラ デザイナーは、電子ドキュメントを生成するプロセス フローを制御する式を定義するために使用できます。 実行できるタスクは次のとおりです。

- ドキュメント作成のプロセスを停止する必要がある場合を判断する条件を定義します。
- 停止したプロセスに対してユーザーにメッセージを作成する式を指定するか、または報告書作成のプロセスに関する実行ログ メッセージをスローする式を指定します。
- 電子ドキュメント生成のファイル名と作成の管理条件を指定します。

プロセス フロー制御の各ルールは、個々の検証として設計されています。 次の図は、このタイプの検証を示しています。 この例のコンフィギュレーションの説明を次に示します。

- 検証は、XML ファイルの生成中に **INSTAT** ノードが作成されたときに評価されます。
- トランザクションのリストが空である場合、検証の実行プロセスを停止し、**FALSE** を返します。
- 検証では、ユーザーの優先的に使用する言語で Finance and Operations ラベル SYS70894 のテキストを含むエラー メッセージを返します。

[[![検証](./media/picture-validation.jpg)](./media/picture-validation.jpg)]

ER フォーミュラ デザイナーは生成する電子ドキュメントのファイル名の生成や、ファイルの作成プロセスの制御にも使用できます。 次の図は、このタイプのプロセス フロー制御の設計を示しています。 この例のコンフィギュレーションの説明を次に示します。

- **model.Intrastat** データ ソースからのレコードの一覧はバッチに分かれています。 バッチごとに、最大1,000 レコードが含まれています。
- 出力は、作成されたバッチごとに XML 形式のファイル 1 つを含む zip ファイルを作成します。
- 式はファイル名とファイル名拡張子を連結して、生成する電子ドキュメントにファイル名を返します。 2 番目のバッチ以降すべてのバッチには、ファイル名の接尾語としてバッチ ID が表示されます。
- 式は、(**TRUE** を返すことで) 少なくともレコードを 1 つ含むバッチのファイル作成プロセスを有効にします。

[![ファイル管理](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>基本構文

ER の式は、次のいずれかまたはすべての要素を含めることができます。

- 定数
- 演算子
- 参照
- パス
- 関数

#### <a name="constants"></a>定数

式の設計時に、テキストおよび数値定数 (つまり、計算されない定数) を使用できます。 たとえば、**VALUE ("100") + 20** の式では、数値定数 **20** および文字列定数 **"100"** を使用し **120** という数値を返します。 ER フォーミュラ デザイナーはエスケープ シーケンスをサポートします。 したがって、別の方法で処理されるべき式文字列を指定することができます。 たとえば、**レフ トルストイ戦争と平和ボリューム 1** の式は、**レフ トルストイ「戦争と平和」ボリューム 1** という文字列を返します。

#### <a name="operators"></a>演算子

次の表に、加算、減算、乗算、除算などの基本的な数学演算の実行に使用できる算術演算子を示します。

| オペレーター | 意味               | 例 |
|----------|-----------------------|---------|
| +        | 追加              | 1+2     |
| -        | 減算、否定 | 5-2, -1 |
| \*       | 乗算        | 7\*8    |
| /        | 区分              | 9/3     |

次の表に、サポートされる比較演算子を示します。 これらの演算子を使用して、2 つの値を比較することができます。

| オペレーター | 意味                  | 例    |
|----------|--------------------------|------------|
| =        | 等しい                    | X=Y        |
| &gt;     | 次の値より大きい             | X&gt;Y     |
| &lt;     | 次の値より小さい                | X&lt;Y     |
| &gt;=    | 以上 | X&gt;=Y    |
| &lt;=    | 以下    | X&lt;=Y    |
| &lt;&gt; | 次の値に等しくない             | X&lt;&gt;Y |

また、テキスト連結演算子としてアンパサンド (&) を使用することができます。 これにより、1 つ以上の文字列を 1 つのテキストに結合または連結することができます。

| オペレーター | 意味     | 例                                             |
|----------|-------------|-----------------------------------------------------|
| &        | 連結 | "印刷対象なし" & ":&nbsp;" & "レコードが見つかりません" |

##### <a name="operator-precedence"></a>演算子の優先順位

複合式のパーツを評価する順番は重要です。 たとえば、**1 + 4/2** の式の結果は、先に加算または除算のどちらを実行するかによって異なります。 明示的に式の評価方法を定義するためにかっこを使用できます。 たとえば、加算を最初に実行する必要があることを示すには、前の式を **(1 + 4) /2** に変更できます。 式で工程の順序を明確に定義しない場合、順序はサポートされる演算子に割り当てられている既定の優先順位に基づきます。 次の表に、各演算子に割り当てられている優先順位を示します。 高い優先順位 (たとえば、7) がある演算子は、低い優先順位 (たとえば、1) がある演算子より前に評価されます。

| 優先順位 | 演算子      | 構文                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | グループ化       | ( … )                                                                   |
| 6          | メンバーのアクセス  | … します。 …                                                                   |
| 5          | 関数の呼び出し  | … ( … )                                                                 |
| 4          | 乗算 | … \* …<br>… / …                                                         |
| 3          | 付加       | … + …<br>… - …                                                          |
| 2          | 比較     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | 区切り     | … , …                                                                   |

式に同じ優先順位を持つ複数の連続した演算子が含まれている場合は、これらの操作は左から右に評価されます。 たとえば、**1 + 6 / 2 \* 3 &gt; 5** の式は **true** を返します。 式の閲覧や管理を簡単にするよう、式で操作する希望の順序を明示的に示すために、かっこを使用することをお勧めします。

#### <a name="references"></a>参照

式の設計中に使用できる現在の ER コンポーネントのすべてのデータ ソースは名前付き参照を使用できます。 (現在の ER コンポーネントは、モデルまたは形式のいずれかです。) たとえば、現在の ER データ モデルに **ReportingDate** データ ソースが含まれており、このデータ ソースは、**DATETIME** データ型の値を返します。 生成ドキュメントでその値を正しく書式設定するために、**DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")** の式のデータ ソースを参照できます。

アルファベットの文字で表されない参照元のデータ ソースの名前のすべての文字は、単一引用符 (') の後に続く必要があります。 参照データ ソースの名前がアルファベットの文字を表さない記号を少なくとも 1 つ含む場合、名前を単一引用符で囲む必要があります。 (たとえば、これらアルファベットでない記号は、句読点またはそのほかの書面記号です。) いくつかの例を挙げます。

- **今日の日付 & 時間** データ ソースは、**'今日の日付 & 時間’** のように ER の式で参照する必要があります。
- **Customers** データ ソースの **name()** メソッドは、ER の式で **Customers.’name()’** のように参照する必要があります。 

Finance and Operations データ ソースのメソッドにパラメータがある場合は、次の構文を使用して、これらのメソッドを呼び出します。

- **システム**データ ソースの **isLanguageRTL** メソッドが、**文字列** データ型の **EN-US** パラメーターを含む場合、このメソッドは ER 式で **System.'isLanguageRTL'("EN-US")** として参照する必要があります。
- メソッド名に英数字シンボルのみが含まれている場合、引用符は必須ではありません。 ただし、名前にかっこが含まれている場合、テーブルのメソッドに対しては必須です。

**システム** データ ソースが、**グローバル** Finance and Operations アプリケーション クラスを参照する ER マッピングに追加される場合、式はブール値 **FALSE** を返します。 変更された式 **System.' isLanguageRTL'("AR")** はブール値**TRUE** を返します。

値がこのメソッドのタイプのパラメータに渡される方法を制限することができます。

- このタイプのメソッドに、定数だけを渡すことができます。 定数の値は、デザイン時に定義されます。
- このタイプのパラメーターで、プリミティブ (基本) データ型のみがサポートされています。 (プリミティブ データ型は整数、実数、ブール値、文字列などです。)

#### <a name="paths"></a>パス

式が構成されたデータ ソースを参照する場合、そのデータ ソースの特定のプリミティブ要素の選択にパス定義を使用できます。 ドット (.) は、構成されたデータ ソースの個別要素を区切るために使用します。 たとえば、現在の ER データ モデルには **InvoiceTransactions** データ ソースが含まれ、このデータ ソースはレコード一覧を返します。 **InvoiceTransactions** レコード構造には、**AmountDebit** および **AmountCredit** フィールドが含まれており、どちらのフィールドも数値を返します。 したがって、請求額を計算するには次の式を設計できます。**InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**。

#### <a name="functions"></a>関数

次のセクションでは、ER の式で使用できる関数について説明します。 すべてのデータ ソースの式のコンテキスト (現在の ER データ モデルまたは ER フォーマット) は、呼び出し元関数の引数に従って呼び出し元関数のパラメータとして使用できます。 定数は、呼び出し関数のパラメータとしても使用できます。 たとえば、現在の ER データ モデルには **InvoiceTransactions** データ ソースが含まれ、このデータ ソースはレコード一覧を返します。 **InvoiceTransactions** レコード構造には、**AmountDebit** および **AmountCredit** フィールドが含まれており、どちらのフィールドも数値を返します。 したがって、請求額を計算するには、ER 丸め関数を使用する次の式を設計できます。**ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**。

## <a name="supported-functions"></a>サポートされている機能

次の表で、ER データ モデルと ER レポートを設計するために使用できるデータ操作関数を説明します。 関数の一覧が固定されていません。 開発者は、それを拡張できます。 使用できる関数の一覧を表示するには、ER フォーミュラ デザイナーの関数ウィンドウを開きます。

### <a name="date-and-time-functions"></a>日時の関数

| 機能 | 説明 | 例 |
|----------|-------------|---------|
| ADDDAYS (日時, 日数) | 指定された日時値までの指定された日数を追加します。 | **ADDDAYS (NOW(), 7)** は、将来の日時の 7 日を返します。 |
| DATETODATETIME (日付) | 日時値に指定された日付値を変換します。 | **DATETODATETIME (CompInfo. 'getCurrentDate()')** は、現在の Finance and Operations セッションの日付 2015 年 12 月 24 日を **12/24/2015 12:00:00 AM** として返します。 この例では、**CompInfo** は、**Finance and Operations/Table** タイプの ER データ ソースで、CompanyInfo テーブルを参照します。 |
| NOW () | 日時値として現在の Finance and Operations アプリケーション サーバーの日時を返します。 | |
| TODAY () | 日付値として現在の Finance and Operations アプリケーション サーバーの日付を返します。 | |
| NULLDATE () | **null** の日付値を返します。 | |
| NULLDATETIME () | **null** の日時値を返します。 | |
| DATETIMEFORMAT (日時, 形式) | 指定された形式の文字列に指定された日時値を変換します。 (サポートされている形式の詳細については、「[標準](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)」と「[カスタム](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)」を参照してください。) | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** は、指定されたカスタム形式に基づいて、現在の Finance and Operations アプリケーション サーバーの日付 2015 年 12 月24 日を **"24-12-2015"** として返します。 |
| DATETIMEFORMAT (日時, 形式, カルチャ) | 指定された形式および [カルチャ](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)の文字列に指定された日時値を変換します。 (サポートされている形式の詳細については、「[標準](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)」と「[カスタム](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)」を参照してください。) | **DATETIMEFORMAT (NOW(), "d", "de")** は、選択されたドイツのカルチャに基づいて、現在の Finance and Operations アプリケーション サーバーの日付 2015 年 12 月 24 日を **"24.12.2015"** として返します。 |
| SESSIONTODAY () | 日付値として現在の Finance and Operations セッションの日付を返します。 | |
| SESSIONNOW () | 日時値として現在の Finance and Operations セッションの日時を返します。 | |
| DATEFORMAT (日付, 形式) | 指定された形式で指定された日付の文字列形式を返します。 | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy"** は、指定されたカスタム形式に基づいて、現在の Finance and Operations セッションの日付 2015 年 12 月24 日を **"24-12-2015"** として返します。 |
| DATEFORMAT (日付, 形式, カルチャ) | 指定された形式および[カルチャ](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)の文字列に指定された日付値を変換します。 (サポートされている形式の詳細については、「[標準](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)」と「[カスタム](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)」を参照してください。) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** は、選択されたドイツのカルチャに基づいて、現在の Finance and Operations セッションの日付 2015 年 12 月 24 日を **"24.12.2015"** として返します。 |
| DAYOFYEAR (日付) | 1 月 1 日から指定された日までの日数の整数表現を返します。 | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** は **61** を返します。 **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** は **1** を返します。 |
| 日 (日付 1、日付 2) | 最初に指定した日付および 2 番目に指定した日付間の日数を返します。 最初の日付が 2 番目の日付より遅い場合は正の値を返し、最初の日付が 2 番目の日付と同じである場合は **0** (ゼロ) を返します。最初の日付が 2 番目の日付より早い場合は、負の値を返します。 | **日数 (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** は **-1** を返します。 |

### <a name="data-conversion-functions"></a>データ変換機能

| 職務 | 説明 | 例 |
|----------|-------------|---------|
| DATETODATETIME (日付) | 日時値に指定された日付値を変換します。 | **DATETODATETIME (CompInfo. 'getCurrentDate()')** は、現在の Finance and Operations セッションの日付 2015 年 12 月 24 日を **12/24/2015 12:00:00 AM** として返します。 この例では、**CompInfo** は、**Finance and Operations/Table** タイプの ER データ ソースで、CompanyInfo テーブルを参照します。 |
| DATEVALUE (文字列、形式) | 指定された形式で指定された文字列の日付形式を返します。 | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** は、指定されたカスタム形式および既定のアプリケーションの **EN-US** カルチャに基づいて、日付 2016 年 12 月 21 日を返します。 |
| DATEVALUE (文字列、形式、カルチャ) | 指定された形式およびカルチャで指定された文字列の日付形式を返します。 | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** は、指定されたカスタム形式とカルチャに基づいて日付 2016 年 1 月 21 日を返します。 ただし、**DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** は、指定した文字列が有効な日付として認識されていないことをユーザーに通知して、例外をスローします。 |
| DATETIMEVALUE (文字列、形式) | 指定された形式で指定された文字列の日時形式を返します。 | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** は、指定されたカスタム形式と既定のアプリケーションの **EN-US** カルチャで、2016 年 12 月 21 日 2 時 55 分 00 秒を返します。 |
| DATETIMEVALUE (文字列、形式、カルチャ) | 指定された形式およびカルチャで指定された文字列の日時形式を返します。 | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** は、指定されたカスタム形式とカルチャに基づいて、2016 年 12 月 21 日 2 時 55 分 00 秒を返します。 ただし、**DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** は、指定した文字列が有効な日時として認識されていないことをユーザーに通知して、例外をスローします。 |

### <a name="list-functions"></a>リスト機能

<table>
<thead>
<tr>
<th>職務</th>
<th>説明</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPLIT (入力, 長さ)</td>
<td>指定された入力文字列を指定された長さのサブ文字列に分割します。 新しいリストとして結果を返します。</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> は、<strong>文字列</strong> フィールドがある 2 つのレコードで構成される新しいリストを返します。 最初のレコードのフィールドには、テキスト <strong>&quot;abc&quot;</strong> が、2 つ目のレコードのフィールドには、テキスト <strong>&quot;d&quot;</strong> が入力されます。</td>
</tr>
<tr>
<td>SPLIT (入力、区切り記号)</td>
<td>指定された入力文字列を指定された区切り記号に基づいてサブ文字列に分割します。</td>
<td><strong>SPLIT (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong> は、<strong>STRING</strong> フィールドがある 3 つのレコードで構成される新しいリストを返します。 最初のレコードのフィールドには、テキスト <strong>&quot;X&quot;</strong> が、2 つ目のレコードのフィールドには、テキスト&quot;&nbsp;&quot;が、3 つ目のレコードのフィールドにはテキスト <strong>&quot;y&quot;</strong> が入力されます。 区切り記号が空の場合、入力テキストを含む <strong>文字列</strong> フィールドを持つ 1 つのレコードで構成される新しいリストが返されます。 入力が空の場合は、新しい空のリストが返されます。
入力または区切り記号のいずれかを指定しない場合 (null)、アプリケーション例外がスローされます。</td>
</tr>
<tr>
<td>SPLITLIST (リスト, 番号)</td>
<td>それぞれ指定されたレコード数を含むバッチに指定されたリストを分割します。 次の要素を含むバッチの新しいリストとして結果を返します。
<ul>
<li>通常のリストとしてのバッチ (<strong>値</strong>コンポーネント)</li>
<li>現在のバッチ番号 (<strong>BatchNumber</strong>コンポーネント)</li>
</ul>
</td>
<td>次の図では、<strong>明細行</strong> データ ソースが、3 つのレコードのレコード一覧として作成されます。 このリストは、それぞれ最大 2 つのレコードを含むバッチに分割されます。
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>次の図は、設計された形式レイアウトを示します。 この形式のレイアウトでは、XML 形式で出力を生成するために作成される <strong>明細行</strong> データ ソースにバインディングされます。 この出力は、各バッチとその中のレコードに対する個々のノードを表示します。</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>次の図は、設計された形式が実行される際の結果を示します。</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (レコード 1 [, レコード 2, ...])</td>
<td>指定された引数から作成される新しいリストを返します。</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> は、空のレコードを返し、フィールドの一覧には、<strong>MainData</strong> および <strong>OtherData</strong> のレコード リストのすべてのフィールドが含まれます。</td>
</tr>
<tr>
<td>LISTJOIN (リスト 1, リスト 2, ...)</td>
<td>指定された引数のリストから作成した結合されたリストを返します。</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> は、6 つのレコードのリストを返し、<strong>文字列</strong>データ型のフィールドの 1 つに単一の文字が含まれます。</td>
</tr>
<tr>
<td>ISEMPTY (リスト)</td>
<td>指定されたリストに要素がない場合、<strong>TRUE</strong> を返します。 それ以外の場合は、<strong>FALSE</strong> を返します。</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (リスト)</td>
<td>指定されたリストをリスト構造のソースとして使用し、空のリストを返します。</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> は、<strong>SPLIT</strong> 関数で返ってきたリストと同じ構造を持つ新しい空のリストを返します。</td>
</tr>
<tr>
<td>FIRST (リスト)</td>
<td>指定されたリストの最初のレコードが空でない場合、そのレコードを返します。 それ以外の場合は、例外をスローします。</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (リスト)</td>
<td>指定されたリストの最初のレコードが空でない場合、そのレコードを返します。 それ以外の場合は、<strong>null</strong> レコードを返します。</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (リスト)</td>
<td>指定されたリストの最初の項目だけを含んだリストを返します。</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (パス)</td>
<td>この機能は、メモリ内の選択範囲として実行されます。 指定されたパスと一致するすべての項目を表す新しい単純化したリストを返します。 パスは、レコード リスト データ型のデータ ソースの要素の有効なデータ ソース パスとして定義する必要があります。 パス文字列や日付などのデータ要素は、デザイン時間で ER 式ビルダーのエラーを生成する必要があります。</td>
<td>データ ソース (DS) として <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> を入力する場合、<strong>COUNT( ALLITEMS (DS.Value))</strong> は <strong>3</strong> を返します。</td>
</tr>
<tr>
<td>ALLITEMSQUERY (パス)</td>
<td>この機能は、結合された SQL クエリとして実行されます。 指定されたパスと一致するすべての項目を表す新しい単純化したリストを返します。 指定されたパスは、レコード リスト データ型のデータ ソースの要素の有効なデータ ソース パスとして定義する必要があり、少なくとも 1 つの関係を含まなければなりません。 パス文字列や日付などのデータ要素は、デザイン時間で ER 式ビルダーのエラーを生成する必要があります。</td>
<td>モデル マッピングでは、次のデータ ソースを定義します。
<ul>
<li>CustInvoiceTable テーブルを参照する <strong>CustInv</strong> (<strong>テーブルレコード</strong>タイプ)</li> 
<li>式 <strong>FILTER (CustInv、CustInv.InvoiceAccount =&quot;US-001&quot;)</strong>を含む <strong>FilteredInv</strong> (<strong>計算済フィールド</strong>タイプ)</li>
<li><strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong> を含む <strong>JourLines</strong> (<strong>計算済フィールド</strong>タイプ)</li>
</ul>
<p><strong>JourLines</strong> データ ソースを呼び出すモデル マッピングを実行すると、次の SQL ステートメントが実行されます。</p>
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN CUSTINVOICETRANS T3 WHERE...
</td>
</tr>
<tr>
<td>ORDERBY (リスト [, 式 1, 式 2, …])</td>
<td>指定した引数に従って並べ替えられた後、指定されたリストを返します。 これらの引数は、式として定義することができます。</td>
<td><strong>仕入先</strong>を VendTable テーブルを参照する ER データ ソースとしてコンフィギュレーションすると、<strong>ORDERBY (仕入先, 仕入先.'name()')</strong> は昇順の名前で並べ替えられた仕入先のリストを返します。</td>
</tr>
<tr>
<td>REVERSE (リスト)</td>
<td>逆の並べ替え順でリストを返します。</td>
<td><strong>仕入先</strong>を VendTable テーブルを参照する ER データ ソースとしてコンフィギュレーションすると、<strong>REVERSE (ORDERBY (仕入先, 仕入先.'name()')) )</strong> は降順の名前で並べ替えられた仕入先のリストを返します。</td>
</tr>
<tr>
<td>WHERE (リスト, 条件)</td>
<td>指定した条件に従ってフィルター処理された後、指定されたリストを返します。 メモリの一覧には、指定した条件が適用されます。 この方法で、<strong>WHERE</strong> 関数は、<strong>FILTER</strong> 関数とは異なります。</td>
<td><strong>仕入先</strong>を VendTable テーブルを参照する ER データ ソースとしてコンフィギュレーションすると、<strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> は仕入先グループ 40 に属している仕入先のみのリストを返します。</td>
</tr>
<tr>
<td>ENUMERATE (リスト)</td>
<td>指定されたリストの列挙されたレコードから構成される新しいリストを返し、次の要素を公開します。
<ul>
<li>通常のリストとして指定されたリスト レコード (<strong>値 </strong>コンポーネント)</li>
<li>現在のレコード インデックス (<strong>番号 </strong>コンポーネント)</li>
</ul>
</td>
<td>次の図では、<strong>列挙型</strong> データ ソースは、VendTable テーブルを参照する <strong>仕入先</strong> データ ソースの仕入先レコードの列挙型リストとして作成されます。
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>次の図は、形式を示します。 この形式では、XML 形式で出力を生成するために、バインディングが作成されます。 この出力では、個々の仕入先が列挙型ノードとして表示されます。</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>次の図は、設計された形式が実行される際の結果を示します。</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT (リスト)</td>
<td>指定されたリストが空でない場合、そのリストのレコードの数を返します。 それ以外の場合は、<strong>0</strong> (ゼロ) を返します。</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> は、<strong>SPLIT</strong> 関数が 2 つのレコードから構成されるリストを作成するため、<strong>2</strong> を返します。</td>
</tr>
<tr>
<td>LISTOFFIELDS (パス)</td>
<td>次のタイプのうち 1 つの引数から作成されたレコード リストを返します。
<ul>
<li>モデルの列挙</li>
<li>形式列挙</li>
<li>コンテナー</li>
</ul>
<p>作成するリストは、次のフィールドを持つレコードで構成されます。</p>
<ul>
<li>氏名</li>
<li>ラベル</li>
<li>説明</li>
</ul>
実行時に、<strong>ラベル</strong> および <strong>説明</strong> フィールドは、形式の言語設定に基づく値を返します。
</td>
<td>次の図では、列挙はデータ モデルで導入されます。
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>次の図は、これらの詳細について説明しています。</p>
<ul>
<li>モデル列挙はデータ ソースとしてレポートに挿入されます。</li>
<li>ER の式は <strong>LISTOFFIELDS</strong> 関数のパラメーターとしてモデル列挙を使用します。</li>
<li>レコード リスト タイプのデータ ソースは、作成された ER の式を使用してレポートに挿入されます。</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>次の例では、<strong>LISTOFFIELDS</strong> 関数を使用して作成されたレコードのリストの種類のデータ ソースにバインドされている ER 形式要素を示します。</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>次の図は、設計された形式が実行される際の結果を示します。</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] 親ファイルおよびフォルダー形式要素の言語設定に基づいて、ラベルと説明の翻訳文は、ER 形式出力に入力されます。</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (パス、言語)</td>
<td>モデルの列挙、形式列挙、またはコンテナーなど、引数から作成されるレコードの一覧を返します。 作成するリストは、次のフィールドを持つレコードで構成されます。
<ul>
<li>氏名</li>
<li>ラベル</li>
<li>説明</li>
<li>翻訳済み</li>
</ul>
実行時に、<strong>ラベル</strong> および <strong>説明</strong> フィールドは、形式の言語設定と特定の言語に基づく値を返します。 <strong>翻訳済み</strong> フィールドは、<strong>ラベル</strong> フィールドが指定した言語に翻訳されていることを示します。
</td>
<td>たとえば、<strong>計算済フィールド</strong>データ ソース型を使用して、<strong>enumType</strong> データ モデル列挙に対する <strong>enumType_de</strong> および <strong>enumType_deCH</strong> データ ソースをコンフィギュレーションします。
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType、&quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>この場合、この翻訳が使用可能な場合は、スイス ドイツ語の列挙値のラベルを取得する次の式を使用できます。 スイス ドイツ語翻訳を使用できない場合、ラベルはドイツ語になります。</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN (リスト, フィールド名, 区切り記号)</td>
<td>指定されたリストから指定したフィールドの連結された値で構成される文字列を返します。 値は、指定した区切り記号で区切られます。</td>
<td><strong>SPLIT(&quot;abc&quot; , 1)</strong> をデータ ソース (DS) として入力した場合、<strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> は <strong>&quot;a-b-c&quot;</strong> を返します。</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (リスト, 制限値, 制限のソース)</td>
<td>指定されたリストをサブリストの新しいリストに分割し、レコード リストの内容の結果を返します。 <strong>制限値</strong>のパラメーターは、元のリストを分割する制限値を定義します。 <strong>制限のソース</strong>のパラメーターは、合計が増加するステップを定義します。 制限は、制限のソースが定義済み制限を超えると、元のリストの 1 つの項目に適用されません。</td>
<td>次の図は、形式を示します。 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>次の図は、形式に対して使用されているデータ ソースを示します。</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>次の図は、形式が実行される際の結果を示します。 この場合、出力は、商品のフラット リストです。</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>次の図では、1 つのバッチに合計重量が 9 を超えない商品を含める必要がある場合、商品アイテムのリストをバッチに表示するために同じフォーマットが調整されています。</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>次の図は、調整された形式が実行される際の結果を示します。</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] 制限は、制限のソース (重量) の値 (11) が定義済みの制限 (9) を超えるため、元のリストの最後の項目に適用されません。 <strong>WHERE</strong> 関数または対応する形式の要素の <strong>有効</strong> 式を使用して、レポート生成時にサブリストを無視 (スキップ) できます。</blockquote>
</td>
</tr>
<tr>
<td>FILTER (リスト, 条件)</td>
<td>指定した条件に対してフィルター処理するためクエリが変更された後、指定されたリストを返します。 この関数は <strong>WHERE</strong> 関数とは異なります。指定された条件がデータベース レベルで <strong>テーブル レコード</strong> タイプの任意の ER データ ソースに適用されるためです。 テーブルおよび関係を使用して、リストと条件を定義することができます。</td>
<td><strong>仕入先</strong>を VendTable テーブルを参照する ER データ ソースとしてコンフィギュレーションすると、<strong>FILTER(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> は仕入先グループ 40 に属している仕入先のみのリストを返します。 <strong>仕入先</strong>が VendTable テーブルを参照する ER データ ソースとしてコンフィギュレーションされ、<strong>parmVendorBankGroup</strong> が <strong>文字列</strong>データ型の値を返す ER データ ソースとしてコンフィギュレーションされている場合、 <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> が特定の銀行グループに属する仕入先の一覧を返します。</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>論理機能

| 職務 | 説明 | 例 |
|----------|-------------|---------|
| CASE (式, オプション 1, 結果 1 \[, オプション 2, 結果 2\] … \[, 既定の結果\]) | 指定された代替オプションに対して指定された式の値を評価します。 式の値に等しいオプションの結果を返します。 それ以外の場合、既定の結果が指定されている場合は、オプションの既定の結果を返します。 (既定の結果はオプションに続かない最後のパラメータです。) | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "冬", "11", "冬", "12", "冬", "")** は、Finance and Operations セッションの日付が 10 月～ 12 月である場合に **"冬"** という文字列を返します。 それ以外の場合は、空白文字列を返します。 |
| IF (条件, 値 1, 値 2) | 特定の条件が満たされているときに最初に指定された値 1 を返します。 それ以外の場合、2 つ目の指定した値を返します。 値 1 と値 2 がレコードまたはレコード リストの場合、両方のリストが存在するフィールドだけの結果になります。 | **IF (1=2, "条件を満たしている", "条件を満たしていない")** は、**"条件を満たしていない"** の文字列を返します。 |
| NOT (条件) | 指定された条件の取消論理値を返します。 | **NOT (TRUE)** は **FALSE** を返します。 |
| AND (条件 1\[, 条件 2, ...\]) | *すべて*の指定された条件が真の場合、**TRUE** を返します。 それ以外の場合は、**FALSE** を返します。 | **AND (1=1, "a"="a")** は、**TRUE** を返します。 **AND (1=2, "a"="a")** は、**FALSE** を返します。 |
| OR (条件 1\[, 条件 2, ...\]) | *すべて*の指定された条件が偽の場合、**FALSE** を返します。 *いずれか*の指定された条件が真の場合、**TRUE** を返します。 | **OR (1=2, "a"="a")** は、**TRUE** を返します。 |
| VALUEIN (入力、リスト、項目式のリスト) | 指定された入力が、指定されたリスト内の項目の値と一致するかどうかを決定します。 指定した入力が、少なくとも 1 つのレコードの指定された式を実行した結果と一致する場合は、**TRUE** を返します。 それ以外の場合は、**FALSE** を返します。 **入力**パラメーターは、データ ソース要素のパスを表します。 この要素の値は一致します。 **リスト**パラメーターは、レコード リスト タイプのデータ ソース要素のパスを、式を含むレコードの一覧として表します。 この要素の値は、指定された入力と比較されます。 **項目式のリスト**引数は、照合に使用されるべき指定されたリストの 1 つのフィールドを指し示すか、そのフィールドを含む式を表します。 | 例については、次のセクション [例: VALUEIN (入力、リスト、項目式のリスト)](#examples-valuein-input-list-list-item-expression)を参照してください。 |

#### <a name="examples-valuein-input-list-list-item-expression"></a>例: VALUEIN (入力、リスト、項目式のリスト)
一般に、**VALUEIN** 関数は一連の **OR** 条件に変換されます。

(input = list.item1.value) OR (input = list.item2.value) OR …

##### <a name="example-1"></a>例 1
モデル マッピングに次のデータ ソースを定義します:**リスト** (**計算済フィールド**タイプ)。 このデータ ソースには、式 **SPLIT ("a,b,c", ",")** が含まれています。

**VALUEIN ("B", List, List.Value)** 式としてコンフィギュレーションされたデータ ソースが呼び出されると、**TRUE** を返します。 この場合、**VALUEIN** 関数は次の一連の条件に変換されます:

**("B" = "b")** が **TRUE** と等しい場合、**(("B" = "a") or ("B" = "b") or ("B" = "c"))**

**VALUEIN ("B", List, LEFT(List.Value, 0))** 式としてコンフィギュレーションされたデータ ソースが呼び出されると、**FALSE** を返します。 この場合、**VALUEIN** 関数は次の条件に変換されます:

**TRUE** と等しくない **("B" = "")**

このような条件のテキストの文字数の上限は 32,768 文字であることに注意してください。 したがって、実行時に制限を超える可能性があるデータ ソースを作成しないでください。 制限を超過した場合は、アプリケーションは実行を停止し、例外がスローされます。 たとえば、この状況は、データ ソースが **WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)** としてコンフィギュレーションされ、**List1** および **List2** リストに大量のレコードが含まれているときに生じます。

場合によっては、**VALUEIN** 関数は **EXISTS JOIN** オペレーターを使用することでデータベース ステートメントに変換されます。 この動作は、**FILTER** 関数が使用され、次の条件が満たされているときに発生します。

- **ASK FOR QUERY** オプションは、レコードのリストを参照する **VALUEIN** 関数のデータ ソースに対してオフになっています。 (このデータ ソースには実行時に適用される追加の条件はありません。)
- 入れ子になった式は、レコードのリストを参照する **VALUEIN** 関数のデータ ソース用にコンフィギュレーションされません。
- **VALUEIN** 関数のリスト品目は、指定されたデータ ソースのフィールド (式またはメソッドではない) を参照します。

この例の前半で説明した **WHERE** 関数の代わりにこのオプションを使用することを検討してください。

##### <a name="example-2"></a>例 2

モデル マッピングでは、次のデータ ソースを定義します。

- イントラスタット テーブルを参照する **In** (**テーブル レコード**タイプ)
- IntrastatPort テーブルを参照する **ポート** (**テーブル レコード**タイプ)

**FILTER (In, VALUEIN(In.Port, Port, Port.PortId)** 式としてコンフィギュレーションされたデータソースが呼び出されると、次の SQL ステートメントが生成され、イントラスタット テーブルのフィルターされたレコードを返します:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

**dataAreaId** フィールドの場合、**IN** 演算子を使用して最終的な SQL ステートメントが生成されます。

##### <a name="example-3"></a>例 3

モデル マッピングでは、次のデータ ソースを定義します。

- 式 **SPLIT ("DEMF,GBSI,USMF", ",")** を含む **Le** (**計算済フィールド**タイプ)
- **会社間**オプションがオンになっていて、イントラスタット テーブルを参照する **In** (**テーブル レコード**タイプ)

**FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)** 式としてコンフィギュレーションされたデータソースが呼び出されると、最終的な SQL ステートメントには次の条件が含まれています:

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>算術関数

| 職務 | 説明 | 例 |
|----------|-------------|---------|
| ABS (数値) | 指定された数の絶対値を返します。 (つまり、符号のない数値を返します。) | **ABS (-1)** は、**1** を返します。 |
| POWER (数値, 累乗) | 指定された正の数に指定された累乗をした結果を返します。 | **POWER (10, 2)** は、**100** を返します。 |
| NUMBERVALUE (文字列、小数点記号、桁区切り記号) | 指定された文字列を数字に変換します。 指定した小数点記号は、整数と小数点以下の数の間で使用されます。 指定した桁区切り記号は千の位の区切り記号として使用されます。 | **NUMBERVALUE("1 234,56", ",", " ")** は、**1234.56** の値を返します。 |
| VALUE (文字列) | 指定された文字列を数字に変換します。 コンマとドット (.) が小数点の区切り記号とみなされ、先頭のハイフン (-) は負の記号として使用されます。 他の数値以外の文字が指定された文字列に含まれている場合、例外をスローします。 | **VALUE ("1 234,56")** は例外をスローします。 |
| ROUND (数値, 小数点以下の桁数) | 指定された小数点以下の桁数に丸めてから、指定された数値を返します。<ul><li>**小数点以下**パラメーターの値が 0 (ゼロ) より大きい場合、指定された数字は小数点以下の桁数で四捨五入されます。</li><li>**小数点以下**パラメーターの値が **0** (ゼロ) の場合、指定された数字は最も近い整数に四捨五入されます。</li><li>**小数点以下**パラメーターの値が 0 (ゼロ) より小さい場合、指定された数字は小数点より左で四捨五入されます。</li></ul> | **ROUND (1200.767, 2)** は、小数点第 2 位で四捨五入され、**1200.77** を返します。 **ROUND (1200.767, -3)** は、1,000 の最も近い倍数に四捨五入され、**1000** を返します。 |
| ROUNDDOWN (数値, 小数点以下の桁数) | 指定された小数点以下の桁数に丸めてから、指定された数値を返します。<blockquote>[!NOTE] この関数は、**ROUND** のように機能しますが、常に指定した数字を (ゼロ方向に) 切り捨てます。</blockquote> | **ROUNDDOWN (1200.767, 2)** は、小数点第 2 位で切り捨てられ、**1200.76** を返します。 **ROUNDDOWN (1700.767, -3)** は、1,000 の最も近い倍数に切り捨てられ、**1000** を返します。 |
| ROUNDUP (数値, 小数点以下の桁数) | 指定された小数点以下の桁数に丸めてから、指定された数値を返します。<blockquote>[!NOTE] この関数は、**ROUND** のように機能しますが、常に指定した数字を (ゼロとは逆方向に) 切り上げます。</blockquote> | **ROUNDUP (1200.763, 2)** は、小数点第 2 位で切り上げられ、**1200.77** を返します。 **ROUNDUP (1200.767, -3)** は、1,000 の最も近い倍数に切り上げられ、**2000** を返します。 |

### <a name="data-conversion-functions"></a>データ変換機能

| 職務 | 説明 | 例 |
|----------|-------------|---------|
| VALUE (文字列) | 指定された文字列を数字に変換します。 コンマとドット (.) が小数点の区切り記号とみなされ、先頭のハイフン (-) は負の記号として使用されます。 他の数値以外の文字が指定された文字列に含まれている場合、例外をスローします。 | **VALUE ("1 234,56")** は例外をスローします。 |
| NUMBERVALUE (文字列、小数点記号、桁区切り記号) | 指定された文字列を数字に変換します。 指定した小数点記号は、整数と小数点以下の数の間で使用されます。 指定した桁区切り記号は千の位の区切り記号として使用されます。 | **NUMBERVALUE("1 234,56", ",", " ")** は、**1234.56** を返します。 |
| INTVALUE (文字列) | 指定された文字列の整数表現を返します。 任意の小数点以下の桁数が切り捨てられます。 | **INTVALUE (「100.77」)** は **100** を返します。 |
| INTVALUE (番号) | 指定された数の整数表現を返します。 任意の小数点以下の桁数が切り捨てられます。 | **INTVALUE (-100.77)** は **-100** を返します。 |
| INT64VALUE (文字列) | 指定した文字列の int64 表現を返します。 任意の小数点以下の桁数が切り捨てられます。 | **INT64VALUE (「22565422744」)** は、**22565422744** を返します。 |
| INT64VALUE (数値) | 指定の文字列の int64 表現を返します。 任意の小数点以下の桁数が切り捨てられます。 | **INT64VALUE (22565422744.00)** は、**22565422744** を返します。 |

### <a name="record-functions"></a>レコード機能

| 職務 | 説明 | 例 |
|----------|-------------|---------|
| NULLCONTAINER (リスト) | 指定されたレコード リストまたはレコードと同じ構造を持つ **null** レコードを返します。<blockquote>[!NOTE] この関数は廃止されています。 代わりに **EMPTYRECORD** を使用します。</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** は、**SPLIT** 関数で返ってきたリストと同じ構造を持つ新しい空のレコードを返します。 |
| EMPTYRECORD (レコード) | 指定されたレコード リストまたはレコードと同じ構造を持つ **null** レコードを返します。<blockquote>[!NOTE] **null** レコードは、すべてのフィールドが空の値があるレコードです。 空の値が数字の場合は **0** (ゼロ)、文字列の場合、空の文字列などです。</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** は、**SPLIT** 関数で返ってきたリストと同じ構造を持つ新しい空のレコードを返します。 |

### <a name="text-functions"></a>テキスト関数

<table>
<thead>
<tr>
<th>機能</th>
<th>説明</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER (文字列)</td>
<td>大文字に変換してから、指定された文字列を返します。</td>
<td><strong>UPPER(&quot;Sample&quot;)</strong> は、<strong>&quot;SAMPLE&quot;</strong> を返します。</td>
</tr>
<tr>
<td>LOWER (文字列)</td>
<td>小文字に変換してから、指定された文字列を返します。</td>
<td><strong>LOWER (&quot;Sample&quot;)</strong> は、<strong>&quot;sample&quot;</strong> を返します。</td>
</tr>
<tr>
<td>LEFT (文字列, 文字数)</td>
<td>指定された文字列の先頭から指定された数の文字を返します。</td>
<td><strong>LEFT (&quot;Sample&quot;, 3)</strong> は、<strong>&quot;Sam&quot;</strong> を返します。</td>
</tr>
<tr>
<td>RIGHT (文字列, 文字数)</td>
<td>指定された文字列の末尾から指定された数の文字を返します。</td>
<td><strong>RIGHT (&quot;Sample&quot;, 3)</strong> は、<strong>&quot;ple&quot;</strong> を返します。</td>
</tr>
<tr>
<td>MID (文字列, 開始位置, 文字数)</td>
<td>指定された文字列の指定された位置から始まる指定された数の文字を返します。</td>
<td><strong>MID (&quot;Sample&quot;, 2, 3)</strong> は、<strong>&quot;amp&quot;</strong> を返します。</td>
</tr>
<tr>
<td>LEN (文字列)</td>
<td>指定された文字列の文字数を返します。</td>
<td><strong>LEN (&quot;Sample&quot;)</strong> は、<strong>6</strong> を返します。</td>
</tr>
<tr>
<td>CHAR (数値)</td>
<td>指定された Unicode 番号で参照される文字列を返します。</td>
<td><strong>CHAR (255)</strong> は、<strong>&quot;ÿ&quot;</strong> を返します。
<blockquote>[!NOTE] この機能を返す文字列は、親ファイル形式の要素で選択したエンコードによって異なります。 サポートされているエンコードの一覧については、<a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">クラスをエンコード</a> で参照できます。</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE (文字列 1 [, 文字列 2, …])</td>
<td>指定されたすべての文字列を 1 つの文字列に結合してから、そのすべての文字列を返します。</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> は、<strong>&quot;abcdef&quot;</strong> を返します。
<blockquote>[!NOTE] 式 <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> でも <strong>&quot;abcdef&quot;</strong> を返します。</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE (文字列, パターン, 置換)</td>
<td>指定されたパターン文字列でのすべての文字の発生が、指定された置換文字列の対応する位置にある文字で置換された後に、指定された文字列を返します。</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> は、パターン <strong>&quot;cd&quot;</strong> を文字列 <strong>&quot;GH&quot;</strong> に置換して、<strong>&quot;abGHef&quot;</strong> を返します。</td>
</tr>
<tr>
<td>REPLACE (文字列, パターン, 置換, 正規表現フラグ)</td>
<td>指定された<strong>正規表現フラグ</strong>パラメーターが <strong>true</strong> の場合、この関数の<strong>パターン</strong>引数として指定される正規表現を適用して変更した後に、指定された文字列を返します。 この式は、置換する必要のある文字列を検索するために使用されます。 指定された<strong>置換</strong>引数の文字は、見つかった文字を置換するために使用されます。 指定された<strong>正規表現フラグ</strong>パラメーターが <strong>false</strong> である場合、この関数は <strong>TRANSLATE</strong> のように機能します。</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> は、すべての数値以外の記号を削除する正規表現を適用し、<strong>&quot;19234564971&quot;</strong> を返します。 <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> は、パターン <strong>&quot;cd&quot;</strong> を文字列 <strong>&quot;GH&quot;</strong> に置換して、<strong>&quot;abGHef&quot;</strong> を返します。</td>
</tr>
<tr>
<td>TEXT (入力)</td>
<td>現在の Finance and Operations インスタンスのサーバーのロケール設定に従って書式設定されるテキスト文字列に変換した後に、指定された入力を返します。 <strong>実数</strong>型の値では、文字列変換が小数点第 2 位に制限されます。</td>
<td>Finance and Operations インスタンスのサーバーのロケールが <strong>EN-US</strong> で定義されている場合、<strong>TEXT (NOW ())</strong> は現在の Finance and Operations セッションの日付 2015 年 12 月 17 日 をテキスト文字列 <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong> として返します。 <strong>TEXT (1/3)</strong> は、<strong>&quot;0.33&quot;</strong> を返します。</td>
</tr>
<tr>
<td>FORMAT (文字列 1, 文字列 2[, 文字列 3, …])</td>
<td>すべての <strong>%N</strong> を <em>n</em> 番目の引数に置き換えて書式設定した後に、指定された文字列を返します。 引数は文字列です。 パラメーターに引数が指定されない場合は、文字列内では <strong>&quot;%N&quot;</strong> として返されます。 <strong>実数</strong>型の値では、文字列変換が小数点第 2 位に制限されます。</td>
<td>この図では、<strong>PaymentModel</strong> データ ソースは <strong>顧客</strong>コンポーネント経由で顧客のリスト、<strong>ProcessingDate</strong> フィールド経由で処理日の値を返します。
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>選択した顧客の電子ファイルを生成するよう設計されている ER 形式では、<strong>PaymentModel</strong> がデータ ソースとして選択され、プロセス フローを制御します。 選択した顧客がレポートが処理される日付に停止されている場合、例外がユーザーに通知してスローされます。 このタイプの処理制御のために設計された式は、次のリソースを使用できます。</p>
<ul>
<li>次のテキストを含む Finance and Operations ラベル SYS70894:
<ul>
<li><strong>EN-US 言語の場合:</strong> &quot;Nothing to print&quot;</li>
<li><strong>DE 言語の場合:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>次のテキストを含む Finance and Operations ラベル SYS18389:
<ul>
<li><strong>EN-US 言語の場合:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>DE 言語の場合:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>設計できる式を次に示します。</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>レポートが 2015 年 12 月 17 日に <strong>EN-US</strong> カルチャおよび <strong>EN-US</strong> 言語で <strong>Litware Retail</strong> の顧客に対して処理される場合、この式は例外メッセージとしてユーザーに示すことができる次のテキストを返します:</p>
<p>&quot;印刷対象なし。 顧客の Litware Retail は 2015 年 12 月 17 日に停止されます。&quot;</p>
<p>同じレポートが 2015 年 12 月 17 日に <strong>DE</strong> カルチャおよび <strong>DE</strong> 言語で <strong>Litware Retail</strong> の顧客に対して処理される場合、この式は別の日付形式を使用する次のテキストを返します。</p>
<p>&quot;Nichts zu drucken。 顧客の Litware Retail は 2015 年 12 月 17 日に停止されます。&quot;</p>
<blockquote>[!NOTE] 次の構文は ER の式でラベルに適用されます。
<ul>
<li><strong>Finance and Operations リソースのラベルの場合: </strong><strong>@&quot;X&quot;</strong>、<strong>X</strong> はアプリケーション オブジェクト ツリー (AOT) のラベル ID です</li>
<li><strong>ER コンフィギュレーションに存在するラベルの場合: </strong><strong>@&quot;GER_LABEL:X&quot;</strong>、<strong>X</strong> は ER コンフィギュレーションのラベル ID です</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT (数値, 形式)</td>
<td>指定された形式で指定された数値の文字列形式を返します。 (サポートされている形式の詳細については、「<a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">標準</a>」と「<a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">カスタム</a>」を参照してください)。この関数が実行されるコンテキストが、数値の書式設定に使用されるカルチャを決めます。</td>
<td>EN-US カルチャの場合、<strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> は <strong>&quot;45.00 %&quot;</strong> を返します。 <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> は <strong>&quot;10&quot;</strong> を返します。</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (数, 言語, 通貨, 通貨名を印刷フラグ, 小数点)</td>
<td>特定の言語で綴られた (文字列に変換された) 後に、指定の数字を返します。 言語コードはオプションです。 空の文字列として定義されている場合、実行中のコンテキストの言語コードが使用されます。 (実行中のコンテキストの言語コードは生成するフォルダーまたはファイルを定義します)。通貨コードは、オプションもあります。 空の文字列として定義されている場合、会社基本通貨が使用されます。
<blockquote>[!NOTE] <strong>通貨名を印刷 フラグ</strong>および<strong>小数点パラメーター</strong>は、次の言語コードに対してのみ分析されることに注意してください: <strong>CS</strong>、<strong>ET</strong>、<strong>HU</strong>、<strong>LT</strong>、<strong>LV</strong>、<strong>PL</strong>、<strong>RU</strong>。 また、<strong>通貨名を印刷 フラグ</strong> パラメーターは、通貨名の語形変化をサポートする国または地域のコンテキストを持つ Finance and Operations の会社に対してのみ分析されることに注意してください。</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> は、<strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong> を返します。 <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> は、 <strong>&quot;Sto dwadzieścia&quot;</strong> を返します。 <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> は、<strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>を返します。</td>
</tr>
<tr>
<td>PADLEFT (文字列, 長さ, パディング文字)</td>
<td>指定の文字列から始まる指定の文字でパディングされた指定の長さの文字列を返します。</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> は、テキスト文字列 <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong> を返します。</td>
</tr>
<tr>
<td>TRIM (文字列)</td>
<td>先頭と末尾のスペースを切り捨ててから指定されたテキスト文字列を返し、その後単語間の複数のスペースが削除されます。</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;サンプル&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;テキスト&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong>は <strong>&quot;サンプル テキスト&quot;</strong> を返します。</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (列挙データ ソースのパス、列挙値のラベル テキスト)</td>
<td>この列挙ラベルの指定されたテキストに基づいて指定された列挙データ ソースの値を返します。</td>
<td>次の図では、<strong>ReportDirection</strong>の列挙はデータ モデルで導入されます。 列挙値のラベルが定義されていることに注意してください。
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>次の図は、これらの詳細について説明しています。</p>
<ul>
<li><strong>ReportDirection</strong> モデル列挙は、データ ソース <strong>$Direction</strong> としてレポートに挿入されます。</li>
<li>ER の式 <strong>$IsArrivals</strong> は、関数のパラメーターとしてモデル列挙を使用するように設計されています。 この式の値は <strong>TRUE</strong> です。</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (入力)</td>
<td><strong>文字列</strong>データ型の指定された入力を、<strong>GUID</strong>データ型のデータ項目に変換します。<blockquote>[!NOTE] 逆方向に変換を行うには (つまり、<strong>GUID</strong> データ型の指定された入力を<strong>文字列</strong>データ型のデータ項目に変換するには)、<strong>TEXT()</strong> 関数を使用します。</blockquote></td>
<td>モデル マッピングでは、次のデータ ソースを定義します。
<ul>
<li>式 <strong>GUIDVALUE (&quot;AF5CCDAC-F728-4609-8C8B-A4B30B0C0AA0&quot;)</strong>を含む <strong>myID</strong> (<strong>計算済フィールド</strong>タイプ)</li>
<li>UserInfo テーブルを参照する <strong>Users</strong> (<strong>テーブルレコード</strong>タイプ)</li>
</ul>
これらのデータ ソースが定義されている場合、次のような式を使用することができます。<strong>GUID</strong> データ型の <strong>objectId</strong> フィールドによって UserInfo テーブルをフィルター処理する <strong>FILTER (Users, Users.objectId = myID)</strong>
</td>
</tr>
<tr>
<td>JSONVALUE (ID、パス)</td>
<td>指定した ID に基づくスカラー値を抽出するための指定したパスでアクセスする JavaScript Object Notation (JSON) 形式で、データを解析します。</td>
<td>データ ソース<strong>$JsonField</strong> は JSON 形式の次のデータを含みます。<strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>。 このデータ ソースでは、</strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong>は、<strong>文字列</strong>データ型の値 <strong>7.3.1234.1</strong> を返します。</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>データ変換機能

| 職務 | 説明 | 例 |
|----------|-------------|---------|
| TEXT (入力) | 現在の Finance and Operations インスタンスのサーバーのロケール設定に従って書式設定されるテキスト文字列に変換した後に、指定された入力を返します。 **実数**型の値では、文字列変換が小数点第 2 位に制限されます。 | Finance and Operations インスタンスのサーバーのロケールが **EN-US** で定義されている場合、**TEXT (NOW ())** は現在の Finance and Operations セッションの日付 2015 年 12 月 17 日 をテキスト文字列 **"12/17/2015 07:59:23 AM"** として返します。 **TEXT (1/3)** は、**"0.33"** を返します。 |
| QRCODE (文字列) | 指定された文字列の Quick Response Code (QR コード) 画像を Base64 バイナリ形式で返します。 | **QRCODE (「サンプル テキスト」)** は **U2FtcGxlIHRleHQ=** を返します。 |

### <a name="data-collection-functions"></a>データ収集機能

| 職務 | 説明 | 例 |
|----------|-------------|---------|
| FORMATELEMENTNAME () | 現在の形式の要素の名前を返します。 現在のファイルの **出力の詳細を収集** フラグを無効にすると空の文字列が返されます。 | これらの関数の用途の詳細については、**IT サービス/ソリューション コンポーネントの取得/開発** 業務プロセスの一部である **ER 棚卸および集計のために出力された形式の使用**タスク ガイドを参照してください。 |
| SUMIFS (集計のためのキー文字列, 基準範囲 1 の文字列, 基準値 1 の文字列 \[, 基準範囲 2 の文字列, 基準値 2 の文字列, …\]) | 形式が実行され、指定された条件 (範囲と値のペア) を満たすときに XML ノード (キーとして定義された名前を持つ) に対して収集された値の合計を返します。 **出力の詳細を収集** フラグを無効にすると **0** (ゼロ) が返されます。 | |
| SUMIF (集計のためのキー文字列, 基準範囲の文字列, 基準値の文字列) | 形式が実行され、指定された条件 (範囲と値) を満たすときに XML ノード (キーとして定義された名前を持つ) に対して収集された値の合計を返します。 **出力の詳細を収集** フラグを無効にすると **0** (ゼロ) が返されます。 | |
| COUNTIFS (基準範囲 1 の文字列, 基準値 1 の文字列 \[, 基準範囲 2 の文字列, 基準値 2 の文字列, …\]) | 形式が実行され、指定された条件 (範囲と値のペア) を満たすときに収集された XML ノードの数を返します。 **出力の詳細を収集** フラグを無効にすると **0** (ゼロ) が返されます。 | |
| COUNTIF (基準範囲の文字列, 基準値の文字列) | 形式が実行され、指定された条件 (範囲と値) を満たすときに収集された XML ノードの数を返します。 現在のファイルの **出力の詳細を収集** フラグを無効にすると **0** (zero) が返されます。 | |
| COLLECTEDLIST (基準範囲 1 の文字列, 基準値 1 の文字列 \[, 基準範囲 2 の文字列, 基準値 2 の文字列, …\]) | 形式が実行され、指定された条件 (範囲と値) を満たすときに XML ノードに対して収集された値のリストを返します。 現在のファイルの**出力の詳細を収集**フラグを無効にすると空のリストが返されます。 | |

### <a name="other-business-domainspecific-functions"></a>その他 (ビジネス ドメインの特定の) 関数

| 職務 | 説明 | 例 |
|----------|-------------|---------|
| CONVERTCURRENCY (数量, 換算元の通貨, 換算先の通貨, 日付, 会社) | 特定の日付で指定された Finance and Operations の会社の設定を使用して、指定された換算元の通貨から指定された換算先の通貨に指定された金額を変換します。 | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** は、DEMF 会社の設定に基づいて現在のセッションの日付の 1 ユーロに相当する額を米ドルで返します。 |
| ROUNDAMOUNT (数値, 小数点以下の桁数, 丸めルール) | 指定された丸めルールに従って、指定された数量の小数点以下の桁数を丸めます。<blockquote>[!NOTE] 丸めルールは Finance and Operations の **RoundOffType** 列挙の値として指定する必要があります。</blockquote> | **model.RoundOff** パラメーターが **切り捨て** に設定されている場合、 **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** は、値 **1000.78** を返します。 **model.RoundOff** パラメータが**標準**または**切り上げ**に設定されている場合、**ROUNDAMOUNT (1000.787, 2, model.RoundOff)** は、値 **1000.79** を返します。 |
| CURCredRef (数字) | 指定された請求書番号の数字に基づいて、送金受取人参照情報を返します。 | **CURCredRef ("VEND-200002")** は、**"2200002"** を返します。 |
| MOD\_97 (数字) | 指定された請求書番号の数字に基づいて、MOD97 式として送金受取人参照情報を返します。 | **MOD\_97 ("VEND-200002")** は、**"20000285"** を返します。 |
| ISOCredRef (数字) | 指定された請求書番号の数字とアルファベット記号に基づいて、国際標準化機構 (ISO) 送金受取人参照情報を返します。<blockquote>[!NOTE] ISO 準拠ではないアルファベットの記号を削除するには、入力パラメータを変換してからこの関数に渡す必要があります。</blockquote> | **ISOCredRef ("VEND-200002")** は、**"RF23VEND-200002"** を返します。 |
| CN\_GBT\_AdditionalDimensionID (文字列, 番号) | 指定した追加の財務分析コード ID を取得します。 **文字列**パラメーターでは、分析コードはコンマで区切られた ID としてこの文字列に表されます。 **番号**パラメーターは、文字列で要求された分析コードの順序コードを定義します。 | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** は、**CC** を返します。 |
| GetCurrentCompany () | 現在ユーザーがサインインしている法人 (会社) のコードのテキスト表現を返します。 | **GETCURRENTCOMPANY ()** は、Finance and Operations の会社 **Contoso Entertainment System USA** にサインインしているユーザーに対する **USMF** を返します。 |
| CH\_BANK\_MOD\_10 (数値) | 指定された請求書番号の数字に基づいて、MOD10 式として送金受取人参照情報を返します。 | **CH\_BANK\_MOD\_10 ("VEND-200002")** は、**3** を返します。 |
| FA\_SUM (固定資産コード, 価値モデル コード, 開始日, 終了日) | 指定した期間の固定資産額の準備済データ コンテナーを返します。 | **FA\_SUM (「COMP-000001」、「Current」、Date1、Date2)** は、**Date1** から **Date2** の期間中で、価値モデル **現行** の固定資産 **COMP-000001** の準備済データ コンテナーを返します。 |
| FA\_BALANCE (固定資産コード, 価値モデル コード, レポート年度, 報告日) | 固定資産残高の準備済データ コンテナーを返します。 レポート年度は、Finance and Operations の列挙の値 **AssetYear** として指定される必要があります。 | **FA\_SUM (「COMP-000001」、「Current」、AxEnumAssetYear.ThisYear、SESSIONTODAY ())** は、現在の Finance and Operations セッションの日付で、値モデル **現行** である固定資産 **COMP-000001** の残高の準備済データ コンテナーを返します。 |
| TABLENAME2ID (文字列) | 指定されたテーブル名のテーブル ID の整数表現を返します。 | **TABLENAME2ID (「イントラスタット」)** は **1510** を返します。 |
| ISVALIDCHARACTERISO7064 (文字列) | 指定された文字列が有効な国際銀行番号 (IBAN) を表す場合、ブール値 **TRUE** を返します。 それ以外の場合、ブール値 **FALSE** を返します。 | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** は **TRUE** を返します。 **ISVALIDCHARACTERISO7064 ("AT61")** は **FALSE** を返します。 |
| NUMSEQVALUE (番号順序コード、スコープ、スコープ ID) | 指定された番号順序コード、スコープ、およびスコープ ID に基づいて、番号順序の新しく生成された値を返します。 スコープは、**ERExpressionNumberSequenceScopeType** 列挙 (**共有**、**法人**、または**会社**) の値として指定する必要があります。 **共有**スコープでは、スコープ ID として空の文字列を指定します。 **会社**および**法人**スコープでは、会社コードとスコープ ID を指定します。 **会社**および**法人**スコープでは、スコープ ID として空の文字列を指定した場合、現在の会社コードを使用します。 | モデル マッピングでは、次のデータ ソースを定義します。<ul><li>**ERExpressionNumberSequenceScopeType** 列挙を参照する **enumScope** (**Dynamics 365 for Operations 列挙**タイプ)</li><li>式 **NUMSEQVALUE ("Gene\_1", enumScope.Company, "")** を含む **NumSeq** (**計算済フィールド**タイプ)</li></ul>**NumSeq** データ ソースが呼び出されると、ER 形式が実行されているコンテキストを提供する会社用にコンフィギュレーションされた **Gene\_1** 番号順序の新しく生成された値を返します。 |
| NUMSEQVALUE (番号順序コード) | 指定された番号順序、**会社**スコープ、および (スコープIDとして) ER 形式が実行されているコンテキストを提供する会社のコードに基づいて、番号順序の新しく生成された値を返します。 | モデル マッピングに次のデータ ソースを定義します: **NumSeq** (**計算済フィールド**タイプ)。 このデータ ソースには、式 **NUMSEQVALUE ("Gene\_1")** が含まれています。 **NumSeq** データ ソースが呼び出されると、ER 形式が実行されているコンテキストを提供する会社用にコンフィギュレーションされた **Gene\_1** 番号順序の新しく生成された値を返します。 |
| NUMSEQVALUE (番号順序レコード ID) | 指定された番号順序レコード ID に基づいて、番号順序の新しく生成された値を返します。 | モデル マッピングでは、次のデータ ソースを定義します。<ul><li>LedgerParameters テーブルを参照する **LedgerParms** (**テーブル**タイプ)</li><li>式 **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)** を含む **NumSeq** (**計算済フィールド**タイプ)</li></ul>**NumSeq** データ ソースが呼び出されると、ER 形式が実行されているコンテキストを提供する会社用に一般会計パラメーターでコンフィギュレーションされた、番号順序の新しく生成された値を返します。 この番号順序は、仕訳帳を一意に識別し、トランザクションをリンクするバッチ番号として機能します。 |

### <a name="functions-list-extension"></a>関数の一覧の拡張

ER では ER の式で使用される関数の一覧を拡張できます。 これにはエンジニアリングの実績が要求されます。 詳細については、「[電子申告関数の一覧の拡張](general-electronic-reporting-formulas-list-extension.md)」を参照してください。

## <a name="additional-resources"></a>その他のリソース

- [電子申告の概要](general-electronic-reporting.md)
- [電子申告 (ER) 関数の一覧の拡張](general-electronic-reporting-formulas-list-extension.md)

