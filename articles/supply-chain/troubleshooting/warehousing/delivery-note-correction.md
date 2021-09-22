---
title: 納品書の修正はできません
description: 転記後に納品書を修正しようとすると、エラーが表示されます。 このページでは、WMS が有効になっている品目の転記済み梱包明細を修正する方法について説明します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476902"
---
# <a name="delivery-note-correction-cant-be-processed"></a>納品書の修正はできません

## <a name="symptoms"></a>現象

**キャンセル** ボタンが使用できないため、納品書を転記した後にキャンセルすることはできません。 また、納品書を修正することもできません。 実行しようとすると、次のエラー メッセージが表示されます。

> 納品書の修正はできません。 納品書には、倉庫管理プロセスの対象となる品目のみが含まれています。これらは納品書の修正ではサポートされていないためです。

## <a name="resolution"></a>解決策

高度な倉庫管理 (WMS) が有効になっている品目に対して転記された梱包明細を修正するには、注文から直接ではなく、積荷から転記する必要があります。
