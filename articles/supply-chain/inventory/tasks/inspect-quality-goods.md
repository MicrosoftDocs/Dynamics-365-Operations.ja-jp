---
title: 商品の品質の調査
description: このトピックでは、品質指示を処理する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbfb3733cc52f0f8f54ab4388764429387358ee7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011525"
---
# <a name="inspect-the-quality-of-goods"></a>商品の品質の調査

[!include [banner](../../includes/banner.md)]

このトピックでは、品質指示を処理する方法について説明します。 デモ データの会社 USMF でこのガイドを実行できます。 このサンプル手順を開始する前に、発注書 "000016" を確認し、製品受領書を転記する必要があります。 これにより、品質指示が自動的に作成されます。 品質検査は、通常、品質検査の担当者により実行されます。


## <a name="select-a-quality-order"></a>品質指示の選択
1. ナビゲーション ウィンドウで **モジュール > 在庫管理 > 定期処理 > 品質管理 > 品質指示** に移動します。
2. この手順を開始する前に作成された品質指示を選択します。  

## <a name="record-test-results"></a>テスト結果の記録
1. **結果** を選択します。
2. **編集** を選択します。
3. **結果数量** フィールドに数値を入力します。
4. **結果** フィールドで、ドロップダウン メニューから目的のレコードを選択します。  
- この例では、結果は定義済の結果に基づいています。 通常、サイズまたは他の分析コードなどより詳細なテスト結果を記録します。  
5. **保存** を選択します。
6. ページを閉じます。

## <a name="validate-the-quality-order"></a>品質指示を検証する
1. **検証** を選択します。
2. **検証者** フィールドで、ドロップダウン メニューから検査を実行するユーザーを選択します。  
3. **選択** をクリックします。
4. **OK** を選択します。
5. ページを閉じます。

