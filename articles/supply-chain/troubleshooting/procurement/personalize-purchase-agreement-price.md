---
title: 購買契約ページに価格単位フィールドを追加できない
description: 行ビュー モードで "購買契約ページ" を開くと、明細行の概要に "価格単位フィールド" を追加してページをカスタマイズできません
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 56d2ce94fb4b74d982cb6a052cca71c18190cd04
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476848"
---
# <a name="you-cant-add-the-price-unit-field-to-the-purchase-agreement-page"></a>購買契約ページに価格単位フィールドを追加できない

## <a name="symptoms"></a>現象

行ビュー モードで **購買契約** ページを開くと、明細行の概要に **価格単位フィールド** を追加してページをカスタマイズできません。

## <a name="resolution"></a>解決策

契約フレームワーク内の一部の共有フィールドは、個人用設定に含めることはできません。 この制限は、実装されるデータ モデルが原因で発生します。 したがって、**価格単位** フィールドをカスタマイズすることはできません。
