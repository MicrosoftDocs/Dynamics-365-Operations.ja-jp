---
title: 複数の品質指示が作成された場合に [最終テスト日] フィールドが更新されない
description: 複数の品質指示が作成された場合に [最終テスト日] フィールドが更新されていません。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742031"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>複数の品質指示が作成された場合に [最終テスト日] フィールドが更新されない

KB 番号: 4612803

## <a name="symptoms"></a>現象

複数の品質指示が作成された場合に **最終テスト日** フィールドが更新されていません。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。 最終テスト日は、品質指示に関連していません。 完成品が最初に購入または製造された日付が保存されます。 この日付は、有効期限通知日の計算に使用されます。
