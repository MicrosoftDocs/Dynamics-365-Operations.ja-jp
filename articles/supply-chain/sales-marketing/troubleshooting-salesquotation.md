---
title: 販売見積に関するトラブルシューティング
description: このトピックでは、販売見積と作業する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824753"
---
# <a name="troubleshoot-sales-quotations"></a>販売見積に関するトラブルシューティング

このトピックでは、販売見積と作業する際に発生する可能性がある問題の修正方法について説明します。

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>サービス品目の販売見積の販売数量を変更できません。

### <a name="issue-description"></a>問題の説明

販売見積明細行の *サービス* タイプの品目の販売数量 (**SalesQty** フィールド) を設定しようとすると、"フィールドの数量に対する更新は許可されません" というメッセージが表示されます。

### <a name="issue-resolution"></a>問題の解決

サービス品目の製品に対して、販売数量を設定することはできません。 たとえば、品目をインストールするサービスを提供している場合は、現物品目がないため、数量を記録する意味はありません。 サービスは 1 つだけです。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]