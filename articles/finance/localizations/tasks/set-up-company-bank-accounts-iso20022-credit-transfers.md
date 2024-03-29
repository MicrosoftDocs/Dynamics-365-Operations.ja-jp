---
title: ISO20022 口座振替用の会社の銀行口座の設定
description: この手順では、支払ファイルの生成に必要な会社固有の銀行口座情報を設定する方法を示します。
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3b3b5ce9d7e24b2b7d3f76e4d770968df897b546df507ba9e3bde5aeac91715
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780773"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>ISO20022 口座振替用の会社の銀行口座の設定

[!include [banner](../../includes/banner.md)]

この手順では、支払ファイルの生成に必要な会社固有の銀行口座情報を設定する方法を示します。 ISO 20022 口座振替形式を生成するために必要な情報を設定しますが、形式に応じて会社 ID または並べ替えコードなど、その他の情報が必要になる場合があります。 

この手順の作成に使用するデモ データの会社は DEMF です。

これは、5 つのうち 2 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="set-up-iban-and-swift-code"></a>IBAN および SWIFT コードの設定
1. [現金および銀行管理] > [銀行口座] の順に移動します。
2. クイック フィルターを使用して、値が「DEMF OPER」である [銀行口座] フィールドをフィルター処理します。
3. [DEMF OPER] をクリックして、銀行口座詳細を開きます。
4. [編集] をクリックします。
5. [追加 ID] セクションを展開します。
6. [IBAN] フィールドに「DE89370400440532013000」と入力します。
7. [SWIFT コード] フィールドに、「DEUTDEFF」を入力します。
    * SWIFT\BIC は多くの支払形式で必須ではありませんが、銀行口座への登録が推奨されていることに注意してください。  
8. [保存] をクリックします。

## <a name="set-up-bank-account-for-the-legal-entity"></a>法人用の銀行口座の設定
1. [組織管理] > [組織] > [法人] の順に移動します。
2. [編集] をクリックします。
3. [銀行口座情報] セクションを展開します。
4. [銀行口座] フィールドで、値を入力または選択します。
5. [保存] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]