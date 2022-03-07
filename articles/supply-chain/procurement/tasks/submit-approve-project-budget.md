---
title: プロジェクト予算のワークフローの作成と送信
description: この手順ではプロジェクトの予算を作成して送信する方法を示します。
author: Henrikan
ms.date: 11/22/2021
ms.topic: article
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f410d824be717537e6dfb5dbd8b71ff7d992e0a
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860412"
---
# <a name="create-and-submit-a-project-budget-workflow"></a>プロジェクト予算のワークフローの作成と送信

[!include [banner](../../includes/banner.md)]

プロジェクトの予算を作成する際には、プロジェクトの収入とコストの見積もりを入力し、その値を使って実際のプロジェクトの取引を管理することができます。 プロジェクトの予算では、すべてのオリジナル予算と改訂版が、プロジェクトのワークフローを経て承認される必要があります。 このワークフローを使用すると、予算編成に対する管理が強化され、変更履歴の記録が作成されます。 [プロジェクトを作成した](/dynamicsax-2012/appuser-itpro/create-a-project)後、この手順で予算を作成して送信します。

1. **モジュール** > **プロジェクト管理と会計** > **プロジェクト** > **すべてのプロジェクト** に移動します。
1. プロジェクト リストから、プロジェクトを選択します。
1. プロジェクトの詳細ページで、**計画** タブを選択します。
1. **予算** グループで、**プロジェクトの予算** を選択します。
1. **一般** クイックタブで、次の情報を入力します。
   - **説明** ボックスに値を入力します。
   - **オリジナル予算** のオプションを選択します。
   - **残りの予算** のオプションを選択します。
1. **コスト** クイックタブを展開し、 **新規** を選択します。 続いて、以下の設定を行います:
   - **トランザクション タイプ** のオプションを選択します。
   - 適切な **カテゴリ** を選択します。
   - **オリジナル予算** に値を入力します。
1. **収益** クイックタブを展開し、 **新規** を選択します。 続いて、以下の設定を行います:
   - **トランザクション タイプ** のオプションを選択します。
   - **カテゴリ** を選択します。
   - **オリジナル予算** に値を入力します。
1. **保存** を選択します。
1. **ワークフロー \> 送信** を選択します。
1. **オリジナル予算ワークフローのレビュー - 送信** ページで、**コメント** を入力し、**送信** を選択します。
