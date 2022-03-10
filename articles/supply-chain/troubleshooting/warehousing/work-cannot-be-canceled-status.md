---
title: 作業の状態が原因で作業をキャンセルできない
description: 作業の状態が原因で作業をキャンセルできない
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
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755981"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>作業の状態が原因で作業をキャンセルできない

エラーコード: WAX2190

## <a name="symptoms"></a>現象

システムは次のエラー メッセージを表示します。

> 作業 %1 は、状態が %2 であるためキャンセルできません。

## <a name="cause"></a>原因

現在の状態では、作業をキャンセルできません。

作業ヘッダーまたは作業明細行に予定された **作業状態** 値がありません。 作業ヘッダーの **作業状態** フィールドは *未終了* または *処理中* に設定されていません。

## <a name="resolution"></a>解像度

作業をキャンセルするには、これらの手順に従います。

1. **倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。
1. **作業 ID** フィールドで、キャンセルする作業の ID を指定します。
1. **OK** を選択します。
1. **はい** を選択して、作業をキャンセルすることを確認します。

詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。
