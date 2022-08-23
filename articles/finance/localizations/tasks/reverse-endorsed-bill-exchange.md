---
title: 裏書済受取手形の取消
description: このタスクは、裏書きされた為替手形の取消について説明します。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseReverse, LedgerTransVoucher
ms.openlocfilehash: 7891d4cd5e5ffa23af8c13b82740fcdf197b8863
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275197"
---
# <a name="reverse-an-endorsed-bill-of-exchange"></a>裏書済受取手形の取消

[!include [banner](../../includes/banner.md)]

このタスクは、裏書きされた為替手形の取消について説明します。

このタスクを完了するには、少なくとも 1 つの裏書きされた為替手形が必要です。 

このタスクは デモ データ会社 JPMF を使用して作成されました。

1. [買掛金勘定] > [支払] > [裏書為替手形] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * ステータスが「裏書済」の為替手形を選択します。 仕入先トランザクションが既に決済されている場合、受取手形を引き当てることはできません。 裏書を引き当てる前に決済を元に戻します。  
3. [裏書の取消] をクリックしてドロップ ダイアログを開きます。
4. [裏書の取消] をクリックします。
    * 引当日は、必要に応じて変更できます。  
5. [照会] をクリックします。
6. [伝票] をクリックします。
    * 会計伝票が取消に対して生成されていることを確認します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
