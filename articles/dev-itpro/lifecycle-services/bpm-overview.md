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
ms.reviewer: kfend
ms.search.scope: AX 2012, Operations
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 1b539a0cda6f663d56b21638303dd828075ae202
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537225"
---
# <a name="business-process-modeler-bpm-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) は、業務プロセス ライブラリとフローチャートに基づいて反復可能な実装を作成、表示、および変更するために使用することができるツールです。 BPM は、[アメリカ生産性&amp;品質センター (APQC)](http://www.apqc.org/) によって説明された業界標準プロセスを使用して、業務プロセスを Microsoft Dynamics 365 for Finance and Operations に配置するのに役立ちます。 Microsoft Dynamics 365 for Finance and Operations で、業務上の要件と既定のプロセスの間でフィットギャップ分析を実行することができます。 また、新しい業務プロセスを追加して、Finance and Operations でまだ定義されていないプロセスのためにフローチャートを作成することができます。

BPM は次のプログラムと互換性があります。

- **Microsoft Word** - 業務プロセスのドキュメントを生成することができます。
- **Microsoft Visio** – 業務プロセスのマップを Visio ファイルにエクスポートできます。

**注記:** このトピックの情報は Dynamics 365 for Finance and Operations 固有です。 ビジネス プロセス モデラーおよび Microsoft Dynamics AX 2012 の詳細については、[ビジネス プロセス モデラー](ax-2012/business-process-modeler-lcs.md)を参照してください。 

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

- [BPM ライブラリの作成、編集、または参照](creating-editing-browsing.md)
- [BPM ライブラリと Azure DevOps の同期](synchronize-bpm-vsts.md)
- [BPM のタスクの完了](complete-tasks-bpm.md)
- [BPM 付き活動ダイアグラムを使用する](using-activity-diagrams.md)
- [ビジネス プロセス モデラーの業務プロセス ライブラリ](business-process-libraries-business-process-modeler.md)
- [ビジネス プロセス モデラーのフローチャート](flowcharts-business-process-modeler.md)


