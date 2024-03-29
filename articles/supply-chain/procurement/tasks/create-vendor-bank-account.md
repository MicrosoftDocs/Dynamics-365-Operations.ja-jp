---
title: 仕入先銀行口座の作成
description: この手順では、仕入先用の銀行口座の作成方法を説明します。
author: GalynaFedorova
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b201f5eb2bf8eb496a761b6fc6ca729a46a85ce
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677845"
---
# <a name="create-a-vendor-bank-account"></a>仕入先銀行口座の作成

[!include [banner](../../includes/banner.md)]

この手順では、仕入先用の銀行口座の作成方法を説明します。 デモ データの会社 USMF でこの手順を使用できます。

1. **ナビゲーション ウィンドウ > モジュール > 調達 > 仕入先 > すべての仕入先** の順に移動します。
2. 銀行口座を作成する対象の仕入先を選択し、**仕入先 ID** フィールドのリンクをクリックします。
3. **アクション ウィンドウ** で、 **仕入先** をクリックします。
4. **銀行口座** をクリックします。
5. **アクション ペイン** で **新規作成** をクリックします。
6. **銀行口座** フィールドに、値を入力します。 この ID を使用して仕入先レコードの銀行口座を識別します。  
7. **名前** フィールドに値を入力します。
8. **銀行グループ** フィールドで、値を入力または選択します。
9. **ルーティン番号タイプ** フィールドで、オプションを選択します。 これは国際送金に使用されるルーティング番号のタイプです。  
10. **銀行口座番号** フィールドに、値を入力します。
11. **SWIFT コード** フィールドに、値を入力します。
12. **IBAN** フィールドに値を入力します。
    - IBAN 番号は正しい形式にする必要があります。 たとえば「DE89370400440532013000」のような形式を使用できます。  
    - 銀行口座の状態は、有効日が来て、有効期限を超過していない場合は [有効] です。 有効日と有効期限フィールドの両方が空白の場合でも有効です。 [有効日] および [有効期限] の両フィールドの日付が将来の日付である場合、電子支払は使用できません。 他の支払タイプは使用可能であり、銀行口座は有効です。  
13. **設定** セクションを展開します。
14. **テキスト コード** フィールドに、値を入力します。 このフィールドでは、受取人の口座取引明細書に表示されるコードを指定します。  
15. **銀行へのメッセージ** フィールドに、値を入力します。
16. **為替参照** フィールドに、値を入力します。 これは、先物為替レートまたは固定期間為替レートの参照番号です。
17. **通貨** フィールドで値を入力または選択します。 事前通知が発行される場合、このセクションではステータス (保留中または承認済) の概要を表示します。  
18. **住所** セクションを展開します。
19. **事前通知** セクションを展開します。
20. **連絡先情報** セクションを展開します。
21. **電話** フィールドに値を入力します。
22. ページを閉じます。
23. **編集** をクリックします。
24. **支払** セクションを展開します。
25. **銀行口座** フィールドにて、作成した口座を選択します。
26. **保存** をクリックします。 指定するか、ここに追加する場合、住所は銀行グループから継承される場合があります。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]