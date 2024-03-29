---
title: スケジュール済み作業指示書の最大能力負荷の計算
description: この記事では、資産管理でスケジュール済み作業指示書の最大能力負荷を計算する方法について説明します。
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53b147198f6aa9e0254312e5ea48b9ae616a79a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857956"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>スケジュール済み作業指示書の最大能力負荷の計算

[!include [banner](../../includes/banner.md)]

 

スケジュール済み作業指示書の最大能力負荷を計算して、特定の期間に対するリソースの作業負荷の概要を取得できます。 メンテナンス作業者、作業者グループ、ツール、および資産に対して計算を行うことができます。

1. **資産管理** > **照会** > **スケジュール** > **最大能力負荷** をクリックします。

2. **最大能力負荷の計算** ダイアログ > **表示** フィールドで、計算する負荷タイプとして **能力**、**引当済**、または **残余** を選択します。

3. ゼロを含む結果を表示しない場合は、**ゼロをスキップ** トグル ボタンで **はい** を選択します。

4. 該当するトグル ボタンの **作業者**、**メンテナンス作業者グループ**、**ツール**、および **資産** で **はい** を選択して、作業負荷を計算に使用するリソース タイプを選択します。

5. **開始日** フィールドで、計算の開始日を選択します。

6. **間隔のタイプ** フィールドで、計算の間隔として **日**、**週**、**月**、または **四半期** を選択します。

7. **期間頻度** フィールドに、計算する間隔の数を挿入します。 たとえば、**日** を間隔タイプとして選択し、このフィールドに数値 "5" を挿入した場合、開始日から 5 日間の計算が行われます。

8. **OK** をクリックして、計算を開始します。

次の図は、負荷タイプ **引当済** に対する 3 週間の計算の結果を示します。

![図 1。](media/08-work-order-scheduling.png)

[!NOTE]
負荷タイプ **能力** または **剰余** を選択した計算では、選択した期間のリソースに対して引当が行われていない場合、同じ結果が表示されます。

スケジュール済み作業指示書でなく、メンテナンス スケジュール明細行で最大能力負荷を計算する方法についての詳細は、[最大能力負荷の計算](../capacity-planning/calculate-capacity-load.md) を参照してください。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]