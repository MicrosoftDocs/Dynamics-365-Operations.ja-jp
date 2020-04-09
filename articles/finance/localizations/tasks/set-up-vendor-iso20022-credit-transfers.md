---
title: 仕入先の設定と ISO20022 口座振替用の仕入先銀行口座の設定
description: この手順では、ISO20022 口座振替またはその他の仕入先支払ファイルの生成に必要な仕入先および仕入先固有の銀行口座情報を設定する方法を示します。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4809a352f87cc3d88429461a06dfe36189ed5f31
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138972"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>仕入先の設定と ISO20022 口座振替用の仕入先銀行口座の設定

[!include [banner](../../includes/banner.md)]

この手順では、ISO20022 口座振替またはその他の仕入先支払ファイルの生成に必要な仕入先および仕入先固有の銀行口座情報を設定する方法を示します。 

この手順の作成に使用するデモ データの会社は DEMF です。
これは、5 つのうち 4 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="set-up-bank-details"></a>銀行詳細を設定します。
1. [買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、[仕入先口座] フィールドに値「DE-001」でフィルターを適用します。
3. 「DE-001」をクリックして、仕入先の詳細を開きます。
4. [アクション] ウィンドウで、[仕入先] をクリックします。
5. [銀行口座] をクリックします。
6. [編集] をクリックします。
    * 銀行口座が存在しない場合は、新しい口座を作成する必要があります。  
7. [SWIFT コード] フィールドで、「COBADEFFXXX」を入力します。
8. [IBAN] フィールドに「DE36200400000628808808」と入力します。
9. ページを閉じます。

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>仕入先に対する支払方法の設定
1. [編集] をクリックします。
2. [支払] セクションを展開または折りたたみます。
3. [支払方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、選択された行「SEPA CT」のリンクをクリックします。
5. [保存] をクリックします。

