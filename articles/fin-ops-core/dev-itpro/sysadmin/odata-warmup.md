---
title: AOS 起動時に OData メタデータ キャッシュを作成する
description: この記事では、AOS 起動時に OData メタデータ キャッシュを作成する方法に関する情報を提供します。
author: hasaid
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Platform update 13
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: e4c52ccc4d45d939eba6bf3bddc1eebc004956f9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272538"
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
