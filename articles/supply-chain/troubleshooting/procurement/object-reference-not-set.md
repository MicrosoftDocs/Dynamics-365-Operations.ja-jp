---
title: 発注書の確認時に "オブジェクト参照が設定されていない" というエラーが発生する
description: 発注書の確認時に "オブジェクト参照が設定されていない" というエラーが発生する
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
ms.openlocfilehash: 78e5e365f7197c1a0c25bf6eb63bcd5bd0f482ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476897"
---
# <a name="error-object-reference-not-set-occurs-during-purchase-order-confirmation"></a>発注書の確認時に "オブジェクト参照が設定されていない" というエラーが発生する

## <a name="symptoms"></a>現象

発注書を確認するときに、次の例外を受信します:

> オブジェクト参照が設定されていない

## <a name="cause"></a>原因

この問題は、発注書の配分に不整合があるために発生することがあります。

## <a name="resolution"></a>解決策

この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。 詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。
