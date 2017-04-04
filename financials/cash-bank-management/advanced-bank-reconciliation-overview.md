---
title: "詳細な口座調整の概要"
description: "この記事は、高度な口座調整プロセスのフローについて説明します。 高度な口座調整機能では、銀行トランザクション内で自動的に調整できる口座取引明細書をインポートできます。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 00f022da597b1de2454e93123de31731c6a65962
ms.openlocfilehash: 20363ef1917f7d0796cb0d5cd8e623c598b5ee01
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>詳細な口座調整の概要

この記事は、高度な口座調整プロセスのフローについて説明します。 高度な口座調整機能では、銀行トランザクション内で自動的に調整できる口座取引明細書をインポートできます。

詳細な口座調整機能により、口座取引明細書のインポートをすることができます。 インポートした口座取引明細書は、次に自動的に銀行トランザクション内から調整されます。 詳細な口座調整のフローを次に示します。

1.  口座取引明細書のインポートを設定します。
    -   データ エンティティ フレームワークを使用して口座取引明細書をインポートします。
    -   ISO20022、BAI2、MT940、の 3 つの一般的な口座取引明細書の形式が組み込まれています。
    -   機能は、任意の形式に拡張できます。

2.  詳細な口座調整に使用する番号順序を設定して、口座調整の照合ルールを定義します。
    -   調整の照合通常、調整プロセス中に工程の銀行トランザクション明細行の口座取引明細書行およびMicrosoft Dynamicsをフィルタ処理する365で使用される一連の条件です。 既に業者によって、調整プロセスを自動化および最適化する複数の照合ルールを設定できます。

3.  工程の銀行トランザクションの365 for Operationsで口座取引明細書を調整します。
    -   口座調整仕訳の自動照合と作成を実行します。
    -   工程の銀行トランザクションの口座取引明細書とDynamics 365 for Operationsに並べて表示します。
    -   口座取引明細書に現われたらを転記して、Dynamics 365 for Operationsで現われないで、自動的に工程の銀行トランザクションのDynamics 365 for Operations。
    -   調整明細書を生成します。




