---
title: "コンフィギュレーション ルール"
description: "この記事は、コンフィギュレーション ルールに関する一般情報を示します。 コンフィギュレーション ルールは、分析コード ベースのコンフィギュレーション テクノロジを使用する製品の部品表 (BOM) の品目間の関係を定義します。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bc8e606cdc0bc5a45321c67ce9b089059f226df2
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---

# <a name="configuration-rules"></a>コンフィギュレーション ルール

[!INCLUDE [banner](../includes/banner.md)]

この記事は、コンフィギュレーション ルールに関する一般情報を示します。 コンフィギュレーション ルールは、分析コード ベースのコンフィギュレーション テクノロジを使用する製品の部品表 (BOM) の品目間の関係を定義します。

コンフィギュレーション ルールは、分析コード ベースのコンフィギュレーション モデルを定義する場合に使用できます。 コンフィギュレーション ルールは、部品表 (BOM) で特定の品目の組み合わせを許可または禁止する場合に使用します。 BOM が作成され、関連する品目をそれぞれのコンフィギュレーション グループに割り当てた後、1 つ以上のコンフィギュレーション ルールを定義できます。 2 つの品目が一緒に含まれる場合、**選択**オペレータを使用して、正しく含まれるようにします。 2 つの品目が相互に排他的な場合、**選択解除**オペレータを使用して排他されるようにします。  

**注意:** この情報は、分析コード ベースのコンフィギュレーション テクノロジを使用する製品マスターにのみ適用されます。  

既存のコンフィギュレーションは、その後発生するコンフィギュレーション ルールに対する変更によって、影響を受けることはありません。 ただし、新しいコンフィギュレーションを定義する前にルールを設定し、ルールが変更されたと考えられる場合にルールを確認することは、重要なことです。  

**注意:** **選択**メソッドでは、派生するコンフィギュレーション グループ、品目番号、およびコンフィギュレーションが自動的に選択されます。 **選択解除**メソッドでは、派生するコンフィギュレーション グループ、品目番号、およびコンフィギュレーションを選択できません。

<a name="see-also"></a>参照
--------

[分析コード ベースの製品コンフィギュレーション](dimension-based-product-configuration.md)




