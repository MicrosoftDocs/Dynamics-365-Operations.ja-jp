---
title: 税エンジンの適用性
description: このトピックでは、税エンジンの適用性について説明します。
author: yijialuan
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, GTE, Applicability
audience: IT Pro
ms.reviewer: roschlom
ms.search.region: India
ms.author: riluan
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 25809059b55d43d23f1c1d27e33a6e56926f88a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988589"
---
# <a name="tax-engine-applicability"></a>税エンジンの適用性

[!include [banner](../includes/banner.md)]

[税エンジン](tax-engine.md) (GTE とも呼ばれます) では、法的要件および業務要件に基づいて、税の適用、計算、転記、および決済を決定する税ルールを設定できます。 このトピックでは GTE が税金の適用性を処理する方法を理解するのに役立つ税エンジン構成について説明します。

> [!NOTE]
> 税エンジン機能は、インドに基本住所がある法人に対してのみ使用可能です。

## <a name="prerequisites"></a>必要条件                                               
このドキュメントでは、インドの商品及びサービス税のコンフィギュレーションを使用して、税の適用について説明します。 詳細については、[インドの商品及びサービス税 (GST) の概要](../localizations/apac-ind-gst.md) を参照してください。

## <a name="overview"></a>概要
税の適用性とは、税タイプ、税コンポーネント、または税率が適用される条件です。 たとえば、インドの GST では、ある州から別の州に商品を販売する場合、IGST を請求する必要があります。販売している商品によって税率が決まります。 税エンジンは 2 種類の方法で、税の適用、ルックアップおよび条件を処理します。 ルックアップは主に動的適用ルールを処理するために使用され、条件は静的適用ルールを処理するために使用されます。

以下の GTE コンポーネントは、税の適用性に関連しています。

|GTE コンポーネント | ルックアップ/条件 | 備考 |
|--------------|------------------|----------|
| 税タイプ | ルックアップ & 条件 |  |
| 税コンポーネント | ルックアップ & 条件 | 税コンポーネントと税タイプの両方に適用性ロジックを含めることができます。 税コンポーネントは税タイプに属しているため、特定の税コンポーネントが適用可能かどうかを判断するために適用性ロジックが使用されます。 |
| 税措置 | ルックアップ | 測定タイプは、**税率**、**割合**、または **割合グループ** である必要があります。 |
| 式 | 条件 | 特定のトランザクション タイプに対して、すべての税計算式が関連するわけではありません。 たとえば、非控除税額の計算に使用される式は、ドキュメントの購入にのみ関連しています。 |
| 転記 | 条件 | 異なるトランザクション タイプには、異なる転記ロジックがあります。 この場合、条件を使用して正しい転記プロファイルが使用されていることを確認します。 | 
| 会計 | ルックアップ | 会計は税勘定と同じです。 ルックアップを使用すると、さまざまなシナリオに応じてさまざまな税勘定セットを管理できます。 たとえば、税務登録番号が異なれば、税勘定も異なります。 |
| クレジット プール | ルックアップ | ルックアップを使用して税の決済方法を決定します。 たとえば、さまざまな税務登録番号に基づいて税を決済できます。 |
| 税期間 | ルックアップ | ルックアップを使用して、さまざまなシナリオに使用する税の期間を決定します。 |


## <a name="condition"></a>条件
適用ルールが常に静的な場合は、条件を使用する必要があります。 たとえば、GST はインドの州内在庫移動には適用されません。  

**デザイナー** ボタンをクリックして税 (インドの GST) を開きます。 

![CGST 条件](media/gte-tax-document-applicability-cgst.png)

CGST、税コンポーネント CGST を選択し、鉛筆アイコンをクリックして、詳細な条件をチェックします。 

![CGST 条件の詳細](media/gte-tax-document-applicability-cgst-condition.png)

条件は、実際には、[電子申告](../../dev-itpro/analytics/general-electronic-reporting.md) 式です。 これは **データ ソース** の左側のフィールドと右側の **関数** で構成されています。 サポートされている機能の一覧については、[電子申告 (ER) のフォーミュラ デザイナー](../../dev-itpro/analytics/general-electronic-reporting-formula-designer.md) を参照してください。 

次の条件は、*課税対象文書のタイプ* を「在庫転送オーダー受信」、「在庫転送オーダー出荷」、または「在庫転送オーダー」にすることはできないことを意味します。 つまり HSN コードまたは SAC のいずれかを指定する必要があります。

```sql
AND(Header.'Taxable Document Type'<>"Invent transfer order receive",
    Header.'Taxable Document Type'<>"Invent transfer order shipment",
    Header.'Taxable Document Type'<>"Invent transfer order", 
    OR(NOT(Header.Lines.'HSN Code'=""), NOT(Header.Lines.SAC=""))
   )
```

### <a name="enable-gst-for-intra-state-inventory-transfer-order"></a>州内在庫移動オーダーに対して GST を有効にする
このシナリオでは、GST 登録番号が出荷元と出荷先の倉庫間で異なる場合、インド政府が州内在庫移動オーダーの GST の計算を要求するとします。 

#### <a name="structure-of-the-data-source-in-the-formula-designer"></a>フォーミュラ デザイナーのデータソースの構造
フォーミュラ デザイナーの左端には、課税対象文書と税務書類に定義されているすべてのフィールドと、課税対象文書に定義されている参照モデルがあります。

```Text
Header
└───Header fields
└───Lines
|   └───Lines field
|       └───Tax types
|           └───Tax components
|               └───Tax measures
Reference models
```

