---
title: ピッキング リスト仕訳帳の倉庫が BOM 明細行で更新されません。
description: ピッキング リスト仕訳帳の倉庫が部品表 (BOM) 明細行で更新されません。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026668"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>ピッキング リスト仕訳帳の倉庫が BOM 明細行で更新されない

KB 番号: 4614848

## <a name="symptoms"></a>現象

ピッキング リスト仕訳帳の倉庫が部品表 (BOM) 明細行で更新されません。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。 生産 BOM 明細行への参照がある (ロット ID を介して) ピッキング リスト仕訳帳の明細行が作成された場合、生産ピッキング リスト仕訳帳明細行の倉庫分析コードが後で変更されても、生産 BOM 明細行の倉庫は更新されません。
