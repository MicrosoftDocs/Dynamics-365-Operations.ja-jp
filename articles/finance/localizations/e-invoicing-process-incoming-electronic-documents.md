---
title: 受信した電子ドキュメントの処理
description: このトピックでは、受信した電子ドキュメントの処理の概要を示します。
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9701367e1ba1f9dbd1e53deb863c10af4213a359
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371605"
---
# <a name="processing-of-incoming-electronic-documents"></a>受信した電子ドキュメントの処理

[!include [banner](../includes/banner.md)]

受信した電子ドキュメント (仕入先電子請求書など) は、次の 2 つの方法でインポートおよび処理できます:

- ファイルは外部チャネルから取得され、接続されたアプリケーションに直接渡されます。 そこで、追加の変換が行われ、データベースにインポートされます。
- ファイルは電子請求サービスで事前処理され、接続されたアプリケーションに渡されます。

電子請求では、受信したドキュメント (メールと Microsoft SharePoint のフォルダー) に対して 2 つのチャネルをサポートします。

ドキュメントを事前処理するか、接続されたアプリケーションに直接渡すかを指定する、2 つの設定タイプがあります:

- **データ チャネル** – システムは、接続されたアプリケーションにドキュメントを直接渡します。
- **処理パイプラインを有するデータ チャネル** – 接続されたアプリケーションにドキュメントが渡される前に実行される追加のアクションを設定できます。

異なるチャネルの受信した電子ドキュメントを処理するためのシナリオを設定する方法については、[メール チャネルの構成](e-invoicing-configure-email.md) と [SharePoint チャネルの構成](e-invoicing-configure-sharepoint-channel.md) を参照してください。
