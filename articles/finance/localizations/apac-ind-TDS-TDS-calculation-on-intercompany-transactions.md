---
title: 会社間取引の TDS の算出
description: このトピックでは、段階的に行われる企業間取引の源泉徴収 (TDS) の計算プロセスについて説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 381b00c64e3e3a09a245c82cbe1f1599986a49aa
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726980"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>会社間取引の TDS の算出

[!include [banner](../includes/banner.md)]

このトピックでは、段階的に行われる企業間取引の源泉徴収 (TDS) の計算プロセスについて説明します。

企業間取引の注文書または販売注文書が作成されると、顧客や仕入先に定義されている既定の TDS グループが TDS 額の計算に使用されます。 TDS の金額は、請求書が転記された後に回収可能勘定または買掛金勘定に転記されます。

会社間販売注文や会社間発注書は、元の発注書または販売注文に対して自動的に作成されます。 既定の TDS グループが会社間注文に表示され、TDS を計算できます。 TDS のグループは変更できます。 自動的に作成された会社間注文の正味請求額が、元の注文の正味請求額と一致した場合にのみ、請求書を転記することができます。 (正味金額は、TDS が控除された後の請求金額です。)

たとえば、50,000 円の売上請求書が作成され、**10%** の TDS グループが関連付けられたとします。 転記された請求金額は 45,000 で、売上請求書の転記された TDS の額は 5,000 です。 会社間取引の注文書には自動的に注文書が作成され、 **10%** のTDSグループが関連付けられます。 TDS グループを **15%** に変更すると、自動的に作成された会社間販売注文の正味請求金額が元販売注文の正味請求金額と一致しないため、請求書を転記できません。

会社間請求書に対して作成された支払仕訳帳は自動的に転記されます。 この支払仕訳帳は、その支払仕訳帳の正味支払金額が元の支払仕訳帳の正味支払金額と一致している場合にのみ転記できます。
