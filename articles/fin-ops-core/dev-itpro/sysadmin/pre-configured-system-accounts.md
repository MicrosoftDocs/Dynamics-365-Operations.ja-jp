---
title: コンフィギュレーション済みのシステム アカウント
description: この記事では、財務と運用環境で事前設定されているシステム アカウントについて説明します。
author: jaredha
ms.date: 03/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2017-11-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 8c70dc94eefcd7940b1171601bf360c145be6014
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871512"
---
# <a name="preconfigured-system-accounts"></a>コンフィギュレーション済みのシステム アカウント

[!include [banner](../includes/banner.md)]

構成済みのシステム アカウントは、Microsoft が Finance and Operations サービスを管理および運用し、特定の機能をユーザーに提供できるように、配置された環境に含まれます。 次のテーブルは、アカウントの目的とユース ケースを含む、各アカウントに関する情報を示しています。  

> [!IMPORTANT] 
> システム アカウントを削除しないでください。 これらの勘定を削除すると、Microsoft が提供する主要な機能が中断されます。

| 取引先企業 | 目的/ユース ケース |
|---|---|
| Axrunner | <p>環境の状態を監視し、必要に応じて警告を提供します。</p><p>**注**: このアカウントは、セルフサービス環境で非推奨になり、使用されなくなりました。</p> |
| FRServiceUser | Financial Reporting サービスのユーザー アカウント。 Management Reporter アプリケーションでは、財務と運用アプリとの統合にこのアカウントを使用します。 |
| PowerPlatformS2S | 財務と運用アプリの二重書き込みテーブルと仮想テーブルを Microsoft Dataverse に接続します。|
| RetailServiceAccount | Retail サービスを財務と運用環境に接続します。 |
| ScaleUnitManagement | スケール ユニット マネージャー ポータルと通信します。 このアカウントは、バージョン 10.0.23 にアップグレードすると自動的に追加されます。 |
| ScaleUnitPipeline | スケール ユニット間の通信を管理および追跡します。 このアカウントは、バージョン 10.0.19 にアップグレードすると自動的に追加されます。 |
| SysHealthServiceUser または Axping (展開された製品バージョンによって異なる) | 環境の可用性と状態を監視し、必要に応じて警告を提供します。 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
