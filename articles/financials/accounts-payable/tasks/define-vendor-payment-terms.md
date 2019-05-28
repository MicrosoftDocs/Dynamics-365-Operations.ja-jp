---
title: 仕入先の支払条件の定義
description: 仕入先請求書の支払条件を設定します。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68c69d5be5ccbdfb17fea7c61121cbf26fee48d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569035"
---
# <a name="define-vendor-payment-terms"></a>仕入先の支払条件の定義

[!include [task guide banner](../../includes/task-guide-banner.md)]

仕入先請求書の支払条件を設定します。 このタスクでは、USMF というデモ会社を使用します。

1. [買掛金勘定] > [支払設定] > [支払条件] の順に移動します。
2. [新規] をクリックします。
    * 支払条件のページは期日を計算する方法を定義するために使用されます。 このページは現金割引日を計算する方法を定義するために使用されてはいません。  
3. [支払条件] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [日] フィールドに数値を入力します。
    * ここで入力された数値は、期日に、または支払方法で指定した期間の終了時に追加するために使用されます。 たとえば、「正味」を選択する場合、数値は期日に追加されます。 「現在の月」を選択する場合、期日を計算するために、数値は現在の月の最終日に追加されます。  
6. [保存] をクリックします。
7. ページを閉じます。
8. [買掛金勘定] > [支払設定] > [現金割引] の順に移動します。
9. [新規] をクリックします。
10. [現金割引] フィールドに ID を入力します。
11. [説明] フィールドに値を入力します。
12. 仕入先が階層化された割引を提供すると、現在の割引の有効期限が経過した後に次の現金割引を選択します。
13. ページを閉じます。
14. [日] フィールドに数値を入力します。
    * [日] フィールドに入力された数量は、[正味/現在] フィールドで選択したオプションに基づいて現金割引日を計算するために使用されます。 正味を選択した場合、数量が請求日に追加され、現金割引日が特定されます。 「現在の月」を選択した場合、数量が当月末に追加され、現金割引日が特定されます。  
15. [割引] フィールドに、現金割引率を入力します。 
16. 現金割引が転記される顧客請求書用の主勘定を入力します。
17. 現金割引が転記される仕入先請求書用の主勘定を入力します。
    * 「割引の相手勘定」に「仕入先割引の主勘定を使用」が設定されている場合、主勘定が使用されるようになります。  オプションで「請求明細行の勘定」を選択した場合、現金割引は、請求書明細行の資産/経費用勘定に転記されるようになります。  
18. [保存] をクリックします。

