---
title: Excel テンプレートへの分析コードの追加
description: このトピックでは、分析コード、エンティティを持つ分析コード、および使用できる分析コード コントロールについて説明します。
author: RyanCCarlson2
ms.date: 03/16/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.custom:
- "11314"
- intro-internal
ms.assetid: 20e6b97e-30ed-48d4-b63c-a073f80300b2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5192157c7f1d664937191d31cbe55e3ef3010b0a
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734415"
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

## <a name="add-dimensions-to-dynamics-365-finance"></a>分析コードを Dynamics 365 Finance に追加

Visual Studio で OData アドイン用の財務分析コードを追加がリリースされ、**DimensionCombinationEntity** の変更が大幅に簡素化されています。

1. Microsoft Visual Studio で、**Dynamics 365 > アドイン > Odata の財務分析コードの追加** をクリックします。
2. **分析コード名** の列に財務分析コードの名前を入力します。 これは、財務分析コードの正確な名前でなければなりません。 拡張機能を持つ **モデル** を選択します。 これは AppSuite レイヤーの上にする必要があります。 **適用** をクリックします。 

    ![Odata の財務分析コード。](media/financial-dimensions-odata.png).

3. プロジェクトをコンパイルし、データベースと同期します。 

    > [!NOTE] 
    > プロジェクトが適切に機能するには、拡張機能名 "DimensionIntegration" を保持する必要があります。

    ![構築および同期するメニュー オプション。](media/8-300x260.png)

4. これで、カスタマイズは完了です。 次のステートメントを使用して、SQL でテストすることができます。

    ```sql
    select * from DIMENSIONCOMBINATIONENTITY 
    ```


## <a name="additional-resources"></a>追加リソース

[既定の分析コード コントロールの分析コード エントリ コントロールへの移行](dimension-entry-control-migration.md)

[分析コード エントリ コントロールの取得](dimension-entry-control-uptake.md)

[拡張機能のホーム ページ](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
