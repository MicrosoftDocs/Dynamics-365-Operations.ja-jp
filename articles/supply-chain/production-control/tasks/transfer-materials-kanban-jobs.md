---
title: かんばん作業と材料の転送
description: この手順では、かんばん回収作業を実行し、材料を転送することに焦点をあてます。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8808b168d2b3845b315e6bbcfb376e37f31fe4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981034"
---
# <a name="transfer-materials-with-kanban-jobs"></a>かんばん作業と材料の転送

[!include [banner](../../includes/banner.md)]

この手順では、かんばん回収作業を実行し、材料を転送することに焦点をあてます。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、倉庫作業者を対象としています。


## <a name="display-transfer-jobs"></a>転送ジョブの表示
1. [生産管理] > [かんばん] > [転送ジョブのかんばんボード] の順に移動します。
2. [フィルター] セクションを展開または折りたたみます。
    * [フィルター] セクションで、[生産フロー]、[活動名]、[移動元倉庫と移動元場所]、[移動先倉庫と移動先場所] にフィルターを使用すると、表示するジョブを指定できます。  
3. [元倉庫] フィールドに、「11」と入力します。
4. [移動先場所] フィールドに、「12」と入力します。

## <a name="start-a-transfer-job"></a>転送ジョブの開始
1. 一覧で、選択された行 (ある場合) を選択解除します。
2. 一覧で行 4 を選択します。
    * ステータスが [未定] である最初のジョブを選択します。 これが選択した唯一のジョブであることを確認します。  
3. [開始] をクリックします。
    * アイコンはジョブが開始されることを示します。  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>2 番目の配送ジョブを選択して数量を変更する
1. 一覧で、目的のレコードを見つけ、選択します。
    * 複数のジョブを選択できますが、とりあえず 5 行目を選択します。  
2. 一覧で、目的のレコードを見つけ、選択します。
    * 以前の手順でジョブ 1 つのみが選択されたことを確認します。 他のすべてのジョブを選択解除します。  
3. 後で参照するために、ジョブ数量フィールドの値をメモする
4. [ジョブ数量] を「30」に設定します。
    * 警告です! 30 を転送することはできません。 かんばんルールの設定に従って、元の数量のみを転送できます。  
5. ジョブ数量フィールドに以前にメモした値を使用する
    * 以前の値にジョブ数量を設定します。  

## <a name="start-the-second-transfer-job"></a>2 番目の配送ジョブの開始
1. [開始] をクリックします。
    * これにより、5 行目のジョブの転送が開始されます。  

## <a name="complete-both-transfer-jobs"></a>両方の転送ジョブの完了
1. 一覧で行 4 を選択します。
    * 2 つの転送ジョブが 4 行目、5 行目で選択されました。  
2. [完了] をクリックします。
    * これで、両方のジョブの転送が完了します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]