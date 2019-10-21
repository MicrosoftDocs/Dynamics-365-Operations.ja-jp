---
title: ISO20022 口座引落用の会社の銀行口座の設定
description: このタスクでは、顧客支払ファイルを生成するのに必要な会社固有の銀行口座情報の設定について説明します。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89c4a8d3cb504df97bad5679bf12b3cdb5931d95
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185707"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>ISO20022 口座引落用の会社の銀行口座の設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスクでは、顧客支払ファイルを生成するのに必要な会社固有の銀行口座情報の設定について説明します。 この手順では、ISO 20022 口座引落形式を例として使用します。 他の形式では、会社 ID または並べ替えコードなどの情報の設定が必要になる場合があります。



このタスクは デモ データ会社 DEMF を使用して作成されました。



これは、5 つのうち 2 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。


## <a name="set-up-the-iban-and-swift-codes"></a>IBAN および SWIFT コードの設定
1. [現金および銀行管理] > [銀行口座] の順に移動します。
2. クイック フィルターを使用して、値が「DEMF OPER」である [銀行口座] フィールドをフィルター処理します。
3. 一覧で、選択された行のリンクをクリックします。
    * たとえば、「DEMF OPER」をクリックして、銀行口座詳細を開きます。  
4. [編集] をクリックします。
5. [追加 ID] セクションを展開または折りたたみます。
6. [IBAN] フィールドに値を入力します。
    * たとえば、「DE89370400440532013000」を入力します。  
7. [SWIFT コード] フィールドに、値を入力します。
    * たとえば、「DEUTDEFF」を入力します。    SWIFT \ BIC は多くの支払形式で必須ではありませんが、銀行口座への登録が推奨されていることに注意してください。  
8. [保存] をクリックします。

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>法人用の銀行口座の設定
1. [組織管理] > [組織] > [法人] の順に移動します。
2. [編集] をクリックします。
3. [銀行口座情報] セクションを展開または折りたたみます。
4. [銀行口座] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。
5. 一覧で、選択された行のリンクをクリックします。
    * たとえば、「DEMF OPER」銀行口座を選択します。  
6. [保存] をクリックします。

