---
title: "生産または調達する製品を設定する"
description: "製品はさまざまな方法で提供できます。製品は生産 (製造) または調達 (購買) できます。 この記事は、複数の調達をサポートするために、製品の構成時に考慮する一般的な点について説明します。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b5ed8c93c13746249605ad8742549c23bb1e0e10
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a>生産または調達する製品を設定する

[!include[banner](../includes/banner.md)]


製品はさまざまな方法で提供できます。製品は生産 (製造) または調達 (購買) できます。 この記事は、複数の調達をサポートするために、製品の構成時に考慮する一般的な点について説明します。 

複数の調達は、通常、購買品目がまれにしか製造されない場合や、主として製造されていた品目が変更になり現在の主とした購買品目になった場合に使用します。 最初に、品目は、部品表 (BOM) と工順情報を定義し、品目の製造オーダーをサポートするために、製造品目として指定されます。 生産タイプは **BOM** に設定します (または、製造プロセスの場合、**式** または **連産品**)。

標準原価を使用すると、品目原価レコードは製造品目に対して計算できます。 ただし、品目原価レコードは、購入目標にする標準原価と一致しない場合があります。 その場合、必要な標準原価を手動で入力し、品目原価レコードに対して有効化する必要があります。 原価計算には、会計年度期間中に製品の供給の組み合わせを示し、差異を経時的に最小限にするような特別な BOM とルーティングの使用を検討します。 さらに、あるサイトの製造品目を別のサイトに転送することもできます。 したがって、品目の転送先となるサイトに対して品目の原価を手動で入力して有効化する必要があります。 製造品目を上位レベルの製品のコンポーネントとして使用する場合、コンポーネントのコストは購入品目として取り扱う必要があります。 このガイドラインは、コンポーネントのコストが計算されたか、手動で入力されたかどうかに関係なく当てはまります。 つまり、BOM 計算では、品目のコストを、品目の部品表と工順の情報に基づいて計算するのではなく、購入したコンポーネントとして扱う必要があります。 

品目に割り当てられている BOM 計算グループに埋め込まれている**展開の停止**フラグを選択することで、この計算を行わないようにすることができます。 マスタ スケジューリング計算が品目を通して要件を展開しないようにするには、品目補充または補充グループの展開フェンスを 0 (ゼロ) 日に設定します。 マスター スケジューリングの計算は、品目を購入品目として扱い、それ以上部品表および工順情報に対する計算を行いません。






