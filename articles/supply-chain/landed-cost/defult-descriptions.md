---
title: 一般会計の既定の説明
description: 既定の説明を使用して、一般会計への伝票の転記の説明フィールドを更新できます。
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f95dff3a77a552d5788d813b3d13dc30579be715
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695710"
---
# <a name="default-descriptions-for-the-general-ledger"></a>一般会計の既定の説明

[!include [banner](../../includes/banner.md)]

既定の説明を使用して、一般会計への伝票の転記の **説明** フィールドを更新できます。 この機能は、陸揚原価に関して強化されました。

元帳転記の既定の説明を設定するには、**組織管理 \> 設定 \> 既定の説明** に移動します。

次の表に、陸揚原価をサポートするために **既定の説明** ページの **説明** フィールドに追加された新しい値を示します。

| 説明タイプ | 摘要 |
|---|---|
| 輸入原価計算 - 原価の見越し計上 | 発注請求書を転記すると、原価の見越計上が処理され、航海コストの見積もりを行います。 既定の説明を指定して、航海番号を説明に追加できます。 出荷番号に *%4* を使用します。 |
| 輸入原価計算 – 輸送中の商品注文 | 輸送中処理を使用している場合は、発注請求書が転記され、商品が輸送中の商品勘定に転記されます。 既定の説明を指定して、輸送中の注文番号を説明に追加できます。 輸送中の注文番号に *%4* を使用します。 |
| 在庫 – 原価計算済 – 調整 | 買掛金勘定 (AP) 請求書が航海コストとして処理される場合は、在庫調整を処理してその航海コストを見積もる必要があります。 既定の説明を指定して、航海番号を説明に追加できます。 出荷番号に *%4* を使用します。 |

**既定の説明** ページの使用方法の詳細については、[自動転記の既定の説明の設定](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md) を参照してください。
