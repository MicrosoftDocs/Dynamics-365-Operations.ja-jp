---
title: Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)
description: この記事では、Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー ツールについて説明します。
author: kfend
manager: AnnBe
ms.date: 10/18/2017
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
ms.author: ntecklu
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: bf20e2690d42e4d7241eeeb732dcf0132b593864
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811701"
---
# <a name="business-process-modeler-bpm-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) は、業務プロセス ライブラリとフローチャートに基づいて反復可能な実装を作成、表示、および変更するために使用することができるツールです。 BPM は、[アメリカ生産性 &amp; 品質センター (APQC)](https://www.apqc.org/) によって説明された業界標準プロセスを使用して、業務プロセスを配置するのに役立ちます。 Finance and Operations アプリで、業務上の要件と既定のプロセスの間でフィットギャップ分析を実行することができます。 また、新しい業務プロセスを追加して、まだ定義されていないプロセスのためにフローチャートを作成することができます。

BPM は次のプログラムと互換性があります。

- **Microsoft Word** - 業務プロセスのドキュメントを生成することができます。
- **Microsoft Visio** – 業務プロセスのマップを Visio ファイルにエクスポートできます。

> [!NOTE]
> このトピックに記載されている情報は、Finance and Operations アプリにのみ適用されます。 ビジネス プロセス モデラーおよび Microsoft Dynamics AX 2012 の詳細については、 [Lifecycle Services (LCS) における ビジネス プロセス モデラー (BPM)](ax-2012/business-process-modeler-lcs.md)を参照してください。 

## <a name="prerequisites"></a>必要条件

BPM を効果的に使用するには、Microsoft Office 2010 と Microsoft Azure DevOps プロジェクトが必要です。

## <a name="getting-started"></a>はじめに

BPM にアクセスするには、これらの手順に従います。

1. [LCS](https://lcs.dynamics.com/)  に移動します。
2. サインインしてプロジェクトを開き、**ビジネス プロセス モデラー** タイルを選択します。 **業務プロセス ライブラリ** ページには 3 つのセクションがあります。

    - **自分のライブラリ** – このセクションには、ユーザーが作成または追加したビジネス プロセスが含まれています。
    - **コーポレート ライブラリ** - このセクションには、組織内のユーザーがアップロードした独自の業務プロセスが含まれます。
    - **グローバル ライブラリ** – このセクションには、産業間の標準の業務プロセスが含まれています。

3. 標準的なビジネス プロセス ライブラリを **グローバル ライブラリ** セクションから **マイ ライブラリ** セクションにコピーするには、**グローバル ライブラリ** セクションでタイルの右上隅を選択し、**コピー** を選択します。
4. 業務プロセス ライブラリが**自分のライブラリ** セクションに追加された後、タイルを選択して業務プロセス ライブラリを表示します。

## <a name="working-in-bpm-libraries"></a>BPM ライブラリでの作業

次のトピックでは、BPM ライブラリを使用して作業する方法について詳しく説明します。

- [ビジネス プロセス モデラー (BPM) のライブラリを作成、編集、および参照](creating-editing-browsing.md)
- [BPM ライブラリと Azure DevOps の同期](synchronize-bpm-vsts.md)
- [ビジネス プロセス モデラー (BPM) でのタスクの完了](complete-tasks-bpm.md)
- [ビジネス プロセス モデラー ライブラリの活動ダイアグラムを使用する](using-activity-diagrams.md)
- [ビジネス プロセス モデラー (BPM) ビジネス プロセス ライブラリ](business-process-libraries-business-process-modeler.md)
- [ビジネス プロセス モデラー (BPM) のフローチャート](flowcharts-business-process-modeler.md)


