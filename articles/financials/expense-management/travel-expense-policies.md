---
title: "経費ポリシーを定義します"
description: "Microsoft Dynamics 365 for Finance and Operations, Enterprise edition で、作業者が経費精算書と出張費要求を入力して提出する際に従う必要がある経費ポリシーを定義できます。"
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: b52fe81015a324bde07f387b42b834b79dc7c2da
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---

# <a name="expense-policies"></a>経費ポリシー

[!include[banner](../includes/banner.md)]

作業者が経費精算書と出張費要求を入力して提出する際に従う必要があるポリシーを定義できます。         
経費ポリシーを実装すると、経費を効率的に管理できます。         

たとえば、ニューヨークでのホテルの 1 泊料金は USD 250 以下にするというホテル経費のポリシーを設定できます。       
経費精算書または宿泊料金がこの金額を超える出張費要求を作業者が提出すると、システムが通知をします        
作業者が、経費に関するポリシー金額を超えました。 作業者が受け取るメッセージをコンフィギュレーションできます        
ポリシーを定義します。      
        
次の 3 種類のポリシーを定義できます。         
        
- 警告: 作業者は経費精算書や出張費要求を提出できますが、経費はすべての承認者にマークされ        
その後の報告用に。        

- エラー: 経費精算書や出張費要求を提出する前に、経費を変更してポリシーに準拠するように作業者に要求します。       
 
 - 妥当性: 経費精算書や出張費要求を提出する前に、ポリシー金額を超えることに関する妥当性を入力するように作業者または管理者に要求します。        
 
 また、経費ポリシーの有効期間の日付範囲を設定することもできます。 たとえば、デンマーク間の便の航空運賃      
 およびニューヨーク市間では、休暇旅行シーズンのピーク時に高くなる可能性があります。 制限する航空経費ルールを定義できます      
 ニューヨーク行きの航空運賃を DKK 5000 に制限し、このルールが 3 月 15 日から有効になるよう指定できます      
 9 月 15 日。

