---
title: 統合されたサイトおよび倉庫
description: このトピックでは、Finance and Operations と Dataverse 間のサイトおよび倉庫データの統合について説明します。
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750669"
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