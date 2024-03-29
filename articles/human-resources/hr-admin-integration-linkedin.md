---
title: LinkedIn Talent Hub との統合
description: この記事では、Microsoft Dynamics 365 Human Resources と LinkedIn タレント ハブ間の統合を設定する方法について説明します。
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df4a0a4dec078392ba835318450f5983a6e95c97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887751"
---
# <a name="integrate-with-linkedin-talent-hub"></a>LinkedIn Talent Hub との統合

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!IMPORTANT]
> この記事で説明されている Dynamics 365 Human Resources と LinkedIn Talent Hub との統合は、2021 年 12 月 31 日に終了しました。 この日付以降、統合サービスは使用できません。 統合サービスを使用していない組織では、終了する前でもサービスを実装することはできません。

[LinkedIn タレント ハブ](https://business.linkedin.com/talent-solutions/talent-hub) は採用管理システム (ATS) のプラットフォームです。 これにより、従業員の調達、管理、雇用をすべて 1 か所で行うことができます。 Microsoft Dynamics 365 Human Resources を LinkedIn タレント ハブと統合することにより、職位に採用された応募者の従業員レコードを Human Resources で簡単に作成することができます。

## <a name="setup"></a>段取り

LinkedIn タレント ハブとの統合を有効にするには、システム管理者が設定作業を完了しておく必要があります。 まず、Power Apps 環境でユーザーおよびセキュリティ ロールを設定して、データを Human Resources に書き込むための適切なアクセス許可を LinkedIn タレント ハブに付与する必要があります。

### <a name="link-your-environment-to-linkedin-talent-hub"></a>環境を LinkedIn タレント ハブにリンク

1. [LinkedIn タレント ハブ](https://business.linkedin.com/talent-solutions/talent-hub) を開きます。

2. ユーザー ドロップダウン メニューで、**製品設定** を選択します。

3. 左のナビゲーション ペインにある **詳細** セクションで、**統合** を選択します。

4. Microsoft Dynamics 365 Human Resources の統合に対して **承認** を選択します。

5. **Dynamics 365 Human Resources** ページで、LinkedIn タレント ハブをリンクする環境を選択し、**リンク** を選択します。

    ![LinkedIn タレント ハブのオンボード。](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > ユーザー アカウントに Human Resources 環境と関連する Power Apps 環境の両方への管理者アクセス権がある環境にのみリンクできます。 Human Resources リンク ページに環境が表示されない場合は、テナントに Human Resources 環境のライセンスがあることと、リンク ページにサインインしたユーザーに Human Resources 環境と Power Apps 環境の両方に対する管理者権限があることを確認してください。

### <a name="create-a-power-apps-security-role"></a>Power Apps セキュリティ ロールを作成する

1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。

2. **環境** の一覧で、LinkedIn タレント ハブのインスタンスをリンクする Human Resources 環境に関連付けられている環境を選択します。

3. **設定** を選択します。

4. **ユーザー + アクセス許可** ノードを展開し、**セキュリティ ロール** を選択します。

5. **セキュリティ ロール** ページのツールバーで、**新しいロール** を選択します。

6. **詳細** タブで、**LinkedIn タレント ハブ HRIS の統合** など、ロールの名前を入力します。

7. **カスタマイズ** タブで、次のエンティティに対する組織レベルの **読み取り** アクセス許可を選択します:

    - エンティティ
    - フィールド
    - 続柄

8. セキュリティ ロールを保存して閉じます。

### <a name="create-a-power-apps-application-user"></a>Power Apps アプリケーション ユーザーの作成

LinkedIn タレント ハブ アダプターに対してアプリケーション ユーザーを作成し、Power Apps 環境に候補者レコードを書き込むアクセス許可をアダプターに付与する必要があります。

1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。

2. **環境** の一覧で、LinkedIn タレント ハブのインスタンスをリンクする Human Resources 環境に関連付けられている環境を選択します。

3. **設定** を選択します。

4. **ユーザー + アクセス許可** ノードを展開し、**ユーザー** を選択します。

5. **Dynamics 365 でユーザーの管理** を選択します。

6. 一覧上にあるドロップダウン メニューを使用して、ビューを既定の **有効なユーザー** ビューから **アプリケーション ユーザー** に変更します。

    ![アプリケーション ユーザー ビュー。](./media/hr-admin-integration-power-apps-application-users.jpg)

7. ツール バーの **新規** を選択します。

8. **新規ユーザー** ページで、次の手順に従います:

    1. **ユーザー タイプ** フィールド値を **アプリケーション ユーザー** に変更します。
    2. **ユーザー名** フィールドを **Dynamics365 HR LinkedIn HRIS の統合** に設定します。
    3. **アプリケーション ID** を **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** に設定します。
    4. **名**、**姓**、**代表電子メール** フィールドに値を入力します。
    5. ツール バーの **保存 \& 終了** を選択します。

### <a name="assign-a-security-role-to-the-new-user"></a>セキュリティ ロールを新規ユーザーに割り当てる

前のセクションで新規アプリケーション ユーザーを保存して終了した後、**ユーザーの一覧** ページに戻ります。

1. **ユーザーの一覧** ページで、ビューを **アプリケーション ユーザー** に変更します。

2. 前のセクションで作成したアプリケーション ユーザーを選択します。

3. ツール バーの **ロールの管理** を選択します。

4. 以前に統合用に作成したセキュリティ ロールを選択します。

5. **OK** を選択します。

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Human Resources に Azure Active Directory アプリを追加

1. Dynamics 365 Human Resources で、**Azure Active Directory アプリケーション** ページを開きます。
2. 一覧に新規レコードを追加し、次のフィールドを設定します:

    - **クライアント ID**: **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** を入力します。
    - **名前**: 以前に作成した Power Apps セキュリティ ロール (**LinkedIn タレント ハブ HRIS の統合** など) の名前を入力します。
    - **ユーザー ID**: 人事管理でデータを書き込むアクセス許可を持つユーザーを選択します。

### <a name="create-the-table-in-dataverse"></a>Dataverse でのテーブルの作成

> [!IMPORTANT]
> LinkedIn タレント ハブは、Dataverse for Human Resources の仮想テーブルに依存します。 設定でのこの手順の前提条件として、仮想テーブルを構成する必要があります。 仮想テーブルの構成方法については、[Dataverse 仮想テーブルの構成](./hr-admin-integration-common-data-service-virtual-entities.md) を参照してください。

1. Human Resources で、**Dataverse の統合** ページを開きます。

2. **仮想テーブル** タブを選択します。

3. エンティティの一覧をエンティティ ラベルでフィルターして、**LinkedIn がエクスポートした候補者** を検索します。

4. エンティティを選択し、**生成/更新** を選択します。

## <a name="exporting-candidate-records"></a>候補者レコードのエクスポート

設定が完了した後、採用担当者と人事管理 (HR) 担当者は、LinkedIn タレント ハブの **HRIS へのエクスポート** 機能を使用して、採用された候補者のレコードを LinkedIn タレント ハブから Human Resources にエクスポートできます。

### <a name="export-records-from-linkedin-talent-hub"></a>LinkedIn タレント ハブからのレコードのエクスポート

候補者が採用プロセスを通過し採用された後は、その候補者レコードを LinkedIn タレント ハブから Human Resource にエクスポートできます。

1. LinkedIn タレント ハブで、新しい従業員を採用したプロジェクトを開きます。

2. 候補者レコードを選択します。

3. **ステージの変更** を選択し、**雇用** を選択します。

4. 候補者の省略記号メニュー (**...**) で、**HRIS へのエクスポート** を選択します。

5. **HRIS へのエクスポート** ペインで、エクスポートする必要がある情報を入力します:

    - **HRIS プロバイダー** フィールドで、**Microsoft Dynamics 365 Human Resources** を選択します。
    - **開始日** フィールドで、新規従業員に対する値を選択します。
    - **役職** フィールドに、新規従業員の役職を入力します。
    - **場所** フィールドに、従業員が拠点とする場所を入力します。
    - 従業員の電子メール アドレスを入力または確認します。

![LinkedIn タレント ハブの HRIS ペインにエクスポート。](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Human Resources でのオンボードの完了

LinkedIn タレント ハブから Human Resources にエクスポートされた候補者レコードは、**人事管理** ページの **採用候補者** セクションに表示されます。

1. Human Resources で、**人事管理** ページを開きます。

2. **採用候補者** セクションで、選択した候補に対して **採用** を選択します。

3. **新しい作業者の採用** ダイアログ ボックスでレコードを確認し、必要な情報を追加します。 また、候補者が採用された職位番号を選択することもできます。

必要な情報を入力した後、従業員レコードの作成および従業員のオンボードに関する標準プロセスを続けることができます。

次の詳細がインポートされ、新しい従業員レコードに含まれます:

- 名
- 姓
- 雇用開始日
- メール アドレス
- 電話番号

## <a name="see-also"></a>参照

[構成 Dataverse 仮想テーブル](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Microsoft Dataverse とは](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
