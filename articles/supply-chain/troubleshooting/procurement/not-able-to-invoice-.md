---
title: 顧客向けの販売注文は請求できません
description: '[請求書の自動転記] オプションを有効した後に、元の販売注文と元の直納発注書の請求は行えなくなりました。'
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756754"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>顧客向けの販売注文は請求できません

KB 番号: 4611793

## <a name="symptoms"></a>現象

仕入れ先の **会社間** ページで **請求書の自動転記** オプションを有効した後に、元の販売注文と元の直納発注書の請求は行えなくなりました。

## <a name="resolution"></a>解像度

会社間および直納注文の請求に関する同期動作は、[パラメーターを設定して会社間の注文を転記する](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order) で説明があるように、パラメータによって制御、強制されています。

これらのパラメータを設定した後、最初に会社間の販売注文を請求する必要があります。 そうすると、元の販売注文と発注書が同期されます。
