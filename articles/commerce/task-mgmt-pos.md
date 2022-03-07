---
title: POS でのタスク管理
description: このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) アプリケーションにおけるタスク管理について説明します。
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3fb7d584b634b0a1e43ef6a02a9edcadc0927b36bd2a814fdfe947fb0e2e1917
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772109"
---
# <a name="task-management-in-pos"></a>POS でのタスク管理

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) アプリケーションにおけるタスク管理について説明します。

Dynamics 365 Commerce POS アプリケーションにはタスク管理機能があり、店舗の管理者および作業者がタスクを管理したり、タスクの状態を更新したりすることができます。 店舗の作業者は、POS ホームページの **タスク** タイルを選択するか、またはタスクの通知を選択することにより、タスクにアクセスすることができます。 既定では、店舗の作業者は **自分のタスク** タブに移動し、割り当てられているタスクを確認できます。 ただし、**期限超過のタスク**、**タスクを開く**、および **タスク リスト** タブに簡単に切り替えることができます。

## <a name="task-operations-for-store-managers"></a>店舗マネージャーのタスク操作

店舗のマネージャーは、コマンド バーのボタンを使用して、POS アプリケーションで次のタスク操作を実行できます。

- **割り当て** – 選択したタスクを店舗の作業者に割り当てます。
- **タスクの状態** – 選択したタスクの状態を変更します。
- **フィルター** – 既定では、有効なタスクのみが表示されます。 ただし、フィルターを適用することにより、マネージャーは完了またはキャンセルしたタスクを含め、すべてのタスクを表示できます。
- **新しいタスク** – 既存のタスク リストの下にタスクを作成するか、または単一目的のタスクを作成します。

店舗の作業者は、コマンド バーのボタンを使用して、POS アプリケーションで次のタスク操作を実行できます。

- **タスクの状態** – 選択したタスクの状態を変更します。
- **フィルター** – 既定では、有効なタスクのみが表示されます。 ただし、フィルターを適用することにより、作業者は完了またはキャンセルしたタスクを含め、すべてのタスクを表示できます。

次の図は、Commerce POS アプリケーションの **自分のタスク** タブを示しています。

![Commerce POS アプリケーションの自分のタスク タブ。](media/POS-task-management.png)

次の図は、**タスク リスト** タブを示しています。

![Commerce POS アプリケーションのタスク リスト タブ。](media/POS-task-lists-management.png)

## <a name="additional-resources"></a>追加リソース

[タスク管理の概要](task-mgmt-overview.md)

[タスク管理のコンフィギュレーション](task-mgmt-configure.md)

[タスク リストの作成およびタスクの追加](task-mgmt-create-lists.md)

[店舗または従業員へのタスク リストの割り当て](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
