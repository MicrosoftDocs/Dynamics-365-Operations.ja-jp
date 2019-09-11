---
title: 使用品目
description: このトピックでは、資産管理における品目の使用場所の概要の取得方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918329"
---
# <a name="item-where-used"></a>使用品目

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

特定の品目の計算を行って、資産管理でその品目が使用された場所の概要を取得できます。 結果は、品目が有効期間中に使用されたコンテキストを示します。 **品目の使用場所**ページは、メインの資産管理メニューから開くことができます。また、次のページからもアクセスできます。

[資産 BOM](../objects/object-BOM.md)

[資産タイプの既定の予備部品](../setup-for-objects/object-types.md)

[メンテナンス作業タイプの既定の予測の品目予測](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[作業指示書メンテナンス予測](../work-orders/maintenance-forecasts.md)

[作業指示書購買要求](../work-orders/procurement.md)

[作業指示書の購買](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>品目の使用場所の計算

1. **資産管理** > **照会** > **品目の使用場所**をクリックするか、または前に説明したいずれかのページで**品目の使用場所**ボタンを選択します。

2. **品目の使用場所**ダイアログで、**品目番号**フィールドで計算を実行する品目を選択します。

3. **レベル** フィールドを使用すると、機能の場所に関する品目明細行の詳細度を指定できます。 たとえば、フィールドに「1」という番号を挿入し、複数レベルの機能の場所の構造がある場合、機能の場所に対するすべての品目明細行が最上位レベルに表示されます。 したがって、明細行の関係または数量が下位レベルにある機能の場所から追加される可能性があります。 **レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能の場所レベルのすべての品目明細行を示す詳細結果が表示されます。

4. **含める**セクションで、計算に含めるトグル ボタンで「はい」を選択します。

5. **OK** をクリックして、計算を開始します。

6. **品目の使用場所**タブ > **グループ化**アクション ウィンドウ グループで、関連するボタンを選択すると、計算の必要な詳細レベルが表示されます。 選択したアクション ウィンドウ ボタンが強調表示されます。 ボタンをクリックして、有効または無効にします。

7. 品目に関連する分析コードを表示する場合は、**分析コードの表示**をクリックして、表示する分析コードを選択します。

次の図では、品目番号「1000」の品目の使用場所の計算例を示しています。

![図 1](media/12-controlling-and-reporting.png)

