---
title: "携帯電話請求書承認"
description: "、Microsoft Dynamics 365の携帯電話機能は、ユーザーが携帯電話経験を作成できるようにします。 高度なシナリオに、プラットフォームは、の開発者としての機能を拡張することができます。 モバイル者の新しい概念の一部を入手最も効率的に時間のシナリオの作成のプロセスによって移動することです。 このトピックでは、ユース ケースとして仕入先請求書の承認を提供するように選択することによってモバイル機器に移動してシナリオのデザインになったな方法を使用します。 このトピックでは、シナリオの他の変動を作成するのに役立つように、仕入先請求書に関連付けられていない他のシナリオに適用できます。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>携帯電話請求書承認

、Microsoft Dynamics 365の携帯電話機能は、ユーザーが携帯電話経験を作成できるようにします。 高度なシナリオに、プラットフォームは、の開発者としての機能を拡張することができます。 モバイル者の新しい概念の一部を入手最も効率的に時間のシナリオの作成のプロセスによって移動することです。 このトピックでは、ユース ケースとして仕入先請求書の承認を提供するように選択することによってモバイル機器に移動してシナリオのデザインになったな方法を使用します。 このトピックでは、シナリオの他の変動を作成するのに役立つように、仕入先請求書に関連付けられていない他のシナリオに適用できます。

<a name="prerequisites"></a>必要条件
-------------

| 前提条件                                                                                            | 説明                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 潜在顧客読取り携帯電話ハンドブック                                                                                | (/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform.md)                                                                                                   |
| Dynamics 365 for Operations                                                                             | 工程バージョン1611では、Microsoft Dynamics 365および工程のプラットフォームの更新は3 (2016年12月11) のMicrosoft Dynamicsがある環境                   |
| 変更KB 3204341をインストールします。                                                                              | タスク レコーダを誤ってこれは、アクションのプラットフォームの更新は3 (11年1月2016日の更新) 365 for Operationsに含まれるなダイアログ ボックスの二つの決算コマンドを記録できます。 |
| 変更KB 3207800をインストールします。                                                                              | この変更が添付ファイルがこれは、アクションのプラットフォームの更新は3 (11年1月2016日の更新) 365 for Operationsに含まれる携帯電話クライアントで表示できるようになります。           |
| 変更KB 3208224をインストールします。                                                                              | 携帯電話仕入先請求書の承認アプリケーションのアプリケーション コードは、Microsoft Dynamics AXアプリケーション7.0.1 (2016年12月5) によって含まれます。                          |
| アンドロイドまたはiOSまたは移動式アプリケーションは、Windowsのデバイスは、Dynamics 365 for Operationsにインストールする | 適切なアプリケーションの店舗のアプリケーションを検索します。                                                                                                                     |

## <a name="introduction"></a>はじめに
仕入先請求書の携帯電話承認前提条件は、「」に示されている3変更が必要です。 これらの変更は、請求書は、ワークスペースは表示されません。 ワークスペースがモバイル機器のコンテキストにおいてされたものついては、「前提条件」に示されている携帯電話ハンドブックを参照してください。 請求書承認ワークスペースを作成する必要があります。 

すべてのコンフィギュレーションは仕入先請求書の業務プロセスを別に調整およびに編曲定義します。 仕入先請求書の承認の携帯電話経験を作成する前に、業務プロセスの次の側面を考慮する必要があります。 これは、デバイスのユーザー エクスペリエンスを最適化する、これらのデータ点をできるだけ使用します。

-   請求書ヘッダーのユーザーは、フィールドを携帯電話経験に表示するし、注文でか。
-   請求明細行のユーザーは、フィールドを携帯電話経験に表示するし、注文でか。
-   請求書に、請求明細行があるか。 80-20ルールをここに適用され、80日に対して最適化します。
-   ユーザーが検証中にモバイル デバイスの会計配分 (請求書のコード) が表示されるか。 この質問への回答がYes場合は、次の質問を考慮します:
    -   複数会計配分 (拡張価格、売上税、雑費、分割など) 請求明細行のためですか。 再度、80-20ルールを適用します。
    -   請求書に、請求書ヘッダーの会計配分があるか。 その場合、これらの勘定の配分がデバイスで使用する必要がありますか。

