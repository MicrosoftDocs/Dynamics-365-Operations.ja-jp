---
title: 使用品目
description: このトピックでは、資産管理における品目の使用場所の概要の取得方法について説明します。
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2308fc4fabe541b8affeba5860a3154f81e8903e4853fd36d777f15a503d9dd8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752829"
---
# <a name="item-where-used"></a>使用品目

[!include [banner](../../includes/banner.md)]

 

特定の品目の計算を行って、資産管理でその品目が使用された場所の概要を取得できます。 結果は、品目が有効期間中に使用されたコンテキストを示します。 **品目の使用場所** ページは、メインの資産管理メニューから開くことができます。また、次のページからもアクセスできます。

- [資産 BOM](../objects/object-BOM.md)

- [資産タイプの既定の予備部品](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [メンテナンス作業タイプのカテゴリとメンテナンス作業タイプ、メンテナンス作業タイプのバリアント、メンテナンス作業の取引、およびメンテナンス チェックリスト](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [メンテナンス予測](../work-orders/maintenance-forecasts.md)

- [調達](../work-orders/procurement.md)

- [作業指示書の購買](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>品目の使用場所の計算

1. **資産管理** > **照会** > **品目の使用場所** をクリックするか、または前に説明したいずれかのページで **品目の使用場所** ボタンを選択します。

2. **品目の使用場所** ダイアログで、**品目番号** フィールドで計算を実行する品目を選択します。

3. **レベル** フィールドを使用すると、機能の場所に関する品目明細行の詳細度を指定できます。 

    たとえば、フィールドに「1」という番号を挿入し、複数レベルの機能の場所の構造がある場合、機能の場所に対するすべての品目明細行が最上位レベルに表示されます。 したがって、明細行の関係または数量が下位レベルにある機能の場所から追加される可能性があります。 
    
    **レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能の場所レベルのすべての品目明細行を示す詳細結果が表示されます。

4. **含める** セクションで、計算に含めるトグル ボタンで「はい」を選択します。

5. **OK** をクリックして、計算を開始します。

6. **品目の使用場所** タブで、**グループ化** ボタンを選択すると、計算の必要な詳細レベルが表示されます。 選択した **グループ化** ボタンが強調表示されます。 ボタンをクリックして、有効または無効にします。

7. 品目に関連する分析コードを表示する場合は、**分析コードの表示** をクリックして、表示する分析コードを選択します。

## <a name="example"></a>例

次のスクリーンショットでは、品目番号「1000」の品目の使用場所の計算例を示しています。

![品目の使用場所の計算例。](media/12-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]