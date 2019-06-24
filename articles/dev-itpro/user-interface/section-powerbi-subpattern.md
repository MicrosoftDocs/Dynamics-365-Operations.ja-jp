---
title: セクション Power BI のサブパターン
description: この記事では、セクション PowerBI サブパターンに関する情報を提供します。 このサブパターンは、PowerBI コントロールを含むパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29431
ms.assetid: 3e760372-e5ee-49d6-b715-c638294345de
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecdb2762e3903eb589f462d26e14e2f22fedd83a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560822"
---
# <a name="section-power-bi-subpattern"></a>セクション Power BI のサブパターン

[!include [banner](../includes/banner.md)]

この記事では、セクション PowerBI サブパターンに関する情報を提供します。 このサブパターンは、PowerBI コントロールを含むパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。

<a name="usage"></a>用途
-----

セクション PowerBI サブパターンは、PowerBI コントロールを含むパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。

## <a name="wireframe"></a>ワイヤーフレーム
[![sectionPowerBIWireframe](./media/sectionpowerbiwireframe.png)](./media/sectionpowerbiwireframe.png)

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a>Microsoft Dynamics AX 用のパターンの変更
このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

TabPage PowerBI (PowerBI)

### <a name="core-components"></a>コア コンポーネント

セクション PowerBI をワークスペース内の適切なタブ ページに適用します。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [運用ワークスペース](workspace-form-pattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
None

## <a name="examples"></a>例
フォーム: **FmClerkWorkspace** (**すべてのワークスペース** &gt; **予約管理**) フォームが表示できる前に、Power BI がコンフィギュレーションされる必要があります。 (PowerBI のコンフィギュレーション方法については、付録を参照してください。)

## <a name="appendix"></a>付録
### <a name="related-articles"></a>関連記事

-   [ワークスペースの PowerBI 統合の構成](../analytics/configure-power-bi-integration.md)
-   [Dynamics AX での Power BI 統合](../analytics/power-bi-integration.md)

### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

-   **ワークスペースとの統合のために PowerBI をどのようにコンフィギュレーションしますか。**
    -   [ワークスペースの PowerBI 統合のコンフィギュレーション](../analytics/configure-power-bi-integration.md)を参照してください。

### <a name="open-issues"></a>未処理の問題

None



