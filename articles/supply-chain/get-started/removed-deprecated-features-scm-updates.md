---
title: Dynamics 365 Supply Chain Management の削除済みまたは推奨されない機能
description: この記事では、Dynamics 365 Supply Chain Management から削除された、または削除される予定の機能について説明します。
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 722b34e89a54715db39259549c11a78d69d2b4d3
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739873"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management の削除済みまたは推奨されない機能

[!include [banner](../includes/banner.md)]

この記事は、Dynamics 365 Supply Chain Management の新規削除または非推奨機能が文書化されると更新されます。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。

> [!NOTE]
> 財務と運用アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](/dynamics/s-e/) を参照してください。 これら異なるバージョンのレポートを比較し、財務と運用アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>Supply Chain Management 10.0.29 リリースの削除済みまたは非推奨の機能

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>移転価格が課税される在庫移動オーダー

| &nbsp;  | &nbsp;  |
|---|---|
| **廃止 / 削除の理由** | [在庫移動注文の移動価格に課税する](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)機能は、[インド向け在庫移動注文](../../finance/localizations/apac-ind-stock-transfer.md)機能に置き換わります。 |
| **別の機能で置き換えられているか?**   | はい、[在庫移動注文の移動価格に課税する](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)機能は、[インド向け在庫移動注文](../../finance/localizations/apac-ind-stock-transfer.md)機能に置き換わります。 |
| **影響を受ける製品領域** | Supply Chain Management - 在庫 |
| **配置オプション** | クラウドとオンプレミス |
| **状態** | <p>現在非推奨です。 *移動価格に課税される在庫移動注文* の機能はバグ修正やセキュリティ修正のサポートを受けられなくなります。</p><p>2023 年 4 月以降、お客様には既定で、改良機能の *インド向け在庫移動注文* をご利用いただくことになります。 2023 年 10 月以降、*移動価格に課税される在庫移動注文* 機能は使えなくなり、お客様には改良された *インド向け在庫移動注文* 機能への移行をご案内する予定です。</p><p>詳細については、[インド向け在庫移動オーダー](../../finance/localizations/apac-ind-stock-transfer.md)を参照してください。</p> |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Supply Chain Management 10.0.19 リリースの削除済みまたは非推奨の機能

### <a name="job-card-device"></a>ジョブ カード デバイス

