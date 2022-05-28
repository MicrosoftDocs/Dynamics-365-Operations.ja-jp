---
title: 予測モデルの改善
description: このトピックでは、予測モデルのパフォーマンスを向上させるために使用できる機能について説明します。
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 96ba1653ea1f9a5ac1037e9ecc7e85c86a6f31c7
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719974"
---
# <a name="improve-the-prediction-model"></a>予測モデルの改善

[!include [banner](../includes/banner.md)]

このトピックでは、予測モデルのパフォーマンスを向上させるために使用できる機能について説明します。 Microsoft Dynamics 365 Finance での **顧客支払予測** ワークスペースのモデルの改善を開始します。 次に、改善手順が AI Builder で完了します。

## <a name="select-historical-outcomes"></a>過去の実績の選択

**期限遵守**、**遅延**、**非常に遅い** の 3 つの結果から、請求書に対して可能な 3 つの結果を最初に選択します。 3 つの結果をすべて選択する必要があります。 いずれかの結果の選択を解除すると、請求書がトレーニング プロセスからフィルターで除外され、予測の精度が低下します。

[![実績を確認します。](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

組織で 2 つの結果しか必要としない場合は、**遅延** と **非常に遅い** のしきい値を 0 (ゼロ) 日に変更します。 このようにして、予測を効果的に、**期限遵守** または **遅延** のバイナリ状態に効果的に折りたたむことができ ます。

## <a name="select-fields"></a>フィールドの選択

モデルに含めるフィールドを選択している場合は、Azure data lakeでデータにマッピングされている Microsoft Dataverse テーブルで使用可能なすべてのフィールドが一覧に含まれていることに注意してください。 一部のフィールドは選択 **しない** でください。 選択されていないフィールドは、次の 3 つのカテゴリのいずれかに分類されます。

- このフィールドは Dataverse テーブルに必要ですが、Data Lake にはこのフィールドのバッキング データがありません。
- このフィールドは ID であるため、機械学習機能に対しては意味を持ちません。
- このフィールドは、予測では使用できない情報を表します。

次のセクションでは、請求書エンティティおよび顧客エンティティに使用できるフィールドと、トレーニング対象として選択 **しない** フィールドを示します。 これらの各フィールドに指定されたカテゴリは、上の一覧のカテゴリを参照します。
 
### <a name="invoice-dataverse-table"></a>請求書 Dataverse テーブル

次の図は、請求書テーブルで使用できるフィールドを示しています。

[![請求書テーブルで使用できるフィールドです。](./media/available-fields.png)](./media/available-fields.png)

次のフィールドは、トレーニング対象として選択しないでください。

- **請求元仕入先** (カテゴリ 2)
- **終了済** (カテゴリ 3) – このフィールドは、(決算された) トレーニングと予測 (決算されていない) の請求書をフィルター処理するために使用されます。
- **名前** (カテゴリ 1)
- **ソース ID** (カテゴリ 2)
- **ソース レコード** (カテゴリ 2)
- **ソース テーブル** (カテゴリ 2)

### <a name="customer-dataverse-table"></a>顧客 Dataverse テーブル

次の図は、顧客テーブルで使用できるフィールドを示しています。

[![顧客テーブルで使用できるフィールドです。](./media/related-entities.png)](./media/related-entities.png)

次のフィールドは、トレーニング対象として選択しないでください。

- **行の固有キー** (カテゴリ 2)

## <a name="filters"></a>フィルター

トレーニングに使用される請求書をフィルター処理するには、請求書または顧客テーブルのフィールドでフィルター規準を設定します。 たとえば、合計が特定の金額以上の請求書のみを含むしきい値を設定できます。 また、特定の顧客グループの顧客に関連付けられている請求書を除外できます。

データのフィルター処理の詳細については、[予測モデルの作成](/ai-builder/prediction-create-model#filter-your-data) を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
