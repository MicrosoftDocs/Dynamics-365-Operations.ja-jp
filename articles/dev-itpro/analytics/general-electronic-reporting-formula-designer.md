---
title: "電子申告のフォーミュラ デザイナー"
description: "このトピックでは、電子申告 (ER) でのフォーミュラ デザイナーの使用方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 58bef33642d83def841eaa8334ea6f942063e0b3
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="formula-designer-in-electronic-reporting"></a>電子申告のフォーミュラ デザイナー

[!include[banner](../includes/banner.md)]


このトピックでは、電子申告 (ER) でのフォーミュラ デザイナーの使用方法を説明します。 ER の特定の電子ドキュメントの形式を設計する場合、データ変換に Microsoft Excel のような式を使用して、そのドキュメントのフルフィルメントおよび書式設定の要件を満たすことができます。 テキスト、日時、算術、論理、情報、データ型変換、およびその他 (ビジネス ドメインの特定の関数) といったさまざまなタイプの関数がサポートされています。

<a name="formula-designer-overview"></a>フォーミュラ デザイナーの概要
-------------------------

電子申告 (ER) はフォーミュラ デザイナーをサポートします。 したがって、設計時に次のタスクに使用できる式を実行時にコンフィギュレーションできます。

-   ER フォーマットのデータ ソースとして設計された ER データ モデルに設定する必要のある Microsoft Dynamics 365 for Finance and Operations データベースから受け取るデータの変換 (フィルタ処理、グループ化、およびデータ型の変換など)。
-   レイアウトと特定の ER 形式の条件 (要求された言語、カルチャ、エンコードなど) に従って生成される電子ドキュメントに送信するデータの書式設定。
-   電子ドキュメント生成プロセス (処理データに応じた形式の特定要素出力の有効化または無効化、ドキュメント作成の中断、エンド ユーザーへのスロー メッセージなど) の制御。

フォーミュラ デザイナーのページは次のいずれかを行うと開くことができます。

-   データ モデルのコンポーネントへのデータ ソース項目のバインド。
-   形式コンポーネントへのデータ ソース項目のバインド。
-   データ ソースの一部としての計算済フィールドのメンテナンス完了。
-   ユーザー入力パラメーターの表示条件の定義。
-   形式の変換の設計。
-   形式のコンポーネントに有効にする条件の定義。
-   形式のファイル コンポーネントに対するファイル名の定義。
-   プロセス制御検証の条件の定義。
-   プロセス制御検証のメッセージ テキストの定義。

## <a name="designing-er-formulas"></a>ER フォーミュラ デザイナー
### <a name="data-binding"></a>データ バインディング

ER フォーミュラ デザイナーは、実行時にデータ消費者に反映できるよう、データ ソースから受信されたデータを変換する式を定義するのに使用できます。

-   Finance and Operations データ ソースとランタイム パラメーターから ER データ モデルへ。
-   ER データ モデルから ER 形式へ。
-   Finance and Operations データ ソースとランタイム パラメーターから ER 形式へ。

