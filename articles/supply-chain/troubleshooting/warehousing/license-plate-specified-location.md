---
title: この場所に対してライセンス プレートを指定する必要がある
description: WMS 対応倉庫の移動オーダーを作成した後にこのエラーが表示された場合、流通倉庫の既定の受入場所が空白になっています。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476843"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>移動オーダーの出荷確認時にライセンス プレートの指定ミスが発生する

## <a name="symptoms"></a>現象

高度な Warehouse Management (WMS) が有効になっている倉庫を使用して移動オーダーを作成し、作業が完了した後、出荷を確認しようとした場合に次のようなエラー メッセージが表示されることがあります。

> この場所に対してライセンス プレートを指定する必要があります。

## <a name="cause"></a>原因

"移動元" 倉庫の流通倉庫の **既定の受入場所** フィールドが空白になっているために発生します。

## <a name="resolution"></a>解決策

この問題を解決するには、流通倉庫の既定の受入場所を指定します。 この場所がライセンス プレートによって制御されていることを確認してください。
