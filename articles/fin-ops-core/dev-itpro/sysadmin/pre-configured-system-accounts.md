---
title: コンフィギュレーション済みのシステム アカウント
description: このトピックでは、Finance and Operations 環境で事前設定されているシステム アカウントについて説明します。
author: manalidongre
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2017-11-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 73e884dee31f5e1978e25fe1bef962dde7984cac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191796"
---
# <a name="preconfigured-system-accounts"></a>コンフィギュレーション済みのシステム アカウント

[!include [banner](../includes/banner.md)]

構成済みのシステム アカウントは、Microsoft が Finance and Operations サービスを管理および運用し、特定の機能をユーザーに提供できるように、配置された環境に含まれます。 次のテーブルは、アカウントの目的とユース ケースを含む、各アカウントに関する情報を示しています。  

> [!IMPORTANT] 
> システム アカウントを削除しないでください。 これらの勘定を削除すると、Microsoft が提供する主要な機能が中断されます。

|                               口座の詳細                               |                                                                    アカウントの目的/ユース ケース                                                                    |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                  Axrunner                                  |                                   このアカウントは、環境の稼働状態を監視し、必要に応じて警告を提供するために使用されます。                                    |
|                               FRServiceUser                                | これは財務諸表サービスのユーザー アカウントで、Management Reporter アプリケーションが Finance and Operations と統合するために使用します。 |
|                            RetailServiceAccount                            |                              このアカウントは、Retail サービスで Finance and Operations 環境に接続するために使用されます。                              |
| SysHealthServiceUser または Axping (展開された製品バージョンによって異なる) |                           このアカウントは、環境の可用性と稼働状態を監視し、必要に応じて警告を提供するために使用されます。                           |

