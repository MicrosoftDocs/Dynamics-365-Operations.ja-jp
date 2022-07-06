---
title: 拡張機能を通じた新しい在庫分析コードの追加
description: この記事では、拡張機能を通じて新しい在庫分析コードを追加する方法について説明します。
author: MichaelFruergaardPontoppidan
ms.date: 02/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 3397e096c3f0f99219905e6c8eb9bd1d4ca402dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866858"
---
# <a name="add-new-inventory-dimensions-through-extension"></a>拡張機能を通じた新しい在庫分析コードの追加

[!include [banner](../includes/banner.md)]

この記事では、拡張機能を使用して新しい在庫分析コードを追加する方法の概要を示します。 また、実際の実装を含むサンプル アプリケーションへのアクセス方法に関する情報も含まれます。

## <a name="solution-overview"></a>ソリューションの概要
このソリューションで重要なことは、複数のロールが、拡張機能を介して新しい在庫分析コードを追加するライフサイクルに参加することです。 次の説明では、このソリューションを簡略化して一般化していますが、現実にはロールの重複があり、時には同じ人が複数のロールを果たす場合もあります。

### <a name="microsofts-role"></a>Microsoft のロール
Microsoft は、使用されていない分析コード フィールドの限定的なセットを提供します。

15 の既存の分析コードに加えて、Microsoft は 10 の一般的な分析コードをサポートします。 
- 8 つの文字列ベース
- リアルベース 1 つ
- utcdatetime ベース 1 つ
 
これにより、標準アプリケーションのインベントリ ディメンションの合計数が 25 になります。

- 5 製品分析コード: 色、サイズ、スタイル、コンフィギュレーションおよびバージョン
- 5 つの追跡用分析コード: シリアル、バッチ、所有者、プロファイル (ロシアのみ)、および GTD (ロシアのみ)
- 6. 保管分析コード: サイト、倉庫、場所、ステータス、ライセンス プレートおよびパレット (アップグレードと移行のみ)
- 12 個の未割り当ての一般的な分析コード: InventDimension1 から InventDimension12

Microsoft は、物理スキーマを提供しています。

### <a name="isv-role"></a>ISV 役割
ISV は、新規在庫分析コードを追加します。 ISV ソリューションは、分析コードの特定のすべての機能を提供します。強力な種類で、管理、テストしやすく、パフォーマンスの高いものでなければなりません。 さらに、ソリューションは、その他の ISV のソリューションに依存しないようにする必要があります。
ISV は、物理スキーマを直接参照せず、シームレスに行うことができる間接参照を通過するソリューションを構築します。 

ISV は、論理実装を提供します。

### <a name="var-role"></a>VAR ロール
VAR は、完全に機能するシステムを顧客に出荷できる必要があります。 システムには、複数の ISV のソリューションを含めることができます。それぞれに新しい在庫分析コードが含まれる可能性があります。 合計で最大 10 個の ISV 分析コード フィールドがサポートされます。

VAR により、物理的データ モデルと論理的実装が結合されます。

## <a name="details"></a>細目
ソリューションの前半はシンプルです。 新しいクラス階層が導入されています。 それぞれの新しい分析コードは、InventProductDimension または InventTrackingDimension のいずれかから派生する新しいクラスに実装する必要があります。 現在、保管分析コードのサポートがされていません。 これを使用すると、ISV は InventDim テーブルのロジックを変更せずに新しい分析コードを導入することができます。 

![InventDimensionClassHierarchy.](media/InventDimensions1.png)

厳密に型指定された新しい分析コードを参照するために、ISV では InventDim テーブルにテーブル拡張クラスが導入されました。 スタイル、色、サイズの拡張クラスをテンプレートとして使用できます。
 
**例: InventDimStyle_Extension** 

```xpp
/// <summary>
/// The <c>InventDimStyle_Extension</c> class extends the <c>InventDim</c> table with behavior for the style dimension.
/// </summary>
[ExtensionOf(tableStr(InventDim))]
final class InventDimStyle_Extension
{
    public EcoResItemStyleName parmInventStyleId(EcoResItemStyleName _style = this.getValueForDimension(classStr(InventProductDimensionStyle)))
    {
        if (!prmIsDefault(_style))
        {
            this.setValueForDimension(classStr(InventProductDimensionStyle), _style);
        }
        return _style;
    }

    /// <summary>
    /// Returns the field id for the style dimension.
    /// </summary>
    /// <returns>The field id.</returns>
    public static FieldId fieldIdStyle()
    {
        return InventDim::fieldIdForDimension(classStr(InventProductDimensionStyle));
    }
}
```

