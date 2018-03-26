---
title: "製品カテゴリの管理"
description: "このトピックでは、販売促進マネージャーが小売製品カテゴリを使用して、小売製品階層とリリースされた製品の詳細な関係を管理する方法について説明します。"
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>拡張された製品とカテゴリの管理

[!include[banner](./includes/banner.md)]

このトピックでは、Dynamics 365 for Retail の小売製品カテゴリと製品を管理するための強化された方法について説明します。 これらの拡張機能で、販売促進マネージャーは小売製品階層、およびリリース済製品の詳細の間の、製品プロパティ製品の共通構造を表示できます。

小売製品カテゴリの管理に関する詳細については、[カテゴリと製品の管理] ワークスペースから [小売製品カテゴリ] へ移動し、[小売製品カテゴリ] ページの拡張構造に注意してください。

![カテゴリと製品の管理ワークスペース](media/LaunchRetailProductHierarchy.png)

以前のバージョンでは、製品のプロパティは適用性の範囲に基づいて [基本的な製品プロパティ] と [小売製品プロパティ] に分割されていました。 [小売製品プロパティ] は適用の範囲で*グローバル*であり、これは特定の [小売製品プロパティ] について、すべての法人で同じ値が共有されることを意味します。 [基本的な製品プロパティ] は*法人固有*です。 つまり、特定の [基本的な製品プロパティ] では、個々の業務要件に基づいて、法人間で値が異なる場合があります。

拡張された小売製品カテゴリ構造では、リリースされた製品の詳細フォーム構造を反映するために、グループ内の適用性に基づいて製品プロパティが論理的に分離されます。

![適用範囲に基づいたフィールドのグループ化](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

法人特定のプロパティをすべての法人で管理するか、特定の法人用に管理するかのどちらかに切り替えることができます。 そのためには、[すべての法人用に表示/編集] または [特定の法人用に表示/編集] のいずれかを選択します。

![個人とすべての法人の表示の切り替え](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![個人とすべての法人の表示の切り替え](media/ToggleToEditForAllLegalEntities.PNG)  

以前のバージョンと比較して、新しい小売製品カテゴリ構造では、販売促進マネージャーは、個々のカテゴリ レベルで追加の製品プロパティ セットの既定値を定義することもできます。 製品の作成時には、これらのデフォルトの製品プロパティ値は、小売製品階層からの個々のカテゴリとの関連性に基づいて、製品に継承されます。 これらの継承された製品プロパティは、個々の業務要件を満たすために、製品ごとに変更することもできます。

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>プロパティを選択して Retail 製品カテゴリ フォームから製品を更新する 
 
この新しい拡張された製品プロパティ構造を使用して、更新された製品プロパティが関連付けられた製品にプッシュされる必要があるかを選択することができます。 

![製品更新の新しい拡張ビュー](media/NewUpdateProductsEnhancedView.PNG) 

販売促進マネージャーは、個々の業務要件を満たすために、各製品のこれらの継承された製品プロパティを変更できます。