> [!NOTE]
> このトピックでは、この機能の携帯電話シナリオで現在サポートされません。会計配分を編集する方法は説明しません。

-   ユーザーはデバイスの請求書について、その添付ファイルが表示されるか。

請求書承認の携帯電話経験のデザインは、これらの質問に回答によって異なります。 目標は、組織のモバイル者の業務プロセスのユーザー エクスペリエンスを最適化することです。 このトピックの他に、前の質問に対する各回答に基づいて二つのシナリオのバリエーションが表示されます。 

一般ついては、移動式デザイナーで働いた場合、更新を失うことに「発行の変更を確認してください。

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>それぞれの簡単な請求書承認のシナリオの作成
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>シナリオの属性</th>
<th>応答</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>請求書ヘッダーのユーザーは、フィールドを携帯電話経験に表示するし、注文でか。</td>
<td><ol>
<li>仕入先名</li>
<li>請求合計</li>
<li>請求先/元 ID</li>
<li>請求書番号</li>
<li>請求日</li>
<li>請求明細</li>
<li>期日</li>
<li>請求書通貨</li>
</ol></td>
</tr>
<tr class="even">
<td>請求明細行のユーザーは、フィールドを携帯電話経験に表示するし、注文でか。</td>
<td><ol>
<li>調達カテゴリ</li>
<li>件数</li>
<li>単価</li>
<li>明細行の正味金額</li>
<li>1099 金額</li>
</ol></td>
</tr>
<tr class="odd">
<td>請求書に、請求明細行があるか。 80-20ルールをここに適用され、80日に対して最適化します。</td>
<td>1</td>
</tr>
<tr class="even">
<td>ユーザーが検証中にモバイル デバイスの会計配分 (請求書のコード) が表示されるか。</td>
<td>有</td>
</tr>
<tr class="odd">
<td>複数会計配分 (拡張価格、売上税、雑費など) 請求明細行のためですか。 再度、80-20ルールを適用します。</td>
<td>拡張価格: 2:売上税 0:請求 0</td>
</tr>
<tr class="even">
<td>請求書に、請求書ヘッダーの会計配分があるか。 その場合、これらの勘定の配分がデバイスで使用する必要がありますか。</td>
<td>不使用</td>
</tr>
<tr class="odd">
<td>ユーザーはデバイスの請求書について、その添付ファイルが表示されるか。</td>
<td>有</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>ワークスペースを作成します。

