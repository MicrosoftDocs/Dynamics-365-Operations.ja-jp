---
title: 高度な選択のフォーム パターン
description: この記事では、高度な選択のフォーム パターンに関する情報を提供します。これにより、ユーザーが大規模で広範なリストから品目をフィルタ処理して選択できます。
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29171
ms.assetid: c3c5eea7-f771-41ea-9976-8d0e1f3d3f25
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5486be8a695536dc782194f106ba119922943d8c845823a3742f824e1e5c78fa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741628"
---
# <a name="advanced-selection-form-pattern"></a>高度な選択のフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、高度な選択フォーム パターンに関する情報を提供します。 このダイアログ フォーム パターンを使用すると、ユーザーは大規模な全体のリストから項目をフィルターして選択できます。 リスト パネルのパターンと同様に、このパターンは主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。

## <a name="usage"></a>用途

高度な選択フォーム パターンは、主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。 このタスクは、通常、複数選択リストによって達成されます。 ただし、多くのシナリオでは、ユーザーは連続していない品目を選択する必要があり、同時に、選択する品目の一覧を表示する必要があります。 このパターンは、ユーザーが 1 つのリスト内の項目を選択して別のリストに追加する点において、リスト パネルのパターンと似ています。 ただし、このパターンにはカスタム フィルターおよび上部の「広い」リストがあり、およびページの画面「不動産」のほとんどを使用します (通常、大きなダイアログ)。 大規模かつ広範囲のリストでフィルター処理および選択しなければならない場合にこのパターンを使用します。

## <a name="wireframe"></a>ワイヤーフレーム

[![高度な選択パターン ワイヤーフレーム。](./media/advancedselection1.png)](./media/advancedselection1.png)

### <a name="related-patterns"></a>関連するパターン

-   [リスト パネルのサブパターン](list-panel-subpattern.md)
-   [ダイアログのフォーム パターン](dialog-form-pattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **標準フォーム ガイドライン:**
    -   標準フォーム ガイドラインは、[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   **高度な選択のガイドライン:**
    -   既定では、クイック フィルターは名前または説明列を使用する必要があります。
    -   リストには最大 15 の列を表示できます。 **注記:** このガイドラインは Microsoft Dynamics AX 2012 から緩和されています。
    -   主な指示は、ユーザーに何をする必要があるかを指示する必要があります。
    -   データが存在しないとき、グリッドは新しいレコードを自動的に追加できません。

## <a name="example"></a>例
フォーム: **ProcCategoryAddVendor** (**調達** &gt; **調達カテゴリ** をクリックします。 **仕入先** クイック タブで、**追加** をクリックします)。 

> [注記] ごのフォームでは、このパターンが利用できません。ここで表示している画像では、一般的な拡張選択フォームパターンの例を示しています。

[![高度な選択の例。](./media/advancedselectionexample.png)](./media/advancedselectionexample.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]