---
title: メンテナンス時に二重書き込みを一時停止する
description: このトピックでは、テーブル マップを一時停止する方法について説明します。
author: nhelgren
ms.date: 10/13/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: nhelgren
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38e1be6d773e42d0c1efa2abc5c6269b18395a9f
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782493"
---
# <a name="pause-dual-write-for-maintenance"></a>メンテナンス時に二重書き込みを一時停止する

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

テーブル マップは、手動で一時停止またはルール経由で自動的に一時停止が可能です。 テーブル マップを一時停止することで、特に計画的または計画外のメンテナンス中にビジネスの継続性を確保するのに役立ちます。 アプリが維持されている間、ユーザーは引き続き作業を行いレコードを作成できます。

**実行中** の状態のテーブル マップを一時停止すると、テーブル マップを再開するまで、作成または更新されたすべてのレコードがキューに入れられます。 キューに入れられたレコードは、安全な Microsoft Azure ストレージに格納されます。 テーブル マップを再開して **実行中** の状態に戻す際、これらのテーブルが再び実行されます。

> [!NOTE]
> テーブル マップが **一時停止** の状態の間、キューに入れるレコードの数とレコードをキューに入れる時間には制限があります。 最初に発生した制限が適用されます。 プロセスはソフト制限から始まり、最終的にハード制限を適用して、ストレージ制限を超えないようにします。

**一時停止** 状態のテーブル マップ用に作成または更新されたレコードは、テーブル マップの **キューに入れられたレコード** で表示できます。

![キューされたレコードのタブ。](media/Queued-Insights1.png)

**キューに入れられたレコード数の合計** 行は、特定のテーブル マップに対してキューに入れらたレコードの合計数を示します。 **さらに読み込む** を選択すると、ページ設定された表示内で追加のレコードを表示できます。 統合キーでレコードのフィルタ処理もできます。

テーブル マップを再開すると、**一時停止** 状態から **実行中** の状態に切り替わり、キューから送信先アプリにレコードが書き込まれます。 送信先アプリ内のビジネス検証など、さまざまな理由により、一部のレコードがエラーが発生し、書き込みに失敗する可能性があります。 この場合、レコードはキューに残り、**キャッチアップ エラー** タブに表示されます。詳細については、[テーブル マップの一時停止からのキャッチアップ エラー](errors-and-alerts.md#catch-up-errors-from-pausing-a-table-map) を参照してください。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
