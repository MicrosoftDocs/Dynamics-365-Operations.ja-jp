---
title: 購買契約書の上限は、購買要求に対して有効ではありません
description: 購買契約書の上限は、購買要求に対して有効ではありません
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476854"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>購買契約書の上限は、購買要求に対して有効ではありません

## <a name="symptoms"></a>現象

購買要求が購買契約書にリンクされている場合、購買要求に対して購買契約書の上限は有効ではありません。 既定の価格情報は正しく入力されていますが、購買要求で購買契約書の上限を超えて注文することができます。

## <a name="resolution"></a>解決策

この動作は予期されています。 要求が常に承認されるとは限らないため、購買契約書に数量または金額を予約しないでください。 したがって、購買契約書の上限には達しません。
