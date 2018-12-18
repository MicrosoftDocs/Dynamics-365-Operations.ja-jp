---
title: "分析レポートは更新されない"
description: "このトピックでは、顧客のデータの変更が、顧客のワークスペースに表示されない場合の対処方法について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a>分析レポートは更新されない

[!include [banner](includes/banner.md)]

**払出**

顧客のデータの変更がいずれかの顧客のワークスペースの**分析**タブに表示されません。

**原因**

既定では、Microsoft Power BI レポートは、測定の配置バッチ ジョブのスケジュールに基づいて 4 時間ごとに更新されます。

**解像度**

この問題は、単なるタイミングの問題である場合があります。 この手順に従ってバッチ ジョブを開始し、分析ワークスペースを更新します。

1. **システム管理\>リンク\>バッチ ジョブ\>バッチ ジョブ**で、**バッチ ジョブ**ページを開きます。 または、検索を使用して、**バッチ ジョブ**と入力します。
1. 一覧で**測定の配置**ジョブを検索します。
1. ページの上部で**編集**を選択して、開始予定日/時刻を現在の時刻に近い分析を更新する値に設定します。

![バッチ ジョブ](media/batch-jobs.png)
