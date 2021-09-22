---
title: 最小在庫管理単位の最大小数点以下桁数が 0
description: 在庫トランザクションや在庫引当を転記しようとする場合、"最小在庫管理単位の最大小数点以下の桁数は 0 です" というエラーが表示されます。
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476915"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>最小在庫管理単位の最大小数点以下桁数が 0


## <a name="symptoms"></a>現象

在庫トランザクションまたは在庫引当を転記しようとする場合、次のエラー メッセージが表示されます。

> 最小在庫管理単位の最大小数点以下桁数は 0 です。

この問題は、在庫トランザクションの数量が、フィールドでサポートされる精度レベルを下回る小数の値として指定されている場合に発生します。 たとえば、在庫トランザクションに対して数量 *0.5* が指定されている一方で、サポートされているのは整数数量のみです。 したがって、値は *0.5* の代わりに *1* にする必要があります。

## <a name="resolution"></a>解決策

1. 在庫トランザクションの数量を丸めるには、SQL Server インスタンスで次のスクリプトを実行します。 このスクリプトは **inventTrans** テーブルの値を修正します。

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. **修正エラー** オプションが有効になっているという一貫性の確認を実行します。 このチェックは、**inventSum** テーブルの値を修正します。

> [!IMPORTANT]
> 実稼働環境でスクリプトを実行する前に、必要に応じてスクリプトを入念に編集し、テスト環境でテストしてから、結果のデータを確認することを強く推奨します。
