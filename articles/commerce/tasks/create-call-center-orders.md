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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ec10e0f79e4eca7f51ba48c679dcf6fe745eb29
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141433"
---
# <a name="create-call-center-orders"></a>コール センター注文の作成

[!include [banner](../includes/banner.md)]

この手順では、顧客の検索、新しい注文の作成、製品の検索、および顧客から支払を回収する方法について説明します。 この手順では、デモ データの会社 USRT を使用して、販売注文の担当者を対象としています。 前提条件: 手順を完了するユーザーが、コール センター ユーザーとして設定され、Fabrikam Semi-Annual Catalog が少なくとも 1 つのソースコードと共に公開されています。

1. Retail とコマース > 顧客 > 顧客サービスに移動します。
2. [検索文字列] フィールドで、顧客を検索するための検索条件を入力します。
    * この手順の例では、「開発者」を入力し、タブをクリックします。  
3. [検索] をクリックします。
    * デモ データに開発者という名前の顧客が一人だけあるため、それが自動的に選択されます。  
4. [新しい販売注文] をクリックします。
5. [販売注文ヘッダー] セクションを展開または折りたたみます。
6. カタログのソース コードを選択します。
    * 有効なソース・コードがない場合、ソース フィールドを閉じ、この手順を省略できます。  
7. [明細行の追加] をクリックします。
8. [品目番号] フィールドで、品目の検索用語を入力します。
    * このサンプルの手順については、品目番号の一部の「8111」を入力し、タブをクリックします。品目の検索ウィンドウがポップアップ表示されます。  
9. 販売注文に追加する製品を選択します。
10. 販売数量を入力します。
11. [作成] をクリックします。
12. 顧客支払を取得するために、[完了] をクリックします。
13. [追加] をクリックします。
    * [追加] リンクは、[支払] タブにあります。[支払] タブが折りたたまれている場合、展開します。  
14. 支払方法を選択します。
    * この手順では、支払方法は現金を選択します。  
15. ページを閉じます。
16. 金額を入力します。
    * この手順では、販売注文の概要ページに表示される注文の残高と同じ金額を、金額フィールドの左側に入力します。 全額支払われるように注文を行うことができます。  
17. [OK] をクリックします。
18. [送信] をクリックします。

