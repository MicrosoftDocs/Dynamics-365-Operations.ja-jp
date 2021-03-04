---
title: 分析コード式ビルダーのサブパターン
description: この記事では、分析コード式ビルダー コントロールを使用するコンテナー コントロールに適用される分析コード式ビルダーのサブパターンについて説明します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29451
ms.assetid: 6ab0f75d-3168-4dfe-b2ce-d17d3861216e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a99bf3c514073d54e61f61ce5c11b978a699fd5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680506"
---
# <a name="dimension-expression-builder-subpattern"></a>分析コード式ビルダーのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、分析コード式ビルダー コントロールを使用するコンテナー コントロールに適用される分析コード式ビルダーのサブパターンについて説明します。  

<a name="usage"></a>用途
-----

分析コード式ビルダー パターンは、分析コード式ビルダー コントロールを使用するグループまたはタブ ページがあるときに使用されます。

## <a name="wireframe"></a>ワイヤーフレーム
[![dimensionExpressionBuilderWireframe](./media/dimensionexpressionbuilderwireframe.png)](./media/dimensionexpressionbuilderwireframe.png)

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

TabPage | Group

*TopFieldGroup (グループ) \[オプション\]* – **注記:** フィールド サブパターンが使用されます。

*DEBGroup (グループ)\[0..N\]*

分析コード式ビルダー

*分析コード式ビルダー \[0..N\]*

### <a name="core-components"></a>コア コンポーネント

-   分析コード式ビルダーのサブパターンを TabPage またはグループ コントロールに適用します。

## <a name="ux-guidelines"></a>UX ガイドライン
None

## <a name="examples"></a>例
フォーム: **BudgetControlConfiguration (RulesDetailsCriteriaFastTabPage)** (**予算作成** &gt; **設定** &gt; **予算管理** &gt; **予算管理コンフィギュレーション**) [![dimensionExpressionBuilderExample](./media/dimensionexpressionbuilderexample.png)](./media/dimensionexpressionbuilderexample.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

None





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]