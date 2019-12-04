---
title: Dynamics 365 Talent - Onboard で研修用ガイドとテンプレートの編集
description: このトピックでは、Microsoft Dynamics 365 Talent - Onboard の研修用ガイドおよびテンプレートに、活動やその他の情報を追加する方法について説明します。
author: andreabichsel
manager: ''
ms.date: 06/19/2019
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
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 24369a878e95076783d670894236d56dca18e765
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812882"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-talent---onboard"></a>Dynamics 365 Talent - Onboard で研修用ガイドとテンプレートの編集

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Onboard で研修用ガイドまたはテンプレートを作成した後、概要、活動、連絡先、およびリソースを追加する必要があります。 研修用ガイドには、次の豊富な内容を含めることができます。

- YouTube ビデオ
- Microsoft Sway プレゼンテーション
- Microsoft PowerApps アプリ
- Microsoft Stream ビデオ
- Microsoft Forms フォーム
- Web コンテンツを含む iframe

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>テンプレートからインポートされた概要または活動の編集

テンプレートからの研修用ガイドを作成した場合、または 1 つのテンプレートから別のテンプレートに活動をインポートした場合、インポートした活動に**ロック** ボタンが表示されます。 これらは*管理型活動*と呼ばれます。

[![管理型活動](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

管理型活動を選択すると、ソース テンプレートが活動の上部に表示されます。

[![管理型活動ソース](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

テンプレートの活動を編集すると、Onboard ではそのテンプレートに基づくすべてのテンプレートおよび未送信ガイドへの変更がプッシュされます。 編集したテンプレートに基づいて未送信ガイドを選択してから、ガイドの**活動**タブを選択すると、ガイドが変更されたことを示す通知が表示されます。 通知を閉じるには、**OK** を選択します。 

[![変更通知](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

更新された活動の横に黒いドットが表示されます。

[![変更済の活動](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

活動の右側のセクションで割り当て対象者、期日、またはその他の情報を追加する場合を除いて、元のテンプレート外で管理型活動を編集することはできません。

管理型活動を編集する場合や、または活動が元のテンプレートから更新を受信しないようにする場合は、その活動の**ロック** ボタンを選択します。 **ロック** ボタンが表示されなくなります。 活動は元のテンプレートにより管理されなくなり、そのテンプレートから更新を受け取ることができなくなります。 活動に対して行った更新は、元のテンプレートには影響しません。

ガイドから活動を削除して、そのガイドのテンプレートから変更をプッシュすると、活動はガイドから削除されたままになります。

> [!NOTE]
> 連絡先およびリソースは、テンプレートによって管理されていません。 さらに、セクションは管理されていないため、テンプレートのセクションを追加または編集しても、そのテンプレートを使用するガイドやテンプレートに変更がプッシュされることはありません。
> 
> 新しい活動をテンプレートに追加すると、新しい活動はそのテンプレートに基づいてガイドおよびテンプレートにプッシュされ、新しい活動が上部に表示されます。

## <a name="import-activities-from-another-template"></a>別のテンプレートからの活動のインポート

1 つ以上のテンプレートからの活動をガイドまたはテンプレートにインポートできます。

1. 編集するガイドまたはテンプレートを選択します。

2. **活動**タブを選択します。

3. 右側のセクションで、**インポート** タブを選択します。

   [![活動のインポート](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. ブラウザーの新しいタブでタスクをプレビューするには、任意のテンプレートで**新しいタブで開く**ボタンを選択します。

   [![活動のインポート](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. 目的のテンプレートを、ガイド テンプレート内の活動を表示する場所にドラッグ アンド ドロップします。 ガイドまたはテンプレートの編集を続行します。

インポートされた活動には**ロック** ボタンが含まれており、これらの活動がインポートしたテンプレートによって管理されていることを示します。 インポートしたテンプレートに変更を加えると、それらの活動はインポートしたテンプレートで更新されます。 ただし、インポートしたテンプレートから作成された任意のガイドに対しては、変更が自動的にプッシュされることはありません。

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>テンプレートから他のテンプレートまたはガイドへの変更のプッシュ

他のテンプレートまたはガイドで使用される活動を含むテンプレートを編集する場合、他のテンプレートまたはガイドで表示する場合の変更をプッシュする必要があります。

テンプレートの活動が別のテンプレートまたはガイドで使用されているかどうか分からない場合は、**使用先**タブを選択してそれらの活動が表示される場所を表示します。

   [![ガイドおよびテンプレート活動の使用先の表示](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

変更をプッシュするには:

1. **保存**ボタンを選択して変更を保存します。 この操作を行わない場合、次の手順で変更を保存するかどうかを確認するメッセージが表示されます。

2. **これらの変更をプッシュする**を選択します。

   
## <a name="add-or-edit-an-introduction"></a>概要の追加または編集

1. **概要**タブで、ガイドのタイトルと開始メッセージを入力します。 サンプル テキストを使用するには、**このメッセージを使用する**を選択します。

    [![研修用テンプレートの概要タブ](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. 書式設定ボタンを使用して、必要に応じてテキストを呼び出したり、画像やリンクを追加したりできます。
3. **保存**を選択して作業内容を保存します。

## <a name="add-or-edit-activities"></a>活動を追加または編集

1. **活動**タブで、項目を右から編集領域にドラッグします。
2. ガイドをセクションに分けて整理するには、**新しいセクション**項目を編集領域にドラッグし、セクション名とオプションの説明を入力します。

    ![[新しいセクションを研修用ガイドまたはテンプレートに追加する](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. 新しい採用に対する活動を追加して完了するには、**新しい活動**項目を編集領域にドラッグし、活動の名前と説明を入力します。

    ![[新しい活動を研修用ガイドまたはテンプレートに追加する](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. 豊富な内容を研修用ガイドに追加します。

    - YouTube ビデオを追加するには、**YouTube** 項目を編集領域にドラッグし、活動の名前と説明を入力して、YouTube ビデオの URL を入力します。
    - Sway プレゼンテーションまたはニュースレターを追加するには、**Sway** 項目を編集領域にドラッグし、活動の名前と説明を入力して、Sway プレゼンテーションまたはニュースレターの埋め込み URL を入力します。
    - Microsoft Power Apps アプリを追加するには、**Power Apps** 項目を編集領域にドラッグし、活動の名前と説明を入力して、Power Apps アプリを選択するか、または Power Apps アプリ ID を入力します。
    - Microsoft Stream ビデオを追加するには、**Microsoft Stream** 項目を編集領域にドラッグし、活動の名前と説明を入力して、Microsoft Stream ビデオの URL を入力します。
    - Microsoft Forms フォームを追加するには、**Microsoft Forms** 項目を編集領域にドラッグし、活動の名前と説明を入力し、Microsoft Forms フォームの URL を入力して、画面領域のサイズを指定します。
    - Web コンテンツを含む iframe を追加するには、**Web コンテンツ (iframe)** 項目を編集領域にドラッグし、活動の名前と説明を入力し、Web コンテンツの URL を入力して、画面領域のサイズを指定します。

    ![[豊富な内容を研修用ガイドまたはテンプレートに追加する](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. オプション: 各活動の右の領域で、活動を特定の個人またはロールに割り当て、期日と連絡担当者を追加し、カテゴリの色を割り当てます。 個人またはロールに活動を割り当てると、各個人に対してタスクが作成されます。 このタスクは、Onboard の**タスク** メニューに表示されます。

    [![研修用ガイドまたはテンプレートで活動を割り当てる](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. **保存**を選択して作業内容を保存します。

活動またはセクションを削除するには、活動またはセクションの右上隅にある**削除**ボタン (ゴミ箱記号) を選択します。

活動およびセクションを並べ替えるには、新しい場所に活動およびセクションをドラッグします。

## <a name="add-or-edit-contacts"></a>連絡先の追加または編集

初日から新しい採用の成功を支援できる連絡担当者を追加できます。 これらの連絡先には、採用担当者、チームメート、先輩従業員、指導担当者、管理者、および IT サポート スタッフが含まれます。

1. **連絡先**タブで、**新しい連絡先**を選択します。
2. **チーム メンバーの追加**ダイアログ ボックスで、連絡担当者の名前または電子メール アドレスを入力し、連絡担当者が新しい採用を支援する方法を示す簡単な説明を入力してから、**追加**を選択します。 

    ![[連絡先を研修用ガイドまたはテンプレートに追加する](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    別の方法として、1 つ以上の連絡先を**候補**から選択できます。

3. **保存**を選択して作業内容を保存します。

連絡先を削除するには、連絡先の側にある**削除**ボタン (ごみ箱記号) を選択します。

連絡先を編集するには、連絡先の右にある**編集**ボタン (鉛筆記号) を選択します。

## <a name="add-or-edit-resources"></a>リソースの追加または編集

研修用ガイドの**リソース** セクションに、役立つファイル、マップ、およびリンクを追加できます。

1. **リソース** タブで、**新しいリソース**を選択します。
2. 次の手順のいずれかを実行します。

    - ファイルを追加するには、**ファイル** タブを選択し、指定した領域にファイルをドラッグします。 (または、その領域内の任意の場所をクリックしてコンピュータ上のファイルを参照するか、または **OneDrive を参照**を選択します。) ファイルの名前を入力してから、**追加**をクリックします。
    - リンクを追加するには、**リンク** タブを選択し、リンクの名前と住所を入力してから、**追加**を選択します。
    - マップを追加するには、**マップ** タブを選択し、マップの名前と住所を入力してから、**追加**を選択します。 Onboard には、指定するアドレスのマップが含まれます。

    ![[リソースを研修用ガイドまたはテンプレートに追加する](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. **保存**を選択して作業内容を保存します。

リソースを削除するには、リソースの右にある**削除**ボタン (ごみ箱記号) を選択します。

連絡先を編集するには、リソースの右にある**編集**ボタン (鉛筆記号) を選択します。

## <a name="next-steps"></a>次のステップ

- [他の投稿者とコンテンツを共有する](./onboard-share-template.md)
- [タスクと研修中の従業員の状態の表示](./onboard-view-status.md)
- [Onboard での採用チームの作成](./onboard-create-team.md)

### <a name="see-also"></a>参照

- [Onboard アプリを試すか購入する](https://dynamics.microsoft.com/talent/onboard/)
- [Dynamics 365 Talent の新機能および変更された機能](./whats-new.md)
- [リリース計画](https://docs.microsoft.com/business-applications-release-notes/index)
- [Microsoft Dynamics 365 Talent に関するサポートの利用](./talent-support.md)
