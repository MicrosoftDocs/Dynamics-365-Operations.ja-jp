---
title: "注文保留"
description: "このトピックでは、Dynamics AX の小売りとコマースを使用して、注文の保留について説明します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1cb18e3275b8dcdf0a61531ee056995f6e8fbc8d
ms.lasthandoff: 03/31/2017


---

# <a name="order-holds"></a>注文保留

このトピックでは、Dynamics AX の小売りとコマースを使用して、注文の保留について説明します。

注文はさまざまな理由で保留にすることができます。 たとえば、顧客の住所や支払方法が確認できるまで、またはマネージャーが顧客の与信限度額を確認できるまで、注文を保留にすることがあります。 販売プロセスの間は、販売注文は保留中にすることが必要な場合があります。 たとえば、顧客の支払いに関する問題のために、または管理者の確認が必要なために、販売注文を保留中にすることが必要な場合があります。 販売注文を保留中にすると、保留の理由を示す注文保留コードが販売注文に割り当てられます。 販売注文の保留コードは**販売およびマーケティング** **設定で &gt; 設定 &gt; されます** **販売注文** &gt; **順序は、コードが含まれています**。 販売注文は注文の作成時に、または後で手動で保留にすることができます。 また、注文を不正ルールに基づいて、自動的に保留にすることができます。 販売注文が保留中の間、詳細情報に基いてそれを更新する必要がある場合があります。 または、販売注文をチェック アウトして作業を続行することもできます。 販売注文を確認し、それを確認し、注文の管理の作業テーブルを使用して他のユーザーの取り消しを上書きします (** [小売りとコマース** &gt; **顧客** &gt; **注文の保留**)。 注文を完了する準備が整ったら、注文プロセスを完了する前に、保留を解除する必要があります。


