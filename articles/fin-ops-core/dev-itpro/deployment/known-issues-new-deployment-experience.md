---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: rashmansur
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: ebeb9584904cc749f5b5a2f3891f851a72d76591
ms.sourcegitcommit: 3fa1e8583003a90ba486f757c3826b139e1b3f73
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421567"
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

## <a name="finance-and-operations-apps"></a>Finance and Operations アプリ 

> [!NOTE]
> Dynamics 365 Commerce は、10.0.10 リリースを使用した最新の配置エクスペリエンスに実装されています。 詳細については、[セルフサービス配置でのアプリケーション エクスプローラー用支払パッケージの作成](../../../commerce/dev-itpro/payment-connector-package.md)を参照してください。

### <a name="features-not-intended-to-be-implemented"></a>実装が意図されていない機能
次の機能は廃止されており、最新の配置エクスペリエンスでは実装されません。

| **機能**  | **説明**                     |
|--------------|-------------------------------------|
| カスタム フォント | カスタム フォントはサポートされません。 詳細については、[Dynamics 365 アプリケーションのドキュメント レポート サービス](../analytics/reporting-experience-iias-environments.md)を参照してください。

> [!NOTE]
> 非推奨の機能の詳細については、[削除済みまたは非推奨のプラットフォーム機能](../get-started/removed-deprecated-features-platform-updates.md)、[以前のリリースからの削除済みおよび非推奨の機能](../migration-upgrade/deprecated-features.md)、[以前のリリースの削除済みおよび非推奨の機能](../get-started/removed-deprecated-features-platform-updates.md)を参照してください。