#### <a name="change-the-applicability-condition"></a>適用条件を変更する
適用条件を変更するには **ヘッダー > 明細行 > GST 登録番号** および **ヘッダー > 明細行 > パーティ GST 登録番号** の順に移動します。 これらは、倉庫からの出荷および倉庫への出荷の GST 登録番号を表します。 条件は以下のように変更できます。

```Text
AND(
    OR(
       AND(
           OR(
              Header.'Taxable Document Type'="Invent transfer order receive",
              Header.'Taxable Document Type'="Invent transfer order shipment",
              Header.'Taxable Document Type'="Invent transfer order"
             ),
             'GST Registration Number'<>'Party GST Registration Number'
           ),
       AND(
           Header.'Taxable Document Type'<>"Invent transfer order receive",
           Header.'Taxable Document Type'<>"Invent transfer order shipment",
           Header.'Taxable Document Type'<>"Invent transfer order"
          )
      ), 
    OR(NOT(Header.Lines.'HSN Code'=""), NOT(Header.Lines.SAC=""))
   )
```

データ ソースからフィールドを選択し、**データ ソースの追加** を使用して、式にフィールドを追加します。 「課税対象文書のタイプ」のように、名前に空白がある場合は、データ ソース フィールドの単一引用符を使用してください。 「在庫移動オーダー」のように空白がある場合は、値に対して二重引用符を使用します。

編集が完了した後に、**テスト** をクリックして式をテストします。

## <a name="lookup"></a>ルックアップ
静的適用ルールが複雑な場合、または動的適用ルールである場合は、ルックアップを使用する必要があります。

### <a name="lookup-for-static-applicability-rules"></a>静的適用ルールのルックアップ
**GST** を選択して、**ルックアップ** をクリックします。

![CGST 条件](media/gte-tax-document-applicability-static-lookups.png)

ルックアップは静的適用ルールと動的適用ルールの両方を処理できるので、**ソース タイプ** ドロップダウンリストはこの目的のためにあります。 静的適用ルールには **コンフィギュレーション** を使用します。これは、ルックアップで使用されるデータがコンフィギュレーションから取得されることを意味します。 動的適用ルールには **ユーザー データ** を使用します。これは、ルックアップに使用されるデータがランタイム環境から取得されることを意味します。

ルックアップはマトリックスです。 各行の関係は *OR* で、行内の各列の関係は *AND* です。 セルの値が空の場合は、すべての値が条件を満たすことを意味します。 

上のスクリーンショットでは、税タイプ GST のルックアップのためのすべてのデータはコンフィギュレーションから来ているので、**ソース タイプ** は **コンフィギュレーション** です。

GST のルックアップを条件に変換する場合は次のように表示されます。

```Text 
OR(
    AND(Exempt=Exempt.No,
        AND('Tax Direction' = "Sales tax receivable",
            'GST Composition Scheme' = NoYes.No,
            'Party GST Registration Number' <> ""
        ),
        AND('Tax Direction' = "Sales tax payable",
            'Export Order' = NoYes.No,
            'GST Registration Number' <> ""
        ),
        AND('Tax Direction' = "Sales tax receivable",
            'GST Composition Scheme' = NoYes.No,
            'GST Registration Number' <> ""
        )
    )
)
```

### <a name="lookup-for-dynamic-applicability-rules"></a>動的適用ルールのルックアップ
多くの適用ルールは、ランタイム データに依存します。 たとえば、一部の税コンポーネントは特定の商品またはサービスにのみ適用されるため、税務取引の種類が異なると税率も異なります。 

**CESS** を選択して、**ルックアップ** をクリックします。

インドでは、CESS は、特定の商品やサービスに適用されます。 Dynamics 365 Finance では、HSN は商品を表し、SAC はサービスを表すため、ルックアップでは HSN コードと SAC が使用されます。 HSN コードと SAC の実際の価は Finance から取得されるため、**ソース タイプ** は **ユーザー データ** です。

ここでは、CGST レートを決定する方法を確認しましょう。 **CGST > レート** の順に選択し、**ルックアップ** をクリックします。

![CGST、レート、ルックアップの選択](media/gte-tax-document-applicability-dynamic-lookups.png)

ランタイム データは税率を決定するために必要なので、システムは **ソース タイプ** と **ユーザー データ** の値を隠します。

商品やサービスが異なれば税率が異なるため、**HSN コード** および **SAC** があります。 **パーティ GST 登録番号** および **税提示方法** は、GST 未登録の仕入先から購入するシナリオを処理するために使用されます。 **トランザクション開始日** および **トランザクション終了日** は、期間ごとに異なる税率を処理するために使用されます。

### <a name="enable-different-tax-rate-for-different-goods"></a>商品ごとに異なる税率を有効にする
異なる商品が 1 つの HSN コードを共有できるため、ルックアップでこのシナリオを満たすことはできません。 これに対応するには、別のルックアップ列が必要です。

**列** をクリックします。 左側に **使用可能な列** がすべてあります。 構造は、参照モデルがないことを除けば、フォーミュラ デザイナーの **データ ソース** と同じです。

![ルックアップ列](media/gte-tax-document-applicability-change-lookups.png)

**使用可能な列** で **品目 ID** を選択し、商品を一意に決定します。 右矢印アイコンをクリックして、**選択された列** 側に追加します。 HSN が不要な場合は、**選択された列** で **HSN コード** を選択し、左矢印アイコンをクリックして削除できます。 
