---
title: モデル管理ライフサイクル
description: この記事では、生成された予測を最適化するために組織の機械学習モデルを管理する方法について説明します。
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
ms.openlocfilehash: 526916929e4bc079f9cea82d8ea9f80813e89b83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880877"
---
# <a name="model-management-lifecycle"></a>モデル管理ライフサイクル

[!include [banner](../includes/banner.md)]

この記事では、生成された予測を最適化するために組織の機械学習モデルを管理する方法について説明します。

AI モデルをサンドボックス環境でトレーニングしてから、マネージド ソリューションを使用して、運用環境に配置することをお勧めします。 この方法によって、モデルのライフサイクルを管理するための適切なコントロールが確実に設定できるようになります。

AI モデルは利用可能な請求書や顧客データに基づいているため、サンドボックス環境には運用データの最新のコピーがあることが重要です。 [顧客支払予測の使用](use-customer-payment-predictions.md) の手順に従ってモデルのトレーニングを開始できます。 モデルが再トレーニングされた後で、[初期の顧客支払予測モデルを評価する](evaluate-payment-prediction.md) の記載に従って結果を評価します。 [予測モデルの改善](improve-model.md) の情報を使用して、モデルの改善に役立つ機能とフィルターの組み合わせを実験します。

トレーニングの結果に問題がなければ、[AI モデルを配布する](/ai-builder/distribute-model) の手順に従って、モデルを運用環境に移行します。
