---
title: Finance and Operations へのコード移行の準備
description: このトピックでは、コード アップグレード サービスと Visual Studio ツールを使用して、Dynamics AX 2012 R3 から Finance and Operations に移行する方法について説明します。
author: RobinARH
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 25971
ms.assetid: a911b0f2-a7b0-4643-bf5b-16e55c9397be
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8521cb727c4541ecf80036ca1819654de2ac21c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743937"
---
# <a name="prepare-to-migrate-code-to-finance-and-operations"></a>Finance and Operations へのコード移行の準備

[!include [banner](../includes/banner.md)]

このトピックでは、Lifecycle Services のコード アップグレード サービスと Visual Studio ツールを使用して、コードとメタデータを Dynamics AX 2012 R3 から Finance and Operations に移行する方法について説明します。 これらの手順のほとんどは、Finance and Operations の 2 つのメジャー バージョンの間でのコードの移行にも適用されます。 

<a name="prerequisites"></a>必要条件
-------------

リモート デスクトップを使用して Finance and Operations 開発環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。 コードをアップグレードする前に、Finance and Operations の開発、カスタマイズ、およびユーザー インターフェイスの概念の幾つかをよく理解しておくことをお勧めします。 次にいくつかの参照を挙げます。

-   [開発ツール](../dev-tools/developer-home-page.md)
-   [モデルとパッケージ](../dev-tools/models.md)
-   [X++ プログラミング言語](../dev-ref/xpp-language-reference.md)
-   [拡張機能およびオーバーレイ](../extensibility/extensibility-home-page.md)
-   [ユーザー インターフェイス開発](../user-interface/user-interface-development-home-page.md)

## <a name="overview-of-the-code-migration-process"></a>コード移行プロセスの概要
### <a name="model-split"></a>分割されたモデル

Finance and Operations アプリケーションは、次のいくつかのパッケージ、またはアセンブリに分割されます。 

**プラットフォームパッケージ**

-   アプリケーション プラットフォーム
-   アプリケーション基準
-   Test Essentials

**アプリケーション パッケージ**

-   Application Suite
-   他のアプリケーション パッケージ

ISV および Dynamics AX 2012 R3 から移行された顧客コードは、正しいパッケージに再ベースラインされます。

### <a name="auto-migration-using-the-lcs-code-upgrade-service"></a>LCS コードのアップグレード サービスを使用して自動移行

LCS コードのアップグレード サービスは、Dynamics AX 2012 R3 モデル ストアを入力として受け取り、次の作業を完了します。

-   メタデータを最新の形式に変換します。
-   適切なモデルに移動およびマージすることで、メタデータのベースラインを再度設定します。
-   ソリューションのアップグレードに必要な作業を理解する見積を提供します。
-   ソリューションの一部を自動移行する移行ルールを実行します。
-   TODO を使って手動で修正する内容を開発者に知らせる移行ルールを実行します。
-   アップグレードされたソリューションを Azure DevOps プロジェクトに自動的にチェックインします。

コード アップグレード サービスを設定および実行する方法については、[[Lifecycle Services (LCS) でコード アップグレード サービスを構成および実行する](../lifecycle-services/configure-execute-code-upgrade.md)] を参照してください。

### <a name="manual-migration-steps"></a>手動での移行の手順

LCS コード アップグレード サービス構成のコードをアップグレードした後、開発者の VM と Azure DevOps にアップグレードされたコード ブランチに接続します。

-   [1 ボックス開発環境のコンフィギュレーション](../dev-tools/configure-developer-vm.md)
-   [コード移動中の Azure DevOps マッピングのコンフィギュレーション](configure-vso-solution.md)

