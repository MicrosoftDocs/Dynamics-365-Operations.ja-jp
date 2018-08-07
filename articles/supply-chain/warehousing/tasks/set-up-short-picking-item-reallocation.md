--- 
title: "品目再配賦の未処理ピッキングの設定"
description: "この手順では、倉庫の在庫が不十分な場合、倉庫従事者はどのようにすれば他の倉庫を素早く見つけることができるか説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b67965b6c8641b5d91ab3c5b0a7a7fd28a07cba6
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>品目再配賦の未処理ピッキングの設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、倉庫の在庫が不十分な場合、倉庫従事者はどのようにすれば他の倉庫を素早く見つけることができるか説明します。 自動的な再配分をすることは可能で、他の場所が手配できる場合、製品を再配分させる指示があります。 また手動再配分を行う場合、有効数量の対応が可能な場所の一覧がモバイル端末に表示され、これにより倉庫従事者は在庫にはどの場所がよいか選択することができます。 デモ データの会社 USMF でこの手順を使用できます。 この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。


## <a name="set-up-work-exceptions"></a>作業例外を設定します
1. [倉庫管理] > [セットアップ] > [作業] > [例外作業] の順に移動します。
2. [新規] をクリックします。
    * 倉庫従事者が処理している出荷のニーズに基づいて品目を選択できるよう、品目再配置ポリシーに複数の例外作業を設定することができます。  
3. [例外作業コード] フィールドで、値を入力します。
    * 例外作業の使途がわかるように例外作業にタイトルを付けます。 たとえば、ショートピッキングに関するマニュアルなど。  
4. [説明] フィールドに値を入力します。
5. [例外タイプ] のフィールドで、「ショートピック」を選択します。
6. [在庫調整] チェック ボックスを選択します。
    * このオプションでは、在庫が簡単なピッキング場所の0に自動的に調整されます。  
7. [既定の調整タイプコード] フィールドで、値を入力または選択します。
    * たとえば、USMFでは「 Res Adj Outを削除」を選択できます。  
8. [品目再配置] フィールドで、「手作業」を選択します。
    * 手動または自動および手動を選択した場合、倉庫従事者は手動での再配分を実行できなければなりません。  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>手作業による品目再配分を使用する作業者を設定します。
1. ページを閉じます。
2. [倉庫管理] > [セットアップ] > [作業者] の順に移動します。
3. [編集] をクリックします。
4. リストで、[作業者 24] を選択します。
5. 作業セクションを展開します。
6. [手動による再配置を許可] フィールドで [はい] を選択します。


