---
title: ハブ連結を使用した積荷計画の概要
description: この記事では、同じ顧客に別の倉庫からの商品を配送する場合、または同じ倉庫に複数の仕入先から商品が配送された場合に、1 つのハブに出荷を統合する機能について説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d61527113746e76889d097e963f70ced24fd241
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432356"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>ハブ連結を使用した積荷計画の概要

[!include [banner](../includes/banner.md)]

この記事では、同じ顧客に別の倉庫からの商品を配送する場合、または同じ倉庫に複数の仕入先から商品が配送された場合に、1 つのハブに出荷を統合する機能について説明します。

同じ顧客に別の倉庫からの商品を配送する場合、または同じ倉庫に複数の仕入先から製品が配送された場合に、1 つのハブに出荷を統合するために役立ちます。

## <a name="building-loads"></a>積荷構築
ハブの統合を使用する前に、**輸送管理パラメーター** ページの **輸送計画中** オプションを有効化する必要があります。 統合が行われるハブを作成する必要もあります。 次の図は、ハブの統合の例を示します。 この例では、異なる倉庫からの販売注文が同じお客様に配送されます。 **積荷計画ワークベンチ** ページを使用して、通常の方法で販売注文に基づいて基本的な積荷が作成されます。 顧客に配送される前に 1 つのハブにある 2 つの積荷を統合するため、**積荷計画ワークベンチ** ページの **輸送** フィールドで、**ハブの連結** を選択します。 各積荷に対して適切なハブを選択すると、「配送先」の行先としてのハブが積荷に割り当てられます。 **積荷計画ワークベンチ** ページの **供給と需要** セクションには、2 つの「輸送要求明細行」もあります。 次にこれらの 2 つの明細行を新しい積荷に追加します。 この新しい積荷には、両方の販売注文明細行があり、「集荷先」の住所としてのハブ、「配送」先としての顧客 A もあります。 次に 3 つの積荷の配送準備が完了し、他の積荷と同様にルーティングされます。 各積荷に対する、出荷配送業者のシステム提案の選択もできます。 [![ハブの連結](./media/hubconsol.jpg)](./media/hubconsol.jpg) 複数の移動オーダーに対して積荷を統合するために、同一の方法を使用することもできます。 この例では、前の図での顧客 A は、倉庫です。 または、積荷を複数の発注書に統合できます。それにより同じ倉庫に異なるベンダーから積荷が配送されます。 複数の統合ハブを作成することが可能で、異なる倉庫から複数の積荷を複数のハブに統合できます。 基本的な積荷を構築し、ハブの統合オプションを使用した後に、統合輸送要求明細行を使用して、新しい積荷を構築します。 次に積荷をレートおよびルートします。



