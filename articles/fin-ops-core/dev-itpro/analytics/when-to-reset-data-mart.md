---
title: データ マートをリセットするタイミング
description: このトピックでは、データ マートのリセットによって改善される可能性がある状況と、データ マートのリセットが役立つ可能性が低い状況を一覧表示します。
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988995"
---
# <a name="when-to-reset-a-data-mart"></a>データ マートをリセットするタイミング

データ マートのリセットは、時間がかかる場合があります。 状況によっては、このアクションが必要なソリューションではない場合があります。 このトピックでは、データ マートのリセットによって改善される可能性がある状況と、データ マートのリセットが役立つ可能性が低い状況を一覧表示します。  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>データ マート リセットはいつ実行すべきですか。
データ マートをリセットする前に、次の質問を検討してください。 1 つ以上の質問に回答すると、データ マートをリセットすることで組織の利益を得る可能性があるという質問が表示される場合があります。

- アプリケーション データベースは復元されましたか。
- サポート インシデントを開き、サポート エンジニアから、トラブルシューティングの手順の一環としてデータ マートをリセットするように指示されたとします。
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>データ マートのリセットが適切ではないタイミングはどのようなものですか。
データ マートのリセットをお勧めできない場合があります。 次のようなものがあります。 

- データ同期に関連するパフォーマンス問題が発生しています。 
- 次の理由によりリセット パターンが繰り返し発生する場合。 
  - **欠落しているデータ** 
  - **統合の行き詰まり状態** 
  - **古いレコード** - 自身による古いレコードはデータ マートのリセットを正当化する必要はありません。 大規模なデータ セットがある場合、リセット プロセスの実行に時間がかかりますが、改良が行う可能性は低いです。
 
## <a name="what-is-a-data-mart-reset"></a>データ マート リセットとは何ですか。
- リセットは、既存のタスクが完了した場合にのみ開始されます。 これにより、古いデータが挿入されるのを確実に行う必要があります。 この時点で、"有効なタスクが原因でデータ マートのリセットを処理できませんでした。 後でもう一度お試しください。" というメッセージが表示されることがあります。
- リセットを実行すると、統合タスクが無効にされ、すべてのデータ マート データが削除されます。 この統合の有効化されます。

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>データ マートをリセットすると、デザインしたレポートが失われますか。 
いいえ、レポートは、データ マートのリセットの影響を受けない SQL テーブルに格納されます。 デザインしたレポートが失われるのではないかと心配な場合は、失いたくないデザインをバックアップできます。 バックアップするには、レポート デザイナーを開いて **会社 > 会社 > 構成要素 > エクスポート** をクリックします。
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>すべてのユーザーがシステムを終了してデータ マートをリセットする必要がありますか。
いいえ、ユーザーはデータ マート リセットしてもシステムで作業を続行できます。 ただし、リセットが完了するまで、Financial Reporter で作成されたレポートにはアクセスできません。 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
