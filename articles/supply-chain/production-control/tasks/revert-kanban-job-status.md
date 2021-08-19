---
title: かんばん作業状態を元に戻す
description: この手順は、間違ったかんばん作業ステータスを元に戻すことに焦点をあてます。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef6d77aae52dc81bb1b34acc74d4174a7dfe0482f3af5123f93688244cf50f9f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728534"
---
# <a name="revert-kanban-job-status"></a>かんばん作業状態を元に戻す

[!include [banner](../../includes/banner.md)]

この手順は、間違ったかんばん作業ステータスを元に戻すことに焦点をあてます。 これは機械オペレーターが間違ったジョブを更新してしまった場合に、または誤って間違ったステータスを設定してしまった場合に役立ちます。 この手順によって、かんばん作業が誤って作成時に登録された時に、ステータスが元に戻されます。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、リーン生産会社で働いている現場監督または機械オペレーターを対象としています。


## <a name="open-process-board-for-the-work-cell"></a>作業セルのプロセス ボードを開く
1. [プロセス ジョブのかんばんボード] に移動します。
2. [作業セル] フィールドで、値を入力または選択します。
    * 作業セル 1260 を選択します。  

## <a name="prepare-kanban-job"></a>かんばん作業の準備
1. [準備] をクリックします。
    * 灰色表示であるために [準備] をクリックできない場合、選択したかんばん作業が、空のかんばんアイコンによって示される [計画済] ステータスになっていることを確認します。 [準備] が失敗した場合、[ピッキング リスト] のすべての材料が使用可能であることを確認します。  
2. リストから準備済のジョブを選択します。
    * 準備した最初のジョブを選択します。  
    * 内側が三角になっているかんばんアイコンが表示されることによって、ジョブのステータスが準備されていることを確認してください。  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>準備済かんばん作業の状態を元に戻す
1. 一覧で、選択された行をマークします。
    * 準備した最初のジョブを選択します。  
2. [アクション ペイン] 上で、[製造] をクリックします。
3. [状態を元に戻す] をクリックします。
    * 次の条件があてはまる場合、代替かんばんルールを使用できます: - 補充方法は両方のルールとも同じです。  - 生産フローのバージョンは両方のルールとも同じです。  - 供給製品は両方のルールとも同じです。  - かんばんルールの最終活動のように構成されている下流活動は、両方のルールとも同じである必要があります。  - 同じ支給された在庫分析コードは両方のルール用に構成する必要があります。  - 材料取り扱い単位のステータスは [未割当] になっている必要があります。  - イベントかんばんの構成が同じである必要があります。  
    * 新しいステータスが [計画済] になっていることを確認します。  
4. [OK] をクリックします。
5. 一覧で、選択された行のマークを解除します。
    * 同じジョブを選択します。  
    * 空のかんばんアイコンによって示される、かんばん作業のジョブ ステータスが [計画済] に戻されていることを確認してください。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]