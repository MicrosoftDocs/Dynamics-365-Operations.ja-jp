---
title: 計画の履歴と計画ログの表示
description: このトピックでは、計画の最適化機能によってトリガーされる計画ジョブの履歴を表示する方法について説明します。
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187250"
---
# <a name="view-plan-history-and-planning-logs"></a>計画の履歴と計画ログの表示

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management で計画の最適化機能によってトリガーされる計画ジョブの履歴を表示する方法について説明します。

計画の履歴を表示するには、**マスター プラン** \> **設定** \> **計画** \> **マスター プラン** の順に移動して **履歴** を選択することにより、計画を開きます。 履歴には、選択された計画のすべてのジョブが一覧表示されます。 一覧には、完了ジョブおよび有効なジョブが含まれます。

計画の最適化マスター プラン実行のジョブ履歴は、マスター プランごとに最大 60 件のレコードまで保持されます。 新しいマスター プラン計算を実行するたびに、その計画の最も早い履歴レコードが削除されます。

ジョブの開始時刻とステータスが表示されるのに加えて、特定のジョブのログも表示できます。 ログには、追加の情報および警告が含まれます。 すべてのジョブにログがあるわけではありません。 ジョブのログを表示するには、**ログ** を選択します。 ログ エントリは、ジョブが完了した日から 30 日間のみ、自動的に削除された後に保存されます。

## <a name="related-resources"></a>関連するリソース

- [計画最適化の概要](planning-optimization-overview.md)
- [計画最適化の開始](get-started.md)
- [計画の最適化フィット分析](planning-optimization-fit-analysis.md)
- [プランへのフィルターの適用](plan-filters.md)
- [計画ジョブのキャンセル](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]