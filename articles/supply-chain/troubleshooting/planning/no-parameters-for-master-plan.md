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
ms.openlocfilehash: d039b79684f87e7791fb9dae7cbdc6ced220bc092d9a0ab624616c1c345986da
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756778"
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
