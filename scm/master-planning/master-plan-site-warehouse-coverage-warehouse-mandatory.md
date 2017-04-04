---
title: "サイトと倉庫の補充倉庫は、のマスタ プラン"
description: "このトピックでは、サイトおよび倉庫の補充分析コードを持つ品目の計画方法について説明します。 倉庫分析コードは必須です。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a0931d88f84544160803e42466575c02f47588a4
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>サイトと倉庫の補充倉庫は、のマスタ プラン

このトピックでは、サイトおよび倉庫の補充分析コードを持つ品目の計画方法について説明します。 倉庫分析コードは必須です。

このマスター計画シナリオの前提条件を次に示します。

-   サイト分析コードが必須に設定され、需要トランザクションで入力されている。
-   倉庫分析コードが必須に設定され、需要トランザクションで入力されている。
-   サイト分析コードおよび倉庫分析コードが補充計画用に設定されている。 他の分析コードが補充計画に対して設定されている場合もある。 ただし、これらはマルチサイト機能の影響を受けない。

次の図は、マスター計画がどのように進行するかを示しています。 図の中で使用されているパラメータとその設定場所を次に示します。
-   The warehouse is set to **Manual**. [**在庫管理設定の &gt;&gt; 詳細の &gt; 在庫倉庫**。 [**マスター計画**] クイック タブに、[**手動**] フィールドが表示されます。
-   品目に対して品目補充が定義されています。 [**製品情報管理 &gt; 製品&gt; 製品のリリースされた**。 [品目を、アクション ウィンドウで、**計画**]タブで、[**品目補充**選択します。
-   倉庫に対して補充関係が定義されています。 [**在庫管理設定の &gt;&gt; 詳細の &gt; 在庫倉庫**。 [**マスター計画**] クイック タブに、[**主要倉庫**] フィールド グループが表示されます。
-   既定の注文タイプには [生産]、[発注書] または [かんばん] が設定されます。 [**製品情報管理 &gt; 製品&gt; 製品のリリースされた**。 [品目を、アクション ウィンドウで、**計画**]タブで、[**既定の注文設定**選択します。 [**既定の注文設定**] フォームの [**既定の注文タイプ**] を参照してください。

![サイトと倉庫の補充が必要、倉庫は必須    ](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a>参照
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[マスター プラン - サイトの補充、倉庫は必須](master-plan-site-coverage-warehouse-mandatory.md)

[マスター プラン - サイトの補充、倉庫は必須ではない](master-plan-site-coverage-warehouse-not-mandatory.md)

[マスター プラン - サイトと倉庫の補充、倉庫は必須ではない](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[マスター プラン - BOM バージョンを決定する方法](master-plan-bom-version-determined.md)


