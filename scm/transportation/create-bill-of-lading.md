---
title: "船荷証券の作成"
description: "このトピックでは、倉庫管理のプロセスを使用して、船荷証券の作成方法を説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b88679f1be00d6a7168c8976f0d7db894c7e77fc
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-bill-of-lading"></a>船荷証券の作成

このトピックでは、倉庫管理のプロセスを使用して、船荷証券の作成方法を説明します。  

船荷証券は、配送業者と品目を出荷する会社間の法律文書です。 この文書は出荷済品目に添えられ、品目が宛先に配送されると出荷明細行として使用されます。 倉庫管理を使用する場合は、船荷証券を生成する 2 つの方法があります。

  -   [**船荷証券**] ページを使用してレポートを手動で作成します。
  -   [**積荷計画ワークベンチ**] からレポートを生成します。

[**積荷計画ワークベンチ**] から船荷証券を生成する場合は、積荷ステータスを [**出荷済**] にする必要があります。 負荷に複数の出荷がある場合は、船荷証券は各出荷に対して作成されます。 船荷証券の作成後に**船荷証券**ページでオーダーに変更を加えることができます。

## <a name="master-bill-of-lading"></a>主船荷証券
1 つの積荷に複数の出荷がある場合、主船荷証券を生成します。 これは船荷証券と同じレイアウトおよび情報がありますが、すべての出荷の集計されたコンテンツが含まれます。 [**輸送管理パラメーター**] ページの [**1 つの積荷に複数の出荷がある場合は主船荷証券を作成**] オプションで [**あり**] を設定した場合、複数の出荷があるときに [**積荷計画ワークベンチ**] から主船荷証券を作成すると、主船荷証券が自動的に生成されます。 **、関連情報** **船荷証券をクリックして**船荷 &gt; 証券の一覧を表示できます。 船荷証券を手動で作成する場合は、[**船荷証券**] ページで主船荷証券を作成できます。


