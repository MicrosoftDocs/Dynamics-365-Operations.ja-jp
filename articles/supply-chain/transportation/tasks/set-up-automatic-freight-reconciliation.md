---
title: 自動運賃調整の設定
description: この手順では、自動運賃調整のデータ設定方法を示します。
author: ShylaThompson
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08fa9fce340a2e0069d3c65d17489966b6bc868b20951698c844edd2bf099013
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747748"
---
# <a name="set-up-automatic-freight-reconciliation"></a>自動運賃調整の設定

[!include [banner](../../includes/banner.md)]

この手順では、自動運賃調整のデータ設定方法を示します。 これは、通常、倉庫マネージャーによって行われます。 デモ データの会社 USMF でこの手順を使用できます。


## <a name="set-up-the-freight-bill-type"></a>運賃請求書タイプの設定
1. [輸送管理] > [設定] > [運賃の調整] > [運賃請求書タイプ] の順に移動します。
    * 運賃請求書タイプは、運賃請求書と配送業者の請求書をどのようにして照合するべきかを定義します。  
2. [新規] をクリックします。
3. [運賃請求書タイプ] フィールドで値を入力します。
4. エンジン アセンブリ フィールドで、「Microsoft.Dynamics.Ax.Tms.dll」と入力します。
    * これは標準の輸送管理照合エンジン コード ライブラリです。  
5. エンジン クラス フィールドで、「Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer」と入力します。
    * これは標準の輸送管理照合エンジン クラスです。  
6. [新規] をクリックします。
7. [説明] フィールドで、運賃請求書と配送業者の請求書で照合する必要のある値を選択します。  
8. [照合が必要] フィールドで、[はい] を選択します。
    * このフィールドで [はい] を設定すると、説明フィールドで選択された値が、運賃請求書と配送業者の請求書の両方で照合する必要があることを意味します。 [いいえ] に設定する場合、このフィールドをいずれかで空白にすることができます。  
9. [保存] をクリックします。

## <a name="set-up-the-freight-bill-type-assignment"></a>運賃請求書タイプの割り当ての設定
1. ページを閉じます。
2. [輸送管理] > [設定] > [運賃の調整] > [運賃請求書タイプの割り当て] の順に移動します。
    * 運賃請求書タイプの割り当てを使用して、特定の配送業者に使用する運賃請求書タイプを指定します。   
3. [新規] をクリックします。
4. [モード] フィールドで値を入力または選択します。
5. [出荷の配送業者] フィールドで値を入力または選択します。
6. [運賃請求書タイプ] フィールドで、先に作成した運賃請求書タイプを選択します。
7. ページを閉じます。

## <a name="set-up-the-audit-master"></a>監査マスターの設定
1. [輸送管理] > [設定] > [運賃の調整] > [監査マスター] の順に移動します。
    * 監査マスターは、自動運賃調整の許容制限を定義します。 これは、運賃請求書と配送業者の請求書の金額の差と調整できる金額で指定します。 また、不一致の処理方法も定義します。  
2. [新規] をクリックします。
3. [監査マスター ID] フィールドに値を入力します。
4. [出荷の配送業者] フィールドで、先で使用した同じ出荷の配送業者を選択します。
5. [運賃請求書タイプ] フィールドで、先に作成した運賃請求書タイプを選択します。
6. [許容範囲] セクションを展開します。
7. [最小許容範囲レベル] フィールドに数値を入力します。
8. [最大許容範囲レベル] フィールドに数値を入力します。
9. [結果] セクションを展開します。
10. [過剰支払の理由コード] フィールドで、値を入力または選択します。
    * 金額が運賃請求書と配送業者の請求書で異なる場合、差異が許容範囲レベル内であれば、超過/不足支払の理由コードに応じて差額を登録する必要のある勘定が指定されます。  
11. [過少支払の理由コード] フィールドで、値を入力または選択します。
12. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]