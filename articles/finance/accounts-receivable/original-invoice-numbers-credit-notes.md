---
title: 貸方票での元の請求書への参照
description: このトピックでは、元の請求書番号を関連する貸方表に設定・印刷する方法について説明します。
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ce06a0ce4f2a308e1917ac2c7cbc66f0494a2ec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811513"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>貸方票での元の請求書への参照

[!include [banner](../includes/banner.md)]


一部の国や地域では、貸方書の印刷に元の請求書への参照を含めるという法的要件があります。 このトピックでは、元の請求書番号を関連する貸方表に設定・印刷する方法について説明します。

## <a name="prerequisites"></a>必要条件

- **機能管理** ワークスペースで、**販売およびプロジェクト請求レポートの請求の貸方転記レイアウト** 機能を有効 にします。 詳細については [機能管理の概要](../../fin-and-ops/get-started/feature-management/feature-management-overview.md) を参照してください。
- 必要なドキュメントの印刷可能な形式については、印刷管理で構成する必要があります。

このトピックで説明する機能は、以下のドキュメントに適用されます:

**売掛金勘定**

- 自由書式の訂正票
- 顧客訂正票

**プロジェクト管理および会計**

- プロジェクト訂正票

## <a name="configure-accounts-receivable-parameters"></a>売掛金のパラメーターを設定する

これらの手順に従って、元の請求書への参照が関連する訂正票に印刷されるかどうかを制御するパラメータを設定します。

1. **売掛金勘定** \> **設定** \> **売掛金勘定パラメーター** に移動します。
2. **更新** タブの **請求書** クイックタブで、**クレジット請求書のレイアウトを販売請求書とプロジェクト請求書レポートに適用する** オプションを **はい** に設定します。

![売掛金のパラメーターを構成する](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>元の請求書への参照を定義する

以下の手順を使用して、文書の種類に基づいて元の請求書への参照を定義します。

### <a name="free-text-credit-note"></a>自由書式の訂正票

1. **売掛金勘定** \> **請求書** \> **すべての自由書式の請求書** に移動します。
2. 新しい貸方書を作成するか、既存の貸方書を選択します。
3. 請求書を開きます。
4. アクション ペインの、**請求書** タブで、**機能** グループから **貸方請求書** を選択します。
5. 元の請求書への参照を入力し、修正の理由を選択します。

![自由形式請求書の参照の定義](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>顧客訂正票

1. **売掛金勘定** \> **注文** \> **すべての販売注文** に移動します。
2. 訂正する必要のある請求書付き販売注文を選択して開きます。
3. [アクション ウィンドウ] の **販売** タブで、 **訂正票** グループで、**訂正票** を選択します。
4. 修正の理由を入力します。 請求書の原本への参照が自動的に確立されます。

![販売注文の参照を定義する](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>プロジェクト訂正票

1. **プロジェクト管理および会計** \> **プロジェクト請求書** \> **プロジェクト請求書** の順に選択します。
2. 訂正する必要のあるプロジェクト請求書を選択して開きます。
3. アクション ペインの、**プロジェクト請求書** タブで、**機能** グループから **訂正票を選択** を選択します。
4. **貸方請求書** を選択します。
5. 修正の理由を入力します。 請求書の原本への参照が自動的に確立されます。

![プロジェクト請求書の参照の定義](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>訂正票の印刷

自由形式、顧客、プロジェクトの貸方伝票を印刷する場合は、元の請求書への参照、修正理由が含まれます。

![印刷された訂正票](media/credit-note-FTI.jpg)

> [!NOTE]
> 請求書の原本への参照が印刷されることを前提として、文書の印刷可能な形式が正しく設定されていることを確認してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
