---
title: 財務と運用アプリのデータベースのバックアップ
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージに必要なデータベースのバックアップに関する情報を提供します。
author: sericks007
ms.date: 04/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.custom: 196833
ms.assetid: fc0f06e8-1a20-45f7-ae98-ee074fe1f030
ms.openlocfilehash: bc5df2c0635c63bea285c534724ca5b22ca63d17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270735"
---
# <a name="back-up-the-databases-for-finance-and-operations-apps"></a>財務と運用アプリのデータベースのバックアップ

[!include[banner](../includes/banner.md)]

財務と運用アプリのデータベースのバックアップは、Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージに必要です。 データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。 このデータは販売前のデモ展開に使用されます。

デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。 データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。 それ以外の場合は 、LCS でアセット ライブラリにデータベースをアップロードしようとすると、タイムアウト エラーが発生する可能性があります。 

Microsoft SQL Server Management Studio で、データベースのバックアップを圧縮するには、**データベースのバックアップ** ページの **バックアップ圧縮を設定** フィールドで、**バックアップの圧縮** を選択します。

[![セット バックアップ圧縮フィールドで選択されたバックアップを圧縮。](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)

## <a name="additional-resources"></a>追加リソース

[AppSource でアプリを公開するための要件](lcs-solutions-app-source.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