次の図は、このタイプの式の設計を示しています。 この例では、式は、Finance and Operations [**イントラスタット**] テーブルの [**Intrastat.AmountMST**] フィールドの値を返し、その値は小数点以下 2 桁に丸められます。 [![picture-expression-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) 次の図は、このタイプの式をどのように使用できるかを示しています。 この例では、設計された式の結果が、[**税申告モデル**] データ モデルの [**Transaction.InvoicedAmount**] コンポーネントに反映されます。 [![picture-expression-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) 実行時、設計された式 **ROUND (Intrastat.AmountMST, 2)** が、**イントラスタット** テーブルの各レコードの [**AmountMST**] フィールドの値を小数点以下 2 桁に丸め、その丸めた値を**税申告**データ モデルの [**Transaction.InvoicedAmount**] コンポーネントに反映します。

### <a name="data-formatting"></a>データの書式設定

ER フォーミュラ デザイナーは、電子ドキュメント生成の一部として送信できるよう、データ ソースから受信されたデータを書式設定する式を定義するのに使用できます。 形式に再利用する必要のある一般的なルールとして適用すべき形式がある場合、書式設定の式が含まれる名前付き変換としてその書式設定を書式設定のコンフィギュレーションで一度導入できます。 この名前付き変換は、作成した式に従って出力を書式設定する必要がある多くの形式コンポーネントに後でリンクできます。 次の図は、このタイプの変換の設計を示しています。 この例では、**TrimmedString** 変換は、**文字列** データ型の受信データを使用し、文字列データを返す際に先頭および末尾にあるスペースを切り詰めます。 [![picture-transformation-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) 次の図は、このタイプの変換を使用できる方法を示しています。 この例では、実行時にテキストを電子ドキュメント生成への出力として送信する複数の形式コンポーネントは、名前で **TrimmedString** 変換を参照します。 [![picture-transformation-usage](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) 形式コンポーネントが **TrimmedString** 変換 (たとえば、前の図の **partyName** コンポーネント) を参照する場合、生成ドキュメントへの出力としてテキストを送信します。 テキストには、先頭および末尾にあるスペースは含まれません。 個別に適用する必要のある形式の場合、特定形式コンポーネントのバインディングの個別の式として導入できます。 次の図は、このタイプの式を示しています。 この例では、**partyType** の形式コンポーネントは、データ ソースの [**Model.Company.RegistrationType**] フィールドからの受信データを大文字テキストに変換する式を介してデータ ソースにバインドされ、電子ドキュメントへの出力としてテキストを送信します。 [![画像 - 式によるバインディング](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>プロセス フローの制御

ER フォーミュラ デザイナーは、ドキュメントを生成するプロセス フローを制御する式を定義するために使用できます。 次の処理を行うことができます:

-   ドキュメント作成のプロセスを停止する必要がある場合を判断する条件を定義します。
-   停止したプロセスに対してエンド ユーザーにメッセージを作成する式を指定するか、または報告書作成のプロセスに関する実行ログ メッセージをスローする式を指定します。
-   生成ドキュメントのファイル名と作成の管理条件を指定します。

プロセス フロー制御の各ルールは、個々の検証として設計されています。 次の図は、このタイプの検証を示しています。 この例のコンフィギュレーションの説明を次に示します。

-   検証は、生成する XML ファイルに **INSTAT** ノードが作成されたときに評価されます。
-   トランザクションのリストが空である場合、検証の実行プロセスを停止し、**FALSE** を返します。
-   検証では、ユーザーの優先的に使用する言語でラベル SYS70894 のテキストを含むエラー メッセージを返します。

[![picture-validation](./media/picture-validation.jpg)](./media/picture-validation.jpg) ER フォーミュラ デザイナーは生成する電子ドキュメントのファイル名の指定や、ファイルの作成プロセスの制御にも使用できます。 次の図は、このタイプのプロセス フロー制御の設計を示しています。 この例のコンフィギュレーションの説明を次に示します。

-   [**model.Intrastat**] データ ソースからのレコード一覧を 1,000 までのレコードが含まれるバッチで割ります
-   出力は、作成されたバッチごとに XML 形式のファイル 1 つを含む zip ファイルを作成します。
-   式はファイル名とファイル拡張子を連結して、生成する電子ドキュメントにファイル名を返します。 2 番目のバッチ以降すべてのバッチには、ファイル名の接尾語としてバッチ ID が表示されます。
-   式は、(**TRUE** を返すことで) 少なくともレコードを 1 つ含むバッチのファイル作成のプロセスを有効にします。

[![画像ファイル コントロール](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>基本構文

ER の式は、次のいずれかまたはすべての要素を含めることができます。

-   定数
-   演算子
-   参照
-   パス
-   関数

#### <a name="constants"></a>定数

式の設計時にテキストおよび数値定数 (計算されない定数) を使用できます。 たとえば、**VALUE ("100") + 20**の式では、数値定数 20 および文字列定数 “100” を使用し、**120** という数値を返します。 ER フォーミュラ デザイナーは、エスケープ シーケンスにサポートしており、別の方法で処理する必要がある式の文字列を指定できます。 たとえば、**「レフ トルストイ」「戦争と平和」「ボリューム 1」** の式は、[**レフ トルストイ「戦争と平和」ボリューム 1**] という文字列を返します。

#### <a name="operators"></a>演算子

次の表に、加算、減算、除算、乗算などの基本的な数学演算の実行に使用できる算術演算子を示します。

| オペレーター | 意味              | 例 |
|----------|----------------------|---------|
| +        | 追加             | 1+2     |
| -        | 減算の否定 | 5-2 -1  |
| \*       | 乗算       | 7\*8    |
| /        | 区分             | 9/3     |

次の表に、2 つの値の比較に使用でき、サポートされている比較演算子を示します。

| オペレーター | 意味                  | 例    |
|----------|--------------------------|------------|
| =        | 等しい                    | X=Y        |
| &gt;     | 次の値より大きい             | X&gt;Y     |
| &lt;     | 次の値より小さい                | X&lt;Y     |
| &gt;=    | 以上 | X&gt;=Y    |
| &lt;=    | 以下    | X&lt;=Y    |
| &lt;&gt; | 次の値に等しくない             | X&lt;&gt;Y |

また、1 つ以上の文字列を 1 つのテキストに結合または連結するテキスト連結演算子としてアンパサンド (&) を使用できます。

| オペレーター | 意味     | 例                                        |
|----------|-------------|------------------------------------------------|
| &        | 連結 | 「印刷対象なし」 & 「: 」 & 「レコードが見つかりません」 |

#### <a name="operator-precedence"></a>演算子の優先順位

複合式のパーツを評価する順番は重要です。 たとえば、**1 + 4 / 2** の式の結果は、先に加算または除算のどちらを実行するかによって異なります。 明示的に式の評価方法を定義するためにかっこを使用できます。 たとえば、加算を最初に実行する必要があることを示すには、前の式を **(1 + 4) /2** に変更できます。 式で実行する必要のある工程の順序が明確に定義されていない場合、順序はサポートされる演算子に割り当てられている既定の優先順位に基づきます。 次の表に、それぞれに割り当てられている演算子および優先順位を示します。 高い優先順位 (たとえば、7) がある演算子は、低い優先順位 (たとえば、1) がある演算子より前に評価されます。

| 優先順位 | 演算子      | 構文                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | グループ化       | ( … )                                                    |
| 6          | メンバーのアクセス  | … します。 …                                                    |
| 5          | 関数の呼び出し  | … ( … )                                                  |
| 4          | 乗算 | … \* … … / …                                             |
| 3          | 付加       | … + … … - …                                              |
| 2          | 比較     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | 区切り     | … , …                                                    |

同じ行の演算子には、同等な優先順位があります。 式にこれらの演算子のうち 1 つ以上が含まれる場合、式は左から右に評価されます。 たとえば、**1 + 6 / 2 \* 3 &gt; 5** の式は **true** を返します。 式の閲覧や管理を簡単にするには、式を評価する希望の順序を明示的に示すために、かっこを使用することをお勧めします。

#### <a name="references"></a>参照

式の設計中に使用できる現在の ER コンポーネント (モデルや形式) のすべてのデータ ソースは名前付き参照を使用できます。 たとえば、現在の ER データ モデルには **ReportingDate** データ ソースが含まれ、**DATETIME** データ型の値を返します。 生成ドキュメントでその値を適切に書式設定するために、**DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")** の式のデータ ソースを参照できます。アルファベットの文字を表さない参照データ ソースの名前であるすべての文字は、単一引用符 (') が前に必要です。 参照データ ソースの名前がアルファベットの文字を表さない記号 (たとえば、句読点またはそのほかの書面記号) を少なくとも 1 つ含む場合、名前を単一引用符で囲む必要があります。 次にいくつか例を挙げます。

-   **今日の日付 & 時間** データ ソースは、次のように ER の式で参照する必要があります。**'今日の日付 & 時間’**
-   **Customers** データ ソースの **name()** メソッドは、ER の式で次のように参照する必要があります。**Customers.’name()’**

次の構文は、パラメーターを含む Dynamics 365 for Operation データ ソースのメソッドを呼び出すのに使用されることに注意してください。

- 文字列データ型のパラメーター EN-US を含むシステム データ ソースの isLanguageRTL メソッドは、ER の式で次のように参照する必要があります。System.'isLanguageRTL'("EN-US")。
- メソッド名に英数字シンボルのみが含まれている場合、引用符は必須ではありません。 名前にかっこが含まれているテーブルのメソッドに対しては必須です。

システム データ ソースが、Dynamics 365 for Operation アプリケーション クラス グローバルを参照する ER マッピングに追加される場合、式は、ブール値 FALSE を返します。 変更された式、System.’ isLanguageRTL'("AR") は、ブール値 TRUE を返します。

そのようなメソッド パラメーターに移動することが次の制限で定義されることに注意してください。

- 定数のみをそれらのメソッドに移動することができ、値はデザイン時に定義されます。
- パラメータのプリミティブ (基本) データ型のみが、該当するパラメーター (整数、実数、ブール値、文字列、など。) でサポートされています。

#### <a name="path"></a>パス

式が構成されたデータ ソースを参照する場合、そのデータ ソースの特定のプリミティブ要素の選択にパス定義を使用できます。 ドット (.) は、構成されたデータ ソースの個別要素を区切るために使用します。 たとえば、現在の ER データ モデルにはレコード一覧を返す **InvoiceTransactions** データ ソースが含まれます。 **InvoiceTransactions** レコード構造には、[**AmountDebit**] および [**AmountCredit**] が含まれており、数値を返します。 したがって、請求額を計算するには次の式を設計できます。**InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>関数

次のセクションでは、ER の式で使用できる関数について説明します。 すべてのデータ ソースの式のコンテキスト (現在の ER データ モデルまたは ER フォーマット)、および定数は、呼び出し元関数の引数に従って呼び出し元関数のパラメータとして使用できます。 たとえば、現在の ER データ モデルにはレコード一覧を返す **InvoiceTransactions** データ ソースが含まれます。 **InvoiceTransactions** レコード構造には、[**AmountDebit**] および [**AmountCredit**] が含まれており、数値を返します。 したがって、請求額を計算するには、ER 丸め関数を使用する次の式を設計できます。**ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>サポートされている機能
次の表で、ER データ モデルと ER レポートを設計するために使用できるデータ操作関数を説明します。 この関数の一覧は、固定ではなく開発者によって拡張することができます。 使用できる関数の一覧を表示するには、ER フォーミュラ デザイナーの関数ウィンドウにアクセスします。

### <a name="date-and-time-functions"></a>日時の関数

| 機能                                   | 説明                                                                                                                                                                                                                                                                                                                                                      | 例                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (日時, 日数)                   | 指定された日時値までの指定された日数を追加します。                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** は、将来の日時の 7 日を返します。                                                                                                                                                                                                                            |
| DATETODATETIME (日付)                      | 日時値に指定された日付値を変換します。                                                                                                                                                                                                                                                                                                            | [**DATETODATETIME (CompInfo. 'getCurrentDate()')**] は、現在の Finance and Operations セッションの日付 12/24/2015 を [**12/24/2015 12:00:00 AM**] として返します。 この例では、[**CompInfo**] は、CompanyInfo テーブルを参照する [**Finance and Operations/Table**] タイプの ER データ ソースです。 |
| NOW ()                                     | 日時値として現在の Finance and Operations アプリケーション サーバーの日時を返します。                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | 日付値として現在の Finance and Operations アプリケーション サーバーの日付を返します。                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | **null** の日付値を返します。                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | **null** の日時値を返します。                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (日時, 形式)          | 指定された形式の文字列に指定された日時値を変換します。 (サポートされている形式の詳細については、「[標準](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)」と「[カスタム](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)」を参照してください。)                                                                        | [**DATETIMEFORMAT (NOW(), "dd-MM-yyyy")**] は、指定されたカスタム形式に従って、現在の Finance and Operations アプリケーション サーバーの日付 12/24/2015 を [**"24-12-2015"**] として返します。                                                                                                          |
| DATETIMEFORMAT (日時, 形式, カルチャ) | 指定された形式および[カルチャ](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)の文字列に指定された日時値を変換します。 (サポートされている形式の詳細については、「[標準](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)」と「[カスタム](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)」を参照してください)。 | [**DATETIMEFORMAT (NOW(), "d", "de")**] は、選択されたドイツのカルチャに従って現在の Finance and Operations アプリケーション サーバーの日付 12/24/2015 を [**"24.12.2015"**] として返します。                                                                                                             |
| SESSIONTODAY ()                            | 日付値として現在の Dynamics 365 for Finance and Operations セッションの日付を返します。                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | 日時値として現在の Dynamics 365 for Finance and Operations セッションの日時を返します。                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (日付, 形式)                  | 指定された形式を使用して日付の文字列形式を返します。                                                                                                                                                                                                                                                                                                    | [**DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")**] は、指定されたカスタム形式に従って現在の Dynamics 365 for Finance and Operations セッションの日付 12/24/2015 を [**24-12-2015**] として返します。                                                                                                                      |
| DATEFORMAT (日付, 形式, カルチャ)         | 指定された形式および[カルチャ](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)の文字列に指定された日付値を変換します。 (サポートされている形式の詳細については、「[標準](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)」と「[カスタム](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)」を参照してください)。     | [**DATETIMEFORMAT (SESSIONNOW (), "d", "de")**] は、選択されたドイツのカルチャに従って現在の Finance and Operations セッションの日付 12/24/2015 を [**“24.12.2015”**] として返します。                                                                                                                       |
| DAYOFYEAR (日付)              | 1 月 1 日から指定された日までの日数の整数表現を返します。       | [**DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))**] は [**61**] を返します。 [**DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))**] は [**1**] を返します。 
                                                                                                                      |

**データ変換機能**

| 職務                                   | 説明                                                                                                                                                                                                                                                                                                                                                      | 例                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DATETODATETIME (日付)                 | 日時値に指定された日付値を変換します。           | [**DATETODATETIME (CompInfo. 'getCurrentDate()')**] は、現在の Finance and Operations セッションの日付 12/24/2015 を [**12/24/2015 12:00:00 AM**] として返します。 この例では、[**CompInfo**] は [**CompanyInfo**] テーブルを参照する [**Finance and Operations/Table**] タイプの ER データ ソースです。                                                                                                                       |
| DATEVALUE (文字列、形式)              | 指定された形式を使用して文字列の日付形式を返します。       | [**DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")**] は、指定されたカスタム形式および既定のアプリケーションの [**EN-US**] カルチャに従って、日付 12/21/2016 を返します。                                                                                                                       |
| DATEVALUE (文字列、形式、カルチャ)              | 指定された形式とカルチャを使用して文字列の日付形式を返します。       | [**DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", “IT”)**] は指定されたカスタム形式とカルチャに従って、日付 01/21/2016 を返します。 この機能に対する例外がスローされ、[**DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", “EN-US”)**] は、指定された文字列が有効な日付として認識されていないことを通知します。                                                                                                                       |
| DATETIMEVALUE (文字列、形式)              | 指定された形式を使用して文字列の日時形式を返します。       | [**DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")**] は、指定されたカスタム形式と既定のアプリケーションの [**EN-US**] カルチャに従って、2016 年 12 月 21 日、午前 2 時 55 分 00 秒を返します。                                                                                                                       |
| DATETIMEVALUE (文字列、形式、カルチャ)              | 指定された形式とカルチャを使用して文字列の日時形式を返します。       | [**DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", “IT”)**] は、指定されたカスタム形式およびカルチャに従って 2016 年 12 月 21 日、午前 2 時 55 分 00 秒を返します。 この機能に対する例外がスローされ、[**DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", “EN-US”)**] は、指定された文字列が有効な日時として認識されていないことを通知します。                                                                                                                       |
### <a name="list-functions"></a>リスト機能

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>職務</th>
<th>説明</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (入力, 長さ)</td>
<td>指定された入力文字列を指定された長さのサブ文字列に分割します。 新しいリストとして結果を返します。</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> は、[<strong>文字列</strong>] フィールドがある 2 つのレコードで構成される新しいリストを返します。 最初のレコードのフィールドには、テキスト <strong>&quot;abc&quot;</strong> が、2 つ目のレコードのフィールドには、テキスト <strong>&quot;d&quot;</strong> が入力されます。</td>
</tr>
<tr class="even">
<td>SPLITLIST (リスト, 番号)</td>
<td>それぞれ指定されたレコード数を含むバッチに指定されたリストを分割します。 次の要素を含むバッチの新しいリストとして結果を返します。
<ul>
<li>通常のリストとしてのバッチ (<strong>値</strong>コンポーネント)</li>
<li>現在のバッチ番号 (<strong>BatchNumber</strong>コンポーネント)</li>
</ul></td>
<td>次の例では、<strong>行</strong>データ ソースは、最大 2 つのレコードを含むバッチに分割された 3 つのレコードのレコード リストとして作成されます。 
<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a> 

バッチに分割されたデータ ソース 設計された形式レイアウトで、<strong>行</strong>データ ソースへのバインディングが作成され、各バッチおよびレコードの個々のノードを示す XML 形式の出力が生成されることを示します。 
<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a> 

以下は、設計された形式を実行した結果です。 
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (レコード 1 [, レコード 2, ...])</td>
<td>指定された引数から作成される新しいリストを返します。</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> は、空のレコードを返し、フィールドの一覧には、<strong>MainData</strong> および <strong>OtherData</strong> のレコード リストのすべてのフィールドが含まれます。</td>
</tr>
<tr class="even">
<td>LISTJOIN (リスト 1, リスト 2, ...)</td>
<td>指定された引数のリストから作成した結合されたリストを返します。</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> は、6 つのレコードのリストを返し、<strong>文字列</strong>データ型のフィールドの 1 つに単一の文字が含まれます。</td>
</tr>
<tr class="odd">
<td>ISEMPTY (リスト)</td>
<td>指定されたリストに要素がない場合、<strong>TRUE</strong> を返します。 それ以外の場合は、<strong>FALSE</strong> を返します。</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (リスト)</td>
<td>指定されたリストをリスト構造のソースとして使用し、空のリストを返します。</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> は、<strong>SPLIT</strong> 関数で返ってきたリストと同じ構造を持つ新しい空のリストを返します。</td>
</tr>
<tr class="odd">
<td>FIRST (リスト)</td>
<td>指定されたリストの最初のレコードが空でない場合、そのレコードを返します。 それ以外の場合は、例外をスローします。</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (リスト)</td>
<td>指定されたリストの最初のレコードが空でない場合、そのレコードを返します。 それ以外の場合は、<strong>null</strong> レコードを返します。</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (リスト)</td>
<td>指定されたリストの最初の項目だけを含んだリストを返します。</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (パス)</td>
<td>指定されたパスと一致するすべての項目を表す新しい単純化したリストを返します。 パスは、レコード リスト データ型のデータ ソースの要素への有効なデータ ソース パスとして定義する必要があります。 文字列、日付などのデータ要素へのパスは、ER 式ビルダーのデザイン時間でエラーを生成する必要があります。</td>
<td>データ ソース (DS) として <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> を入力する場合、<strong>COUNT( ALLITEMS (DS.Value))</strong> は <strong>3</strong> を返します。</td>
</tr>
<tr class="odd">
<td>ORDERBY (リスト [, 式 1, 式 2, …])</td>
<td>式として定義できる引数指定に従って並べ替えて、指定されたリストを返します。</td>
<td><strong>仕入先</strong>を VendTable テーブルを参照する ER データ ソースとしてコンフィギュレーションすると、<strong>ORDERBY (仕入先, 仕入先.'name()')</strong> は昇順の名前で並べ替えられた仕入先のリストを返します。</td>
</tr>
<tr class="even">
<td>REVERSE (リスト)</td>
<td>逆の並べ替え順でリストを返します。</td>
<td><strong>仕入先</strong>を VendTable テーブルを参照する ER データ ソースとしてコンフィギュレーションすると、<strong>REVERSE (ORDERBY (仕入先, 仕入先.'name()')) )</strong> は降順の名前で並べ替えられた仕入先のリストを返します。</td>
</tr>
<tr class="odd">
<td>WHERE (リスト, 条件)</td>
<td>指定された条件に従ってフィルタ処理して、指定されたリストを返します。 <strong>FILTER</strong> 関数とは異なり、指定された条件がメモリの一覧に適用されます。</td>
<td><strong>仕入先</strong>を VendTable テーブルを参照する ER データ ソースとしてコンフィギュレーションすると、<strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> は仕入先グループ 40 に属している仕入先のリストを返します。</td>
</tr>
<tr class="even">
<td>ENUMERATE (リスト)</td>
<td>指定されたリストの列挙されたレコードから構成される新しいリストを返し、次の要素を公開します。
<ul>
<li>通常のリストとして指定されたリスト レコード (<strong>値 </strong>コンポーネント)</li>
<li>現在のレコード インデックス (<strong>番号 </strong>コンポーネント)</li>
</ul></td>
<td>次の例では、<strong>列挙型</strong>データ ソースは、<strong>VendTable</strong> テーブルを参照する<strong>仕入先</strong>データ ソースの仕入先レコードの列挙型リストとして作成されます。 
<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a> 

データ バインディングが作成され、列挙型ノードとして個々の仕入先を示す XML 形式の出力が生成されます。 
<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a> 

これは、設計された形式を実行した結果です。 
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (リスト)</td>
<td>指定されたリストが空でない場合、そのリストのレコードの数を返します。 それ以外の場合は、<strong>0</strong> (ゼロ) を返します。</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> は、<strong>SPLIT</strong> 関数が 2 つのレコードから構成されるリストを作成するため、<strong>2</strong> を返します。</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (パス)</td>
<td>次のタイプのうち 1 つの引数から作成されたレコード リストを返します。
<ul>
<li>モデルの列挙</li>
<li>形式列挙</li>
<li>コンテナー</li>
</ul>
作成されたリストは、次のフィールドを持つレコードで構成されます。
<ul>
<li>氏名</li>
<li>ラベル</li>
<li>説明</li>
</ul>
ラベルおよび説明フィールドは、形式の言語設定に基づいてランタイム値で返します。</td>
<td>次の例は、データ モデルで導入された列挙を示します。 
<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

以下に例を示します。
<ul>
<li>データ ソースとしてレポートに挿入されるモデル列挙。</li>
<li>この関数のパラメーターとしてモデル列挙を使用するように設計されている ER の式。</li>
<li>作成された ER の式を使用してレポートに挿入されるレコード リスト タイプのデータ ソース。</li>
</ul>
<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> 

次の例では、LISTOFFIELDS 機能を使用して作成されたレコードのリストの種類のデータ ソースにバインドされている ER 形式要素を示します。
<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

これは、設計された形式を実行した結果です。
<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>

注:</strong> ラベルと説明の翻訳文は、親ファイルおよびフォルダー形式要素に対して設定されている言語設定に従って、ER 形式出力で入力されます。</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (リスト, フィールド名, 区切り記号)</td>
<td>選択した区切り記号で区切られた一覧から連結されたフィールドの値の文字列を返します。</td>
<td>SPLIT (“abc” , 1) をデータ ソース DS として入力した場合、式 STRINGJOIN (DS, DS.Value, “:”) は、「a:b:c」を返します</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (リスト, 制限値, 制限のソース)</td>
<td>指定されたリストをサブリストの新しいリストに分割し、レコード リストの内容の結果を返します。 制限値のパラメーターは、元のリストを分割する制限値を指定します。 制限のソースのパラメーターは、合計が増加するステップを指定します。 制限は、制限のソースが定義済み制限を超えると特定のリストの 1 つの項目に適用されません。</td>
<td>次の例では、データ ソースを使用してサンプル形式を示します。 
<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

これは、商品のフラット リストを示す形式実行の結果です
<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

次の例は、1 つのバッチに合計重量が 9 を超えない商品を含める必要がある場合、商品アイテムのリストをバッチに表示するために調整されたフォーマットと同じフォーマットを示しています。
<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

これは、調整された形式を実行した結果です。 <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

<strong>注記:</strong> 制限は、制限のソース (重量) の値 (11) が定義済みの制限 (9) を超えるため、元のリストの最後の項目に適用されません。 関数 <strong>WHERE</strong> または対応する形式の要素で<strong>有効</strong>な式を使用して、レポート生成時 (必要な場合) サブリストを無視 (スキップ) できます。</td>
</tr>
<tr class="odd">
<td>FILTER (リスト, 条件)</td>
<td>クエリの変更によって指定された条件でフィルター処理された特定のリストを返します。 <strong>WHERE</strong> 関数とは異なり、指定された条件はテーブル レコード タイプのすべての ER データ ソースにデータベース レベルで適用されます。</td>
<td>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;) は、<strong>仕入先</strong> が <strong>VendTable</strong> テーブルを参照する ER データ ソースとしてコンフィギュレーションされている場合、仕入先のグループ「40」に属している仕入先だけのリストを返します。</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>論理機能

| 職務                                                                                | 説明                                                                                                                                                                                                                                                                     | 例                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CASE (式, オプション 1, 結果 1 \[, オプション 2, 結果 2\] ... \[, 既定の結果\]) | 指定された代替オプションに対して指定された式の値を評価します。 式の値に等しいオプションの結果を返します。 それ以外の場合は、任意で入力された既定の結果 (オプションに続く最後のパラメータ) を返します。 | [**CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "冬", "11", "冬", "12", "冬", "")**] は、Finance and Operations セッションの日付が 10 月～ 12 月である場合に[**"冬"**] という文字列を返します。 それ以外の場合は、空白文字列を返します。 |
| IF (条件, 値 1, 値 2)                                                        | 特定の条件が満たされているときに指定された値 1 を返します。 それ以外の場合は、値 2 を返します。 値 1 と値 2 がレコードまたはレコード リストの場合、両方のリストが存在するフィールドだけの結果になります。                                                                     | **IF (1=2, "条件を満たしている", "条件を満たしていない")** は、**"条件を満たしていない"** の文字列を返します。                                                                                                                                                      |
| NOT (条件)                                                                         | 指定された条件の取消論理値を返します。                                                                                                                                                                                                                   | **NOT (TRUE)** は **FALSE** を返します。                                                                                                                                                                                                                            |
| AND (条件 1\[, 条件 2, ...\])                                                 | *すべて*の指定された条件が真の場合、**TRUE** を返します。 それ以外の場合は、**FALSE** を返します。                                                                                                                                                                                            | **AND (1=1, "a"="a")** は、**TRUE** を返します。 **AND (1=2, "a"="a")** は、**FALSE** を返します。                                                                                                                                                                           |
| OR (条件 1\[, 条件 2, ...\])                                                  | *すべて*の指定された条件が偽の場合、**FALSE** を返します。 *いずれか*の指定された条件が真の場合、**TRUE** を返します。                                                                                                                                                                 | **OR (1=2, "a"="a")** は、**TRUE** を返します。                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>算術関数

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>機能</th>
<th>説明</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (数値)</td>
<td>指定された数値の絶対値 (符号なしの数値) を返します。</td>
<td><strong>ABS (-1)</strong> は、<strong>1</strong> を返します。</td>
</tr>
<tr class="even">
<td>POWER (数値, 累乗)</td>
<td>指定された正の数に指定された累乗をした結果を返します。</td>
<td><strong>POWER (10, 2)</strong> は、<strong>100</strong> を返します。</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (文字列、小数点記号、桁区切り記号)</td>
<td>指定された文字列を数字に変換します。 指定された記号は整数と小数点以下の数を区切り、指定された千の位の区切り記号も使用されます。</td>
<td><strong>NUMBERVALUE(&quot;1 234,56&quot;, &quot;,&quot;, &quot; &quot;)</strong> は、<strong>1234.56</strong> の値を返します。</td>
</tr>
<tr class="even">
<td>VALUE (文字列)</td>
<td>指定された文字列を数字に変換します。 コンマとドット (.) が小数点の区切り記号とみなされ、先頭のハイフン (-) は負の記号として使用されます。 他の数値以外の文字が指定された文字列にある場合、例外をスローします。</td>
<td><strong>VALUE (&quot;1 234,56&quot;)</strong> は例外をスローします。</td>
</tr>
<tr class="odd">
<td>ROUND (数値, 小数点以下の桁数)</td>
<td>指定された小数点以下の桁数に丸めて、指定された数値を返します。
<ul>
<li>指定した小数値が 0 (ゼロ) より大きい場合、指定された数字は指定された小数点以下の桁数で四捨五入されます。</li>
<li>指定した小数値が 0 (ゼロ) の場合、指定された数字は最も近い整数に四捨五入されます。</li>
<li>指定した小数値が 0 (ゼロ) より小さい場合、指定された数字は小数点より左で四捨五入されます。</li>
</ul></td>
<td><strong>ROUND (1200.767, 2)</strong> は、小数点第 2 位で四捨五入され、<strong>1200.77</strong> を返します。 <strong>ROUND (1200.767, -3)</strong> は、1,000 の最も近い倍数に四捨五入され、<strong>1000</strong> を返します。</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (数値, 小数点以下の桁数)</td>
<td>指定された小数点以下の桁数で (ゼロ方向に) 切り捨てて、指定された数値を返します。 <strong>注:</strong> この関数は、<strong>ROUND</strong> のように機能しますが、常に指定した数字を切り捨てます。</td>
<td><strong>ROUNDDOWN (1200.767, 2)</strong> は、小数点第 2 位で切り捨てられ、<strong>1200.76</strong> を返します。 <strong>ROUNDDOWN (1700.767, -3)</strong> は、1,000 の最も近い倍数に切り捨てられ、<strong>1000</strong> を返します。</td>
</tr>
<tr class="odd">
<td>ROUNDUP (数値, 小数点以下の桁数)</td>
<td>指定された小数点以下の桁数で (ゼロとは逆方向に) 切り上げて、指定された数値を返します。 <strong>注:</strong> この関数は、<strong>ROUND</strong> のように機能しますが、常に指定した数字を切り上げます。</td>
<td><strong>ROUNDUP (1200.763, 2)</strong> は、小数点第 2 位で切り上げられ、<strong>1200.77</strong> を返します。 <strong>ROUNDUP (1200.767, -3)</strong> は、1,000 の最も近い倍数に切り上げられ、<strong>2000</strong> を返します。</td>
</tr>
</tbody>
</table>

**データ変換機能**

| 職務             | 説明                                                                                                                                                                                                                                     | 例                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| VALUE (文字列) | 指定された文字列を数字に変換します。 コンマとドット (.) が小数点の区切り記号とみなされ、先頭のハイフン (-) は負の記号として使用されます。 他の数値以外の文字が指定された文字列にある場合、エラーが発生します。                                                                                  | **VALUE ("1 234,56")** は例外をスローします。   |
| NUMBERVALUE (文字列、小数点記号、桁区切り記号) | 指定された文字列を数字に変換します。 指定された記号は整数と小数点以下の数を区切り、指定された千の位の区切り記号も使用されます。                                                                                  | **NUMBERVALUE("1 234,56", ",", " ")** は、**1234.56** の値を返します。    |
| INTVALUE (文字列) | 文字列の整数表現を返します。 任意の利用可能な小数部分は切り捨てられます。                                                                                  | [**INTVALUE (「100.77」)**] は [**100**] を返します。 |
| INTVALUE (番号) | 番号の整数表現を返します。 任意の利用可能な小数部分は切り捨てられます。                                                                                  | [**INTVALUE (-100.77)**] は [**-100**] を返します。 |
| INT64VALUE (文字列) | 文字列の int64 表現を返します。 任意の利用可能な小数部分は切り捨てられます。                                                                                  | [**INT64VALUE (“22565422744”)**] は、[**22565422744**] を返します。 |
| INT64VALUE (数値) | 番号の int64 表現を返します。 任意の利用可能な小数部分は切り捨てられます。                                                                                  | [**INT64VALUE (22565422744.00)**] は、[**22565422744**] を返します。 |



### <a name="record-functions"></a>レコード機能

| 職務             | 説明                                                                                                                                                                                                                                     | 例                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (リスト) | 指定されたレコード リストまたはレコードと同じ構造を持つ **null** レコードを返します。 **注:**この関数は廃止されています。 代わりに **EMPTYRECORD** を使用します。                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** は、**SPLIT** 関数で返ってきたリストと同じ構造を持つ新しい空のレコードを返します。 |
| EMPTYRECORD (レコード) | 指定されたレコード リストまたはレコードと同じ構造を持つ **null** レコードを返します。 **注記:** **null** レコードは、すべてのフィールドが空の値 (数字の場合 **0** \[ゼロ\]、文字列の場合、空の文字列など) を持つレコードです。 | **EMPTYRECORD (SPLIT ("abc", 1))** は、**SPLIT** 関数で返ってきたリストと同じ構造を持つ新しい空のレコードを返します。   |

### <a name="text-functions"></a>テキスト関数

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>機能</th>
<th>説明</th>
<th>例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (文字列)</td>
<td>大文字に変換して、指定された文字列を返します。</td>
<td><strong>UPPER(&quot;Sample&quot;)</strong> は、<strong>&quot;SAMPLE&quot;</strong> を返します。</td>
</tr>
<tr class="even">
<td>LOWER (文字列)</td>
<td>小文字に変換して、指定された文字列を返します。</td>
<td><strong>LOWER (&quot;Sample&quot;)</strong> は、<strong>&quot;sample&quot;</strong> を返します。</td>
</tr>
<tr class="odd">
<td>LEFT (文字列, 文字数)</td>
<td>指定された文字列の先頭から指定された数の文字を返します。</td>
<td><strong>LEFT (&quot;Sample&quot;, 3)</strong> は、<strong>&quot;Sam&quot;</strong> を返します。</td>
</tr>
<tr class="even">
<td>RIGHT (文字列, 文字数)</td>
<td>指定された文字列の末尾から指定された数の文字を返します。</td>
<td><strong>RIGHT (&quot;Sample&quot;, 3)</strong> は、<strong>&quot;ple&quot;</strong> を返します。</td>
</tr>
<tr class="odd">
<td>MID (文字列, 開始位置, 文字数)</td>
<td>指定された文字列の指定された位置から始まる指定された数の文字を返します。</td>
<td><strong>MID (&quot;Sample&quot;, 2, 3)</strong> は、<strong>&quot;amp&quot;</strong> を返します。</td>
</tr>
<tr class="even">
<td>LEN (文字列)</td>
<td>指定された文字列の文字数を返します。</td>
<td><strong>LEN (&quot;Sample&quot;)</strong> は、<strong>6</strong> を返します。</td>
</tr>
<tr class="odd">
<td>CHAR (数値)</td>
<td>指定された Unicode 番号で参照される文字列を返します。</td>
<td><strong>CHAR (255)</strong> は、<strong>&quot;ÿ&quot;</strong> を返します。 <strong>注記:</strong> 返される文字列は親ファイル形式の要素で選択したエンコードによって異なります。 サポートされているエンコードの一覧は、<a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">エンコード クラス</a> トピックで参照できます。</td>
</tr>
<tr class="even">
<td>CONCATENATE (文字列 1 [, 文字列 2, …])</td>
<td>指定されたすべての文字列を 1 つの文字列に結合して返します。</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> は、<strong>&quot;abcdef&quot;</strong> を返します。 <strong>注記:</strong> 式 <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> でも <strong>&quot;abcdef&quot;</strong> を返します。</td>
</tr>
<tr class="odd">
<td>TRANSLATE (文字列, パターン, 置換)</td>
<td>指定されたパターン文字列でのすべての文字の発生が、指定された置換文字列の対応する位置にある文字で置換され、指定された文字列を返します。</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> は、パターン <strong>&quot;cd&quot;</strong> を文字列 <strong>&quot;GH&quot;</strong> に置換して、<strong>&quot;abGHef&quot;</strong> を返します。</td>
</tr>
<tr class="even">
<td>REPLACE (文字列, パターン, 置換, 正規表現フラグ)</td>
<td>指定された正規表現フラグが<strong>真</strong>である場合、この関数のパターン引数として指定される正規表現を適用して変更し、指定された文字列を返します。 この式は、置換する必要のある文字列を検索するために使用されます。 指定された置換引数の文字は、見つかった文字を置換するために使用されます。 指定された正規表現フラグが<strong>偽</strong>である場合、この関数は <strong>TRANSLATE</strong> のように機能します。</td>
<td>  <strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> は、すべての数値以外の記号を削除する正規表現を適用し、<strong>&quot;19234564971&quot;</strong> を返します。 <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> は、パターン <strong>&quot;cd&quot;</strong> を文字列 <strong>&quot;GH&quot;</strong> に置換して、<strong>&quot;abGHef&quot;</strong> を返します。</td>
</tr>
<tr class="odd">
<td>TEXT (入力)</td>
<td>現在の Finance and Operations インスタンスのサーバーのロケール設定に従って書式設定されるテキスト文字列に変換して、指定された入力を返します。 <strong>実数</strong>型の値では、文字列変換が小数点第 2 位に制限されます。</td>
<td>Finance and Operations インスタンスのサーバーのロケールが [<strong>EN-US</strong>] で定義されている場合、[<strong>TEXT (NOW ())</strong>] は現在の Finance and Operations セッションの日付 12/17/2015 をテキスト文字列 [<strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>] として返します。 <strong>TEXT (1/3)</strong> は、<strong>&quot;0.33&quot;</strong> を返します。</td>
</tr>
<tr class="even">
<td>FORMAT (文字列 1, 文字列 2[, 文字列 3, ...])</td>
<td>すべての <strong>%N</strong> を <em>n</em> 番目の引数に置き換えて書式設定し、指定された文字列を返します。 引数は文字列です。 パラメーターに引数が指定されない場合は、文字列内では <strong>&quot;%N&quot;</strong> として返されます。 <strong>実数</strong>型の値では、文字列変換が小数点第 2 位に制限されます。</td>
<td>この例では、<strong>PaymentModel</strong> データ ソースは <strong>顧客</strong>コンポーネント経由で顧客のリスト、[<strong>ProcessingDate</strong>] フィールド経由で処理日の値を返します。 
<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a> 

選択した顧客の電子ファイルを生成するよう設計されている ER 形式では、<strong>PaymentModel</strong> がデータ ソースとして選択され、プロセス フローを制御します。 選択した顧客がレポートが処理される日付に停止されている場合、例外がエンド ユーザーにスローされます。 このタイプの処理制御のために設計された式は、次のリソースを使用できます。
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
設計できる式を次に示します。FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;)) レポートが 2015 年 12 月 17 日に <strong>EN-US</strong> カルチャおよび <strong>EN-US</strong> 言語で <strong>Litware Retail の顧客</strong>に対して処理される場合、この式はエンド ユーザーへの例外メッセージとして示すことができる次のテキストを返します。&quot;Nothing to print. 顧客の Litware Retail は 2015 年 12 月 17 日に停止されます。&quot; 同じレポートが 2015 年 12 月 17 日に [<strong>DE</strong>] カルチャおよび [<strong>DE</strong>] 言語で [<strong> Litware Retail の顧客</strong>] に対して処理される場合、この式は別の日付形式を使用する次のテキストを返します。&quot;Nichts zu drucken. Debitor ' Litware Retail' wird für 17.12.2015 gesperrt.&quot;<strong>注記:</strong> 次の構文は ER の式でラベルに適用されます。
<ul>
<li><strong>Finance and Operations リソースのラベルの場合: </strong><strong>@&quot;X&quot;</strong>、X はアプリケーション オブジェクト ツリー (AOT) のラベル ID です</li>
<li><strong>ER コンフィギュレーションに存在するラベルの場合: </strong><strong>@&quot;GER_LABEL:X&quot;</strong>、X は、ER コンフィギュレーションのラベル ID です</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (数値, 形式)</td>
<td>指定された形式で指定された数値の文字列形式を返します。 (サポートされている形式の詳細については、「<a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">標準</a>」と「<a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">カスタム</a>」を参照してください)。この関数が実行されるコンテキストが、数値の書式設定に使用されるカルチャを決めます。</td>
<td>EN-US カルチャの場合、<strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> は <strong>&quot;45.00 %&quot;</strong> を返します。 <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> は <strong>&quot;10&quot;</strong> を返します。</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (数, 言語, 通貨, 通貨名を印刷フラグ, 小数点)</td>
<td>定義された言語でのテキスト文字列で綴られた (変換された) 数字を返します。 言語コードはオプションです。空の文字列として定義されている場合、連続したコンテキストの言語コード (生成するフォルダーまたはファイルで指定) が代わりに使用されます。 通貨コードはオプションです。 空の文字列として定義されている場合、会社基本通貨が取得されます。 <strong>通貨名を印刷</strong>パラメーターおよび<strong>小数点</strong>パラメーターは次の言語コードに対してのみ分析されることに注意してください: <strong>CS</strong>、<strong>ET</strong>、<strong>HU</strong>、<strong>LT</strong>、<strong>LV</strong>、<strong>PL</strong>、<strong>RU</strong>。 [<strong>通貨名を印刷</strong>] パラメーターは、通貨の語形変化にサポートする国のコンテキストを持つ Finance and Operations の会社に対してのみ分析されることに注意してください。</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2) は、「One Thousand Two Hundred Thirty Four and 56」を返します NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) は、「Sto dwadzieścia」を返します NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2) は、「Сто двадцать евро 21 евроцент」を返します</td>
</tr>
<tr class="odd">
<td>PADLEFT (文字列, 長さ, パディング文字)</td>
<td>現在の文字列の先頭が指定の文字でパディングされた指定の長さの文字列を返します。</td>
<td>PADLEFT (“1234”, 10, “ “) は、テキスト文字列「      1234」を返します。</td>
</tr>
<tr class="even">
<td>TRIM (文字列)</td>
<td>先頭と末尾のスペースを切り捨て、単語間の複数のスペースを削除してから、指定されたテキストを返します。 </td>
<td>[<strong>TRIM (「     サンプル     テキスト     」)</strong>] は [<strong>「サンプル テキスト」。</strong>] を返します</td>
</tr>
<tr class="odd">
<td>GETENUMVALUEBYNAME (列挙データ ソースのパス、列挙値のラベル テキスト)</td>
<td>この列挙ラベルの指定されたテキストで、指定された列挙データ ソースの値を返します。</td>
<td>次の例は、データ モデルで導入された列挙 ReportDirection を示します。 列挙値のラベルが定義されていることに注意してください。
<a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>  
<p>以下に例を示します。</p>
<ul><li>データ ソース [<strong>$Direction</strong>] としてレポートに挿入されるモデル列挙 [<strong>ReportDirection</strong>]</li>
<li>この関数のパラメーターとしてモデル列挙を使用するように設計されている ER の式 [<strong>$IsArrivals</strong>]。 この式の値は [<strong>TRUE</strong>] です。
</li></ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></td>
</tr>
</tbody>
</table>

