---
title: 月次締め請求書のパラメーターのコンフィギュレーションと買掛金勘定の設定
description: この記事では、月次締め請求書の設定と構成について説明します。
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
ms.search.form: VendParameters, PaymDay, PaymTerm
ms.openlocfilehash: b4bea02711fcdb4ea8b4951fceef3a130a15f11c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276476"
---
# <a name="configure-consolidated-invoice-parameters-and-setup-for-accounts-payable"></a>月次締め請求書のパラメーターのコンフィギュレーションと買掛金勘定の設定

[!include [banner](../../includes/banner.md)]

日本では、日本の商習慣に合わせて月次締め請求書を有効にできます。



この手順では、月次締め請求書の機能について説明します。



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="configure-accounts-payable-parameters-for-consolidated-invoices"></a>月次締め請求書に対する [買掛金勘定パラメーター] のコンフィギュレーション
1. [買掛金勘定] > [設定] > [買掛金勘定パラメーター] の順に移動します。
2. [仕入先] セクションを展開します。
3. [仕入先に対する月次締め請求書] チェック ボックスをチェックします。
4. [番号順序] タブをクリックします。
    * 締め ID に使用される番号順序を指定します。  

## <a name="configure-payment-days"></a>[支払期日] のコンフィギュレーション
1. [買掛金勘定] > [支払の設定] > [支払期日] の順に移動します。
    * 支払期日のコンフィギュレーション  

## <a name="configure-terms-of-payment"></a>[支払条件] のコンフィギュレーション
1. [買掛金勘定] > [支払設定] > [支払条件] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、[支払い条件] フィールドで「代金引換払い」という値を指定してフィルターを実行します。
3. [編集] をクリックします。
    * [支払方法] として [締日] を選択  
    * [締日] は R1 リリースでは表示されません。 代わりに [当月] を選択できます。 この結果、手動での調整を必要とするわずかな差が生じる場合があります。   
4. [支払期日] フィールドに値を入力します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
