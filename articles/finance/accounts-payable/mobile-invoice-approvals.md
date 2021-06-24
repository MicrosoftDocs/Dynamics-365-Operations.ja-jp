---
title: モバイルによる請求書承認
description: このトピックは、サポート案件としてモバイルのベンダー請求書の承認を取得することによる、モバイル シナリオを設計するための実際的なアプローチを提供することを目的としています。
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 78ab17952801a1d77f321e212bb61e9b45d93216
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189205"
---
# <a name="mobile-invoice-approvals"></a>モバイルによる請求書承認

[!include [banner](../includes/banner.md)]

モバイル機能により、ビジネス ユーザーはモバイル エクスペリエンスを設計できます。 高度なシナリオでは、開発者はプラットフォームを使用して、必要に応じて機能を拡張することもできます。 モバイルに関する新しい概念のいくつかを学ぶ最も効果的な方法は、いくつかのシナリオを設計するプロセスを経ることです。 このトピックは、サポート案件としてモバイルのベンダー請求書の承認を取得することによる、モバイル シナリオを設計するための実際的なアプローチを提供することを目的としています。 このトピックは、シナリオのさまざまなバリエーションを設計するのに役立ちますが、仕入先請求書に関連しない他のシナリオにも適用できます。

## <a name="prerequisites"></a>前提条件

