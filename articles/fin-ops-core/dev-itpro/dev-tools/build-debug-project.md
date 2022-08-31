---
title: プロジェクトのビルドおよびデバッグ
description: このチュートリアルでは、フリート管理アプリを使用して、ブレークポイントの設定方法、コードの変更方法、および結果の構築方法を示します。
author: pvillads
ms.date: 02/06/2019
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 26731
ms.assetid: 5c2378fe-cb34-4a81-a940-57d4e13eb282
ms.openlocfilehash: a40d13f6c108aef9a44312a6d48c5f906f991740
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271227"
---
# <a name="build-and-debug-projects"></a>プロジェクトのビルドおよびデバッグ

[!include [banner](../includes/banner.md)]

このチュートリアルでは、フリート管理アプリケーションでコードを分析してデバッグするために Visual Studio でのツールの使用について確認します。 ブレークポイントを設定し、あるコードを変更し、その結果を構築する、単純な開発者のシナリオを検討します。 

## <a name="prerequisites"></a>必要条件

コードおよび Visual Studio の以前の経験は、このチュートリアルを完全に活用するのに役立ちます。 このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。

## <a name="key-concepts"></a>重要な概念

-   Visual Studio のデバッガーは、プロジェクトのコードの分析とデバッグに使用されます。
-   Visual Studio デバッガーの標準機能は、実行中のアプリケーションを調べているときに使用することができます。 これらの機能には、変数の値の変更、ブレークポイントの設定などが含まれます。
-   IntelliSense および Visual Studio の他の機能は、効率的なコード編集および理解に不可欠です。
-   開発は反復的なプロセスです。 コードを変更すると、プロジェクトが作成され、変更をテストできます。

## <a name="scenario"></a>シナリオ

レンタル会社は、顧客が有効期限を過ぎているクレジット カードを使用して車を借りているときに、不幸な出来事に見舞われました。 開発者は、この状況の阻止を支援するために、アプリケーションを修正する責任を負います。 Visual Studio のデバッガーを使用して、問題を特定します。 問題識別された後は、修正を実装するためにいくつかのコードを編集します。 最後に、プロジェクトを構築し、修正プログラムが成功したことを検証します。

## <a name="run-to-a-breakpoint"></a>ブレークポイントまで実行

1.  デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。
2.  FleetManagement ソリューションを開きます。 **ファイル** メニューで、**開く** をポイントし、**プロジェクト/ソリューション** をクリックします。
3.  デスクトップを参照し、次に **FleetManagement** フォルダーを開きます。 ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。
4.  **FleetManagement** という名前のファイルを選択します。 表示されるファイル タイプは SLN ファイルです。
5.  **開く** をクリックします。 ソリューションの読み込みには時間がかかる場合があります。
6.  **FleetManagement** プロジェクトをスタートアップ プロジェクトにします。 **ソリューション エクスプローラー** で、**フリート管理** プロジェクトを右クリックして、コンテキスト メニューで **スタートアップ プロジェクトとして設定** を選択します。
7.  **ソリューション エクスプローラー** で、**フリート管理** プロジェクトをダブルクリックして内容を表示します。
8.  フリート管理プロジェクトの **クラス** フォルダーをダブルクリックします。 **FMRentalCheckoutProcessor** クラスを検索します。 このクラスを右クリックしてから、**開く** をクリックします。 または、ソリューション エクスプローラー ウィンドウの上部にあるソリューション エクスプローラーの検索バーを使用できます。 検索バーに名前を入力すると、ソリューション エクスプローラーで選択された対応するコンポーネントが表示されます。 クラスで X++ コードを表示できるようになりました。 このクラスには **FinalizeRentalCheckout** という名前のメソッドがあります。
9.  最初のコメントの次の行にあるこのメソッドにブレークポイントを配置します。 これを行うには、デバッガで実行を一時停止するコード行の左側の余白をクリックします。 また、コード行の任意の場所をクリックして、F9 を押すことができます。 次の図はブレークポイントを示しています。ブレークポイントは余白に赤で塗りつぶされた円として表示されます。 

    [![FMRentalCheckoutProcessor のブレークポイント。](./media/redcirclemargin_builddebugproj.png)](./media/redcirclemargin_builddebugproj.png) 

    FinalizeRentalCheckout メソッドは、レンタル トランザクションが保存されるときに呼び出されます。 このメソッドは、RentalTransactionAboutTobeFinalizedEvent という名前のデリゲートを呼び出します。 このデリゲートで呼び出される、イベント ハンドラー メソッドを実装することができます。 デリゲートを呼び出すメソッドは、RentalConfirmation という名前のパラメーターを渡します。このパラメーターには、レンタルを許可するかブロックするかを示す値が含まれています。 レンタルが許可されている場合、値に true が含まれ、ブロックされている場合は、値に false が含まれます。 イベント ハンドラーは、開発者がコード内で実装するために選択するテストに基づいてこの値を変更できます。 この場合、クレジット カードの有効期限をテストするコードを変更します。
