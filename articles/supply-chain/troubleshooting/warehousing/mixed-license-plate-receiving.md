---
title: 混合ライセンス プレートの受取は、すべての廃棄コードに対して機能するわけではありません
description: 廃棄コードの アクション フィールドが 貸方 または 仕損 に設定されている場合、返品品目を処理するには、混合ライセンス プレートの受取 メニュー項目のみ使用できます。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476901"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>混合ライセンス プレートの受取は、貸方を除く廃棄コードに対しては機能しません

## <a name="symptoms"></a>現象

廃棄コードの **アクション** フィールドが *貸方* または *仕損* に設定されている場合、返品品目を処理するには、[混合ライセンス プレートの受取](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) メニュー項目のみ使用できます。

## <a name="resolution"></a>解決策

Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。 現在のところ、**アクション** フィールドが *貸方* または *仕損* に設定された[廃棄コード](/dynamics365/supply-chain/service-management/set-up-disposition-codes)のみが、混合ライセンス プレート受取でサポートされています。
