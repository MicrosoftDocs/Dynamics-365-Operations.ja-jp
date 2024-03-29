---
title: 詳細な口座調整の概要
description: この記事は、高度な口座調整プロセスのフローについて説明します。 高度な口座調整機能では、銀行トランザクション内で自動的に調整できる口座取引明細書をインポートできます。
author: angelad116
ms.date: 10/24/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: kfend
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 677a032ce77fbe57393c85235a1c64dba3958f2d
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715152"
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
