---
title: Excel テンプレートに財務分析コードの値の検索を追加
description: この記事では、Microsoft Excel テンプレートで分析コード値を検索する機能を追加する方法について説明します。
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.custom: 261064
ms.assetid: f3ab87ab-ee8b-462c-bb6f-4d98e0030513
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 56c931872f53e9164ef9e9add8cf6c4f8f8de692
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866801"
---
# <a name="add-lookup-values-for-financial-dimensions-to-excel-templates"></a>Excel テンプレートに財務分析コードの値の検索を追加

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Excel テンプレートで分析コード値を検索する機能を追加する方法について説明します。

インストール後に Microsoft Excel テンプレートに存在する唯一の値は MainAccount です。 これは、すべての顧客が持つ唯一の分析コード です。 Microsoft Excel テンプレートに分析コードを追加するには、[Excel テンプレートへの分析コードの追加](dimensions-overview.md)の記事の手順を完了する必要があります。 分析コードを追加した後、分析コード値の一覧を検索する機能が必要な場合この記事の手順を完了します。 

> [!NOTE]
> この情報は、リリースごとに変更される可能性がありますので、定期的に最新の情報を確認してください。

1.  Visual Studio で、**DimensionCombinationEntity** または **DimensionSetEntity** を変更したプロジェクトを開きます。
2.  **DimensionCombinationEntity** または **DimensionSetEntity** を右クリックします。 **開く** を選択します。
3.  **関係** を右クリックします。 **新規** を選択して **関係** をクリックします。
4.  **プロパティ** ウィンドウで、次のプロパティを設定します。
    -   **検証** - 番号
    -   **基数** - ZeroMore
    -   **名前** - 部門などの、財務分析コードの名前を入力します。
    -   **関連データ エンティティ** - **名前** フィールドで入力した財務分析コードのエンティティを選択します。 次のテーブルに、財務分析コードと関連するエンティティの一覧を示します。

        | 財務分析コード '値の使用元'     | 関連するエンティティ                            |
        |-------------------------------------------|-------------------------------------------|
        | &lt; カスタム分析コード &gt;                | DimAttributeFinancialTagEntity            |
        | 契約                                | DimAttributeAgreementHeaderExt\_RUEntity  |
        | 銀行口座                             | DimAttributeBankAccountTableEntity        |
        | BusinessUnits                             | DimAttributeOMBusinessUnitEntity          |
        | キャンペーン                                 | DimAttributeSmmCampaignTableEntity        |
        | 現金勘定                             | DimAttributeRCashTable\_RUEntity          |
        | コスト センター                              | DimAttributeOMCostCenterEntity            |
        | 顧客グループ                           | DimAttributeCustGroupEntity               |
        | 顧客                                 | DimAttributeCustTableEntity               |
        | 繰延                                 | DimAttributeRDeferralsTable\_RUEntity     |
        | 部門                               | DimAttributeOMDepartmentEntity            |
        | 経費および所得コード                  | DimAttributeRTax25ProfitTable\_RUEntity   |
        | 経費の目的                          | DimAttributeTrvTravelTxtEntity            |
        | 会計施設                     | DimAttributeFiscalEstablishment\_BREntity |
        | 固定資産グループ                        | DimAttributeAssetGroupEntity              |
        | 固定資産                              | DimAttributeAssetTableEntity              |
        | 固定資産 (ロシア)                     | DimAttributeRAssetTable\_RUEntity         |
        | 資金                                     | DimAttributeLedgerFund\_PSN               |
        | 品目グループ                               | DimAttributeInventItemGroupEntity         |
        | アイテム                                     | DimAttributeInventTableEntity             |
        | 職務                                      | DimAttributeHcmJobEntity                  |
        | 法人                            | DimAttributeCompanyInfoEntity             |
        | POS レジスター                             | DimAttributeRetailTerminalEntity          |
        | 職位                                 | DimAttributeHcmPositionEntity             |
        | プロジェクト契約                         | DimAttributeProjInvoiceTableEntity        |
        | プロジェクト グループ                            | DimAttributeProjGroupEntity               |
        | プロジェクト                                  | DimAttributeProjTableEntity               |
        | 見込顧客                                 | DimAttributeSmmBusRelTableEntity          |
        | リソース グループ                           | DimAttributeWrkCtrResourceGroupEntity     |
        | リソース                                 | DimAttributeWrkCtrTableEntity             |
        | 店舗                                    | DimAttributeRetailStoreEntity             |
        | バリュー ストリーム                             | DimAttributeOMValueStreamEntity           |
        | 仕入先グループ                             | DimAttributeVendGroupEntity               |
        | 仕入先                                   | DimAttributeVendTableEntity               |
        | 作業者                                   | DimAttributeHcmWorkerEntity               |

    -   **関連データ エンティティ カーディナリティ** - **ZeroOne**
    -   **関連データ エンティティ ロール** - "分析コード部門の検索" などの一意の名前を入力します。
    -   **関係タイプ** - **関連**
    -   **ロール** - 分析コード部署などの一意の名前を入力します。

5.  **関係** で、**財務分析コード** の名前を右クリックします。
6.  **新規** を選択して **標準** をクリックします。
7.  プロパティ ウィンドウで、**フィールド** で財務分析コードの名前を選択します。
8.  関連フィールドに **Value** と入力します。 新しいリレーションは、次の例のようになります:
    
    ```xpp
    DimensionCombinationEntity.DimensionIntegration.Department==DimAttributeOMDepartmentEntity.Value
    ```

    ![Visual Studio の関係プロパティ。](./media/lookupwiki.png)

9.  プロジェクトを構築してデータベースと同期します。


## <a name="additional-resources"></a>追加リソース

[Excel テンプレートに財務分析コードの値の検索を追加](add-dimensions-excel-templates.md)

[拡張機能のホーム ページ](../extensibility/extensibility-home-page.md)

[[Excel で開く] エクスペリエンスの作成](../office-integration/office-integration-edit-excel.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
