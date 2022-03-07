---
title: 在庫分析コードが無効のために積荷明細行を作成できない
description: 返品販売注文を倉庫にリリースしようとする場合、無効な在庫分析コードに関するエラーが表示されることがあります。 これらを注文明細行から削除します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac58
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cb728f6a989cdac63c91d49baaea094bace59e4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476892"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>在庫分析コードが無効のために返品販売注文の積荷明細行を作成できません

## <a name="symptoms"></a>現象

返品販売注文を倉庫にリリースしようとする場合、次のエラー メッセージが表示されることがあります。

> 無効な在庫分析コードがあるため、この注文明細行には積荷明細行を作成できません。 引当階層の場所分析コードの下に配置されている在庫分析コードを参照することはできません。 無効な分析コードを注文明細行から削除します。

## <a name="resolution"></a>解決策

残念ながら、この製品は、販売返品プロセスの積荷プロセスをサポートしていません。 したがって、返品販売注文を倉庫にリリースすることはできません。

販売注文トランザクションで、引当階層の **場所** 分析コードの下に配置されている在庫分析コードを参照することはできません。 無効な分析コードを注文明細行から削除すると解決できます。
