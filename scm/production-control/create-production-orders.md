---
title: "製造オーダーを作成します"
description: "製造オーダーを作成すると、品目の製造開始が要求されます。 製品オーダーには、生産対象、生産の数量、および予定終了日に関する情報が含まれています。 また、品目を生産するために消費する材料および従うプロセスについての情報が含まれます。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: bcbb07553d990c35057ba32fd56d26fbc9c6f71b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="create-production-orders"></a>製造オーダーを作成します

[!include[banner](../includes/banner.md)]


製造オーダーを作成すると、品目の製造開始が要求されます。 製品オーダーには、生産対象、生産の数量、および予定終了日に関する情報が含まれています。 また、品目を生産するために消費する材料および従うプロセスについての情報が含まれます。

製造オーダーは生産ライフ サイクルの各ステージを通過します。 製造オーダーが作成されると、そのオーダーに [**作成済み**] ステータスが割り当てられます。 製造オーダーが終了すると、そのオーダーに [**終了済**] ステータスが割り当てられます。 各ステージのパラメーター設定によってユーザーは各ステップをコンフィギュレーションすることができます。 この設定は単一のユーザーまたはすべてのユーザーに設定できます。

生産部品表および生産工順は、製造オーダーの主要なエンティティです。 これらは、生産される選択した品目および数量に基づいて製造オーダーにコピーされます。 製造オーダーを開始する前に、生産部品表と工順は編集できます。

製造オーダーは、次のシナリオで作成できます:

-   材料需要に基づいてマスター プランを実行することによって作成されます。
-   販売注文明細行から直接作成する場合、または上位レベルの製造オーダーの作成と見積をする (ペギングされた供給) 場合です。
-   手動で作成します。





