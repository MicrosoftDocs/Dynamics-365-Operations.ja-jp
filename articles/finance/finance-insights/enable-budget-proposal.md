---
title: 予算案の有効化 (プレビュー)
description: このトピックでは、財務インサイトの予算案機能を有効にする方法について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
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
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d8443c4e3e6f3d3a90acedc7c05b2846d6b68369
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646208"
---
# <a name="enable-budget-proposals-preview"></a>予算案の有効化 (プレビュー)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、財務インサイトの予算案機能を有効にする方法について説明します。

1. Microsoft Dynamics Lifecycle Services (LCS) で環境ページの情報を使用して、その環境に対する Azure SQL のプライマリ インスタンスに接続します。 次の Transact-SQL (T-SQL) コマンドを実行して、サンドボックス環境のフライトを有効にします。 (Application Object Server \[AOS\] にリモートで接続する前に、LCS で IP アドレスに対してアクセスを有効にする必要がある場合があります。)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Microsoft Dynamics 365 Finance の配置が Service Fabric 配置である場合は、この手順を省略できます。 財務インサイト チームは既にフライトを有効にしている必要があります。 **機能管理** ワークスペースに機能が表示されない場合、または有効にしようとしたときに問題が発生した場合は、[財務インサイト アプリ プレビュー チーム](mailto:fiap@microsoft.com) に電子メールを送信してください。

2. **機能管理** ワークスペースを開き、次の手順に従います:

    1. **更新プログラムの確認** を選択します。
    2. **予算案** を検索し、その機能を有効にします。

3. **予算作成 \>設定 \> 基本予算作成 \> 予算案 (プレビュー)** に移動して、**機能の有効化** を選択します。

#### <a name="privacy-notice"></a>プライバシー通知
プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]