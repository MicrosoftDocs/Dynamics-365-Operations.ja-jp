---
title: 電子申告 (ER) 機能の一覧の拡張
description: この記事では、新しい機能を導入するために完了しなければならない重要なタスクの概要について説明します。
author: NickSelin
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERExpressionDesignerFormula
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58911
ms.assetid: 62c740dc-6a88-4ded-9c41-6857b82b335e
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ad8d29dd5a59bb6be0a6b57b08452aaaf322439
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750120"
---
# <a name="extend-the-list-of-electronic-reporting-er-functions"></a>電子申告 (ER) 関数の一覧の拡張

[!include [banner](../includes/banner.md)]

テキスト、日時、算術、論理、情報、データ型変換、およびその他 (ビジネス ドメインの特定の関数) といったさまざまなタイプの関数がデータ変換のための電子報告式でサポートされています。 組み込み関数に加えて、電子申告により使用可能な関数の一覧を拡張できます。 この記事では、新しい機能を導入するために完了しなければならない重要なタスクの概要について説明します。

アプリケーション コードのすべての電子レポート機能は、**ERExpression** クラスを拡張するクラスとして表示されます。 2 種類の関数が認識されます。

- **引数の数を固定** – これらの関数は、接頭語 **parm** (次のサンプルコードの **parmInput**、**parmStartNum** を参照してください) を持つメソッドを含むクラスで表されます。 引数の順序は、**SysOperationDisplayOrderAttribute** 属性によって設定されます。
- **可変数の引数** – これらの機能は (**ERExpressionGenericCase** クラスを参照してください)**ERIObjectContainer** インターフェイスを実装するクラスで表されます。 追加の **追加** メソッドを使用して関数を受け入れる型を宣言します。

電子申告式の新しい機能を導入するのに推奨されている手順を次に示します。

- 戻り値の型に基づいて関数の基本クラスを選択します (以下のサンプル コードで **ERExpressionString** を参照してください)。

    - 選択したクラスを拡張する新しいクラスを作成します (サンプル コードの **ERExpressionStringMid** を参照してください)。

        - 必須属性を提供:

            - **SysOperationLabelAttribute** – この属性は、関数の名前を定義します。
            - **SysOperationHelpTextAttribute** – この属性は、関数のヘルプ テキストを定義します。
            - **ERComponentGroupAttribute** - この属性は、この機能が属するグループを定義します。 (詳細については、 [電子申告 (ER) のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md) を参照してください。)

        - 引数を提供します。

            - 引数関数の固定番号については、接頭語 **parm** を持つメソッドを提供し、**SysOperationDisplayOrderAttribute** 属性を使用して引数の順序を設定します。
            - 引数関数の変数番号で、**ERIObjectContainer** インターフェイスを実装します。

        - 評価方法を提供します。

次に例を示します。

```xpp
/// <summary>
/// Returns the characters from the middle of a text string, given a starting position and length.
/// </summary>
[
    SysOperationLabelAttribute ('MID'),
    SysOperationHelpTextAttribute ("@ElectronicReporting:ExpressionStringMidHelpText"),
    ERComponentGroupAttribute ("@ElectronicReporting:String")
]
class ERExpressionStringMid extends ERExpressionString
{
    ERExpressionString input;
    ERExpressionInt startNum;
    ERExpressionInt numChars;
    public str evaluateString(ERIDataContext _dataContext)
    {
        return subStr(
            this.parmInput().evaluateString(_dataContext),
            this.parmStartNum().evaluateInt(_dataContext),
            this.parmNumChars().evaluateInt(_dataContext));
    }
    [DataMemberAttribute, SysOperationLabelAttribute ("@ElectronicReporting:Input"), SysOperationDisplayOrderAttribute ("1")]
    public ERExpressionString parmInput(ERExpressionString _input = input)
    {
        input = _input;
        return input;
    }
    [DataMemberAttribute, SysOperationLabelAttribute ("@ElectronicReporting:NumChars"), SysOperationDisplayOrderAttribute ("3")]
    public ERExpressionInt parmNumChars(ERExpressionInt _numChars = numChars)
    {
        numChars = _numChars;
        return numChars;
    }
    [DataMemberAttribute, SysOperationLabelAttribute ("@ElectronicReporting:StartNum"), SysOperationDisplayOrderAttribute ("2")]
    public ERExpressionInt parmStartNum(ERExpressionInt _startNum = startNum)
    {
        startNum = _startNum;
        return startNum;
    }
    public str toString()
    {
        return ERExpressionStringPresenter::namedFunctionToStr(this);
    }
}
```

## <a name="suggested-guidance"></a>推奨されるガイダンス
次のガイダンスは、カスタム電子申告機能の設計を支援することを目的としています。

- 電子レポート式が Excel と同じようにされるため、可能な限り Microsoft Excel の関数名を再利用してください。 この方法で、電子申告のフォーミュラをエンド ユーザーにわかりやすく保持します。
- 電子申告では、プリミティブ データ型のリスト タイプがサポートされません。 したがって、単一の **Value** 項目を持つデータ コンテナー リストを使用することに決めました。
- 新しい関数の一覧の拡張機能を新しいアプリケーションの修正プログラムとしてリリースします。 電子申告デザイナーは、新しいユーザー定義関数を使用する電子申告 コンフィギュレーションの修正プログラム番号を参照します。 このタイプの構成が新しいインスタンスにインポートされるときはいつでも、必要な修正プログラムがインストールされたかどうかが電子申告によって評価され、電子申告構成と、構成がインポートされるバージョンとの間のコンプライアンスを維持します。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[電子申告 (ER) のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]