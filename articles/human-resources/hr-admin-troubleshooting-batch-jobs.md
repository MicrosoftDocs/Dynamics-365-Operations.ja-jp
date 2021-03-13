---
title: 数時間後にバッチ ジョブのスケジュールを設定して、パフォーマンスを最適化する
description: このトピックでは、数時間後の実行時間が長いバッチ ジョブのスケジュールを設定して、Microsoft Dynamics 365 Human Resources でのパフォーマンスに関する問題を解決する方法について説明します。
author: andreabichsel
manager: tfehr
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 219537aab2015469b6ca6ebed5c00af0190c5187
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113292"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>数時間後にバッチ ジョブのスケジュールを設定して、パフォーマンスを最適化する

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>問題

Microsoft Dynamics 365 Human Resources は、通常の営業時間中に実行時間の長いバッチジョブを実行する場合、パフォーマンスの問題が発生する可能性があります。

## <a name="resolution"></a>解像度

次のバッチ ジョブを業務時間外にスケジュールします。 また、頻繁に実行されるバッチ ジョブの頻度を確認することもお勧めします。 可能な場合は、バッチ ジョブの繰り返しを減らすことができます。 多くの場合、既定の頻度で十分です。

次のバッチ ジョブは、深夜またはそれより後の時間に実行する必要があります。 これらの定期的なバッチ ジョブのタイム ゾーンを確認してください。 一部のバッチ ジョブは、太平洋標準時 (PST) を使用している場合があります。

| バッチ ジョブ | 既定の発生 |
| --- | --- |
| バッチ ジョブ履歴のクリーンアップ | 月ごとに 1 回 |
| ステージング クリーンアップのエクスポート | 1 日に 1 回 |
| Common Data Service の統合で要求の同期が達成されませんでした | 1 日に 1 回 |
| 業務時間外に定期的に実行する必要があるデータベース圧縮システム ジョブ | 1 日に 1 回 |
| 業務時間外に定期的に実行する必要があるデータベース インデックス リビルド システム ジョブ | 1 日に 1 回 |

1. 人事管理では、**システム管理** を選択します。

2. **検索** バーで、上記のバッチ ジョブのいずれかを検索します。

3. **バックグラウンドで実行** を選択して、**再実行** を選択します。

   ![再実行の設定](media/talent-batch-history-cleanup-recurrence.png)

4. **再実行の定義** で、**開始日** および **開始時刻** を時間外または週末に発生するよう設定します。 **終了日なし** を選択します。 

   ![再実行の開始日時の定義](media/talent-batch-history-cleanup-define-recurrence.png)

5. **OK** を選択します。

6. 必要に応じて、**バックグラウンドで実行** でその他のパラメータを変更してから、**OK** を選択します。

## <a name="additional-resources"></a>追加リソース

[自動クリーンアップ タスクを使用したパフォーマンスの最適化](hr-admin-troubleshooting-batch-history.md)
