---
title: 仕入先月次締め請求書の作成および確認
description: このトピックでは、毎月の仕入先の請求書を集約して支払額を算出する方法を説明しています。
author: ShylaThompson
ms.date: 10/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendConsInvoice_JP
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e892129f7593fb61a71cef5b8811fa222f87bfd1
ms.sourcegitcommit: 2fba4f2ef7e513357366fc640befe0d2f7bc31f5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/05/2021
ms.locfileid: "7601520"
---
# <a name="create-and-confirm-a-vendor-consolidated-invoice"></a>仕入先月次締め請求書の作成および確認

[!include [banner](../../includes/banner.md)]

日本では、その月の販売請求書および仕入請求書は、未払金額を計算するため月末に連結されます。 

このタスクでは、仕入先の月次締め請求書の作成と確定について説明します。

このタスクを完了するためには、仕入請求書の転記が完了している必要があります。 

このタスクは デモ データ会社 JPMF を使用して作成されました。

1. **買掛金勘定** > **定期処理タスク** > **月次締め請求書** の順に移動します。
2. **新規** を選択し、 **実行日** フィールドに日付を入力します。
3. **以下で指定する月次締め日の使用** チェックボックスをオンまたはオフにします。 月次締め日を上書きする場合は、**月次締め日の使用** のスライダーを **はい** に指定する必要があります。  
4. **月次締め日** フィールドに日付を入力します。 例: 月次締め日が 25 日の場合、このスライダーを **はい** に設定していれば、24 日に連結を実行できます。 月次締め日は手動で指定する必要があります。  
5. **OK** を選択します。 生成された月次締め請求書を確認します。  
6. 一覧で、選択した行のリンクを選択します。 グリッド内の [月次締め請求書] の [締め ID] を選択して **月次締め請求書** ページの詳細表示に切り替えます。  
7. 請求済の発注書が月次締め請求書に含まれていることを確認し、**確認** を選択します。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
