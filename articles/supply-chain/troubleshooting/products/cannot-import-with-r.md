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
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764695"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>リリース済製品 V2 エンティティを使用して品目をインポートできない

KB 番号: 4611825

## <a name="symptoms"></a>現象

*リリース済製品V2* エンティティを使用して品目をインポートしようとする場合は、次のような エラー メッセージが表示されます。

> 品目にレコードを作成することはできません - 分析コード グループを追跡する (ResResGroupingDimensionGroupItem)。 品目番号: 2040663、バッチ。 レコードが既に存在します。

## <a name="resolution"></a>解像度

新しいリリース済製品をインポートするには、*リリースされた製品 V2* エンティティの代わりに、*リリースされた製品作成 V2* エンティティを使用する必要 があります。
