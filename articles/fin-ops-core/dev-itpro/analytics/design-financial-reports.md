---
title: 財務諸表の表示およびデザイン
description: この記事では、Microsoft Dynamics 365 Finance の財務諸表の表示および作成の練習を提供します。
author: jcart1106
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.form: FinancialReportingSetup
ms.openlocfilehash: 92474e7b99af7d83b2089b6652558630c60824c1
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799521"
---
# <a name="view-and-design-financial-reports"></a>財務諸表の表示とデザイン

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Finance の財務諸表の表示および作成の練習を提供します。 財務報告は、アプリケーション内の表示エクスペリエンスと、財務諸表を作成して編集するクリック ワンス レポート デザイナーで構成されます。

## <a name="exercise-1-generate-and-explore-a-default-financial-report"></a>練習 1: 既定の財務諸表の生成と活用

この練習では、既存の既定のレポートを生成および検討します。 このレポートには、すべての勘定と、勘定の勘定プロパティ (属性) も含まれます。 トランザクションの詳細を表示し、分析コード フィルターを適用し、レポートの通貨を変更します。 最初に、財務報告の分析コードの表示順序を更新します。 これにより、財務諸表の設計および表示だけでなく、分析コードをどのように表示するかも選択できます。

1. 総勘定元帳の、**勘定科目表の分析コード**、**アプリケーション統合用の財務分析コードの構成** に移動します。
2. 次の順序で分析コードを移動します:

    1. 主勘定
    2. 事業単位
    3. コスト センター
    4. 部門

    > [!NOTE]
    > 他の分析コードは現状の順序に残すことができます。

3. 分析コード コンフィギュレーションを保存します。 次に、レポートを生成し、レポートのデータを活用します。
4. 総勘定元帳の **照会およびレポート** の下の **財務レポート** に移動します。
5. **GL の詳細 – 既定** という名前のレポートの行を選択します。
6. **編集** を選択します。

    > [!NOTE]
    > クリック ワンス レポート デザイナーをダウンロードして、ログインするように求めるメッセージが表示されます。 資格情報を使用してログインします。

7. 基準年を 2021 に変更し、**生成** を選択します。 レポート デザイナーからレポートが生成された場合、新しいブラウザーのタブで開きます。新しいブラウザー タブのレポートを活用するか、元のブラウザー タブに移動し、**財務レポート** リストからそのレポートを選択して任意のレポートを開きます。
8. 開いたレポートで、レポートの勘定の詳細に調査する金額の 1 つを選択します。
9. 勘定の詳細で 1 回、データがある勘定を選択し、**レポート トランザクション レベルを表示** します。 レポートのトランザクション レベルで、このレポートのデザインに含まれているプロパティ (属性) を確認できます。 トランザクションおよび勘定に応じて、属性のいくつかまたはすべてが表示されます。
10. レポート トランザクション レベルを閉じます。
11. 同じ勘定または別の勘定を選択し、**伝票トランザクションを開きます**。 伝票トランザクションは、選択した勘定の期間、年および口座と分析コードの組み合わせでフィルタ処理されます。 **伝票トランザクション** では、トランザクションに関する他の情報を活用するために選択できます。
12. **伝票トランザクション** を閉じます。 財務諸表の中で、別の期間と年に対するデータ、または異なる属性および分析コードが適用されたデータを表示するように選択できます。 これは **レポート オプション** を使用して実行されます。
13. **レポート オプション** を選択します。
14. **分析コード フィルターの追加** を選択して、**事業単位** を選択します。
15. フィールドに **001** と入力し、**OK** を選択します。 レポートには 001 の事業単位のデータのみが表示されます。 これは、レポートのカスタマイズされた表示で、他のレポートの表示には使用できません。
16. フィルター処理されたレポートを閉じます。 財務諸表は、アプリケーションに追加されている通貨すべてで表示できます。
17. **通貨** を選択してから、**EUR** を選択します。 ユーロで、レポートが表示されます。 レポートのデザインに含まれる通貨コードまたは通貨記号はすべて適用された通貨で表示されます。 通貨記号が通貨に対して定義されていない場合、通貨記号は表示されません。
18. **GLの詳細** レポートを閉じます。
19. **レポート デザイナー** を閉じます。

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>練習 2: レポート デザインへの追加の勘定プロパティの追加
この練習では、既存の既定のレポートを変更します。 両方の行定義がすべての勘定を含むか、勘定属性を含むように列の定義を更新します。 更新が完了したら、新しく作成されたレポートを生成し、レポートを活用します。 **財務諸表** の一覧から開始します。