| &nbsp;  | &nbsp;  |
|---|---|
| **廃止 / 削除の理由** | [ジョブ カード デバイス](../production-control/config-job-card-device.md) が、新しい [生産現場の実行インターフェイス](../production-control/production-floor-execution-configure.md) により置き換えられています。 |
| **別の機能で置き換えられているか?**   | はい、[ジョブ カード デバイス](../production-control/config-job-card-device.md) が、新しい [生産現場の実行インターフェイス](../production-control/production-floor-execution-configure.md) により置き換えられます。 |
| **影響を受ける製品領域** | Supply Chain Management - 製造制御 |
| **配置オプション** | クラウドとオンプレミス |
| **状態** | 非推奨。 ジョブ カード デバイスではバグとセキュリティの修正がサポートされますが、機能拡張は提供されなくなります。 2022 年 4 月以降、ジョブ カード デバイスはサポートされなくなりました。顧客は、新しい生産現場の実行インターフェイスに移動する必要があります。 |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Supply Chain Management 10.0.18 リリースの削除済みまたは非推奨の機能

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a>Supply Chain Management- 倉庫管理 (倉庫管理アプリ)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 2021 年 4 月付で、*Supply Chain Management - 倉庫管理* (倉庫管理アプリ) は廃止され、2022 年 4 月以降はサポートされません。 これで、Supply Chain Management のバージョン 10.0.17 にリリースされた *Warehouse Mobile モバイル アプリ* によって置き換えられたのです。 この新しいアプリは完全に交換するものですが、移行を容易にする基になる同じフレームワークを使用します。 必要に応じて、2 つのアプリケーションを並べて、新しいアプリの使い方をユーザーが徐々に調整できるよう支援することができます。<br><br>新しい Warehouse Management モバイル アプリについての詳細は、[Warehouse Management モバイル アプリケーション](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) と [Warehouse Management モバイル アプリのインストールと接続](../warehousing/install-configure-warehouse-management-app.md) をご覧ください。 |
| **別の機能で置き換えられているか?**   | はい、新しい Warehouse Mobile モバイル アプリによって置き換えられる必要があります。 |
| **影響を受ける製品領域**         | Supply Chain Management - 倉庫アプリ |
| **配置オプション**              | クラウドとオンプレミス |
| **状態**                         | 非推奨。 倉庫アプリではセキュリティとセキュリティ面の修正がサポートされますが、機能拡張は提供されなくなりました。 2022 年 4 月以降、古い倉庫アプリはサポートされなくなりました。顧客は、新しい Supply Chain Managementモバイル アプリに移動する必要があります。 古い倉庫アプリは、Microsoft Store と Google Play ストアから削除されます。  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Supply Chain Management 10.0.15 リリースの削除済みまたは非推奨の機能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 による Internet Explorer 11 サポートの非推奨

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。<br><br>これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。 2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。 |
| **別の機能で置き換えられているか?**   | Microsoft Edge に移行することをお勧めします。|
| **影響を受ける製品領域**         | すべての Dynamics 365 製品 |
| **配置オプション**              | All|
| **ステータス**                         | 非推奨。 2021 年 8 月以降は、Internet Explorer 11 はサポートされません。|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>製造シナリオに、組み込み型 Supply Chain Management マスター プラン エンジンを使用する

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | マスター プランの実行中のパフォーマンスを向上させ、SQLデータベースの負荷を最小化する目的で、組み込み型 Supply Chain Management マスタープラン エンジンは、プランの最適化によって置き換えられます。 プランの最適化を使用すると、オフィス時間内でも実行できる迅速な計画の実行が可能となります。 これにより、立案者は、需要またはプランのパラメーターの変更にすぐに対応できます。 |
| **別の機能で置き換えられているか?**   | 既存の組み込み Supply Chain Management 計画エンジンは、マスター計画の最適化によって置き換えられます。 |
| **影響を受ける製品領域**         | Supply Chain Management -マスター プラン |
| **配置オプション**              | クラウドのみ。 プランの最適化では、オンプレミス展開に対応していません。 |
| **状態**                         | 非推奨。 2022 年の 4 月 1 日までに、製造シナリオは組込型の Supply Chain Management マスター プラン エンジンに対してはサポートされなくなります。 その日付を以て、組み込み型計画エンジンの製造シナリオにおける有効な開発はすべて中止され、新しい機能はリリースされなくなり、重要なバグ修正のみがリリースされます。 この日付以降は、製造シナリオのサポートを必要となすべての会社がマスター プランの計算に計画の最適化を使用する必要があります。 計画の最適化では、2022 年 10 月までに製造シナリオが完全サポートされる予定です。 詳細については、[非推奨のマスター計画の概要](../master-planning/deprecated-master-planning-overview.md)を参照してください。<br><br>Supply Chain Management のオンプレミスをデプロイしている顧客は、2022 年 4 月以降の製造シナリオでは引き続き組み込み型のマスター プラン エンジンを使用することができます。 ただし、今後の機能拡張は提供されません。 |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Management 10.0.11 リリースの削除済みまたは非推奨の機能

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>配送シナリオに、組み込み型 Supply Chain Management マスター プラン エンジンを使用する

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | マスター プランの実行中のパフォーマンスを向上させ、SQLデータベースの負荷を最小化する目的で、組み込み型 Supply Chain Management マスタープラン エンジンは、プランの最適化によって置き換えられます。 プランの最適化を使用すると、オフィス時間内でも実行できる迅速な計画の実行が可能となります。 これにより、立案者は、需要またはプランのパラメーターの変更にすぐに対応できます。 |
| **別の機能で置き換えられているか?**   | 既存の組み込み Supply Chain Management 計画エンジンは、マスター計画の最適化によって置き換えられます。 |
| **影響を受ける製品領域**         | Supply Chain Management -マスター プラン |
| **配置オプション**              | クラウドのみ。 プランの最適化では、オンプレミス展開に対応していません。 |
| **ステータス**                         | 非推奨。 2021 年の 4 月 1 日までに、配布シナリオは組込型の Dynamics 365 Supply Chain Management マスター プラン エンジンではサポートされなくなります。 配分シナリオでは、顧客はマスター プランの計画にプラン最適化を使用する必要があります。 詳細については、[非推奨のマスター計画の概要](../master-planning/deprecated-master-planning-overview.md)を参照してください。 Dynamics 365 Supply Chain Management のオンプレミスの配置の顧客は、2021 年 4 月以降の配送シナリオでは引き続き Supply Chain Management のマスター プラン エンジンを使用することができます。 ただし、今後の機能拡張は提供されません。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>削除済みまたは非推奨の機能に関する以前の発表

以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

