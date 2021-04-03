---
title: チャネル設定の前提条件
description: このトピックでは、Microsoft Dynamics 365 Commerce のチャネル設定の前提条件における概要を示します。
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 270f751e860e56a03e20df720c088f275d0298e7
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477927"
---
# <a name="channel-setup-prerequisites"></a>チャネルの設定の前提条件

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のチャネル設定の前提条件における概要を示します。

Dynamics 365 Commerce チャネルを作成する前に、いくつかの前提条件タスクを完了しておく必要があります。 次の前提条件タスクの一覧は、チャネル タイプ別にまとめられています。

> [!NOTE]
> 一部のドキュメントはまだ作成中であり、新しいコンテンツが公開されるとリンクは更新されます。

## <a name="initialization"></a>初期化

- [シード データの初期化](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>すべてのチャネル タイプに必要であるグローバルな前提条件

- [法人構造の定義とコンフィギュレーション](channels-legal-entities.md) 
- [組織階層のコンフィギュレーション](channels-org-hierarchies.md)
- [倉庫の設定](channels-setup-warehouse.md)
- [消費税のコンフィギュレーション](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [電子メール通知プロファイルの設定](email-notification-profiles.md)
- [番号順序の設定](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [既定の顧客およびアドレス帳の設定](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>小売チャネルの前提条件

- [情報コードおよび情報コード グループ](info-codes-retail.md)
- [小売機能プロファイルの設定](retail-functionality-profile.md)
- [従業員のアドレス帳の設定](new-address-book.md)
- [画面レイアウトの設定](pos-screen-layouts.md)
- [ハードウェア ステーションの設定](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>コール センター チャネルの前提条件

- コール センター パラメーター
- [通話センター注文と払戻支払の方法](work-with-payments.md)
- [デリバリーのコール センター モードと諸費用](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>オンライン チャネルの前提条件

- [オンライン機能プロファイルの作成](online-functionality-profile.md)

## <a name="additional-resources"></a>追加リソース

[チャネルの概要](channels-overview.md)

[組織と組織階層の概要](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[組織階層の設定](channels-org-hierarchies.md)

[法人の作成](channels-legal-entities.md)

[小売チャネルの設定](channel-setup-retail.md)
    
[オンライン チャネルの設定](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