コードのアップグレード サービスは、コードをコンパイルするために開くことができる Visual Studio ソリューションを提供します。 競合を含むすべての要素向けの **コード マージ** ソリューションと、すべてのアップグレードされた要素向けの **アップグレード** ソリューション。 通常、以下の順序でコンパイル エラーを修正して、アプリケーションをコンパイルできます。 順序はパッケージの依存関係のグラフに基づいて決定され、グラフの中で最も低いパッケージから開始されます。 パッケージの依存関係を調べるには、[モデルおよびパッケージ](../dev-tools/models.md) を参照してください。 標準的な注文は、Application Platform、Application Foundation、Directory など、Application Suite です。 各アップグレードされたモデル対象:

-   マージの競合を修正します。
-   モデルの分割 (パッケージ全体の参照) に関連するコンパイル エラーを修正します。
    -   一般的なエラー メッセージは次のとおりです。
        -   &lt;要素タイプ&gt; X は、存在しない &lt;要素タイプ&gt; Y を参照します。
        -   名前 &lt;Name&gt; はクラス、テーブル、または拡張データ型を示すものではありません。
    -   たとえば、オーバーレイされたカスタマイズは、パッケージの依存関係グラフの上位にある要素またはコードを参照している場合があります。
        -   ディレクトリ モデル内のメソッドは、アプリケーション スイート パッケージ内のテーブルを参照しています。
        -   ディレクトリ パッケージ内のフォームは、アプリケーション スイート パッケージ内のデータ ソースを参照しています。
    -   モデル要素またはビジネス ロジックを上位のパッケージに移動することによって、これらの依存関係に対応するようにコードをリファクターする必要があります。
    -   [コードの移行中にデリゲートを使用してモデル間の依存関係を解決する](delegates-migration.md) は、これらの問題を解決する方法について説明します。
-   コンパイル エラーを修正します。

すべてのコンパイル エラーを解決した後は、すべてのパッケージがコンパイルされます。 次に、次のタスクを完了する必要があります。

1.  ガイド付きコード アップグレード TODO とコード アップグレード固有のベスト プラクティス警告に対処します。 いくつかの例と詳細を以下のセクションに示します。
2.  たとえば、ActiveX や代替の検索など、非推奨のコントロールを置き換えます。
3.  すべてのフォームにフォーム パターンとサブ パターンを適用します。
4.  すべてのシナリオが、カスタム パターンに対して異なるサイズで、複数のブラウザーで動作することを検証します。
5.  記述してテストを実行します。

## <a name="best-practice-setup"></a>ベスト プラクティスの設定
ベスト プラクティス フレームワークには、移行を完了するために解決する必要があるベスト プラクティス警告のサブセットがあります。 これは、Dynamics AX 2012 R3 またはそれ以前から移行する場合に適用されます。

1.  Visual Studio で、**Dynamics 365 &gt; オプション &gt; ベスト プラクティス** をクリックします。
2.  **モデル** ドロップダウン メニューで、**アプリケーション スイート** を選択します (作業しているすべてのモデルで繰り返します)

これらのルールは、ソリューションの移行中に「オン」に設定する必要があります。 この設定は、AxRuleSet フォルダー内の XML ファイルによって実行されます。 たとえば、C:\\Packages\\ApplicationSuite\\Foundation\\AxRuleSet の下にある、アプリケーション スイート xml ファイル、BPRules.xml を参照してください。 

[![bpupgraderules](./media/bpupgraderules.png)](./media/bpupgraderules.png) 

移行を完了するには、すべての移行固有のベスト プラクティス ルールを修正する必要があります。 エラーは警告としてエラー リストに表示されます。 エラー一覧には、コンパイラの警告やベスト プラクティスのエラーが表示されます。 ベスト プラクティスのエラーには接頭語として **BP** のテキストが付けられます。 たとえば、**BPErrorFormControlPatternUnspecified**。

