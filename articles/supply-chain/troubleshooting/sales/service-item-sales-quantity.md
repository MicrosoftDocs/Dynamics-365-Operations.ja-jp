---
title: 販売見積明細行のサービス品目の数量を設定できない
description: 販売見積の作業時には、カウントする物理的な品目がないので、サービス品目である製品の販売数量を設定できません。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476917"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>販売見積明細行のサービス品目の販売数量を変更できない

## <a name="symptoms"></a>現象

販売見積明細行の *サービス* タイプの品目の販売数量 (**SalesQty** フィールド) を設定しようとすると、次のメッセージが表示されます。

> 数量フィールドの更新は許可されていません。

## <a name="cause"></a>原因

これは仕様です。 サービス品目の製品に対して、販売数量を設定することはできません。 たとえば、品目をインストールするサービスを提供している場合は、カウントする現物品目がないため、数量を記録する意味はありません。 サービスは 1 つだけです。
