---
title: 重量には正の値を指定してください
description: 重量には正の値を指定してください
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776779"
---
# <a name="weight-must-be-positive"></a>重量には正の値を指定してください

エラー コード: WeightMustBePositive

## <a name="symptoms"></a>現象

システムは次のエラー メッセージを表示します。

> 重量には正の値を指定してください。

## <a name="cause"></a>原因

**総重量** フィールドは *0* (ゼロ) または負の値に設定されています。

## <a name="resolution"></a>解像度

重量を指定するには、次の手順のいずれかに従います。

- **総重量** フィールドで、値を設定します。 その後、ドロップダウン リストで単位を選択します。
- **システム重量を取得** を選択して、**総重量** 値を計算します。
