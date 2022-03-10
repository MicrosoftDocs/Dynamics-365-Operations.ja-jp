---
title: 分析コード エントリ コントロールのサブパターン
description: この記事では、分析コード エントリ コントロールのサブパターンについて説明します。
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 15951
ms.assetid: 6baee22e-2a86-428c-b9e2-178581c57830
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d255c50e9249d80aa976debbdb79b2a652dad71
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782901"
---
# <a name="dimension-entry-control-subpattern"></a>分析コード エントリ コントロールのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、分析コード エントリ コントロールのサブパターンについて説明します。 このサブパターンは、分析コード エントリ コントロール (DEC) を使用するグループまたはタブ ページがあるときに使用されます。 

## <a name="usage"></a>用途

分析コード エントリ コントロール パターンは、分析コード エントリ コントロール (DEC) を使用するグループまたはタブ ページがあるときに使用されます。

## <a name="wireframe"></a>ワイヤーフレーム

![分析コード エントリ コントロールのサブパターンのワイヤーフレーム。](media/decwireframe.png)

## <a name="model"></a>モデル

### <a name="high-level-structure"></a>高レベル構造体

TabPage | Group *TopFieldGroup (グループ) \[オプション\]* – **注:** フィールド サブパターンが使用されます。

*DECGroup (グループ) \[0..N\]* 分析コード エントリ コントロール *分析コード エントリ コントロール \[0..N\]* *BottomFieldGroup (グループ) \[オプション\]* – **注記:** フィールド サブパターンが使用されます。

### <a name="core-components"></a>コア コンポーネント

- 分析コード エントリ コントロールのサブパターンを TabPage コントロールに適用します。

## <a name="ux-guidelines"></a>UX ガイドライン

なし。

## <a name="examples"></a>例

フォーム: **CustTable (TabFinancialDimensions)**

![TabFinancialDimensions を使用した CustTable の例。](media/decexample.png)

## <a name="appendix"></a>付録

### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

なし。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]