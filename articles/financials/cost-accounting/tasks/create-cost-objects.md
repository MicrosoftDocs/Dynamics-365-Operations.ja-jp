---
title: 原価オブジェクトの作成
description: この手順では、データ コネクタ経由で Dynamics 365 for Finance and Operations Enterprise Edition コスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543774"
---
# <a name="create-cost-objects"></a>原価オブジェクトの作成 

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、データ コネクタ経由で Dynamics 365 for Finance and Operations Enterprise Edition コスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された原価計算の機能についての手順です。


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

