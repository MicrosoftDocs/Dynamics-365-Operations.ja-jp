---
title: X++ データの選択と操作の概要
description: このトピックでは、X++ データの選択と操作についてのトピックへのリンクを提供します。
author: robinarh
ms.date: 06/16/2020
audience: Developer
ms.reviewer: rhaertle
ms.custom: intro-internal
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 54f6e7a48a77d1f51a8a39102bebf22723894542995c9feb605d2b0a3fb15958
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769860"
---
# <a name="x-data-selection-and-manipulation-overview"></a>X++ データの選択と操作の概要

[!include [banner](../../includes/banner.md)]

データベースに格納されているデータを取得し変更するため、SQL ステートメントを対話式またはソース コード内で使用することができます。 これらのタスクには、**select** ステートメントおよび API メソッドを使用できます。

- [データの選択](xpp-select.md): 表示または変更するデータを選択します。

    - **[select](xpp-select-statement.md) ステートメント** – レコードをフェッチします。

- [データの挿入](xpp-insert.md): 1 つ以上の新しいレコードをテーブルに追加します。

    - **[insert](xpp-insert.md#insert-method) および [doInsert](xpp-insert.md#do-insert-method) メソッド** – 一度に 1 つのレコードを挿入します。
    - **[insert\_recordset](xpp-insert.md#insert-recordset-statement)、[RecordInsertList.insertDatabase](/dotnet/api/dynamics.ax.application#method-insertdatabase)、および [RecordSortedList.insertDatabase](/dotnet/api/dynamics.ax.application#method-insertdatabase) メソッド** – 複数のレコードを同時に挿入します。

- [データの更新](xpp-update.md): 既存のテーブル レコードでデータを変更します。

    - **[update](xpp-update.md#update-method) および [doUpdate](xpp-update.md#do-update-method) メソッド** – 一度に 1 つのレコードを更新します。
    - **[update\_recordset](xpp-update.md#update-recordset-statement) ステートメント** – 複数のレコードを同時に更新します。

- [データの削除](xpp-delete.md): 既存のレコードをテーブルから削除します。

    - **[delete](xpp-delete.md#delete-method) および [doDelete](xpp-delete.md#do-delete-method) メソッド** – 一度に 1 つのレコードを削除します。
    - **[delete\_from](xpp-delete.md#delete-from-statement) ステートメント** – 複数のレコードを同時に削除します。

データ アクセスに使用するその他のステートメントを次に示します。

- [while select](xpp-while-select.md) ステートメント
- [select](xpp-select-expression.md) 式
- [next](xpp-select.md) ステートメント

[トランザクションの整合性](xpp-transaction.md) により、データの破損を防ぎ、スケーラビリティを向上させることができます。

[セット ベースからレコード単位への操作の変換](xpp-data-perf.md) トピックでは、レコード セット ベースのステートメントおよびメソッドをより効率的に使用するための情報を提供します。

[SysDa クラス](../sysda.md)を使用してデータを取得および変更することもできます。 拡張可能な SysDa API では、X++ で使用できるほとんどすべてのデータアクセス可能性が提供されます。

**executeQueryWithParameters** API は、[SQL インジェクション攻撃の軽減](../query-with-parameters.md) に役立ちます。

結合の使用の詳細については、[Exists 結合および Notexists 結合についてのよくある誤解](https://community.dynamics.com/365/financeandoperations/b/peter-s-x-developer-blog/posts/common-misconception-about-exists-and-notexists-joins) を参照してください。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