分析コードは、次のように参照することができます。

```xpp
//Setting a value
inventDim.parmISVDim("Some value");

//Select statements
select inventDim
    where inventDim.(InventDim::fieldIdISVDim()) == "Some value";
```

ISV は、新しい在庫分析コードの分析コード値のリストを保持するために、データ モデルおよびユーザー インターフェイスなどのロジックを構築できるようになりました。

ソリューションの後半はデータ モデルです。 標準アプリケーションには、新しい分析コードごとに次の内容が含まれます。
- ラベル ファイル。
- コンフィギュレーション キー。
- 2 つの拡張データ型 (EDT) (InventDim のフィールド用と InventDimParm のフラグ用) です。
- InventDim テーブルの 1 つのフィールドです。
- InventDimParm テーブルの 1 つのフィールドです。
- InventDimFieldMap マップの 1 つのフィールドと、各テーブルの 1 つのフィールド (約 30) がマップされています。

VAR の職務は、特定の顧客の InventDim の分析コード フィールドに ISV ソリューションを書き込むことです。 この作業を最小にするために、現在以下が含まれています。
- バインディング マッピングを実装します。 これは、メソッド InventDimFieldBinding.className2FieldName() メソッドを拡張するよって行います。
- コンフィギュレーション キーを有効にします。
- 右側の文字列のサイズを指定するには、EDT を拡張します。
- ISV 製ラベルを正しいラベル ファイルにコピーするなど、ラベル ファイルを拡張します。
- InventDim の ProductDimensions または TrackingDimensions フィールド グループおよび分析コードのタイプに応じていくつかの他のテーブルを拡張します。
- 関係およびインデックスを必要に応じて、InventDim で拡張します。

![InventDimensionISVVARExtensions.](media/InventDimensions4.png)

## <a name="known-issues"></a>既知の問題

ソリューションの設計に影響を与えるいくつかの技術的な制限があります。 最も重要なのは、InventDim のWhere 句を含むアプリケーション全体の SQL 文です。 これらのほとんどはマクロを使用して実装され、SQL ステートメントが拡張可能ではないという事実を変更しません。 SQL ステートメントの多くは書き換えることができ、クエリ オブジェクトを使用して拡張できますが、多くの delete_from および update_recordset は残ります。 実行可能なソリューションは、新しい分析コードを追加するときに、これらの SQL ステートメントへの変更を要求することはできません。

もう 1 つの技術的な制限は、サポートできる在庫分析コードの量です。 それぞれが小さなオーバーヘッドを追加し、InventDimFixed EDT は上限を 32 に設定します。 この EDT には各分析コードのビットマスクが含まれており、EDT は整数であるため制限は 32 です。 指定されたソリューションは 32 の制限内で保持されます。 将来に必要になる場合、InventDimFixed を Int64、コンテナーに変更するまたは削除することができます。

## <a name="sample-application"></a>サンプル アプリケーション

「製品フレーバーの分析コード サンプル アプリケーション」と呼ばれるサンプル アプリケーションは、[GitHub](https://github.com/Microsoft/Product-flavor-dimension-sample-app) で見つけることができます。 

この例は 3 つのモデルで構成されています。 
 - ISV の生産コード
 - ISV テスト コード
 - VAR 統合コード
 
これらのモデルを組み合わせると、新しい在庫分析コードを実装するための出発点となります。 サンプル アプリケーションでは、Flavor という新しい製品ディメンションが導入されています。 

アプリケーションでは、さまざまなフレーバーの品目の製造、購入、販売などの多くのエンド ツー エンドのビジネス シナリオがサポートされています。

必要な場合は、問題を GitHub に直接記録し、追加の補充を提供するサンプル アプリケーションへ自由に投稿してください。
 
![InventDimensionFlavorScreenshot.](media/InventDimensions5.jpg)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]