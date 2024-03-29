---
title: 発注書および請求書の減額後の繰り越し予算の更新
description: この記事では、発注書がキャンセルまたは減額された場合、および請求書が減額された場合の繰り越し予算に発生したことをどのように管理するかについて説明します。
author: TaylorVH
ms.date: ''
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: Version 1611
ms.search.form: LedgerFund
ms.openlocfilehash: 790f1e770fd77d5209436c1c89e0f6125aac150f
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573049"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>発注書および請求書の減額後の繰り越し予算の更新

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

この記事では、発注書がキャンセルまたは減額された場合、および請求書が減額された場合の繰り越し予算に発生したことをどのように管理するかについて説明します。

年末に発注書を処理する方法の詳細については、[年末の発注書の処理](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end) を参照してください。

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>請求書の差異に対する繰り越し予算の減額のオン/オフの切り替え

システムは、発注書がキャンセルまたは減額された場合に繰り越し予算をいつでも更新できます。 ただし、請求書の減額時に繰り越し予算を更新する場合は、*発注書に対する請求書を差異で減額する場合に、繰り越し予算を減額する* 機能を有効にする必要があります。 管理者は、**[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ワークスペースでそれを検索して、この機能のオン/オフを切り替えることができます。

## <a name="purchase-order-reductions-and-cancellations"></a>発注書の減額とキャンセル

*発注書に対する請求書が差異で減額される場合に、繰り越し予算を減額する* 機能が有効かどうかに関係なく、条件を満たす発注書がキャンセルまたは減額された場合には繰り越し予算が更新されます。 各一般会計資金は、次のいずれかの方法で応答するように設定できます。

- 作成された繰り越し予算を維持します。
- 繰り越し予算を自動的に調整して、キャンセルされた金額または減額した金額を削除します。

資金を含む配分を持つ発注書明細行のみが自動予算調整を利用できます。 自動予算調整は、発注書が確定された場合、または発注書の減額が確認された場合に行われます。

## <a name="invoice-reductions"></a>請求書の減額

*発注書に対して請求書が差異で削減される場合に、繰り越し予算を減額する* 機能が有効化かどうかに関係なく、条件を満たす発注書がキャンセルまたは減額された場合には繰り越し予算が更新されます。 この請求書は、繰り越し予算がある発注書に対するものである必要があります。 減額には、価格の差異、請求金額の差異、税金の差異があります。 請求中に繰り越し発注書が減額されると、差異が作成されます。 請求書を転記すると、発注書の債務が差異の金額分減額されます。 この機能により、差異の金額に対する自動予算調整も作成されます。

*発注書に対して請求書が差異で減額された場合は、繰り越し予算を減額する* 機能が無効になっている場合、繰り越し予算はこのシナリオでは減額されません。 したがって、差異の金額に対する残りの繰り越し予算は残ります。

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>各資金に対する繰り越し予算オプションを構成する

発注書または請求書を減額した場合に、繰り越し予算を減額できるようにする必要がある各一般会計資金については、次の手順に従います。

1. **一般会計 \> 勘定科目表 \> 資金 \> 資金** の順に移動します。
1. 設定する資金を選択します。
1. **発注書の年度末プロセス** で、**選択した年度末の上書きオプション** オプションを *はい* に設定してください。
1. **繰り越し予算ステータス** で、必要に応じで **繰り越し発注書がキャンセルまたは減額された場合に予算を復帰させる** フィールドを設定します。 この設定は、*発注書に対して請求書を差異で下なくする場合、繰り越し予算を減額する* 機能がシステムで有効になっているかどうかによって少し異なる影響を与える場合があります。

    - この機能を無効にすると、キャンセルされた発注書または削減された発注書に対する処理だけが処理されます。 オプション設定は次の方法で動作します。

        - *いいえ* - キャンセルまたは削減された発注書の残りの残高に対する予算登録エントリが作成されます。
        - *はい* - システムは発注書のキャンセルまたは減額は許可しますが、予算登録エントリは作成しません。 繰り越し予算は、他のドキュメントによる消費に対して使用できます。

    - この機能を有効にすると、システムは請求書の差異に対してと、キャンセルされたまたは減額された発注書の両方に対して反応します。 オプション設定は次の方法で動作します。

        - *いいえ* - 請求書の差異に対しては、システムは差異減少金額について発注書に対して予算登録エントリを作成します。 キャンセルされた発注書または減額した発注書の場合、この設定は、機能をオフにした場合と同じ効果があります。
        - *はい* - 請求書の差異については、システムは請求書の減額は許可しますが、予算登録エントリは作成しません。 繰り越し予算は、他のドキュメントによる消費に対して使用できます。 キャンセルされた発注書または減額した発注書の場合、この設定は、機能をオフにした場合と同じ効果があります。

## <a name="additional-resources"></a>追加リソース

- [年末の発注書の処理](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [一般予算引当の管理](general-budget-reservation-tasks.md)
- [公的機関の資金](funds-public-sector.md)
- [公的部門の資金の設定](tasks/set-up-fund-public-sector.md)
