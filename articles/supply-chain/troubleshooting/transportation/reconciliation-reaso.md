---
title: 調整の理由から、主勘定のみを貸方勘定として追加できる
description: 輸送管理で調整理由を設定した場合、主勘定のみを貸方勘定として追加できます。
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750885"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>調整の理由から、主勘定のみを貸方勘定として追加できる

KB 番号: 4603538

## <a name="symptoms"></a>現象

輸送管理で調整理由を設定した場合、主勘定のみを貸方勘定として追加できます。 コスト センターまたは他の分析コードを貸方勘定として追加することはできません。 ただし、借方勘定では他の分析コードを選択できます。

## <a name="resolution"></a>解像度

調整で仕入先への支払は行われなかったが、特定の主勘定の貸方に転記される場合、調整理由の設定時に貸方勘定の財務分析コードを選択することはできません。

勘定構造で貸方主勘定に対して特定の財務分析コード値が必要な場合は、財務分析コード値が存在しないため、結果の仕入先仕訳帳を自動的に転記することはできません。 したがって、最初に **請求仕訳帳** ページを使用して貸方勘定を手動で指定する必要があります。

貸方勘定には分析コード値が必要なため、仕入先請求仕訳帳を自動的に転記することはできません。 貸方記入行の主勘定に分析コード値を手動で追加した後、手動で転記する必要があります。
