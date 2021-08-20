---
title: 現物入庫済み購買注文は在庫決算レポートに表示されない
description: 現物入庫済み購買注文が、オープン数量チェック在庫決算レポートに表示されません。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 49faa2c68d496c5c0d8c7e4abfd93d9a917857220dd23c09a050fa3436e1d49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746870"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>現物入庫済み購買注文は在庫決算レポートに表示されない

KB 番号: 4612595

## <a name="symptoms"></a>現象

現物入庫済み購買注文が、**オープン数量チェック** 在庫決算レポートに表示されません。

## <a name="resolution"></a>解像度

**オープン数量チェック** レポートには、選択した決算日現在で現物入庫済みの在庫入庫に対して決済できない出庫トランザクションが表示されます。 レポートでは現物入庫を含めるオプションを選択できます。 この場合、決済できない出庫トランザクションに対処できる場合は、現物入庫が表示されます。 詳細については、[在庫原価計算の実行の準備](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close)を参照してください。
