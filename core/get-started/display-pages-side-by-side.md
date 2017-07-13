---
title: "[新しいウィンドウで開く] アイコンを使用してページを並べて表示します"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations でページを並べて表示する方法を説明します。"
author: aneesmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: aad98247692bdbaf5b8023b393b5e33260dd0b1a
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017


---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>[新しいウィンドウで開く] アイコンを使用してページを並べて表示する

[!include[banner](../includes/banner.md)]


この記事は、Microsoft Dynamics 365 for Finance and Operations でページを並べて表示する方法を説明します。

Microsoft Dynamics 365 for Finance and Operations により、効率的にタスクを実行できます。 場合によっては、タスクをすばやく完了するために複数ページを並べて表示することができます。 たとえば、複数の仕訳帳で明細行を検証または入力することができます。 通常、そのためには、仕訳帳の一覧が表示されたページや特定の仕訳帳の明細行が表示されたページの間を行き来する必要があります。 ただし、[**新しいウィンドウで開く**] 機能は、タスクをすばやく実行できるように、これらのページを並べて表示できます。 引き続き上記の例で考えてみると、明細行を表示した場合には、[**新しいウィンドウで開く**] アイコンをクリックできます。 [![新しいウィンドウで開くアイコン](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) [**新しいウィンドウで開く**] アイコンをクリックすると新しいポップアップ ブラウザーに明細行ページが開き、元のブラウザーは履歴をさかのぼり仕訳帳の一覧が表示されたページに移動します。 その後、両方のページを並べて表示できます。 仕訳帳の表示が終了すると、仕訳帳リスト ページで選択された仕訳帳を変更できます。また、ポップアップ ウィンドウの明細行ページには、新しく選択された仕訳帳の明細行が自動的に表示されます。 [![ページを並べて表示する](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) これらのページをバッキングしているデータ間に存在する関係により、動的リンクと動的更新が発生します。 システムがデータ間の関係を認識しない場合、ポップアップ ウィンドウはそれが生成されたウィンドウでの変更に対して自動的に更新されません。 一部のページには、グリッド ビュー、ヘッダー ビュー、詳細ビューなどの複数のビューがあります。 [**新しいウィンドウで開く**] アイコンにより、ページ全体を新しいブラウザー ウィンドウで開くことができます。 したがって、[**新しいウィンドウで開く**] 機能では、同じページの 2 つのビューを並べて表示することはできません。 ただし、このようなページのほとんどすべてには、レコードの切り替えや同様の操作を達成するために使用できるナビゲーション リストがあります。 [**新しいウィンドウで開く**] 機能を使用する前に、ブラウザーのポップアップ ブロッカーをコンフィギュレーションして、Dynamics 365 for Finance and Operations サイトの URL からのポップアップを許可する必要があります。 たとえば、「\*.dynamics.com」からのポップアップを許可することができます。 [**新しいウィンドウで開く**] 機能は、ウィンドウで 1 つ以上のページが開いている場合にのみ使用できます。 また、ポップアップ ウィンドウは、開いているページがなくなると (つまり、そのウィンドウで最後のページが閉じると) 自動的に閉じます。 アプリケーションの別の領域に移動すると、Finance and Operations も開いているページを閉じます。 したがって、ポップアップ ウィンドウが開いているときに、アプリケーションで別の領域に移動すると、システムがそれらのウィンドウ内のページを閉じるので、ポップアップ ウィンドウは自動的に閉じます。 ポップアップ ウィンドウの上部バーは読み取り専用で、その中にページが開かれ、会社に関する情報が表示されます。 また、ポップアップ ウィンドウは、メインの Finance and Operations ブラウザー ウィンドウに依存します。 メイン ウィンドウが閉じるか、または更新されると、開いているすべてのポップアップ ウィンドウは、読み取り専用になります。 これは、これらのウィンドウに情報を表示することはできますが、その情報とやり取りができないことを示します。




