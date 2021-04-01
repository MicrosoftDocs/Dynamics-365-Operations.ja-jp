---
title: 資産エラー原価管理
description: このトピックでは、資産管理の資産エラー原価管理について説明します。
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c25b3efbd0f2f0ec22a08aeac54ffb7fd9398c83
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253833"
---
# <a name="asset-fault-cost-control"></a>資産エラー原価管理

[!include [banner](../../includes/banner.md)]

 

資産管理では、資産エラー登録で原価を計算して、予算原価と比較した実際原価の概要を取得できます。 実際原価は、転記されたトランザクションに基づいています。 日付は、現象が記録されたエラー日付を示します。

1. **資産管理** > **照会** > **資産エラー** > **資産エラー原価管理** の順にクリックします。

2. **資産エラー原価管理** ダイアログでは、必要に応じて計算に含める財務分析コード セットを選択します。

4. 原価がゼロの結果を表示しない場合は、**ゼロをスキップ** トグル ボタンで "はい" を選択します。

5. **レベル** フィールドを使用すると、機能的な場所に関する原価管理明細行の詳細度を指定できます。 

    たとえば、フィールドに "1" の番号を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべての資産エラー原価管理の明細行が最上位レベルに表示されます。したがって明細行の時間は、下位レベルにある機能的な場所から追加される場合があります。 
    
    **レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルですべての資産エラー原価管理の明細行を示す、詳細な結果が表示されます。

6. 検索を制限する場合は、**対象に含めるレコード** クイック タブで特定の資産、エラー日付、およびエラーの原因を選択できます。

7. **OK** をクリックして、計算を開始します。

8. **グループ化** ボタンをクリックすると、計算の必要な詳細レベルが表示されます。 選択した **グループ化** ボタンが強調表示されます。 ボタンをクリックして、有効または無効にします。

## <a name="example"></a>例

この例では、資産エラー原価管理の計算を示します。

- **元の予算** フィールドでは、作業指示書予測からの予算原価が表示されます。 
- **実際原価** フィールドには、作業指示書の転記済原価が表示されます。 
- **確定済み費用** フィールドには、作業指示書に関連して会社が確定した原価合計が表示されます。

    ![図 1](media/05-controlling-and-reporting.png)

エラーの設定方法に関しては、[エラー管理](../setup-for-work-orders/fault-management.md) トピックを参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]