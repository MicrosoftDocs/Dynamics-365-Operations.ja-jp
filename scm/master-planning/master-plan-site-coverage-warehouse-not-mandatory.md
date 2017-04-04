---
title: "サイト補充のマスタ プランが必要、倉庫は必須ではない"
description: "このトピックでは、サイト分析コードを品目補充用に持つ品目の計画方法について説明します。"
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 28607f0fc8db99c9fc8e96b4514763b8cf589dd8
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>サイト補充のマスタ プランが必要、倉庫は必須ではない

このトピックでは、サイト分析コードを品目補充用に持つ品目の計画方法について説明します。

このマスター計画シナリオの前提条件を次に示します。

-   サイト分析コードが必須に設定され、需要トランザクションで入力されている。
-   倉庫分析コードが必須に設定されていない。 倉庫は既知である場合もあるが、マスタ 計画計算には使用されない。
-   サイト分析コードが補充計画用に設定されている。
-   倉庫分析コードが補充計画用に設定されていない。 そのため、供給と需要はサイトごとに集計され、多分、他の補充計画分析コードも同様です。

次の図は、マスター計画がどのように進行するかを示しています。 図の中で使用されているパラメータとその設定場所を次に示します。
-   品目に対して品目補充が定義されています。 [**製品情報管理 &gt; 製品&gt; 製品のリリースされた**。 品目を選択し、[]をクリックします。**計画の &gt; 品目補充**。
-   倉庫に対して補充関係が定義されています。 [**在庫管理設定の &gt;&gt; 詳細の &gt; 在庫倉庫**。 **マスター計画**タブに、**主要倉庫**フィールド グループが表示されます。
-   既定の注文タイプは [生産]、[発注書] または [かんばん] に設定されます。 [**製品情報管理 &gt; 製品&gt; 製品のリリースされた**。 品目を選択し、[]をクリックします。**計画の &gt; 既定の注文設定**。 [**既定の注文設定**] フォームの [**既定の注文タイプ**] フィールドを参照してください。

![サイトの補充が必要、倉庫は必須ではない    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a>参照
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[マスター プラン - サイトの補充、倉庫は必須](master-plan-site-coverage-warehouse-mandatory.md)

[マスター プラン - サイトと倉庫の補充、倉庫は必須ではない](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[マスター プラン - サイトと倉庫の補充、倉庫は必須](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

- BOMバージョンを決定するかどのように[マスター プラン] (マスター プランbomバージョンdetermined.md) 


