---
title: ATS 統合 API のサーバー間認証
description: この記事では、Dynamics 365 Human Resources 申請者追跡システム (ATS) 統合 API の統合に対するサーバー間認証を設定する方法について説明します。
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: de3dc29c5366996276c02576eba27f7e831e4ccf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879369"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>ATS 統合 API のサーバー間認証


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources 申請者追跡システム (ATS) 統合 API のアプリケーション統合に対するサーバー間認証を設定する方法について説明します。 Microsoft Dataverse の仮想テーブルおよび関連するデータにアクセスするためにサービス プリンシパルが管理する必要のあるいくつかのセキュリティの階層があります。 ユーザーに、Microsoft Power Platform の Dataverse 仮想テーブルへのアクセス、および Dynamics 365 Human Resources のデータへのアクセス許可を与える必要があります。

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Power Platform の Dataverse 仮想テーブルへのアクセスを有効にする

Power Platform で Dataverse 仮想テーブルへのアクセスを有効にするための最初の手順として、Dataverse 仮想テーブル エンドポイントに対する認証用に Power Platform でアプリケーションを設定します。 これを行う手順は、[Microsoft Dataverse 開発者ガイド](/powerapps/developer/data-platform)で説明されています。

  - 単一テナントのアプリ登録の場合: [単一テナントのサーバー間認証を使用する](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - マルチ テナントのアプリ登録の場合: [マルチ テナントのサーバー間認証を使用する](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>ATS 統合のセキュリティ ロールの作成

アプリケーション ユーザーを作成した後の手順の 1 つとして、エンドポイントに対するアプリケーションのアクセスを定義するセキュリティ ロールにユーザーを割り当てます。 これは、単一テナントのアプリ登録に対する[アプリケーション ユーザー作成](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation)の手順 7、およびマルチ テナント登録の[アプリケーション ユーザーのセキュリティ ロールの作成](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user)です。 

アプリケーション ユーザーを割り当てるロールには、ATS 統合に使用されるデータ エンティティへのアクセス権が必要です。 このロールはそのままでは存在しないため、新しいセキュリティ ロールを作成する必要があります。 新しいロールは、[セキュリティ ロールの作成](/power-platform/admin/create-edit-security-role#create-a-security-role)で示した手順に従って作成できます。

新しいロールには、少なくとも、新しいロールの **カスタム エンティティ** タブにある次のエンティティへの適切なアクセス権を割り当てる必要があります。 統合で、より広範なアプリケーション データを使用する場合は、追加のエンティティが必要になる場合があります。 新しいロールが作成された後、そのロールをアプリケーション ユーザーに割り当てることができます。

  - 基本作業者 (mshr)
  - 採用候補者 (mshr)
  - 証明書コンピテンシー (mshr)
  - 証明書タイプ (mshr)
  - 法人
  - 報酬ジョブ機能 (mshr)
  - 報酬ジョブ タイプ (mshr)
  - 国/地域 (mshr)
  - 部署 (mshr)
  - 教育コンピテンシー (mshr)
  - 教育学位 (mshr)
  - 教育訓練 (mshr)
  - 学歴要件 (mshr)
  - ID (mshr)
  - ID タイプ (mshr)
  - 機関 (mshr)
  - 発行機関 (mshr)
  - 職務の報酬 (mshr)
  - 職務 (mshr)
  - 教育レベル (mshr)
  - 関係者の連絡先 (mshr)
  - 人員 (mshr)
  - 個人の住所 (mshr)
  - 審査 (mshr)
  - 職位タイプ (mshr)
  - 職位 V2 (mshr)
  - 職務経験コンピテンシー (mshr)
  - 評価レベル (mshr)
  - 評価モデル (mshr)
  - 理由コード (mshr)
  - 採用要求 (mshr)
  - 採用要求場所 (mshr)
  - 採用要求職位 (mshr)
  - 採用要求スキル (mshr)
  - 審査タイプ (mshr)
  - スキル コンピテンシー (mshr)
  - スキル (mshr)
  - 職位 (mshr)
  - 退役軍人ステータス (mshr)
  - 作業者 (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Human Resources データへのアプリケーションのアクセス許可の付与

次に、Human Resources アプリケーションのユーザーにリンクすることで、アプリケーションに Human Resources データへの適切なアクセス許可が付与されます。 アプリケーション ユーザーの場合、Dataverse 仮想テーブルを介したサーバー間の呼び出しは、アクションを開始する Dataverse のユーザー (アプリ) の ID に関連して実行されます。 仮想テーブル アダプター サービスは、Human Resources で関連したユーザーを検索し、そのユーザーのコンテキストでクエリを実行します。 つまり、統合アプリケーションに必要なデータへのアクセス許可を提供するために、適切なロールが割り当てられた Human Resources でユーザーを作成する必要があります。

Human Resources ユーザーには、Human Resources データに対する適切なアクセス許可を割り当てる必要があります。 **採用アプリケーション** (HcmRecruitingIntegrator) ロールは、採用データと統合するために必要な主なエンティティの権限で利用できます。 このロールを **ユーザー** ページのアプリケーション ユーザーに割り当て、データへの適切なアクセス権を付与できます。 Human Resources セキュリティ ロールの詳細については、[ロールベース セキュリティ](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security)を参照してください。

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>適切なアクセス許可を持つ新しいユーザーの設定

適切なアクセス許可を持つ新しいユーザーを設定するには、次の手順を実行します。

  1. Human Resources の **ユーザー** ページを開き、**新規** を選択します。
  2. 新しいアプリケーション ユーザーの **ユーザー ID** と **ユーザー名** を入力します。 たとえば、「RecruitingIntegration」と入力できます。

      > [!NOTE]
      > Microsoft Azure Active Directory (Azure AD) のユーザー アカウントや電子メール アドレスがアプリに存在しない場合は、ユーザーの電子メール アドレスとプロバイダー フィールドに「RecruitingApp」のように入力できます。

  3. **ユーザーのロール** クイック タブで、**ロールの割り当て** アクションを選択します。
  4. **ユーザーへのロールの割り当て** ウィンドウで、**採用アプリケーション** を選択して、**OK** を選択します。
  5. 新しいユーザー レコードを保存します。

### <a name="link-the-new-human-resources-user-to-the-application"></a>新しい Human Resources ユーザーのアプリケーションへのリンク

ユーザーの作成後に、**Azure Active Directory アプリケーション** フォームでアプリケーションのレコードを作成し、Human Resources ユーザーにアプリをリンクする必要があります。

  1. **Azure Active Directory アプリケーション** フォームを開き、**新規** を選択します。
  2. **クライアント ID** フィールドに、アプリケーションに対して作成したアプリケーション ユーザーのクライアント ID を入力します。
  3. **名前** フィールドに、統合アプリケーションの名前を入力します。
  4. **ユーザー ID** フィールドで、採用統合用に作成された新しい Human Resources ユーザーを選択します。
  5. 新しいレコードを保存します。

その後、Human Resources データへのアクセス許可が、採用アプリケーションの統合に必要なデータのみに限定されます。

## <a name="see-also"></a>参照

[職務候補者の採用](hr-personnel-recruit.md)<br>
[Microsoft Dataverse とは](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse Web API を使用する](/powerapps/developer/data-platform/webapi/overview)<br>
[Web API を使用したオプション セットの作成と更新](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
