---
title: WMS へのアップグレードまたは移行時の証明書パスに関するエラー
description: WMS へのアップグレードまたは移行時に、アプリケーションで "証明書パスのトラスト アンカーが見つかりません" というエラーが表示される場合、このページで問題を修正する方法に関する情報が表示されます。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476850"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>WMS へのアップグレードおよび移行時に証明書パスのトラスト アンカーが見つからない

## <a name="symptoms"></a>現象

高度な倉庫管理 (WMS) へのアップグレードおよび移行時に、Warehouse Management アプリで次のエラー メッセージが表示される場合があります。

> java.security.cert.certPathValidatorException: 証明書パスのトラスト アンカーが見つかりません。

## <a name="cause"></a>原因

これは、オンプレミス環境の Android 8+ 上では、自己署名証明書が信頼されないため発生します。

## <a name="resolution"></a>解決策

外部 (パブリック) 証明機関 (CA) を使用します。 この問題の修正プログラムは、Warehouse Management アプリのバージョン 1.9.0.0 で入手できます。 この問題と修正方法の詳細については、[アプリケーション接続の設定時に証明書パスのトラスト アンカーが見つからない](certification-path-app-connection-error.md) を参照してください。
