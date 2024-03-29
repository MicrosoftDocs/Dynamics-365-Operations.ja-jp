---
title: かんばん数量計算ポリシーのかんばんルールへの追加
description: この手順では、かんばん数量の計算ポリシーを作成し、それをかんばんルールへ追加し、かんばんのサイズおよび数量を最適化することに焦点をあてます。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a844d455b1e583f234ddc47280f5cac8ee0ab852
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579283"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>かんばん数量計算ポリシーのかんばんルールへの追加

[!include [banner](../../includes/banner.md)]

この手順では、かんばん数量の計算ポリシーを作成し、それをかんばんルールへ追加し、かんばんのサイズおよび数量を最適化することに焦点をあてます。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、バリュー ストリーム マネージャーを対象としています。 この手順は、かんばん数量修正候補の計算という手順を作成するための前提条件です。 


## <a name="create-a-kanban-quantity-calculation-policy"></a>かんばん数量計算ポリシーの作成
1. [生産管理] > [定期処理タスク] > [かんばん数量の計算] > [かんばん数量の計算ポリシー] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
    * たとえば、「Speaker2016」と入力します。  
4. [マスター プラン] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、目的のレコードを見つけ、選択します。
    * StaticPlan を選択して、需要を計算します。  
6. 一覧で、選択された行のリンクをクリックします。
7. [保存] をクリックします。
8. [最小かんばん数量] フィールドに、「1」を入力します。
    * これはかんばん数量計算に含まれる追加のかんばんの数です。  
9. 安全係数に「1」を設定します。
    * これは安全在庫の追加数量を計算するのに使用する係数です。  
10. [進んだ日数] フィールドに「30」を入力します。
    * これは需要計算に含まれるかんばん数量計算の日付より前の日数です。  
11. [遅れた日数] フィールドに「30」を入力します。
    * これは、需要の計算に含まれるかんばん数量の計算の日付からの繰り越し日数です。  計算に使用する式は、実際の値とともに表示されます。 たとえば、かんばん数量 = ((1 日の平均需要 x リード タイム x 2.00) / 材料取り扱い単位あたりの製品数量) + 1  
12. ページを閉じます。

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>かんばん数量計算ポリシーをかんばんルールへ追加する
1. [製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * この手順では、かんばんルール 000020 を選択します。  
3. 一覧で、選択された行のリンクをクリックします。
4. [かんばん数量計算ポリシー] セクションの展開を切り替えます。
5. [追加] をクリックします。
    * 以前のサブタスクで作成したかんばん数量の計算ポリシーを追加します。  
6. 一覧で、選択された行をマークします。
7. [名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
8. 一覧で、選択された行のリンクをクリックします。
    * 以前のサブタスクで作成した ポリシー Speaker2016 を追加します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]