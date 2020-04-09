---
title: 連続プログラムの使用
description: この手順では、連続プログラムの販売と関連する販売注文の処理について説明します。
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baf0127a35cc62952fd78daaf8204d35ec8d2b3
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141157"
---
# <a name="using-continuity-program"></a>連続プログラムの使用

[!include [banner](../includes/banner.md)]

この手順では、連続プログラムの販売と関連する販売注文の処理について説明します。 この手順を完了するには、コール センターのユーザーとして設定する必要があります。 この手順では、デモ データの会社 USRT を使用します。

1. Retail とコマース > 顧客 > 顧客サービスに移動します。
2. SearchText フィールドに、「Karen」を入力し、タブ キーを押します。
    * 高度な検索ダイアログがポップアップするはずです。 表示されない場合は、このフィールドの右側にある [検索] をクリックします。  
3. 一覧で、選択された行をマークします。
    * Karen Berg の表示は 1 行のみのはずです。 グリッドの左側のチェックマークの列をクリックして行を選択します。  
4. [選択] をクリックします。
5. [新しい販売注文] をクリックします。
    * 販売注文番号を確認することを推奨します。 この手順の後半で、それが必要になります。  
6. [品目番号] フィールドに、「88000」を入力し、[タブ] キーを押します。
    * これは、USRT デモ データの連続品目です。  
7. [完了] をクリックします。
8. [支払方法] フィールドに、「Visa」を入力します。
9. [クレジット カードの追加] をクリックします。
    * このページに必須のクレジット カード情報を入力します。  
10. [OK] をクリックします。
11. [支払] セクションを展開します。
    * コール センター 注文を送信するには、注文の支払いを入力する必要があります。  
12. [OK] をクリックします。
13. [送信] をクリックします。
    * 新しい連続注文が作成されています。 次に、連続オーダーを処理するのに使用される、2 つのバッチ処理を実行します。  
14. ページを閉じます。
15. Retail とコマース > 連続 > 連続の支払いへ移動します。
16. [連続品目] フィールドに、「88000」を入力し、[タブ] キーを押します。
17. [OK] をクリックします。
18. Retail とコマース > 連続 > 連続子注文の作成へ移動します。
    * このプロセスは、連続プログラムの設定に基づいて新しい販売注文を作成します。  
19. [連続品目] フィールドに、「88000」を入力し、[タブ] キーを押します。
    * 品目「88000」は、USRT デモ データの連続品目です。  
20. [販売注文] フィールドで、値を入力または選択します。
    * 前の手順でメモした販売注文番号を入力します。 これにより、この手順の処理時間は最小限に抑えられます。 [販売注文] フィールドはオプションです--いずれかのプログラムのすべての注文を処理することができます。  
21. [OK] をクリックします。

