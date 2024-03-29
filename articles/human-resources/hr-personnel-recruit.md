---
title: 職務候補者の採用
description: この記事では、Dynamics 365 Human Resources でどのように候補者を採用するかについて説明します。
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 743c78d3526db2707630229d4cf21531f9641dd6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879253"
---
# <a name="recruit-job-candidates"></a>職務候補者の採用


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources を使用すると、採用要求の管理が簡単になります。 また、職務の候補者が従業員になるまでの移行をシームレスに実行することもできます。 組織で別の採用アプリケーションを使用している場合、採用プロセスには次の手順が含まれる場合があります。<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- 採用要求を Human Resources に入力する。
- 採用アプリケーションから候補者の推薦状を Human Resources で受け取る。
- Human Resources で候補者の承認プロセスを完了する。

別の採用アプリケーションを使用していない場合は、Human Resources で手動で候補者を管理することもできます。

> [!NOTE]
> 管理者または開発者が Human Resources とサードパーティの採用アプリケーションを統合する場合は、[Dataverse 統合の構成](hr-admin-integration-common-data-service.md) および [Dataverse 仮想テーブルの構成](hr-admin-integration-common-data-service-virtual-entities.md) に移動します
>
> [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) からも採用統合アプリを利用できます。
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>マージされたインフラストラクチャで採用依頼を有効にする

HR 採用で採用依頼を送信する場合は、最初に **HR ユーザー エクスペリエンス** と **採用プロセス管理** の機能を有効にする必要があります。

機能を有効にしたら、次の手順にで機能を選択します: 
1. **人事管理** > **設定** > **人事管理パラメーター** に移動します。
2.  **採用** タブで **採用有効化** フィールドを **はい** に設定します。
3. **採用エクスペリエンス** ドロップダウンで **HR 採用** を選択します。  
4. **保存** をクリックします。 

> [!Note] 
> **HR 採用** が選択されると、**採用プロジェクト** (レガシ) は利用できなくなります。 


## <a name="add-a-recruiting-request-location"></a>採用要求の勤務場所の追加

組織に勤務場所が複数ある場合は、勤務場所を追加して、要求者が新しい採用がある勤務場所を選択できるようにできます。 勤務場所は求人情報に記載されます。

1. 検索バーで **採用要求の勤務場所** を入力します。
2. **新規** を選択します。
3. **採用要求の勤務場所** フィールドに、勤務場所の名前を入力します。

    ![採用要求の勤務場所の追加。](./media/hr-recruit-0a-add-location.png)

4. **説明** に場所の説明を入力します。
5. **勤務場所** で、**追加** を選択します。 **新しい住所** ダイアログが表示されたら、場所の住所を入力します。<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![住所の入力。](./media/hr-recruit-0b-address.png)

6. **連絡先情報** で、勤務場所の連絡先の情報を入力します。
7. **保存** を選択します。

## <a name="add-a-recruiting-request"></a>採用要求の追加

管理者は、Human Resources に採用要求を送信できます。 別の採用アプリケーションを使用する場合は、これらの手順を完了すると採用要求が送信され、そのアプリケーションで採用プロセスが開始されます。 それ以外の場合は、この手順を実行して、社内採用プロセスのワークフローを開始します。

1. **従業員セルフ サービス** を選択します。
2. **自分のチーム** タブを選択します。
3. **採用を要求** を選択します。

    ![採用要求の開始。](./media/hr-recruit-1-request-to-recruit.png)

4. **説明**、**職務**、および **予想開始日** フィールドに入力します。

    ![採用要求の完了。](./media/hr-recruit-2-request-to-recruit.png)

5. **続行** を選択します。 希望する職務の採用要求が表示されます。
6. **全般** で **採用担当者** ドロップダウン リストから採用担当者を選択し、**採用依頼場所** ドロップダウン リストから場所を選択します。
7. **職務** で、必要に応じて情報を変更し、**職務から詳細を作成** を選択します。

    ![職務から詳細を作成。](./media/hr-recruit-3-create-details-from-job.png)

    採用依頼の残りの部分には、入力した職務の既定の情報が入力されます。

8. **外部説明** で、外部向け職務明細書を入力します。
9. **職位** で **追加** を選択してから、この採用要求の職位を選択します。<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![職位の追加。](./media/hr-recruit-4-select-position.png)

