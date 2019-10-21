---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: sarvanisathish
manager: AnnBe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: f109c5d996aa31b1d71af85cdea7e8caa7e16edc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191584"
---
# <a name="known-issues-with-self-service-deployment"></a>セルフサービス配置に関する既知の問題

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

このトピックでは、[セルフ サービス配置](infrastructure-stack.md)の既知の問題について説明します。

## <a name="lifecycle-services-lcs"></a>Lifecycle Services (LCS)

### <a name="features-not-intended-to-be-implemented"></a>実装が意図されていない機能
次の LCS 機能は廃止されており、セルフ サービス配置では実装されません。

| **機能**        | **説明**   |
|--------------------|--------|
| システム診断 | システム診断は非推奨です。 現在のシステム診断によって提供されるすべてのデータと機能は、製品と LCS のその他の機能を通じて使用可能になります。 |
| サービス要求   | サービス要求は、セルフ サービス アクションに置き換えられます。 |

### <a name="known-issues-in-this-release"></a>このリリースの既知の問題
既知の問題は、将来のリリースで解決されるバグです。 2 週間おきに LCS の新しいリリースがあります。

-   配置エラーを一覧表示するログ ファイルは、まだ LCS を通じて使用できません。 現時点では、ログ ファイルが必要な場合は、サポート チケットを開くことができます。

-   アプリケーション環境からの LCS の統合が機能しません。 この結果使用できない機能は次のとおりです。

    -   はじめに

    -   BPM ライブラリを通じて有効なオンライン ヘルプ。 docs.microsoft.com のオンライン ヘルプは使用できます。

    -   アプリケーション内からのサポート チケットを引き上げます。 LCS からのクラウドを利用したサポートが有効です。

## <a name="finance-and-operations-apps"></a>Finance and Operations アプリ 

### <a name="features-not-yet-implemented"></a>まだ実装されていない機能

インフラストラクチャの依存関係がある次の機能は、最新の配置エクスペリエンスにはまだ実装されていません。 これらの機能は推奨されていませんでした。

| **機能**                 | **説明**                                           |
|-----------------------------|-----------------------------------------------------------|
| 小売                      | Retail のサポートがまだ有効ではありません。                        |
| Trace Parser                | 実績ツールはまだサポートされていません。                         |

### <a name="features-not-intended-to-be-implemented"></a>実装が意図されていない機能
次の機能は廃止されており、最新の配置エクスペリエンスでは実装されません。

| **機能**  | **説明**                     |
|--------------|-------------------------------------|
| カスタム フォント | カスタム フォントはサポートされません。 |

