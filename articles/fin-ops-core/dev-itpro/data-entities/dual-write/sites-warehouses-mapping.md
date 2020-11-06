---
title: 統合されたサイトおよび倉庫
description: このトピックでは、Finance and Operations と Common Data Service 間のサイトおよび倉庫データの統合について説明します。
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d5c2030160f6025c9de63b2c29215364f5f87e6f
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997627"
---
# <a name="integrated-sites-and-warehouses"></a>統合されたサイトおよび倉庫

[!include [banner](../../includes/banner.md)]



このトピックでは、Finance and Operations と Common Data Service 間のサイトおよび倉庫データの統合について説明します。 運営サイトおよび倉庫は、Supply Chain Management における共通の概念です。 これらは会社のサプライ チェーンをモデル化するために使用されます。

## <a name="templates"></a>テンプレート

Common Data Service との統合により、これらの概念とすべての関連情報は、次の表のサイトおよび倉庫データ エンティティを使用する Common Data Service で使用可能です。

Finance and Operations アプリ | その他の Dynamics 365 アプリ | 説明
--------------------------|---------------------------|---
サイト | msdyn_operationalsites | 
倉庫 | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

