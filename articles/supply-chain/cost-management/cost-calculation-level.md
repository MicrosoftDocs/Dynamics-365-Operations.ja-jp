---
title: 原価計算レベル
description: この記事では、原価計算レベルという名前の部品表 (BOM) のレベルについて説明します。 このBOMレベルでは、計算から生産およびバッチ注文は計算から除外されます。
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e63a868696e36c1d4f5d19ea87bdf4d682c39f8c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334958"
---
# <a name="cost-calculation-level"></a>原価計算レベル

[!include [banner](../includes/banner.md)]

**原価計算レベル** が指定された部品表 (BOM) レベルでは、計算から製造注文とバッチ注文が除外されます。 このシステムは、原価計算のバージョンで原価計算を実行する際に、このレベルを使用します。 再計算や在庫原価計算などのプロセスでは、システムは代わりに **原価計算レベル** の BOM レベルを使用します。

## <a name="turn-the-cost-calculation-level-feature-on-or-off"></a>原価計算レベル機能のオン/オフの切り替え

この機能を使用するには、システムでオンにする必要があります。 Supply Chain Management のバージョン10.0.29 では、この機能は既定で有効になっています。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *コスト計算レベル* 機能を検索して、この機能をオンまたはオフにできます。

## <a name="example-scenario"></a>シナリオ例

以下の簡単なシナリオでは、**原価計算レベル** の  BOM レベルと **原価レベル** の BOM レベルの違いを示しています。

ここでは、A、B、C の 3 つの製品が使用されます。製品 C は製品 B のコンポーネントで、製品 B は製品 A のコンポーネントです。

- **原価レベル** では、次の BOM レベルが割り当てられます :

    - **製品 A :** 0
    - **製品 B :** 1
    - **製品 C :** 2

- **原価計算レベル** では、次の BOM レベルが割り当てられます :

    - **製品 A :** 0
    - **製品 B :** 1
    - **製品 C :** 2

製品 C の製造オーダーが作成され、製品 A が製造オーダー BOM に追加されます。 注文の見積後、BOM レベルは次のように更新されます :

- **原価レベル** では、次の BOM レベルが割り当てられます :

    - **製品 B :** 1
    - **製品 C :** 2
    - **製品 A :** 3

- **原価計算レベル** では、次の BOM レベルが割り当てられます :

    - **製品 A :** 0
    - **製品 B :** 1
    - **製品 C :** 2

この動作により、製造オーダー BOM に対する変更が後続の原価計算に影響を与えることがなくなります。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]