---
title: AOS 起動時に OData メタデータ キャッシュを作成する
description: このトピックでは、AOS 起動時に OData メタデータ キャッシュを作成する方法に関する情報を提供します。
author: hasaid
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 45b767abc716b3b5d9e0a92f2c4c35881e2ca93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745969"
---
# <a name="build-odata-metadata-cache-when-the-aos-starts"></a>AOS 起動時に OData メタデータ キャッシュを作成する

[!include [banner](../includes/banner.md)]


Platform update 32 のリリースでは、最初の OData 要求が行われたときにではなく、Application Object Server (AOS) の起動時に OData メタデータ キャッシュを作成する機能が導入されました。 これにより、AOS プロセスの再起動後の最初の OData 呼び出しの応答時間が大幅に短縮されます。

このオプションは、AOS プロセスが再起動するたびに ビジネス プロセスが OData メタデータ キャッシュが作成されるのを待てない場合に役立ちます。 この機能を有効にするには、次の手順を実行します。 

1. **システム管理** \> **設定** \> **システム パラメーター** に移動します。
2. **一般 タブ** で、**AOS 起動時に OData メタデータ キャッシュを作成する** を選択し、**保存** を選択します。

> [!NOTE]
> この機能を有効にした場合は、AOS が既に実行されており、1 つの OData 要求を処理している必要があります。 これは、キャッシュが既に作成されていることを意味します。 この新しい機能は、次の AOS 再起動時に有効になります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]