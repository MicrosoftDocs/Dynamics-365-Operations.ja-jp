---
title: Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)
description: この記事では、Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー ツールについて説明します。
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012, Operations
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 0ad6f86cfb21b2d74078fba1e9ae2dd358eb4cbb
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454801"
---
# <a name="business-process-modeler-bpm-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) は、業務プロセス ライブラリに基づいて反復可能な実装を作成、表示、および変更するために使用することができるツールです。 BPM は、[アメリカ生産性 &amp; 品質センター (APQC)](https://www.apqc.org/) によって説明された業界標準プロセスを使用して、業務プロセスを配置するのに役立ちます。 Finance and Operations アプリで、業務上の要件と既定のプロセスの間でフィット アンド ギャップ分析を行うことができます。 また、まだ定義されていない新たなビジネス プロセスを追加することができます。

BPM は次の製品と互換性があります。

- **Microsoft Word** - 業務プロセスのドキュメントを生成することができます。
- **Microsoft Visio** – 業務プロセスのマップを Visio ファイルにエクスポートできます。

> [!NOTE]
> このトピックに記載の情報は Finance and Operations アプリのみに特化しています。 ビジネス プロセス モデラーおよび Microsoft Dynamics AX 2012 の詳細については、 [Lifecycle Services (LCS) における ビジネス プロセス モデラー (BPM)](ax-2012/business-process-modeler-lcs.md)を参照してください。 

## <a name="prerequisites"></a>必要条件

BPM を効果的に使用するには、Microsoft Office 2010 と Microsoft Azure DevOps プロジェクトが必要です。

## <a name="getting-started"></a>はじめに

BPM にアクセスするには、これらの手順に従います。

1. [LCS](https://lcs.dynamics.com/)  に移動します。
2. サインインしてプロジェクトを開き、ドロップダウン メニューから **ビジネス プロセス モデラー** を選択します。 **業務プロセス ライブラリ** ページには 3 つのセクションがあります。

    - **プロジェクト ライブラリ** – このセクションには、ユーザーが作成、追加したビジネス プロセスが含まれています。
    - **コーポレート ライブラリ** - このセクションには、組織内のユーザーが発行した独自の業務プロセスが含まれます。
    - **グローバル ライブラリ** – このセクションには、Microsoft が一般的に公開している業界に共通する標準的なビジネス プロセスが含まれています。

3. 標準的なビジネス プロセス ライブラリを **グローバル ライブラリ** セクションから **プロジェクト ライブラリ** セクションにコピーするには、**グローバル ライブラリ** セクションでタイルの右上隅を選択し、**コピー** を選択します。
4. 業務プロセス ライブラリが**プロジェクト ライブラリ** セクションに追加された後、タイルを選択して業務プロセス ライブラリを表示します。

## <a name="additional-resources"></a>追加リソース

- [ビジネス プロセス モデラー (BPM) のライブラリを作成、編集、および参照](creating-editing-browsing.md)
- [BPM ライブラリと Azure DevOps の同期](synchronize-bpm-vsts.md)
- [ビジネス プロセス モデラー (BPM) でのタスクの完了](complete-tasks-bpm.md)
- [ビジネス プロセス モデラー ライブラリの活動ダイアグラムを使用する](using-activity-diagrams.md)
- [ビジネス プロセス モデラー (BPM) ビジネス プロセス ライブラリ](business-process-libraries-business-process-modeler.md)
- [ビジネス プロセス モデラー (BPM) のフローチャート](flowcharts-business-process-modeler.md)


