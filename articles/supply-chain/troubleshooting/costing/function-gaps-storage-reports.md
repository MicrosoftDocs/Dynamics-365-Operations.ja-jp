---
title: 在庫金額/エイジング レポートとそのストレージ バージョンの間の機能的なギャップ
description: 在庫金額/エイジング レポートとそのストレージ バージョンの間の機能的なギャップ
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f74389648034bf036ce48ac84b3421a8a340f105
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686656"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>在庫金額/エイジング レポートとそのストレージ バージョンの間の機能的なギャップ

[在庫エイジング レポート ストレージ](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage)および[在庫金額のストレージ レポート](/dynamics365/supply-chain/cost-management/inventory-value-report-storage)機能では、Supply Chain Management を使用して大量の在庫トランザクションを表示できます。 いずれの場合も、これらのレポートの非ストレージ バージョンとは異なり、レポート結果は、参照とエクスポートのために保存されます。 ただし、これらのレポートの非ストレージ バージョンに存在する機能のいくつかは、ストレージ バージョンには存在しません。 以下のサブセクションでは、この違いについて説明し、回避策を示します。

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>ストレージ レポートには、レポート レイアウトで有効になっている場合でも、小計は含まれません。

小計は、特にレコード シーケンスが変更された場合、結果がエクスポートされるときに問題が発生することがあります。

小計をチェックするには、結果を Microsoft Excel にエクスポートします。 または、Supply Chain Management の中で小計をチェックする場合は、[機能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を使用して、*新しいグリッド コントロール* と *グリッド内でのグループ化* 機能を有効にします。これにより、グループの小計をはるかに柔軟な方法で列ごとに表示できます。 詳細については、[グリッド機能](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities) を参照してください。

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>在庫金額ストレージ レポートでは、勘定科目情報はサポートされない

試算表を実行して在庫勘定の残高を取得し、**在庫金額ストレージ** レポートと比較することができます。
