---
title: Azure Pipelines でのレガシ パイプラインの更新
description: このトピックでは、Azure Pipelines でのレガシ パイプラインを更新して、新しいバージョンの Visual Studio を使用する方法について説明します。
author: jorisdg
ms.date: 09/23/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d180759f89aa457f676b28fc4e9b19aa04ef46f0329a62ab519eb45ed9a0bfb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736256"
---
# <a name="update-a-legacy-pipeline-in-azure-pipelines"></a>Azure Pipelines でのレガシ パイプラインの更新

[!include [banner](../includes/banner.md)]

> [!NOTE]
> このドキュメントは、ビルド仮想マシン上で実行する場合でも、[新しいビルド パイプライン](hosted-build-automation.md) には適用されません。

> バージョン 10.0.13 またはそれ以降が配置された仮想マシン上で **Visual Studio 2017** が使用可能な場合でも、**VSTest** を使用した単体テストをサポートするのに必要なビルド スクリプトには、バージョン 10.0.15 が必要です。

**Azure Pipelines** パイプラインは、**MSBuild** および **VS テスト** などの **Visual Studio** ツールのバージョンを明示的に指定します。 これらの製品の新しいバージョンのサポートを継続するために、新しい仮想マシンはプレインストールされている **Visual Studio** よりも新しいバージョンで配置されます。 新しいバージョンを使用するために、既存のパイプラインはすべて手動で更新する必要があります。

## <a name="determine-if-your-pipeline-needs-to-be-updated"></a>パイプラインを更新する必要があるかどうか確認する

バージョン 10.0.13 を使用して配置されたビルドおよび開発仮想マシンには **Visual Studio 2017** が含まれます。 2021 年 4 月のリリースでは、[Visual Studio 2015 のサポートは非推奨](../get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10011-of-finance-and-operations-apps) になります。 ビルド仮想マシンに **Visual Studio 2017** が含まれていない場合、バージョン 10.0.13 またはそれ以降の新しいビルド仮想マシンを配置する計画をするか、または新しく [ホストされるビルド パイプライン](hosted-build-automation.md) の使用を考慮する必要があります。

ビルド仮想マシンに Visual Studio 2017 がインストールされている場合、新しいバージョンの **MSBuild** と **VS テスト** を使用することができます。 パイプラインがバージョン 10.0.13 以前の仮想マシン配置によって作成されている場合、パイプラインを手動で更新する必要があります。

最後に、**ソリューションのビルド** ステップでビルド パイプラインを確認できます。 **MSBuild のバージョン** プロパティは、使用中の **Visual Studio** のバージョンを示しています。

| MSBuild のバージョン | Visual Studio のバージョン |
|---|---|
| MSBuild 14.0 | Visual Studio2015 |
| MSBuild 15.0 | Visual Studio2017 |

## <a name="updating-the-azure-pipelines-pipeline"></a>Azure Pipelines のパイプラインを更新する

> [!NOTE]
> **Azure Pipelines** のパイプラインを更新して、**Visual Studio 2017** を使用できるようにするには、ビルドの仮想マシンのバージョンが 10.0.15 またはそれ以降に更新されていることを確認してください。

パイプラインの 3 つのタスク内にある、次の 4 つのプロパティを更新する必要があります。

| タスク名 | タスクのプロパティ | 元の値 | 新しい値|
| --- | --- | --- | ---|
| ソリューションをビルドする | MSBuild のバージョン | MSBuild 14.0 | MSBuild 15.0 |
| データベース同期 | MSBuild のバージョン | MSBuild 14.0 | MSBuild 15.0 |
| テストの実行 | プラットフォーム バージョンのテスト | Visual Studio2015 | Visual Studio2017 |
| テストの実行 | その他のコンソール オプション | `/Platform:X64 /InIsolation /UseVsixExtensions:true` | `/Platform:X64 /InIsolation /TestAdapterPath:"$(VsixExtensionFolder)"` |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]