---
title: BOM バージョンの決定
description: 需要の展開中に、品目の既定のオーダー タイプが生産になっている場合、計画エンジンはサイトに基づいて有効な BOM バージョンを探します。
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370091eed4ee050031d5d135aa7b1d8d0fe82491
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570972"
---
# <a name="determine-the-bom-version"></a>BOM バージョンの決定

[!include [banner](../includes/banner.md)]

需要の展開中に、品目の既定のオーダー タイプが生産になっている場合、計画エンジンはサイトに基づいて有効な BOM バージョンを探します。 

サイト分析コードは常に既知で、需要トランザクションに記述されています。 使用する BOM バージョンを決定するには、次のプロセスを使用します。

-   品目の BOM バージョンが需要サイトで定義されている場合は、このサイト固有の BOM が使用されます。
-   品目のサイト固有の BOM バージョンが需要サイトで定義されていない場合は、汎用 BOM が使用されます。 汎用 BOM はサイト固有ではなく、複数のサイトに対して有効です。 汎用 BOM がある場合は、その BOM が使用されます。
-   使用できる汎用 BOM のバージョンがない場合、需要の展開はここで停止します。

サイト固有の BOM であるか、または汎用 BOM であるかにかかわらず、有効な BOM バージョンは、必要な日付と数量の基準を満たす必要があります。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]