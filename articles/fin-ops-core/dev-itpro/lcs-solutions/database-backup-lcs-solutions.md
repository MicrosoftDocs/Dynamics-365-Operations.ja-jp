---
title: Finance and Operations アプリのデータベースのバックアップ
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージに必要なデータベースのバックアップに関する情報を提供します。
author: kfend
ms.date: 04/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 196833
ms.assetid: fc0f06e8-1a20-45f7-ae98-ee074fe1f030
ms.search.region: Global
ms.author: omarc
ms.openlocfilehash: b7edc94ea71c2a72a064c100db2590b23df20f8e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750354"
---
# <a name="back-up-the-databases-for-finance-and-operations-apps"></a>Finance and Operations アプリのデータベースのバックアップ

[!include[banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージには、Finance and Operations アプリ データベースのバックアップが必要です。 データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。 このデータは販売前のデモ展開に使用されます。

デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。 データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。 それ以外の場合は 、LCS でアセット ライブラリにデータベースをアップロードしようとすると、タイムアウト エラーが発生する可能性があります。 

Microsoft SQL Server Management Studio で、データベースのバックアップを圧縮するには、**データベースのバックアップ** ページの **バックアップ圧縮を設定** フィールドで、**バックアップの圧縮** を選択します。

[![セット バックアップ圧縮フィールドで選択されたバックアップを圧縮](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)

デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。 データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。 データベースが大きい場合、Lifecycle Services (LCS) のアセットライブラリにデータベースをアップロードする際に、タイムアウトエラーが発生することがあります。 
  
SQL Server Management Studio で、データベースのバックアップを圧縮するには、 **データベースのバックアップ** ページの **バックアップ圧縮を設定する** フィールドで、 **バックアップを圧縮する** を選択します。 

[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)

## <a name="additional-resources"></a>追加リソース

[AppSource でアプリを公開するための要件](lcs-solutions-app-source.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]