---
title: 会社間梱包明細
description: この記事では、会社間取引の梱包明細を生成および印刷する方法について説明します
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
ms.openlocfilehash: 3516058bbf925df4b0a0c75286a3d97457cc1e69
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900857"
---
# <a name="intercompany-packing-slips"></a>会社間梱包明細

## <a name="generate-intercompany-packing-slips"></a>会社間梱包明細の生成

[!include [banner](../../includes/banner.md)]

直納を使用する場合、会社間販売注文書で梱包明細を生成すると、梱包明細は、常に会社間発注書と元の販売注文の両方で自動的に生成されます。 会社間発注請求書は、以前に生成された会社間発注書の梱包明細に基づきます。

会社間販売注文書の梱包明細を更新すると、これらの更新は会社間発注書と元の販売注文の両方に反映されます。

直納を使用しない場合、会社間販売注文書、会社間発注書、および元の販売注文の梱包明細を手動で生成する必要があります。

## <a name="print-intercompany-packing-slips"></a>会社間梱包明細の印刷

[!include [banner](../../includes/banner.md)]

直納を使用する場合、会社間販売注文書に梱包明細を転記すると、会社間発注書と元の販売注文の梱包明細が自動的に印刷されます。

梱包明細を自動的に印刷するには、発注書の **会社間** ページで両方の **梱包明細を自動的に印刷** フィールドを選択します。

会社間販売注文書の梱包明細を更新すると、変更内容が会社間発注書と元の販売注文に自動的に反映されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