## <a name="debugging"></a>デバッグ
既定では、Finance and Operations は作業中のファイルのデバッグ環境を最適化します。 結果として、プロジェクトに含まれていないファイル (F11) にステップ インすると、 PDB が読み込まれず、コードをデバッグできなくなります。 この問題を回避するには、<strong>Dynamics 365 **&gt;**オプション</strong>&gt;<strong>デバッグ</strong> をクリックしてプロジェクトのデバッグ設定を変更します。 <strong>ソリューション内の項目に対してのみシンボルを読み込む</strong> チェックボックスが選択されていないことを確認します。 このオプションは、デバッガの速度を大幅に向上させるため、既定で選択されています。 Intellitrace をオフにしたい場合、別のデバッグ設定をします。 Intellitrace はアプリケーションの完全な実行履歴を収集します。 デバッグ時に IDE で多くのノイズが作成されます。 Intellitrace をオフにするには、<strong>オプション</strong>&gt;<strong>IntelliTrace</strong>&gt;<strong>IntelliTrace を有効にする</strong> をクリックしてチェック ボックスをオフにし、<strong>OK</strong> をクリックします。 Intellitrace は Visual Studio の Enterprise 版でのみ使用できることに注意してください。  

## <a name="address-code-migration-tasks"></a>アドレス コード移行タスク
メタデータを Finance and Operations に移行するとき、複数の自動アップグレード スクリプトが実行されます。 開発者が手動で移行タスクを完了する必要がある場合、行う内容とベスト プラクティス (BP) が追加されました。

-   TO DO には `/* TODO: (Code Upgrade)` の接頭語が付いており、コード移行の一部として修正する必要があります。
-   BP 移行固有のルールはコード移行の一環として修正される必要があります。

以下のこの例では、**PurchCommitment\_PSN** フォームを使用して、ナビゲーションを修正する移行タスクについて説明します。 具体的には、重複するボタンおよびアクション ウィンドウ TODO などの例が表示されます。

### <a name="setup"></a>セットアップ

1.  Visual Studio で、**アプリケーション エクスプローラー** を開き、フォーム PurchCommitment\_PSN を検索します。
2.  **OK** をクリックします。
3.  プロジェクトを右クリックし、**プロパティ** を選択します。
4.  モデル プロパティで **アプリケーション スイート** を選択します。
5.  会社プロパティで、FRSI を選択します。
6.  注記: このフォームは、フランスのデモ データ会社 FRSI に配置されます。
7.  **Ctrl+F5** キーを押してフォームを表示します。

フォームは完成しているように見えますが、移行を完了するために必要なコード移行タスクがあります。 

[![i](./media/i1.png)](./media/i1.png)

### <a name="navigation-migration-tasks"></a>ナビゲーション移行タスク

1.  Visual Studio で、プロジェクトをビルドし、ツール バーで **表示** &gt; **タスク一覧** をクリックします。
2.  **コメント** ドロップダウン リストをクリックして、TO DO: (コード アップグレード) タスクを表示します。
3.  一覧で、ActionPane TODO を検索します。

[![j](./media/j1.png)](./media/j1.png)

### <a name="code-upgrade-rule---action-pane"></a>コード アップグレード ルール - アクション ウィンドウ

Finance and Operations では、次の主要なアクションはシステム定義ボタンとして提供されます。

-   新規
-   消去
-   編集
-   輸出

自動移行の一環として、アクション ペイン ルールは冗長ボタンを識別するために実行されます。 この移行の部分を完了するには、手動で行う必要があります。

-   コードを削除するか移動します。
-   アプリケーション コード内の冗長なコントロールを削除します。

> [!NOTE]
> 以下のセクションでは、システム定義ボタンを複製するモデル化されたボタンのコードを移行および変更する方法の例を示します。 ただし、実際には、この記事で行われたのと同様の変更を加える前に、シナリオに関してコードをまず評価して、それがまだ必要かどうかを決定する必要があります。 最初に、システム定義の削除ボタンと重複する、DeleteCmdButton に対する TODO を修正します。

1.  Visual Studio では、次に示す TODO を検索して、TODO をダブルクリックします。

    [![k](./media/k1.png)](./media/k1.png)

