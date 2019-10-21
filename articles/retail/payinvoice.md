---
title: 請求書の支払シナリオを設定する
description: このトピックでは、請求書の支払に関するさまざまなシナリオに対応できるように、Dynamics 365 Retail を構成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4fb9101843396e489e4d7b63879e9df35e52fe64
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018016"
---
# <a name="set-up-pay-invoice-scenarios"></a>請求書の支払シナリオを設定する

[!include [banner](includes/banner.md)]

Dynamics 365 Retail の請求書の支払機能は拡張され、以下の機能がサポートされています。

- 1 回の POS トランザクションでの複数の販売注文の請求書の支払。
- 自由書式の請求書、プロジェクト ベースの請求書、訂正表を含む、さまざまな種類の顧客請求書の支払。

これらのシナリオに対応するには、以下に説明するように、店舗用の機能プロファイルを構成する必要があります。

1. **小売 \> チャネル設定 \> POS の設定 \> POS プロファイル \> 機能プロファイル** の順にクリックし、変更する店舗にリンクされているプロファイルを選択します。
2. **機能** タブで、必要に応じて、以下のパラメーターを構成します。

    - **販売注文請求書** – 単一の POS トランザクションで 1 つ以上の販売注文に基づく請求書の支払をユーザーが行えるようにするには、**はい** を選択します。
    - **自由書式の請求書** – 単一の POS トランザクションで 1 つ以上の自由書式の請求書の支払をユーザーが行えるようにするには、**はい** を選択します。
    - **プロジェクト請求書** – 単一の POS トランザクションで 1 つ以上のプロジェクト ベースの請求書の支払をユーザーが行えるようにするには、**はい** を選択します。
    - **販売注文 - 訂正票** – 未処理の請求書に対する複数の販売注文ベースの訂正表の決済をユーザーができるようにする、または未処理の訂正表について顧客への払戻を処理できるようにするには、**はい** を選択します。

> [!NOTE]
> 金額の部分的な支払や決済は、まだサポートされていません。
