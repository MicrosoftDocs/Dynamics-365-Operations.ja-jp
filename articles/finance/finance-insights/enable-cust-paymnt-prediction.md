---
title: 顧客支払予測の有効化 (プレビュー)
description: このトピックでは、財務インサイトで顧客支払予測機能をオンにし構成する方法について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e10aa9342ec9f089ef8ecec5e1221a31c580fc87
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644996"
---
# <a name="enable-customer-payment-predictions-preview"></a>顧客支払予測の有効化 (プレビュー)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、財務インサイトで顧客支払予測機能をオンにし構成する方法について説明します。 **機能管理** ワークスペースで機能を有効にし、**財務インサイト パラメーター** ページで構成設定を入力します。 このトピックには、機能を効果的に使用するために役立つ情報も含まれています。

> [!NOTE]
> 次の手順を実行する前に、[財務インサイトの構成](configure-for-fin-insites.md) トピックの前提条件の手順を必ず完了してください。

1. Microsoft Dynamics Lifecycle Services (LCS) で環境ページの情報を使用して、その環境に対する Azure SQL のプライマリ インスタンスに接続します。 次の Transact-SQL (T-SQL) コマンドを実行して、サンドボックス環境のフライトを有効にします。 (Application Object Server \[AOS\] にリモートで接続する前に、LCS で IP アドレスに対してアクセスを有効にする必要がある場合があります。)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > Microsoft Dynamics 365 Finance の配置が Service Fabric 配置である場合は、この手順を省略できます。 財務インサイト チームは既にフライトを有効にしている必要があります。 **機能管理** ワークスペースに機能が表示されない場合や、有効にしようとしたときに問題が発生した場合は、<fiap@microsoft.com> に連絡してください。

2. 顧客支払に関するインサイト機能を有効にします:

    1. **システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。
    2. **顧客支払に関するインサイト (プレビュー)** と呼ばれる機能を検索します。
    3. **直ちに有効化** を選択します。

    これで、顧客支払に関するインサイト機能が有効になり、構成する準備が整いました。

3. 顧客支払に関するインサイト機能を構成します:

    1. **与信および回収 \> 設定 \> 財務インサイト \> 財務インサイト パラメーター** に移動します。

        [![機能を構成する前の財務インサイト パラメーター ページ](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. **財務インサイト パラメーター** ページの **顧客支払に関するインサイト** タブで、**予測モデルに使用されるデータ フィールドの表示** リンクを選択して、**予測モデルのデータ フィールド** ページを開きます。 ここでは、顧客支払予測に対して人工知能 (AI) 予測モデルを作成するために使用されるフィールドの既定の一覧を表示できます。

        既定のフィールド一覧を使用して予測モデルを作成するには、**予測モデルのデータ フィールド** ページを閉じて、**財務インサイト パラメーター** ページで **機能の有効化** オプションを **はい** に設定します。

    3. "かなりの遅延" トランザクション期間を指定して、**かなりの遅延** の予測バケットがビジネスにとって何を意味するかを定義します。

        未処理の請求書ごとに、システムは、以下の 3 つのバケットで支払いの確率を予測します: **期限内**、**遅延**、**かなりの遅延**。

        - **期限内** – このバケットには、トランザクションの期日またはそれ以前に支払われると予測される支払が含まれます。
        - **遅延** – このバケットには、トランザクション期日後ではあるが、"かなりの遅延" トランザクション期間の開始前に支払われると予測される支払が含まれます。
        - **かなりの遅延** – このバケットには、"かなりの遅延" トランザクション期間の開始後に支払われると予測される支払が含まれます。

        > [!NOTE]
        > "かなりの遅延" トランザクション期間を変更し、顧客支払の AI 予測モデルが作成された後に **遅延しきい値の変更** を選択した場合、既存の予測モデルが削除され、新しいモデルが作成されます。 新しい予測モデルは、それを定義するために入力された設定に基づいて、トランザクションを "かなりの遅延" 期間に移動します。

    4. "かなりの遅延" トランザクション期間の定義が完了したら、**予測モデルの作成** を選択し、予測モデルを作成します。 **財務インサイト パラメーター** ページの **予測モデル** セクションには、予測モデルの状態が表示されます。

        > [!NOTE]
        > 予測モデルの作成中はいつでも、**モデル作成のリセット** を選択して、プロセスを再起動できます。

    これで、機能が構成され、使用する準備が整いました。

機能を有効にして構成し、予測モデルを作成して実行すると、次の図に示すように、**財務インサイト パラメーター** ページの **予測モデル** セクションにモデルの精度が表示されます。

[![財務インサイト パラメーター ページの予測モデルの正確性](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>リリースの詳細

財務インサイトのパブリック プレビューは、米国、ヨーロッパ、および英国での試用版の展開に使用できます。 Microsoft は、より多くの地域に対するサポートを段階的に追加しています。

パブリック プレビュー機能は、Tier-2 のサンドボックス環境でのみ有効にすることができます。 サンドボックス環境で作成された設定および AI モデルは、運用環境に移行できません。 詳細については、[Microsoft Dynamics 365 プレビューの補足の使用条件](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms) を参照してください。

## <a name="privacy-notice"></a>プライバシー通知

プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。
