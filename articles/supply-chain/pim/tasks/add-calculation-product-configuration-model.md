---
title: 製品コンフィギュレーション モデルへの計算の追加
description: この手順は、製品コンフィギュレーション モデルに新しい計算を追加する方法を表示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb753878a3ce8c29e2a7e7e90e1d6cf6d56c0358d16e3173253ae729cb123502
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731820"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>製品コンフィギュレーション モデルへの計算の追加

[!include [banner](../../includes/banner.md)]

この手順は、製品コンフィギュレーション モデルに新しい計算を追加する方法を表示します。 スピーカーの高さを、白いスピーカーは 10 に、他のすべてのキャビネットの仕上げは 15 に設定するため、「If」 演算子を使用して論理式を作成する方法を表示します。 その手順は、デモ会社 USMF で [ハイエンド スピーカー] コンポーネントを使用します。


## <a name="add-a-calculation"></a>計算の追加

## <a name="create-calculation-expression"></a>計算式の作成
1. [式の編集] をクリックします。
2. ConstraintBody フィールドで、「If[CabinetFinish=="White", 10, 15]」を入力します。
3. [検証] をクリックします。
4. [閉じる] をクリックします。
5. [OK] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]