---
title: Dataverse で財務と運用の仮想テーブルの変更を追跡する (プレビュー)
description: この記事では、Microsoft Dataverse で財務と運用の仮想テーブルの追跡変更を有効にする方法について説明します。
author: peakerbl
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2022-10-10
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 77412f9e5c248f029e6fe78814fcaa4b0b84f4fd
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690368"
---
# <a name="track-changes-for-finance-and-operations-virtual-tables-in-dataverse-preview"></a>Dataverse で財務と運用の仮想テーブルの変更を追跡する (プレビュー) 

[!include[banner](../includes/banner.md)]

[このトピックは、プレリリース ドキュメントであり、変更される場合があります。]

## <a name="row-version-change-tracking-for-finance-and-operations"></a>財務と運用の行バージョン変更追跡

財務と運用アプリに新しい変更追跡オプションが追加され、Microsoft Dataverse を使用したデータの増分同期が有効になりました。 新しい変更追跡は、データ アーカイブ、Synapse Analytics 統合、モバイル オフライン、関連検索など、複数の機能に対する必要条件です。 目標は、Dataverse 同期サービスに基づいて、既存する財務と運用のデータ同期フレームワークすべてを一つに統合することです。

## <a name="prerequisite-to-track-changes-for-finance-and-operations-virtual-tables-in-dataverse"></a>Dataverse で財務と運用の仮想テーブルの変更を追跡するため必要条件 

track-changes-fin-ops-virtual-table.md)
- **行バージョン Change Tracking を許可** メタデータ プロパティは、データ エンティティに対して **はい** に設定する必要があります。詳細は [データ エンティティに対する行バージョンの変更追跡](../data-entities/rowversion-change-track.md) を参照してください
- 財務と運用エンティティは、Dataverse で表示される必要があります。詳細は、[Microsoft Dataverse 仮想エンティティを有効にする](enable-virtual-entities.md)を参照してください
 
 ## <a name="track-changes-for-finance-and-operations-virtual-tables-in-dataverse"></a>Dataverse で財務と運用の仮想テーブルの変更を追跡する 

上記の必要条件を満している場合、最後の手順は、Power Apps の仮想テーブルに対する **変更追跡** を選択して変更の追跡を有効にすることです。詳しくは、[変更追跡を有効にしてデータ同期をコントロールする](/power-platform/admin/enable-change-tracking-control-data-synchronization.md) を参照してください。

> [!IMPORTANT]
> - このプレビュー機能は、Microsoft Power Platform 統合が Dataverse データベースで有効になっているリリース 10.0.31 で使用することができます。詳細は、[Microsoft Power Platform 統合を有効にする](/power-platform/enable-power-platform-integration.md) を参照してください。 有効にする方法については、[プレビュー機能とは？プレビュー機能を有効にするには？](/power-platform/edit/main/power-platform/admin/what-are-preview-features-how-do-i-enable-them.md) を参照してください。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
