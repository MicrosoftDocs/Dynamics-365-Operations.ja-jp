---
title: チャネル設定の前提条件
description: このトピックでは、Microsoft Dynamics 365 Commerce のチャネル設定の前提条件における概要を示します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002292"
---
# <a name="channel-setup-prerequisites"></a>チャネル設定の前提条件


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のチャネル設定の前提条件における概要を示します。

## <a name="overview"></a>概要

Dynamics 365 Commerce チャネルを作成する前に、いくつかの前提条件タスクを完了しておく必要があります。 次の前提条件タスクの一覧は、チャネル タイプ別にまとめられています。

> [!NOTE]
> 一部のドキュメントはまだ作成中であり、新しいコンテンツが公開されるとリンクは更新されます。

## <a name="initialization"></a>初期化

- [シード データの初期化](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>すべてのチャネル タイプに必要であるグローバルな前提条件

- [法人構造の定義とコンフィギュレーション](channels-legal-entities.md) 
- [組織階層のコンフィギュレーション](channels-org-hierarchies.md)
- [倉庫の設定](channels-setup-warehouse.md)
- [消費税のコンフィギュレーション](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [電子メール通知プロファイルの設定](email-notification-profiles.md)
- [番号順序の設定](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [既定の顧客およびアドレス帳の設定](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>小売チャネルの前提条件

- [情報コードおよび情報コード グループ](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [小売機能プロファイルの設定](retail-functionality-profile.md)
- [従業員のアドレス帳の設定](new-address-book.md)
- [画面レイアウトの設定](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [ハードウェア ステーションの設定](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>コール センター チャネルの前提条件

- コール センター パラメーター
- コール センターの払戻方法
- レンタル タイプ
- 支払サービス
- 注文保留コード

## <a name="online-channel-prerequisites"></a>オンライン チャネルの前提条件

- [オンライン機能プロファイルの作成](online-functionality-profile.md)

## <a name="additional-resources"></a>追加リソース

[チャネルの概要](channels-overview.md)

[組織と組織階層の概要](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[組織階層の設定](channels-org-hierarchies.md)

[法人の作成](channels-legal-entities.md)

[小売チャネルの設定](channel-setup-retail.md)
    
[オンライン チャネルの設定](channel-setup-online.md)