**データ変換機能**

| 職務             | 説明                                                                                                                                                                                                                                     | 例                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| TEXT (入力) | 現在の Finance and Operations インスタンスのサーバーのロケール設定に従って書式設定されるテキスト文字列に変換して、指定された入力を返します。
実数型の値では、文字列変換が小数点第 2 位に制限されます。| Finance and Operations インスタンスのサーバーのロケールが [**EN-US, TEXT (NOW ())**] として定義されている場合、現在の Finance and Operations セッションの日付 12/17/2015 はテキスト文字列 [**"12/17/2015 07:59:23 AM"**] として返されます。
[**TEXT (1/3) は「0.33」を返します**]。 |
| QRCODE (文字列) | 指定された文字列の QR コード画像を base64 バイナリ形式で返します。 | [**QRCODE (「サンプル テキスト」)**] は [**U2FtcGxlIHRleHQ=**] を返します。   |

### <a name="data-collection-functions"></a>データ収集機能

| 職務             | 説明                                                                                                                                                                                                                                     | 例                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATELEMENTNAME () | 現在の形式の要素の名前を返します。 現在のファイルの**出力の詳細を収集**フラグを無効にすると空の文字列が返されます。| これらの関数の用途の詳細については、**ER 棚卸および集計のために出力された形式の使用** (**IT サービス/ソリューション コンポーネントの取得/開発**業務プロセスの一部) タスク ガイドを参照してください。 |
| SUMIFS (集計のためのキー文字列, 基準範囲 1 の文字列, 基準値 1 の文字列 \[, 基準範囲 2 の文字列, 基準値 2 の文字列, …\]) |この形式の実行中に収集された、入力した条件 (範囲と値のペア) を満たす XML のノード (キーとして定義された名前を持つ) の合計値を返します。 現在のファイルの**出力の詳細を収集**フラグを無効にすると 0 が返されます。 |            |
| SUMIF (集計のためのキー文字列, 基準範囲の文字列, 基準値の文字列) | この形式の実行中に収集された、入力した条件 (範囲と値) を満たす XML のノード (キーとして定義された名前を持つ) の合計値を返します。 現在のファイルの**出力の詳細を収集**フラグを無効にすると 0 が返されます。|           |
| COUNTIFS (基準範囲 1 の文字列, 基準値 1 の文字列 \[, 基準範囲 2 の文字列, 基準値 2 の文字列, …\]) | この形式の実行中に収集された、入力した条件 (範囲と値のペア) を満たす XML のノードの数を返します。 現在のファイルの**出力の詳細を収集**フラグを無効にすると 0 が返されます。|     |
| COUNTIF (基準範囲の文字列, 基準値の文字列) | この形式の実行中に収集された、入力した条件 (範囲と値) を満たす XML のノードの数を返します。 現在のファイルの**出力の詳細を収集**フラグを無効にすると 0 が返されます。|          |
| COLLECTEDLIST (基準範囲 1 の文字列, 基準値 1 の文字列 \[, 基準範囲 2 の文字列, 基準値 2 の文字列, …\]) | この形式の実行中に収集された、入力した条件 (範囲と値) を満たす XML のノードの値のリストを返します。 現在のファイルの**出力の詳細を収集**フラグを無効にすると空のリストが返されます。|               |   




