---
title: 電子レポートの式でサポートされる複合データ型
description: このトピックでは、電子申告 (ER) の式でサポートされる複合データ型について説明します。
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 933c8211276c1335a6a81bf4a8cb1c3f270762d4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689245"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>電子レポートの式でサポートされる複合データ型

[!include [banner](../includes/banner.md)]

このトピックでは、[電子申告 (ER)](general-electronic-reporting.md)の式でサポートされる複合データ型について説明します。 複合データ型は、[クラス](#class)、[コンテナー](#container)、[レコード](#record)、[レコード リスト](#record-list)、[オブジェクト](#object) です 。

## <a name="class"></a><a name="class"></a>クラス

データ型: *クラス* は、パブリック アプリケーション クラスを参照します。 ERでは、参照されるクラスのすべてのパブリック メソッドに対して個別のフィールドを含む [*レコード*](#record) として表現されます。 メソッドの呼び出しがパラメータ化されている場合は、メソッドを呼び出す構成がされている ER 式の中で、適切なタイプの必要な引数も指定する必要があります。

ER マッピング および フォーマット のコンポーネントでは、データソースとして提示され、*クラス* タイプの値を返す **クラス** データソースを追加することができます。 このデータ ソースは、実行時に呼び出すクラスのパブリック メソッドを公開しています。

> [!NOTE]
> 値を返すメソッドのみを ER 式から呼び出できます。
>
> ER 式から呼び出することができるのは、0 から 8 の範囲の引数を持つメソッドのみです。

*クラス* の既定値は **null 値** です。

次の図では、 **クラス** タイプの **System information(xInfo)** データソースを追加して **xInfo** アプリケーション クラスのインスタンスを作成し、その **productName()** メソッドを呼び出して現在のアプリケーションの名前を受け取る方法を表わしています。 現在のアプリケーションの名前は、ER データモデルの **ソフトウェア名 (SoftwareName)** フィールドに設定された `xInfo.productName` バインドの実行により、ランタイムに取得されます。 このバインドは、現在のモデル・マッピングで **システム情報 (xInfo)** データ ソースとして表現されている **xInfo** アプリケーション・クラスの `productName()` メソッドを呼び出します。

[![ER モデル マッピング デザイナーでのクラス データ ソースの構成。](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

以下の図は、生成されたドキュメントに提供されたアプリケーション名を入れる ER フォーマットの設定です。 使用したデータモデルの **ソフトウェア名 (SoftwareName)** フィールドは、ER フォーマットの **softwareUsed** XML 要素の下に入れ子になっている **String** コンポーネントにバインドされます。 そのため、現在のアプリケーションの名前は、XML形式で生成されたドキュメントの **softwareUsed** XML要素にランタイムで配置されます。

[![ER 形式デザイナでの電子発信ドキュメントの構造の構成。](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>コンテナー

*コンテナ* データ 型はバイナリ コンテンツを保持します。 *コンテナー* 値は、ストレージから生成されたドキュメントに特定の情報を渡すために使用できます。 このデータタイプは、ER フレームワークでは、生成されたドキュメントに会社のロゴなどのメディア コンテンツを入れるためによく使われます。

> [!NOTE]
> すべてのメディア アイテムは *コンテナー* 値として表現できますが、すべての *コンテナー* 値がメディア アイテムを表すわけではありません。 そのため、ER形式を構成して、*コンテナー* を使用して生成されたドキュメントに画像を格納する場合に、参照先の *コンテナー* がメディア コンテンツを返さない場合、次のような例外が発生する可能性があります: 「コードの実行エラー: バイナリ (object) メソッドの method constructFromContainer が無効なパラメーターを呼び出しました」。

*コンテナー* の既定値は **null 値** です。

次の図は、**販売請求書** モデルのマッピングにおいて、*コンテナー* タイプの **ビットマップ (Image)** フィールドが、**コンテナー** タイプのデータモデル **ロゴ** フィールドにバインドされている様子を示しています。 このバインドにより、**SalesInvoice** ルート定義用に設計され、実行時にこのモデルマッピングを使用する任意の ER フォーマットで会社のロゴを使用できるようになります。

[![ER モデル マッピング デザイナーでのコンテナー タイプのフィールドのバインド。](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>レコード

*レコード* とは、名前の付いたフィールドの集合で、それぞれが、[プリミティブ](er-formula-supported-data-types-primitive.md) データタイプまたはコンポジット データ タイプの値に関連付けられています。 通常、1 つの *レコード* を使用してレコード リストの 1 つのレコードを表します。 この場合、すべての品目は個々のフィールド、メソッド、関係を表します。

 *レコード* の既定値は **空白値** です。

> [!NOTE]
> 空の *レコード* のフィールドの値を取得すると、適切なデータ型の既定の値が返されます。

*レコード* は、次の関数を使用して取得できます。

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

*レコード* 値の変換については、[リストカテゴリーのER関数一覧](er-functions-category-list.md)を参照してください。

## <a name="record-list"></a><a name="record-list"></a>レコード リスト

*レコード* リストは 、その *レコード* タイプの項目の リストです。 通常、 *レコード リスト* は、データベース テーブルから取得されたレコードのリストを表すために使用します。

既定では、*レコード リスト* の レコードは連続してアクセスされます。 特定のレコードにアクセスするために、[INDEX](er-functions-list-index.md) 関数を使用して *整数* インデックスを指定できます。

 *レコード リスト* の既定値は **空白値** です。 [ISEMPTY](er-functions-list-isempty.md) 関数を使用して、*レコード リスト* が空白かどうかを評価できます。

> [!NOTE]
> *レコード リスト* が空白の場合、その中の *レコード* のフィールド値を取得しようとすると、実行時の例外エラーが発生します。 このタイプのランタイム例外エラーの回避方法については、[空のリストケースを考慮する](er-components-inspections.md#i9) を参照してください。

*レコード リスト* は、次の関数を使用して開始できます:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

*レコード リスト* 値の変換については、[リスト カテゴリーの ER 関数一覧](er-functions-category-list.md)を参照してください。 *レコード リスト* の項目アイテムを導入し、そこにアプリケーション データを入力し、そのデータを使ってビジネス ドキュメントを作成する方法については、[カスタム レポートを印刷する新しい ER ソリューションの設計](er-quick-start1-new-solution.md)を参照してください。

## <a name="object"></a><a name="object"></a>オブジェクト

*オブジェクト* は、*クラス* のインスタンスを表します。 通常、*オブジェクト* は、ソース コードで開始されます。 その後、ER モデル マッピングに渡され、実行コンテキストの詳細が提供されます。

*オブジェクト* の既定値は **null 値** です。

次の図は、*オブジェクト* タイプの **ReportDataContract** データ ソースが、ソース コードから **プロジェクト請求書** モデル マッピングに生成された請求書に関する情報を渡すように追加する方法を示しています。 たとえば、請求書インスタンスのテキストは、実行コンテキストの一部として渡されます。 このテキストは、ER データモデルの **注記** フィールド用に設定された `ReportDataContract.parmInvoiceInstanceText` バインドの実行により、ランタイムにソースコードから取得されます。 このバインドは、現在のモデル・マッピングで **ReportDataContract** データ ソースとして表現されている **PSAProjInvoiceContract** アプリケーション・クラスの `parmInvoiceInstanceText()` メソッドを呼び出します。

[![ER モデル マッピング デザイナーでのオブジェクト データ ソースの構成。](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

実行コンテキストの詳細を、ソース コードから実行中の ER ソリューションに渡す方法については、 [設計されたレポートを呼び出すアプリケーション アーティファクトの開発](er-quick-start1-new-solution.md#DevelopCustomCode) を参照してください。

## <a name="additional-resources"></a>追加リソース

- [電子申告の概要](general-electronic-reporting.md)
- [電子報告のフォーミュラ言語](er-formula-language.md)
- [対応しているプリミティブ データ型](er-formula-supported-data-types-primitive.md)
