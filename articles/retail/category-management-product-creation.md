---
title: 小売製品カテゴリと製品を管理します。
description: このトピックでは、販売促進マネージャーが小売製品カテゴリを使用して、小売製品階層とリリースされた製品の詳細な関係を管理する方法について説明します。
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 27870fe6172479b891b885d9e84ca10b250e3399
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019511"
---
# <a name="manage-retail-product-categories-and-products"></a>小売製品カテゴリおよび製品の管理

[!include [banner](./includes/banner.md)]

このトピックでは、Dynamics 365 Retail の製品カテゴリと製品を管理するための強化された方法について説明します。 拡張機能で、販売促進マネージャーは製品階層、およびリリース済製品の詳細の間で共有されている製品プロパティの構造を表示できます。

製品カテゴリの管理に関する詳細については、**カテゴリと製品の管理**ワークスペースの**小売製品階層**タイルを選択してください。

表示される **小売製品階層** ページの強化された構造を確認します。 Retail の以前のバージョンでは、製品のプロパティは適用性の範囲に基づいて *基本的な製品プロパティ* と *小売製品プロパティ* に分割されていました。 小売製品プロパティは適用範囲が*グローバル*です。 つまり、特定の製品のプロパティに、すべての法人で同じ値が共有されます。 対照的に、基本的な製品プロパティは*法人固有*です。 つまり、特定の製品のプロパティでは、各法人の個々の業務要件に応じて、法人間で値が異なる場合があります。

拡張された製品カテゴリ構造では、リリースされた製品の詳細フォーム構造の構造を反映するために、グループの適用性に基づいて製品プロパティが論理的に分離されます。

![フィールドはプロパティの適用範囲に基づいてグループ化されます。](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

法人特定のプロパティをすべての法人で管理するか、特定の法人用に管理するかのどちらかに切り替えることができます。

すべての法人の間でプロパティを管理するには、**すべての法人用に表示** (または**すべての法人用に編集**) を選択してください。

![すべての法人用に表示/編集](media/ToggleBackToEditForSpecificLegalEntity.PNG)

特定の法人のプロパティを管理するには、**特定の法人用に表示** (または**特定の法人用に編集**) を選択してください。

![特定の法人用に表示/編集](media/ToggleToEditForAllLegalEntities.PNG)

また、拡張された小売製品カテゴリ構造では、販売促進マネージャーが、個々のカテゴリ レベルで追加の製品プロパティ セットの既定値を定義できるようになりました。 次に、製品が作成されると、製品階層内の個々のカテゴリとそれらのプロパティの関連付けに基づいて、製品プロパティの既定値が継承されます。 これらの継承された製品プロパティは、個々の業務要件を満たすために製品ごとに変更することもできます。

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Retail 製品階層ページで製品を更新するためのプロパティの選択

新しい、拡張された製品プロパティ構造を使用して、関連付けられた製品にプッシュされる必要がある更新された製品プロパティを選択することができます。 **小売製品階層** ページのアクション ウィンドウで、**カテゴリ**を選択し、次に**製品の更新**を選択して **製品の更新** ダイアログ ボックスを開きます。

![製品の更新ダイアログ ボックス](media/NewUpdateProductsEnhancedView.PNG)
