---
title: 仕入先の設定と ISO20022 口座振替用の仕入先銀行口座の設定
description: この手順では、ISO20022 口座振替またはその他の仕入先支払ファイルの生成に必要な仕入先および仕入先固有の銀行口座情報を設定する方法を示します。
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a901591f9f3d1a892c29f92e59dc96c1f172143cae6bec571da33b4a50d274
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723722"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]