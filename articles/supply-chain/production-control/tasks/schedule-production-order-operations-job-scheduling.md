---
title: 工程とジョブのスケジューリングによる製造オーダーのスケジュール
description: この記事では、工程のスケジューリングとジョブのスケジューリングで製造オーダーのスケジューリングを行うことに焦点を当てています。
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d82d5439e57c02ddc9db4222a946bd15f4ed67e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903930"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>工程とジョブのスケジューリングによる製造オーダーのスケジュール

[!include [banner](../../includes/banner.md)]

この記事では、工程のスケジューリングとジョブのスケジューリングで製造オーダーのスケジューリングを行うことに焦点を当てています。 ジョブは、ジョブのスケジューリングで作成されますが、工程のスケジューリングでは作成されません。 このタスクの作成に使用するデモ データの会社は USMF です。 この手順は、個別の製造環境で作業をしている生産マネージャ、生産計画担当者、または作業現場の監督を対象としています。


## <a name="create-a-production-order"></a>製造オーダーの作成
1. ナビゲーション ウィンドウで、**モジュール > 生産管理 > 製造オーダー > すべての製造オーダー** の順に移動します。
2. **新しい製造オーダー** を選択します。
3. **品目番号グループ** フィールドで、値を入力または選択します。 品目番号 **D0001** を選択します。  
4. **作成** を選択します。

## <a name="schedule-operations-for-the-production-order"></a>製造オーダの工程のスケジュール
1. 新しく作成された行をマークします。      
2. アクション ウィンドウで、**スケジュール** を選択します。
3. **工程のスケジュール** を選択します。
4. **スケジューリング指示** のフィールドで、**スケジューリングの日付からフォワード** を選択します。
5. **スケジューリングの日付** フィールドに、日付を入力します。 将来期日、たとえば、今日とさらに 1 週間を選択します。 選択されたスケジューリング指示で、製造オーダーは、この日付を起点としてスケジューリングされます。  
6. **OK** を選択します。
7. 一覧で、選択された行をマークします。 ステータスが **スケジュール済** に変わることに注意してください。 
8. **すべてのジョブ** を選択します。 ジョブは、工程のスケジューリングで作成されないことに注意してください。  
9. ページを閉じます。

## <a name="schedule-jobs-for-the-production-order"></a>製造オーダのジョブのスケジュール
1. アクション ウィンドウで、**スケジュール** を選択します。
2. **ジョブのスケジュール** を選択します。
3. **スケジューリング指示** のフィールドで、**スケジューリングの日付からフォワード** を選択します。
4. **スケジューリングの日付** フィールドに、日付を入力します。 将来の日付、たとえば、今日とさらに 1 週間を選択します。 選択されたスケジューリング指示で、製造オーダーは、この日付を起点としてスケジューリングされます。  
5. **OK** を選択します。
6. アクション ウィンドウで、**製造オーダー** をクリックします。
7. **すべてのジョブ** を選択します。 有効な工順に基づいて、ジョブ スケジューリングで5 つのジョブが作成されることに注意してください。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]