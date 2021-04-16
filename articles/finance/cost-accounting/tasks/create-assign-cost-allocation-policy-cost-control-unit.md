---
title: 原価配賦ポリシーの作成と原価管理単位への割り当て
description: 原価配賦ポリシーと対応ルールを原価管理単位に作成し割り当てるには、この手順を使用します。
author: ShylaThompson
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cff10132e8007be885e9c69d97cf96c30d69f50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822858"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>原価配賦ポリシーの作成と原価管理単位への割り当て

[!include [banner](../../includes/banner.md)]

原価配賦ポリシーと対応ルールを原価管理単位に作成し割り当てるには、この手順を使用します。 この記録では、USP2 デモ データ会社を使用します。


## <a name="create-a-policy"></a>ポリシーの作成
1. [原価会計] > [ポリシー] > [原価配賦ポリシー] へ移動します。
2. [新規] をクリックします。
3. [ポリシー名] フィールドで、値を入力します。
4. [原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。
    * [組織] を選択します。  
5. [統計分析コード] フィールドで、値を入力または選択します。
6. [保存] をクリックします。

## <a name="create-allocation-rules"></a>配賦ルールの作成
1. [新規] をクリックします。
2. 一覧で、選択された行をマークします。
3. [原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。
4. [原価動作] フィールドで、[合計] を選択します。
5. [配賦基準] フィールドで、値を入力または選択します。
6. [新規] をクリックします。
7. 一覧で、選択された行をマークします。
8. [原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。
9. [原価動作] フィールドで、[合計] を選択します。
10. [配賦基準] フィールドで、値を入力または選択します。
11. [新規] をクリックします。
12. 一覧で、選択された行をマークします。
13. [原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。
14. [原価動作] フィールドで、[合計] を選択します。
15. [配賦基準] フィールドで、値を入力または選択します。
    * すべてのルールを作成するまで、続行します。  
16. [保存] をクリックします。

## <a name="assign-the-policy-to-a-cost-control-unit"></a>原価管理単位へポリシーを割り当て
1. 原価管理単位の [ポリシーの割り当て] をクリックします。
2. [新規] をクリックします。
3. 一覧で、選択された行をマークします。
4. [会計日から有効] フィールドで、値を入力します。
    * ルールの日付は有効です。 新しいバージョンが作成された場合、ユーザーまたはシステムは、そのルールの期限を切ることが可能です。  
5. [原価管理単位] フィールドで、値を入力または選択します。
6. [保存] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]