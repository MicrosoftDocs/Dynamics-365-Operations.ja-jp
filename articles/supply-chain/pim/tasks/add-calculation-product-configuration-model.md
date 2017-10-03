--- 
title: "製品コンフィギュレーション モデルへの計算の追加"
description: "この手順は、製品コンフィギュレーション モデルに新しい計算を追加する方法を表示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 9ac2d9bcc316a57941136c248a0c5ff030a1fe49
ms.contentlocale: ja-jp
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>製品コンフィギュレーション モデルへの計算の追加

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順は、製品コンフィギュレーション モデルに新しい計算を追加する方法を表示します。 スピーカーの高さを、白いスピーカーは 10 に、他のすべてのキャビネットの仕上げは 15 に設定するため、「If」 演算子を使用して論理式を作成する方法を表示します。 その手順は、デモ会社 USMF で [ハイエンド スピーカー] コンポーネントを使用します。


## <a name="add-a-calculation"></a>計算の追加

## <a name="create-calculation-expression"></a>計算式の作成
1. [式の編集] をクリックします。
2. [ConstraintBody] フィールドで、「If[CabinetFinish=="White", 10, 15]」を入力します。
3. [検証] をクリックします。
4. [閉じる] をクリックします。
5. [OK] をクリックします。


