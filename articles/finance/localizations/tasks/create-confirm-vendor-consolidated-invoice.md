---
title: 仕入先月次締め請求書の作成および確認
description: 日本では、その月の販売請求書および仕入請求書は、未払金額を計算するため月末に連結されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendConsInvoice_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4f0b8207dde38cdc542f9aa18d42c20843ac546
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145253"
---
# <a name="create-and-confirm-a-vendor-consolidated-invoice"></a>仕入先月次締め請求書の作成および確認

[!include [banner](../../includes/banner.md)]

日本では、その月の販売請求書および仕入請求書は、未払金額を計算するため月末に連結されます。 



このタスクでは、仕入先の月次締め請求書の作成と確定について説明します。



このタスクを完了するためには、仕入請求書の転記が完了している必要があります。 



このタスクは デモ データ会社 JPMF を使用して作成されました。

1. [買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
2. [新規] をクリックします。
3. [実行日] フィールドに日付を入力します。
4. [以下で指定する月次締め日の使用] チェックボックスをオンまたはオフにします。
    * 月次締め日を上書きする場合は、[月次締め日の使用] のスライダーを「はい」に指定する必要があります。  
5. [月次締め日] フィールドに日付を入力します。
    * 例: 月次締め日が 25 日の場合、このスライダーを「はい」に設定していれば、24 日に連結を実行できます。 [月次締め日] は手動で指定する必要があります。  
6. [OK] をクリックします。
    * 生成された月次締め請求書を確認します。  
7. 一覧で、選択された行のリンクをクリックします。
    * グリッド内の [月次締め請求書] の [締め ID] をクリックして [月次締め請求書] ページの詳細表示に切り替えます。  
    * 請求済の発注書が月次締め請求書に含まれていることを確認します。  
8. [確認] をクリックします。

