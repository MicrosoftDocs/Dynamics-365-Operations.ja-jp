---
title: 福利厚生の管理の概要
description: Dynamics 365 Human Resources の福利厚生の管理機能の概要。 使いやすいオンライン エクスペリエンスで、従業員に拡張された給付金オプションを提供します。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 91a4425b4f020f90843bb3b0b280b7ee28463670
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230157"
---
# <a name="benefits-management-overview"></a>給付金管理の概要

競争力を維持するには、最高の従業員を獲得し維持するために、充実したメリットを提供する必要があります。 医療や歯科などの標準的な利点に加えて、採用支援、レクリエーション プログラム、および衣料手当などの拡張サービスを提供することもできます。 Microsoft Dynamics 365 Human Resources の福利厚生の管理には、さまざまな福利厚生オプションをサポートする柔軟なソリューションが用意されています。 人事管理では、製品を紹介するための使いやすい従業員エクスペリエンスも含まれています。

- 拡張された給付金プランを使用すると、独自の給付金プランを作成および管理し、複雑な給付金のレート テーブルとネストされた階層をサポートできます。 より簡単な従業員エクスペリエンスのために、給付金プログラム、バンドル、および自動登録ルールを容易に作成できます。

- レックス クレジット プログラムでは、退職やその他のライフ イベントをサポートします。

- 広範な適格性ルールによって、適切な従業員が適切な利益を得ることができます。

- オンライン給付金の登録は、従業員にとって簡単なエクスペリエンスです。

- 認定されたライフ イベント処理は将来のライフ イベントをサポートします。

デモ データにアクセスする場合は、サンドボックス環境を再配置する必要があります。

## <a name="benefits-management-known-issues"></a>給付金管理に関する既知の問題

### <a name="flex-credit-programs"></a>フレックス クレジット プログラム

フレックス クレジット プログラムに定義された合計クレジット値は、**作業者の福利厚生計画** フォームには表示されません。 また、フレックス クレジット プログラムに **なし** の比例配分ルールを設定すると、計画を選択して確認するときに、**作業者の福利厚生計画** フォームでエラーが発生します。

## <a name="enable-benefits-management"></a>給付金管理を有効にする

この記事では、Human Resources の機能を有効にする方法について説明します。 また、福利厚生の管理を有効にすると、福利厚生の管理が置換されるか無効になる Human Resources の既存機能も示されます。

> [!IMPORTANT]
> **実稼働** 環境で福利厚生の管理を有効にした後、無効にすることはできません。 **実稼働** 環境で有効にする前に、**サンドボックス** 環境で福利厚生の管理を有効にしてテストすることをお勧めします。 従来の福利厚生機能と新しい福利厚生の管理機能には大きな違いがあり、追加の設定が必要であり、実稼働前にテストする必要があります。

- [機能の管理](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>従業員情報のコンフィギュレーション

従業員を福利厚生に登録する前に、必要な情報を提供する必要があります。 従業員を開始日に **固定報酬プラン** に登録し、**従業員** フォームの **従業員の詳細** で **給付金支払頻度** を選択する必要があります。

性別または年齢に基づくレートを使用する給付金プランを作成する場合、従業員が福利厚生コストを計算するには、生年月日と性別を入力する必要があります。

## <a name="configure-benefits-management"></a>福利厚生の管理のコンフィギュレーション

従業員の給付金計画を作成する前に、その計画のオプションを構成する必要があります。

- [給付金管理パラメーターを設定](hr-benefits-setup-parameters.md)
- [適格性ルールとオプションを構成](hr-benefits-setup-eligibility-rules.md)
- [個人の連絡先の適格性オプションのコンフィギュレーション](hr-benefits-setup-contact-eligibility-options.md)
- [補充オプションの作成](hr-benefits-setup-coverage-options.md)
- [支払頻度の設定](hr-benefits-setup-payment-frequencies.md)
- [ライフ イベント タイプのコンフィギュレーション](hr-benefits-setup-life-event-types.md)
- [計画タイプの作成](hr-benefits-setup-plan-types.md)
- [理由コードの設定](hr-benefits-setup-reason-codes.md)
- [層コードの設定](hr-benefits-setup-tier-codes.md)
- [レートのコンフィギュレーション](hr-benefits-setup-rates.md)
- [控除のコンフィギュレーション](hr-benefits-setup-deductions.md)
- [待機日数のコンフィギュレーション](hr-benefits-setup-waiting-days.md)
- [待機期間のコンフィギュレーション](hr-benefits-setup-waiting-periods.md)
- [丸めルールの設定](hr-benefits-setup-rounding-rules.md)
- [雇用カテゴリの作成](hr-benefits-setup-employment-categories.md)
- [雇用タイプを設定](hr-benefits-setup-employment-types.md)
- [従業員のセルフ サービスを構成](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>給付金プランの作成

これらの記事では、バンドルおよびフレックス クレジット プログラムなどの給付金プランの作成方法を示します。

- [福利厚生計画の設定](hr-benefits-plans-setup.md)
- [フレックス クレジット プログラムの設定](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>福利厚生計画の処理

変更を有効にするには、いくつかの変更を処理する必要があります。

- [登録の適格性を処理](hr-benefits-process-enrollment-eligibility.md)
- [ライフ イベントの処理](hr-benefits-process-life-events.md)
- [ライフ イベントの変更の処理](hr-benefits-process-life-event-changes.md)
- [ライフ イベントの適格性の処理](hr-benefits-process-life-event-eligibility.md)
- [レート変更の処理](hr-benefits-process-rate-changes.md)

