---
title: 在庫仕訳帳の "ワークフロー" ドロップダウン ダイアログ ボックスが見つかりません
description: 仕訳帳ページには「ワークフロー」ドロップダウン ダイアログ ボックスが表示されないか、関連するワークフロー操作を選択できません
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476858"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>在庫仕訳帳の "ワークフロー" ドロップダウン ダイアログ ボックスが見つかりません

## <a name="symptoms"></a>現象

仕訳帳ページには **ワークフロー** ドロップダウン ダイアログ ボックスが表示されないか、関連するワークフロー操作を選択できません。

この問題は、次のセクションで説明するように、3 つの理由で発生する可能性があります。

## <a name="resolution-1"></a>解決策 1

すべてのユーザーに問題が適用される場合は、承認ワークフローが仕訳帳名に割り当てられていないため、問題が発生している可能性があります。 問題を解決するには、次の手順に従います。

1. **在庫管理 &gt; 設定 &gt; 仕訳帳名 &gt; 在庫** に移動します。
1. リスト ペイン列から仕訳帳名を選択して、設定ページを開きます。
1. **一般** クイック タブで、**承認ワークフロー** オプションを *はい* に設定します。 変更の確認を求められたら、**はい** を選択します。
1. **ワークフロー** フィールドで、選択した仕訳帳名にに使用するワークフローを選択します。

## <a name="resolution-2"></a>解決策 2

ワークフローでカスタマイズされたコードを使用している場合、システムをアップグレードすると問題が発生することがあります。 たとえば、仕訳帳ワークフローで **送信** ボタンはグレー表示され、送信を承認するために選択できない場合があります。

**送信** ボタンがグレー表示されている場合、ワークフローはカスタマイズされている場合があります (つまり、ワークフローの方法。`FormDataUtil` の `canSubmitToWorkflow()` は拡張されています)。 この問題を修正するには、次の例で構造を使用する `canSubmitToWorkflow()` の方法を拡張する方法を変更します。

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>解決策 3

特定のユーザーにのみ問題が適用される場合、そのユーザーには、在庫仕訳帳に対するワークフロー操作の実行に必要なセキュリティ特権が付与されていない可能性があります。 影響を受ける各ユーザーに *在庫仕訳帳ワークフロー の維持* のセキュリティ特権が付与されているかを確認します。 既定では、この特権は同じ名前の関税に割り当てされ、その関税は *倉庫作業者* と *倉庫マネージャ* のロールに適用されます。
