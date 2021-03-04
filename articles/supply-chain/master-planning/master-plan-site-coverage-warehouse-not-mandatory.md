---
title: マスター プラン - サイトの補充、倉庫は必須ではない
description: このトピックでは、サイト分析コードを品目補充用に持つ品目の計画方法について説明します。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f4cde5c570148ca58c4ea583a8f538a72d4957d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432197"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>マスター プラン - サイトの補充、倉庫は必須ではない

[!include [banner](../includes/banner.md)]

このトピックでは、サイト分析コードを品目補充用に持つ品目の計画方法について説明します。

このマスター計画シナリオの前提条件を次に示します。

-   サイト分析コードが必須に設定され、需要トランザクションで入力されている。
-   倉庫分析コードが必須に設定されていない。 倉庫は既知である場合もあるが、マスタ 計画計算には使用されない。
-   サイト分析コードが補充計画用に設定されている。
-   倉庫分析コードが補充計画用に設定されていない。 そのため、供給と需要はサイトごとに集計され、多分、他の補充計画分析コードも同様です。

次の図は、マスター計画がどのように進行するかを示しています。 図の中で使用されているパラメータとその設定場所を次に示します。
-   品目に対して品目補充が定義されています。 **製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。 品目を選択し、**計画] &gt; [品目補充** の順にクリックします。
-   倉庫に対して補充関係が定義されています。 **在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫** の順にクリックします。 **マスター計画** タブに、**主要倉庫** フィールド グループが表示されます。
-   既定の注文タイプは [生産]、[発注書] または [かんばん] に設定されます。 **製品情報管理] &gt; [製品] &gt; [リリースされた製品** の順にクリックします。 品目を選択し、**計画] &gt; [既定の注文設定** の順にクリックします。 **既定の注文設定** フォームの **既定の注文タイプ** フィールドを参照してください。

![サイトの補充が必要、倉庫は必須ではない    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a>追加リソース
--------

[マスター プランとマルチサイト機能の概要](master-plan-multisite-functionality.md)

[マスター プラン - サイトと倉庫の補充、倉庫は必須](master-plan-site-coverage-warehouse-mandatory.md)

[マスター プラン - サイトの補充、倉庫は必須](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[マスター プラン - サイトの補充、倉庫は必須ではない](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[BOM バージョンの決定](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]