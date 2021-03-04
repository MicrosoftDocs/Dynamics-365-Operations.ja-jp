---
title: 積荷計画ワークベンチを使用した積荷および出荷の計画
description: このトピックでは、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c37a98a3728cb1233a6e1207975a6b8f23f8120d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432343"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>積荷計画ワークベンチを使用した積荷および出荷の計画

[!include [banner](../../includes/banner.md)]

このトピックでは、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。 前提条件として、まず販売注文を作成します。 この手順は、配送コーディネーターの日常の作業一部です。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="create-a-sales-order"></a>販売注文の作成
1. **ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 注文 > すべての販売注文** の順に移動します。
2. **新規** を選択します。
3. **顧客口座** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。
4. 勘定 **US-004** を選択します。
5. **OK** を選択します。
6. **品目番号** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。
7. 品目 **A0001** を選択します。 **A0001** は輸送管理に対して有効になっています。  
8. **サイト** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開き、次に品目を選択します。
9. **数量** フィールドに、数値を入力します。
10. **倉庫** フィールドに、この例の場合、「24」と入力します。 この倉庫は、輸送管理および高度な倉庫管理で有効になっています。  
11. **保存** を選択します。
12. ページを閉じます。

## <a name="create-a-new-load"></a>新しい積荷の作成
1. **ナビゲーション ウィンドウ > モジュール > 輸送管理 > 計画 > 積荷計画ワークベンチ** の順に移動します。
2. **販売明細行** タブを選択します。次に、作成した販売注文の積荷を構築します。 積荷は、発注書、移動オーダー、および販売注文からの供給と需要に基づいて作成することができます。  
3. アクション ウィンドウで、**供給と需要** を選択します。
4. **新しい積荷へ** を選択します。
5. **読み込みテンプレート ID** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。 積荷のテンプレートには、積荷全体の重量および容積の最大測定値を定義します。 たとえば、積荷テンプレートは、コンテナーまたはトラックのサイズを表す場合があります。 品目を選択します。
6. **OK** を選択します。

## <a name="rate-and-route-the-load"></a>積荷のレートと工順
1. **評価とルート指定** を選択します。
2. **レート工順ワークベンチ** を選択します。
3. **レート ショップ** を選択します。
4. 一覧で、目的のレコードを見つけ、選択します。
5. **割り当て** を選択します。
6. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]