---
title: Project Service Automation
description: "このソリューションは、データ統合機能を使用して、Common Data Service (CDS) 経由で Microsoft Dynamics 365 for Finance and Operations のインスタンス、および Microsoft Dynamics 365 for Project Service Automation 間でデータを同期します。"
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

Project Service Automation から Finance and Operations への統合のソリューションは、データ統合機能を使用して、Common Data Service (CDS) 経由で Microsoft Dynamics 365 for Finance and Operations のインスタンス、および Microsoft Dynamics 365 for Project Service Automation 間でデータを同期します。 データの統合機能で使用可能な統合テンプレートは、Project Service Automation から Finance and Operations へのプロジェクト、プロジェクト契約、プロジェクト契約ライン、プロジェクト契約明細行のマイルストーン、プロジェクト タスク、経費トランザクション カテゴリ、時間見積、および経費見積の流れを有効にします。

> [!NOTE] 
> Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4074835 をインストールする必要があります。 これにより、固定価格プロジェクトを統合することができます。
>
> Dynamics 365 for Finance and Operations バージョン 8.0 を使用している場合は、プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックを使用できるようになります。
>
> Dynamics 365 for Finance and Operations バージョン 8.0.1 を使用している場合は、実績を同期することができます。
>
> Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。 勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。

Project Service Automation を Finance and Operations と統合する前に、Project Service Automation の統合パラメーターをコンフィギュレーションする必要があります。 詳細については、Project Service Automation の統合パラメーターを参照してください。

統合ソリューションにより、次のシナリオで直接同期できます。

- Project Service Automation でプロジェクト契約を管理し、Project Service Automation から Finance and Operations に直接同期させます。
- Project Service Automation でプロジェクトを作成し、Project Service Automation から Finance and Operations に直接同期させます。
- Project Service Automation でプロジェクト契約明細行を管理し、Project Service Automation から Finance and Operations に直接同期させます。
- Project Service Automation でプロジェクト契約明細行のマイルストーンを管理し、Project Service Automation から Finance and Operations に直接同期させます。
- Project Service Automation でプロジェクト タスクを管理し、Project Service Automation から Finance and Operations に直接同期させます。
- Finance and Operations で経費トランザクション カテゴリを管理し、Finance and Operations から Project Service Automation に直接同期させます。
- Project Service Automation でプロジェクト時間見積を作成し、Project Service Automation から Finance and Operations に直接同期させます。
- Project Service Automation でプロジェクト経費見積を作成し、Project Service Automation から Finance and Operations に直接同期させます。

## <a name="data-synchronization"></a>データ同期
次の図は、データが Project Service Automation と Finance and Operations との間で統合の一部として同期される方法を示しています。

> [!NOTE]
> 現在利用可能なテンプレートはありません。 完了するとテンプレートがリリースされます。

[![Project Service Automation を Finance and Operations と統合](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations のシステム要件

Finance and Operations 統合ソリューションに対して Project Service Automation を使用するには、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 およびプラットフォーム更新プログラム 12 またはそれ以降のバージョンをインストールする必要があります。

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation のシステム要件

Finance and Operations 統合ソリューションに対して Project Service Automation を使用するには、次のコンポーネントをインストールする必要があります。

- Microsoft Dynamics 365 for Project Service Automation バージョン 9.0.0.0 以降。
- Dynamics 365 for Sales バージョン 1.14.0.0 (v14) またはそれ以降の見込顧客を現金化するソリューション。
- Dynamics 365 for Project Service Automation バージョン 1.0.0.0 以降の Operations ソリューションに対する Project Service Automation。

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automation インスタンス に Finance and Operations 統合ソリューションに対する Project Service Automation をインストールします



