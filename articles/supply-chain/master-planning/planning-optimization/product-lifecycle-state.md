---
title: 特定の製品ライフサイクル状態の製品を除外する
description: この記事では、ライフサイクルの状態に基づいて製品を除外する方法について説明します。
author: t-benebo
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 647e2cf4f14dbdfc3e7f04f43dcbd7115f19e8dc
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740768"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>特定の製品ライフサイクル状態の製品を除外する

[!include [banner](../../includes/banner.md)]

リリース済製品およびリリース済の製品バージョンには、**製品ライフサイクルの状態** フィールドが含まれます。 このフィールドを使用すると、特にマスター プラン作成の際に含める製品を制御できます。 **製品情報管理 \> 設定 \> 製品ライフサイクルの状態** に移動して、必要に応じてライフサイクルの状態を追加、削除、および編集できます。 製品ライフサイクルの各状態について、その状態を持つ製品がマスター プラン中に含まれる必要がある場合は、**計画に対して有効** オプションを *はい* に設定します。 このオプションを *いいえ* に設定すると、関連付けられている製品とバリアントは、部品表 (BOM) レベルのすべてのマスター プランと計算から除外されます。

**製品ライフサイクルの状態** フィールドが空白のままになっているリリースされた製品およびバリアントは、**計画に対して有効** オプションが *はい* に設定されている製品ライフサイクルの状態を持つものとして処理されます。 つまり、マスター プラン作成の際に含まれます。

> [!NOTE]
> 不要な入力候補を回避するために、**計画に対して有効** オプションが *いいえ* に設定されている製品ライフサイクル状態に、すべての古いリリース製品とバリアントを関連付けることを強くお勧めします。 この方法は、無駄を省くことができるため、再利用できない製品コンフィギュレーション バリアントを使用する場合に特に重要です。

## <a name="related-resources"></a>関連するリソース

製品ライフサイクルの状態の詳細については、[製品ライフサイクルの状態の概要](../../pim/product-lifecycle.md)を参照してください。

製品ライフサイクルの状態を使用して、製品をマスター プランおよび BOM レベルの計算から製品を除外する手順の詳細については、[マスター プランから製品を除外する製品ライフサイクルの状態を作成](../../pim/tasks/exclude-products-master-planning.md)を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]