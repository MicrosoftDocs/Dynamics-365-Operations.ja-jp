---
title: "製造オーダーを作成します"
description: "製造オーダーを作成すると、品目の製造開始が要求されます。 製品オーダーには、生産対象、生産の数量、および予定終了日に関する情報が含まれています。 また、品目を生産するために消費する材料および従うプロセスについての情報が含まれます。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 33d2e4f1a6bc8bc28e43b4c985d9a780a9481e97
ms.lasthandoff: 03/31/2017


---

# <a name="create-production-orders"></a>製造オーダーを作成します

製造オーダーを作成すると、品目の製造開始が要求されます。 製品オーダーには、生産対象、生産の数量、および予定終了日に関する情報が含まれています。 また、品目を生産するために消費する材料および従うプロセスについての情報が含まれます。

製造オーダーは生産ライフ サイクルの各ステージを通過します。 製造オーダーが作成されると、そのオーダーに [**作成済み**] ステータスが割り当てられます。 製造オーダーが終了すると、そのオーダーに [**終了済**] ステータスが割り当てられます。 各ステージのパラメーター設定によってユーザーは各ステップをコンフィギュレーションすることができます。 この設定は単一のユーザーまたはすべてのユーザーに設定できます。

生産部品表および生産工順は、製造オーダーの主要なエンティティです。 これらは、生産される選択した品目および数量に基づいて製造オーダーにコピーされます。 製造オーダーを開始する前に、生産部品表と工順は編集できます。

製造オーダーは、次のシナリオで作成できます:

-   材料需要に基づいてマスター プランを実行することによって作成されます。
-   販売注文明細行から直接作成する場合、または上位レベルの製造オーダーの作成と見積をする (ペギングされた供給) 場合です。
-   手動で作成します。



