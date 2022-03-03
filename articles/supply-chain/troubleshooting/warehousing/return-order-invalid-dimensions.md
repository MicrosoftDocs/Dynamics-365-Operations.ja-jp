---
title: 在庫分析コードが無効のために積荷明細行を作成できない
description: 返品販売注文を倉庫にリリースしようとする場合、無効な在庫分析コードに関するエラーが表示されることがあります。 これらを注文明細行から削除します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119215"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>在庫分析コードが無効のために返品販売注文の積荷明細行を作成できません

## <a name="symptoms"></a>現象

返品販売注文を倉庫にリリースしようとする場合、次のエラー メッセージが表示されることがあります。

> 無効な在庫分析コードがあるため、この注文明細行には積荷明細行を作成できません。 引当階層の場所分析コードの下に配置されている在庫分析コードを参照することはできません。 無効な分析コードを注文明細行から削除します。

## <a name="resolution"></a>解決策

残念ながら、この製品は、販売返品プロセスの積荷プロセスをサポートしていません。 したがって、返品販売注文を倉庫にリリースすることはできません。

販売注文トランザクションで、引当階層の **場所** 分析コードの下に配置されている在庫分析コードを参照することはできません。 無効な分析コードを注文明細行から削除すると解決できます。
