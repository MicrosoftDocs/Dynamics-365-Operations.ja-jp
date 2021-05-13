---
title: ユーザーに割り当てられた作業がキャンセルできない
description: ユーザーに割り当てられた作業がキャンセルできない
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924404"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>ユーザーに割り当てられた作業がキャンセルできない

エラーコード: WAX708

## <a name="symptoms"></a>現象

システムは次のエラー メッセージを表示します。

> ユーザーに割り当てられた作業はキャンセルできません。

## <a name="cause"></a>原因

作業はユーザーによってロックされており、キャンセルすることができません。 これを確認するには、作業 ID を開き、**一般** タブを開きます。作業がロックされている場合は、**作業ステータス** フィールドが *進行中* に設定され、**ロック元** フィールドはユーザー ID に設定されます。

## <a name="resolution"></a>解像度

作業をキャンセルするには、これらの手順に従います。

1. **倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。
1. **作業 ID** フィールドで、キャンセルする作業の ID を指定します。
1. **OK** を選択します。
1. **はい** を選択して、作業をキャンセルすることを確認します。

詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。
