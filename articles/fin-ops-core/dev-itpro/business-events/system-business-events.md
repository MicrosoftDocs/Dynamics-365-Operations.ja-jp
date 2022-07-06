---
title: バッチ ビジネス イベント
description: この記事では、バッチ ビジネス イベントの詳細情報を提供します。
author: matapg007
ms.date: 02/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2021-03-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 354dea9ca53c409dcc1b99325d619e99382d9a32
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848733"
---
# <a name="batch-business-events"></a>バッチ ビジネス イベント

[!include[banner](../includes/banner.md)]

バッチ フレームワークは、次のシステム ビジネス イベントを出力します。

| ビジネス イベント | 説明 | モジュール |
|----------------|-------------|--------|
| バッチ ジョブの開始 | このイベントは、バッチ ジョブが実行中としてマークされているときに発生します。 | バッチ |
| バッチ ジョブの終了 | このイベントは、バッチ ジョブが完了としてマークされているときに発生します。 | バッチ |
| バッチ ジョブの失敗 | このイベントは、バッチ ジョブが失敗としてマークされているときに発生します。 | バッチ |
| バッチ ジョブのキャンセル | このイベントは、バッチ ジョブがキャンセルとしてマークされているときに発生します。 | バッチ |

## <a name="usage"></a>用途

### <a name="batch-job-started-and-batch-job-finished"></a>バッチ ジョブの開始およびバッチ ジョブの完了

**バッチ ジョブの開始** および **バッチ ジョブの完了** イベントは、実行時間の長いバッチ ジョブの監視および特定を行うために使用されます。 ジョブに予想以上の時間がかかる場合に関係者に通知するためにも使用できます。 既定では、これらのイベントはアプリケーションで無効になっています。

### <a name="batch-job-failed"></a>バッチ ジョブの失敗

**バッチ ジョブの失敗** イベントは、特定のバッチ ジョブが失敗していないか監視し、リアルタイムに関係者に通知するために使用できます。 既定では、このイベントはアプリケーションで有効になっています。

## <a name="configure-batch-business-events"></a>バッチ ビジネス イベントのコンフィギュレーション

1. **システム管理 \> 照会 \> バッチ ジョブ** の順に移動します。
2. **ビジネス イベント** タブで設定を更新して、バッチ ビジネス イベントを発生させます。

イベントには次のペイロードが含まれます。

| フィールド名 | フィールド ラベル |
|------------|-------------|
| JobId | バッチ ジョブ ID |
| JobDescription | バッチ ジョブの説明 |
| JobStatus | バッチ ジョブの状態 |
| JobOwnerEmailId | バッチ ジョブの所有者の電子メール ID |
| JobExecutedByEmailId | 電子メール ID によって実行されたバッチ ジョブ |
| AdminEmailId | 管理者ユーザーの電子メール ID |
| JobEndUtcDateTime | ジョブ終了の UTC 日時 |
| BusinessEventId | ビジネス イベント ID |
| ControlNumber | ビジネス イベントの制御番号 |
| イベント ID | ビジネス イベント インスタンス ID |
| EventTime | ビジネス イベント インスタンス ID |
| MajorVersion | メジャー バージョン |
| MinorVersion | マイナー バージョン |

現在のカタログおよびビジネス イベントのスキーマを取得するには、**システム管理 \> 設定 \> ビジネス イベント** に移動します。
