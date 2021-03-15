---
title: 顧客月次締め請求書の作成および確認
description: 日本では、その月の販売請求書および仕入請求書は、未払金額を計算するため月末に連結されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustConsInvoice_JP
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ad904c8b89810cca1021cfc6e3adca9cc9c0f9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961359"
---
# <a name="create-and-confirm-a-customer-consolidated-invoice"></a>顧客月次締め請求書の作成および確認

[!include [banner](../../includes/banner.md)]

日本では、その月の販売請求書および仕入請求書は、未払金額を計算するため月末に連結されます。 



このタスクでは、月締め請求書の作成と確定方法について説明します。 



このタスクを完了するためには、販売請求書または仕入請求書が事前に転記されている必要があります。



この手順では、JPMF デモ会社のデータを使用します。

1. [売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
2. [新規] をクリックします。
    * 既定の [実行日] はセッション日付です。  
    * 月次締め日を上書きする場合は、[以下で指定する月次締め日の使用] スライダーを「はい」に指定します。  
    * 例: 月締め日が 25 日に指定されている場合、このスライダーが「はい」に設定されていれば、24 日に連結を実行できます。 [月次締め日] は手動で指定する必要があります。  
3. [OK] をクリックします。
    * [月次締め請求書] が生成されていることを確認します。  
    * 1 つの月次締め請求書に記載されるのは 1 つのの顧客 ID だけです。 連結する顧客 ID が複数ある場合は、複数の月次締め請求書が生成されます。  
4. 一覧で、選択された行のリンクをクリックします。
    * グリッド内の [月次締め請求書] の [締め ID] をクリックして [月次締め請求書] ページの詳細表示に切り替えます。  
    * 請求済の販売注文が月次締め請求書に含まれていることを確認します。  
5. [確認] をクリックします。
    * [確定] をクリックすると、[月次締め請求書のステータス] は「確定済」に変わります。 確定後、月次締め請求書はロックされ編集できません。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]