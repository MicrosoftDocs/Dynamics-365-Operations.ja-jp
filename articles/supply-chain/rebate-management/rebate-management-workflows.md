---
title: リベート管理取引のワークフロー
description: このトピックでは、リベート管理の契約ワークフローを設定して、取引を承認および有効化する方法について説明します。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020390"
---
# <a name="rebate-management-deal-workflows"></a>リベート管理取引のワークフロー

[!include [banner](../includes/banner.md)]

リベート契約を承認するには、リベート管理が他の Finance and Operations アプリと同じワークフロー プラットフォームを使用します。 2 つのジョブ プロセスが各ワークフローに関連付けられている。

- ワークフローの 1 つの要素によって取引が有効化された場合、ユーザー プロセスまたはワークフロー プロセスによってトランザクションが承認されます。
- ワークフローの 1 つの要素で取引が承認されます。

リベート契約を使用するには、**リベート管理** モジュールでリベート契約を有効にする必要 があります。 契約を有効にするには、最初に *リベート管理契約ワークフロー* を作成および構成する必要があります。

リベート管理でワークフローが有効になると、ユーザーは取引を手動で承認できません。 ワークフローは常に使用する必要があります。

## <a name="create-and-manage-rebate-management-deal-workflows"></a>リベート管理取引のワークフローの作成と管理

自分のリベート管理契約ワークフローで作業を行うには、**リベート管理 \> 設定 \> リベート管理ワークフロー** に移動します。 そのレポートで、必要に応じてワークフローを表示、作成、更新できます。 一度にこのタイプのワークフロー 1 つのみをアクティブにすることができます。 ワークフローの詳細、**リベート管理ワークフロー** ページの使用方法、ワークフローの作成方法については、[ワークフロー システムの概要](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) および関連トピックを参照してください。

## <a name="use-a-workflow-to-activate-a-deal"></a>ワークフローを使用した取引の有効化

ワークフローを通じて取引を有効にするには、取引を開きます (例えば **すべてのリベート管理契約** ページなど)。 その後、アクション ペインで、**ワークフロー \>提出** を選択します。 ワークフローを通じて新しい取引が処理および承認されると、新しい取引が有効にされ、使用できる状態になります。

取引が有効化された後は、設定を変更できません。 有効な取引を変更する必要がある場合は、無効にしてから、新しい取引を作成します。 新しい取引が古い取引と似ている場合は、古い取引をコピーして作成できます。
