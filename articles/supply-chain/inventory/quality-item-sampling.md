---
title: 品質管理品目サンプリング
description: このトピックでは、品目サンプリングの設定方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022231"
---
# <a name="quality-management-item-sampling"></a>品質管理品目サンプリング

品目サンプリングは、品質関連の一部として使用されます。 検査する必要がある現在の現物在庫の量を定義します。 サンプリングは、固定数量、割合、または完全なライセンス プレートに基づいて行うことができます。

## <a name="set-up-item-sampling"></a>品目サンプリングの設定

品目サンプリングを設定するには、次の手順を実行します。

1. **在庫管理 \> 設定 \> 品質管理 \> 品目サンプリング** の順に移動します。
1. **新規** を選択します。
1. **品目サンプリング** フィールドに値を入力します。
1. **説明** フィールドで値を入力します。
1. **値** フィールドに数値を入力します。 この値は、隣のフィールドで選択された数量の仕様に関連します。
1. テストが失敗した場合にロット全体または注文明細行の数量をブロックする必要がある場合は、**プロセス** セクションで、**完全ブロック** ボックスをオンにします。 このチェック ボックスをオフにすると、テストに失敗した場合でも品質指示内の品目のみがブロックされます。
1. **保存** を選択します。
1. ページを閉じます。

> [!NOTE]
> *倉庫プロセスの品質管理* 機能により、その他の品目のサンプリング機能が追加されます。 これにより、*品目サンプリング スコープ* の概念が追加され、完全なライセンス プレートを数量指定として定義することができます。 この機能をオンにする場合は、[倉庫プロセスの品質管理](quality-management-for-warehouses-processes.md)を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