2.  以下に示すように、TODO とコード行を置き換えます。
    -   システム定義の **削除** ボタンの状態は、firstmaster データソースの AllowDelete プロパティによって制御されます。 AllowDelete を false に設定することにより、キーボード ショートカットが使用されている場合に削除タスクは実行されません。

        ```xpp
        // Delete button
        /* TODO: (Code Upgrade) [Action Pane Rule] Please consider moving all references to the form task override method and remove the control: DeleteCmdButton */
        deleteCmdButton.enabled(purchCommitmentHeader && purchCommitmentHeader.canDelete());
        PurchCommitmentHeader_DS.allowDelete(purchCommitmentHeader && purchCommitmentHeader.canDelete());
        ```

3.  エディターで、DeleteCmdButton を探してフォーム デザインから削除します。 

    [![l](./media/l1.png)](./media/l1.png)

4.  **Ctrl+S** キーを押してフォームを保存します。
    -   次に、システム編集ボタンと重複する EditCmdButton に焦点を当てて、このボタンに関連付けられた 2 つの "仕事" の処理とこのボタンの削除を行います。

5.  Visual Studio では、次に示す TODO を検索して、TODO をダブルクリックします。

    [![m](./media/m1.png)](./media/m1.png)

6.  **編集** ボタンの表示はフォームの表示/編集モードで制御されるため、このコードを変更してプロパティを設定する必要があります。 次の図に示すように、TODO とコード行を置き換えます。

    ```xpp
    /* TODO: (Code Upgrade) [Action Pane Rule] Please consider moving all references to the form task override method and remove the control: EditCmdButton */
    editCmdButton.enabled(purchCommitmentHeader && isInDraftOrUnderRevisionStatus && !isInWorkFlowReviewState && !isLineReferenced);

    if(purchCommitmentHeader && isInDraftOrUnderRevisionStatus && !isInWorkFlowReviewState && !isLineReferenced)
    {
        element.design().ViewEditMode(ViewEditMode::Auto);
    }
    else
    {
        element.design().ViewEditMode(ViewEditMode::View);

    }
    ```

7.  このボタンのその他の TODO をダブルクリックします。

    [![n](./media/n1.png)](./media/n1.png)

8.  モデル化された **編集** ボタンでコードを検査します。 このロジックは、フォームの task() メソッドに移動する必要があります。

    ```xpp
    [Control("CommandButton")]
    class EditCmdButton
    {
        /* TODO: (Code Upgrade) [Action Pane Rule] Please consider moving this button code to the task override method and remove the control EditCmdButton. */
        void clicked()
        {
            if (purchCommitmentHeader.WorkflowApprovalState ==     
                PurchCommitmentWorkflowApprovalState_PSN::Approved)
            {
                if (Box::yesNo(strFmt("@SPS2140", purchCommitmentHeader.CommitmentNumber), 
                    DialogButton::No) == DialogButton::Yes)
                {
                    super();

                    PurchCommitmentHeader_PSN::setWorkflowState(purchCommitmentHeader.RecId, 
                        PurchCommitmentWorkflowApprovalState_PSN::NotSubmitted);
                }
            }
            else
            {
                super();
            }
        }
    }
    ```

9.  Visual Studio デザイナーの左側で、**メソッド** &gt; **上書き** を右クリックし、**タスク** を選択して、フォームのタスク メソッドの上書きを追加します。
10. システム定義の **編集** ボタンをクリックしたときに上記のコードがトリガーされるように、以下に示すようにタスク メソッドを更新します。

    ```xpp
    /// 
        ///
        /// 
        /// 
        /// 
        public int task(int _taskId)
        {
            #Task
            int ret;

            switch (_taskId)
            {
                case #taskEditRecord:

                    if (purchCommitmentHeader.WorkflowApprovalState == PurchCommitmentWorkflowApprovalState_PSN::Approved)
                    {
                        if (Box::yesNo(strFmt("@SPS2140", purchCommitmentHeader.CommitmentNumber), DialogButton::No) == DialogButton::Yes)
                        {
                            ret = super(_taskId);

                            PurchCommitmentHeader_PSN::setWorkflowState(purchCommitmentHeader.RecId, PurchCommitmentWorkflowApprovalState_PSN::NotSubmitted);
                        }
                    }
                    else
                    {
                        ret = super(_taskId);
                    }

                    break;

                default:
                    ret = super(_taskId);
                    break;
            }

            return ret;
        }
    ```

