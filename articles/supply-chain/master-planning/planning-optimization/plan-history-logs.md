---
title: 計画の履歴と計画ログの表示
description: この記事では、計画の最適化機能によってトリガーされる計画ジョブの履歴を表示する方法について説明します。
author: t-benebo
ms.date: 06/01/2020
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b2c9257fc67a06b57418b2f5b035b2b540131405
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863943"
---
# <a name="view-plan-history-and-planning-logs"></a>計画の履歴と計画ログの表示

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management で計画の最適化機能によってトリガーされる計画ジョブの履歴を表示する方法について説明します。

計画の履歴を表示するには、**マスター プラン** \> **設定** \> **計画** \> **マスター プラン** の順に移動して **履歴** を選択することにより、計画を開きます。 履歴には、選択された計画のすべてのジョブが一覧表示されます。 一覧には、完了ジョブおよび有効なジョブが含まれます。

システムでは、マスター プランごとに最大 60 件の履歴レコードが保持され、30 日以上が過ぎた古いレコードが削除されます。 新しいマスター プラン計算を実行するたびに、システムは新しい履歴レコードを追加し、必要に応じて最も古いレコードをクリーンアップします。

ジョブの開始時刻とステータスが表示されるのに加えて、特定のジョブのログも表示できます。 ログには、追加の情報および警告が含まれます。 すべてのジョブにログがあるわけではありません。 ジョブのログを表示するには、**ログ** を選択します。 ログ エントリは、ジョブが完了した日から 30 日間のみ、自動的に削除された後に保存されます。

マスター プランの処理の設定時に、**バックグラウンドで実行** クイック タブの **バッチ処理** オプションが有効にされた場合、マスター プランの実行時に生成された任意の警告およびエラーに関する詳細な情報がバッチ ジョブ ログに表示されます。 たとえば、自動確定エラーは、バッチ ジョブ ログ内にのみキャプチャされます。 **履歴** ページのログには表示されません。

マスター プランの実行時に発生した自動確定エラーおよび他の警告やエラーを表示するには、次の手順に従います。

1. **システム管理 \> 照会 \> バッチ ジョブ** の順に移動します。
1. 目的のマスター プランの実行を表すレコードを検索して選択します。 (たとえば、**職務明細書** フィールドの値は、*マスター プラン* から開始する場合があります。)
1. **バッチ ジョブ** ページで *拡張フォーム* または *レガシー (通常の) フォーム* のどちらを使用しているかに応じて、次のいずれかの手順に従います。

    - 拡張フォームを使用している場合: アクション ウィンドウで、**バッチ ジョブ履歴** を選択します。 次に、**バッチ ジョブ履歴** ページの、アクション ウィンドウで、**ログ** を選択します。
    - レガシー フォームを使用している場合: アクション ウィンドウの、**バッチ ジョブ** タブで、**ログ** を選択します。

1. **メッセージの詳細** を選択して **メッセージの詳細** ウィンドウを開くと、処理中にキャプチャされたすべての警告とエラーを表示できます。

## <a name="related-resources"></a>関連するリソース

- [計画最適化の概要](planning-optimization-overview.md)
- [計画最適化の開始](get-started.md)
- [計画の最適化フィット分析](planning-optimization-fit-analysis.md)
- [プランへのフィルターの適用](plan-filters.md)
- [計画ジョブのキャンセル](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
