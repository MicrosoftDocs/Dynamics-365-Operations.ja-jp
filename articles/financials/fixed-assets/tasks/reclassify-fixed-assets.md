--- 
title: "固定資産の再分類"
description: "固定資産を再分類するには、その固定資産を新しい固定資産グループに移動するか、同じグループ内でその固定資産に新しい固定資産番号を割り当てる必要があります。"
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: 6bce294329c7ec6dc436c3d3baf6597e0283c9bd
ms.contentlocale: ja-jp
ms.lasthandoff: 10/30/2017

---
# <a name="reclassify-fixed-assets"></a>固定資産の再分類

[!include [task guide banner](../../includes/task-guide-banner.md)]

固定資産を再分類するには、その固定資産を新しい固定資産グループに移動するか、同じグループ内でその固定資産に新しい固定資産番号を割り当てる必要があります。 

固定資産が再分類されるとき:

• 既存の固定資産のすべての価値モデルが新しい固定資産で作成されます。 元の固定資産に対して設定されていたすべての情報が、新しい固定資産にコピーされます。 元の固定資産の価値モデルのステータスは、[クローズ済] になります。 

• 新しい固定資産の価値モデルでは、[取得日付] フィールドに再分類の日付が含まれます。 [減価償却日] フィールドの日付は、元の資産の情報からコピーされます。 減価償却が既に開始されている場合には、[最新減価償却日] フィールドに再分類の日付が表示されます。 

• 元の固定資産の既存の固定資産トランザクションはキャンセルされ、新しい固定資産に対して再生成されます。

1. [固定資産] > [定期処理のタスク] > [再分類] の順に移動します。
2. [固定資産グループ] フィールドで、再分類するグループを選択します。
3. [固定資産番号] フィールドで、再分類する固定資産を選択します。
4. [新しい固定資産グループ] フィールドで、固定資産の転送先のグループを選択します。
    * 新しい固定資産グループが番号順序に関連付けられた場合、[新しい固定資産番号] フィールドが、新しい固定資産グループの番号順序の番号で更新されます。 そうでない場合は、新しい固定資産グループは、[固定資産パラメーター] ページで設定された番号順序の番号で更新されます。 番号順序が[固定資産パラメーター] ページで設定されていない場合は、[新しい固定番号] フィールドに番号を入力します。  
5. [再分類日] フィールドに、日付を入力します。
6. [伝票] フィールドで値を入力または選択します。
7. [OK] をクリックします。


