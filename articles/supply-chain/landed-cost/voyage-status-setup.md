---
title: 航海状態の設定
description: このトピックでは、ユーザーが航海に割り当て可能な状態の値を確立する方法について説明します。
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500889"
---
# <a name="voyage-status-setup"></a>航海状態の設定

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

**航海状態ページ** では、ユーザーが航海に割り当て可能な一連の状態値を確立します。 ユーザーは、航海のすべてのレベル: 航海、輸送コンテナ、Folio、発注書、品目 (購買注文明細行および移動オーダー明細行) に航海状態値を割り当てることができます。 これらは 2 つの目的で使用されます。

- 航海、輸送コンテナ、Folio、発注書、または品目 (購買注文明細行および移動オーダー明細行) の状態をユーザーに通知します。
- 変更または削除を防止することにより、原価領域の使用を制限します。

航海状態の設定をするには、**陸揚原価 \> 設定 \> 航海状態** に移動します。 アクション ウィンドウのボタンを使用して、状態を追加、削除、および編集できます。

各原価領域には、独自の航海状態のセットと階層があります。 したがって、**航海状態** ページの **原価領域** フィールドで、最初に、航海状態を表示または作成する原価領域を選択する必要があります。 その後、各航海状態ごとに、必要に応じて次の表に示されているフィールドを設定します。 航海の状況は、追跡コントロール センターを使用して確立されたルールなどのシステム イベントによって自動的に変更されることもあることに注意してください。

| フィールド | 説明 |
|---|---|
| 航海状態 | 航海状態の名前を入力します。 |
| 説明 | 航海状態の説明を入力します。 |
| 変更 | この状態の航海の変更をユーザーに許可する場合は、このチェックボックスをオンにします。 |
| 消去 | この状態の航海の削除をユーザーに許可する場合は、このチェックボックスをオンにします。 |
| 必須 | このチェックボックスをオンにすると、航海の状態を必須にし、スキップできない状態になります。 |
| 親 | このフィールドを使用すると、状態値の間の階層を設定できます。 航海状態は、親状態からその子状態の 1 つまで、階層の下位にのみ (手動または自動で) 変更できます。

> [!NOTE]
> 組織が使用する特定の航海状態のみを設定する必要があります。 一般的な航海状態には、*確認済*、*輸送中の商品*、*入庫済*、*原価設定* および *原価計算済* が含まれます。 ただし、他の状態が存在する可能性があります。
