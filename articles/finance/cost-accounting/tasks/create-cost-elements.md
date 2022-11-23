---
title: 原価要素の作成
description: 原価計算の原価要素を作成するにはいくつかの方法があります。
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779692"
---
# <a name="create-cost-elements"></a>原価要素の作成 

[!include [banner](../../includes/banner.md)]

原価計算の原価要素を作成するにはいくつかの方法があります。 この手順では、データ コネクタ経由で主勘定をインポートしてコスト要素を作成する方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された原価計算の機能についての手順です。


## <a name="create-new-cost-elements"></a>新規コスト要素を作成する
1. **原価計算 > 分析コード > コスト要素分析コード** の順序で進みます。
2. **新規** をクリックします。
3. **名前** フィールドに値を入力します。
4. **分析コード メンバーのデータ コネクター** フィールドで、値を入力または選択します。
5. **説明** フィールドで、値を入力します。
6. **保存** をクリックします。

## <a name="configure-the-data-connector"></a>データコネクターを構成する
1. **分析コード メンバー プロバイダーのコンフィギュレーション** をクリックします。
2. **勘定科目表** フィールドで、値を入力または選択します。
    * 共有勘定科目表使用の **共有** を選択します。  
3. **新規** をクリックします。
4. 一覧で、選択された行をマークします。
    * 基準を満たす口座にフィルターを適用できます。  
5. **主勘定 (元)** フィールドで、値を入力または選択します。
6. **主勘定 (先)** フィールドで、値を入力または選択します。
7. **OK** をクリックします。

## <a name="import-main-accounts"></a>主勘定のインポート
1. **分析コード メンバーをインポート** をクリックします。
    * 主勘定は原価計算にインポートされ、コスト要素として使用されます。  
2. **OK** をクリックします。

## <a name="view-the-imported-accounts-as-cost-elements"></a>コスト要素としてインポートされた勘定を表示する
1. **分析コード メンバーの表示** をクリックします。
    * 原価が適用される事業のコスト要素として、インポートされた勘定科目が表示されます。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
