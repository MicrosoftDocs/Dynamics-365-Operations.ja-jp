---
title: "マスタ プランとマルチサイト機能"
description: "マスター プランでは、サイトと倉庫の在庫分析コードの設定が考慮されます。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19eeee753c15cf2670948ce2c615a112813c16ad
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-and-multisite-functionality"></a>マスタ プランとマルチサイト機能

マスター プランでは、サイトと倉庫の在庫分析コードの設定が考慮されます。 

サイト分析コードは必須になり、倉庫分析コードを必須に設定できます。

分析コードが必須の場合は、分析コード値をすべての在庫トランザクションに入力する必要があります。 このため、マスター プラン時には、初期需要があるサイトと倉庫は明らかになっています。 また、サイト分析コードは、下位レベルの補充展開時にサイト値が変わらないように一貫しています。

倉庫が必須に設定されていない場合は、初期需要が不明である可能性があります。 計画エンジンは、品目、各倉庫、および注文明細の詳細に対して定義されている設定に基づいて、使用する倉庫を決定する必要があります。

Wiki の記事では、使用する倉庫を決定するために計画エンジンを使用する方法について、定義されている各種の設定ごとに説明します。

[マスター プラン - サイトと倉庫の補充、倉庫は必須](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[マスター プラン - サイトの補充、倉庫は必須](master-plan-site-coverage-warehouse-mandatory.md)

[マスター プラン - サイトと倉庫の補充、倉庫は必須ではない](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[マスター プラン - サイトの補充、倉庫は必須ではない](master-plan-site-coverage-warehouse-not-mandatory.md)

[マスター プラン - BOM バージョンを決定する方法](master-plan-bom-version-determined.md)


