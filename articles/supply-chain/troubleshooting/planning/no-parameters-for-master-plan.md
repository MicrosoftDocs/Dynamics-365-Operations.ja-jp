---
title: マスター プランのパラメーターが存在しない
description: 計画オーダーを確定しようとすると、マスター プランのパラメーターが存在しないというエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294121"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>マスター プランのパラメーターが存在しない

エラーコード: SYS25368

## <a name="symptoms"></a>現象

計画オーダーを確定しようとする際に、次のエラー メッセージが表示されます:

> マスター プラン %1 のパラメーターは存在しません。

## <a name="cause"></a>原因

コンフィギュレーションの問題により、システムは指定した計画の設定を見つけられません。

## <a name="resolution"></a>解決策

- **マスター プラン \> 設定 \> 計画 \> マスター プラン** に移動し、指定した名前の計画が存在することを確認します。
