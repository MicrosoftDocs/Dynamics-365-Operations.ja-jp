---
title: 仕入先の検索
description: 特定の基準に基づく仕入先の検索方法を習得します。
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dda8cfa55809ebeeda695d02ed5f99e493325c3b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207587"
---
# <a name="search-for-vendors"></a>仕入先の検索

[!include [banner](../../includes/banner.md)]

特定の基準に基づく仕入先の検索方法を習得します。 この例では、特定の調達カテゴリに対して承認されていて、特定の国に基本住所をもっている仕入先の検索方法を示します。 この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。 通常、このタスクを実行するのは、調達担当者です。

1. [調達] > [仕入先] > [仕入先の検索]の順に移動します。
2. [調達カテゴリの選択] ページを開くには、プラス アイコンをクリックします。  
3. ツリーで、「CORP PROCUREMENT CATEGORIES\OFFICE MACHINES」を選択します。
    * タスク ガイドのこの手順を実行している場合は、正しいノードを選択する前に、[ロック解除] ボタンのクリックが必要となる場合があります。 USMF を使用していない場合は、カテゴリから 1 つを選択します。  
4. [追加] をクリックします。
    * 複数のカテゴリをここで選択することができます。 これを行う場合は、検索では、少なくとも 1 つのカテゴリに対して承認されている仕入先をすべて探します。  
5. [OK] をクリックします。
6. [国/地域] フィールドに値を入力します。
7. [OK] をクリックします。

