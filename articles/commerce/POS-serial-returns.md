---
title: POS でシリアル番号管理された製品の返品
description: このトピックでは、Microsoft Dynamics 365 Commerce POS (POS) アプリケーションの返品プロセスの一部としてシリアル番号が付された品目を検証するための機能について説明します。
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e53c8ceb91a007775fa74f0c9598a65745f01cec
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638100"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>POS でシリアル番号管理された製品の返品

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce POS (POS) アプリケーションの返品プロセスの一部としてシリアル番号が付された品目を検証するための機能について説明します。

> [!NOTE]
> Commerce バージョン 10.0.20 リリース以降では、**POS での統合返品処理エクスペリエンス** という新しい機能が利用可能です。 POS での返品注文処理時にシリアル番号の検証を使用するには、この機能を有効にする必要があります。 この機能が有効な場合に提供される他の機能の詳細については、[POS での返品の作成](POS-returns.md)を参照してください。
>
> 機能を有効にした後で無効にすることはできません。

## <a name="options-for-validating-serialized-returns"></a>シリアル番号付き返品を検証するためのオプション

**POS での統合返品処理エクスペリエンス** 機能を有効にすると、組織が、POS を通じてシリアル番号で制御される品目の返品検証を実行できます。 この機能により、返品されるシリアル番号が販売された元のシリアル番号と異なる場合に警告を表示できます。 Commerce Version 10.0.20 リリース以降では、ユーザーが受信するメッセージは警告メッセージのみです。 ユーザーは、当初販売されたシリアル番号とは異なるシリアル番号に対する返品処理を続行できます。

**POS での統合返品処理エクスペリエンス** 機能が有効になった後に組織に対してシリアル番号の検証を構成するには、Commerce Headquarters の **Retail と Commerce \> 本社の設定 \> パラメーター \> コマース パラメーター** に移動します。 **在庫** タブの **店舗在庫操作** クイックタブで、**POS 返品時にシリアル番号の検証を有効にする** オプションを **はい** に設定 します。

## <a name="process-returns-for-serialized-items-in-pos"></a>POS でシリアル番号が設定された品目の返品の処理

**POS 返品でのシリアル番号の検証を有効にする** オプションが **はい** に設定されている場合、POS を使用してシリアル番号管理されている品目が返品されれば、ユーザーは **返品可能な製品** ページの詳細ペインに返品行のシリアル番号を入力できます。 入力したシリアル番号が販売トランザクションで販売された元のシリアル番号と一致しない場合、ユーザーに警告メッセージが表示されます。 ただし、アプリケーションによりユーザーが返品の転記を続行できなくなることはありません。

> [!NOTE]
> 現在、POS では、元の注文数量が 1 つ以下の返品明細行でのみシリアル番号の検証がサポートされます。 元の販売注文行が POS 以外のチャンネルで作成されている場合、特定の販売行のシリアル番号が付いた品目の注文済数量が複数の場合、POS を使用して品目を適切に返品することはできません。

## <a name="additional-resources"></a>追加リソース

[POS での返品の作成](POS-returns.md)
