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
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740554"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>ピッキング リスト仕訳帳の倉庫が BOM 明細行で更新されない

KB 番号: 4614848

## <a name="symptoms"></a>現象

ピッキング リスト仕訳帳の倉庫が部品表 (BOM) 明細行で更新されません。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。 生産 BOM 明細行への参照がある (ロット ID を介して) ピッキング リスト仕訳帳の明細行が作成された場合、生産ピッキング リスト仕訳帳明細行の倉庫分析コードが後で変更されても、生産 BOM 明細行の倉庫は更新されません。
