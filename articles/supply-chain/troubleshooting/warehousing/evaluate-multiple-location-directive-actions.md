---
title: 複数 SKU の場所ディレクティブのすべてのアクションを評価する
description: 新しい機能が追加され、複数の SKU の場所ディレクティブのすべてのアクションを評価することができます。 このページでは、有効にする方法について情報が表示されます。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea265166902f85c2c09cae08ee6de5cd7094e1b4
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778405"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>複数の SKU オプションでは、複数の場所ディレクティブ アクションを評価しない

## <a name="symptoms"></a>現象

**複数 SKU** オプションが選択されているときは、*販売注文* 作業指示タイプおよび *プット* 作業タイプの場所ディレクティブにより、複数の場所ディレクティブ アクションが評価されることはありません。 最初の場所ディレクティブ アクションのみが評価されます。

## <a name="resolution"></a>解決策

バージョン 10.0.15 では、新しい機能 *複数の SKU の場所ディレクティブのすべてのアクションを評価する* が追加されています ([KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091) を参照)。 この機能は、複数 SKU の場所ディレクティブのすべてのアクションを評価します。 Supply Chain Management のバージョン 10.0.21 では、この機能は既定で有効になっています。 管理者は、[機能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ページで機能状態を確認し、必要に応じて有効化または無効化することができます。
