---
title: コンフィギュレーション済みのシステム アカウント
description: このトピックでは、Finance and Operations 環境で事前設定されているシステム アカウントについて説明します。
author: laneswenka
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
ms.author: laswenka
ms.search.validFrom: 2017-11-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: d7d429de1e263f79327ba93d7b8a890e54098b06
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096937"
---
# <a name="preconfigured-system-accounts"></a>コンフィギュレーション済みのシステム アカウント

[!include [banner](../includes/banner.md)]

構成済みのシステム アカウントは、Microsoft が Finance and Operations サービスを管理および運用し、特定の機能をユーザーに提供できるように、配置された環境に含まれます。 次のテーブルは、アカウントの目的とユース ケースを含む、各アカウントに関する情報を示しています。  

> [!IMPORTANT] 
> システム アカウントを削除しないでください。 これらの勘定を削除すると、Microsoft が提供する主要な機能が中断されます。

|                               口座の詳細                               |                                                                    アカウントの目的/ユース ケース                                                                    |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                  Axrunner                                  |                                   このアカウントは、環境の稼働状態を監視し、必要に応じて警告を提供するために使用されます。                                    |
|                               FRServiceUser                                | これは Financial Reporting のユーザー アカウントで、Management Reporter アプリケーションが  Finance and Operations と統合するために使用します。 |
|                            RetailServiceAccount                            |                              このアカウントは、Retail サービスで Finance and Operations 環境に接続するために使用されます。                              |
| SysHealthServiceUser または Axping (展開された製品バージョンによって異なる) |                           このアカウントは、環境の可用性と稼働状態を監視し、必要に応じて警告を提供するために使用されます。                           |

