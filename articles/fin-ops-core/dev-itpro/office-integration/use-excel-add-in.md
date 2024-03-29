---
title: Excel でのエンティティ データの表示および更新
description: この記事では、Microsoft Excel でエンティティ データを開き、Excel 用の Microsoft Dynamics Excel アドインを使用してそのデータを表示、更新、また編集する方法を説明します。
author: jasongre
ms.date: 05/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 388be651164af622dbabd7b2c7b3437233454bea
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108604"
---
# <a name="view-and-update-entity-data-with-excel"></a>Excel でのエンティティ データの表示および更新 

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]


この記事では、Microsoft Excel でエンティティ データを開き、Excel 用の Microsoft Dynamics Excel アドインを使用してそのデータを表示、更新、また編集する方法を説明します。 エンティティ データを開くには、Excel または財務と運用アプリのいずれからでも開始できます。

Excel でエンティティ データを開くことにより、Excel アドインを使用して迅速かつ簡単にデータを表示し編集することができます。 このアドインには Microsoft Excel 2016 以降が必要です。

> [!NOTE]
> Microsoft Azure Active Directory (Azure AD) テナントが Active Directory フェデレーション サービス (AD FS) を使用するようにコンフィギュレーションされている場合は、Excel のアドインに正しくサインインできるように、2016 年 5 月の Office の更新が適用されていることを確認する必要があります。

