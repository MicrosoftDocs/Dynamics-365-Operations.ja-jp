---
title: Commerce Data Exchange パッケージをプライマリ インデックスで並べ替える
description: このトピックでは、Dynamics 365 Commerce 機能の概要を提供し、パッケージごとのプライマリ インデックスで Commerce Data Exchange (CDX) パッケージを並べ替えます。
author: jashanno
ms.date: 08/24/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: jashanno
ms.search.validFrom: 2021-08-24
ms.openlocfilehash: 12cd6b72339a3560436b98615b16828cbb53ab48
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674320"
---
# <a name="sort-commerce-data-exchange-packages-by-primary-index"></a>Commerce Data Exchange パッケージをプライマリ インデックスで並べ替える

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Commerce 機能の概要を提供し、パッケージごとのプライマリ インデックスで Commerce Data Exchange (CDX) パッケージを並べ替えます。 **プライマリ インデックス機能による CDX パッケージの並べ替え** 機能では、データ変換の前処理パフォーマンスを最適化します。 この機能は、Commerce Scale Unit (CSU) または Modern POS のオフライン データベースのデータ アプリケーション ロジックを変更したり、それらのコンポーネントのパフォーマンスを向上したりしない点に注意が必要です。

## <a name="prerequisites"></a>必要条件

**プライマリ インデックスによる CDX パッケージの並べ替え** 機能は、**機能管理** ワークスペースでオンにする必要があります。 詳細については [機能管理の概要](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。

## <a name="feature-value"></a>機能の値

この機能により、Digital Commerce、Headless Commerce または Dynamics 365 Commerce (Dataverse が使われている場合) で Micrsoft Dataverse を使用する場合は、追加パフォーマンスが提供されます。

## <a name="using-this-feature"></a>この機能の使用

この機能は、**機能管理** でオンになった後、エンド ユーザーに対する可視性なしに機能します。
