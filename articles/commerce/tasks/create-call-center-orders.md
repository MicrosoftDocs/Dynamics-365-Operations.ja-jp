---
title: コール センター注文の作成
description: この手順では、顧客の検索、新しい注文の作成、製品の検索、および顧客から支払を回収する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08a806514a92a99a9f0b18b36817f49a09516ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964848"
---
# <a name="create-call-center-orders"></a>コール センター注文の作成

[!include [banner](../includes/banner.md)]

この手順では、顧客の検索、新しい注文の作成、製品の検索、および顧客から支払を回収する方法について説明します。 この手順では、デモ データの会社 USRT を使用して、販売注文の担当者を対象としています。 前提条件: 手順を完了するユーザーが、コール センター ユーザーとして設定され、Fabrikam Semi-Annual Catalog が少なくとも 1 つのソースコードと共に公開されています。

1. **Retail と Commerce \> 顧客 \> 顧客サービス** に移動します。
2. **検索文字列** には、顧客を検索するための検索条件を入力します。
    * この手順の例では、「Karen」を入力し、**タブ** を選択します。  
3. 検索 を選択します。
    * デモ データに「Karen」という名前の顧客が 1 人だけいるため、それが自動的に選択されます。  
4. **新しい販売注文** を選択します。
5. **販売注文** ヘッダー セクションを展開または折りたたみます。
6. カタログのソース コードを選択します。
    * 有効なソース・コードがない場合、この手順を省略できます。  
7. **明細行の追加** を選択します。
8. **品目番号** では、品目の検索用語を入力します。
    * このサンプルの手順については、品目番号の一部の「8111」を入力し、タブをクリックします。すると、品目の検索ウィンドウが表示されます。  
9. 販売注文に追加する製品を選択します。
10. 販売数量を入力します。
11. **作成** を選択します。
12. 顧客支払を取得するために、**完了** を選択します。
13. **追加** を選択します。
    * [追加] リンクは、[支払] タブにあります。[支払] タブが折りたたまれている場合、展開します。  
14. 支払方法を選択します。
    * この手順では、支払方法は現金を選択します。  
15. ページを閉じます。
16. 金額を入力します。
    * この手順では、販売注文の概要ページに表示される注文の残高と同じ金額を、金額フィールドの左側に入力します。 全額支払われるように注文を行うことができます。  
17. **OK** を選択します。
18. **送信** を選択します。

## <a name="additional-resources"></a>追加リソース

[配送モードによるトランザクション メールのカスタマイズ](../customize-email-delivery-mode.md)

[POS での荷渡方法の変更](../pos-change-delivery-mode.md)