11. エディターで、**EditCmdButton** を探してフォーム デザインから削除します。 

    [![o](./media/o1.png)](./media/o1.png)

12. **Ctrl+S** キーを押してフォームを保存します。
13. **Ctrl+F5** キーを押してフォームを表示します。 **確約** タブの **削除** および **編集** ボタンが削除されたことを確認します。

## <a name="resolve-casting-exceptions"></a>キャスト例外を解決
Finance and Operations では、X++ は完全に中間言語 (IL) ベースであるため、解釈された Dynamics AX 2012 よりも厳密なランタイム タイプ動作を行います。 この厳しいランタイム タイプの動作により、移行された Dynamics AX 2012 R3 メタデータの例外を生成できます。 移行中にこれらの例外が発生することがあります。 キャスト例外は、ダウンキャスト、タイム オブジェクトを設計するためのキャスト ランタイム、サイド キャストなど、さまざまな実行時シナリオで発生させることができます。 以下のセクションで、フォーム CosJournalName が実行時にコントロールを生成し、強い型付けのために .NET 例外を発生させる型の不一致がある例について説明します。

### <a name="example-side-casting-exception"></a>例: サイドキャストの例外

1.  Visual Studio で、**プロジェクト プロパティ** を選択して右クリックし、USMF が既定の会社であることを確認します。
2.  表示メニュー項目に CosJournalName を追加し、スタートアップ オブジェクトとしてメニュー項目を設定します。
3.  プロジェクトに CosJournalName フォームを追加します。
4.  プロジェクトに cosDimCheckBoxController クラスを追加します。
5.  プロジェクトのリビルドします。
6.  **Ctrl+F5** キーを押してフォームを実行します。
7.  フォームを実行するときに、次のような例外が発生することに注意してください。

    [![u](./media/u1.png)](./media/u1.png)

8.  cosDimCheckBoxController クラスを右クリックし、**コードの表示** を選択します。
9.  cosDimCheckBoxController::getBuildControl() にブレークポイントを設定します。
10. **F5** キーを押します。
    -   ブレークポイントをヒットします。 これがキャスティング エラーが発生する場所です。 キャスト エラーの理由は、型のコントロールを返そうとしているためです。FormBuildCheckboxControl とオブジェクトは FormBuildStringControl を想定しています。

11. buildcontrol をポイントしてタイプを表示し、相違点に注目します。

    [![v](./media/v1.png)](./media/v1.png)

12. **F10** キーを押して例外をヒットします。

    [![w](./media/w2.png)](./media/w2.png)

13. デバッグを停止します。
14. 例外を修正するには、メソッド宣言を FormBuildStringControl から FormBuildCheckBoxControl に変更します。

    ```xpp
    protected FormBuildStringControl getBuildControl()
    protected FormBuildCheckBoxControl getBuildControl()
    ```
    
15. プロジェクトをリビルドして、**Ctrl+F5** を押します。 キャスト エラーが解決されたため、フォームが正常に開きます。

    [![a](./media/a-1024x576.png)](./media/a.png)

## <a name="migrating-context-menus-and-mouse-double-click-code"></a>コンテキスト メニューとマウス ダブルクリック コードの移行
コンテキスト メニューとマウスのダブルクリック アクションを処理する Dynamics AX 2012 コードを移行するには、このトピックを参照してください。

-   [コードの移行 - コンテキスト メニュー コード](code-migration-context-menus.md)
-   [コードの移行 - マウス ダブルクリック ロジック](code-migration-double-click.md)






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]