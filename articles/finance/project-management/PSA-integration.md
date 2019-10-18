---
title: Project Service Automation の概要
description: このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance への統合について説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250556"
---
# <a name="project-service-automation-overview"></a>Project Service Automation の概要

[!include[banner](../includes/banner.md)]

Project Service Automation から Finance の統合ソリューションは、データの統合機能を使用して、Common Data Service 経由で Dynamics 365 Finance のインスタンスおよび Dynamics 365 Project Service Automation 間でデータを同期します。 データの統合機能で使用可能な統合テンプレートは、Project Service Automation から Finance へのプロジェクト、プロジェクト契約、プロジェクト契約ライン、プロジェクト契約明細行のマイルストーン、プロジェクト タスク、経費トランザクション カテゴリ、時間見積、および経費見積の流れを有効にします。

> [!NOTE]
> - バージョン 7.3.0 を使用している場合は、KB 4074835 をインストールする必要があります。 その後、固定価格プロジェクトを統合することができます。
> - バージョン 7.3.0 を使用し、Project Service Automation から手数料トランザクションを挿入する場合は、プロジェクト請求書にそれらの手数料を含めるために KB 4345320 をインストールする必要があります。
> - バージョン 8.0 を使用している場合は、プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックを使用できるようになります。
> - バージョン 8.0.1 以降を使用している場合は、実績を同期できます。

Project Service Automation Finance を統合する前に、Project Service Automation の統合パラメーターをコンフィギュレーションする必要があります。 詳細については、[Project Service Automation 統合パラメーター](PSA-parameters.md) を参照してください。

統合ソリューションにより、次のシナリオで直接同期できます。

- Project Service Automation でプロジェクト契約を管理し、Project Service Automation から Finance に直接同期させます。
- Project Service Automation でプロジェクトを作成し、Project Service Automation から Finance に直接同期させます。
- Project Service Automation でプロジェクト契約明細行を管理し、Project Service Automation から Finance に直接同期させます。
- Project Service Automation でプロジェクト契約明細行のマイルストーンを管理し、Project Service Automation から Finance に直接同期させます。
- Project Service Automation でプロジェクト タスクを管理し、Project Service Automation から Finance に直接同期させます。
- Finance で経費トランザクション カテゴリを管理し、Finance から Project Service Automation に直接同期させます。
- Project Service Automation でプロジェクト時間見積を作成し、Project Service Automation から Finance に直接同期させます。
- Project Service Automation でプロジェクト経費の見積を作成し、Project Service Automation から Finance に直接同期させます。
- Project Service Automation でプロジェクト時間、経費、および手数料の実績を作成し、Finance に転記できるように、Project Service Automation 統合仕訳帳でプロジェクト トランザクションを作成します。

## <a name="data-synchronization"></a>データ同期

次の図は、データが Project Service Automation と Finance との間で統合の一部として同期される方法を示しています。

> [!NOTE]
> 現在利用可能なテンプレートはありません。 完了するとテンプレートがリリースされます。

[![Project Service Automation とFinance の統合](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Finance のシステム要件

Finance 統合ソリューションに対して Project Service Automation を使用するには、Enterprise edition 7.3 およびプラットフォーム更新プログラム 12 またはそれ以降のバージョンをインストールする必要があります。

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation のシステム要件

Finance 統合ソリューションに対して Project Service Automation を使用するには、次のコンポーネントをインストールする必要があります。

- Dynamics 365 Project Service Automation バージョン 9.0.0.0 以降
- Dynamics 365 Sales バージョン 1.14.0.0 (v14) またはそれ以降の見込顧客を現金化するソリューション
- Dynamics 365 Project Service Automation バージョン 1.0.0.0 以降の Finance ソリューションに対する Project Service Automation

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automation インスタンス に Finance 統合ソリューションに対する Project Service Automation をインストールします

[Microsoft ダウンロード センター](https://www.microsoft.com/download/details.aspx?id=57016) から Finance ソリューションに対する Project Service Automation をダウンロードし、ソリューションに含まれている手順に従ってください。
