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
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe33ecbb1c330b65cbc910e08b297d287cdbfa14
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175150"
---
# <a name="create-and-confirm-a-customer-consolidated-invoice"></a>顧客月次締め請求書の作成および確認

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

