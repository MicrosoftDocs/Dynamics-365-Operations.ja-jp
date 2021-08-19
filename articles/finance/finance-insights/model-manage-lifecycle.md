---
title: モデル管理ライフサイクル (プレビュー)
description: このトピックでは、生成された予測を最適化するために組織の機械学習モデルを管理する方法について説明します。
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 3daec03b7ba349d8f72863317e2d601a83417d58
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638395"
---
# <a name="model-management-lifecycle-preview"></a>モデル管理ライフサイクル (プレビュー)

[!include [banner](../includes/banner.md)]

このトピックでは、生成された予測を最適化するために組織の機械学習モデルを管理する方法について説明します。

AI モデルをサンドボックス環境でトレーニングしてから、マネージド ソリューションを使用して、運用環境に配置することをお勧めします。 この方法によって、モデルのライフサイクルを管理するための適切なコントロールが確実に設定できるようになります。

AI モデルは利用可能な請求書や顧客データに基づいているため、サンドボックス環境には生産データの最新のコピーがあることが重要です。 [顧客支払予測の使用](use-customer-payment-predictions.md) の手順に従ってモデルのトレーニングを開始できます。 モデルが再トレーニングされた後で、[初期の顧客支払予測モデルを評価する](evaluate-payment-prediction.md) の記載に従って結果を評価します。 [予測モデルの改善](improve-model.md) の情報を使用して、モデルの改善に役立つ機能とフィルターの組み合わせを実験します。

トレーニングの結果に問題がなければ、[AI モデルを配布する](https://docs.microsoft.com/ai-builder/distribute-model) の手順に従って、モデルを運用環境に移行します。