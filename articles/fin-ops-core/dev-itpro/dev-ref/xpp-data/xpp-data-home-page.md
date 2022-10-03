---
title: X++ データの選択と操作の概要
description: この記事では、X++ データの選択と操作についてのトピックへのリンクを提供します。
author: josaw1
ms.date: 09/28/2022
ms.topic: overview
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5caaeeffc0a7981014cd5fbc20fe95738843dc6f
ms.sourcegitcommit: 97cf0c1d6ce0e2a535c67322134f6c31628548cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2022
ms.locfileid: "9596329"
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

[セット ベースからレコード単位への操作の変換](xpp-data-perf.md)の記事では、レコード セット ベースのステートメントおよびメソッドをより効率的に使用するための情報を提供します。

[SysDa クラス](../sysda.md)を使用してデータを取得および変更することもできます。 拡張可能な SysDa API では、X++ で使用できるほとんどすべてのデータアクセス可能性が提供されます。

**executeQueryWithParameters** API は、[SQL インジェクション攻撃の軽減](../query-with-parameters.md) に役立ちます。

結合の使用の詳細については、[Exists 結合および Notexists 結合についてのよくある誤解](https://community.dynamics.com/365/financeandoperations/b/peter-s-x-developer-blog/posts/common-misconception-about-exists-and-notexists-joins) を参照してください。

## <a name="sql-statement-timeout"></a>SQL ステートメントのタイムアウト

上記のすべての SQL ステートメントには、発行するセッション タイプに応じて、ステートメントごとにタイムアウトが設定されます。  

- **対話型** セッション - 30 分。
- **非対話型 (バッチ、サービス、OData)** - 3 時間。 

ブロックが原因で、または予想以上のデータ量やクエリ プランの問題で、ステートメントがタイムアウトした場合、メッセージ *クエリの実行中に、データベース内でタイムアウトが発生しました。* と共に型の例外 **Exception::Timeout** がスローされます X++ では、この例外に基づく処理タイムアウト例外および再試行を許可します。 既定のタイムアウトは、[queryTimeout API](/dotnet/api/microsoft.dynamics.ax.xpp.common.querytimeout) を呼び出すことによって上書きできます。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
