---
title: "製品カテゴリの管理と作成"
description: "このトピックでは、Retail 製品カテゴリの管理エクスペリエンスに対する拡張機能について説明します。 これらの拡張機能で、販売促進マネージャーは Retail 製品階層とリリース済製品の詳細との間に相関関係を持てます。"
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 98250062892e0c5f665616dc3944181a3ff8599a
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="product-category-management-and-creation"></a>製品カテゴリの管理と作成

[!include[banner](./includes/banner.md)]

Retail 製品カテゴリの管理エクスペリエンスに対する拡張機能で、販売促進マネージャーは Retail 製品階層とリリース済製品の詳細との間に相関関係を持てます。 これらの拡張機能を表示するには、**カテゴリと製品の管理**ワークスペースで、[Retail 製品階層] を選択して [Retail 製品カテゴリの新しい構造] ページを開きます。 

以前のリリースでは、適用性の範囲に基づいて、製品のプロパティが Basic 製品のプロパティと Retail 製品のプロパティに分割されていました。 Retail 製品のプロパティは*グローバル*でした。 つまり、特定の製品のプロパティに、すべての法人で同じ値が共有されます。 Basic 製品のプロパティは*法人固有*でした。 つまり、特定の製品のプロパティは、個々の業務要件に基づいて、法人間で異なる場合があります。

これらの拡張機能では、Retail 製品カテゴリの製品のプロパティについて、グループ内の適用性に基づいて引き続きフィールドを区切り、リリース済製品の詳細フォームの構造を反映します。

法人特定のプロパティをすべての法人で管理するか、特定の法人用に管理するかのどちらかに切り替えることができます。 必要に応じて、[すべての法人用に表示/編集] または [特定の法人用に表示/編集] のいずれかを選択するだけです。

販売促進マネージャーは、個々のカテゴリのレベルで製品のプロパティの追加のセットに既定値を定義することもできます。 これらのプロパティ値は、製品の作成時に、カテゴリとの関連に基づいて製品に継承されます。

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>プロパティを選択して Retail 製品カテゴリ フォームから製品を更新する

論理グループのプロパティを使用して、関連付けられた製品にプッシュされる更新済の製品のプロパティを選択します。

販売促進マネージャーは、個々の業務要件を満たすために、各製品のこれらの継承された製品プロパティを変更できます。

