---
title: 作業セルで材料が利用不可の場合にプロセスかんばん作業を準備
description: この手順では、作業セルで材料が利用不可能な場合にプロセスかんばん作業を準備することに焦点をあてるため、倉庫からの材料をピッキングすることが必要です。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d57df6188aacc2f8a56a7ba91c4ab50a90901a7e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431660"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>作業セルで材料が利用不可の場合にプロセスかんばん作業を準備

[!include [banner](../../includes/banner.md)]

この手順では、作業セルで材料が利用不可能な場合にプロセスかんばん作業を準備することに焦点をあてるため、倉庫からの材料をピッキングすることが必要です。 「材料が利用可能な場合にプロセスかんばん作業を準備する」という手順は、この手順を作成するための前提条件です。 この手順は、機械オペレーターを対象としています。 この手順の作成に使用するデモ データの会社は USMF です。

1. [生産管理] > [かんばん] > [プロセス ジョブのかんばんボード] の順に移動します。
2. [作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
    * 作業セル 1250 を選択します。  
4. 一覧で、目的のレコードを見つけ、選択します。
    * 「かんばん 000356」を選択します。  
5. 一覧で、目的のレコードを見つけ、選択します。
    * 一覧で、行 4 を選択解除します。 または、「材料が利用可能な場合にプロセスかんばん作業を準備する」というタスクが完了していない場合は、行 4 を選択します。  
6. [ピッキング リスト] セクションの展開を切り替えます。
    * 供給のステータスにエントリー アイコンがないということは、品目「P0002」の 48 ea が作業セルに存在しないことを示します。  

## <a name="transfer-materials-to-work-cell"></a>材料を作業セルに移動する
1. [転送ジョブ] セクションの展開を切り替えます。
2. クイック フィルターを使用して、'P0002' の値で品目番号フィールドにフィルターを適用します。
3. 一覧で、目的のレコードを見つけ、選択します。
4. [開始] をクリックします。
    * 転送処理中です。  
5. [完了] をクリックします。
    * 品目「P0002」は、かんばん作業のピッキング リストから使用可能です。 これは、必要なすべての材料でかんばんを準備することを意味します。  
6. [準備] をクリックします。
    * [ジョブ ステータス] にアイコンがあるということは、ジョブが準備が整っていることを意味します。  

