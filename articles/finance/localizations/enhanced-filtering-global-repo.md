---
title: RCS/グローバル レポジトリの強化されたフィルター処理
description: このトピックでは、追加フィルターを含むように改善された RCS グローバル レポジトリの拡張フィルター処理機能について説明します。
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a67a4345271cbeffc100fc1d9077cc866846a4d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005845"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>RCS では、RCS/グローバル リポジトリで構成を見つけるフィルタリング オプションを強化しました

[!include [banner](../includes/banner.md)]

このトピックでは、次のフィルターを含むように改善された、Regulatory Configuration Services (RCS) グローバル レポジトリの拡張フィルター処理機能について説明します： 
- **国/地域** ― ISO 国コードに基づく  
- **タグ** 次のタイプ：
  - 職務分野
  - 機能領域
  - 業界 
  - ビジネス ドキュメント 

特定の構成や関連する構成を見つけやすくするために、個別に、またはグループとしてフィルタを適用することができます。 例えば、「仕入先請求書に関連する構成可能なビジネス文書」という単一のタイプの文書を検索するには、**ビジネス ドキュメント タイプ** のフィルタを適用することで、そのタイプの文書を検索することができます。 

[![グローバル レポジトリのフィルター セクション](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

[仕入先請求書] などのドキュメントタイプを選択し、**フィルターの適用** をクリックすることで、検索をさらに絞り込むことができます。 次の例では、**ビジネス ドキュメント タイプ** でフィルター処理した場合の結果を表示します。 

[![フィルターを適用してビジネス ドキュメント タイプをインポートする](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

フィルタ処理された結果は、個別に、またはセットとして、ユーザーの RCS リポジトリまたは Dynamics 365 Finance 環境にインポートできます。 これを行うには、構成のグループを選択し、**インポート** をクリックします。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]