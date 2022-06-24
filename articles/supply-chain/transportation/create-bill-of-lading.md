---
title: 船荷証券の作成
description: この記事では、倉庫管理のプロセスを使用する場合に、船荷証券を作成する方法について説明します。
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e84fee13dcff574f1700ba2b8f577f4c401cbc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885786"
---
# <a name="create-a-bill-of-lading"></a>船荷証券の作成

[!include [banner](../includes/banner.md)]

この記事では、倉庫管理のプロセスを使用する場合に、船荷証券を作成する方法について説明します。  

船荷証券は、配送業者と品目を出荷する会社間の法律文書です。 この文書は出荷済品目に添えられ、品目が宛先に配送されると出荷明細行として使用されます。 倉庫管理を使用する場合は、船荷証券を生成する 2 つの方法があります。

  -   **船荷証券** ページを使用してレポートを手動で作成します。
  -   **積荷計画ワークベンチ** からレポートを生成します。

**積荷計画ワークベンチ** から船荷証券を生成する場合は、積荷ステータスを **出荷済** にする必要があります。 積荷に複数の出荷がある場合、船荷証券は各出荷ごとに生成されます。 船荷証券の作成後、**船荷証券** ページで変更を加えることができます。

## <a name="master-bill-of-lading"></a>主船荷証券
1 つの積荷に複数の出荷がある場合、主船荷証券を生成します。 これは船荷証券と同じレイアウトおよび情報がありますが、すべての出荷の集計されたコンテンツが含まれます。 **輸送管理パラメーター** ページの **1 つの積荷に複数の出荷がある場合は主船荷証券を作成** オプションで **あり** を設定した場合、複数の出荷があるときに **積荷計画ワークベンチ** から主船荷証券を作成すると、主船荷証券が自動的に生成されます。 **関連情報** &gt; **船荷証券** の順にクリックして船荷証券のリストを取得できます。 船荷証券を手動で作成する場合は、**船荷証券** ページで主船荷証券を作成できます。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]