---
title: 理由コードの設定
description: Dynamics 365 Human Resources は、理由コードを使用して、従業員の給付金が変化する理由を説明します。
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 176ce59547456a14b494caa4dc3c2d8251920fe5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360547"
---
# <a name="set-up-reason-codes"></a>理由コードの設定

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources は、理由コードを使用して、従業員の給付金が変化する理由を説明します。

> [!NOTE]
> 2021 年 1 月時点で、理由コードは、**従業員管理ワーク** スペースに移行されているため、**福利厚生管理** ワークスペースでは　ご利用いただけません。 詳細については、[従業員管理に理由コードを手動で移行する](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management)を参照してください。

## <a name="create-reason-codes"></a>理由コードの作成

1. **Human Resources** ワークスペース (または理由コードがまだ移行されていない場合は **福利厚生管理** ワークスペース) で、**リンク** を選択し、**理由コード** を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | **理由コード** | 従業員が給付金プランの登録を変更する理由を識別する一意の名前。 |
   | **説明** | 理由コードの説明。 |

4. **該当するシナリオ** で、**福利厚生管理** を **はい** に 設定します。 (理由コードがまだ **担当者管理** ワークスペースに移行していない場合は、適用されません。)

5. **保存** を選択します。

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>従業員管理に理由コードを手動で移行する

2021 年 1 月時点で、理由コードは、**従業員管理** ワークスペースに移行されているため、**福利厚生管理** ワークスペースではご利用いただけません。 ほとんどの理由コード データは、環境内で自動的に移行されます。 一部の理由コード データは移行されない場合があります。 たとえば、理由コードの最大文字数が15文字となった場合、15文字を超える理由コードは自動的に移行されません。

**福利厚生管理** ワークスペースの **リンク** ページにバナーが表示され、移行に関する情報やコードが移行されなかった理由が通知されます。

1. 移行ステータスに関する詳細を示す **理由コード** を選択します。

   [![理由コード。](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. 移行に失敗した理由コードを選択します。

   [![理由コードの移行状態。](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. **理由コードの移行** を選択します 。

   [![理由コードを移行する。](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. **福利厚生理由コード移行** ペインでは、Human Resources の理由コードにマッピングする 2 つのオプションがあります。

   - 従業員管理で既存の理由コードを使用するには、**既存の理由コードを使用** から選択します。
     > [!NOTE]
     > 従業員管理で既存の理由コードを使用できるのは、別の福利厚生管理理由コードにまだ移行していない場合のみです。
   - 従業員管理に新しい理由コードを作成するには、**新しい理由コード** に新たな理由コードを入力し、**新しい説明** に説明を入力します。

   [![従業員管理の理由コードへのマッピング。](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

理由コードが Human Resources に移行した後で、福利厚生管理でそれらを使用するオプションは自動的に **はい** に設定 されます。

[![福利厚生管理で理由コードを使用する。](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]