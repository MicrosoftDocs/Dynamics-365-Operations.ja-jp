---
title: Regulatory Configuration Service
description: このトピックでは、Regulatory Configuration Service (RCS) の機能の概要を示し、サービスにアクセスする方法について説明します。
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890803"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) は、コードなし/ロー コードのグローバリゼーション機能のための、スタンドアロン デザイナーおよびライフサイクル管理サービスです。 RCS を使用すると、グローバリゼーションの関係者は、開発者を関与させることなく、税、電子請求、規制に関する報告、銀行、およびビジネス ドキュメントの主要なグローバリゼーション領域を拡張およびカスタマイズできます。 このコードなし/ロー コードのグローバリゼーション アプローチにより、グローバリゼーションの作成または拡張がより簡単に、より迅速に、よりコスト効率が高くなります。

RCS は次の機能を提供します。

- 電子レポート (ER) によって提供されるすべての機能のサポート。
- 新しいグローバリゼーション マイクロサービスを構成する前提条件。
- 電子請求のサポート。 詳細については、[電子請求](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga) を参照してください。
- 税計算のサポート。 詳細については、[税サービス](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview) を参照してください。
- マルチコンポーネント機能のライフサイクル管理を簡素化し、アクションを構成し、機能パラメーターを設定するための追加機能を提供する、新しいグローバリゼーション機能のサポート。 詳細については、[Regulatory Configuration Service – グローバリゼーション サービスに対する簡素化されたグローバリゼーション機能の管理](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services) を参照してください。
- Microsoft Dynamics Lifecycle Services (LCS) を使用せずに構成管理を簡素化するための、グローバル リポジトリでのカスタム構成の集中公開、保存、および共有のサポート。

## <a name="access-rcs"></a>アクセス RCS

[Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/) から RCS に登録またはサインインできます。

![RSC 登録/サインイン](media/202103_RCS%20Marketing%20page_updated_1.jpg)

**Regulatory Configuration Service** ページで、サービスの使用に関する追加の条件を確認して承認し、次のいずれかのボタンを選択します。

- 初めてサービスを利用するユーザーで、組織にサービス環境をプロビジョニングするためにビジネス メール アドレスを使用している場合に **登録** する
- サービスに以前にサインアップした、組織環境にアクセスしたい場合に **サインイン** する

## <a name="regional-availability"></a>地域の可用性

通常、RCS は次の地域で使用できます。

- 米国
- インド
- フランス
- ヨーロッパ

地域の完全な一覧については [Dynamics 365 および Power Platform: 使用可能性、データの場所、言語、およびローカライズ](https://aka.ms/dynamics_365_international_availability_deck) を参照してください。

## <a name="related-rcs-documentation"></a>関連する RCS ドキュメント

関連コンポーネントの詳細については、次のドキュメントを参照してください。

- **グローバル リポジトリ:**

    - [ER コンフィギュレーションの作成 & グローバル リポジトリへのアップロード](rcs-global-repo-upload.md)
    - [グローバル リポジトリ でのコンフィギュレーションの共有](rcs-global-repo-share-configuration.md)
    - [グローバル レポジトリの拡張フィルター処理](enhanced-filtering-global-repo.md)
    - [ER コンフィギュレーションをグローバル リポジトリからダウンロードする](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [グローバル リポジトリのコンフィギュレーションを中止する](discontinuing-configurations-rcs-global-repo.md)

- **グローバリゼーション機能:**

    - [Regulatory Configuration Service (RCS) - グローバリゼーション機能](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)