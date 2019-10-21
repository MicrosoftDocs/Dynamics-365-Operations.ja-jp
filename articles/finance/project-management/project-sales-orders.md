---
title: プロジェクト販売注文
description: このトピックでは、時間/実費払いプロジェクトに対するプロジェクト ベースの販売注文を作成する方法について説明します。
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185500"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>時間/実費払いプロジェクトに対するプロジェクト販売注文

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

このトピックでは、プロジェクトの販売注文を作成する方法について説明します。 販売注文は、タイプが**時間/実費払い**のプロジェクトに対してのみ作成できます。

時間/実費払いプロジェクトがプロジェクト契約に複数の資金調達元がある場合、**プロジェクト管理および会計パラメーター**ページの**複数の資金調達元があるプロジェクトの販売注文を許可する**パラメーターを有効にする必要があります。 

> [!NOTE]
> - 複数の資金調達元があるプロジェクト販売注文のサポートは、アプリケーション リリース 10.0.2 以降で利用可能です。
> - 複数の資金調達先があるプロジェクト販売注文のサポートを有効にするためのパラメーターは 2020 年 4 月リリース ウェーブで削除されます。その後、機能は常に有効になります。

プロジェクト ベースの販売注文は 2 通りの方法で作成できます。

- プロジェクト自体に移動します。 アクション ウィンドウで、**管理 > 品目作業 > 販売注文**を選択します。 プロジェクト情報は、既定でプロジェクトから販売注文になります。 プロジェクト契約に複数の資金調達元がある場合は、販売注文の顧客を設定する資金調達元を選択する必要があります。 プロジェクトに 1つだけ資金調達元がある場合、顧客は自動的に設定されます。
- **すべての販売注文**リスト ページに移動し、新しい販売注文を作成します。 販売注文のプロジェクトを選択する必要があります。 プロジェクトを選択すると、顧客が資金調達元から設定されます。またはプロジェクト契約に複数の資金調達元がある場合は、資金調達元を選択する必要があります。

