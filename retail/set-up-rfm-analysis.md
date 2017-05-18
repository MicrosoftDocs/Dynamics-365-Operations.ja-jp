---
title: "RFM 分析の設定"
description: "このトピックでは、顧客の Recency、頻度、および金融 (RFM) 分析の設定方法について説明します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: b6f49413d6226a37e16a30a8f68095211faa6d3d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-rfm-analysis"></a>RFM 分析の設定

[!include[banner](includes/banner.md)]


このトピックでは、顧客の Recency、頻度、および金融 (RFM) 分析の設定方法について説明します。

最新、頻度、金融 (RFM) 分析は、顧客の購買で生成されるデータを評価する際に組織が使用できるマーケティング手段です。 RFM 分析を設定すると、顧客が購買をしたとき、計算された RFM スコアが顧客に割り当てられます。 RFM スコアは、組織が RFM 分析をコンフィギュレーションした方法に基づいた、3 桁の評価か、または合計値です。 組織でスコアに 3 桁の評価を使用する場合、最初の桁は、顧客の recency の評価です (どれほど最近に顧客が組織から購買したか)。 2 番目の桁は、顧客が購買を行う頻度の評価です (組織からの顧客の購買の頻度)。 3 番目の桁は、顧客の金額の評価です (組織から購買を行うときに顧客が費やす金額)。 たとえば、1 から 5 のスケールで 5 が最も高い評価で、評価を設定します。 この場合、535 の顧客の評価は、顧客に関する次の情報を示します:

-   **Recency 評価 5** - 顧客は最近購買をしました。
-   **頻度評価 3** - 顧客が中程度の頻度で組織から製品を購入します。
-   **金額評価 5** - 顧客が購買を行うとき、かなりの金額を使用します。

組織がこれらの数の合計を使用する場合は、スコアとして、個別の評価が合計されます。 同じ例では、顧客の評価は 13 です (5 + 3 + 5)。




