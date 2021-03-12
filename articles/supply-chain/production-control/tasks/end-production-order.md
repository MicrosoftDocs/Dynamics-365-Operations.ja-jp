---
title: 製造オーダーの終了
description: この手順では、製造オーダーの終了方法を説明します。
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f3e121fdc0f69ace15e0fa08bde0af739ef7d28
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977816"
---
# <a name="end-a-production-order"></a>製造オーダーの終了

[!include [banner](../../includes/banner.md)]

この手順では、製造オーダーの終了方法を説明します。 この手順の作成に使用するデモ データの会社は USMF です。 これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 最後の手順です。


## <a name="end-a-production-order"></a>製造オーダーの終了
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
    * ステータスが [報告済] つまり完了済の製造オーダーを選択します。  
2. アクション ウィンドウで、[製造オーダー] をクリックします。
3. [終了] をクリックします。
    * このページで、終了する製造オーダーを確認できます。  
4. [一般] タブをクリックします。
5. [日付] フィールドに日付を入力します。
6. [仕損方法] フィールドで「配賦」を選択します。
    * [配賦方法] を選択すると、仕損材料の原価は完成品に追加されます。  
7. [OK] をクリックします。

## <a name="validate-calculation-results"></a>計算結果の検証
1. [アクション] ペインで [原価の管理] をクリックします。
2. [原価の比較の表示] をクリックします。
    * 製造オーダーの終了後は、見積原価価格を実際の原価価格と比較して製造差異の概要を得ることができます。  
