---
title: 原価オブジェクトの作成
description: この手順は、データコネクター経由でコスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734133"
---
# <a name="create-cost-objects"></a>原価オブジェクトの作成 

[!include [banner](../../includes/banner.md)]

この手順は、データコネクター経由でコスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 


## <a name="create-new-cost-objects"></a>新規原価対象を作成する
1. **原価計算 > 分析コード > 原価オブジェクト分析コード** の順序で進みます。
2. **新規** をクリックします。
3. **名前** フィールドに値を入力します。
4. **分析コード メンバーのデータ コネクター** フィールドで、値を入力または選択します。
5. **説明** フィールドで、値を入力します。
6. **保存** をクリックします。

## <a name="configure-the-data-connector"></a>データコネクターを構成する
1. **分析コード メンバー プロバイダーのコンフィギュレーション** をクリックします。
    * コストセンターを選択し、コストセンターの分析コードを原画計算にインポートします。  
2. **分析コード名称** フィールドでコスト センターを選択します。
3. **OK** をクリックします。

## <a name="import-cost-centers"></a>コスト センターをインポートする
1. **分析コード メンバーをインポート** をクリックします。
2. **OK** をクリックします。

## <a name="view-the-imported-cost-centers"></a>インポートされたコストセンターを表示します。
1. **分析コード メンバーの表示** をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
