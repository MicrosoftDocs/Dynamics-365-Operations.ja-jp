---
title: 利用可能な予算財源
description: このトピックでは、利用可能な予算資金機能を紹介し、組織の財源管理を最適化するための予算管理設定に役立つ情報を提供します。
author: rcarlson
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: a8279ae9b08c7537548c1c8b71e6e978fee2b8a1
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891318"
---
# <a name="budget-funds-available"></a>利用可能な予算財源

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、利用可能な予算資金機能を紹介し、組織の財源管理を最適化するための予算管理設定に役立つ情報を提供します。

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>予算資金の計算機能を強化

**予算資金使用可能計算の金額のみを追跡する** 機能は、**予算管理パラメータの定義** ページでの設定に基づいて、文書の種類と状態の基礎となる予算管理テーブルを追跡することができます。

予算管理の構成オプションの中には、機能を正しく動作させるために固有の設定が必要なものがあります。 これらのオプションは、**予算管理パラメータの定義** ページの **利用可能な予算資金** タブで選択またはクリアされます。 次の表は、利用可能な予算資金機能で必要となる設定を示しています。

| このオプションが選択されている場合 | このオプションも選択する必要があります |
| ------------------------- | -------------------------------- |
| 事前の債務に対する予算引当 | 予算引当金 *と* 実際の支出 |
| 債務に対する予算引当 | 実際の経費 |
| 購買要求タイプのドキュメントを含む予算要求 | 事前の債務に対する予算引当 |

この機能は新しいドキュメントにのみ影響します。 既存の文書の金額は、利用可能な予算資金の設定が変更され、新しい予算管理の設定が有効になるまで継続的に追跡され、予算管理統計の照会に表示されます。 その時点で、利用可能な予算資金の計算から削除された文書については、予算追跡データが削除されます。

**未転記の実際の支出** オプションはオフのままにしておくすることをお勧めします。 これを選択した場合、保留中の仕入先請求書など、未転記の文書に対して時間のかかる予算管理計算が行われることになります。
