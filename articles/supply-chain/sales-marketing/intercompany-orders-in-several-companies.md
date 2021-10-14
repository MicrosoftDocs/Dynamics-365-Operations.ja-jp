---
title: 複数の会社間での会社間発注書および販売注文の作成
description: このトピックでは、複数の会社間での会社間発注書または販売注文の作成方法について説明します
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5d756a82abb7e7b19080128353d863f29837fc5b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548373"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>複数の会社間での会社間発注書および販売注文の作成

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management では、1 社の生産会社と数社の販売会社を扱うだけではありません。 会社間に設定されたすべての会社は、取引会社と生産会社の両方にすることができます。

複数の会社が同じ品目を提供している場合は、購入先を自由に選択でき、1 件の販売注文が複数の発注書になった場合でも更新が処理されます。

1 件の会社間発注書を自動的に作成する場合と同じように、会社で元の販売注文を作成し、その後に複数の会社間発注書を作成することで、複数の会社間仕入先会社に注文を処理させることができます。 Microsoft Dynamics 365 Supply Chain Management は、仕入先会社の会社間販売注文書を自動的に作成します。

これを行うには、すべての会社を取引関係として設定する必要があります。 仕入先会社は、Microsoft Dynamics 365 Supply Chain Management で会社間仕入先として設定され、関連アイテムの主要仕入先である必要があります。 販売注文の **ヘッダーの表示** で、**会社間設定** クイックタブの **会社間注文の自動作成** フィールドと **直納** フィールドを選択する必要があります。 これが既定の設定です。

販売明細行は通常の方法で作成します。 レコードの処理を終了すると、会社間発注書と会社間販売注文書が作成されたことを通知するメッセージが表示されます。 メッセージには新しい注文へのリンクが含まれます。 仕入先会社で作成された会社間販売注文書を表示するには、元の販売注文を開き、**全般** タブの **関連情報** グループで **参照** を選択します。

仕入先の会社間発注書を開くと、Microsoft Dynamics 365 Supply Chain Management が各仕入先の元の販売注文番号と会社間の販売注文番号を自動的に入力していることがわかります。

同様に、仕入先の会社間販売注文を開くと、Microsoft Dynamics 365 Supply Chain Management が各仕入先の元の販売注文番号と会社間の発注書番号を自動的に入力していることがわかります。

> [!NOTE]
> 会社間仕入先会社の 1 社に注文中の品目が存在し、他の会社に存在しない場合、Microsoft Dynamics 365 Supply Chain Management は、品目が存在する仕入先会社に対して会社間注文を作成しますが、他の会社に対する注文作成を停止します。 この場合、通知メッセージが表示されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
