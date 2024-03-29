---
title: 適用できる価格および割引の検索
description: この手順は、特定の顧客に対して現在有効な製品の価格や割引を、販売注文を作成せずに検索する方法を示します。
author: Henrikan
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c80ae00e1bcbc4498ec4705195c3208170cee1b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578923"
---
# <a name="look-up-applicable-prices-and-discounts"></a>適用できる価格および割引の検索

[!include [banner](../../includes/banner.md)]

この手順は、特定の顧客に対して現在有効な製品の価格や割引を、販売注文を作成せずに検索する方法を示します。 この手順では、特定の例について説明します。必要な値を選択するには、USMF のデモ会社を使用したこの例に従う必要があります。


## <a name="find-the-applicable-price"></a>適用できる価格の検索
1. [販売とマーケティング] > [価格と割引] > [価格の検索] の順に移動します。
2. [顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. リストで、顧客 US-001 を見つけ、選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. [品目番号] フィールドに、'T0004' を入力します。
    * 既定では、[数量] フィールドは 1 に設定されています。 ただし、顧客が対象製品に対して予定している注文のサイズがわかっている場合は、代わりにこの値を入力します。 この情報は、顧客との売買契約に数量の区分があるかどうかに関連しています。つまり、製品の価格は購買最小数量に依存します。  
6. [日付] フィールドで、顧客が注文を発注する予定の日付を入力します。 
    * 日付には、今日、または将来の任意の日付を指定できます。  
    * 指定された数量で選択した日付に選択した顧客によって購入された場合、システムは選択した製品で有効になる価格を返します。 この例では、今日、顧客 US-001 が製品 T0004 を 1 単位購入した場合、その製品は 1 単位 350 CAD に変更されます。 この価格は、既存で有効な、顧客との売買契約から取得されます。      ページの他のフィールドでは、(製品マスターで設定されている場合) 製品価格と製品原価、および計算される収益性に関する詳細情報を確認できます。  
    * [関連製品バリアントの表示] オプションを選択した場合、製品バリアントに追加の売買契約があることを意味します。  
7. [関連製品バリアントの表示] チェック ボックスをクリックします。
    * 製品バリアントの一覧が、分析コードに関する情報とともに表示されます。  
8. リストで、白色を表す明細行にマークを付けます。
    * 製品価格は、分析コードごとに指定されていなかった場合、以前に表示されたものとは異なることに注意してください。  
9. [販売価格の表示] をクリックします。
    * [価格 (販売)] ページには、バリアントを含めた、製品に適用可能なすべての売買契約が表示されます。  
10. ページを閉じます。

## <a name="find-the-applicable-discount"></a>適用できる割引の検索
[顧客口座] フィールドには顧客番号 US-001 が含まれていることを確認してください。   
1. [品目番号] フィールドに、'T0012' を入力します。
    * [数量] フィールドが 1 に設定されていることを確認してください。  
    * 製品 T0012 に表示される次の価格決定の詳細は、複数の売買契約から取得されます: 単価は 1,000 CAD で、割引率は 5 です。  
2. 数量を '20' に設定します。
    * 注文数量の増加は、5 から 7% に変更予定の顧客に対する行割引によるものです。  
    * 正味金額は、単価、割引、合計数量に基づいて計算されます。  
3. [行割引の表示] をクリックします。
    * 製品 T0012 には、2 つの行割引契約があります。つまり、1 から 10 の注文明細行数量で 5% の割引が指定され、10 以上では注文数量が 7％ 割引されています。 割引は、製品グループ、この例では、製品 T0012 が所属するグループ コード 01 に適用されることに注意してください。  
4. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]