---
title: Azure Pipelines でのレガシ パイプラインの更新
description: この記事では、Azure Pipelines でのレガシ パイプラインを更新して、新しいバージョンの Visual Studio を使用する方法について説明します。
author: gianugo
ms.date: 09/23/2020
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.openlocfilehash: a90c477a8806449df39998abcba32dd7cb3b82f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271051"
---
# <a name="update-a-legacy-pipeline-in-azure-pipelines"></a>Azure Pipelines でのレガシ パイプラインの更新

[!include [banner](../includes/banner.md)]

> [!NOTE]
> このドキュメントは、ビルド仮想マシン上で実行する場合でも、[新しいビルド パイプライン](hosted-build-automation.md) には適用されません。

**Azure Pipelines** パイプラインは、**MSBuild** および **VS テスト** などの **Visual Studio** ツールのバージョンを明示的に指定します。 これらの製品の新しいバージョンのサポートを継続するために、新しい仮想マシンはプレインストールされている **Visual Studio** よりも新しいバージョンで配置されます。 新しいバージョンを使用するために、既存のパイプラインはすべて手動で更新する必要があります。

## <a name="determine-if-your-pipeline-needs-to-be-updated"></a>パイプラインを更新する必要があるかどうか確認する

 **Visual Studio 2017** を含むバージョン 10.0.20 を通してバージョン 10.0.13 を展開した Virtual Machines をビルドおよび開発します。 バージョン10.0.21以降に展開 **されたシステムには、Visual Studio 2019** も含まれます。 2021 年 4 月に [Visual Studio2015 のサポートは廃止](../get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10011-of-finance-and-operations-apps) となり、2022 年 4 月に [Visual Studio 2017 のサポートは廃止されました](/lifecycle/products/visual-studio-2017)。 ビルド仮想マシンに **Visual Studio 2019** が含まれていない場合、バージョン 10.0.21 またはそれ以降の新しいビルド仮想マシンを配置する計画をするか、または新しく [ホストされるビルド パイプライン](hosted-build-automation.md) の使用を考慮する必要があります。

ビルド仮想マシンに Visual Studio 2019 がインストールされている場合、新しいバージョンの **MSBuild** と **VS テスト** を使用することができます。 パイプラインがバージョン 10.0.21 以前の仮想マシン配置によって作成されている場合、パイプラインを手動で更新する必要があります。

最後に、**ソリューションのビルド** ステップでビルド パイプラインを確認できます。 **MSBuild のバージョン** プロパティは、使用中の **Visual Studio** のバージョンを示しています。

| MSBuild のバージョン | Visual Studio のバージョン |
|---|---|
| MSBuild 14.0 | Visual Studio 2015 |
| MSBuild 15.0 | Visual Studio2017 |
| MSBuild 16.0 | Visual Studio 2019 |

## <a name="updating-the-azure-pipelines-pipeline"></a>Azure Pipelines のパイプラインを更新する

> [!NOTE]
> **Azure Pipelines** パイプラインを更新して、**Visual Studio 2019** を使用できるようにするには、ビルドの仮想マシンのバージョンが 10.0.21 以降に更新されていることを確認してください。

パイプラインの 3 つのタスク内にある、次の 4 つのプロパティを更新する必要があります。

| タスク名 | タスクのプロパティ | 元の値 | 新しい値|
| --- | --- | --- | ---|
| ソリューションをビルドする | MSBuild のバージョン | MSBuild 14.0/15.0 | MSBuild 16.0 |
| データベース同期 | MSBuild のバージョン | MSBuild 14.0/15.0 | MSBuild 16.0 |
| テストの実行 | プラットフォーム バージョンのテスト | Visual Studio 2015/2017 | Visual Studio 2019 |
| テストの実行 | その他のコンソール オプション | `/Platform:X64 /InIsolation /UseVsixExtensions:true` | `/Platform:X64 /InIsolation /TestAdapterPath:"$(VsixExtensionFolder)"` |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
