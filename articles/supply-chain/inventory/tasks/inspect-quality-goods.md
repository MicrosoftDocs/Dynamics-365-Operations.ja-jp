---
title: 商品の品質の調査
description: このトピックでは、品質指示を処理する方法について示します。
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956137"
---
# <a name="inspect-the-quality-of-goods"></a>商品の品質の調査

[!include [banner](../../includes/banner.md)]

このトピックでは、品質指示を処理する方法について示します。 品質検査は、通常、品質検査の担当者により実行されます。

標準のデモ データがインストールされている場合は、そのデータを使用してこのトピックの手順を完了できます。 デモ データを使用するには、開始する前に *USMF* 法人を選択する必要があります。 その後、発注書 *000016* を確認して、製品のレシートを転記する必要があります。 品質指示は自動的に生成されます。

## <a name="step-1-select-a-quality-order"></a>手順 1: 品質指示を選択する

品質指示を選択するには、次の手順に従います。

1. **在庫管理 \> 定期処理タスク \> 品質管理 \> 品質指示** の順に移動します。
1. この手順を開始する前に生成された品質指示を選択します。

## <a name="step-2-record-test-results"></a>手順 2: テスト結果を記録する

テスト結果を記録するには、次の手順に従います。

1. **結果** を選択します。
1. **編集** を選択します。
1. **結果数量** フィールドに数値を入力します。
1. **結果** フィールドで、目的の記録を選択します。 この例では、結果は定義済の結果に基づいています。 通常、サイズまたは他の分析コードなどより詳細なテスト結果を記録します。
1. **保存** を選択します。
1. ページを閉じます。

## <a name="step-3-validate-the-quality-order"></a>手順 3: 品質指示を検証する

品質指示を検証するには、次の手順に従います。

1. **検証** を選択します。
1. **検証者** フィールドで、検査を行うユーザーを選択します。
1. **選択** を選択します。
1. **OK** を選択します。
1. ページを閉じます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
