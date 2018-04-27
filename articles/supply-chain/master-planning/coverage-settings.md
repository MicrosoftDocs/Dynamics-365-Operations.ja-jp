---
title: "補充設定"
description: "マスタ スケジューリングでは補充設定を使用して在庫品目要求を計算します。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 591b1cd739bb3be61299f33f180ca7c264d21a35
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="coverage-settings"></a>補充設定

[!INCLUDE [banner](../includes/banner.md)]

マスタ スケジューリングでは補充設定を使用して在庫品目要求を計算します。 

補充設定は次のように複数の方法で指定できます。

-   補充グループの補充設定を指定します。 リンク先のすべての製品の設定を含む補充グループを作成できます。 補充グループを作成するには、[マスター プラン] &gt; [設定] &gt; [補充] &gt; [補充グループ] の順にクリックします。 補充グループは製品にリンクできます。 サイト、倉庫、製品分析コードに固有のリンクの場合、**品目の補充**ページで**補充グループ**のフィールドを使用します。 製品分析コードに関係なく、一般のリンクの場合は、**製品の詳細**ページの**計画**クイック タブの**補充グループ**を使用します。 補充グループを製品にリンクしない場合は、マスター プランでは**マスター プランのパラメーター**ページで指定された**一般補充グループ**が既定値として使用されます。

-   製品の補充設定を指定します。 特定の製品の補充設定を作成できます。 [製品情報管理] &gt; [製品] &gt; [リリースされた製品] の順にクリックします。 製品を選択し、[アクション ペイン]、[計画] タブ、[補充グループ]、[品目補充] の順にクリックして**品目補充**ページを開きます。 製品が補充グループにすでにリンクされている場合、**上書き**フィールドで設定した補充グループの設定は無視できます。 **品目の補充**ページの補充設定は、**補充グループ** ページの設定より優先されます。

<!-- -->

-   ウィザードで製品の補充設定を指定します。 ウィザードは、基本的な品目補充パラメーターを着実に設定するお手伝いをするガイドです。 **品目の補充**ページで、**ウィザード**をクリックして**品目補充ウィザード**を開きます。

<!-- -->

- 分析コード グループの補充設定を指定します。 <strong>[製品情報管理] &gt; [共通] &gt; [リリースされた製品]</strong> の順にクリックします。 <strong>リリース済製品の詳細 **ページ**で、[一般]</strong> タブ、<strong>管理</strong>グループ、<strong>保管分析コード グループ</strong> リンクの順にクリックします。 <strong>保管分析コード グループ</strong> ページで<strong>分析コード別補充計画</strong>フィールドを選択して、保管分析コード グループの分析コードについて補充設定を作成します。 コンフィギュレーション、色、サイズ、スタイルなどすべての製品分析コードで、<strong>[分析コード別補充計画]</strong> フィールドを選択する必要があります。



<a name="see-also"></a>参照
--------

[マスター プラン](master-plans.md)




