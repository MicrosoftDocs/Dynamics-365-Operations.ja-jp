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
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476859"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>複数の SKU オプションでは、複数の場所ディレクティブ アクションを評価しない

## <a name="symptoms"></a>現象

**複数 SKU** オプションが選択されているときは、*販売注文* 作業指示タイプおよび *プット* 作業タイプの場所ディレクティブにより、複数の場所ディレクティブ アクションが評価されることはありません。 最初の場所ディレクティブ アクションのみが評価されます。

## <a name="resolution"></a>解決策

バージョン 10.0.15 では、新しい機能 *複数の SKU の場所ディレクティブのすべてのアクションを評価する* が追加されています ([KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091) を参照)。 この機能は、複数 SKU の場所ディレクティブのすべてのアクションを評価します。 この機能が必要な場合は、[機能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)を使用してオンにします。
