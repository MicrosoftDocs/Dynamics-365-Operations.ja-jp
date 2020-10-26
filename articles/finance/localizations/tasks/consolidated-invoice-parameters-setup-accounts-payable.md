---
title: 月次締め請求書のパラメーターのコンフィギュレーションと買掛金勘定の設定
description: 日本では、日本の商習慣に合わせて月次締め請求書を有効にできます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters, PaymDay, PaymTerm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59900cbbd2912daa0f6f31c8ebe83736be87b2d8
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978563"
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