| 前提条件                                                                                            | 説明                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| モバイル ハンドブックの先行読取                                                                                |[モバイル プラットフォーム](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 Finance                                                                              | バージョン 1611 およびプラットフォーム更新プログラム 3 (2016 年 11 月) がある環境                   |
| 更新プログラム KB 3204341 をインストールします。                                                                              | タスク レコーダーは誤って 2 つのドロップダウン ダイアログの Close コマンドを記録できます。これはプラットフォーム更新プログラム 3 (2016 年 11 月の更新プログラム) に含まれています。 |
| 更新プログラム KB 3207800 をインストールします。                                                                              | この修正プログラムは、モバイル クライアント上で表示される添付ファイルを有効にします。これはプラットフォーム更新プログラム 3 (2016 年 11 月の更新プログラム) に含まれています。           |
| 更新プログラム KB 3208224 をインストールします。                                                                              | モバイルの仕入先請求書承認アプリケーションのアプリケーション コードです。これはバージョン 7.0.1 (2016 年 5 月) に含まれています。                          |
| モバイル アプリがインストールされている Android、iOS または Windows デバイス。 | 適切なアプリ ストアでアプリを検索します。                                                                                                                     |

## <a name="introduction"></a>はじめに
ベンダー請求書のモバイル承認には、「前提条件」セクションに記載されている 3 つの修正プログラムが必要です。 これらの修正プログラムは、請求書承認のためのワークスペースを提供しません。 ワークスペースがモバイルのコンテキストでどのようなものかを知るには、「前提条件」セクションで説明したモバイル ハンドブックをお読みください。 請求書承認ワークスペースを設計する必要があります。 

すべての組織は、ベンダー請求書の異なるビジネス プロセスを調整し定義します。 ベンダーの請求書承認のためのモバイル エクスペリエンスを設計する前に、ビジネス プロセスの次の側面を考慮する必要があります。 このアイデアは、これらのデータ ポイントを可能な限り使用して、デバイス上のユーザー エクスペリエンスを最適化することです。

-   モバイル エクスペリエンスで、請求書ヘッダーのどのフィールドを、どのような順序で表示したいですか?
-   モバイル エクスペリエンスで、請求書行のどのフィールドを、どのような順序で表示したいですか?
-   請求書にはいくつの請求書明細行がありますか? 80-20 ルールをここで適用し、80 パーセントを最適化します。
-   ユーザーは、レビュー中にモバイル デバイス上の勘定配賦 (請求書コーディング) を見たいでしょうか? この質問に対する回答が「はい」の場合は、次の質問を検討してください。
    -   請求書行にはいくつの勘定配賦 (拡張価格、消費税、料金、分割など) がありますか? 再度、80-20 ルールを適用します。
    -   請求書には請求書ヘッダーに勘定配賦も含まれていますか? もしそうなら、これらの勘定配賦はデバイス上で利用できるはずですか?

    > [!NOTE]
    > このトピックでは、現在モバイル シナリオでこの機能がサポートされていないため、勘定配賦の編集方法については説明していません。

-   ユーザーはデバイス上の請求書の添付ファイルを見たいですか?

請求書承認のためのモバイル エクスペリエンスの設計は、これらの質問に対する回答によって異なります。 その目的は、組織内のモバイルでのビジネス プロセスのユーザー エクスペリエンスを最適化することです。  このトピックの残りでは、前述の質問とは異なる回答に基づいた 2 つのシナリオのバリエーションを見ていきます。 

一般的なガイダンスとして、モバイル デザイナーと協力している場合は、アップデートを失わないように変更を「公開」してください。

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Contoso の簡単な請求書承認シナリオの設計
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
<td>モバイル エクスペリエンスで、請求書ヘッダーのどのフィールドを、どのような順序で表示したいですか?</td>
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
<td>モバイル エクスペリエンスで、請求書行のどのフィールドを、どのような順序で表示したいですか?</td>
<td><ol>
<li>調達カテゴリ</li>
<li>件数</li>
<li>単価</li>
<li>明細行の正味金額</li>
<li>1099 金額</li>
</ol></td>
</tr>
<tr class="odd">
<td>請求書にはいくつの請求書明細行がありますか? 80-20 ルールをここで適用し、80 パーセントを最適化します。</td>
<td>1</td>
</tr>
<tr class="even">
<td>ユーザーは、レビュー中にモバイル デバイス上の勘定配賦 (請求書コーディング) を見たいでしょうか?</td>
<td>有</td>
</tr>
<tr class="odd">
<td>請求書行にはいくつの勘定配賦 (拡張価格、消費税、料金、など) がありますか? 再度、80-20 ルールを適用します。</td>
<td>拡張価格: 2 売上税: 0 料金: 0</td>
</tr>
<tr class="even">
<td>請求書には請求書ヘッダーに勘定配賦も含まれていますか? もしそうなら、これらの勘定配賦はデバイス上で利用できるはずですか?</td>
<td>不使用</td>
</tr>
<tr class="odd">
<td>ユーザーはデバイス上の請求書の添付ファイルを見たいですか?</td>
<td>はい</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>ワークスペースの作成

1.  ブラウザーで、アプリケーションにログインします。
2.  サインインした後、次の例のように **&mode=mobile** を URL に追加し、ページを更新します: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  ページの右上角にある **設定** (歯車) ボタンをクリックし、次に **モバイル アプリ** をクリックします。 モバイル アプリのデザイナーは、タスク レコーダーが表示されるのと同じように表示される必要があります。
4.  新しいワークスペース作成するには、**追加** をクリックします。 この例として、ワークスペースを **自分の承認** と名付けます。
5.  説明を入力します。
6.  ワークスペースの色を選択します。 ワークスペースの色は、このワークスペースのモバイル エクスペリエンスの全体的なスタイルに使用されます。
7.  ワークスペースのアイコンを選択します。
8.  **完了** をクリックします。
9.  変更を保存するには、**ワークスペースを公開** をクリックします。

### <a name="vendor-invoices-assigned-to-me"></a>自分に割り当てられている仕入先請求書

設計する必要がある最初のモバイル ページは、レビューのためにユーザーに割り当てられている請求書の一覧です。 このモバイル ページを設計するには、**VendMobileInvoiceAssignedToMeListPage** ページを使用します。 この手順を完了する前に、少なくとも 1 つの仕入先請求書がレビューのために割り当てられていること、および請求書行に 2 つの配布があることを確認してください。 この設定は、このシナリオの要件を満たしています。

1.  URL で、メニューの名前を **VendMobileInvoiceAssignedToMeListPage** に置き換え、**買掛金勘定** モジュールの **私に割り当てられた保留中の仕入先請求書** リスト ページのモバイル版を開きます。 システムに割り当てられている請求書の数に応じて、このページにこれらの請求書が表示されます。 特定の請求書を検索するには、左側のフィルターを使用します。 ただし、この例では特定の請求書は必要ありません。 割り当てられた請求書を要求するだけで、モバイル ページをデザインすることができます。 利用可能な新しいページは、ベンダーの請求書のモバイル シナリオを開発するために特別に設計されています。 したがって、これらのページを使用する必要があります。 URL は次の URL のようになります。また、入力後、図に示されているページが表示されます: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile 

    [![自分に割り当てられた保留中の仕入先請求書ページ](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
    
2.  ページの右上角にある **設定** (歯車) ボタンをクリックし、次に **モバイル アプリ** をクリックします
3.  ワークスペースを選択し、**編集** をクリックします。
4.  **ページを追加** をクリックして、最初のモバイル ページを作成します。
5.  **私のベンダーの請求書** などの名前と、**レビュー用に割り当てられたベンダーの請求書** などの説明を入力します。
6.  **完了** をクリックします。
7.  モバイル デザイナーの **フィールド** タブで **フィールドの選択** をクリックします。 リスト ページの列は、次の図のようにする必要があります。 

    [![自分に割り当てられた保留中の仕入先請求書ページ](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
    
8.  リスト ページから、モバイル ページのユーザーに表示する必要がある列を追加します。 追加する順序は、フィールドがエンド ユーザーに表示される順序です。 フィールドの順序を変更する唯一の方法は、すべてのフィールドを再選択することです。 このシナリオの要件に基づいて、次の 8 つのフィールドが必要です。 しかし、一部のユーザは、8 つのフィールドが多くの情報をモバイル デバイス上に持つと考える可能性があります。 したがって、モバイル リスト ビューで最も重要なフィールドのみを表示します。 残りのフィールドは、後で設計する詳細ビューに表示されます。 今のところ、次のフィールドを追加します。 モバイル ページに追加するには、これらの列のプラス記号 (**+**) をクリックします。
    - 仕入先名
    - 請求合計
    - 請求先/元 ID
    - 請求書番号
    - 請求日

    フィールドが追加されると、モバイル ページは次の図のようになります。 
    
    [![フィールドの後ページが表示される](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)

9.  ワークフロー アクションを後で有効にできるように、次の列も追加する必要があります。
    - 完了したタスクを表示する
    - 委任タスクを表示する
    - リコールタスクを表示する
    - 拒否タスクを表示する
    - リクエスト完了タスクを表示する
    - 再送信タスクを表示する

10. **完了** をクリックして、編集モードを終了します。
11. **戻る**、次に **完了** をクリックして、ワークスペースを終了します。
12. **ワークスペースの公開** をクリックして作業を保存します。
13. **請求書** の買掛金勘定パラメータ フォームの **仕入先請求書一覧の請求書総額の表示** を有効化します。 このパラメータを有効にすることによってのみ、請求書合計が計算され、保留中の仕入先請求一覧ページに表示されます。 これは前提条件の修正プログラム 3208224 の一部の新しい機能です。

### <a name="vendor-invoice-details"></a>ベンダー請求書の詳細

モバイル用の請求書の詳細ページを設計するには、**VendMobileInvoiceHeaderDetails** ページを使用します。 システムに登録されている請求書の数に応じて、このページには最も古い請求書（最初に作成された請求書）が表示されます。 特定の請求書を検索するには、左側のフィルターを使用します。 ただし、この例では特定の請求書は必要ありません。 モバイルページを設計できるように、請求書データが必要です。 

[![ワークフロー ページ](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. URL で、メニュー アイテムの名前を **VendMobileInvoiceHeaderDetails** に置き換えてフォームを開きます。

2. **設定** (ギア) ボタンからモバイル デザイナーを開きます。

3. ワークスペースで編集モードを開始するには、**編集** ボタンをクリックします。

4. 前に作成した **私のベンダーの請求書** ページを選択して、それから **編集** をクリックします。

5. **フィールド** タブで、**グリッド** 列見出しをクリックします。

6. **プロパティ &gt; ページの追加** をクリックします。 **注:** **グリッド** 見出しをクリックしてページを追加すると、詳細ページとの関係が自動的に確立されます。

7. **請求書の詳細** などのページタイトルと、**請求書ヘッダーと行の詳細の表示** などの説明を入力します。

8. **フィールドの選択** をクリックします。 追加する順序は、フィールドがエンド ユーザーに表示される順序に留意してください。 フィールドの順序を変更する唯一の方法は、すべてのフィールドを再選択することです。 

9. このシナリオの要件に基づいて、ヘッダーから次のフィールドを追加します。
   - 仕入先名
   - 請求合計
   - 請求先/元 ID
   - 請求書番号
   - 請求日
   - 請求明細
   - 期日
   - 請求書通貨

10. ページの行グリッドから次のフィールドを追加します。
    - 調達カテゴリ
    - 件数
    - 単価
    - 明細行の正味金額
    - 1099 金額

11. 前の 2 つの手順のすべてのフィールドが追加されたら、**完了** をクリックします。 ページは次の図のようにする必要があります。
    
    [![追加されたフィールドを示す図](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)

12. **完了** をクリックして、編集モードを終了します。

13. **戻る**、次に **完了** をクリックして、ワークスペースを終了します。

14. **ワークスペースの公開** をクリックして作業を保存します

### <a name="workflow-actions"></a>ワークフロー アクション

ワークフロー アクションを追加するには、**VendMobileInvoiceHeaderDetails** ページを使用します。 このページを開くには、先ほどと同様に、URL 内のメニュー項目の名前を置き換えます。 次に、**設定** (ギア) ボタンからモバイル デザイナーを開きます。  詳細ページにワークフロー アクションを追加するには、次の手順に従います。 ワークフローアクションを利用できるようにするため、請求書は適切な状態で割り当てられる必要があります。

#### <a name="record-workflow-actions"></a>ワークフロー アクションを記録
1.  ワークスペースで編集モードを開始するには、**編集** ボタンをクリックします。
2.  前に作成した **請求書の詳細** ページを選択し、**編集** をクリックします。
3.  **アクション** タブで、**アクションの 追加** をクリックします。
4.  **承認** などのアクションタイトルと、**請求書の承認** などの説明を入力します。 ここに入力するアクション タイトルは、モバイル アプリでユーザーに表示されるアクションの名前になります。
5.  **完了** をクリックします。
6.  **フィールドの選択** をクリックします。
7.  **VendMobileInvoiceHeaderDetails** ページのワークフロー プロセスを実行し、記録するアクションを完了します。 このプロセス中にワークフロー コメントを入力して、コメント フィールドもモバイル エクスペリエンスに含めるようにしてください。
8.  ワークフロー アクションの実行後、**完了** をクリックしてフィールドの選択タスクを完了します。
9.  **完了** をクリックして、編集モードを終了します。
10. **戻る**、次に **完了** をクリックして、ワークスペースを終了します。
11. **ワークスペースの公開** をクリックして作業を保存します
12. 必要なすべてのワークフロー アクションを記録するには、前の手順を繰り返します。 

#### <a name="create-a-js-file"></a>.js ファイルの作成
1. メモ帳または Microsoft Visual Studio を開き、次のコードを貼り付けます。 ファイルを .js ファイルとして保存します。 このコードを使い、次の処理を行います。
    - 以前にモバイル リスト ページに追加した追加のワークフロー関連の列は非表示になっています。 アプリケーションがコンテキスト内にその情報を持ち、次のステップを実行できるように、これらの列を追加しました。
    - アクティブなワークフロー ステップに基づいて、それらのアクションのみを表示するロジックが適用されます。

    > [!NOTE]
    > コード内のページおよび他のコントロールの名前は、ワークスペース内で同じ名前でなければなりません。

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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
    ```

2.  **ロジック** タブを選択して、コード ファイルをワークスペースにアップロードします。
3.  **完了** をクリックして、編集モードを終了します。
4.  **戻る**、次に **完了** をクリックして、ワークスペースを終了します。
5.  **ワークスペースの公開** をクリックして作業を保存します

### <a name="vendor-invoice-attachments"></a>ベンダー請求書の添付

1. ページの右上角にある **設定** (歯車) ボタンをクリックし、次に **モバイル アプリ** をクリックします

2. ワークスペースで編集モードを開始するには、**編集** ボタンをクリックします。

3. <strong>前に作成した請求書の詳細 **ページを選択し、それから**編集</strong>をクリックします。

4. 以下のように、**文書管理** オプションを **はい** に設定します。 **注:** モバイル デバイスに添付ファイルを表示する必要がない場合は、このオプションをデフォルト設定の **いいえ** に設定しておくことができます。
   
   ![ドキュメント管理](./media/docmanagement-216x300.png)

5. **完了** をクリックして、編集モードを終了します。

6. **戻る**、次に **完了** をクリックして、ワークスペースを終了します。

7. **ワークスペースの公開** をクリックして作業を保存します

### <a name="vendor-invoice-line-distributions"></a>ベンダー請求書行の配布

このシナリオの要件により、行レベルの配布のみが存在し、請求書には常に 1 行しか含まれないことが確認されます。 このシナリオは単純なので、モバイル デバイスのユーザー エクスペリエンスは、配布を表示するためにユーザーが複数のレベルをドリルダウンする必要がないほど単純でなければなりません。 仕入先請求書は、請求書のヘッダーからすべての配布を表示するオプションがあります。 この経験は、モバイル シナリオに必要なものです。 したがって、**VendMobileInvoiceAllDistributionTree** ページを使用してモバイル シナリオのこの部分を設計します。 

> [!NOTE] 
> 要件を知ることで、使用する特定のページと、シナリオを設計する際にユーザーのモバイル エクスペリエンスをどのように最適化するかを決定するのに役立ちます。 2 番目のシナリオでは、そのシナリオの要件が異なるため、異なるページを使用して配布を表示します。

1.  URL で、前と同じように、メニュー項目の名前を置き換えます。 表示されるページは、次の図のようになります。

    [![すべての配分ページ](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)

2.  **設定** (ギア) ボタンからモバイル デザイナーを開きます。

3.  ワークスペースで編集モードを開始するには、**編集** ボタンをクリックします。 **注:** 2 つの新しいページが自動的に作成されたことがわかります。 前のセクションでドキュメント管理を有効にしたため、システムがこれらのページを作成します。 これらの新しいページは無視できます。

4.  **ページの追加** をクリックします。

5.  **会計の表示** などのページ タイトルと、**請求書の会計の表示** などの説明を入力します。

6.  **完了** をクリックします。

7.  **フィールド** タブで、**フィールドの選択** をクリックし、配布ページから次のフィールドを選択して、**完了** をクリックします。
    1.  金額
    2.  通貨
    3.  勘定科目

    > [!NOTE] 
    > このシナリオの要件では、拡張価格だけで配布が行われることが確認されているため、ディストリビューション グリッドから **説明** 列を選択しませんでした。 したがって、ユーザーは、その配信が対象とする金額タイプを決定するために別のフィールドを必要としません。 ただし、次のシナリオでは、このシナリオの要件によって、他の金額タイプに配賦 (たとえば、消費税) があることが指定されているため、この情報を使用 **します**。

8.  **完了** をクリックして、編集モードを終了します。

9.  **戻る**、次に **完了** をクリックして、ワークスペースを終了します。

10. **ワークスペースの公開** をクリックして作業を保存します

#### <a name="adding-navigation-to-view-accounting-page"></a>「会計の表示」ページへのナビゲーションの追加

**会計の表示** モバイル ページは、現在のところ私たちが設計したモバイル ページのいずれにもリンクしていません。 ユーザーはモバイル デバイスの **請求書の詳細** ページから **会計の表示** ページに移動できる必要があるため、**請求書の詳細** ページから **会計の表示** ページまでのナビゲーションを提供する必要があります。 このナビゲーションは JavaScript を介する追加のロジックを使用して確立します。

1.  前に作成した .js ファイルを開き、次のコードで強調表示されている行を追加します。 このコードは 2 つのことを行います:
    1.  ユーザーがワークスペースから **会計の表示** ページに直接ナビゲートできないようにします。
    2.  **請求書の詳細** ページから **会計の表示** ページへのナビゲーション制御を確立します。

    > [!NOTE] 
    > コード内のページおよび他のコントロールの名前は、ワークスペース内で同じ名前でなければなりません。

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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
    ```
    
2.  前のコードを上書きするには、**ロジック** タブを選択してコード ファイルをワークスペースにアップロードします。
3.  **完了** をクリックして、編集モードを終了します。
4.  **戻る**、次に **完了** をクリックして、ワークスペースを終了します。
5.  **ワークスペースの公開** をクリックして作業を保存します

### <a name="validation"></a>妥当性確認

モバイル デバイスからアプリを開き、インスタンスに接続します。 ベンダーの請求書が審査のために割り当てられている会社にサインインしてください。 次の操作を実行できるはずです:

-   **私の承認** ワークスペースを参照してください。
-   **私の承認** ワークスペースをドリルインし、**私のベンダーの請求書** ページを参照してください。
-   **私のベンダーの請求書** ページをドリルインし、割り当てられた請求書の一覧を表示します。
-   請求書の 1 つをドリルインし、請求書ヘッダーの詳細と行の詳細を確認します。
-   詳細ページで、添付ファイルへのリンクを参照し、このリンクを使用して添付ファイル リストに移動し、添付ファイルを表示します。
-   詳細ページで、**会計の表示** ページへのリンクを参照し、このリンクを使用して配布ページに移動し、配布を表示します。
-   詳細ページで、下部にある **操作** メニューをクリックし、ワークフロー ステップに該当するワークフロー アクションを実行します。

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Fabrikam の複雑な請求書承認シナリオの設計
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
<td>モバイル エクスペリエンスで、請求書ヘッダーのどのフィールドを、どのような順序で表示したいですか?</td>
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
<td>モバイル エクスペリエンスで、請求書行のどのフィールドを、どのような順序で表示したいですか?</td>
<td><ol>
<li>調達カテゴリ</li>
<li>件数</li>
<li>単価</li>
<li>明細行の正味金額</li>
<li>1099 金額</li>
</ol></td>
</tr>
<tr class="odd">
<td>請求書にはいくつの請求書明細行がありますか? 80-20 ルールをここで適用し、80 パーセントを最適化します。</td>
<td>5</td>
</tr>
<tr class="even">
<td>ユーザーは、レビュー中にモバイル デバイス上の勘定配賦 (請求書コーディング) を見たいでしょうか?</td>
<td>有</td>
</tr>
<tr class="odd">
<td>請求書行にはいくつの勘定配賦 (拡張価格、消費税、料金、など) がありますか? 再度、80-20 ルールを適用します。</td>
<td>拡張価格: 2 売上税: 2 料金: 2</td>
</tr>
<tr class="even">
<td>請求書には請求書ヘッダーに勘定配賦も含まれていますか? もしそうなら、これらの勘定配賦はデバイス上で利用できるはずですか?</td>
<td>不使用</td>
</tr>
<tr class="odd">
<td>ユーザーはデバイス上の請求書の添付ファイルを見たいですか?</td>
<td>有</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>次のステップ

シナリオ 2 の要件に基づいて、シナリオ 1 で以下のバリエーションを実行できます。 モバイル アプリ エクスペリエンスを向上するには、このセクションを使用してください。

1.  シナリオ 2 では、より多くの請求書行が予想されるため、以下のデザイン変更により、モバイル デバイスのユーザー エクスペリエンスが最適化されます。
    1.  (シナリオ 1 のように) 詳細ページで請求書の行を表示する代わりに、別のモバイル ページに行を表示することを選択できます。
    2.  このシナリオでは複数の請求書行が予想されるため、**VendMobileInvoiceAllDistributionTree** ページを使用してモバイルの配布ページを設計すると (シナリオ 1 のように)、ユーザーは行を配布に関連付けるのが紛らわしく感じる可能性があります。 したがって、**VendMobileInvoiceLineDistributionTree** ページを使用して配布ページを設計します。
    3.  理想的には、このシナリオでは、配布を請求明細行のコンテキストで表示する必要があります。 したがって、ユーザーが行にドリルダウンして配布ページを表示できることを確認してください。 シナリオ 1 のヘッダーおよび詳細ページの場合と同様に、ページ リンク機能を使用してドリルスルーを確立します。

2.  シナリオ 2 の配布では、複数の金額タイプ (消費税、請求など) が予想されるため、金額タイプの説明を表示すると便利です。 (この情報はシナリオ 1 では省略しました。)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
