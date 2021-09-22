---
title: 積載重量に正の数しか入力できない
description: 場所間で作業を処理するときに、積載重量に関するエラーが発生し、更新がキャンセルされることがあります。 問題を解決するには、次の手順に従います。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476864"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>場所間の作業の処理時に積載重量のエラーおよび更新がキャンセルされる

## <a name="symptoms"></a>現象

梱包場所からステージングの場所への作業またはステージング場所からドッキング場所への作業を処理するときにオープン作業がある場合に、次のこエラーが表示されることがあります。

> '積載重量'(=-%1) フィールドに、正の数値しか入力できません。 更新はキャンセルされました。

## <a name="resolution"></a>解決策

この問題を解決するには、**システム管理 \> 定期タスク \>データベース \> 整合性チェック** を実行し、**倉庫積荷重量の整合性チェック** のプロセスを実行します。