Excel アドインを使用する方法に関する詳細は、[ヘッダーと明細行のパターンの Excel テンプレートを作成する](https://youtu.be/RTicLb-6dbI) のショート ビデオをご覧ください。

## <a name="open-entity-data-in-excel-when-you-start-from-a-finance-and-operations-app"></a>財務と運用アプリから開始して Excel でエンティティ データを開く
1. 財務と運用アプリのページで、**Microsoft Office で開く** を選択します。

    そのページのルート データ ソース (テーブル) がエンティティのルート データ ソースと同じである場合は、既定の **Excel で開く** オプションがそのページに生成されます。 **Excel で開く** オプションは **すべての仕入先** や **すべての顧客** などの頻繁に使用するページに表示されます。
 
2. **Excel で開く** オプションを選択し、生成されるブックを開きます。 このブックには、エンティティのバインディング情報、環境へのポインター、また Excel アドインへのポインターがあります。
3. Excel で **編集機能を有効にする** を選択し、Excel アドインが実行されるようにします。 Excel のウィンドウ右側のウィンドウで Excel アドインが実行されます。
4. 初めて Excel アドインを実行する場合は、**このアドインを信頼します** を選択します。
5. サインインするようにとのメッセージが表示されたら、**サインイン** を選択し、財務と運用アプリへのサインインに使用するのと同じ資格情報を用いてサインインします。 可能な場合、Excel アドインはブラウザーからのサインイン コンテキストを使用し、自動的にサインインします。 (オペレーティング システムに基づいて使用されるブラウザーの詳細については、[Office アドインで使用されるブラウザー](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins) を参照してください。サインインが正常に行われるか確認するには、Excel アドインの右上隅にあるユーザー名を確認します。 

Excel アドインが、選択したエンティティのデータを自動的に読み取ります。 Excel アドインが読み込むまでブックにデータはないことに注意してください。

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Excel から開始して Excel でエンティティ データを開く
1. Excel の **挿入** タブの **アドイン** グループで、**ストア** を選択して Office ストアを開きます。
2. Office ストアで、**Dynamics** で検索し、**Microsoft Dynamics Office アドイン** (Excel アドイン) の隣の **追加** を選択します。
3. 初めて Excel アドインを実行する場合は、**このアドインを信頼します** を選択して Excel アドインの実行を有効化します。 Excel のウィンドウ右側のウィンドウで Excel アドインが実行されます。
4. **サーバー情報の追加** を選択して **オプション** ウィンドウを開きます。
5. お使いのブラウザで、ターゲットの財務と運用アプリ インスタンスから URL をコピーし、それを **サーバー URL** フィールドに貼り付けてから、ホスト名以降をすべて消去します。 結果の URL はホスト名のみである必要があります。

    たとえば、URLが `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage` の場合、`https://xxx.dynamics.com` を除くすべてを削除します。

6. **OK** を選択してから **はい** を選択し、変更を確認します。 Excel アドインが再開しメタデータを読み込みます。

    **デザイン** ボタンが使用できるようになりました。 Excel アドインに **アプレットの読み込み** リンクがある場合は、正しいユーザーとしてサインインしていない可能性があります。 この問題への対処の詳細については、[アプレットの読み込み](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) のトラブルシューティング エントリを参照してください。

7. **デザイン** を選択します。 Excel アドインがエンティティ メタデータを取得します。
8. **テーブルの追加** を選択します。 エンティティの一覧が表示されます。 エンティティは「名前 - ラベル」形式で一覧表示されます。
9. 一覧にある **顧客 - 顧客** などのエンティティを選択し、**次へ** を選択します。
10. フィールドを **使用可能なフィールド** リストから **選択されたフィールド** リストに追加するには、そのフィールドを選択してから **追加** を選択します。 また、**利用可能なフィールド** リストをダブルクリックします。
11. **選択されたフィールド** リストへフィールドの追加が完了したら、カーソルがブックの正しい場所 (たとえば、セル A1) にあることを確認し、**完了** を選択します。 その後 **完了** を選択してデザイナーを終了します。
12. **更新** を選択してデータを取得します。

## <a name="view-and-update-entity-data-in-excel"></a>Excel でのエンティティ データの表示および更新
Excel アドインがエンティティ データをブックに読み込んだら、Excel アドインで **更新** を選択することでいつでもデータを更新できます。

## <a name="edit-entity-data-in-excel"></a>Excel でのエンティティ データの編集
Excel アドインで **公開** を選択することにより、必要に応じてエンティティ データを変更してから財務と運用アプリに再公開することができます。 レコードを編集するには、ワークシートのセルを選択し、セルの値を変更します。 新しいレコードを追加するには、次のいずれかの手順を実行します。

- データ ソース テーブルの任意の場所をクリックし、Excel アドインで **新規** を選択します。
- データ ソース テーブルの最終行の任意の場所をクリックし、カーソルがその行の最終列から出て新しい行が作成されるまで Tab キーを押します。
- データ ソース テーブルの真下の行の任意の場所をクリックして、セルへのデータ入力を開始します。 そのセルからフォーカスを移動させると、テーブルが拡張してその新しい行を含めます。
- ヘッダー レコードのフィールド バインディングには、いずれかのフィールドを選択し、Excel アドインの **新規** を選択します。

新しいレコードは、ワークシートですべてのキーと必須フィールドが選択されている場合、もしくはフィルタ条件を使用して既定値が入力された場合にのみ作成できることに注意してください。

レコードを削除するには、次のいずれかの手順を実行します。

- 削除するべきワークシートの行の横にある行番号を右クリックし、**削除** をクリックします。
- 削除するべきワークシートの行の任意の場所を右クリックし、**削除**&gt;**表の行** をクリックします。

関連するデータ ソースとしてデータ ソースが関連付けて追加される場合、行の前にヘッダーが発行されます。 他のデータ ソースとの間に依存関係がある場合は、既定の公開オーダーを変更する必要があるかもしれません。 公開オーダーを変更する場合、Excel アドインで **オプション** ボタン (ギヤ記号) を選択してから、**データ コネクタ** クイック タブで **公開オーダーのコンフィギュレーション** を選択します。

## <a name="add-or-remove-columns"></a>列の追加または削除
デザイナーを使用して、ワークシートに自動的に追加された列を調整することができます。

> [!NOTE]
> **デザイン** ボタンが Excel アドインで **フィルタ** ボタン下に表示されない場合、データ ソース デザイナーを有効にする必要があります。 **オプション** ボタン (ギヤ記号) を選択してから、**デザインの有効化** チェック ボックスをオンにします。

1. Excel アドインで **デザイン** を選択します。 すべてのデータ ソースが一覧表示されます。
2. データ ソースの横にある **編集** ボタン (鉛筆記号) を選択します。
3. 必要に応じて **選択されたフィールド** リストの一覧を調整します。

    - フィールドを **使用可能なフィールド** リストから **選択されたフィールド** リストに追加するには、そのフィールドを選択してから **追加** を選択します。 また、**利用可能なフィールド** リストをダブルクリックします。
    - **選択されたフィールド** リストからフィールドを削除するには、そのフィールドを選択してから **削除** を選択します。 または、そのフィールドをダブルクリックします。
    - フィールドの順序を変更するには、**選択されたフィールド** リストで対象のフィールドを選択してから **上へ** または **下へ** を選択します。

4. データ ソースに変更を適用するには、**更新** を選択します。 その後 **完了** を選択してデザイナーを終了します。
5. フィールド (列) を追加した場合、**更新** を選択して更新されたデータを取得します。

## <a name="change-the-publish-batch-size"></a>バッチ サイズの発行の変更
ユーザーが Excel アドインを使用してデータ レコードに対する変更を公開すると、更新はバッチで送信されます。 既定 (かつ最大) の公開バッチ サイズは 100 行です。ただし、Excel から更新を公開しようとするとタイムアウトが発生する場合は特に、**Excel アドインで公開するバッチ サイズの構成を許可する** 機能を使用して公開バッチ サイズを下げ、柔軟に対処することができます。

システム管理者は 、**Office アプリケーション パラメーター** ページの **アプリケーション パラメーター** セクションの **バッチ制限の公開** フィールドを設定することにより、"Excelで開く" ブックの発行バッチ サイズに対するシステム全体の制限を指定できます。

Excel アドインを使用すると、発行のバッチ サイズを個々のブックに対して変更することもできます。

1. Excel でブックを開きます。
2. Excel アドインの右上隅にある **オプション** (ギア) ボタンを選択します。
3. 必要に応じて **バッチ サイズの発行** フィールドを設定します。 設定する値は、システム全体の公開バッチ制限を超える必要があります。
4. **OK** を選択します。
5. ワークブックを保存します。 アドインの設定を変更した後にブックを保存しない場合、ブックを再度開くと、その変更は維持されません。

Excel ワークブック テンプレートの作成者は、テンプレートをシステムにアップロードする前に、同じ手順でテンプレートのバッチ サイズを設定できます。

## <a name="copy-environment-data"></a>環境データのコピー

1 つの環境からブックに読み込めるデータは、別の環境にもコピーできます。 ただし、ブック内のデータ キャッシュは引き続き既存のデータとして扱われるために、接続 URL だけを変更することはできません。 代わりに、環境データのコピー機能を使用して、新しいデータとして新しい環境にデータを発行する必要があります。

1. **オプション** ボタン (ギヤ記号) を選択してから、**データ コネクタ クイック タブ** で **環境データのコピー** を選択します。 
2. 新しい環境にサーバー URL を入力してください。 
3. **OK** を選択してから、**はい** を選択しアクションを確認します。 Excel アドインが再開し、新しい環境に接続します。 ブック内の既存データは、新しいデータとして扱われます。

    Excel アドインの再起動後に、ブックが環境コピー モードになっているとメッセージ ボックスが表示されます。

4. 新しいデータとして新しい環境にデータをコピーするには、**発行** を選択します。 環境コピー操作をキャンセルし、新しい環境で既存のデータを確認するには、**更新** を選択します。

## <a name="troubleshooting"></a>トラブルシューティング
生じる問題のいくつかは簡単なステップで解決できます。

- **"アプレットの読み込み" リンクが表示される** – この問題の詳細については、[アプレットの読み込み](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) のトラブルシューティング エントリを参照してください。 
- **禁止されたメッセージを受信する** - Excel アドインのメタデータの読み込み中に「禁止された」メッセージを受信する場合、Excel アドインにサインインしているアカウントには、対象のサービス、インスタンス、またはデータベースを使用するためのアクセス許可がありません。 この問題を解決するために、Excel アドインの右上隅に正しいユーザー名が表示されることを確認します。 正しくないユーザー名が表示されている場合は、それを選択し、サインアウトしてから再度サインインします。
- **Excel 上に空白の Web ページが表示される** – サインイン プロセス中に空白の Web ページが開く場合、そのアカウントには AD FS が必要ですが、Excel のアドインを実行している Excel のバージョンがサインイン ダイアログ ボックスを読み込めるほど新しくありません。 この問題を解決するには、使用している Excel のバージョンを更新します。 繰延チャンネルの企業にいる場合に Excel のバージョンを更新するには、[繰延チャンネルから現在のチャンネルに移動する](/deployoffice/overview-update-channels) ために [Office 配置ツール](/deployoffice/overview-office-deployment-tool) を使用します。
- **データの変更を公開する際にタイム アウトが返されます** - データ変更をエンティティに公開しようとしている間にタイム アウト メッセージを受信する場合は、影響を受けるワークブックのバッチ サイズを減らすことを検討してください。 レコードの変更で大量のロジックをトリガするエンティティは、タイム アウトを防ぐため、より小さいバッチで更新を送信する必要がある場合があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

