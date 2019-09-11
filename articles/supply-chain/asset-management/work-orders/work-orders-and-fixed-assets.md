---
title: 作業指示書と固定資産
description: このトピックでは、資産管理における固定資産と作業指示書について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875750"
---
# <a name="work-orders-and-fixed-assets"></a>作業指示書と固定資産


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


資産管理では、資産を固定資産に関連付けることができます。またこれらの資産の作業指示書を作成することもできます。 この機能を使用する場合、**プロジェクト管理および会計**モジュールと Dynamics 365 for Finance and Operations の**固定資産**モジュールで、固定資産、関連する投資プロジェクトおよび投資プロジェクトに登録されている原価の概要を完全に取得できます。

>[!NOTE]
>**固定資産番号**フィールドは、作業指示書ジョブ プロジェクトでプロジェクト タイプとして "投資" タイプが選択されている場合にのみ、作業指示書ジョブ プロジェクトに入力されます。

![図 1](media/24-work-orders.png)

次の手順では、資産、作業指示書、作業指示書プロジェクト、および固定資産関連について説明します。

1. 下の図が示すように、固定資産に関連付ける資産を作成します。

![図 2](media/25-work-orders.png)

2. 作業指示書タイプ (**資産管理** > **設定** > **作業指示書** > **作業指示書タイプ**) を設定する場合は、投資を処理するための作業指示書タイプを作成します。 [作業指示書タイプ](../setup-for-work-orders/work-order-types.md) も参照してください。

![図 3](media/26-work-orders.png)

3. 作業指示書プロジェクト グループ (**資産管理** > **設定** > **作業指示書** > **プロジェクト設定** > **プロジェクト グループ** リンク) を設定する場合は、投資のために使用される作業指示書と**プロジェクト管理および会計**モジュール (**プロジェクト管理および会計** > **設定** > **転記** > **プロジェクト グループ**)で投資のために作成されたプロジェクト グループの関係を作成することができます。

![図 4](media/27-work-orders.png)

4. 固定資産オブジェクトに関連する作業指示書を作成する場合は、投資の処理に使用する "投資" などの作業指示書タイプを選択します。

5. 作業指示書が作成されると、関連する作業指示書タイプが**すべての作業指示書**で表示されます。

![図 5](media/28-work-orders.png)

6. 作業指示書が作成されると、その作業指示書に関連付けられているプロジェクトが**プロジェクト管理および会計** > **すべてのプロジェクト**に作成されます。 作業指示書で**プロジェクト ID** リンクをクリックすると、プロジェクト関連の情報を確認できます (**資産管理**の作業指示書の詳細ビュー > **明細行の詳細**クイックタブ > **一般** タブ > **プロジェクト ID** フィールド)。

![図 6](media/29-work-orders.png)

7. **固定資産**では、固定資産に関連付けられているプロジェクトの概要を閲覧できます (**固定資産** > **固定資産** > **固定資産** > **固定資産番号**フィールドの固定資産をクリック > **関連情報**ウィンドウでコンテンツを表示 > **関連付けられたプロジェクト** セクション)。

