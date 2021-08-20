---
title: 販売価格の選択基準の作成
description: この手順では、属性ベースの販売価格モデルに対して販売価格の選択基準を作成する方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47ea7ea2093c540a88d9fd7249b470009c7595d40e2a727d8fcd3bb4b5d74bac
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750079"
---
# <a name="create-sales-price-selection-criteria"></a>販売価格の選択基準の作成

[!include [banner](../../includes/banner.md)]

この手順では、属性ベースの販売価格モデルに対して販売価格の選択基準を作成する方法を示します。 この手順では、少なくとも 1 つの販売価格モデルが必要です。 この例では、デモ データの会社 USMF でスピーカー ソリューションの販売価格モデルに対して価格モデルを使用します。 通常、製品マネージャーがこの手順を使用します。

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>既存の販売価格モデルへの新しい条件の追加

1. **製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。
1. 一覧で、モデル名のリンクを選択せずに、スピーカー ソリューション製品モデルの行を選択します。
1. アクション ウィンドウで、**モデル** を選択します。
1. **価格モデル基準** を選択します。
1. **新規** を選択します。
1. **名前** フィールドに 「顧客グループ 10」 と入力します。
    * 価格モデル基準の名前を使用すると、基礎の選択基準を特定する場合に役立ちます。  
1. **価格モデル** フィールドで値を入力または選択します。
1. **注文タイプ** フィールドで *販売注文* を選択します。
    * 注文タイプで、選択クエリで使用できるデータベース フィールドが決まります。  
1. **発効日** フィールドに日付を入力します。
1. **有効期限** フィールドに、日付を入力します。
1. **保存** を選択します。

## <a name="create-the-query-for-the-selection-criteria"></a>選択基準のクエリの作成

1. **編集** を選択します。
2. **テーブル** フィールドで、*顧客* を選択します。
3. **フィールド** フィールドで、*顧客グループ* を選択します。
    * この例では、選択基準に特定の顧客グループを使用します。  
4. **基準** フィールドで、*顧客グループ 10* を選択します。
5. **OK** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]