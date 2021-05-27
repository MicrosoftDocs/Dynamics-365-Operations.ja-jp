---
title: リリース済製品 V2 エンティティを使用して品目をインポートできない
description: リリース済製品 V2 エンティティを使用して品目をインポートできません。
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026669"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>リリース済製品 V2 エンティティを使用して品目をインポートできない

KB 番号: 4611825

## <a name="symptoms"></a>現象

*リリース済製品V2* エンティティを使用して品目をインポートしようとする場合は、次のような エラー メッセージが表示されます。

> 品目にレコードを作成することはできません - 分析コード グループを追跡する (ResResGroupingDimensionGroupItem)。 品目番号: 2040663、バッチ。 レコードが既に存在します。

## <a name="resolution"></a>解像度

新しいリリース済製品をインポートするには、*リリースされた製品 V2* エンティティの代わりに、*リリースされた製品作成 V2* エンティティを使用する必要 があります。
