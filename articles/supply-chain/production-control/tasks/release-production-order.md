---
title: 製造オーダーのリリース
description: この手順では、製造オーダーのリリース方法を示します。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm, ProdSetupRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f5c5ca5ebf51d0722318c455e6ca59d3a893793
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831965"
---
# <a name="release-a-production-order"></a>製造オーダーのリリース

[!include [banner](../../includes/banner.md)]

この手順では、製造オーダーのリリース方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 4 番目です。

1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
    * [スケジュール済] 状態を持つ製造オーダーをグリッドで選択します。  
2. アクション ペインで、[製造オーダー] をクリックします。
3. [リリース] をクリックします。
    * このページで、製造オーダーの選択範囲のリリースを確認できます。 注文を追加する場合は、[選択] をクリックします。  
    * リリース ステップは、作業現場のオペレーターが生産ジョブの進捗をレポートできるように製造オーダーを生産の作業現場にいつリリースするかを示します。 ジョブの処理に関する情報を含む生産文書は発行できます。 原材料ピッキングの倉庫作業は、倉庫のプロセス用に設定された品目に対して生成されます。  
4. [一般] タブをクリックします。
    * どの生産レポートを印刷するかを選択します。 ジョブ カード レポートでは、スケジュールされた個々のジョブのページが印刷され、製造オーダーがジョブ レベルにスケジュールされることを必要とします。 レポートには、予定された開始時刻と終了時刻、生産数量、どのリソースがジョブを処理するかに関する情報が含まれます。 工順ジョブ レポートは、同じページにある同じ情報を収集しますが、各ジョブのページは印刷されません。 工順カード レポートには工程のみが表示され、ジョブは表示されません。 したがって、このレポートは、ジョブのスケジューリングを必要としませんが、製造オーダーが工程レベルでスケジューリングされる時に使用できます。  
5. [工順カードの印刷] チェック ボックスをクリックします。
6. [OK] をクリックします。
7. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]