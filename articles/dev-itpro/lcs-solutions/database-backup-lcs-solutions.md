---
title: "Microsoft Dynamics 365 for Finance and Operations ソリューションに対するデータベースをバックアップ"
description: "このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージに必要なデータベースのバックアップに関する情報を提供します。"
author: kfend
manager: AnnBe
ms.date: 04/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Lifecycle Services
ms.custom: 196833
ms.assetid: fc0f06e8-1a20-45f7-ae98-ee074fe1f030
ms.search.region: Global
ms.author: omarc
ms.translationtype: HT
ms.sourcegitcommit: 43c18efc4b02da594821018b6d4b8748a4f5eb84
ms.openlocfilehash: 10fbb6aa3c68a5a6c0873feac7d5b5d51d39866a
ms.contentlocale: ja-jp
ms.lasthandoff: 06/12/2018

---

# <a name="back-up-the-database-for-a-microsoft-dynamics-365-for-finance-and-operations-solution"></a>Microsoft Dynamics 365 for Finance and Operations ソリューションに対するデータベースをバックアップ

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations データベースのバックアップが、Microsoft Dynamics Lifecycle Services (LCS) のソリューション パッケージには必要です。 データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。 このデータは販売前のデモ展開に使用されます。

デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。 データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。 それ以外の場合は 、LCS でアセット ライブラリにデータベースをアップロードしようとすると、タイムアウト エラーが発生する可能性があります。 Microsoft SQL Server Management Studio で、データベースのバックアップを圧縮するには、**データベースのバックアップ** ページの**バックアップ圧縮を設定**フィールドで、**バックアップの圧縮**を選択します。

<a name="compress-backup-selected-in-the-set-backup-compression-fieldmediadatabasebackup01jpgmediadatabasebackup01jpg"></a>[![セット バックアップ圧縮フィールドで選択されたバックアップを圧縮](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)
=======
デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。 データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。 データベースが大きい場合、Lifecycle Services (LCS) で<strong>アセット ライブラリ**にデータベースをアップロードしようとすると、タイムアウト エラーが発生する場合があります。データベース バックアップを圧縮するには、SQL Server Management Studio で、**データベースのバックアップ</strong> ページの<strong>バックアップ圧縮の設定</strong>フィールドで、<strong>バックアップの圧縮</strong>を選択します。 

[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)

<a name="additional-resources"></a>その他のリソース
--------

[AppSource の Dynamics 365 for Finance and Operations アプリを公開](lcs-solutions-app-source.md)

