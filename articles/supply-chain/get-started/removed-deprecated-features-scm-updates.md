---
title: Dynamics 365 Supply Chain Management の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Supply Chain Management から削除された、または削除される予定の機能について説明します。
author: kamaybac
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d4d2805e36f132660152370cbeee856862ad6faa
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689532"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management の削除済みまたは推奨されない機能

[!include [banner](../includes/banner.md)]

このトピックは、Dynamics 365 Supply Chain Management の新規削除または非推奨機能が文書化されると更新されます。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。

> [!NOTE]
> Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。 これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Supply Chain Management 10.0.15 リリースの削除済みまたは非推奨の機能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 による Internet Explorer 11 サポートの非推奨

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | 2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。<br><br>これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。 2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。 |
| **別の機能で置き換えられているか?**   | お客様が Microsoft Edge に移行することをお勧めします。|
| **影響を受ける製品領域**         | すべての Dynamics 365 製品 |
| **配置オプション**              | All|
| **ステータス**                         | 非推奨。 2021 年 8 月以降は、Internet Explorer 11 はサポートされません。|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>製造シナリオに、組み込み型 Supply Chain Management マスター プラン エンジンを使用する

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | マスター プランの実行中のパフォーマンスを向上させ、SQLデータベースの負荷を最小化する目的で、組み込み型 Supply Chain Management マスタープラン エンジンは、プランの最適化によって置き換えられます。 プランの最適化を使用すると、オフィス時間内でも実行できる迅速な計画の実行が可能となります。 これにより、立案者は、需要またはプランのパラメーターの変更にすぐに対応できます。 |
| **別の機能で置き換えられているか?**   | 既存の組み込み Supply Chain Management 計画エンジンは、マスター計画の最適化によって置き換えられます。 |
| **影響を受ける製品領域**         | Supply Chain Management -マスター プラン |
| **配置オプション**              | クラウドのみ。 プランの最適化では、オンプレミス展開に対応していません。 |
| **ステータス**                         | 非推奨。 2021 年 10 月 1 日までに、製造シナリオは組込型の Dynamics 365 Supply Chain Management マスター プラン エンジンではサポートされなくなります。 製造シナリオでは、顧客はマスター プランの計画にプラン最適化を使用する必要があります。 詳細については、[プランの最適化ドキュメント](https://go.microsoft.com/fwlink/?linkid=2105830) を参照してください。 Dynamics 365 Supply Chain Management のオンプレミスの配置の顧客は、2021 年 10 月以降の製造シナリオでは引き続き Supply Chain Management のマスター プラン エンジンを使用することができます。 ただし、今後の機能拡張は提供されません。 |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Management 10.0.11 リリースの削除済みまたは非推奨の機能

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>配送シナリオに、組み込み型 Supply Chain Management マスター プラン エンジンを使用する

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | マスター プランの実行中のパフォーマンスを向上させ、SQLデータベースの負荷を最小化する目的で、組み込み型 Supply Chain Management マスタープラン エンジンは、プランの最適化によって置き換えられます。 プランの最適化を使用すると、オフィス時間内でも実行できる迅速な計画の実行が可能となります。 これにより、立案者は、需要またはプランのパラメーターの変更にすぐに対応できます。 |
| **別の機能で置き換えられているか?**   | 既存の組み込み Supply Chain Management 計画エンジンは、マスター計画の最適化によって置き換えられます。 |
| **影響を受ける製品領域**         | Supply Chain Management -マスター プラン |
| **配置オプション**              | クラウドのみ。 プランの最適化では、オンプレミス展開に対応していません。 |
| **ステータス**                         | 非推奨。 2021 年の 4 月 1 日までに、配布シナリオは組込型の Dynamics 365 Supply Chain Management マスター プラン エンジンではサポートされなくなります。 配分シナリオでは、顧客はマスター プランの計画にプラン最適化を使用する必要があります。 詳細については、[プランの最適化ドキュメント](https://go.microsoft.com/fwlink/?linkid=2105830) を参照してください。 Dynamics 365 Supply Chain Management のオンプレミスの配置の顧客は、2021 年 4 月以降の配送シナリオでは引き続き Supply Chain Management のマスター プラン エンジンを使用することができます。 ただし、今後の機能拡張は提供されません。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>削除済みまたは非推奨の機能に関する以前の発表

以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]