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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748694"
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
