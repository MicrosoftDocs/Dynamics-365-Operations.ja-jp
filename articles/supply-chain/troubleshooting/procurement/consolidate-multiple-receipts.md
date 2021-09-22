---
title: 複数の製品受領書を 1 つの発注書にまとめることはできません
description: 複数の製品受領書を 1 つの発注書にまとめることはできません。異なる製品受領書明細行の会計日付が異なる場合に使用します。
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476845"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>複数の製品受領書を 1 つの発注書にまとめることはできません

## <a name="symptoms"></a>現象

複数の製品受領書を 1 つの発注書にまとめることはできません。異なる製品受領書明細行の会計日付が異なる場合に使用します。

## <a name="resolution"></a>解決策

Dynamics 365 Supply Chain Management の以前のバージョンでは、このような場合にまとめることができました。 ただし、このプラクティスではエラーが発生しやすくなります。 作成された発注書明細行の会計日と、その発注書明細行の作成元である製品受領書明細行の会計日とは異なるものにする必要があります。 (発注書明細行の会計日は、発注書ヘッダーの会計日と一致します。) したがって、複数の製品受領書を1つの発注書に連結することはできなくなります。

たとえば、予算引当や債務など、会計日が使用されます。 したがって、この品目は、製品受領書から発注書への移行時に保持する必要があります。
