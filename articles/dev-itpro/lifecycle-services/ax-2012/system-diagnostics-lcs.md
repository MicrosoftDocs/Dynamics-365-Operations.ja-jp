---
title: Lifecycle Services (LCS) のシステム診断
description: このトピックでは、Lifecycle Services (LCS) のシステム診断に関する詳細情報を提供します。
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 19061
ms.assetid: 9a217373-f72b-4a28-adef-79900e40c872
ms.search.region: Global
ms.author: murtazac
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: ce87b1bf76a8a2ec2fb33c40ec142a386dc98cc5
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850489"
---
# <a name="system-diagnostics-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) のシステム診断

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics Lifecycle Services で、システム診断は管理者が 1 つまたは複数の Microsoft Dynamics AX 環境の正常性を監視および把握するのに役立ちます。 次のタスクを実行するように構成できるローカルにインストールされたコンポーネントがあるクラウド ベースのツールです。
-   オンプレミスの Microsoft Dynamics AX 環境を検出 (データベースのインスタンスおよび Microsoft Dynamics AX Application Object Server (AOS) インスタンス)。
-   検出された環境からデータを収集します。
-   収集したデータでルールを実行します。
-   ダッシュボードの規則違反を報告します。
-   レポートを提供します。

データは、事前定義されたスケジュールで実行されるジョブを使用して収集されます。 次の図は、システム診断プログラムとローカルにインストールされたコンポーネントがどのようにやり取りするかを示しています。
システム診断サービス

![システム診断サービス (Lifecycle Services)](./media/systemdiagnosticservicelifecycleservices.png) システム診断では、Microsoft Dynamics AX の次のバージョンがサポートされています。
-   Microsoft Dynamics AX 2012 R2
-   Microsoft Dynamics AX 2012 Feature Pack
-   Microsoft Dynamics AX 2012
-   Microsoft Dynamics AX 2012 R3

## <a name="prerequisites"></a>必要条件
システム診断を使用する前に、次の作業を行う必要があります。
-   Diagnostic サービスのインストーラーをダウンロードして実行します。
-   検出ウィザードを実行します。
-   データの収集をスケジュールまたは実行します。

## <a name="getting-started"></a>はじめに
次のトピックでは、システム診断をインストールして使用する方法について説明します。
-   [システム診断のインストールと実行 (Lifecycle Services)](install-run-system-diagnostics-lcs.md)
-   [システム診断を使用する (Lifecycle Services)](system-diagnostics-lcs.md)





