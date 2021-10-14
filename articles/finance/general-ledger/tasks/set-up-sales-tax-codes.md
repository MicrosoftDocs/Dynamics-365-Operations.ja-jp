---
title: 消費税コードを設定します
description: このトピックでは、Dynamics 365 Finance で売上税コードを設定する方法について説明します。
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2539d701dda4ef5e1484d095b2d86d1f68a0dc98
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562105"
---
# <a name="set-up-sales-tax-codes"></a>消費税コードを設定します

[!include [banner](../../includes/banner.md)]

このトピックでは、消費税コードを設定する方法について説明します。 売上税コードは、法人が計算、収集、税務当局への支払いの義務のあるそれぞれの間接税または関税について作成されます。

このタスクでは、USMF というデモ会社を使用します。

1. **ナビゲーション ウィンドウ > 税 > 間接税 > 売上税 > 売上税コード** の順に移動します。
2. **新規** を選択します。
3. **売上税コード** フィールドで、値を入力します。
4. **名前** フィールドに値を入力します。
5. プルダウン リストを開いて **決済期間** を選択すると、この売上税の報告と支払いを行う売上税所轄官庁の指定や、その間隔の指定ができます。
6. 総勘定元帳に売上税を転記する主勘定を指定するには、**元帳転記グループ** を選択します。
7. **計算** クイック タブを展開します。 これには、売上税額の計算方法を制御する複数のフィールドがあります。 必要に応じて、これらのフィールドに入力します。  
8. インターフェイスの上部にある **アクション ウィンドウ** で、**売上税コード** を選択します。
9. **値** を選択します。
10. この税コードの値を **値** 列に入力します。

    **計算** クイック タブの **発生元** フィールドで、**単位ごとの金額** が選択されている場合、売上税金額の計算では、値にトランザクションの数量が乗算されます。  税コードが単位に基づく税でない場合、値は、売上税金額を計算するためにこの税コードの発生元に適用される割合を示す値になります。     

11. **保存** を選択します。
12. ページを閉じます。
13. **保存** を選択します。

Microsoft Dynamics 365 Finance バージョン 10.0.22 では、[税サービス](../../localizations/global-tax-calcuation-service-overview.md) を使用し、**機能管理** ワークスペースで [**複数の VAT 登録番号のサポート**](../../localizations/emea-multiple-vat-registration-numbers.md) 機能が有効になっている場合、**税のタイプ** フィールドを使用して税コードのタイプを指定できます。 使用可能な値は次のとおりです。

- 標準 VAT
- 減額 VAT
- VAT 0%
- 物品税
- その他

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
