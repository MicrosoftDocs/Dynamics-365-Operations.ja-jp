---
title: 会社間注文と返品注文
description: この記事では、会社間注文と返品注文について説明します
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 65d0dc6049969ff7d8f84ca4eb3baf486ddad660
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859030"
---
# <a name="intercompany-orders-and-return-orders"></a>会社間注文と返品注文

[!include [banner](../../includes/banner.md)]

この記事では、会社間の発注書、販売注文、返品注文、購買契約書と販売契約書の作成または変更方法を説明しています。

## <a name="about-intercompany-orders"></a>会社間注文について

会社間の販売注文を作成すると、Microsoft Dynamics 365 Supply Chain Management は自動的に対応する発注書を作成します。 同様に、会社間の発注書を作成すると、対応する会社間販売注文の自動作成を促します。

これは、2 社間 (関連する 2 社間の取引) と、ほとんどの 3 社間 (会社間の取引が外部顧客の販売注文から発生した場合) の注文に当てはまります。

## <a name="intercompany-order-example"></a>会社間注文の例

2 つの関連会社があります。 会社 A は販売子会社で、会社 B は配送会社です。 会社間の販売注文書と発注書は次のシナリオで自動的に作成されます:

- 会社 A が発注書を作成し、仕入先が会社 B の場合、会社 B で自動的に会社間販売注文が作成されます。2 社間の注文チェーンは、会社 A の発注書と会社 B の会社間販売注文で構成されます。
- 会社 B が販売注文を作成し、顧客が会社 A の場合は、会社 A で自動的に会社間発注書が作成されます。2 社間の注文チェーンは、会社 B の販売注文と会社 A の会社間発注書で構成されます。
- 会社 A が初めて外部顧客の販売注文を作成すると、会社 A で発注書を自動的に作成できます。これにより、会社 B での会社間販売注文の自動作成を促します。3 社間の注文チェーンは、販売注文、会社 A の発注書、および会社 B の会社間販売注文で構成されます。

## <a name="about-intercompany-return-orders"></a>会社間返品注文について

会社間品目は通常の返品と同様に返品できます。 ただし、会社間品目では、外部顧客からの返品注文によって、会社間発注書が作成されます。 これにより、会社間の販売返品注文が自動的に作成されます。 会社間品目を外部顧客の返品注文なしで返品することもできます。

会社間返品注文は、**返品注文の作成** ページで通常の返品注文と同様に開始されます。

Microsoft Dynamics 365 Supply Chain Management では、会社間の販売および購買契約書が自動的に更新され、返品品目が反映されます。 その品目の販売または購買契約書の確約は、品目の返品時に数量または金額の変更を反映するように自動的に調整されます。

## <a name="intercompany-return-order-example"></a>会社間返品注文の例

会社 A は会社間品目の購買契約書にリンクされている発注書を作成します。 会社間販売注文は、対応する販売契約書にリンクされている会社 B で自動的に作成されます。 購買契約書と販売契約書は会社間契約として関連付けられます。

会社 A は会社 B に会社間品目を返品します。会社 B がその品目の返品注文を作成し、会社Aでは購買返品注文が自動的に作成されます。元の注文にリンクされている購買契約書と販売契約書の両方の確約は、数量または金額の変更を反映するように自動的に調整されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