### <a name="other-business-domainspecific-functions"></a>その他 (ビジネス ドメインの特定の) 関数

| 職務                                                                         | 説明                                                                                                                                                                                                                                                        | 例                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (数量, 換算元の通貨, 換算先の通貨, 日付, 会社)        | 特定の日付で指定された Finance and Operations の会社の設定を使用して換算元の通貨から換算先の通貨に指定された金額を変換します。                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** は、DEMF 会社の設定に基づいて現在のセッションの日付の 1 ユーロに相当する額を米ドルで返します。                                                                                                                                  |
| ROUNDAMOUNT (数値, 小数点以下の桁数, 丸めルール)                                       | 指定された丸めルールと小数点以下の桁数に従って指定された数量を丸めます。 [**注記:**] 丸めルールは Finance and Operations の [**RoundOffType**] 列挙の値として指定する必要があります。                          | **model.RoundOff** パラメーターが****切り捨て****に設定されている場合、**ROUNDAMOUNT (1000.787, 2, model.RoundOff)** は、値 **1000.78** を返します。 **model.RoundOff** パラメータが**標準**または**切り上げ**に設定されている場合、**ROUNDAMOUNT (1000.787, 2, model.RoundOff)** は、値 **1000.79** を返します。 |
| CURCredRef (数字)                                                              | 指定された請求書番号の数字に基づいて、送金受取人参照情報を返します。                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** は、**"2200002"** を返します。                                                                                                                                                                                                                                                         |
| MOD\_97 (数字)                                                                 | 指定された請求書番号の数字に基づいて、MOD97 式として送金受取人参照情報を返します。                                                                                                                                                            | **MOD\_97 ("VEND-200002")** は、**"20000285"** を返します。                                                                                                                                                                                                                                                           |
| ISOCredRef (数字)                                                              | 指定された請求書番号の数字とアルファベット記号に基づいて、ISO 送金受取人参照情報を返します。 **注:**ISO 準拠ではないアルファベットの記号を削除するには、入力パラメータを変換してからこの関数に渡す必要があります。 | **ISOCredRef ("VEND-200002")** は、**"RF23VEND-200002"** を返します。                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (文字列, 番号)                                  | 追加の財務分析コード ID を取得します。 分析コードはコンマで区切られた ID としてこの文字列に表されます。 番号は、この文字列で要求された分析コードの順序コードを定義します。                                                                            | CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3) は、「CC」を返します                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | 現在ユーザーがログインしている法人 (会社) のコードのテキスト表現を返します。                                                                                                                                                                                                                    | [**GETCURRENTCOMPANY ()**] は、ユーザーがログインした Finance and Operations の会社 [**Contoso Entertainment System USA**] に対する [**USMF**] を返します。                                                                                                                                                                                                                                                                                                              |
| CH\_BANK\_MOD\_10 (数値)                                                       | 指定された請求書番号の数値に基づいて、MOD10 式として送金受取人参照情報を返します。                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") は、3 を返します                                                                                                                                                                                                                                                                   |
| FA\_SUM (固定資産コード, 価値モデル コード, 開始日, 終了日)               | 期間の固定資産額の準備済データ コンテナーを返します。                                                                                                                                                                                         | FA\_SUM ("COMP-000001", “現行”, Date1, Date2) は、Date1 から Date2 の期間中で、価値モデル「現行」の固定資産「COMP-000001」の準備済データ コンテナーを返します。                                                                                                                        |
| FA\_BALANCE (固定資産コード, 価値モデル コード, レポート年度, 報告日) | 固定資産残高の準備済データ コンテナーを返します。 レポート年度は、Finance and Operations の列挙の値 [**AssetYear**] として指定される必要があります。                                                                                           | 「FA\_SUM ("COMP-000001", “現行”, AxEnumAssetYear.ThisYear, SESSIONTODAY ())」は、現在の 365 for Finance and Operations セッションの日付で価値モデル「現行」である固定資産「COMP-000001」の残高の準備済データ コンテナーを返します。                                                                |
| TABLENAME2ID (文字列)                                                       | 指定されたテーブル名のテーブル ID の整数表現を返します。                                                                                                                                                                      | [**TABLENAME2ID (「イントラスタット」)**] は [**1510**] を返します。                                                                                                                                                                                                                                                                   |
| ISVALIDCHARACTERISO7064 (文字列)                                                       | 指定された文字列が有効な国際銀行番号 (IBAN) を表す場合、ブール値 [**TRUE**] を返します。 それ以外の場合は、ブール値 [**FALSE**] を返します。                                                                                                                                                                      | [**ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")**] は [**TRUE**] を返します。 [**ISVALIDCHARACTERISO7064 ("AT61")**] は [**FALSE**] を返します。                                                                                                                                                                                                                                                                   |

### <a name="functions-list-extension"></a>関数の一覧の拡張

ER では ER の式で使用される関数の一覧を拡張できます。 これにはエンジニアリングの実績がいくらか要求されます。 詳細については、「[電子申告関数の一覧の拡張](general-electronic-reporting-formulas-list-extension.md)」を参照してください。

<a name="see-also"></a>参照
--------

[電子申告の概要](general-electronic-reporting.md)

[電子申告 (ER) 関数の一覧の拡張](general-electronic-reporting-formulas-list-extension.md)