1. 総勘定元帳の **照会およびレポート** の下の **財務レポート** に移動します。
2. **試算表の集計 – 既定** という名前のレポート行を選択します。
3. **編集** を選択します。 **集計試算表 - 既定** がレポート デザイナーで開きます。
4. **ファイル**、**名前を付けて保存** を選択し、レポートに **属性の詳細な試算表** という名前を付けます。

    > [!NOTE]
    > Report Designer で新しいレポートが作成されると、**財務諸表** のリストが更新されます。

5. レポート定義から開いた場合は、行定義のアイコンを選択し、**試算表 – 既定の行定義** を開きます。
6. **属性の詳細な試算表** として行定義を保存します。
7. 50 行にカーソルを置いて、**編集**、**分析コードからの行の挿入** を選択します。 分析コードからの行の挿入により、行定義にどのような分析コードを設定するかを選択できます。 この練習では、主勘定を使用して行定義を構築します。
8. **主勘定** がすべてのアンパサンドを含むことを確認し **OK** を選択します。 今回の行の定義には、USMF 法人の主勘定すべてが含まれます。
9. 行 11110 にスクロールし、行 11110 を削除します。
10. 11080 行で、**--- (アンダースコア金額)** を選択します。
11. 11140 行で、列 B に **すべての勘定の合計** と入力します。
12. 列 C で、ドロップダウンから **TOT** を選択します。
13. 列 D で、**50:11080** と入力します。
14. 行定義を **保存** します。 今回の行の定義には、すべての勘定とすべての勘定を一緒に追加する合計行が含まれます。 次に、追加の勘定の属性を含む、列定義を更新します。
15. **属性の詳細な試算表** レポート定義から、列定義アイコンを選択して、**試算表の集計 - 既定** 列定義を開きます。
16. **属性の詳細な試算表** として列定義を保存します。 列定義には、財務データの列、列の説明、および計算列が含まれます。 列定義に属性列を追加して、勘定に関する追加情報を提供します。
17. 次の属性が列定義に追加されます。

    - 仕訳帳番号
    - 仕訳帳の説明
    - トランザクション日付
    - 作成者
    - 最終更新者

18. 列 I で、**ATTR** を列タイプとして選択します。 次に、**仕訳帳番号** を属性のカテゴリとして選択します。
19. 残りの属性に対して列を追加し続けます。
20. **ヘッダー 2** 行で、追加された新しい列それぞれの説明を追加します。
21. 列定義を保存します。 行定義と列定義が更新されたため、レポート定義にそれらを追加する必要があります。
22. **属性の詳細な試算表** レポート定義から、行定義と列定義に対する、属性の詳細な試算表を選択します。
23. 基準年を **2012** に変更します。
24. レポート定義を **保存** し、**生成します**。 レポートの生成が完了しそれを開くと、最初の練習で実行したように、レポートを活用できます。 追加の属性がどのように表示されるかをさまざまな勘定で特定します。
25. **属性の詳細な試算表** レポートを閉じます。
26. **レポート デザイナー** を閉じます。

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>練習 3: レポート ツリーを使用する多次元レポートの作成
この練習では、既存の既定のレポートを変更します。 レポート ツリーを作成し、**コスト センター/部門別損益計算書** を生成するレポートの定義を追加します。 更新が完了したら、**コスト センター/部門別損益計算書** を生成し、レポート ツリーを使用して、レポートを活用します。 **財務諸表** の一覧から開始します。

