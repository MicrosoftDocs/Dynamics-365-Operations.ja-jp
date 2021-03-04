---
title: 先日付小切手の設定
description: このトピックでは、先日付小切手の仕訳入力を転記するかどうかと、どの転記仕訳帳を清算項目と仕入先支払に使用するかを指定する方法について説明します。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445252"
---
# <a name="set-up-postdated-checks"></a>先日付小切手の設定

[!include [banner](../../includes/banner.md)]

このトピックでは、先日付小切手の仕訳入力を転記するかどうかと、どの転記仕訳帳を清算項目と仕入先支払に使用するかを指定する方法について説明します。 発行済小切手、受領済小切手、および源泉徴収税の精算勘定も指定できます。 将来の日付で支払を履行または受け取るために発行される先日付小切手です。 小切手が、その有効期限前に、会計帳簿に反映する必要があるかどうかを指定できます。



この手順のロールは会計登録者です。 この手順では、USMF というデモ会社を使用します。


## <a name="set-up-postdated-checks"></a>先日付小切手の設定
1. [現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。
2. [先日付小切手] タブをクリックします。
3. [先日付小切手の有効化] チェック ボックスをオンまたはオフにします。
4. [先日付小切手用の仕訳入力の転記] チェック ボックスをオンまたはオフにします。
5. [発行済の小切手の清算勘定] フィールドで、任意の値を指定します。
6. [受領済みの小切手の清算勘定] フィールドで、任意の値を指定します。
7. [清算項目用の一般仕訳帳] フィールドに値を入力します。
8. [この仕入先の支払仕訳帳への先日付小切手の転送] フィールドに値を入力します。
9. [源泉徴収税の清算勘定] フィールドで、任意の値を指定します。
10. [保存] をクリックします。
11. ページを閉じます。
12. [買掛金勘定] > [支払設定] > [支払方法] の順に移動します。
13. [新規] をクリックします。
14. [支払方法] フィールドに値を入力します。
15. 小切手金額を精算勘定に転記されたことを示すには、[先日付小切手の清算の転記] オプションを選択します。
16. [勘定タイプ] フィールドで、「銀行」を選択します。
    * 支払方法の相手勘定は銀行となります。  
17. [支払勘定] フィールドで、任意の値を指定します。
    * 請求書額を控除するために使用される銀行口座を選択します。  
18. [保存] をクリックします。
19. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]