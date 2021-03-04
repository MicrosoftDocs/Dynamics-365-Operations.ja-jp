---
title: コスト管理のトラブルシューティング
description: このトピックでは、コスト管理を実行する際に発生する可能性がある問題の修正方法について説明します。
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e84bb167395c06295b0e8ef8b9fd98aa4bc0cc14
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4432408"
---
# <a name="troubleshoot-cost-management"></a>コスト管理のトラブルシューティング

このトピックでは、コスト管理を実行する際に発生する可能性がある問題の修正方法について説明します。

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>在庫金額/エイジング レポートとそのストレージ バージョンの間の機能的なギャップ

[在庫エイジング レポート ストレージ](inventory-aging-report-storage.md)および[在庫金額のストレージ レポート](inventory-value-report-storage.md)機能では、Supply Chain Management を使用して大量の在庫トランザクションを表示できます。 いずれの場合も、これらのレポートの非ストレージ バージョンとは異なり、レポート結果は、参照とエクスポートのために保存されます。 ただし、これらのレポートの非ストレージ バージョンに存在する機能のいくつかは、ストレージ バージョンには存在しません。 以下のサブセクションでは、この違いについて説明し、回避策を示します。

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>ストレージ レポートには、レポート レイアウトで有効になっている場合でも、小計は含まれません。

小計は、特にレコード シーケンスが変更された場合、結果がエクスポートされるときに問題が発生することがあります。

小計をチェックするには、結果を Microsoft Excel にエクスポートします。 または、Supply Chain Management の中で小計をチェックする場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して、*新しいグリッド コントロール* と *(プレビュー) グリッド内でのグループ化* 機能を有効にします。これにより、グループの小計を、はるかに柔軟な方法で列ごとに表示できます。 詳細については、[グリッド機能](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md) を参照してください。

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>在庫金額ストレージ レポートでは、勘定科目情報はサポートされない

試算表を実行して在庫勘定の残高を取得し、**在庫金額ストレージ** レポートと比較することができます。

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>在庫決算なしで元帳期間のステータスを変更すると、警告またはエラーが表示される

Microsoft では、決算に関する不適切な期末プロセスが原因で発生する問題を防止するために、次の検証を導入しました。 次のいずれかのエラー メッセージが表示される場合は、[KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) を参照して、これらの問題を解決する方法の詳細を確認してください。

- 日付 %1 (10-02-2019) を使用して再計算を実行しようとしています。 最後に登録された再計算は、日付 %2 (20-01-2019) で前期に実行されました。 期末と一致する日付 %3 (31-01-2019) での在庫決算の実行が登録されていません。 期末に一致する %3 (31-01-2019) の時点で在庫決算を実行することを忘れないでください。 補助元帳および総勘定元帳において、在庫評価、売却済の商品の原価、および差異は、この処理が実行されるまで正しくない可能性があります。

- 元帳期間 %1 のステータスを %2 に変更しようとしています。 期末と一致する日付 %3 での在庫決算の実行が登録されていません。 ステータスを変更する前に、期末と一致する %3 の時点で在庫決算を実行してください。 補助元帳および総勘定元帳において、在庫評価、売却済の商品の原価、および差異は、この処理が実行されるまで正しくない可能性があります。 法人 %4 から報告されました。 今のところは情報のみですが、将来はこのようなアクションを実行する必要があります。

- 勘定構造 %1 が変更されています。 1 つ以上の主勘定 %2 が存在しなくなっています。 これらの主勘定は、日付 %4 に %3 によって求められています。 %3 ジョブを再開するには、これらの主勘定を勘定構造 %1 に追加してください。 今のところは情報のみですが、将来はこのようなアクションを実行する必要があります。

- 日付 %1 (31-01-2019) を使用して在庫決算を実行しようとしています。 期末と一致する日付 %2 (31-01-2019) での一括引き落とし原価計算の実行が登録されていません。 期末と一致する日付 %3 (31-01-2019) での一括引き落とし原価計算を必ず実行してください。 補助元帳および総勘定元帳において、在庫評価、売却済の商品の原価、および差異は、この処理が実行されるまで正しくない可能性があります。

- 日付 %1 (28-02-2019) で一括引き落とし原価計算を実行しようとしています。 最後に登録された一括引き落とし原価計算は、日付 %2 (31-01-2019) で前期に実行されました。 期末と一致する日付 %3 (31-01-2019) での在庫決算の実行が登録されていません。
期末に一致する %3 (31-01-2019) の時点で在庫決算を実行することを忘れないでください。 補助元帳および総勘定元帳において、在庫評価、売却済の商品の原価、および差異は、在庫決算が実行されるまで正しくない可能性があります。

## <a name="inventory-aging-report-discrepancies"></a>在庫エイジング レポートの差異

**在庫エイジング レポート** には、さまざまな保管分析コード (サイトや倉庫など) で表示した場合、異なる値が表示されます。 レポート ロジックの詳細については、[在庫エイジング レポートの例とロジック](inventory-aging-report.md)を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]