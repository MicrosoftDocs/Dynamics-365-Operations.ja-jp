---
title: 生産のスケジューリングで安全マージンが考慮されない
description: 生産のスケジューリングでは、ペギングされた供給に対して品目補充で設定されている安全マージンは考慮されません
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476855"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>生産のスケジューリングで安全マージンが考慮されない

## <a name="symptoms"></a>現象

マスター プランでは安全マージンが考慮されます。 ただし、計画製造オーダーのスケジューリング時に安全マージンは無視されます。

## <a name="resolution"></a>解決策

マージンは、マスター プラン中にのみ考慮され、手動のスケジューリングでは考慮されません。 マージンは、計画フェーズでバッファーとして機能するように設計されており、実際のプロセスのために "マージン" を提供します。

目的の結果を得るには、マージンを削除します。 次に、目的の時間 (待ち時間など) を含めるように工順を更新する必要があります。 その後、マスター プランと手動のスケジューリングの両方で同じ結果が生成される必要があります。
