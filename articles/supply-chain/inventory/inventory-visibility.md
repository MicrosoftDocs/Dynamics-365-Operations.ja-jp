---
title: 在庫の可視化アドイン概要
description: このトピックでは、在庫の可視化とその機能について説明します。
author: yufeihuang
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dfc1bc0d457d0b0b2632aa2e2e5ba6a3c2f3fae7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575174"
---
# <a name="inventory-visibility-add-in-overview"></a>在庫の可視化アドイン概要

[!include [banner](../includes/banner.md)]

在庫の可視化アドイン (*在庫の可視化* とも呼ばれる) は、リアルタイムで手持在庫の追跡を可能にする独立したスケーラブルなマイクロサービスです。 そのため、在庫をグローバルに表示できます。

外部システムは、RESTful API を使用してサービスにアクセスします。 この方法で、特定の分析コード セットに関する手持在庫情報を入手するか、カスタマイズされた別のデータ ソースで在庫を変更することができます。

Microsoft Dataverse に構築されるマイクロサービスとして、在庫の可視化は拡張性を提供します。 Power Apps を使用してアプリを作成できます。 Power BI を適用して、業務要件を満たすカスタマイズされた機能を提供することもできます。

標準化された在庫分析コードの構成オプションを設定し、トランザクション タイプを設定することにより、在庫の可視化を複数のサードパーティ システムと統合できます。 在庫の可視化では、構成できる計算済の数量によってカスタマイズされた拡張性もサポートされます。

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management を使用した在庫の可視化統合

統合ソリューションは、Dynamics 365 Supply Chain Management から在庫データを取得し、在庫変更を継続的に追跡します。 詳細については、[在庫視覚化統合のインストールと設定](inventory-visibility-setup.md)および[在庫視覚化のコンフィギュレーション](inventory-visibility-configuration.md)を参照してください。

## <a name="get-a-global-view-of-inventory"></a>在庫のグローバル表示の取得

統合ソリューションを使用すると、独自のデータ ソースを定義し、在庫データを集中管理できます。 詳細については、[在庫視覚化のコンフィギュレーション](inventory-visibility-configuration.md)を参照してください。

在庫を表示するには 2 つの方法があります。

- 高性能な API を使用してクエリを送信します。 この API は、凖リアルタイムの在庫データをキャッシュされたインスタンスから直接返します。 契約およびサンプルは、[在庫の可視化のパブリック API](inventory-visibility-api.md) で確認できます。
- 手持在庫リストを表示します。 このリストは、定期的にキャッシュされたインスタンスと同期され、Dataverse で表示されます。 詳細については、[在庫の可視化アプリ](inventory-visibility-power-platform.md) を参照してください。

## <a name="soft-reservations"></a>仮引当

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

仮引当は、過剰販売を回避する販売注文のフルフィルメントなど、サポートする特定の数量の製品をビジネスが引当する必要がある場合に適用されます。 Supply Chain Management または他の注文管理システムで販売注文が作成および確認されると、数量を引当する要求が在庫の可視化に送信されます。 在庫の可視化により、分析コードの詳細および特定の在庫トランザクション タイプを持つ製品の引当を行うことができます。 (詳細については、[在庫の可視化アプリ](inventory-visibility-power-platform.md) を参照してください。) 数量が正常に引当されると、引当 ID が返されます。 この引当 ID を使用して、Supply Chain Management または他の注文管理システムの元の注文にリンクすることができます。

この機能は、在庫の可視化の引当によって合計数量が変わらないように設計されています。 代わりに、引当済数量にフラグするのみです。 (この理由から、*仮引当* と呼ばれます。) 製品が Supply Chain Management またはサード パーティのシステムで消費される場合、数量控除を行い、在庫の可視化で合計数量を更新するため API を再び呼び出すことによって、仮引当済の数量をオフセットできます。 詳細については、[在庫の視覚化引当](inventory-visibility-reservations.md) を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
