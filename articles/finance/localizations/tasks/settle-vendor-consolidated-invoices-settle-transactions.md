---
title: 決済トランザクションを使用した仕入先月次締め請求書の決済
description: 日本では、支払は月次締め請求書に対して行われ決済されます。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendConsInvoice_JP, VendTable, VendOpenTrans
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8da8be016a85ae10a8d62a7f373168ded8a212df
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566107"
---
# <a name="settle-vendor-consolidated-invoices-by-using-settle-transactions"></a>決済トランザクションを使用した仕入先月次締め請求書の決済

[!include [banner](../../includes/banner.md)]

日本では、支払は月次締め請求書に対して行われ決済されます。



この手順では、決済トランザクションを使用した月次締め請求書の決済について説明します。



この手順を実行する前に、月次締め請求書が作成され確定済であること、および支払いが転記されていることを確認する必要があります。 



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="confirm-consolidation-invoice-to-be-settled"></a>決済される月次締め請求書の確定
1. [買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
2. 後で参照するために、[締め ID] フィールドの値をメモします。
    * 決済する月次締め請求書のステータスが「確定済」であることを確認します。    この例: 締め ID - JPMF-000004  

## <a name="settle-consolidation-invoice"></a>月次締め請求書の決済 
1. [買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * 月次締め請求書を決済する仕入先を選択します。 この例では、JPMF-000002 を使用します。  
3. アクション ウィンドウで、[請求書] をクリックします。
4. [トランザクションの決済] をクリックします。
5. 一覧で、目的のレコードを見つけ、選択します。
    * [締め ID] が JPMF-000004 のレコードを選択します。  
6. [マーク] のチェック ボックスをオンまたはオフにします。
    * [請求書] をマークします。  
7. 一覧で、目的のレコードを見つけ、選択します。
    * 請求金額を超過して評価されている支払トランザクションを選択します。  
8. [マーク] のチェック ボックスをオンまたはオフにします。
    * 支払トランザクションをマークします。  
9. [転記] をクリックします。

## <a name="validate-consolidation-invoice-status-to-settled"></a>月次締め請求書のステータスが [決済済] であることを検証
1. [買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
    * 月次締め請求書のステータスが「決済済」になっていることを確認します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]