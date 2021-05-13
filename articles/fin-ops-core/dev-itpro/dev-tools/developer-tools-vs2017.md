---
title: X++ の Visual Studio 2017 の要件
description: このトピックでは X++ の Visual Studio拡張機能を実行するために必要な Visual Studio 2017 コンポーネントの一覧を示します。
author: jorisdg
ms.date: 04/01/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.author: jorisde
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8dbafdac2dbab7057f921d128c84eedd02680049
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880702"
---
# <a name="visual-studio-2017-requirements-for-x"></a>X++ の Visual Studio 2017 の要件

[!include [banner](../includes/banner.md)]

このトピックでは X++ の **Visual Studio** 拡張機能を実行するために必要な Visual Studio 2017 コンポーネントの一覧を示します。

> [!NOTE]
> Lifecycle Services (LCS) から配置されたダウンロード可能な仮想ハード ドライブ (VHD) または仮想マシンに Visual Studio を手動でインストールすることはお勧めしません。 代わりに、新しい仮想マシンをダウンロードまたは配置することを強く推奨します。 バージョン10.0.13 以降に配置された仮想マシンにはすべて Visual Studio 2017 とその前提条件がインストールされ、マシンの互換性とセキュリティを維持するために Visual Studio の外部に他の更新が付属しています。

## <a name="visual-studio-editions"></a>Visual Studio エディション

Visual Studio のサポートされているエディションは次のとおりです。

- Visual Studio 2017 Professional
- Visual Studio 2017 Enterprise

> [!NOTE]
> Visual Studio のエディションが異なれば、ライセンス要件とコストも異なります。 詳細については、[Visual Studio](https://visualstudio.microsoft.com) を参照してください。

## <a name="required-visual-studio-components"></a>必要とされる Visual Studio コンポーネント

次の表に、必要な Visual Studio コンポーネントを一覧表示します。

| 種類 | 氏名 | 必須 | 摘要 |
| --- | --- | --- | --- |
| ワークロード | .NET デスクトップ開発 | あり | |
| 個々のコンポーネント | モデリング SDK | あり | |
| 個々のコンポーネント | DGML エディター | なし | このコンポーネントは、有向グラフ マークアップ言語を使用する依存関係グラフ機能で使用されます。 |
| Visual Studio Marketplace | Microsoft Reporting Services プロジェクト | あり | このコンポーネントは、レポート開発に必要です。 コンポーネントがインストールされていない場合、Visual Studio はレポート デザインを開こうとすると、メッセージを表示します。 |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce

コマースおよび Visual Studio 2017 の詳細については、次のトピックを参照してください。

- [Retail SDK の Visual Studio 2015 から Visual Studio 2017 への移行](../../../commerce/dev-itpro/retail-sdk/migrate-sdk.md)
- [バージョン 10.0.10 から 10.0.13 における開発と ALM の変更](../../../commerce/dev-itpro/dev-changes-10-13.md)
