---
title: コード別消費税支払レポートの印刷
description: このトピックでは、会計または税コードの通貨でコード別消費税支払レポートを印刷するために必要な設定とアクションについて説明します。
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815455"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>コード別消費税支払レポートの印刷 

[!include [banner](../includes/banner.md)]

**コード別消費税支払** レポートを印刷するには、**税** \> **照会およびレポート** \> **消費税レポート** \> **コード別消費税支払** に移動します。 既定では、レポート金額は、**消費税レポート コード** ページで設定されたすべてのレポート コードについて法人の会計通貨で生成されます。

また、このレポートを生成して、**消費税コード** ページで消費税コードに割り当てられているすべてのレポート コードについて、消費税コードの通貨で消費税支払額を表示することもできます。

## <a name="turn-on-the-feature"></a>機能をオンにする

**機能管理** ワークスペースで、次の機能を有効にします: **コード別消費税支払レポートを消費税コードの通貨で生成する**。

## <a name="run-the-report"></a>レポートの実行

1. **税** \> **照会およびレポート** \> **消費税レポート** \> **コード別消費税支払** の順に移動します。
2. **レポート通貨** フィールドで、次のいずれかの値を選択します:

    - **会計通貨** – レポート金額を会計通貨で印刷します。
    - **消費税コードの通貨** – 消費税コードの通貨でレポート金額を印刷します。

    ![コード別消費税支払ダイアログ ボックス](media/Sales-tax-payment-by-code.png)

次の図で、生成されるレポートの例を示します。 レポート コードが割り当てられている消費税コードに対して **消費税通貨** フィールドが **EUR** に設定されている場合、レポート コード **101** が通貨 **EUR** であることがレポートに表示されます。

![コード別消費税支払レポートの例](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]