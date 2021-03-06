---
title: Attract の人材プールを使用した候補者のソーシング
description: このトピックでは、Microsoft Dynamics 365 Talent - Attractの人材プールを作成および設定する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 06/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 97385da9d258cc169a9976be7c7798faa41661c3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527696"
---
# <a name="source-candidates-with-talent-pools-in-attract"></a>Attract の人材プールを使用した候補者のソーシング

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

採用担当者および採用マネージャーは、Attract の人材プール機能を使用して、その候補者を整理することができます。 人材プールは、番号の追跡を助け、社内のジョブに対して適用されるすべての候補者と連携を可能にします。

## <a name="create-and-share-a-talent-pool"></a>人材プールを作成および共有

採用担当者、採用マネージャー、または Attract 管理者のロールを示すすべてのユーザーは、人材プールを作成できます。 人材プールの所有者は他のユーザーとプールを共有することもできるので、特に採用担当者のユーザー グループは、候補者の共有プールを見ることができます。

人材プールへの寄稿者は、そのプールの候補者リストを表示できます。 候補者をプールに追加または削除もできます。

人材プールの作成および共有に関しては、次の手順に従います。

1. Attract ホーム ページの左側のナビゲーション ウィンドウで、**人材プール** を選択します。

    **自分の人材プール** タブでは、それぞれに関する詳細へのアクセスを持つすべての人材プールを表示します。 詳細には、プールの所有者および候補者の数が含まれます。

1. ページの右上で **新規** を選択し、**人材プールの作成** ダイアログ ボックスをオープンします。
1. 人材プールの一意の名前を入力します。
1. 寄稿者となるユーザーをプールに追加するには、人員ピッカーを使用して名前を検索し、リストに追加します。 採用担当者、採用マネージャー、または Attract 管理者のロールを示すユーザーのみと人材プールを共有できます。
1. **追加** 選択し、人材プールを作成します。
     > [!NOTE]
     > 作成後、人材プールに寄稿者を追加することもできます。 人材プールへのアクセスを管理することもできます。 たとえば、人材プールへのユーザーのアクセスを破棄できます。
     > - 所有しているに既存の人材プールに寄稿者を追加するには、人材プール カードの右上隅の **自分の人材プール** タブで、省略記号ボタン (**…**) を選択し、**編集** を選びます。 人員ピッカーを使用して人員を検索し、リストに追加します。 
     > - 人材プールへのユーザー アクセスを無効にするには、人材プール カードの右上隅で、省略記号ボタン (**…**) を選択し、**編集** を選びます。 **アクセスを管理** タブで、ユーザーの横にあるゴミ箱ボタンを選択します。

6. **更新** を選択して、操作を完了および保存します。

> [!NOTE]
> 1 つ以上の人材プールを作成するには、包括採用アドオンが組織に必要です。

## <a name="add-and-remove-candidates"></a>候補者の追加および削除

人材への所有者および寄稿者は、候補者を人材プールへ追加、表示、削除できます。

1. **自分の人材プール** タブで、人材プールを選択しオープンします。

    人材プールの一部である候補者リストが表示されます。

1. 人材プールに候補者を追加するには、右上の **+ 新規** を選び、**候補者の追加** ダイアログ ボックスをオープンし、次のいずれかの操作を行います。

    - 内部候補者を追加するには、電子メール アドレスで個人を検索できます。 検索に成功した後は、候補者の電子メール アドレス、名前、および姓が入力されます。 候補者の履歴または候補者に関するドキュメントがある場合は、この時点でアップロードできます。 **追加** を選択し、人材プールに候補者を追加します。
    - 外部の候補を追加するには、自分の電子メール アドレス、名、および姓を手動で入力します。 候補者の経歴または候補者に関するドキュメントがある場合は、この時点でアップロードできます。 **追加** を選択し、人材プールに候補者を追加します。
    - 複数の候補者を追加するには、**Excel から** タブを選択します。そして適切な Microsoft Excel テンプレートをダウンロードし、候補者の詳細を入力後 Excel ワークシートを保存し、アプリケーションにアップロードします。

        ワークシートにエラーが見つかった場合は、それらに関するメッセージが表示されます。 エラーを修正し、ワークシートをもう一度アップロードしてください。 エラーがそれ以上見つからない場合は、**追加** を選択しワークシートをアップロードします。 ワークシートがバック グラウンドで処理されると、すべての候補者が人材プールに追加されると通知されます。

1. 人材プールから既存の候補者を削除するには、**アクション** 列でその候補者を選び、ごみ箱ボタンをクリックします。

## <a name="search-and-view-candidate-profiles"></a>候補者プロファイルの検索および表示

> [!NOTE] 
> 現在プレビューにある機能です。 試行する場合は、[Attract 管理者の設定で有効にする](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) を実行します。 

人材管理グループは、候補者のプロファイル、LinkedIn 情報、書類関連およびアプリケーションの履歴の閲覧を許可します。 決算済および有効な申請者を含むすべての人材プールに追加される候補者のデータベース全体を、検索することができます。

>[!NOTE]
> 新しい候補者または申請者を追加するとき、新規追加は検索用インデックスを付けるのに最大 15 分を要します。

