---
title: 原価オブジェクトの作成
description: この手順は、データコネクター経由でコスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990770"
---
# <a name="create-cost-objects"></a>原価オブジェクトの作成 

[!include [banner](../../includes/banner.md)]

この手順は、データコネクター経由でコスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 


## <a name="create-new-cost-objects"></a>新規原価対象を作成する
1. [原価計算] > [分析コード] > [原価対象分析コード] の順序で進みます。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [分析コードメンバーのデータコネクター] フィールドで、値を入力または選択します。
5. [説明] フィールドに値を入力します。
6. [保存] をクリックします。

## <a name="configure-the-data-connector"></a>データコネクターを構成する
1. 「分析コード メンバー プロバイダーのコンフィギュレーション」をクリックします。
    * コストセンターを選択し、コストセンターの分析コードを原画計算にインポートします。  
2. [分析コード名称] フィールドでコストを選択します。
3. [OK] をクリックします。

## <a name="import-cost-centers"></a>コスト センターをインポートする
1. [分析コード メンバーをインポート] をクリックします。
2. [OK] をクリックします。

## <a name="view-the-imported-cost-centers"></a>インポートされたコストセンターを表示します。
1. [分析コード メンバーの表示] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]