---
title: 販売更新履歴のクリーンアップ ジョブが失敗するか、パフォーマンスに問題があります
description: 大量の販売更新データがある場合は、販売履歴のクリーンアップ バッチ ジョブが失敗したり、非常に長くかかる場合があります。
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
ms.openlocfilehash: 4f04dc204c705b40ed25fadc75118feaef4d6b6e
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641469"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>販売更新履歴のクリーンアップ ジョブが失敗するか、パフォーマンスに問題があります

## <a name="symptoms"></a>現象

**販売更新履歴のクリーンアップ** バッチ ジョブが失敗するか、パフォーマンスに問題があります。  

## <a name="cause"></a>原因

これは、システムに大量の販売更新が含まれる場合に発生し、その結果、大量の販売更新データにつながります。 このクリーンアップ ジョブによって、1 つのトランザクション内のすべてのデータのクリーンアップが試行されます。 その結果、ジョブの実行に非常に長い時間がかかる場合や失敗する場合があります。

## <a name="resolution"></a>解決策

**販売更新履歴クリーンアップ** バッチ ジョブの新しいバージョンが、Supply Chain Management のバージョン 10.0.19 以降で使用できます。 この機能は、規定では有効ではありません。 それの機能方法と機能管理でそれを有効にする方法の詳細については、[販売履歴のクリーンアップ パフォーマンスの改善](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md) を参照してください。

