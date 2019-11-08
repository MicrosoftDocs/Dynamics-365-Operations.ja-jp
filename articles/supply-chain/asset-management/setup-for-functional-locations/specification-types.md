---
title: 属性タイプの管理
description: このトピックでは、資産管理で属性タイプを作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c07f303b72f286c33979181fca1592b47efa1303
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571234"
---
# <a name="maintenance-attribute-types"></a>属性タイプの管理

[!include [banner](../../includes/banner.md)]

 

このトピックでは、資産管理で属性タイプを作成する方法について説明します。 属性は、さまざまな要素のプロパティを記述するために使用されます。 次の要素の属性を設定できます。

- [機能的な場所のタイプ](../setup-for-functional-locations/functional-location-types.md)
- [機能的な場所](../functional-locations/create-functional-locations.md)
- [資産タイプ](../setup-for-objects/object-types.md)
- 資産

設定できる属性は、要素によって異なります。 たとえば、機能的な場所の場合、場所の構成と物理サイズの属性を設定できます。 資産タイプまたは資産の場合、さまざまな条件下でエンジンのボリューム、パワー消費量、および最大積載能力の属性を設定できます。

## <a name="create-attribute-types"></a>属性タイプの作成

独自の属性タイプを作成できます。 また、**属性タイプ** ページに製品分析コードを転送できます。

1. **資産管理** \> **設定** \> **属性タイプ**選択します。
2. 属性タイプを初めて設定する場合は、**製品分析コードの作成**を選択し、標準の製品分析コードを自動的に転送します。
3. **新規作成**を選択して、新しい属性タイプを作成します。
4. **属性タイプ** フィールドに、属性タイプの名前を入力します。
5. **説明**フィールドに説明を入力します。
6. **単位**フィールドで、必要に応じて関連する属性単位を選択します。
7. **データ型**フィールドで、単位のデータ型を選択します。
8. データ型として**文字列**を選択した場合は、次の手順に従って属性タイプの値を作成します。

    1. 属性タイプを選択し、**値**を選択します。
    2. **属性値**フィールドで、**新規**を選択します。
    3. **属性タイプ** フィールドで、属性タイプ (分析コード) を選択します。
    4. **値**フィールドで、関連する値を入力します。
    5. **説明**フィールドに説明を入力します。
    6. レコードを保存します。
    7. **属性タイプ** ページに戻ります。

9. レコードを保存します。

    **機能的な場所のタイプ** フィールドには、属性タイプを使用する機能的な場所の数が表示されます。 **資産タイプ** フィールドには、使用する資産タイプの数が表示されます。
