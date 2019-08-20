---
title: 分析コードの作成と分析コード メンバーのインポート
description: 原価会計は、他のモジュールからのマスター データを必要とする独立モジュールです。
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a7db93e1877034051b6add4c11ddfe7cd7d17e0b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841588"
---
# <a name="create-dimensions-and-import-dimension-members"></a>分析コードの作成と分析コード メンバーのインポート

[!include [banner](../includes/banner.md)]

原価会計は、他のモジュールからのデータを必要とする独立モジュールです。 このデータは、次のように分類されます。

-  コスト要素
-  原価オブジェクト
-  統計分析コード

**原価要素**は、勘定科目表で原価関連品目に対応します。 **原価オブジェクト**は、製品、コスト センター、またプロジェクトといった、見積したり、原価を割り当てたり、直接測定したりする財務分析コードのすべてのタイプに対応します。 **統計分析コード**とそのメンバーは、非通貨入力を登録するために使用されます。 統計分析コード メンバーは、コスト配分や配賦の配賦基準として使用できます。 

次の図は、原価会計で使用される分析コードを示します。

[![原価会計分析コード](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

原価会計にデータをインポートすると、組織のすべてのレベルでマネージャーに洞察を提供するさまざまな分析視点を構築するためにそのデータを使用することができます。 以下のトピックでは、分析コードの作成および分析コード メンバーのインポートに関する情報を提供します。 

-  [原価要素分析コード](cost-elements.md)
-  [原価要素の作成 (タスク ガイド)](./tasks/create-cost-elements.md)
-  [原価オブジェクト分析コード](cost-objects.md)
-  [原価要素の作成 (タスク ガイド)](./tasks/create-cost-objects.md)
-  [分析コード メンバーの共通セットに対する原価要素分析コード メンバーのマップ](map-cost-elements-dimension-members.md)
-  [原価要素分析コードのマップ (タスク ガイド)](./tasks/map-cost-element-dimension.md)
-  [統計分析コード メンバーと統計測定プロバイダー テンプレート](statistical-measure-provider-template.md)






