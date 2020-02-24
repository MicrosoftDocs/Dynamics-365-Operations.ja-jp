---
title: 給付金管理の概要
description: Dynamics 365 Human Resources の給付金管理プレビュー機能の概要。 使いやすいオンライン エクスペリエンスで、従業員に拡張された給付金オプションを提供します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029466"
---
# <a name="benefits-management-overview"></a>給付金管理の概要

[!include [banner](includes/preview-feature.md)]

競争力を維持するには、最高の従業員を獲得し維持するために、充実したメリットを提供する必要があります。 医療や歯科などの標準的な利点に加えて、採用支援、レクリエーション プログラム、および衣料手当などの拡張サービスを提供することもできます。 Microsoft Dynamics 365 Human Resources の給付金管理プレビュー機能には、さまざまな給付金オプションをサポートする柔軟なソリューションが用意されています。 人事管理では、製品を紹介するための使いやすい従業員エクスペリエンスも含まれています。

- 拡張された給付金プランを使用すると、独自の給付金プランを作成および管理し、複雑な給付金のレート テーブルとネストされた階層をサポートできます。 より簡単な従業員エクスペリエンスのために、給付金プログラム、バンドル、および自動登録ルールを容易に作成できます。

- レックス クレジット プログラムでは、退職やその他のライフ イベントをサポートします。

- 広範な適格性ルールによって、適切な従業員が適切な利益を得ることができます。

- オンライン給付金の登録は、従業員にとって簡単なエクスペリエンスです。

- 修飾ライフ イベントの処理は、従業員セルフ サービスと統合し、将来のライフ イベントもサポートします。

デモ データにアクセスする場合は、サンドボックス環境を再配置する必要があります。

直接のフィードバックまたはレポート問題については、D365BenefitsPreview@microsoft.com で提供可能です。

## <a name="benefits-management-known-issues"></a>給付金管理に関する既知の問題

### <a name="eligibility-processing"></a>適格性処理中

1-5X 給与、給与の % および均一額の補償金額を使用する給付金の適格性を実行する場合、**給付金の詳細**日付を**従業員履歴**の**従業員の雇用開始日**に設定します。 また、**就業時間**、**支払頻度**および**年間給付金の給与額**を含む必要があります。 作業者に固定報酬がある場合、**勤務時間**および**支払頻度**を入力します。 年収額が計算されます。 従業員に給与がかかる場合は、**作業時間**を入力する必要はありません。 新しい従業員を作成する場合は、先に固定報酬を入力することをお勧めします。 給付金の詳細記録を更新するには、**従業員 > 作業員の履歴 > 従業員の詳細**に移動します。 日付を作業者の雇用開始日に調整します。

### <a name="employee-self-service"></a>従業員セルフ サービス

生命保険の補償金額を更新する場合、従業員の金額は計算されません。 たとえば、従業員に生命保険プランが提供されている場合は、1,000 ドルの補償につき 0.36 ドルの費用で、最大 50,000 ドルの補償を選択できます。  従業員が補充金額を更新すると、従業員に関連付けられている原価はゼロのままになります。

その計画タイプの単一選択のみを許可する給付金計画の場合、ユーザーは計画を選択した後に、計画を放棄しようとするとエラーを受け取ります。 たとえば、ユーザーが医療プランを選択してカートに配置したとします。 その後、ユーザー は別の医療プランの**放棄**を選択します。 ユーザーにはエラーが表示されます。

## <a name="enable-benefits-management"></a>給付金管理を有効にする

給付金管理はプレビュー機能であり、**サンドボックス**環境でのみ使用できます。 これらの記事では、人事管理でプレビュー機能を有効にする方法について説明します。 また、人事管理のプレビュー機能のうち、一度給付金管理をオンにして、給付金管理に置き換わるか無効になるかを示します。

- [機能の管理](hr-admin-manage-features.md)
- [プレビュー機能: 給付金管理](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>給付金管理の構成

従業員の給付金計画を作成する前に、その計画のオプションを構成する必要があります。

- [給付金管理パラメーターを設定](hr-benefits-setup-parameters.md)
- [適格性ルールとオプションを構成](hr-benefits-setup-eligibility-rules.md)
- [個人の連絡先適格性オプションを構成](hr-benefits-setup-contact-eligibility-options.md)
- [補償オプションを作成](hr-benefits-setup-coverage-options.md)
- [支払頻度の設定](hr-benefits-setup-payment-frequencies.md)
- [将来のライフ イベントの構成](hr-benefits-setup-life-event-types.md)
- [プラン タイプの作成](hr-benefits-setup-plan-types.md)
- [理由コードの設定](hr-benefits-setup-reason-codes.md)
- [階層コードの設定](hr-benefits-setup-tier-codes.md)
- [レートの構成](hr-benefits-setup-rates.md)
- [控除の構成](hr-benefits-setup-deductions.md)
- [待機日数の構成](hr-benefits-setup-waiting-days.md)
- [待機期間の構成](hr-benefits-setup-waiting-periods.md)
- [丸めルールの設定](hr-benefits-setup-rounding-rules.md)
- [従業員カテゴリの作成](hr-benefits-setup-employment-categories.md)
- [雇用タイプを設定](hr-benefits-setup-employment-types.md)
- [従業員のセルフ サービスを構成](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>給付金プランの作成

これらの記事では、バンドルおよびフレックス クレジット プログラムなどの給付金プランの作成方法を示します。

- [給付金プランの設定](hr-benefits-plans-setup.md)
- [作業者の給付金プランの作成](hr-benefits-plans-worker.md)
- [フレックス クレジット プログラムの設定](hr-benefits-plans-flex-credit-programs.md)
- [将来のライフ イベントの構成](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>給付金プランの処理

変更を有効にするには、いくつかの変更を処理する必要があります。

- [登録の適格性を処理](hr-benefits-process-enrollment-eligibility.md)
- [ライフ イベントの処理](hr-benefits-process-life-events.md)
- [ライフ イベントの変更の処理](hr-benefits-process-life-event-changes.md)
- [ライフ イベントの適格性の処理](hr-benefits-process-life-event-eligibility.md)
- [レート変更の処理](hr-benefits-process-rate-changes.md)

