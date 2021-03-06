---
title: 予算案の有効化 (プレビュー)
description: このトピックでは、財務インサイトの予算案機能を有効にする方法について説明します。
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222537"
---
# <a name="enable-budget-proposals-preview"></a>予算案の有効化 (プレビュー)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、財務インサイトの予算案機能を有効にする方法について説明します。

1. Microsoft Dynamics Lifecycle Services (LCS) で環境ページの情報を使用して、その環境に対する Azure SQL のプライマリ インスタンスに接続します。 次の Transact-SQL (T-SQL) コマンドを実行して、サンドボックス環境のフライトを有効にします。 (Application Object Server \[AOS\] にリモートで接続する前に、LCS で IP アドレスに対してアクセスを有効にする必要がある場合があります。)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > バージョン 10.0.20 以降を使用している場合や、Service Fabric のデプロイを使用している場合は、この手順をスキップします。 財務インサイト チームは既にフライトを有効にしている必要があります。 **機能管理** ワークスペースに機能が表示されない場合や、有効にしようとしたときに問題が発生した場合は、<fiap@microsoft.com> までご連絡ください。

2. **機能管理** ワークスペースを開き、次の手順に従います:

    1. **更新プログラムの確認** を選択します。
    2. **予算案** を検索し、その機能を有効にします。

3. **予算作成 \>設定 \> 基本予算作成 \> 予算案 (プレビュー)** に移動して、**機能の有効化** を選択します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
