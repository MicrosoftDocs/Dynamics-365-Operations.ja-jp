---
title: プロセス ジョブのかんばんルールの変更
description: この手順は、使用されているかんばんルールの指定されたかんばんへの変更を対象としています。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13798e3521efacda896ca88a39faf36ac979d42c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574500"
---
# <a name="change-kanban-rules-for-a-process-job"></a>プロセス ジョブのかんばんルールの変更

[!include [banner](../../includes/banner.md)]

この手順は、使用されているかんばんルールの指定されたかんばんへの変更を対象としています。 これは負荷リソースのレベルに、または故障の場合に便利です。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、リーン生産会社で働いていて、バリュー ストリームを担当するプランナーを対象としています。


## <a name="copy-kanban-rule"></a>かんばんルールのコピー
1. [かんばんルール] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * L0001 のイベントかんばんルール 000022 を選択します。  
3. [かんばんルールの複製] をクリックします。
4. [OK] をクリックします。

## <a name="change-kanban-rule"></a>かんばんルールの変更
1. ページを閉じます。
2. [かんばん作業のスケジューリング] に移動する。
3. 一覧で、選択された行をマークします。
    * かんばん 000177 の明細行を選択します。  
4. [代替かんばんルールの使用] をクリックします。
5. [次へ] をクリックします。
6. [かんばんルール] フィールドで、値を入力または選択します。
    * 先に作成されたかんばんルールを選択します。 これは、最大数のかんばんルールです。  
7. [完了] をクリックします。
    * ここでは、かんばん作業は別のかんばんルールを使用します。 これは負荷の作業セルのレベルに有用です。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]