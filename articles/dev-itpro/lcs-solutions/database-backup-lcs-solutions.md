---
title: "LCS ソリューション データベースのバックアップ"
description: "LCS ソリューション パッケージには、Finance and Operations のデータベース バックアップが必要です。 データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。 これは、販売前のデモ展開に使用されます。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 6736f40192130a45a3c115e1183b3f11f0d0819f
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="back-up-database-for-an-lcs-solution"></a>LCS ソリューション データベースのバックアップ

[!include [banner](../includes/banner.md)]

LCS ソリューション パッケージには、Finance and Operations のデータベース バックアップが必要です。 データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。 これは、販売前のデモ展開に使用されます。 

デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。 データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。 データベースが大きい場合、Lifecycle Services (LCS) で<strong>アセット ライブラリ**にデータベースをアップロードしようとすると、タイムアウト エラーが発生する場合があります。データベース バックアップを圧縮するには、SQL Server Management Studio で、**データベースのバックアップ</strong> ページの<strong>バックアップ圧縮の設定</strong>フィールドで、<strong>バックアップの圧縮</strong>を選択します。 

[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)

<a name="additional-resources"></a>その他のリソース
--------

[AppSource 向け LCS ソリューション ホームページ](lcs-solutions-app-source.md)