10. **スキル** で **追加** を選択してからスキルを選択します。
11. **学歴要件** で **追加** を選択してから、**教育** および **教育レベル** ドロップダウン メニューから値を選択します。

    ![学歴要件の追加。](./media/hr-recruit-5-select-educational-requirements.png)

12. **コメント** で、必要に応じてコメントを追加します。
13. **報酬** で **レベル** ドロップダウン リストからレベルを選択してから、必要に応じて **最小しきい値**、**標準職務給**、**最大しきい値** を調整します。
14. 採用要求が完了し採用プロセスを開始する準備ができたら、メニュー バーの **有効化** を選択します。

    ![採用要求の有効化。](./media/hr-recruit-6-activate-recruit-request.png)

15. **保存** を選択します。

## <a name="view-and-edit-your-recruiting-requests"></a>採用要求の表示と編集

マネージャーに要求を表示する場合は、次の操作を行います。

1. **従業員セルフ サービス** を選択します。
2. **自分のチーム** タブを選択します。
3. **自分のチームの情報** で、**採用要求** タブを選択します。

    ![採用要求タブの選択。](./media/hr-recruit-7-recruiting-requests.png)

4. 採用要求を表示または編集するには、グリッドで選択します。

HR のプロフェッショナルにすべての採用要求を表示するには、次の操作を行います。

1. **人事管理** を選択する。
2. **採用要求** を選択する。

    ![人事管理で採用要求を表示する。](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. 採用要求を表示または編集するには、グリッドで選択します。

## <a name="add-or-edit-a-candidate-profile"></a>候補者プロファイルの追加または編集

採用要求を管理するために組織が別のアプリケーションと統合している場合、採用要求はそのアプリケーションに転送されます。 その後、採用アプリケーションが候補者の情報を Human Resources に送り返します。 それ以外の場合は、独自の内部採用プロセスに従って、候補者の情報を手動で入力できます。

1. **人事管理** を選択する。
2. **リンク** を選択します。
3. **採用** で **候補者** を選択します。

    ![候補者の表示。](./media/hr-recruit-9-candidates.png)

4. 候補者を追加するには、**新規** を選択します。 既存の候補者を編集するには、リストから候補者を選択し、**編集** を選択します。 候補者のプロファイルが表示されます。
5. **候補者の概要** で、必要に応じて候補者情報を入力または編集します。
6. **採用要求** で、候補者にリンクする採用要求を選択します。 必要に応じて、**推定開始日**、**採用マネージャー**、**職位**、**説明** のフィールドに入力します。

    ![採用要求へのリンク。](./media/hr-recruit-10-link-to-recruiting-request.png)

7. 候補者のレコードに含める次の領域のすべての情報を入力します。

    - **備考**
    - **職務経験**
    - **連絡先情報**
    - **教育**
    - **スキル**
    - **証明書**
    - **審査**

8. **保存** を選択します。

## <a name="hire-a-candidate"></a>候補者の採用

候補者を採用する準備ができたら、次の手順に従って採用者から従業員へ移行します。

1. **候補者** ページで、**採用** を選択します。

    ![候補者の採用。](./media/hr-recruit-11-hire.png)

2. **新規採用** ページにある **詳細** で、すべてのフィールドに入力します。

    ![新入社員の詳細の入力。](./media/hr-recruit-12-hire-new-worker.png)

3. **職位の詳細** で、必要に応じて情報を確認および変更します。
4. **オンボード チェックリスト** で、この従業員に関連するオンボード チェックリストを選択します。
5. **続行** を選択して従業員レコードを作成します。

    > [!NOTE]
    > 組織のワークフローによっては、候補者レコードが従業員レコードに移行する前に他の承認ステップを実行する場合があります。

## <a name="decide-not-to-hire-a-candidate"></a>候補者の不採用

候補者を採用しない場合は、次の手順に従って、候補者を審査プロセスから削除します。 

1. **候補者** ページで、**不採用** を選択します。

    ![候補者の不採用。](./media/hr-recruit-13-do-not-hire.png)

2. **理由コード** を選択し、コメントを記入します。
3. **OK** を選択します。

## <a name="dismiss-a-candidate"></a>候補の消去

必要に応じて、採用後に候補を消去することができます。 たとえば、候補者が採用を拒否したり、初日に出勤しなかったりする場合です。

- **候補者** ページで、**候補を消去** を選択します。

    ![候補の消去。](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>参照

[構成 Dataverse 仮想テーブル](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[従業員の編成](hr-personnel-departments-jobs-positions.md)<br>
[職務のコンポーネントの設定](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