1. 総勘定元帳の [照会およびレポート] の下の **財務レポート** に移動します。
2. **損益計算書 – 既定** という名前のレポート行を選択します。
3. **編集** を選択します。 **損益計算書 - 既定** がレポート デザイナーで開きます。
4. **ファイル** メニューの **新規** をポイントしてから、**レポート ツリー定義** をクリックします。
5. **編集** メニューで、**分析コードからレポート ユニットを挿入** をクリックします。
6. **コスト センター** を除き、すべての分析コードのチェックボックスをクリアします。
7. **移動元分析コード** フィールドから、原価部門分析コードをクリックし、**007** と入力し、[タブ] キーを押します。 **移動先分析コード** フィールドで、**018** と入力します。
8. **区分別コスト センター** という名前で、生成されるツリーを **保存** します。 レポート ツリーが作成されたので、3 つの新しいロールアップの単位、マーケティング、工程、小売を含むように、レポート ツリーを変更します。
9. **ウィンドウ** メニューの **区分別原価部門** をクリックします。 (レポート ツリーを閉じた場合、ナビゲーション ウィンドウの **レポート ツリー定義** から選択します。)
10. 2 番目の単位をクリックし、**取引の表示** をクリックし、**レポート単位の挿入** アイコンをクリックします。
11. 空白の行のエンティティの列をダブルクリックし、**USMF** を選択します。
12. 列 B および列 C に **マーケティング** と入力します。
13. 5 番目の単位、**サービス工程** をクリックして、右クリックします。 **レポート単位の挿入を選択します**。
14. ステップ 11 を繰り返します。
15. 列 B および列 C に **操作** と入力します。
16. 12 番目の単位をクリックし、**アウトレット** をクリックし、右クリックします。 **レポート単位の挿入** を選択します。
17. ステップ 11 を繰り返します。
18. 列 B および列 C に **小売** と入力します。現在のロールアップの単位と同じレベルで、マーケティング、工程、小売単位が表示されていることに注意してください。 新しい単位が、次に組織されます。 レポート単位は右クリックすると表示されるオプションの昇格および降格を使用するか、またはドラッグ アンド ドロップを使用して組織します。
19. 3 つめの単位 **取引の表示** が有効なことを確認し、右クリックします。
20. **レポート単位の降格** を選択します。 単位が **販売** の子として今回は表示されていることに注意します。
21. 単位 4、**販売キャンペーン** をクリックして、右クリックします。
22. **レポート単位の降格** を選択します。
23. グラフィカル表示で、**サービス工程** をクリックします。 マウスの左ボタンをクリックし押しながら、**工程** まで単位をドラッグします。 マウスの左クリックを離し、単位を工程のロールアップにドロップします。 **生産**、**品質管理**、**物流**、**調達** および **管理** についても同じ手順を繰り返します。
24. 降格またはドラッグ アンド ドロップを使用して **小売** の子の、**アウトレット**、**スーパー**、**モール**、**オンライン** を作成します。
25. 結果の再編成を保存します。 レポート ツリーが作成され組織されたので、レポート定義に追加できます。
26. **ウィンドウ** メニューで、**損益計算書 - 既定** を選択し、レポート定義を開きます。
27. **ツリー タイプ** ドロップダウン矢印をクリックし、**レポート ツリー** を選択します 。
28. ツリーのドロップダウン矢印をクリックし、**区分別原価部門** を選択します。
29. 基準年を **2021** に変更し、変更を **保存** し、レポートを **生成** します。 レポートが完了し開くと、レポートを活用できます。
30. **レポート ツリー** ドロップダウンを選択し、レポート単位を表示します。 または、レポート ツリーのすべての単位の残高を表示するために、レポートの行をドリルダウンすることもできます。
31. **損益計算書 - 既定** を閉じます。
32. **レポート デザイナー** を閉じます。

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>練習 4: 組織階層を使用する連結レポートの作成
この練習では、既存の既定のレポートを変更します。 レポート定義で組織階層を追加し、連結損益計算書と貸借対照表を生成します。 更新が完了したら、連結レポートを生成し、レポート ツリーを使用して、レポートを活用します。 財務レポートの一覧から開始します。

