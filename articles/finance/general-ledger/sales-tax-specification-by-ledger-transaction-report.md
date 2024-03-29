---
title: 元帳トランザクション別消費税詳細のレポート
description: この記事では、元帳トランザクション レポート別の消費税詳細を使用して、消費税の計算対象である元帳トランザクションに関する情報を表示および印刷する方法について説明します。
author: EricWang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: c96f457a0ea24aef1769f370c3c0657ada31eebf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898094"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>元帳トランザクション別消費税詳細のレポート
[!include [banner](../includes/banner.md)]

この記事では、**元帳トランザクション別の消費税詳細** レポートを使用して、消費税の計算対象である元帳トランザクションに関する情報を表示および印刷する方法について説明します。

## <a name="tax-accounts-vs-non-tax-accounts"></a>税勘定と非課税勘定の対比

**元帳トランザクション別の消費税詳細** レポートには、税勘定と非課税勘定の両方の税トランザクションが表示されます。 これらの勘定は、次のように分類されます。

- **税勘定** – 税トランザクションが転記されると勘定は税勘定と見なされ、**消費税** 仕訳帳明細行の主勘定は、消費税支払の勘定または消費税収入の勘定などの税勘定となります。
- **非課税勘定** – 税トランザクションが転記されると勘定は非課税勘定と見なされ、元のトランザクションの主勘定は、収益勘定または経費勘定などの非課税勘定となります。

税勘定の場合、レポートの **発生元**、**消費税収入**、**消費税支払** 列は **0**(ゼロ) と表示されます。 非課税勘定の場合は、これらの列に金額が表示されます。

## <a name="filtering-the-data-on-the-report"></a>レポート上のデータをフィルタリング

レポートを生成するとき、次の既定のフィールドが使用可能になります。 これらのフィールドを使用して、レポートに表示されるデータをフィルタリングできます。

| フィールド                      | 説明 |
|----------------------------|-------------|
| 日                       | **開始** および **終了** セクションのフィールドを使用して、税トランザクションの日付範囲を定義します。 |
| 主勘定               | **開始** および **終了** セクションのフィールドを使用して、主勘定の範囲を定義します。 |
| 消費税コード             | **開始** および **終了** セクションのフィールドを使用して、消費税コードの範囲を定義します。 |
| グループ化                   | レポートを勘定科目別または消費税コード別にグループ化するかどうかを選択します。 |
| 消費税コードごとの小計 | 消費税コード別の小計を表示するには、このオプションを **はい** に設定します。 |
| 合計のみ                | 合計のみを表示するには、このオプションを **はい** に設定します。 |
| 主勘定のみ         | レポートに主勘定のみを含めるには、このオプションを **はい** に設定します。 |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>レポートで非課税勘定のみを表示する

レポートで非課税勘定のみを表示するには、次の図に示すように、アスタリスク(\*) などのフィルター条件を設定します。

![非課税勘定を表示するレポート。](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
