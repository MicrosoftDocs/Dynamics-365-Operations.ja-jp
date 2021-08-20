---
title: ISO20022 口座引落用の支払方法の設定
description: この手順では、ISO20022 口座振替の顧客の支払方法や電子レポートを使用したその他の支払タイプを設定する方法を示します。
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 127d5402abfedcce124b39b76a6c1036a6c818a7c1318aaeabdb0688b50f738e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779764"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>ISO20022 口座引落用の支払方法の設定

[!include [banner](../../includes/banner.md)]

この手順では、ISO20022 口座振替の顧客の支払方法や電子レポートを使用したその他の支払タイプを設定する方法を示します。 



このタスクを完了する前に、エクスポート形式のコンフィギュレーションおよび支払口座を設定する必要があります。



この手順は、デモ データ会社 DEMF を使用して作成されました。



これは、5 つのうち 3 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。

1. [売掛金管理] > [支払設定] > [支払方法] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、[支払い方法] フィールドに値「ELECTRONIC」でフィルターを適用します。
3. [編集] をクリックします。
4. [支払勘定] フィールドで、値「DEMF OPER」を指定します。
5. [ファイル形式] セクションを展開します。
6. [一般的な電子申告] フィールドで [はい] を選択します。
7. [エクスポート形式のコンフィギュレーション] フィールドで、値を入力または選択します。
    * 一覧で、[ISO20022 口座引落 (DE)] を選択します。  一覧が空の場合、顧客支払エクスポート形式のコンフィギュレーションはインポートされず有効になりません。  
8. [委任状の要求] フィールドで、[はい] を選択します。
    * 顧客支払形式の [委任状の要求] パラメーターを選択します。これには、SEPA 口座引落などの支払メッセージの委任状の情報が含まれている必要があります。  
9. [保存] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]