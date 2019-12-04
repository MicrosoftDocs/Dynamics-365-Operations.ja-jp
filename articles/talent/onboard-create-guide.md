---
title: Dynamics 365 Talent - Onboard を使用した研修用ガイドの作成と送信
description: このトピックでは、Microsoft Dynamics 365 Talent - Onboard アプリを使用して新規採用者向けの研修用ガイドを作成する方法について説明します。 このタスクは、人事管理 (HCM) の採用から退職までの戦略における重要な第一歩です。
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a095fe97b05898403b501763204a462ee8dcc12a
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814631"
---
# <a name="create-and-send-an-onboarding-guide-by-using-dynamics-365-talent---onboard"></a>Dynamics 365 Talent - Onboard を使用した研修用ガイドの作成と送信

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Onboard では、自分で作成したテンプレートもしくはギャラリーで使用できるテンプレートから、または最初から研修用ガイドを作成できます。

研修用ガイドを作成したら、新規採用者に送信できます。 または、Onboard アプリからダウンロードした Microsoft Excel ファイルで指定した複数の新規採用者に送信することもできます。

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>テンプレートから研修用ガイドを作成し、1 人の新規採用者に送信する

1. 左側のメニューで、**テンプレート**を選択します。
2. **自分のテンプレート**で、新規採用者の研修用ガイドとして設定するテンプレートを選択します。
3. 必要に応じてテンプレートを編集します。 作業内容は定期的に保存してください。
4. テンプレートの編集が終了したら、**ガイドの作成**を選択します。

    [![テンプレートから研修用ガイドを作成する](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. **ガイドの作成**ウィンドウの、**研修を受けるのは誰ですか**で、新規採用者の名前または電子メール アドレスを入力します。 新規採用者がまだシステムにない場合は、**今すぐ追加**を選択し、従業員の情報を入力します。

    ![[研修ガイドの情報を入力する](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. **いつ開始しますか**で、開始日を選択します。
7. 研修用ガイドを特定の日付に新規採用者に自動的に送信する場合は、**自動送信日をスケジュール**のオプションがオンになっていることを確認し、自動送信日を選択します。 ガイドをすぐに送信するには、**自動送信日をスケジュール** オプションをオフにします。
8. **完了** を選択します。
9. 研修用ガイドの編集が完了したら、右上隅の**送信**を選択します。 そして、次の手順のいずれかを実行します。

    - 新規採用者に研修用ガイドのリンクを送信するには、**リンクをコピー**を選択してから**コピー**を選択します。
    - 研修用ガイドの電子メールを送信前にカスタマイズするには、**送信前に電子メールをカスタマイズする**を選択し、**次へ**を選択して必要に応じて電子メールをカスタマイズし、**送信**を選択します。
    - カスタマイズせずに電子メールを送信するには、**次へ**を選択し、**送信**を選択します。

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>テンプレートから研修用ガイドを作成し、複数の新規採用者に送信する

Onboard では、複数の新規採用者に同時に研修用ガイドを送信できます。

1. 左側のメニューで、**テンプレート**を選択します。
2. **自分のテンプレート**で、新規採用者の研修用ガイドとして設定するテンプレートを選択します。
3. 必要に応じてテンプレートを編集します。 作業内容は定期的に保存してください。
4. テンプレートの編集が終了したら、**ガイドの作成**を選択します。
5. **ガイドを作成**ウィンドウで、**一度に複数の人を対象として研修を行う必要がある**を選択します。

    [![複数の新規採用者に対して研修ガイドを作成する](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. **新規採用テンプレート**を選択します。
7. .xlsx ファイルをダウンロードしたら、**開く**を選択し、Excel ブックに従業員に関する情報を入力し、ブックを保存します。

    [![複数の新規採用者に研修用ガイドを送信するための Excel テンプレートのダウンロード](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > ブックを編集する前に、Excel で**編集の有効化**を選択する必要があります。
    > 
    > [![編集の有効化](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Excel ブックを**複数のガイドを作成**ウィンドウの指定した領域にドラッグするか、その領域内の任意の場所をクリックしてコンピュータ上のファイルを参照します。

    [![編集したブックをドラッグする](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. 研修用ガイドの編集が完了したら、右上隅の**送信**を選択します。 そして、次の手順のいずれかを実行します。

    - 新規採用者に研修用ガイドのリンクを送信するには、**リンクをコピー**を選択してから**コピー**を選択します。
    - 研修用ガイドの電子メールを送信前にカスタマイズするには、**送信前に電子メールをカスタマイズする**を選択し、**次へ**を選択して必要に応じて電子メールをカスタマイズし、**送信**を選択します。
    - カスタマイズせずに電子メールを送信するには、**次へ**を選択し、**送信**を選択します。

## <a name="create-a-guide-without-using-a-template"></a>テンプレートを使用せずにガイドを作成する

常にテンプレートからガイドを作成する必要はありません。 必要であれば、代わりに最初からガイドを作成できます。

1. 左側のメニューにある**ガイド**を選択し、**追加**ボタン (プラス記号 \[**+**\]) を選択します。
2. **ガイドの作成**ウィンドウの、**研修を受けるのは誰ですか**で、新規採用者の名前または電子メール アドレスを入力します。 新規採用者がまだシステムにない場合は、**今すぐ追加**を選択し、従業員の情報を入力します。

    ![[研修ガイドの情報を入力する](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. **いつ開始しますか**で、開始日を選択します。
4. 研修用ガイドを特定の日付に新規採用者に自動的に送信する場合は、**自動送信日をスケジュール**のオプションがオンになっていることを確認し、自動送信日を選択します。 ガイドをすぐに送信するには、**自動送信日をスケジュール** オプションをオフにします。
5. **完了** を選択します。

## <a name="save-a-guide-as-a-template"></a>ガイドをテンプレートとして保存する

研修用ガイドをテンプレートとして保存できます。 これにより、後でさらに研修用ガイドを作成する必要がある場合に、時間を節約できます。

1. 左側のメニューで、**ガイド**を選択します。
2. テンプレートを作成したいガイドの**詳細**ボタン (省略記号\[**...**\]) を選択し、**テンプレートとして保存**を選択します。

    ![[テンプレートとして研修用ガイドを保存する](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. **新規テンプレートとして保存**ウィンドウで、新しいテンプレートの名前を入力し、**保存**を選択します。

## <a name="next-steps"></a>次のステップ

- [研修用ガイドとテンプレートの編集](./onboard-edit-guides-templates.md)
- [他の投稿者とコンテンツを共有する](./onboard-share-template.md)
- [タスクと研修中の従業員の状態の表示](./onboard-view-status.md)
- [Onboard での採用チームの作成](./onboard-create-team.md)

### <a name="see-also"></a>参照

- [Onboard アプリを試すか購入する](https://dynamics.microsoft.com/talent/onboard/)
- [Dynamics 365 Talent の新機能および変更された機能](./whats-new.md)
- [リリース計画](https://docs.microsoft.com/business-applications-release-notes/index)
- [Microsoft Dynamics 365 Talent に関するサポートの利用](./talent-support.md)