強化された検索エクスペリエンスにより、すべてのドキュメントを検索および銀メダリスト、ソース、スキルそして教育などでフィルターをかけることが可能です。 以前のバージョンでは、検索したいエンティティを指定する必要がありました。 Attract では、候補の関連フィールドをすべて検索でき、結果をランク付けできます。

1. 候補データベースから新しい検索を開始するには、**人材プール** タブの検索ボックス内で検索したいテキストを入力します。 

お探しの候補者の名前または任意の属性を入力できます。 属性を分けるには、スペースを使用します。

検索クエリを変更するか、またはページの左側にあるスマート フィルターを使用するかで結果を絞り込むことができます。

検索結果は、検索クエリと照合したさまざまな属性をハイライトで表示します。 興味のある候補者を選択して、プロファイルを表示します。

### <a name="syntax-highlights"></a>構文ハイライト 

| オペレーター | 用途                                                      | 例              |
|----------|------------------------------------------------------------|----------------------|
| \*       | サブ文字列の検索; すべてのレコードを返すために使用可能 | 入力: Mi\* <br></br> 結果: Microsoft や Micro systems、Midtown Enterprises、MiddletonAll など 「Mi」ではじまるフィールドを含むすべてのレコード <br></br>入力: \* <br></br> 結果: データベース内のすべてのレコード |
| 「」       | 完全一致の検索                                | 入力: 「Microsoft」 <br></br> 結果: 「Microsoft」を含むすべてのレコード                    |

>[!WARNING]
> Common Data Service インスタンスの関連性検索を無効にしないでください。 Attract の検索エクスペリエンスが無効になります。

すべてのユーザーは、候補者プロファイルを共通に表示できます。 **プロファイル** タブを使用して、スキル、業務の経験および候補者がキャリア ポータルを使い申請の一部を提供した教育に関する情報を表示します。

- 候補者の詳細な連絡先を表示できます。 **詳細の編集** ボタンを使用して、必要な情報を編集または更新できます。

- 候補者のアプリケーションの全体履歴を表示することができます。 候補者が組織内で応募したすべてのジョブおよびこれらのアプリケーション状態を表示できます。 ジョブの採用チームの一員である場合は、**表示** を選択し、詳細にアプリケーションを確認できます。

- **ドキュメント** タブを使用して、候補者が自身のプロファイルからまたはジョブ アプリケーション間に、追加したドキュメントを表示します。 このタブを使用して、候補者の履歴書、カバー レター、ポートフォリオの作業などを管理できます。 このタブを使用して、ドキュメントを追加することもできます。

    ドキュメントを表示するには、ドキュメント リストでドキュメント名を選択します。 Microsoft 365 を使用して、アプリケーションの Microsoft Word ドキュメントを表示できます。 各ドキュメントの **ダウンロード** オプションを使用して、ドキュメントをローカル コンピューターにダウンロードすることもできます。

- **LinkedIn** タブを使用して、候補者の LinkedIn 情報を表示します。 このタブを使用するには、ユーザー設定で LinkedIn アカウントを接続する必要があり、自身の環境 LinkedIn Recruiter の接続は確立されている必要があります。 詳細については、[Microsoft Dynamics 365 Talent - Attract での、LinkedIn Recruiter を使用した候補者のソーシング](./attract-linkedin-recruiter.md).

> [!NOTE]
> 候補者だけが、自分のスキル、学歴、および業務経験を更新できます。

## <a name="add-candidates-from-a-talent-pool-to-a-job"></a>人材プールからジョブに候補者を追加

検索結果または人材プールから、採用している有効なジョブに候補者をプッシュできます。 特定なジョブに候補者をプッシュするには、以下の手順を実行します。

1. 検索オプションを使用して候補を検索し、自身のプロファイルを開きます。 また、**自分の人材プール** タブから人材プールを開いて候補者を検索し、そして自身のプロファイルを開きます。

1. 候補者プロファイルのページで、右上の **ジョブに追加** を選択します。 
     
     採用担当者または採用マネージャーのいずれかの採用チームに属しているジョブの一覧が表示されます。

1. 候補者を追加するジョブを選択し、**追加** をクリックします。 **ジョブに候補者を追加** ダイアログ ボックスの上部にある検索フィールドを使用して、ジョブを検索することもできます。

    見込顧客がジョブに対して有効になった場合、**見込顧客** ステージに候補者を追加します。

    見込顧客がジョブに対して有効にならなかった場合、**適用** ステージに候補者を追加します。 ジョブのコンフィギュレーションしだいで、候補者はアプリケーションを確認できる電子メールを受信するかもしれません。

## <a name="add-candidates-from-a-job-to-a-talent-pool"></a>ジョブから人材プールに候補者を追加

多くの場合、ジョブのための一部の優秀な候補者は選択されません。しかし、優秀な候補者の追跡継続を望んでいます。 この場合、その候補者を人材プールに追加して、今後の他のジョブに応募できるよう招待することができます。

1. 候補者を追加するジョブに移動します。

1. 候補者を選択して、そのアプリケーションを開きます。

1. アプリケーション ページで **人材プールへの追加** を選択します。 アクセスできる人材プール リストが表示されます。

1. 人材プールを選択または検索し、**追加** を選択して人材プールに候補者を追加します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]