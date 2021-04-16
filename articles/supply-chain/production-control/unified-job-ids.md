---
title: ジョブ ID の統合番号順序
description: この機能により、生産管理、製造の実行、および時間/出席モジュール用のジョブ ID を生成する、単一の統合番号順序が提供されます。
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824945"
---
# <a name="unified-number-sequence-for-job-ids"></a>ジョブ ID の統合番号順序

[!include [banner](../includes/banner.md)]

この機能により、生産管理、製造の実行、および時間/出席モジュール用のジョブ ID を生成する、単一の統合番号順序が提供されます。 以前は、これらのモジュールごとに異なる番号順序を選択する必要があります。これらの順序の 2 つ以上で同一の形式を使用した場合に、ジョブ ID が競合する場合があります。 このような競合によってデータが破損する可能性があります。

## <a name="turn-on-this-feature-for-your-system"></a>システムでこの機能を有効化する

このトピックで説明する機能がシステムにまだ含まれていない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*ジョブ ID の統一された番号シーケンス* 機能を有効にします。

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>ジョブ ID の統合番号シーケンスの設定

この機能を有効にすると、生産管理、製造の実行、時間/出席モジュールのパラメータ ページにある既存の **ジョブ ID** 番号シーケンス設定は廃止され、新しい **統合ジョブ ID** フィールドが追加されます。 **統合ジョブ ID** の値は 3 つのモジュールすべてで共有するため、すべてのモジュールが同じ番号順序 を参照することができます。 したがって、ジョブ ID は 3 つのモジュールすべてで一意であり、競合は発生しません。

ジョブ ID の統一番号シーケンスを設定するには:

1. 前のセクションで説明されている手順に従って機能を有効にします。
1. 統合ジョブの ID に使用する番号順序を識別するか、新しい番号シーケンスを作成します。 詳細については、[番号順序の概要](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)を参照してください。
1. **生産管理パラメータ**、**製造の実行パラメータ**、または **時間と出席 パラメータ** ページに移動 します。 これらのページでこの設定を行う場合、他のすべてのページが自動的に更新されるので、どちらを選択しても問題ではありません。
1. パラメータ ページの **番号シーケンス** タブを開きます。
1. 前に特定した **番号シーケンスコード** をグリッドの **統合したジョブ ID** 行に割り当てます。
