---
title: 資産除去責務の転記および市場割引率のための主勘定のコンフィギュレーション
description: 日本では、法的な除去責務のある固定資産を取得した場合、除去する際には資産除去責務を評価し転記する必要があります。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting, AssetDiscountRateSchedule_JP
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd85a8edd539a8158457a09bca49bd1718bb074396d2d0a1dbd970f6a81090be
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756214"
---
# <a name="configure-main-accounts-for-asset-retirement-obligation-posting-and-market-discount-rates"></a>資産除去責務の転記および市場割引率のための主勘定のコンフィギュレーション

[!include [banner](../../includes/banner.md)]

日本では、法的な除去責務のある固定資産を取得した場合、除去する際には資産除去責務を評価し転記する必要があります。 



ユーザーは、資産の除去責務のトランザクションを転記できるようにするには、すべての主勘定を構成する必要があります。



このタスクでは、資産の除去責務の転記のために主勘定を構成する方法について説明します。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順では、JPMF デモ会社のデータを使用します。


## <a name="configure-ledger-accounts-for-asset-retirement-obligation-posting"></a>資産除去責務の転記のための勘定科目のコンフィギュレーション
1. [固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。
2. [資産除去責務] セクションを展開します。
3. [追加] をクリックします。
4. [帳簿] フィールドに値を入力します。
5. [グループ化] フィールドで、オプションを選択します。
6. [固定資産番号] フィールドに値を入力します。
    * オプション: [グループ] または [テーブル] として「グループ化」を選択した場合は、固定資産グループまたは固定資産を指定する必要があります。  
7. [主勘定] フィールドに、目的の値を指定します。
8. [相殺勘定] フィールドで、任意の値を指定します。
9. [選択] フィールドで、オプションを選択します。
10. [文書種類ごとの廃棄パラメーター] セクションを展開します。
11. [売却または仕損] フィールドで、オプションを選択します。
    * [販売] および [仕損] の両方のタイプのトランザクションを転記する前に、これらの処分勘定を設定する必要があります。  
12. [新規] をクリックします。
13. [帳簿] フィールドに値を入力します。
14. [有効] フィールドで、オプションを選択します。
15. [固定資産関係] フィールドに値を入力します。
    * オプション: [グループ] または [テーブル] として「有効」を選択した場合は、固定資産グループまたは固定資産を指定する必要があります。  
16. [主勘定] フィールドに、目的の値を指定します。
17. [相殺勘定] フィールドで、任意の値を指定します。
    * トランザクションの他の組み合わせに対して、主勘定のコンフィギュレーション ステップを繰り返します。  
    * コンフィギュレーションの各行は転記金額の 1 つのタイプに必要です。  

## <a name="configure-market-discount-rates"></a>市場割引率のコンフィギュレーション
1. [固定資産] > [設定] > [キャッシュフロー割引率] に移動します。
2. [新規] をクリックします。
3. [開始日] フィールドに日付を入力します。
4. [市場割引率] フィールドに、数値を入力します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]