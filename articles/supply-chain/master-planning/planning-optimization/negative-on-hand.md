---
title: マイナスの手持在庫数量を使用した計画
description: このトピックでは、計画の最適化を使用する場合のマイナスの手持在庫の処理方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72ed2ba42c6233461743492fe6776f376195ada6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983469"
---
# <a name="planning-with-negative-on-hand-quantities"></a>マイナスの手持在庫数量を使用した計画

[!include [banner](../../includes/banner.md)]

システムによってマイナスの集計手持在庫数量が表示される場合、計画エンジンは過剰な供給を回避するため、数量を 0 (ゼロ) として扱います。 この機能の動作は次のとおりです。

1. 計画の最適化機能では、最下位レベルの補充分析コードの手持在庫数量が集計されます。 (たとえば、*場所* が補充分析コードではない場合、計画の最適化では手持在庫数量が *倉庫* レベルで集計されます。)
1. 最下位レベルの補充分析コードの集計手持在庫数量がマイナスの場合、システムでは手持在庫数量が実際に 0 (ゼロ) であると見なされます。

> [!IMPORTANT]
> 計画システムは、入力データと同じ精度でしか設定できません。 入力データが誤っている場合、マイナスの手持在庫レコードによって、Microsoft Dynamics 365 Supply Chain Management の在庫情報が実際の世界と同期されていないことが示されます。 したがって、計画結果には欠陥があります。 正確な計画の結果を得るには、マイナスの手持在庫数量を表示するレコードの数を最小限にする必要があります。

## <a name="example-1"></a>例 1

倉庫 13 は、次の方法で構成されています。

- **補充コード:** 最小/最大。
- **最小:** 15 個
- **最大:** 25 個。

最下位レベルの補充分析コードは *倉庫* で、次の手持在庫数量は *場所* レベルで記録されます。

- **サイト 1、倉庫 13、場所 1:** 20 個。
- **サイト 1、倉庫 13、場所 2:** &minus;8 個。

したがって、倉庫 13 の集計手持在庫数量は 12 個です。 (= 20 個。 &minus; 8 個)。

この場合、計画エンジンでは 12 個の集計手持数量が使用されます。 倉庫 13 に対して。

結果は 13 個の計画オーダーです。 (= 25 個。 &minus; 12 個) 12 個から倉庫 13 に補充する場合に行います。 25 個へ。

## <a name="example-2"></a>例 2

倉庫 13 は、次の方法で構成されています。

- **補充コード:** 最小/最大。
- **最小:** 15 個。
- **最大:** 25 個。

最下位レベルの補充分析コードは *倉庫* で、次の手持在庫数量は *場所* レベルで記録されます。

- **サイト 1、倉庫 13、場所 1:** 4 個。
- **サイト 1、倉庫 13、場所 2:** &minus;8 個。

したがって、倉庫 13 の集計手持在庫数量は &minus;4 個です。 (= 4 個。 &minus; 8 個)。 つまり、0 (ゼロ) 以下です。

この場合、計画エンジンは、倉庫 13 の手持在庫数量が 0 個であるとみなします。 &minus;4 個の代わりに。

結果は 25 個の計画オーダーです。 (= 25 個。 &minus; 0 個) 0 個から倉庫 13 に補充する場合に行います。 25 個へ。

## <a name="related-resources"></a>関連するリソース

[計画最適化の概要](planning-optimization-overview.md)

[計画最適化の開始](get-started.md)

[計画の最適化フィット分析](planning-optimization-fit-analysis.md)

[計画の履歴と計画ログの表示](plan-history-logs.md)

[計画ジョブのキャンセル](cancel-planning-job.md)
