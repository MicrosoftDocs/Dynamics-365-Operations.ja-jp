---
title: マスター プランの品目を関連する補充グループ値でフィルター処理できません
description: マスター プランの品目を関連する補充グループ値でフィルター処理できません。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9750a73f0962179512c5e21a614a276c313ff975b7494f31589ca936886ecf6e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781396"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>マスター プランの品目を関連する補充グループ値でフィルター処理できません

KB 番号: 4612572

## <a name="symptoms"></a>現象

品目補充テーブルの関連レコードの値に基づいて、マスター プラン バッチ ジョブに含まれる品目をフィルター処理します。 (たとえば、**仕入先** や **補充グループ** の 値で品目をフィルター処理する場合など)。 バッチ ジョブのフィルター設定を使用すると、**品目** テーブルから **品目補充** テーブルへの結合を作成し、クエリで品目補充テーブルからフィールド値を指定できます。 ただし、この設定を完了した後も、システムは品目補充テーブルから指定されたフィールド値に一致する品目に対してだけでなく、品目補充全体に対して計画オーダーを作成します。

## <a name="resolution"></a>解決策

バッチ ジョブ フィルターでは、品目についてのみフィルター処理できます。 **品目補充** テーブルに結合を追加できますが、そのテーブルに対して行うフィルター設定はクエリの出力に影響を与えません。 実行時にシステムは、すべての補充グループと、フィルター処理された品目に含まれるすべてのバリエーションに対する計画を実行します。 実行に品目が既に含まれていれば、品目フィルターに含まれる補充グループは計画出力に影響しません。
