---
title: ジョブ カード デバイスからライセンス プレートにより制御されている場所への完了レポート
description: このトピックでは、場所がライセンス プレートによって制御される場合に、在庫への製造オーダーの完成品を完了させるプロセスについて説明します。
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995145"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>ジョブ カード デバイスからライセンス プレートにより制御されている場所への完了レポート 

完了レポートを呼び出したプロセスが在庫への製造オーダーの完成品を完了させます。 完成品が高度な倉庫管理プロセスに対して有効化されている場合、生産出荷の場所と呼ばれる場所に製品が完了したことが報告されます。 生産出荷の場所の設定の詳細については、[生産出荷の場所](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location) を参照してください。

このタスクを完了するには、既存のライセンス プレート番号を選択する必要があります。 生産出荷の場所をライセンス プレート別に追跡するように設定している場合、生産出荷の場所を完了として報告する時に、ライセンス プレート番号を含める必要があります。 **ライセンス プレート** フィールドは、**ジョブ カード デバイス** ページの**進捗状況のレポート**の確認に表示されます。 このフィールドは、製造オーダーの最後の工程を報告する時、**進捗状況のレポート**の確認にのみ表示されます。 このフィールドは、製造オーダーの品目が倉庫管理プロセスに対して有効化されている場合にのみ表示されます。 
