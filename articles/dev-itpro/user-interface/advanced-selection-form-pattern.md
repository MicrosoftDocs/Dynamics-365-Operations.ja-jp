---
title: 高度な選択のフォーム パターン
description: この記事では、高度な選択フォーム パターンに関する情報を提供します。 このダイアログ フォーム パターンを使用すると、ユーザーは大規模な全体のリストから項目をフィルターして選択できます。 リスト パネルのパターンと同様に、このパターンは主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。
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
ms.custom: 29171
ms.assetid: c3c5eea7-f771-41ea-9976-8d0e1f3d3f25
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b590d39f9ae26a278bd2dfd976bdf915d24040
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537288"
---
# <a name="advanced-selection-form-pattern"></a>高度な選択のフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、高度な選択フォーム パターンに関する情報を提供します。 このダイアログ フォーム パターンを使用すると、ユーザーは大規模な全体のリストから項目をフィルターして選択できます。 リスト パネルのパターンと同様に、このパターンは主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。

<a name="usage"></a>用途
-----

高度な選択フォーム パターンは、主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。 このタスクは、通常、複数選択リストによって達成されます。 ただし、多くのシナリオでは、ユーザーは連続していない品目を選択する必要があり、同時に、選択する品目の一覧を表示する必要があります。 このパターンは、ユーザーが 1 つのリスト内の項目を選択して別のリストに追加する点において、リスト パネルのパターンと似ています。 ただし、このパターンにはカスタム フィルターおよび上部の「広い」リストがあり、およびページの画面「不動産」のほとんどを使用します (通常、大きなダイアログ)。 大規模かつ広範囲のリストでフィルター処理および選択しなければならない場合にこのパターンを使用します。

## <a name="wireframe"></a>ワイヤーフレーム

[![高度な選択パターン ワイヤーフレーム](./media/advancedselection1.png)](./media/advancedselection1.png)

### <a name="related-patterns"></a>関連するパターン

-   [リスト パネル](list-panel-subpattern.md)
-   [ダイアログ](dialog-form-pattern.md)

## <a name="pattern-changes"></a>パターンの変更
これは、Finance and Operations における新しいパターンです。

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **標準フォーム ガイドライン:**
    -   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   **高度な選択のガイドライン:**
    -   既定では、クイック フィルターは名前または説明列を使用する必要があります。
    -   リストには最大 15 の列を表示できます。 **注記:** このガイドラインは Microsoft Dynamics AX 2012 から緩和されています。
    -   主な指示は、ユーザーに何をする必要があるかを指示する必要があります。
    -   データが存在しないとき、グリッドは新しいレコードを自動的に追加できません。

## <a name="example"></a>例
フォーム: **ProcCategoryAddVendor** (**調達** &gt; **調達カテゴリ**をクリックします。 **仕入先**クイック タブで、**追加**をクリックします)。 

[![advancedSelectionExample](./media/advancedselectionexample.png)](./media/advancedselectionexample.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

この時点ではなし



