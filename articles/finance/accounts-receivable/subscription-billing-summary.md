---
title: サブスクリプション請求の概要
description: この記事では、Microsoft Dynamics 365 Finance でのサブスクリプション請求管理について説明します。
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 10302e9ae7dff3d018897b666caaf4d4289b4866
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856744"
---
# <a name="subscription-billing-overview"></a>サブスクリプション請求の概要

[!include [banner](../includes/banner.md)]

サブスクリプション請求管理を使用すると、組織がサブスクリプション収益機会と、請求スケジュールを使用した繰り返し請求を管理できます。 複雑な価格決定モデルおよび請求モデルと収益配賦を簡単に管理し、明細行レベルで請求および認識されます。 多要素収益配賦を使用すると、国際会計基準 (国際財務報告標準 15 \[IFRS 15\]) および米国 GAAP (Accounting Standards Codification Topic 606 \[ASC 606\]) に準拠して収益を配賦できます。

このソリューションには、それぞれ独立して使用できる 3 つのモジュールがあります。 また、3 つのモジュールすべてを一緒に使用することもできます。

- **定期契約請求** ― このモジュールを使用すると、定期請求管理および価格管理で、価格決定パラメーターと請求書作成パラメーター、契約の適用方法、および月次締め請求書を制御できます。
- **収益および経費の繰延** ― このモジュールは、収益を管理し、毎月の経常収益に関するリアルタイムの情報を可能にすることで、手動のプロセスと外部システムへの依存を排除します。
- **多要素収益配賦** ― このモジュールは、複数の品目にわたる価格決定および収益配賦を処理することで、収益への準拠に役立ちます。

サブスクリプション請求管理の詳細については、[サブスクリプション請求管理 Power BI コンテンツ](sub-bill-power-bi.md)を参照してください。

**機能管理** を使用してサブスクリプションの請求書作成を有効にします。 ただし、**収益認識** 機能では使用できません。 したがって、定期購読の請求を有効にする前に、その機能を無効にする必要があります。

1. **機能管理** ワークスペースの **すべて** タブで、フィルターに **収益認識** を入力し、機能名にフィルターを選択します。
2. **収益認識** 機能を選択し、**無効** ボタンを選択します。
3. **機能名** フィルターで **サブスクリプション請求管理** を入力し、モジュール フィルターを選択します。
4. **サブスクリプション請求管理** 機能を選択し、**有効にする** を選択します。
5. 前の一覧から 3 つのモジュールのいずれかを選択し、**有効にする** を選択します。 他の 2 つのモジュールについて、このステップを繰り返します。

    > [!IMPORTANT]
    > 3 つのモジュールのいずれかを有効にする前に **サブスクリプション請求管理** 機能を有効にする必要があります。
