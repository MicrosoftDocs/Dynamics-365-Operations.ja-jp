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
ms.openlocfilehash: bf6eb0eb755de3f2842c235946bfd7ccad04ccf7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474727"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>リリース済製品 V2 エンティティを使用して品目をインポートできない

KB 番号: 4611825

## <a name="symptoms"></a>現象

*リリース済製品V2* エンティティを使用して品目をインポートしようとする場合は、次のような エラー メッセージが表示されます。

> 品目にレコードを作成することはできません - 分析コード グループを追跡する (ResResGroupingDimensionGroupItem)。 品目番号: 2040663、バッチ。 レコードが既に存在します。

## <a name="resolution"></a>解像度

新しいリリース済製品をインポートするには、*リリースされた製品 V2* エンティティの代わりに、*リリースされた製品作成 V2* エンティティを使用する必要 があります。
