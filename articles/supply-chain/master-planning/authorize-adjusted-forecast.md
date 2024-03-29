---
title: 調整された予測の承認
description: すべての予測データがすぐに承認される必要はありません。 この記事では、予測が承認される期間を指定する方法を説明します。 また、特定の会社と予測モデルの予測を承認する方法も説明します。
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4954b70e56482e419d81485b544cb5d0b4e4a3ce
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740714"
---
# <a name="authorize-an-adjusted-forecast"></a>調整された予測の承認

[!include [banner](../includes/banner.md)]

すべての予測データがすぐに承認される必要はありません。 この記事では、予測が承認される期間を指定する方法を説明します。 また、特定の会社と予測モデルの予測を承認する方法も説明します。

すべての予測データがすぐに承認される必要はありません。 予測が承認される期間の開始日と終了日を指定できます。 この機能により、特定のバケットを凍結できます。 

指定する開始日と終了日が、予測が生成されたバケットの開始日と終了日に対応する必要があります。 調整が必要な場合、システムではこの制限が適用され、自動的に日付を調整します。 

**認証** ページの **詳細** タブで、最後に生成された予測に関する詳細を表示できます。 

会社および予測モデルを選択して、使用する予測を承認できます。 既定では、グリッドに需要予測が作成されたすべての会社が含まれます。 会社ごとに、現在の予測計画に対応する予測モデルは、パラメーターが事前に入力されているマスタ プランに設定されています。 ただし、この予測モデルをその会社に属するすべての予測モデルに変更できます。 需要予測データが選択した会社に対して生成されない場合は、インポート時に警告メッセージが表示されます。 

**ベースライン需要予測に対して行われた手動調整の保存** チェック ボックスの機能を理解することは非常に重要です。 統計ベースラインの予測に手動調整がある場合、調整された値はこのチェック ボックスがオフの場合でも使用のために承認されます。 ただし、変更は承認後に破棄されます。 したがって、次に予測が生成される時、**手動調整を需要予測に転送** が選択されている場合でも、その予測は統計予測のみで手動上書きはありません。 したがって、**ベースライン需要予測に対して行われた手動調整の保存** チェック ボックスを、すべて手動による変更で維持または破棄するメカニズムと仮定できます。

## <a name="additional-resources"></a>追加リソース

- [ベースライン予測に対して手動調整を行う](manual-adjustments-baseline-forecast.md)
- [予測精度の監視](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]