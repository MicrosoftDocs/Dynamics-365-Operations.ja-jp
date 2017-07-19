---
title: "マスター プラン - サイトの補充、倉庫は必須"
description: "このトピックでは、補充分析コードとしてサイトを持つ品目の計画方法について説明します。 倉庫は必須の分析コードです。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a1bf8f2253c63e4b6ca8fee02ec6b1cfb8aad73c
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>マスター プラン - サイトの補充、倉庫は必須

[!include[banner](../includes/banner.md)]


このトピックでは、補充分析コードとしてサイトを持つ品目の計画方法について説明します。 倉庫は必須の分析コードです。

このマスター計画シナリオの前提条件を次に示します。

-   サイト分析コードが必須に設定され、需要トランザクションで入力されている。 この設定は変更できません。
-   倉庫分析コードが必須に設定され、需要トランザクションで入力されている。
-   サイト分析コードが補充計画用に設定されている。 他の分析コードが補充計画に対して設定されている場合もある。 ただし、これらはマルチサイト機能の影響を受けない。
-   倉庫分析コードが補充計画用に設定されていない。 そのため、供給と需要はサイトごとに集計され、多分、他の補充計画分析コードも同様です。

次の図は、マスター計画がどのように進行するかを示しています。 図の中で使用されているパラメータとその設定場所を次に示します。
-   品目に対して品目補充が定義されています。 [**製品情報管理] &gt; [製品] &gt; [リリースされた製品**] の順にクリックします。 品目を選択し、[**計画] &gt; [品目補充**] の順にクリックします。
-   倉庫に対して補充関係が定義されています。 [**在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫**] の順にクリックします。 **マスター計画**タブに、**主要倉庫**フィールド グループが表示されます。
-   既定の注文タイプには [生産]、[発注書] または [かんばん] が設定されます。 [**製品情報管理] &gt; [製品] &gt; [リリースされた製品**] の順にクリックします。 品目を選択し、[**計画] &gt; [既定の注文設定**] の順にクリックします。 [**既定の注文設定**] フォームの [**既定の注文タイプ**] を参照してください。

![サイトの補充が必要、倉庫は必須    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a>参照
--------

[マスター プランとマルチサイト機能](master-plan-multisite-functionality.md)

[マスター プラン - サイトと倉庫の補充、倉庫は必須](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[マスター プラン - サイトの補充、倉庫は必須](master-plan-site-coverage-warehouse-mandatory.md)

[マスター プラン - サイトと倉庫の補充、倉庫は必須ではない](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[マスター プラン - BOM バージョンを決定する方法](master-plan-bom-version-determined.md)




