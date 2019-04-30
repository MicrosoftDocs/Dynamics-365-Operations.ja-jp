---
title: 中国金税データ エンティティのインポート
description: このトピックでは、中国金税データ エンティティを Microsoft Dynamics 365 for Finance and Operations にインポートする方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr
audience: IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261394
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c957ec8ddc91a59b5b52c3f596a6037379f48b28
ms.sourcegitcommit: b5e2835e2245414837b7b37056af228dd000f756
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/20/2019
ms.locfileid: "879864"
---
# <a name="import-the-chinese-golden-tax-data-entity"></a>中国金税データ エンティティのインポート

[!include [banner](../includes/banner.md)]
  
このトピックでは、中国金税データ エンティティを Microsoft Dynamics 365 for Finance and Operations にインポートする方法について説明します。

> [!NOTE] 
> Dynamics 365 for Finance and Operations の10.0以降のバージョンでは、中国で使用されている金税システムのデータ エンティティをインポートする必要はありません。 

中国金税データ エンティティをインポートするには、以下の手順を実行します。

1.  **システム管理** &gt; **データ管理** の順に移動します。
2.  **インポート** タイルをクリックして新しいインポート プロジェクトを作成します。
3.  プロジェクトの名前を入力します。
4.  ソース データ形式 **XML-Element** を選択します。
5.  **エンティティ名** フィールドで、**税の統合されたインポート** エンティティを選択します。
6.  アップロードをクリックしてから、金税データ ファイルの場所を参照します。
7.  **マップの表示** を **税の統合されたインポート** タイルでクリックします。
8.  **変換** タブで、**新規** をクリックします。
9.  **ファイルのアップロード** をクリックして .xlst ファイルの場所を参照します。

データ エンティティのインポート方法を示す特定の手順については、[エンティティを使用したデータのインポート](../../dev-itpro/data-entities/build-consuming-data-entities.md)を参照してください。 デモ データ会社 CNMF を使用して中国金税データ エンティティのインポートを実行するには、以下のファイルを [CustomerSource](https://mbs.microsoft.com/customersource/global/ax/learning/samplefilestaximportchina) からダウンロードします。

-   **ImportSampleFile.xml** - このファイルは中国金税データ エンティティ複合です。
-   **Tax-Import-to-XML.xslt** - このファイルは変換ファイル マッピングとして使用されます。

次のスクリーン ショットは、中国金税データ エンティティのマッピングのビジュアル化例を示します。 [![この画像は中国金税データ エンティティのマッチングのビジュアル化例を示します。](./media/goldentaximportmappingvisualization.png)](./media/goldentaximportmappingvisualization.png)      

詳細については、[金税統合エクスポートの設定](./tasks/golden-tax-integration-export-setup.md)を参照してください。

