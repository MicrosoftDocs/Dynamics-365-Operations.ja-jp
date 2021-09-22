---
title: 販売注文明細行の在庫引当の解除ができない
description: 販売明細行に対してオープン作業がある場合に、その明細行の在庫引当を解除しようとすると、エラーが表示されます。 引当を解放する作業を完了または削除します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476885"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>販売注文明細行の在庫引当の解除ができない

## <a name="symptoms"></a>現象

販売明細行に対してオープン作業がある場合に、その明細行の在庫引当を解除しようとすると、以下のエラー メッセージが表示されます。

> 引当に依存する作業が作成されているために、引当を削除できません。

## <a name="resolution"></a>解決策

未処理の梱包グループ作業があるかどうかを調べて、品目を梱包ステーションから別の場所 (*Baydoor* など) に移動します。 **作業の作成履歴ログ** ページと **作業の詳細** ページのレコードを確認して、在庫が物理的に引当されているかどうかを確認し、その作業を完了または削除して引当を解放します。
