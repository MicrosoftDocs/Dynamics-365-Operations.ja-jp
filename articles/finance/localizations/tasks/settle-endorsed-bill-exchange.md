---
title: 裏書済受取手形の決済
description: このタスクは、裏書きされた為替手形の決済について説明します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustBillOfExchangeEndorseListPage, VendOpenTrans, CustBillOfExchangeEndorseSettle
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1c7e5a0ea866a9d0f0520696ef675e87e45634
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839726"
---
# <a name="settle-an-endorsed-bill-of-exchange"></a>裏書済受取手形の決済

[!include [banner](../../includes/banner.md)]

このタスクは、裏書きされた為替手形の決済について説明します。



このタスクを完了するには、裏書きされた為替手形および未処理の仕入先トランザクションが必要です。 



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="settle-a-vendor-transaction-that-was-generated-by-an-endorsement"></a>裏書によって生成された仕入先トランザクションの決済
1. [買掛金勘定] > [支払] > [裏書為替手形] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * ステータスが「裏書済」の為替手形を選択します。  
3. [トランザクションの決済] をクリックします。
4. 一覧で、目的のレコードを見つけ、選択します。
    * 為替手形の裏書によって生成されたトランザクションを選択します。  
5. [マーク] のチェック ボックスをオンにします。
6. 一覧で、目的のレコードを見つけ、選択します。
    * 対応する仕入先トランザクションで決済に使用するものを選択します。  
7. [マーク] のチェック ボックスをオンにします。
8. [転記] をクリックします。

## <a name="settle-an-endorsed-bill-of-exchange"></a>裏書済受取手形の決済
1. [裏書済為替手形の決済] をクリックしてドロップ ダイアログを開きます。
2. [裏書済為替手形の決済] をクリックします。
    * 決済日は、必要に応じて変更できます。  
    * ステータスが「裏書決済済」に更新されていることを確認します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]