---
title: 販売履歴クリーンアップ パフォーマンスの改善
description: このトピックでは、販売履歴クリーンアップのパフォーマンス改善機能、およびこれを有効にする方法について説明します。
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1b2de9d6a7b1b7793b6bb753dd580d052d3c2841
ms.sourcegitcommit: 96515ddbe2f65905140b16088ba62e9b258863fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2021
ms.locfileid: "7891771"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>販売履歴クリーンアップ パフォーマンスの改善

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.24 -->

**販売更新履歴のクリーンアップ** の定期的なバッチ ジョブは、大量の販売更新がある環境で頻繁に実行されないと、時間がかかることがあります。 このような場合は、*販売履歴クリーンアップのパフォーマンス改善* を使用すると、実行期間の短縮と信頼性の改善に役立ちます。

この機能により、次の方法で既存のクリーンアップ ジョブが改善します。

- クリーンアップはバッチに分割されます (カスタマイズしてバッチ サイズを変更できます)。
- 最大 2 時間実行されます (カスタマイズして期間を変更できます)。
- 可能であれば、データベース機能を活用して、競合のロックを最小限にし、クリーンアップ中にトランザクション テーブルが入らないようにします。

この機能を有効にした後、**販売更新履歴のクリーンアップ** バッチ ジョブ (**販売およびマーケティング \> 期間タスク \> クリーンアップ \> 販売更新履歴クリーンアップ**) が以前と同じ方法で実行されますが、パフォーマンスは改善し、最大 2 時間実行されます。 つまり、特定の保管期間のすべてのデータをクリーンアップするために何度か実行する必要がある場合があります。

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>販売履歴クリーンアップ パフォーマンスの改善機能をオンにする

この機能を使用するには、システム上で有効にする必要があります。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。 **機能管理** ワークスペースで、この機能は次のようにリストされています。

- **モジュール:** *販売とマーケティング*
- **機能名:** *販売履歴クリーンアップ パフォーマンスの改善*
