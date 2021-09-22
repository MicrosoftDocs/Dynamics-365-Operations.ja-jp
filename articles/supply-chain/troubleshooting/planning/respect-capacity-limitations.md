---
title: マスター プランでは、利用可能なキャパシティを超えてスケジューリングを行う
description: マスター プランでは、キャパシティ制限を考慮せず、利用可能なキャパシティを超えてスケジューリングしています
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
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476890"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>マスター プランでは、利用可能なキャパシティを超えてスケジューリングを行う

## <a name="symptoms"></a>現象

マスター プランがキャパシティ制限を考慮していないように見え、利用可能なキャパシティを超えてスケジューリングしています。

有限キャパシティを持つ工程スケジューリングを使用していて、工順がリソース グループと個々のリソースの両方で混在する要件を指定している場合は、アルゴリズムがキャパシティ競合を検証する方法のため、予約超過の可能性が小さくなります。 この予約超過は、ヘルパーを使用してマスター プランを実行するときに発生する可能性があります。 実行時間が比較的短いジョブが多数存在する場合に、この問題が発生する可能性が最も高くなります。

## <a name="resolution"></a>解決策

工程のスケジューリングに対して予約超過を行わないことが必須である場合、**マスター プラン パラメーター** ページで **工程のスケジューリングの正確な有限キャパシティ** オプションをオンにして、マスター プランのスケジューリングの一部を行うことができます。 このオプションは、既定では使用できません。 この機能は、パーソナル化機能を使用してページに手動で追加する必要があります。 このオプションを使用すると、並列処理が行われないため、スケジューリングの実行速度が遅くなります。