10. F5 を押してアプリケーションをデバッグのために起動するか、**デバッグ** メニューで **デバッグ開始** をクリックします。 これらの方法のいずれかでアプリケーションを開始することが重要です。 しない場合は、Visual Studio デバッガーは起動されないため、設定されたブレークポイントのいずれかはヒットされません。 **注記**: デバッガーは、コードの位置をソースの位置に関連付ける必要があります。 アセンブリおよび net モジュールに沿って生成された PDB ファイルの消費を通じて実行されます。 デバッガーは、グローバル ツール設定の設定に示すように、PDBファイルから記号を読み込みます。 読み込むシンボルを制御する設定を含むオプション ページを開くには、**ツール** メニューで **オプション** を選択します。 **Microsoft Dynamics 365 Finance** グループで、**デバッグ** ページを選択します。 このオプションが選択されている場合、システムは、現在のソリューションのコンポーネントに関連する PDB ファイルのみから記号を読み込みます。 これにより起動時間が大幅に短縮されるため、このラボでは必ずそれを選択してください。 このオプションを選択すると、現在のソリューションの外部にあるエンティティからソース コードを確認することはできません。 数分後、ブラウザーが起動し、プロジェクトで選択されたスタートアップ オブジェクトを表示します。
11. **現在のレンタル** ページが開きます。
    1.  アクション ウィンドウで、**編集** をクリックします。
    2.  ページが表示されたら、**表示/非表示** リストで **リストの表示** をクリックします (または **Ctrl+F8** を押します)。

12. 既存のレンタルに変更を加えます。 たとえば、**編集** をクリックして、レンタル期間が開始した時刻を変更します。
13. レンタル レコードを強制的に検証するには、**保存** をクリックします。 ブレークポイントを配置するメソッドが呼び出されます。 実行は、ブレークポイントを含むコード行で一時停止します。 

    [![ブレークポイントでの実行の一時停止。](./media/forcevalidation_builddebugproj.png)](./media/forcevalidation_builddebugproj.png) 
    
    アプリケーションがブレークポイントで一時停止している間に、アプリケーションの状態を調べることができます。 通常 Visual Studio で開発するアプリケーションと同じ方法を使用します。 たとえば、ツールヒントでその値を表示する変数またはパラメーターにカーソルを置きます。 
    
    [![一時停止中のブレークポイントのヒント。](./media/tooltip_builddebugproj.png)](./media/tooltip_builddebugproj.png)

14. Visual Studio の他のデバッグ ツールも利用することができます。 たとえば、**ローカル** ウィンドウは、実行が停止した場所のすべてのローカル変数を表示します。 Visual Studio の下部にある **ローカル** タブをクリックし、**fmrentalrecord** 変数を展開します。 レコード内のすべてのフィールドの値を示す、レコードの内部状態が表示されます。 

    [![ローカル ウィンドウ。](./media/internalstate_builddebugproj.png)](./media/internalstate_builddebugproj.png) 
    
    **fmrentalrecord** 変数の **車両** プロパティの値に注目してください。 このプロパティは、**FMRental** テーブルの外部キー フィールドです。 デバッガーを使用すると、FMVehicle テーブルの関連するレコードを調べることができます。 **AutoIdentification** フィールド グループに属する値を示します。
15. **ブレークポイント** ウィンドウには、設定されているすべてのブレークポイントが一覧表示されます。 **ブレークポイント** タブをクリックし、コンテンツを表示します。 

    [![ブレークポイント ウィンドウ。](./media/breakpoint_builddebugproj.png)](./media/breakpoint_builddebugproj.png)

16. F10 キーを数回押してコードを 1 行ずつ実行し、デバッガー機能の完全な補完を使用します。 **ローカル** ウィンドウが、実行される各ステートメントですぐに変数の値を更新することに注意します。
17. ツール バーで、**続行** をクリックするか、F5 を押します。
18. Internet Explorer を閉じ、**Fleet Management** アプリケーションを閉じます。 Visual Studio はデバッグ モードを終了します。 代替は **デバッグの停止** を **デバッグ** メニューから選択します。 これにより、Internet Explorer は開いたままになり、次のデバッグ セッションをより早く開始することができます。

