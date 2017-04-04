---
title: "減価償却方法"
description: "この記事は、Microsoft Dynamics AX にサポートされた減価償却方法および減価償却方式の概要を提供します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 51c053e6c130d20258e02284d097431a18bb38cb
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-methods-and-conventions"></a>減価償却方法

この記事は、Microsoft Dynamics AX にサポートされた減価償却方法および減価償却方式の概要を提供します。

さまざまな減価償却方法を選択できます。 減価償却方法の目的は、固定資産の減価償却が可能な値を各会計年度期間に配賦することです。 固定資産の減価償却が可能な値は、取得価格から仕損価格 (存在する場合) を差し引いた値です。 

減価償却法を使用している場合、ある資産の最後の減価償却日を変更すると、一部の減価償却がスキップされ、最終年度の減価償却が予定よりも多くなったり少なくなったりすることがあります。 減価償却は、最後の減価償却日の変更によって影響される減価償却期間の数で調整されます。

たとえば、[半年] の減価償却方法を 3 年以上採用している場合、通常は 3 年半にわたって減価償却が行われます。 この 3 年半の間に最後の減価償却日を変更すると、その変更の影響を受ける期間の数だけ最終年度の減価償却が移動します。 最後の減価償却日を 3 か月先送りした場合、通常であれば 6 か月分である最終年度の減価償却が 9 か月分になります。

次のいずれかの減価償却方法を選択できます。


-   半年
-   全月
-   四半期の期中
-   月中 (月の 1 日)
-   月中 (月の 15 日)
-   半年 (開始年)
-   半年 (来年)

減価償却方法は次の中から選択できます。
-   定額法耐用年数
-   逓減残高
-   マニュアル
-   係数
-   消耗
-   定額法残余耐用年数
-   200% 逓減残高
-   175% 逓減残高
-   150% 逓減残高
-   125% 逓減残高

 



<a name="see-also"></a>参照
--------

[Fixed asset depreciation](fixed-asset-depreciation.md)

[Straight line service life depreciation](Straight-line-service-life-depreciation.md)

[Reducing balance depreciation](reduce-balance-depreciation.md)

[Manual depreciation](manual-depreciation.md)

[Factor depreciation](factor-depreciation.md)

[Consumption depreciation](consumption-depreciation.md)

[Straight line life remaining depreciation](straight-line-life-remaining-depreciation.md)

[逓減残高による減価償却125日] (125パーセント減らdepreciation.md残高) 

[逓減残高による減価償却150日] (150パーセント減らdepreciation.md残高) 

[逓減残高による減価償却175日] (175パーセント減らdepreciation.md残高) 

[200 percent reducing balance depreciation](200-percent-reducing-balance-depreciation.md)


