---
title: ワークスペース ページ フィルター グループのサブパターン
description: この記事では、ワークスペース ページ フィルター グループのサブパターンについて説明します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 29231
ms.assetid: 90d5a70b-a99b-4e79-a52d-b4ef5a942607
ms.openlocfilehash: 5506761635579a764dc3065f3e6116c55921a77d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275960"
---
# <a name="workspace-page-filter-group-subpattern"></a>ワークスペース ページ フィルター グループのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、ワークスペース ページ フィルター グループのサブパターンについて説明します。 このサブパターンは、ワークスペースがフォーム上で 1 つのワークスペース全体にかかわるフィルターを公開する必要があるとき、運用ワークスペース パターンの一部として使用されます。

## <a name="usage"></a>用途

ワークスペース ページ フィルター グループのサブパターンは、特にワークスペースがフォーム上で 1 つのワークスペース全体にかかわるフィルターを公開する必要があるときに、運用ワークスペース パターンの一部として使用されます。

## <a name="wireframe"></a>ワイヤーフレーム

[![ワークスペース ページ フィルター グループのサブパターンのワイヤーフレーム。](./media/workspacepagefiltergroupwireframe.png)](./media/workspacepagefiltergroupwireframe.png)

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a>Microsoft Dynamics AX 用のパターンの変更
このパターンは、Microsoft Dynamics AX 2012 には存在しませんでした。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- グループ化

    - フィールド ($Field)

### <a name="core-components"></a>コア コンポーネント

ワークスペース ページ フィルター グループを (運用) ワークスペースの適切なグループに適用します。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [カスタム フィルター グループ](custom-filter-group-subpattern.md)
-   [運用ワークスペース](workspace-form-pattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   フィルター フィールドには、使用可能な値のリストを含むドロップダウンが必要です。
-   フィルター フィールドは、ターゲット ユーザーによって 1 日に複数回変更される予定です。 フィルター フィールドがより頻度が少ない回数で変更される場合、または主に静的である場合は、構成ダイアログ ボックスに配置する必要があります。
-   さらにフィルター フィールドが必要な場合は、コンフィギュレーション ダイアログ (最大で5つのフィルター フィールド) に配置する必要があります。

## <a name="examples"></a>例
フォーム: **ReqCreatePlanWorkspace** (**すべてのワークスペース** &gt; **マスター プラン**) 

[![ワークスペース ページ フィルター グループの例。](./media/workspacepagefiltergroupexample.png)](./media/workspacepagefiltergroupexample.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

None


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