## <a name="add-the-validation-code"></a>検証コードの追加

**FinalizeRentalCheckout** メソッドでは、開発者がコードを追加してレンタルの有効性を決定するために使用されるデリゲートを呼び出したことを確認します。 期限切れのクレジット カードの問題を解決するには、クレジット カードが期限切れではないことを確認するために使用するイベント ハンドラーを追加します。 ラボを簡素化するために、ハンドラはデリゲートを含む同じファイルに追加されます。 インスピレーションとして、次のコードを使用します。 コードをコピーして貼り付けるのではなく、手動で入力して IntelliSense 機能の動作を参照してください。 これらの機能により、Visual Studio ユーザーは高い生産性を期待することができます。

```xpp
[SubscribesTo(classstr(FMRentalCheckoutProcessor), 
    delegatestr(FMRentalCheckoutProcessor, RentalTransactionAboutTobeFinalizedEvent))]
public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct rentalConfirmation)
{
    FMPaymentInformation paymentInfo;
    date ccExpiryDate, lastDayOfExpiryMonth;
    str s;

    select firstonly * from paymentInfo where paymentinfo.RecId == rentalRecord.PaymentInformationId;

    if (paymentInfo)
    {
        // Check if the payment info is valid
        // For now, we will check if the credit card is expired
        // Credit cards expire on the last day of the month indicated
        ccExpiryDate = mkdate(1, str2int(paymentInfo.ExpirationMonth), paymentInfo.ExpirationYear);
        lastDayOfExpiryMonth = endmth(ccExpiryDate);

        if (lastDayOfExpiryMonth < today())
        {
            rentalConfirmation.value('OktoRent', false);
            s = "Credit card validation failed for rental ";
        }
        else
        {
            s = "Credit card validation succeeded for rental ";
        }

        info (s + rentalrecord.RentalId);
    }
    else
    {
        rentalConfirmation.value('OktoRent', false);
        info ("No Credit card available for " + rentalrecord.RentalId);
    }
}
```

上記のコードはわかりやすいです。 このメソッドは、**SubscribesTo** 属性を使用して、関連するデリゲートのハンドラーとしてマークされています (図参照) コードでは、顧客レコードが取得されてから、クレジット カードの日付が今日の日付と比較されます。 クレジット カードの有効期限が過ぎている場合は、**RentalConfirmation** 構造でイベント ハンドラーの値を設定し、顧客が車両の貸し出しの対象ではないことを通知します。 これは、任意の数のハンドラーがデリゲートにサブスクライブできるようにするためです。 ハンドラーでレンタルを続行しないと決定した場合、**OkToRent** フラグを設定します。 優れた実装では、**OkToRent** フラグがすでに false に設定されていると判断した場合、分析を行わないことがあります。

1.  FMRentalCheckoutProcessor.xpp ファイルで作業していることを確認します。 新しいイベント ハンドラー定義を FMRentalCheckoutProcessor クラスに追加することによって開始します。 クラス定義の終了を示す波括弧 (}) のすぐ上の空の明細行に次のコードを追加します。

    ```xpp
    public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct rentalConfirmation)
    {

    }
    ```

2.  イベント ハンドラーの先頭に、属性を追加します。 これらの属性は、イベントハンドラーがどのデリゲートに加入しているかを示します。

    ```xpp
        [SubscribesTo(classstr(FMRentalCheckoutProcessor),
            delegatestr(FMRentalCheckoutProcessor, RentalTransactionAboutTobeFinalizedEvent))]
            public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct 
                                                                           RentalConfirmation)
        {

        }
    ```

3.  ここで、クレジット カードの有効期限の値を確認するコードを追加します。 完了したメソッドは、次のコードのようになります。

    ```xpp
    [SubscribesTo(classstr(FMRentalCheckoutProcessor), 
        delegatestr(FMRentalCheckoutProcessor, RentalTransactionAboutTobeFinalizedEvent))]
    public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct rentalConfirmation)
    {
        FMPaymentInformation paymentInfo;
        date ccExpiryDate, lastDayOfExpiryMonth;
        str s;

        select firstonly * from PaymentInfo where paymentinfo.RecId == rentalRecord.PaymentInformationId;

        if (paymentInfo)
        {
            // Check if the payment info is valid
            // For now we will check if the credit card is expired
            // Credit cards expire on the last day of the month indicated
            ccExpiryDate = mkdate(1, str2int(paymentInfo.ExpirationMonth), paymentInfo.ExpirationYear);
            lastDayOfExpiryMonth = endmth(ccExpiryDate);

            if (lastDayOfExpiryMonth < today())
            {
                rentalConfirmation.value('OktoRent', false);
                s = "Credit card validation failed for rental ";
            }
            else
            {
                s = "Credit card validation succeeded for rental ";
            }

            info (s + rentalrecord.RentalId);
        }
        else
        {
            rentalConfirmation.value('OktoRent', false);
            info ("No Credit card available for " + rentalrecord.RentalId);
        }
    }
    ```

