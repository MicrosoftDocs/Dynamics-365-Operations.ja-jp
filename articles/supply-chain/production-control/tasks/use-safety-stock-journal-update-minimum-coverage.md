---
title: 安全在庫仕訳帳を使用した最小補充の更新
description: この手順では、履歴トランザクションに基づいて最小補充提案を計算し、提案を使用して品目補充を更新する方法を示します。
author: ChristianRytt
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 022ec17d0fdc8b1ee204280ecaac40d75e9c1a44974f2bd4a9bb49fa0aa7878e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759434"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>安全在庫仕訳帳を使用した最小補充の更新

[!include [banner](../../includes/banner.md)]

この手順では、履歴トランザクションに基づいて最小補充提案を計算し、提案を使用して品目補充を更新する方法を示します。 これは安全在庫仕訳帳を使用して実行されます。 このタスクの作成に使用するデモ データの会社は USMF です。 このタスクは、生産計画担当者による最小補充の維持を支援することを意図しています。


## <a name="create-a-new-safety-stock-journal-name"></a>新しい安全在庫仕訳帳名を作成します。
1. **ナビゲーション ウィンドウ** で、**マスター プラン > 設定 > 安全在庫仕訳帳名** に移動します。
2. **新規** をクリックします。
3. **名前** フィールドに、「材料」と入力します。
4. **説明** フィールドに、「材料」と入力します。
5. ページを閉じます。

## <a name="create-a-safety-stock-journal"></a>安全在庫仕訳帳の作成
1. **ナビゲーション ウィンドウ** で、**マスター プラン > マスター プラン > 実行 > 安全在庫の計算** に移動します。
2. **新規** をクリックします。
3. **名前** フィールドで値を入力または選択します。 作成した安全在庫仕訳帳名、たとえば「材料」を選択します。  
4. **明細行の作成** をクリックします。
5. **開始日** フィールドに日付を入力します。  
6. **終了日** フィールドに、日付を入力します。
7. **OK** をクリックします。 これにより、在庫トランザクションがある分析コードの行が作成されます。  

## <a name="calculate-proposal"></a>提案の計算
1. **提案の計算** をクリックします。
2. **リード タイムで平均払出を使用** オプションを選択します。
3. **乗算の係数** を「10」に設定します。 提案を調整するために倍率が使用されます。 デモ データにはわずかなトランザクションしかないため、現実的な提案を得るためにはこの係数を設定する必要があります。  
4. **OK** をクリックします。 下へスクロールして M0002 と M0003 を見つけます。 **算出された最小** 数量列を表示します。   

## <a name="update-minimum-quantity"></a>最小数量の更新
1. **新しい最小数量** フィールドに数値を入力します。 [算出された最小数量] の値と一致するように新しい最小数量を更新します。 算出された最小がゼロの場合は、必要な将来価値を入力できます。 たとえば、倉庫 12 がある M0002 のこのフィールドに、[算出された最小数量] を入力できます。  
2. 一覧で、目的のレコードを見つけ、選択します。 たとえば、倉庫 12 がある M0002 を選択できます。  
3. **新しい最小数量** フィールドに数値を入力します。 [算出された最小数量] の値と一致するように新しい最小数量を更新します。 算出された最小がゼロの場合は、必要な将来価値を入力できます。  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>新しい最小数量を転記して結果を検証
1. **転記** をクリックします。
2. **OK** をクリックします。
3. クリックして、**品目番号** フィールドのリンク先を表示します。
4. クリックして、**品目番号** フィールドのリンク先を表示します。
5. **アクション ウィンドウ** で計画をクリックします。
6. **品目補充** をクリックします。 **最小数量** が、安全在庫仕訳帳からの新しい最小数量で更新されたことを確認します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]