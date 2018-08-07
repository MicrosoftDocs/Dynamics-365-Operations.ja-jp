---
title: "詳細な口座調整 MT940 のインポート – 複合データ エンティティのアップグレード"
description: "番号順序は、MT940 形式をサポートするために、口座取引明細書のインポート エンティティに追加する必要があります。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a76558d220e98de85060d23d6e5d8df1c0cd1baf
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>詳細な口座調整 MT940 のインポート – 複合データ エンティティのアップグレード

[!include [banner](../includes/banner.md)]

番号順序は、MT940 形式をサポートするために、口座取引明細書のインポート エンティティに追加する必要があります。 

次の手順で、口座取引明細書のインポート エンティティを MT940 形式をサポートするために追加します。

1.  以下をコンパイルして同期します:
    -   複合エンティティ\\BankStatementImportEntity
    -   Entity\\BankStatementBalanceEntity
    -   Entity\\BankStatementDocumentEntity
    -   Entity\\BankStatementEntity
    -   Entity\\BankStatementLineEntity
    -   Tables\\BankStatementStaging

2.  データ管理\\data projects.
    1.  MT940 のプロジェクトのインポートを読み込みます。
        1.  XSLT に変更します。
            -   [マップの表示]をクリックします。
            -   口座取引明細書ドキュメントの[表示のマップ]をクリックします。
            -   [変換]をクリックします。
            -   BankReconiliation-to-Composite.xslt ファイルを削除します。
            -   BankReconiliation-to-Composite.xsl の新しいバージョンを追加します。

        2.  [ソース データ] レイアウトで**番号順序**を公開します。
            1.  ソースデータ形式 = XML-Element
            2.  エンティティ名 = 口座取引明細書
            3.  データ ファイルのアップロード = 新しいバージョンの SampleBankCompositeEntity.xml
            4.  既存のファイルを上書きするには、[はい]をクリックします。
            5.  新しいマップを生成するためには、[はい]をクリックします。
            6.  [SequenceNumber] がマップされていることを確認します。
                -   明細書エンティティの[マップの表示]をクリックします。
                -   [SequenceNumber] がソースからステージングにマップされたことを確認します。

3.  新しい明細書をインポートします。





