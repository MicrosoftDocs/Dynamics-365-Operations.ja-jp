---
title: コンフィギュレーション済みのシステム アカウント
description: このトピックでは、Finance and Operations 環境で事前設定されているシステム アカウントについて説明します。
author: laneswenka
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-11-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 5d56f8bede3d312c39f0619c1969607da912e4eb
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216550"
---
# <a name="preconfigured-system-accounts"></a>コンフィギュレーション済みのシステム アカウント

[!include [banner](../includes/banner.md)]

構成済みのシステム アカウントは、Microsoft が Finance and Operations サービスを管理および運用し、特定の機能をユーザーに提供できるように、配置された環境に含まれます。 次のテーブルは、アカウントの目的とユース ケースを含む、各アカウントに関する情報を示しています。  

> [!IMPORTANT] 
> システム アカウントを削除しないでください。 これらの勘定を削除すると、Microsoft が提供する主要な機能が中断されます。

| 口座の詳細 | アカウントの目的/ユース ケース|
|---|---|
| `Axrunner` | このアカウントは、環境の稼働状態を監視し、必要に応じて警告を提供するために使用されます。<br><br>**注**: このアカウントは、セルフサービス環境で非推奨になり、使用されなくなりました。 |
| `FRServiceUser` | このアカウントは Financial Reporting のユーザー アカウントで、Management Reporter アプリケーションが  Finance and Operations と統合するために使用します。 |
| `RetailServiceAccount` | このアカウントは、Retail サービスで Finance and Operations 環境に接続するために使用されます。 |
| `SysHealthServiceUser` または `Axping` (展開された製品バージョンによって異なる) | このアカウントは、環境の可用性と稼働状態を監視し、必要に応じて警告を提供するために使用されます。 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
