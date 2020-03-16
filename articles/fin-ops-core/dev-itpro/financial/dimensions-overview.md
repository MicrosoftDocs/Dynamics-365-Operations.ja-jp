---
title: Excel テンプレートへの分析コードの追加
description: このトピックでは、分析コード、エンティティを持つ分析コード、および使用できる分析コード コントロールについて説明します。
author: robinarh
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 11314
ms.assetid: 20e6b97e-30ed-48d4-b63c-a073f80300b2
ms.search.region: Global
ms.author: rbrow
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb90940bb07478f518ff4e8f479d9e89b1889753
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080758"
---
# <a name="add-dimensions-to-excel-templates"></a>Excel テンプレートへの分析コードの追加

[!include [banner](../includes/banner.md)]

このトピックでは、分析コード、エンティティを持つ分析コード、および使用できる分析コード コントロールについて説明します。

インストール後に Microsoft Excel テンプレートに存在する唯一の値は MainAccount です。 これは、すべての顧客が持つ唯一の分析コード です。 Microsoft Excel テンプレートに分析コードを追加するには、次の手順を実行する必要があります。

1.  DimensionCombinationEntity または DimensionSet エンティティに分析コードを追加します。
2.  個々の列に分析コードを配置する各テンプレートに分析コードを追加します。 詳細については、[Excel で開くエクスペリエンスの作成](../office-integration/office-integration-edit-excel.md) を参照してください。
3. [Excel で財務分析コード値の検索機能](add-dimensions-excel-templates.md) を追加します。
3.  テンプレートを公開します。

このトピックでは、DimensionCombinationEntity を変更して Excel の列で分析コードを有効にする方法を示します。 同じ手順を使用して DimensionSet エンティティを変更できます。 

> [!NOTE]
> この情報は、リリースごとに変更されることがあります。 したがって、頻繁に最新の情報を確認してください。

## <a name="add-dimensions-to-dynamics-365-finance"></a>Dynamics 365 Finance への分析コードの追加

2016 年 11 月リリースでは、Visual Studio で OData アドイン用の財務分析コードを追加がリリースされ、**DimensionCombinationEntity** の変更が大幅に簡素化されています。

1. Microsoft Visual Studio で、**Dynamics 365 > アドイン > Odata の財務分析コードの追加**をクリックします。
2. **分析コード名** の列に財務分析コードの名前を入力します。 これは、財務分析コードの正確な名前でなければなりません。 拡張機能を持つ **モデル** を選択します。 これは AppSuite レイヤーの上にする必要があります。 **適用** をクリックします。 

    ![Odata の財務分析コード](media/financial-dimensions-odata.png).

3. プロジェクトをコンパイルし、データベースと同期します。

    ![8](media/8-300x260.png)

4. これで、カスタマイズは完了です。 次のステートメントを使用して、SQL でテストすることができます。

    ```sql
    select * from DIMENSIONCOMBINATIONENTITY 
    ```

## <a name="add-dimensions--before-dynamics-365-for-finance-and-operations"></a>Dynamics 365 for Finance and Operations の前に分析コードを追加します。
たとえば、Microsoft Excel との統合で、列に配置する分析コードとの相互作用をサポートするには、最初にカスタムを使用して分析コードの列を作成する必要があります。 

1. Visual Studio で、アプリケーション エクスプローラーを開きます (**表示**&gt;**アプリケーション エクスプローラー**)。 
2. DimensionCombinationEntity **(AOT** &gt; **データ モデル** &gt; **データ エンティティ**) に移動します。 
3. エンティティを右クリックし、**カスタマイズ** を選択します。 

    [![5](./media/5-300x187.png)](./media/5.png)

4. 変更するエンティティのデザイナー、この例では **DimensionCombinationEntity** を開きます。 
5. **departmentValue** という名前の str を返す新しいプライベート静的メソッドを作成します。 
6. この方法では、**DimensionAttributeValueCombination** から分析コードの値を取得する必要があります。 最終的な方法はこのようになります。

    ```xpp
    /// <summary>
    /// This method returns the value of Department.
    /// </summary>
    private static str departmentValue()
    {     
        Name dimensionName = 'Department';
        str sqlStatement;

        DimensionAttribute dimensionAttribute = DimensionAttribute::findByName(dimensionName);

        if (!dimensionAttribute)
        {
            sqlStatement = SysComputedColumn::returnLiteral('');
        }
        else
        {
            sqlStatement = strFmt('SELECT TOP 1 T1.%1 ', dimensionAttribute.DimensionValueColumnName);
        }

        return sqlStatement;
    }
    ```

7. エンティティに新しい「マップされていない文字列フィールド」を作成します。

   - **名前** プロパティを分析コード名 **部門** に設定します。
   - **拡張データ型** プロパティを **DimensionValue** に設定します。
   - **DataEntityView メソッド** プロパティを、前の手順で作成したメソッドに設定します (たとえば、**departmentValue**)。
   - **ラベル** プロパティを分析コード名 **部門** に設定します。

     [![6](./media/6-300x64.png)](./media/6.png)

8. 分析コードの名前を適切な分析コードに変更することで、追加する分析コードごとに手順 5 ～ 7 を繰り返します。 
9. プロジェクトをコンパイルし、データベースと同期します。 

    [![8](./media/8-300x260.png)](./media/8.png)

10. これで、カスタマイズは完了です。 次のステートメントを使用して、SQL でテストすることができます。

    ```sql
    select * from DIMENSIONCOMBINATIONENTITY
    ```


## <a name="additional-resources"></a>追加リソース

[既定の分析コード コントロールの分析コード エントリ コントロールへの移行](dimension-entry-control-migration.md)

[分析コード エントリ コントロールの取得](dimension-entry-control-uptake.md)

[拡張機能のホーム ページ](../extensibility/extensibility-home-page.md)




