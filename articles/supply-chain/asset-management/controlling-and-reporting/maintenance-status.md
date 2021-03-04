---
title: メンテナンスの状態
description: このトピックでは、資産管理でメンテナンス ステータスを計算する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43389db93032ec29adb805f86ae04a686803176f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431859"
---
# <a name="maintenance-status"></a>メンテナンスの状態

[!include [banner](../../includes/banner.md)]

 

資産管理で、新しい、有効な、および完了したメンテナンス要求、作業指示書、およびメンテナンス ダウンタイム アクティビティに関する特定の期間の概要計算を実行できます。 また、同じ期間に完了した条件評価の数を表示することもできます。 この計算を使用して、受信および完了したメンテナンス要求および作業指示書に関するワークロードの概要を取得することができます。

## <a name="make-a-maintenance-status-calculation"></a>メンテナンス ステータスの計算の実行

1. **資産管理** > **照会** > **メンテナンス ステータス** をクリックします。

2. **ステータスの計算** ダイアログ内の **開始日** および **終了日** フィールドで、計算を実行する時間範囲を選択します。

3. **レベル** フィールドを使用すると、機能の場所に関するメンテナンス明細行の詳細度を指定できます。 

  たとえば、フィールドに「1」の番号を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべてのメンテナンス明細行が最上位レベルに表示されます。したがって明細行のステータスは、下位レベルにある機能的な場所から追加される場合があります。 
  
  **レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルですべてメンテナンス明細行を示す、詳細な結果が表示されます。

4. **OK** をクリックして、計算を開始します。

5. **グループ化** ボタンをクリックすると、計算の必要な詳細レベルが表示されます。 選択した **グループ化** ボタンが強調表示されます。 ボタンをクリックして、有効または無効にします。

6. **グループ化** ボタンを有効化または無効化するか、または新しい期間に対して計算を実行することにより、変更を行うたびに **更新** ボタンをクリックし、計算を更新してください。

7. 新しいメンテナンス ステータスの計算を作成する場合、**ステータス** をクリックします。

>[!NOTE]
>**メンテナンス ステータス** に表示される結果には、実際の開始日時があるメンテナンス要求および作業指示書のみが含まれます。 終了日時は空白にすることができます。

## <a name="example-1"></a>例 1

次のスクリーンショットでは、**年** および **月** ボタンが有効化されています。 これらの **グループ化** オプションを選択すると、メンテナンス要求と作業指示書に関連する月ごとのワークロードとスループットの一般的な概要を取得します。 

![月ごとのワークロードの例](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>例 2

次のスクリーンショットでは、機能の場所に関する情報が追加されています。 地理的な場所、工場、または作業領域を表す機能の場所間でワークロードおよびスループットを比較することができるようになりました。 

![機能の場所を含む月ごとのワークロードの例](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]