4.  ハンドラーとデリゲートが 1 行の空白行で区切られていることを確認します。
5.  Visual Studio のツールバーで、**保存** をクリックします。
6.  コードに問題がなければ、フリート管理プロジェクトのコードをビルドします。 これを行うには、**ソリューション エクスプローラー** で、**FleetManagement** プロジェクト名を右クリックし、**Build** をクリックします。 コードが正しくない場合は、エラーまたは警告が表示される場合があります。 その場合は、コードを修正し、再度ビルド警告やエラーが解決されるまでビルドを続行します。 これで、リビジョンが意図したとおりに動作することを確認する準備が整いました。
7.  **デバッグ** メニューをクリックして、**すべてのブレークポイントを削除** します。
8.  次のステートメントを含む明細行にあるイベント ハンドラー メソッドに新しいブレークポイントを配置します。

    ```xpp
    if (lastDayOfExpiryMonth < today())
    ```
    
9.  F5 キーを押してデバッグをアクティブにし、フリート管理サンプルを開始します。
10. 前のセクションのステップ 11 で説明されているように **現在のレンタル** ページを参照してください。 いずれかの予約を選択し、**編集** をクリックします。
11. **顧客** ドロップダウン リストで、一覧から Adrian Lannin を選択して **保存** をクリックします。 実行は、イベントハンドラー メソッドで設定したブレークポイントで一時停止します。
12. F10 キーを 3 回押して、コード ブロックを実行します。 

    [![コードを進める。](./media/stepcodeblock_builddebugproj.png)](./media/stepcodeblock_builddebugproj.png)
    
13. F5 キーを押して続行します。 その顧客が許可されていないことが表示されます。
14. 同じレンタルで、顧客名を Phil Spencer に変更してから **更新** をクリックします。 今回は、トランザクションが可能です。
15. Internet Explorer を閉じます。
16. **RentalFinalizedEventHandler** メソッドで **SubscribesTo** をコメントにします。 このステップでは、残りのチュートリアルで作業してもクレジット カード テストが実行されなくなります。

## <a name="best-practices"></a>ベスト プラクティス

このチュートリアルの前半では、プロジェクトにコードを追加し、変更を加えてソリューションをビルドする営業案件を得ました。 ビルド プロセスが成功しなかったため、エラー ウィンドウを参照する必要があります。 このウィンドウを使用しているとき、エラーを説明する明細行をクリックすると、エラー状態になります。 コンパイル エラーを表していないいくつかの診断メッセージが通知される場合があります。 これらは、**ベスト プラクティス** チェッカーからの診断です。 このツールは、開発者が既知のベスト プラクティスに違反したインスタンスをチェックして、違反が見つかったときに警告を表示します。 ベスト プラクティス ルールは、コードの構成要素とメタデータの両方に適用されます。 各ソフトウェアの開発組織は、実施するベスト プラクティスのセットを持つ可能性が高いです。 既存のベスト プラクティス チェックの一部を無視する場合があります。 これをサポートするために、報告されたベスト プラクティスの診断セットを個々の開発者が変更することができます。 これを実証するには、次の手順を実行します。

1.  **表示** メニューで、**エラー リスト** をクリックします。 いくつかのベスト プラクティス警告が表示されます。
2.  **Dynamics 365** メニューで、**オプション** をクリックします。 **Dynamics 365** グループで、**ベスト プラクティス** を選択します。
3.  **モデル** ドロップダウン リストで、**フリート管理** モデルが選択されていることを確認します。 ベスト プラクティス ルールは、特定のモデルに適用されます。
4.  ベスト プラクティス ルールのセットの一部に対する選択内容をマークします。 たとえば、**CodeStyleRules** のエントリを選択する場合、変数のベスト プラクティスのガイドラインが検査されます。 選択を更新した後、**OK** をクリックします。
5.  プロジェクト名を右クリックして **リビルド** をクリックすることにより、フリート管理プロジェクトをリビルドします。 指定したベスト プラクティス ルールの違反が **エラー一覧** ウィンドウに表示されることがわかります。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

