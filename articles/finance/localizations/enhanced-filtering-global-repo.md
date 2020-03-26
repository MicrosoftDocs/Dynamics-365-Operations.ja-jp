---
title: RCS/グローバル レポジトリの拡張フィルター処理
description: このトピックでは、追加フィルターを含むように改善された RCS グローバル レポジトリの拡張フィルター処理機能について説明します。
author: JaneA07
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ed5a217b8844bfc76d53370ab4c4c339f5bece36
ms.sourcegitcommit: 0dcdfedec7125562f6b33deb009a3e044a1243eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2020
ms.locfileid: "3099870"
---
# <a name="enhanced-filtering-options-for-finding-configurations-in-the-global-repository"></a>グローバル レポジトリのコンフィギュレーション検索のための拡張フィルター処理オプション

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、次のフィルターを含むように改善された、Regulatory Configuration Services (RCS) グローバル レポジトリの拡張フィルター処理機能について説明します。 
- **国/地域** - ISO 国コードに基づく  
- **タグ** - 機能/機能領域 ; 業種 ; ビジネス ドキュメント タイプ用 

個別にまたはグループ別のいずれかでフィルターを適用して、特定または関連するコンフィギュレーションを検索できます。 たとえば、仕入先請求書に関連したすべてのコンフィギュレーション可能なビジネス ドキュメントを検索するには、**ビジネス ドキュメント タイプ** フィルターを適用できます。 

国コードを選択して、**フィルターを適用する**をクリックすることによってさらに絞り込んだ検索ができます。  

[![グローバル レポジトリのフィルター セクション](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

次の例では、**ビジネス ドキュメント タイプ**でフィルター処理した場合の結果を表示します。 

[![フィルターを適用してビジネス ドキュメント タイプをインポートする](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

フィルター処理された結果は、ユーザー RCS または Dynamics 365 Finance 環境に、個別にまたは (コンフィギュレーションのグループを選択することによって) セットとして**インポート**をクリックしてインポートできます。






