---
title: "経費ポリシーを定義します"
description: "Microsoft Dynamics 365 for Finance and Operations, Enterprise edition で、作業者が経費精算書と出張費要求を入力して提出する際に従う必要がある経費ポリシーを定義できます。"
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 940d6f8c3d878c2c12806ad04a092856df2acb33
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="expense-policies"></a>経費ポリシー

[!include[banner](../includes/banner.md)]

作業者が経費精算書と出張費要求を入力して提出する際に従う必要があるポリシーを定義できます。 経費ポリシーを実装すると、経費を効率的に管理できます。 

たとえば、ニューヨークでのホテルの 1 泊料金は USD 250 以下にするというホテル経費のポリシーを設定できます。 宿泊料金がこの金額を超える経費精算書を作業者が提出すると、経費に関するポリシー金額を超えたことが作業者に通知されます。 ポリシーの定義時に作業者に送信するメッセージをコンフィギュレーションできます。 

次の 3 種類のポリシーを定義できます。 

 - 警告: 作業者は経費精算書や出張費要求を提出できますが、経費はすべての承認者にマークされ  
 その後の報告用に。 
 - エラー: 経費精算書や出張費要求を提出する前に、経費を変更してポリシーに準拠するように作業者に要求します。 
 - 妥当性: 経費精算書や出張費要求を提出する前に、ポリシー金額を超えることに関する妥当性を入力するように作業者または管理者に要求します。 

また、経費ポリシーの有効期間の日付範囲を設定することもできます。 たとえば、デンマーク発着ニューヨーク便の航空運賃は、休暇の旅行シーズンのピーク時に高くなる可能性があります。 ニューヨーク行きの航空運賃を DKK 5000 に制限する航空経費ルールを定義し、このルールが 3 月 15 日から 9 月 15 日まで有効になるように指定することができます。 

