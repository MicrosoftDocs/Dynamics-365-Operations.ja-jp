---
title: 製造オーダーのライフサイクルの概要
description: 製造オーダーを作成すると、品目の製造開始が要求されます。 製品オーダーには、生産対象、生産の数量、および予定終了日に関する情報が含まれています。 また、品目を生産するために消費する材料および従うプロセスについての情報が含まれます。
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80031737ab0d0c4ab1e4dbd5646ad91f1a010cd5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432108"
---
# <a name="production-order-lifecycle-overview"></a>製造オーダーのライフサイクルの概要

[!include [banner](../includes/banner.md)]

製造オーダーを作成すると、品目の製造開始が要求されます。 製品オーダーには、生産対象、生産の数量、および予定終了日に関する情報が含まれています。 また、品目を生産するために消費する材料および従うプロセスについての情報が含まれます。

製造オーダーは生産ライフ サイクルの各ステージを通過します。 製造オーダーが作成されると、そのオーダーに **作成済み** ステータスが割り当てられます。 製造オーダーが終了すると、そのオーダーに **終了済** ステータスが割り当てられます。 各ステージのパラメーター設定によってユーザーは各ステップをコンフィギュレーションすることができます。 この設定は単一のユーザーまたはすべてのユーザーに設定できます。

生産部品表および生産工順は、製造オーダーの主要なエンティティです。 これらは、生産される選択した品目および数量に基づいて製造オーダーにコピーされます。 製造オーダーを開始する前に、生産部品表と工順は編集できます。

製造オーダーは、次のシナリオで作成できます:

-   材料需要に基づいてマスター プランを実行することによって作成されます。
-   販売注文明細行から直接作成する場合、または上位レベルの製造オーダーの作成と見積をする (ペギングされた供給) 場合です。
-   手動で作成します。




