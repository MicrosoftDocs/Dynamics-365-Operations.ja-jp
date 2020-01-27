---
title: ジョブ カード デバイスからライセンス プレートにより制御されている場所への完了レポート
description: このトピックでは、場所がライセンス プレートによって制御される場合に、在庫への製造オーダーの完成品を完了させるプロセスについて説明します。
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 63073035941cd2ef343c65364536fe76a9b71430
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935125"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>ジョブ カード デバイスからライセンス プレートにより制御されている場所への完了レポート 

完了レポートを呼び出したプロセスが在庫への製造オーダーの完成品を完了させます。 完成品が高度な倉庫管理プロセスに対して有効化されている場合、生産出荷の場所と呼ばれる場所に製品が完了したことが報告されます。 生産出荷の場所の設定の詳細については、[生産出荷の場所](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location) を参照してください。

生産出荷の場所がライセンス プレートで管理されている場合は、完了報告時にライセンス プレートを指定する必要があります。 **ライセンス プレート** フィールドは、**ジョブ カード デバイス** ページの**進捗状況のレポート**の確認に表示されます。 このフィールドは、製造オーダーの最後の工程を報告し、製造オーダーの品目が倉庫管理プロセスに対して有効になっている場合に、**進捗状況レポート**確認にのみ表示されます。 

ライセンス プレートを指定するには 2 つのオプションがあります
- ユーザーは、ライセンス プレート フィールドで既存のライセンス プレートを選択しています。
- ライセンス プレートは、番号順序から自動生成され、ライセンス プレート フィールドに既定値が設定されます。

ライセンス プレートを自動生成するためのオプションをコンフィギュレーションするには、**デバイスのジョブ カードのコンフィギュレーション** ページの、**ライセンス プレートの作成**オプションを選択します。
