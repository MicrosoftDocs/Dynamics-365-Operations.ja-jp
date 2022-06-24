---
title: 会社間注文をフィルター処理して Orders および OrderLines の同期を回避する
description: この記事では、会社間注文をフィルタ処理して、Orders と OrderLines エンティティが同期されないようにする方法について説明します。
author: negudava
ms.date: 11/09/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: negudava
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 47d5cc358165d9a870892e0d026948d65343e5f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910354"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>会社間注文をフィルター処理して Orders および OrderLines の同期を回避する

[!include [banner](../../includes/banner.md)]

会社間注文をフィルター処理して **Orders** テーブルと **OrderLines** テーブルが同期されないようにすることができます。 一部のシナリオでは、Customer Engagement アプリで会社間注文の詳細は必要ありません。

各標準 Dataverse テーブルは、**IntercompanyOrder** 列への参照を使用して拡張され、デュアル書き込みマップは、フィルターの追加列を参照するように変更されます。 したがって、会社間注文は同期されなくなります。 このプロセスは、Customer Engagement アプリで不要なデータを防ぐことができます。

1. **IntercompanyOrder** 列への参照を追加して、**CDS 販売注文ヘッダー** テーブルを拡張します。 この列は、会社間注文でのみ入力されます。 **IntercompanyOrder** 列は、**SalesTable** テーブルで使用できます。

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="CDS 販売注文ヘッダーのターゲット ページにステージングをマップする。":::

2. **CDS 販売注文ヘッダー** が拡張されたら、マッピングで **IntercompanyOrder** 列が使用可能になります。 クエリ文字列として `INTERCOMPANYORDER == ""` を含むフィルターを適用します。

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CDS 販売注文ヘッダーのクエリ ダイアログ ボックスを編集する。":::

3. **IntercompanyInventTransId** 列への参照を追加して、**CDS 販売注文明細行** テーブルを拡張します。 この列は、会社間注文でのみ入力されます。 **InterCompanyInventTransId** 列は、**SalesLine** テーブルで使用できます。

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="CDS 販売注文明細行のターゲット ページにステージングをマップする。":::

4. **CDS 販売注文明細行** が拡張されたら、マッピングで **IntercompanyInventTransId** 列が使用可能になります。 クエリ文字列として `INTERCOMPANYINVENTTRANSID == ""` を含むフィルターを適用します。

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CDS 販売注文明細行のクエリ ダイアログ ボックスを編集する。":::

5. 手順 1 と 2 を繰り返して、**売上請求書ヘッダー V2** テーブルを拡張し、フィルター クエリを追加します。 この場合は、フィルターのクエリ文字列として `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` を使用します。

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="売上請求書ヘッダー V2 のターゲット ページにステージングをマップする。":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="売上請求書ヘッダー V2 のクエリ ダイアログ ボックスを編集する。":::

6. 手順 3 と 4 を繰り返して、**売上請求明細行 V2** テーブルを拡張し、フィルター クエリを追加します。 この場合は、フィルターのクエリ文字列として `INTERCOMPANYINVENTTRANSID == ""` を使用します。

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="売上請求明細行 V2 のクエリ ダイアログ ボックスを編集する。":::

7. **見積書** テーブルには会社間関係がありません。 他のユーザーが会社間顧客に対する見積を作成した場合は、**CustGroup** 列を使用して、そのすべての顧客を 1 つの顧客グループに含めることができます。 **CustGroup** 列を追加してヘッダーと行を拡張し、グループが含まれないようにフィルター処理できます。

    :::image type="content" source="media/filter-cust-group.png" alt-text="CDS 販売見積書ヘッダーのターゲット ページにステージングをマップする。":::

8. **見積書** を拡張した後、クエリ文字列として `CUSTGROUP != "<company>"` を含むフィルターを適用します。

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS 販売見積ヘッダーのクエリ ダイアログ ボックスを編集する。":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]