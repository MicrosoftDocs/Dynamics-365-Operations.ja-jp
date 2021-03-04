---
title: 詳細な口座調整の概要
description: この記事は、高度な口座調整プロセスのフローについて説明します。 高度な口座調整機能では、銀行トランザクション内で自動的に調整できる口座取引明細書をインポートできます。
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26b6e1e50e5a9b53ca6b5315de760f5bcec4769
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445282"
---
# <a name="advanced-bank-reconciliation-overview"></a>詳細な口座調整の概要

[!include [banner](../includes/banner.md)]

この記事は、高度な口座調整プロセスのフローについて説明します。 高度な口座調整機能では、銀行トランザクション内で自動的に調整できる口座取引明細書をインポートできます。

詳細な口座調整機能により、口座取引明細書のインポートをすることができます。 インポートした口座取引明細書は、次に自動的に銀行トランザクション内から調整されます。 詳細な口座調整のフローを次に示します。

1.  口座取引明細書のインポートを設定します。
    -   データ エンティティ フレームワークを使用して口座取引明細書をインポートします。
    -   ISO20022、BAI2、MT940、の 3 つの一般的な口座取引明細書の形式が組み込まれています。
    -   機能は、任意の形式に拡張できます。

2.  詳細な口座調整に使用する番号順序を設定して、口座調整の照合ルールを定義します。
    -   調整の照合ルールは、調整プロセス中に口座取引明細書行および Microsoft Dynamics 365 Finance 銀行トランザクション明細行をフィルター処理するために使用される一連の基準です。 業務内容によって、1 つ以上の照合ルールを設定して、調整プロセスを自動化また最適化できます。

3.  Finance 銀行トランザクションを使用して、口座取引明細書を調整します。
    -   口座調整仕訳の自動照合と作成を実行します。
    -   口座取引明細書と Finance 銀行トランザクションを並べて表示します。
    -   口座取引明細書には表示されるが Finance アプリには表示されない場合、Finance 銀行のトランザクションを自動的に転記します。
    -   調整明細書を生成します。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]