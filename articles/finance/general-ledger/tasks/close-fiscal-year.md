---
title: 会計年度の決算
description: この手順では、残高を新しい会計年度に振り替える年度末決算処理について説明します。
author: aprilolson
ms.date: 11/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d52e6789a96defaf1d0132fe97fc183a05af207
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779815"
---
# <a name="close-the-fiscal-year"></a>会計年度の決算

[!include [banner](../../includes/banner.md)]

この手順では、残高を新しい会計年度に振り替える年度末決算処理について説明します。


## <a name="validate-year-end-close-parameters"></a>年度末決算のパラメーターを検証します。
1. **ナビゲーション ウィンドウ > モジュール > 一般会計 > 元帳の設定 > 一般会計パラメーター** の順に移動します。
2. **会計年度末決算** セクションを展開します。
3. **振替時に決算トランザクションを削除する** オプションで、**はい** または **いいえ** を選択します。
    
会計年度が既に決済され、年度末決算が再度実行されている場合、この設定が重要です。 **はい** と設定されている場合、以前の年度末決算の伝票が削除されると、新しい伝票がすべての勘定の開始残高に対して作成されます。 **いいえ** と設定されている場合、以前の伝票が保持され、新しい伝票が最後の年度末決算の転記後に調整エントリに対してのみ作成されます。

4. **振替時に決算トランザクションを作成する** オプションで、**はい** または **いいえ** を選択します。

**はい** と設定している場合、2 つのトランザクションが作成されます。 終了した会計年度に 1 番目の伝票がすべての勘定科目の残高をゼロにするために引き下げるために作成され、2 番目の伝票は、次の会計年度に期首残高のために作成されます。 **いいえ** と設定している場合、期首残高のために次の会計年度に、1 つの伝票が作成されます。  

5. **会計年度の状態を完全に終了する** オプションで、**はい** または **いいえ** を選択します。

**はい** に設定している場合、会計年度のステータスは **完全に終了** に設定されます。 完全に終了した年度は再度開くことができないため、このオプションを **いいえ** に設定することを推奨します。  

6. **伝票番号を年度末決算時に転記する必要がある** オプションで、**はい** または **いいえ** を選択します。

**はい** に設定している場合、年度末決算処理中に、伝票番号を手動で入力する必要があります。 番号の順序は、この伝票番号の生成には使用されません。 この推奨設定は **はい** です。  

7. ページを閉じます。
8. **一般会計 > 期間の締め > 年度末決算** の順に移動します。
9. **新規** をクリックして、年度末決算テンプレートを作成します。

テンプレートは年度末決算を実行する法人グループ用に作成できます。 このテンプレートは次年度にも再利用できます。  

10. **グループ名** フィールドで、年度末決算テンプレートの名前を入力します。
11. **会計カレンダー** フィールドで、テンプレートを作成する会計年度を選択します。

同じ会計年度を使用する法人のみを、年度末決算テンプレートにグループ化できます。 これは、期末決算が日付ではなく、会計年度の選択によって実行されるためです。  

12. **アクション ウィンドウ** で、**保存** をクリックします。
13. **法人** セクションで、**追加** をクリックして、このテンプレートの法人を選択します。
    
法人を選択するか、または組織階層を選択することにより、法人を追加できます。 選択された同じ会計カレンダーを使用する組織階層の法人のみが追加されます。  

14. 法人または組織階層を選択します。
15. **OK** をクリックします。
16. **貸借対照表の分析コードを転送** で、**はい** または **いいえ** を選択します。

貸借対照表勘定では、このオプションを **はい** に設定するのが最善です。 これは、貸借対照表勘定の開始残高を作成するときに転記されたトランザクションの財務分析コードを管理します。 損益勘定の場合、残高が利益剰余金に移動した場合に財務分析コード (**すべて閉じる**) を維持するように選択するか、または異なる分析コード値 (**1 つ閉じる**) を使用して財務分析コードを置き換えることができます。 **1 つ閉じる** を選択した場合は、各分析コードに特定の分析コード値を定義するか、またはそれを空のままにすることもできます。  

17. **保存** をクリックします。
18. **アクション ウィンドウ** の **期末決算の実行** の選択によって年度末決算を開始します。 年度末決算が選択されたテンプレートに対して実行されます。  
19. テンプレートから年度末決算を実行する法人グループのすべてまたはサブセットを選択します。

年度末決算を最初に実行する場合、開始残高を取得するために、ほとんどの組織は、テンプレート内のすべての法人の年度末決算を実行することを選択します。 調整エントリがその後に行われた場合、調整がある法人のみに対して、年度末決算を実行することを選択できます。  

20. **OK** をクリックします。
21. 年度末決算を実行する会計年度を選択します。
22. **伝票フィールド** に値を入力します。 作成された年度末決算伝票を検索しやすいように、伝票番号に会計年度を含めることを推奨します。  
23. バッチで実行する年度末決算の既定値。 処理時間が長いプロセスはバッチ モードで処理することを推奨します。 これが、既定ではバッチ モードを使用する理由となる、典型的な処理の 1 つです。  
24. **OK** をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
