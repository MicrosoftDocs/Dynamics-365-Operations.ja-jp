---
title: 製造品目の雑費の表示
description: 製造品目の固定費は、工程の段取り時間と、数量または仕損金額が固定されているコンポーネントを反映します。
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: b8fcfc1a9386d05c2adbcb4208e7ef5d01644430
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562256"
---
# <a name="display-charges-for-a-manufactured-item"></a>製造品目の雑費の表示

[!include [banner](../includes/banner.md)]

製造品目の固定費は、工程の段取り時間と、数量または仕損金額が固定されているコンポーネントを反映します。

品目の請求金額の計算された金額は、品目の単位原価で表示できます。 ただし、請求金額は、別個のフィールドとして表示され、品目の単位原価には含まれません。 請求金額が別個のフィールドとして表示されるとき、1 つのフィールドには請求金額の合計金額が表示され、別のフィールドにはその金額の償却に使用される原価ロット サイズが表示されます。 たとえば、品目価格ページには、請求金額が 2 つの別個のフィールドとして表示されます。 ただし、完了ページには品目の単位あたりの合計原価が表示され、償却原価が単位原価に含まれます。

製造品目の請求金額は、常に、標準費目別原価に対する品目の単位原価に含まれます。 必要に応じて、計画費目別原価に含めることもできます。 原価バージョン内のポリシーにより、製造品目の原価に請求金額が含まれます。 品目の原価レコードを有効にすると、品目価格ページに表示されるように、品目の基準原価情報に対する請求金額が更新されます。 ただし、請求金額は、2 つの別個のフィールドとして表示され、品目の単位原価には含まれません。 有効化が異なるサイトを反映するものであっても、有効化のたびに品目の基準原価情報が更新されます。 したがって、基準原価情報を参照情報として表示する必要があります。





