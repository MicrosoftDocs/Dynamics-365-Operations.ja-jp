---
title: 最大能力負荷の計算
description: この記事では、資産管理で最大能力負荷を計算する方法について説明します。
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95d1e38db8e4658a57f36139836264b87d525e61
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016133"
---
# <a name="calculate-capacity-load"></a>最大能力負荷の計算

[!include [banner](../../includes/banner.md)]


資産管理で、次の最大能力負荷を計算します。

- メンテナンス スケジュール明細行  
- まだスケジュールされていない作業指示書  
- スケジュール済作業指示書

これは、特定の期間における予想される最大能力負荷の概要を取得する場合に役に立ちます。 最大能力負荷の計算は、すべての資産または選択した資産に対して行うことができます。 また、メンテナンス ダウンタイム活動や作業指示書プールで計算を行うこともできます。

1. **資産管理** > **照会** > **最大キャパシティ負荷** の順に、または **資産管理** > **作業指示書プール** > **すべての作業指示書プール** / **有効な作業指示書プール** > リスト内で作業指示書プールの選択 > **最大キャパシティ負荷** ボタンの順に、または **資産管理** > **メンテナンス ダウンタイム活動** > **すべてのメンテナンス ダウンタイム活動** / **有効なメンテナンス ダウンタイム活動** > リスト内でメンテナンス活動を選択 > **最大キャパシティ負荷** ボタンの順にクリックします。

2. **最大能力負荷の計算** ダイアログで、**開始日/時刻** および **終了日/時刻** フィールドの計算に対する期間を選択します。

3. 計算にメンテナンス スケジュール行を含める場合は、**メンテナンス スケジュールを含める** トグル ボタンで "はい" を選択します。

4. 計算に作業指示書ジョブを含める場合は、**作業指示書を含める** トグル ボタンで "はい" を選択します。

5. **レベル** フィールドを使用すると、機能的な場所に関する最大能力負荷行の詳細度を指定できます。 

    たとえば、フィールドに数値 "1" を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべてのメンテナンス スケジュール明細行および作業指示書が最上位レベルに表示されます。したがって明細行の時間は、下位レベルにある機能的な場所から追加される場合があります。 
    
    **レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルですべてメンテナンス スケジュール行および作業指示書を示す、詳細な結果が表示されます。

6. **OK** をクリックして、計算を開始します。

7. **グループ化** グループで、関連するボタンをクリックすると、計算の必要な詳細レベルが表示されます。 下のスクリーンショットでは、選択した **グループ化** ボタンが青色で強調表示されています。 ボタンをクリックして、有効または無効にします。

    ![図 1。](media/01-capacity-planning.png)

>[!NOTE]
>スケジュール済み作業指示書に関する能力計画にのみ焦点を合わせる場合は、[スケジュール済み作業指示書の最大能力負荷の計算](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md) を参照してください。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]