---
title: シリアル番号が設定されている場合は、分析コードの場所を空白にすることはできない
description: シリアル品目の移動オーダーの作成後に出荷を確認するときにこのエラーが発生した場合は、既定の受入場所フィールドが空白になります。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476912"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>シリアル品目の移動オーダーの作成後に出荷を確認する際にエラーが発生する

## <a name="symptoms"></a>現象

高度な倉庫管理 (WMS) が有効になっている倉庫を使用してシリアル品目の転送オーダーを作成し、作業が完了した後、出荷を確認しようとすると、次のエラー メッセージが表示されます。

> 分析コード シリアル番号が設定されている場合は、分析コードの場所を空白のままにすることはできません。

## <a name="cause"></a>原因

"移動元" 倉庫の流通倉庫の **既定の受入場所** フィールドが空白になっているために発生します。

## <a name="resolution"></a>解決策

この問題を解決するには、流通倉庫の既定の受入場所を指定します。 この場所がライセンス プレートによって制御されていることを確認してください。
