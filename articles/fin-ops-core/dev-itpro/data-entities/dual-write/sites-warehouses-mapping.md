---
title: 統合されたサイトおよび倉庫
description: このトピックでは、Finance and Operations と Dataverse 間のサイトおよび倉庫データの統合について説明します。
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
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679323"
---
# <a name="integrated-sites-and-warehouses"></a>統合されたサイトおよび倉庫

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



このトピックでは、Finance and Operations と Dataverse 間のサイトおよび倉庫データの統合について説明します。 運営サイトおよび倉庫は、Supply Chain Management における共通の概念です。 これらは会社のサプライ チェーンをモデル化するために使用されます。

## <a name="templates"></a>テンプレート

Dataverse との統合により、これらの概念とすべての関連情報は、次の表のサイトおよび倉庫データ テーブルを使用する Dataverse で使用可能です。

Finance and Operations アプリ | その他の Dynamics 365 アプリ | 説明
--------------------------|---------------------------|---
サイト | msdyn_operationalsites | 
倉庫 | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]