---
title: Dynamics 365 Talent の廃止 - Attract および Onboard アプリ
description: このトピックでは、Dynamics 365 Talent の廃止について説明します - Attract および Onboard アプリ。
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e17b92621f05ad8483a7c578bfaece58a530df2d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692005"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract および Onboard アプリの廃止


2019 年 12 月、Dynamics 365 Talent - Attract および Onboard アプリを 2022 年 2 月 1 日に廃止する旨を発表し、顧客には計画期間が 2 年与えられました。

これらのアプリの廃止に関する詳細については、次を参照してください。
 - [Dynamics 365 Talent - Attract および Dynamics 365 Talent: Onboard アプリの廃止](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Dynamics 365 Human Resources で従業員の質を向上させる](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

マイクロソフトは Dynamics 365 Human Resources へのサポートを続行し、複数の領域に広がるデータ駆動型の従業員エクスペリエンスを構築するために必要な従業員に関するインサイトを顧客が獲得できるようにします。

- 報酬
- メリット
- 休暇
- コンプライアンス
- Payroll
- パフォーマンス フィードバック
- トレーニングおよび証明
- セルフサービス プログラム

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent アプリの廃止に関する FAQ

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>2022 年 2 月 1 日から開始される Dynamics 365 Talent - Attract および Onboard アプリの両方で体験できるユーザー エクスペリエンスはどのようなものですか。

ユーザーはアプリケーションを使用することができなくなり、廃止ページにリダイレクトされます。

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>2022 年 2 月 1 日以降でも、Dynamics 365 Talent - Attract および Onboard アプリのデータをエクスポートすることができますか。
  
いいえ、廃止は 2019 年 12 月に発表され、必要なエクスポート機能は 2022 年 2 月 1 日まで提供されました。 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Dataverse 内の Dynamics 365 Talent - Attract および Onboard アプリに関連した顧客のデータは、2022 年 2 月 1 日移行に削除されますか。

いいえ、人材管理タレント ソリューションが削除またはアンインストールした場合を除いては、廃止後でも Dataverse エンティティは、顧客の Microsoft Dataverse 環境に残ります。

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Talent 環境名がわかります。 Dataverse の Attract および Onboard データは、どのように表示できますか。

1.  Power Apps にサインイン: https://make.powerapps.com
2.  Attract および Onboard データを表示する環境を選択します。
3.  **Dataverse > テーブル** へ移動します。 
4.  **検索** に「msdyn_」と入力します。 "msdyn_" + テーブル名 (例: msdyn_candidate) で始まるテーブルの一覧が表示される場合は、Attract および Onboard データで構成された環境が検出されます。

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Talent 環境名がわかりません。 Dynamics 365 Talent: Attract と Dynamics 365 Talent: Onboard アプリケーション用のデータを含む環境を確認するにはどうしたらいいですか。

1)  Power Platform 管理センターにサインインします: https://admin.powerplatform.microsoft.com/
2)  **環境** を選択します。
3)  評価する特定の環境を選択します。
4)  **リソース > Dynamics 365 アプリ** を選択します。
5)  **HCM Talent** ソリューションがインストールされている場合、この環境にはそのソリューション内に Attract および Onboard 格納データがあります。 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> **HCM Talent** ソリューションは、Dynamics 365 Human Resources でも使用されます。