1.  ブラウザでは、工程の未処理のDynamics 365、署名します。
2.  署名すると、** &mode=mobile ** URLし、次の例で示すように、付け、ページを更新します: https://yoururl/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**&lt;&gt;
3.  クリックして** **設定 (ギヤ) ページの上部のアクセス許可にボタンをクリックして[]をクリックします。**携帯電話アプリケーション**。 携帯電話、デザイナ、タスク レコーダが表示されませんされるように現れなければがあります。
4.  新しいワークスペースを作成します。** **追加します。 この例では、ワークスペース**自分の承認を**指定します。
5.  説明を入力します。
6.  ワークスペース色を選択します。 ワークスペース色は、ワークスペースの携帯電話経験の全体的な形式に使用されます。
7.  ワークスペースにアイコンを選択します。
8.  [**可能な**
9.  変更を保存します**発行ワークスペース**

### <a name="vendor-invoices-assigned-to-me"></a>自分に割り当てられている仕入先請求書

[デザインする最初のモバイル ページは、請求書の一覧が確認のユーザーに割り当てられている。 このモバイル ページを作成するには、** VendMobileInvoiceAssignedToMeListPage **]ページで、Dynamics 365 for Operationsで使用します。 この手順を実行する前に、少なくとも一つの仕入先請求書が校閲自分に割り当てられていること、および請求明細行としての配分があることを確認します。 この設定はこのシナリオの要求を満たします。

1.  工程URL 365 for Operationsでは、** **買掛金勘定モジュールの**自分に割り当てられている仕入先請求書の保留中**リスト ページの携帯電話バージョンを開くには、メニュー項目の名前と** VendMobileInvoiceAssignedToMeListPage **置き換えます。 、自分に割り当てられているシステムの請求の数によってこのページでは、それらの請求書を表示します。 特定の請求書を検索するには、左側のフィルタを使用できます。 ただし、この例では、特定の請求書を必要としません。 Microsoftでモバイル ページを作成することを許可する、ピッキングが自分に割り当てられている請求書が必要です。 使用できる新しいページは、仕入先請求書の携帯電話シナリオを開発するための配送オペレーション用に設計されています。 したがって、これらのページを使用する必要があります。 URLは、次のURLに類似するか、それを入力すると、図に表示されるページが出なければがあります: https://yourURL/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile&lt;&gt;[自分に割り当てられている![の保留中の仕入先請求書]ページ (。/media/mobile請求approvals01 1024x281.png) ] (。/media/mobile請求approvals01.png) 
2.  クリックして** **設定 (ギヤ) ページの上部のアクセス許可にボタンをクリックして[]をクリックします。**携帯電話アプリケーション**
3.  ワークスペースと]を選択します** **編集します。
4.  最初のモバイル ページを作成します**ページを追加します。**。
5.  名前などに**自分の仕入先請求書**、および説明を、など) を入力します。**書に自分に割り当てられている仕入先請求書**。
6.  [**可能な**。
7.  携帯電話デザイナーで、**フィールド**]タブで、[**]フィールド**。 リスト ページの列は次のようになりますする必要があります。 [自分に割り当てられている保留中の仕入先請求書の![列]ページ (。/media/mobile請求approvals02 1024x117.png) ] (。/media/mobile請求approvals02.png) 
8.  モバイル ページでユーザーに表示必要があるリスト ページから必要な列を追加します。 [追加注文は、フィールドがエンドユーザーに表示される順序です。 フィールドの順序を変更する唯一の方法はすべてのフィールドの再選択して実行します。 このシナリオの要件に基づいて、次の8つのフィールドは必須です。 ただし、複数のユーザーがモバイル デバイスにすると8つのフィールドが大量の情報と仮定するかもしがあります。 したがって、携帯電話リスト ビューで最も重要なフィールドのみが表示されます。 残りのフィールドに詳細ビューでMicrosoftが後で作成することに表示されます。 ここでは、次のフィールドを追加します。 モバイル ページに追加するこれらの列のプラス記号 (+) ** **クリックします。
    1.  仕入先名
    2.  請求合計
    3.  請求先/元 ID
    4.  請求書番号
    5.  請求日

    フィールドが追加された後、モバイル ページは、次のようになりますする必要があります。 [フィールドの後![ (]ページが表示されます。/media/mobile請求approvals03.png) ] (。/media/mobile請求approvals03.png) 
9.  Microsoftがワークフロー アクションを後で有効にするためするには、次の列がすぐに追加する必要があります。
    1.  完全なタスクを表示します。
    2.  委任タスクを表示します。
    3.  取り消すタスクを表示します。
    4.  否認タスクを表示します。
    5.  要求の完了を表示します。
    6.  にはタスクを再送信します

10. 終了する[**可能な**編集モードを。
11. ** [戻る**、[**される**ワークスペースを終了する
12. 作業を保存します**発行ワークスペース**。
13. 有効**保留中の仕入先請求書の一覧で、請求合計**買掛金勘定パラメータ フォームで、[**請求**。 このパラメータを有効にすることで、請求合計が保留中の仕入先請求書のリスト ページに表示されるようにのみ計算されることに注意してください。 これは、前提条件に熱い変更3208224の一部として新しい機能です。

### <a name="vendor-invoice-details"></a>仕入先請求書の詳細

モバイル機器の請求書の詳細]ページを作成するには、** VendMobileInvoiceHeaderDetails **]ページで、Dynamics 365 for Operationsで使用します。 自分にシステムの請求の数によってことで、このページには最も古い請求書 (最初に作成された) 請求書注意してください。 特定の請求書を検索するには、左側のフィルタを使用できます。 ただし、この例では、特定の請求書を必要としません。 Microsoftでは、今後のモバイル ページを作成してできるようになる請求書データが必要です。 [![作業の現在のページ] (。/media/mobile請求approvals04 1024x425.png) ] (。/media/mobile請求approvals04.png) 

1.  工程URL 365 for Operationsで、フォームを開く場合は、メニュー項目の名前と** VendMobileInvoiceHeaderDetails **置き換えます。
2.  から移動式デザイナーを開きます** **設定 (ギヤ ボタン)。
3.  **編集を行います**ワークスペースの編集モードを開始するためにボタンをクリックします。
4.  **自分の仕入先請求書**先に作成し、サイド リンク指定します。]ページで、** **編集します。
5.  ** **フィールドで、**グリッド**列のヘッダーをクリックします。
6.  [**プロパティ** &gt; **ページを**追加します。 **注記: ** **グリッド**ヘッダーをクリックし、ページを追加すると、詳細]ページとの関係が自動的に設定されます。
7.  ページのタイトルのなどに**請求書の詳細**、および説明を、など) を入力します。**ビューの請求書ヘッダーと明細行の詳細**。
8.  [**]フィールド**。 これで、のフィールドがエンドユーザーに表示される順序を注文確認します。 フィールドの順序を変更する唯一の方法はすべてのフィールドの再選択して実行します。
9.  このシナリオの要件に基づいてヘッダーから次のフィールドを追加します:
    1.  仕入先名
    2.  請求合計
    3.  請求先/元 ID
    4.  請求書番号
    5.  請求日
    6.  請求明細
    7.  期日
    8.  請求書通貨

10. ページの行のグリッドで次のフィールドを追加します:
    1.  調達カテゴリ
    2.  件数
    3.  単価
    4.  明細行の正味金額
    5.  1099 金額

11. すべての前の二つの手順のフィールドは、[追加された**可能な**。 ここでは、次のようになりますする必要があります。 [![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. 終了する[**可能な**編集モードを。
13. ** [戻る**、[**される**ワークスペースを終了する
14. 作業を保存します**発行ワークスペース**

### <a name="workflow-actions"></a>ワークフロー アクション

ワークフロー アクションを追加するには、** VendMobileInvoiceHeaderDetails **]ページで、Dynamics 365 for Operationsで使用します。 先にように、このページを開くには、URLのメニュー項目の名前を置き換えます。 このからからの携帯電話デザイナーを開きます** **設定 (ギヤ ボタン)。 詳細のワークフロー アクションを追加するには、次の手順に従います。

1.  **編集を行います**ワークスペースの編集モードを開始するためにボタンをクリックします。
2.  **請求書の詳細**先に作成し、サイド リンク指定します。]ページで、** **編集します。
3.  **工程**タブで、[**工程を追加します。**。
4.  アクションのタイトルなどに**承認します。**、および説明を、など) を入力します。**請求書を承認します。**。 ここで入力した工程のタイトルが携帯電話アプリケーションでユーザーに表示する操作の名前になることに注意してください。
5.  [**可能な**。
6.  [**]フィールド**。
7.  ** VendMobileInvoiceHeaderDetails **ページのワークフロー プロセスを通じて受信、記録する場合は、アクションを完了します。 コメント フィールドが移動して経験に含める場合、このプロセス中に作業の現在のコメントを入力してください。
8.  ワークフロー アクションの実行後、[フィールド タスクを完了するために**される**クリックします。
9.  終了する[**可能な**編集モードを。
10. ** [戻る**、[**される**ワークスペースを終了する
11. 作業を保存します**発行ワークスペース**
12. 手順3 ~すべての必須のワークフロー アクションを記録する11を繰り返してします。 これには、要件に割り当てられたのために設計することワークフロー アクションが利用可能にするステータスにある請求書を持つように注意してください。
13. メモまたはMicrosoft Visual Studioを開き、次のコードを貼ってします。 ファイルを.jsファイルとして保存します。 このコードは、の操作を実行します:
    1.  また、Microsoftが携帯電話リスト ページでは、先に追加する特別な作業の現在関連する列を非表示にします。 ただし、アプリケーションのコンテキストにする情報ありますが、次の手順を実行できるようにこれらの列を追加します。
    2.  有効なワークフロー ステップに基づいて、それらのアクションのみを表示する場合はロジックを適用します。

これでの名前表示しますJSコードの他のコントロールは、ワークスペースの同じである必要があります。

1.  機能の基本 (metadataService、dataService、cacheService、$q) {返品{appInit: 機能 (appMetadata) {する必要がある//の非表示を表示する見えないmetadataService.configureControl (「の仕入先請求書に、非表示ShowAccept 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowApprove 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowReject 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowDelegate 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowRequestChange 「」、{: }調整する) こと;              metadataService.configureControl (「の仕入先請求書に、非表示ShowRecall 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowComplete 「」、{: }調整する) こと;            metadataService.configureControl (「の仕入先請求書に、非表示ShowResubmit 「」、{: }調整する) こと;            }、pageInit: 機能 (pageMetadata、パラメーター) { (pageMetadata.Nameの== 「請求書詳細」) //{基づくワークフロー ステップの表示/非表示のワークフロー アクションmetadataService.configureActionに使用します (「」、{表示: }調整する) こと;                    metadataService.configureAction承認します (「」、{表示: }調整する) こと;                    metadataService.configureAction (表示されている「否認」、{: }調整する) こと;                    metadataService.configureAction (表示されている「委任」、{: }調整する) こと;                    metadataService.configureAction (表示されている「要求」変更、{: }調整する) こと;                    metadataService.configureAction (表示されている「取り消すには、{: }調整する) こと;                    metadataService.configureAction完了します (「」、{表示: }調整する) こと;                    metadataService.configureAction再送信します (「」、{表示: }調整する) こと;

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  **ロジック**タブを選択して、ワークスペースのコード ファイルをアップロードします。
3.  終了する[**可能な**編集モードを。
4.  ** [戻る**、[**される**ワークスペースを終了する
5.  作業を保存します**発行ワークスペース**

### <a name="vendor-invoice-attachments"></a>仕入先請求書の関連付け

1.  クリックして** **設定 (ギヤ) ページの上部のアクセス許可にボタンをクリックして[]をクリックします。**携帯電話アプリケーション**
2.  **編集を行います**ワークスペースの編集モードを開始するためにボタンをクリックします。
3.  **請求書の詳細**先に作成し、サイド リンク指定します。]ページで、** **編集します。
4.  **次に示すように、**ドキュメント管理**オプションを**はい設定します。 **注記: **モバイル デバイスの添付ファイルを参照要件がある**既定の設定で、このオプションを設定を**ままにすることができます。
5.  [![のdocmanagement] (。/media/docmanagement-216x300.png) ] (。/media/docmanagement.png) 
6.  終了する[**可能な**編集モードを。
7.  ** [戻る**、[**される**ワークスペースを終了する
8.  作業を保存します**発行ワークスペース**

### <a name="vendor-invoice-line-distributions"></a>仕入先請求明細行の配分

このシナリオの要件は同等の配布に使用できる、および請求書に一つの行が常にいることを確認します。 このシナリオは単純なので、配分を表示するには、ユーザーが複数のレベルであけるには、モバイル デバイスのユーザー エクスペリエンスが完全に簡単である必要があります。 Dynamics 365 for Operationsの仕入先請求書が請求書ヘッダーのすべての配分の提示のオプションがあります。 このエクスペリエンス、Microsoftが携帯電話場合のために必要です。 したがって、移動できます。このシナリオの一部を作成するのに** VendMobileInvoiceAllDistributionTree **ページを使用します。 

> [!NOTE] 
> 要件を把握することが、今後のシナリオを作成すると、で、ユーザーについて携帯電話経験を最適化する方法を使用する特定のページを決定できます。 2番目のシナリオでは、そのシナリオの要件は異なるため、配分を示す、異なるページを使用します。

1.  URLに、前にした場合、メニュー項目の名前を置き換えます。 ページには、次のようになりますする必要があります。 [![すべての配分]ページ (。/media/mobile請求approvals06.png) ] (。/media/mobile請求approvals06.png) 
2.  から移動式デザイナーを開きます** **設定 (ギヤ ボタン)。
3.  **編集を行います**ワークスペースの編集モードを開始するためにボタンをクリックします。 **注記: **二つの新しいページが自動的に作成されることを示します。 [前のセクションのドキュメント管理をつけたため、これらのページを作成します。 これらの新しいページを無視できます。
4.  [**ページを追加します。**。
5.  ページのタイトルのなどに**ビューの会計**、および説明を、など) を入力します。**請求書の表示の会計**。
6.  [**可能な**。
7.  ** **フィールドで、**]フィールド**クリックし、配分のページから次のフィールドを選択し、[クリックして**される**:
    1.  金額
    2.  通貨
    3.  勘定科目

> [!NOTE] 
> ただし、配分のグリッドから配分に対してのある拡張価格が唯一の金額であることをこのシナリオの要件を確認するため、** **説明列を選びませんでした。 これにより、ユーザーは配分の対象の金額のタイプを決定するに別のフィールドが必要はありません。 ただし、次のシナリオで、** **他の金額のタイプの配分 (たとえば、売上税) がある場合は、そのシナリオの要件を指定するときに、この情報を使用します。
8.  終了する[**可能な**編集モードを。
9.  ** [戻る**、[**される**ワークスペースを終了する
10. 作業を保存します**発行ワークスペース**

**注記: ** **ビューの会計**モバイル ページ、Microsoftがこれまでに作成したモバイル ページのいずれかに現在リンクされていない。 ユーザーがモバイル デバイス**請求書の詳細**ページから**ビューの会計**ページに移動するためのお**請求書の詳細**ページから**ビューの会計**ページのナビゲーションを指定する必要があります。 ただし、JavaScriptによって追加ロジックを使用して、ナビゲーションを設定します。

1.  [先に作成した開き、次のコードで強調表示された行を追加します。.jsファイルを。 このコードは、の操作を実行します:
    1.  して、ユーザーがワークスペースから**ビューの会計**ページに直接アクセスできないという保証ができます。
    2.  これは**請求書の詳細**ページから**ビューの会計**ページのナビゲーション コントロールを設定します。

> [!NOTE] 
> JSコードのページなどのコントロールの名前は、ワークスペースの同じである必要があります。

1.  機能の基本 (metadataService、dataService、cacheService、$q) {返品{appInit: 機能 (appMetadata) {する必要がある//の非表示を表示する見えないmetadataService.configureControl (「の仕入先請求書に、非表示ShowAccept 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowApprove 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowReject 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowDelegate 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowRequestChange 「」、{: }調整する) こと;              metadataService.configureControl (「の仕入先請求書に、非表示ShowRecall 「」、{: }調整する) こと;                metadataService.configureControl (「の仕入先請求書に、非表示ShowComplete 「」、{: }調整する) こと;            metadataService.configureControl (「の仕入先請求書に、非表示ShowResubmit 「」、{: }調整する) こと;                //の非表示にルート ナビゲーションmetadataService.hideNavigation (「会計」) の適用にページのすること;                説明metadataService.addLink請求書詳細 (「」、会計nav制御」、「会計」、「会計」、「を参照) //Link;            }、pageInit: 機能 (pageMetadata、パラメーター) { (pageMetadata.Nameの== 「請求書詳細」) //{基づくワークフロー ステップの表示/非表示のワークフロー アクションmetadataService.configureActionに使用します (「」、{表示: }調整する) こと;                    metadataService.configureAction承認します (「」、{表示: }調整する) こと;                    metadataService.configureAction (表示されている「否認」、{: }調整する) こと;                    metadataService.configureAction (表示されている「委任」、{: }調整する) こと;                    metadataService.configureAction (表示されている「要求」変更、{: }調整する) こと;                    metadataService.configureAction (表示されている「取り消すには、{: }調整する) こと;                    metadataService.configureAction完了します (「」、{表示: }調整する) こと;                    metadataService.configureAction再送信します (「」、{表示: }調整する) こと;

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  **ロジック**タブの前のコードを上書きする場合に選択して、ワークスペースのコード ファイルをアップロードします。
3.  終了する[**可能な**編集モードを。
4.  ** [戻る**、[**される**ワークスペースを終了する
5.  作業を保存します**発行ワークスペース**

### <a name="validation"></a>検証

モバイル デバイス、アプリケーションを開いて、工程のインスタンス365 for Operationsに接続します。 仕入先請求書が校閲自分に割り当てられている会社に署名することを確認します。 次の操作を行えます必要があります:

-   **自分の承認**ワークスペースを表示します。
-   **自分の承認**ワークスペースにあけ**、自分の仕入先請求書**ページを表示します。
-   **に自分の仕入先請求書**]ページで、"自分に割り当てられている請求書の一覧にドリルダウン。
-   請求書の一つにあけ、請求書ヘッダーの詳細と明細行の詳細を参照してください。
-   詳細]ページおよびリンクを添付ファイルに表示、および添付ファイルの一覧に移動し、添付ファイルを表示、このリンクを使用します。
-   詳細]ページおよびリンクを**ビューの会計**ページに表示、および配分のページに移動し、配分を表示、このリンクを使用します。
-   詳細]ページおよび**工程**メニューの順にクリックして、ワークフロー ステップに適用できるワークフロー アクションを実行します。

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Fabrikamの複雑な請求書承認のシナリオの作成
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>シナリオの属性</th>
<th>応答</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>請求書ヘッダーのユーザーは、フィールドを携帯電話経験に表示するし、注文でか。</td>
<td><ol>
<li>仕入先名</li>
<li>請求金額</li>
<li>請求先/元 ID</li>
<li>請求書番号</li>
<li>請求日</li>
<li>請求明細</li>
<li>期日</li>
<li>請求書通貨</li>
</ol></td>
</tr>
<tr class="even">
<td>請求明細行のユーザーは、フィールドを携帯電話経験に表示するし、注文でか。</td>
<td><ol>
<li>調達カテゴリ</li>
<li>件数</li>
<li>単価</li>
<li>明細行の正味金額</li>
<li>1099 金額</li>
</ol></td>
</tr>
<tr class="odd">
<td>請求書に、請求明細行があるか。 80-20ルールをここに適用され、80日に対して最適化します。</td>
<td>5</td>
</tr>
<tr class="even">
<td>ユーザーが検証中にモバイル デバイスの会計配分 (請求書のコード) が表示されるか。</td>
<td>有</td>
</tr>
<tr class="odd">
<td>複数会計配分 (拡張価格、売上税、雑費など) 請求明細行のためですか。 再度、80-20ルールを適用します。</td>
<td>拡張価格: 2:売上税 二つの請求: 2</td>
</tr>
<tr class="even">
<td>請求書に、請求書ヘッダーの会計配分があるか。 その場合、これらの勘定の配分がデバイスで使用する必要がありますか。</td>
<td>不使用</td>
</tr>
<tr class="odd">
<td>ユーザーはデバイスの請求書について、その添付ファイルが表示されるか。</td>
<td>有</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>演習

次のシナリオ バリエーションは2.の要件に基づいてシナリオ1の場合、できます。 [学習目的で実行できる演習としてこのセクションを使用します。

1.  詳細の請求明細行のシナリオ2で予定されているため、設計に次の変更がモバイル デバイスのユーザー エクスペリエンスの最適化ができます:
    1.  詳細の表示の請求明細行の結果 (シナリオで、1) のユーザーは別のモバイル ページの行の表示を選択できます。
    2.  複数の請求明細行には、このシナリオでは、想定されるため、モバイル機器の配送ページを作成すると、** VendMobileInvoiceAllDistributionTree **ページを使用しているシナリオ (1) 配分に行を関連するには、ように、ユーザーに複雑なかもしがあります。 したがって、配分のページを作成するのに** VendMobileInvoiceLineDistributionTree **ページを使用します。
    3.  原則的には、配分がこのシナリオで請求明細行のコンテキストで表示される必要があります。 従って配分ページが表示されるようにユーザーによって行にドリルダウンできることを、確認してください。 そのヘッダーに、シナリオ1.のページの詳細を示すようにドリルダウンして設定する場合でも、ページの機能を使用します。

2.  複数の金額のタイプがシナリオ2の配分 (売上税、雑費など) 予想されるため、金額のタイプの説明を表示することもできます。  (ただし、シナリオ1.でこの情報は省略できます) 

## <a name="conclusion"></a>まとめ
携帯電話プラットフォーム、アプリケーション機能は、組織のユーザー ベースに対して最適化された携帯電話シナリオを作成することができます。 このトピックに示されている例に基づいて、他のバリエーションについて、特定のニーズを満たす別の経験を作成できます。