1. 総勘定元帳の **照会およびレポート** の下の **財務レポート** に移動します。
2. **貸借対照表と損益計算書の並行表示 – 既定** という名前のレポート行を選択します。
3. **編集** を選択します。 **貸借対照表と損益計算書の並行表示 – 既定** が、レポート デザイナーで開きます。
4. **ファイル** &gt; **名前を付けて保存** を選択し、**貸借対照表と損益計算書の並行表示** レポートの名前を付けます。
5. 基準年を 2021 に変更します。
6. ツリー タイプのドロップダウン矢印をクリックし、**組織階層** を選択します。
7. ツリーのドロップダウン矢印をクリックし、**Contoso Holdings** を選択します。
8. 変更を保存し、レポートを生成します。 求められた場合は、すべてのレポート単位を選択します。 レポートが完了し開くと、レポートを活用できます。
9. **レポート オプション** を選択します。
10. **分析コード フィルターの追加** を選択して、**部門** を選択します。
11. フィールドに **022** と入力し、 **OK** を選択します。
12. フィルター処理されたレポートを閉じます。
13. **レポート ツリー** ドロップダウンを選択し、レポート単位を表示します。 または、レポート ツリーのすべての単位の残高を表示するために、レポートの行をドリルダウンすることもできます。
14. **連結貸借対照表と損益計算書の並行表示** を閉じます。
15. **レポート デザイナー** を閉じます。

## <a name="exercise-5-create-a-side-by-side-departmental-report"></a>練習 5: 部門別平行レポートの作成
この練習では、新しいレポートを作成します。 このレポートは、並行部門の損益計算書です。 既存の行定義を使用しますが、新しいレポート定義および分析コード フィルタを使用する新しい列定義を作成します。 **財務諸表** の一覧から開始します。

1. 総勘定元帳の **照会およびレポート** の下の **財務レポート** に移動します。
2. **新規** を選択します。 レポート デザイナーは、空白のレポート定義を開きます。 最初のタスクは、列定義の作成です。
3. **ファイル**、**新規**、**列定義** の順にクリックして新しい列定義を作成します。
4. **列 A** で、**DESC** を列タイプとして選択します。
5. **列 B** で、**FD** を列タイプとして選択します。
6. **分析コード フィルター** フィールドをダブルクリックします。
7. **分析コード** ウィンドウで、**部門** 列をダブルクリックします。
8. ダイアログの **個々または範囲** セクションで、**ソース** フィールドの **省略記号** をクリックして、部門の一覧を表示します。
9. 部門 **022**、**販売とマーケティング** を選択し、**OK** をクリックします。
10. 部門 23 から 25 でステップ 5 から 8 を繰り返します。
11. 各 FD 列の **ヘッダー 2** 行で、次の部門の説明を入力します:

    - 列 B – 販売およびマーケティング
    - 列 C - 工程
    - 列 D - 財務
    - 列 E - IT

12. 並行部門として列定義を保存します。 既存の行定義を使用するため、レポート定義は、新しく作成された列定義および既存の行定義を使用するように変更できます。
13. **ウィンドウ** メニューで、**新しいレポート定義** を選択し、レポート定義を開きます。
14. 行定義として **損益計算書 - 既定** を選択し、列定義として **並行部門** を選択します。
15. **並行部門損益計算書** としてレポート定義を保存します。
16. 基準年を **2021** に変更します。
17. 詳細レベルを **財務、勘定および トランザクション** に変更します 。
18. 変更を **保存** して、**生成します**。 レポートが完了し開くと、レポートを活用できます。

## <a name="additional-resources"></a>追加リソース
[財務諸表](../../../finance/general-ledger/financial-reporting-getting-started.md)

[財務諸表の表示](../../../finance/general-ledger/view-financial-reports.md)

[Dynamics 365 Finance のブログ](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
