---
title: 積荷計画ワークベンチを使用した積荷および出荷の計画
description: この記事では、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。
author: Mirzaab
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e53b7667dd4589a7c6c14b8aaf8ba51017eee0d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068333"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>積荷計画ワークベンチを使用した積荷および出荷の計画

[!include [banner](../../includes/banner.md)]

この記事では、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。 前提条件として、まず販売注文を作成します。 この手順は、配送コーディネーターの日常の作業一部です。 この手順の作成に使用するデモ データの会社は USMF です。


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
10. **倉庫** フィールドに、この例の場合、「24」と入力します。 この倉庫は、輸送管理および倉庫管理プロセス (WMS) で有効になっています。  
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