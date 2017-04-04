---
title: "補充設定"
description: "マスタ スケジューリングでは補充設定を使用して在庫品目要求を計算します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c1c5654afa6b592e178af052e3e4a7e246a94c9f
ms.lasthandoff: 03/31/2017


---

# <a name="coverage-settings"></a>補充設定

マスタ スケジューリングでは補充設定を使用して在庫品目要求を計算します。 

補充設定は次のように複数の方法で指定できます。

-   補充グループの補充設定を指定します。 リンク先のすべての製品の設定を含む補充グループを作成できます。 補充グループを作成 &gt; します &gt; ** &gt; マスタ プラン補充の補充グループを設定します。**。 補充グループは製品にリンクできます。 サイト、倉庫、製品分析コードに固有のリンクの場合、**品目の補充**ページで**補充グループ**のフィールドを使用します。 製品分析コードに関係なく、一般のリンクの場合は、**製品の詳細**ページの**計画**クイック タブの**補充グループ**を使用します。 補充グループを製品にリンクしない場合は、マスター プランでは**マスター プランのパラメーター**ページで指定された**一般補充グループ**が既定値として使用されます。

-   製品の補充設定を指定します。 特定の製品の補充設定を作成できます。 [**製品情報管理 &gt; 製品 &gt; 製品のリリースされた**。 **品目補充**ページを開くには、の製品を、**アクション ウィンドウ**、**計画**記録するに、**補充グループ**、[**品目補充**を選択します。 製品が補充グループにすでにリンクされている場合、**上書き**フィールドで設定した補充グループの設定は無視できます。 **品目の補充**ページの補充設定は、**補充グループ** ページの設定より優先されます。

<!-- -->

-   ウィザードで製品の補充設定を指定します。 ウィザードは、基本的な品目補充パラメーターを着実に設定するお手伝いをするガイドです。 **品目の補充**ページで、**ウィザード**をクリックして**品目補充ウィザード**を開きます。

<!-- -->

-   分析コード グループの補充設定を指定します。 [**製品情報管理 &gt; 共通 &gt; の製品のリリースされた**。 **にリリース済製品の詳細**で、**概要**記録、**管理**グループに、[**保管分析コード グループ**リンクを]ページでします。 **保管分析コード グループ** ページで**分析コード別補充計画**フィールドを選択して、保管分析コード グループの分析コードについて補充設定を作成します。 すべての製品分析コードは、組織など、色、サイズ、スタイル、選択した**分析コード別補充計画**フィールドが必要です。



<a name="see-also"></a>参照
--------

[Master plans](master-plans.md)


