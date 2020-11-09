---
title: 出荷配送業者の設定
description: このトピックでは、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a71ea3983018b136d4fe3b22eadc0c332d2a698
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016450"
---
# <a name="set-up-shipping-carriers"></a>出荷配送業者の設定

[!include [banner](../../includes/banner.md)]

このトピックでは、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。 配送コーディネーターは、出荷の配送業者を入荷または出荷に割り当てることができます。


## <a name="create-a-new-shipping-carrier"></a>新しい出荷の配送業者の作成
1. **ナビゲーション ウィンドウ > モジュール > 輸送管理 > 設定 > 配送業者 > 出荷の配送業者** の順に移動します。
2. アクション ウィンドウで、 **新規** を選択します。
3. **出荷の配送業者** フィールドに値を入力します。
4. **名前** フィールドに値を入力します。
5. **モード** フィールドで、ドロップダウン メニューからオプションを選択します。

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>出荷配送業者の一般情報を入力します。
1. **概要** セクションの展開を切り替えます。
2. **出荷配送業者の有効化** チェック ボックスをオンまたはオフにします。
3. **仕入先** フィールドで、ドロップダウン メニューからオプションを選択します。 出荷配送業者の仕入先を選択します。  
4. **輸送業者タイプ** フィールドで、オプションを選択します。 **マニュアル** を選択して配送業者のページを使用するか、または **EDI** を選択して、電子データ交換 (EDI) で業者を更新できます。  
5. **配送業者の評価をアクティブ化** チェック ボックスをオンまたはオフにします。

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>出荷配送業者の必要なサービスを作成します。
1. **サービス** セクションの展開を切り替えます。
2. **新規** を選択します。
3. **配送サービス** フィールドに値を入力します。
4. **名前** フィールドに値を入力します。
5. **輸送方法** フィールドで、ドロップダウン メニューからオプションを選択します。

## <a name="set-up-the-address-for-the-carrier-optional"></a>配送業者の住所の設定 (オプション)
1. **住所** セクションの展開を切り替えます。
2. **新規** を選択します。
3. **名前または説明** フィールドに値を入力します。
4. **国/地域** フィールドで、ドロップダウン メニューからオプションを選択します。
5. **配送先郵便番号** フィールドで、ドロップダウン メニューからオプションを選択します。
6. **番地** フィールドに値を入力します。
7. **OK** を選択します。

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>出荷配送業者の評価プロファイルの設定
1. **評価プロファイル** セクションの展開を切り替えます。
2. **新規** を選択します。
3. **評価プロファイル** フィールドに値を入力します。
4. **名前** フィールドに値を入力します。
5. **サイト** フィールドで、ドロップダウン メニューからオプションを選択します。
6. **倉庫** フィールドで、ドロップダウン メニューからオプションを選択します。
7. **レート エンジン** フィールドで、ドロップダウン メニューからオプションを選択します。 配送業者との契約に従ってレート エンジンを選択します。  
8. **レート マスター** フィールドで、ドロップダウン メニューからオプションを選択します。
9. **輸送時間エンジン** フィールドで、ドロップダウン メニューからオプションを選択します。
10. **保存** を選択します。

