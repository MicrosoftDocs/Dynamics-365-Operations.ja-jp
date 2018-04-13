---
title: "BOM バージョンの決定"
description: "需要の展開中に、品目の既定のオーダー タイプが生産になっている場合、計画エンジンはサイトに基づいて有効な BOM バージョンを探します。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e6745a52138e545b557fa1aa286cd49481b2ecd
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="determine-the-bom-version"></a>BOM バージョンの決定

[!INCLUDE [banner](../includes/banner.md)]

需要の展開中に、品目の既定のオーダー タイプが生産になっている場合、計画エンジンはサイトに基づいて有効な BOM バージョンを探します。 

サイト分析コードは常に既知で、需要トランザクションに記述されています。 使用する BOM バージョンを決定するには、次のプロセスを使用します。

-   品目の BOM バージョンが需要サイトで定義されている場合は、このサイト固有の BOM が使用されます。
-   品目のサイト固有の BOM バージョンが需要サイトで定義されていない場合は、汎用 BOM が使用されます。 汎用 BOM はサイト固有ではなく、複数のサイトに対して有効です。 汎用 BOM がある場合は、その BOM が使用されます。
-   使用できる汎用 BOM のバージョンがない場合、需要の展開はここで停止します。

サイト固有の BOM であるか、または汎用 BOM であるかにかかわらず、有効な BOM バージョンは、必要な日付と数量の基準を満たす必要があります。






