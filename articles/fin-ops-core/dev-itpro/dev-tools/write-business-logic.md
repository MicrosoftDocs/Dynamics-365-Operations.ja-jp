---
title: C# および X++ ソース コードを使用したビジネス ロジックを記述する
description: このチュートリアルでは、C# と X++ 間での相互運用性について説明します。 このチュートリアルでは、C# ソース コードおよび X++ ソース コードでビジネス ロジックを記述します。
author: pvillads
ms.date: 02/07/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26821
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f479e13d3921c63c6140c91d51cc329fe1894f70
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360336"
---
# <a name="write-business-logic-by-using-c-and-x-source-code"></a>C# および X++ ソース コードを使用したビジネス ロジックを記述する

[!include [banner](../includes/banner.md)]

このチュートリアルの主な目的は、 C# と X++ 間で相互運用性について説明することです。 このチュートリアルでは、C# ソース コードおよび X++ ソース コードでビジネス ロジックを記述します。 

このチュートリアルでは、C\# ソース コードおよび X++ ソース コードでビジネス ロジックを記述します。 以下の経験が得られます。

-   Visual Studio の新しいツール。
-   C\# でのイベント処理です。
-   C\# の言語統合クエリ (LINQ) を使用してデータをフェッチする。

## <a name="prerequisite"></a>前提条件
このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。 

> [!NOTE]
> **ソリューション内の項目のシンボルの読み込み** チェック ボックスがオンになっている場合、C\# プロジェクトのデバッグ サポートは機能しません。 このオプションが既定で選択されているため、演習を実行する前に変更する必要があります。 Visual Studio で、 **Dynamics 365** &gt; **オプション** をクリックし、 **ソリューション内の項目に対してのみシンボルを読み込む** チェック ボックスをオフにします。

## <a name="scenario"></a>シナリオ
危険な運転習慣の経歴を持つ運転手に、余りにも多くの車がレンタルされています。 フリート管理レンタル会社は、外部ソースからドライブ レコードを確認する必要があります。 上級管理職は、運転免許とその関連情報を管理する法人である運輸省 (DOT) が運用するサービスに加入することに決まりました。 このサービスは、指定された一意のライセンス番号の引用数を取得します。 X++ ソース コードから直接外部サービスを呼び出すことは容易ではありません。 Visual Studio にはサービスを呼び出す「コードビハインド」を (C\# で) 生成するツールがあり、これらのツールにより開発作業が簡単になります。 Visual Studio を活用してコードを記述することが当然の選択です。 ただし、このチュートリアルでは物流が簡単なラボ環境の範囲を超えているため、コードは実際に外部サービスを呼び出しません。 代わりに、サービス コールのモック実装を提供します。 このチュートリアルの目標は、C\# の現在の状態と X++ との相互運用性の理解について教えることです。

## <a name="create-a-c-class-library"></a>C\# クラス ライブラリの作成
プロジェクトから、 C\# クラス ライブラリ、またはアセンブリを生成する C\# プロジェクトの別のタイプへの参照を作成できます。 このような参照は、ビルド順序に影響します。 C\# プロジェクトは、それを参照して依存するプロジェクトより前にビルドされます。 インフラストラクチャは参照を理解し、 C\# アセンブリが実行前にクラウドに正しく配置されるようにします。 フリート管理ソリューションで C\# クラス ライブラリを作成するには、これらの手順に従います。

1.  Visual Studio で、**ファイル** &gt; **プロジェクト/ソリューションを開く** をクリックします。
2.  **プロジェクトを開く** ダイアログ ボックスの **ファイル名** テキスト ボックスに次のパスを入力してから **Enter** キーを押します - *C:\\users\\public\\desktop\\FleetManagement*。
3.  FleetManagement.sln というファイルを選択し、**開く** をクリックします。 ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。

    [![OpenProject\_LinqC.](./media/openproject_linqc2.png)](./media/openproject_linqc2.png)

4.  **FleetManagement** ソリューションを右クリックし、**追加** &gt; **新しいプロジェクト** をクリックします。 **新しいプロジェクトの追加** ダイアログ ボックスが表示されます。
5.  左ウィンドウで、**Visual C\#** をクリックしてから、中央ウィンドウで **クラス ライブラリ** をクリックします。
6.  **名前** テキスト ボックスの下部に **DriversLicenseEvaluator** という名前を入力します。
7.  **場所** テキスト ボックスに、*C:\\users\\public\\desktop\\FleetManagement* というディレクトリ パスを入力します。
8.  上部にあるドロップダウン リストで、プロジェクトが ".NET Framework 4.5" に設定されていることを確認します。
9.  プロジェクトを作成するには、**OK** をクリックします。 

    [![AddNewProject\_LinqC.](./media/addnewproject_linqc2.png)](./media/addnewproject_linqc2.png)

10. **ソリューション エクスプローラー** の DriversLicenseEvaluator プロジェクトで、ファイル名 Class1.cs を右クリックして DriversLicenseChecker.cs に名前を変更します。
11. クラスへのすべての参照の名前を変更するか、確認するメッセージが表示されたら、**はい** をクリックします。 

    [![RenameClass\_LinqC.](./media/renameclass_linqc1.png)](./media/renameclass_linqc1.png)

## <a name="write-a-c-method-named-checkdriverslicense"></a>CheckDriversLicense という名前で C\# メソッドを記述
このセクションでは、CheckDriversLicense という名前のメソッドの C\# コードを追加します。 このメソッドでは、運転免許証を検証する必要があります。 これを行うには、メソッドは顧客テーブルに格納されている運転免許証番号を取得する必要があります。 このメソッドには、メソッドで必要な情報が含まれている顧客レコードの RecId値が与えられます。 C\# コードは、 LINQ プロバイダーを使用して、顧客テーブルから読み取ります。 LINQ が作動するためには、最初に LINQ アセンブリを指定している参照を追加する必要があります。 これらの参照を DriversLicenseEvaluator という名前の C\# プロジェクトに追加します。

1.  **ソリューション エクスプローラー** で、DriversLicenseEvaluator プロジェクト ノードを展開し、**参照** を右クリックしてから **参照の追加** をクリックします。
2.  **参照** をクリックし、次のパスを入力します: C:\\Packages\\bin

    注: 一部の環境では、パッケージ フォルダーの場所が c: ドライブ上に存在していません。

3.  **ファイル名** フィールドに、パターン \*LINQ\*.dll を入力してから **Enter** を押します。 LINQ という名前が入っている、アセンブリの一覧が表示されます。 その一覧から、次のファイルを選択し、**追加** をクリックします。
    -   Microsoft.Dynamics.AX.Framework.Linq.Data.dll
    -   Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
    -   Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll

    [![SelectReferences\_LinqC.](./media/selectreferences_linqc1.png)](./media/selectreferences_linqc1.png)
    
4.  以下のコードで使用する共通タイプを含むサポート アセンブリも追加する必要があります。 **参照** をもう一度クリックし、フィールドに次のファイル名を入力します。
    -   Microsoft.Dynamics.AX.Xpp.Support.dll
    -   Microsoft.Dynamics.AX.Data.Core.dll

5.  **追加** をクリックし、**OK** をクリックします。 アセンブリが、プロジェクトの参照ノードの下に表示されます。
6.  **参照の追加** プロセスを繰り返します。ただし、今回は以下の DLL ファイルを指定されたパスから追加します。
    -   C:\\Packages\\FleetManagement\\bin 内の Dynamics.Ax.FleetManagement.dll

7.  **ソリューション エクスプローラー** で、Dynamics.Ax.FleetManagement.dll の参照を選択し、プロパティ **Copy Local = False** に設定します。
8.  **ソリューション エクスプローラー** で、**DriversLicenseChecker.cs** を右クリックしてから、**コードの表示** をクリックします。
9.  **DriversLicenseEvaluator** 名前空間に、次の使用する 3 つのステートメントを追加し、外部クラスを参照するコードの冗長性を減らします。 Dynamics.AX.Application の使用。Microsoft.Dynamics.AX.Framework.Linq.Data の使用。Microsoft.Dynamics.AX.Xpp の使用。ユーザーの C\# コードは以下の例のように見えるはずです。

    ```csharp
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace DriversLicenseEvaluator
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.AX.Framework.Linq.Data;
        using Microsoft.Dynamics.Ax.Xpp;

        public class DriversLicenseChecker
        {
        }
    }
    ```

10. クラス CheckDriversLicense を次のコードに置き換えます。 

    > [!TIP] 
    > C:\\FMLab ディレクトリ内の DriversLicenseChecker.cs ファイルからコードに貼り付けることもできます。

    ```csharp
    public class DriversLicenseChecker
    {
        public static bool CheckDriversLicense(long customerId)
        {
            // Use LINQ to get back to the information about the license number
            FMCustomer customer;
            QueryProvider provider = new AXQueryProvider(null);
            var customers = new QueryCollection<FMCustomer>(provider);

            // Build the query (but do not execute it)
            var query = from c in customers 
                where c.RecId == customerId 
                select c;

            // Execute the query:
            customer = query.FirstOrDefault();
            if (customer == null)
            {
                throw new ArgumentException
                    ("The customerId does not designate a customer");
            }

            if (string.IsNullOrEmpty(customer.DriverLicense))
            {
                // No driver's license was recorded. Veto the rental.
                return false;
            }

            // Call the DOT web service to validate the license number.
            // This is not practical for this lab, because all the service providers
            // charge for this service. Instead, just assume that any license number
            // that contains the sequence "89" is valid.
            // In the demo data, this is true for Adrian Lannin,
            // but not for Phil Spencer.
            return customer.DriverLicense.Contains("89");
        }
    }
    ```

### <a name="understand-the-linq-code"></a>LINQ コードを理解する

さらに C\# コードに進む前に、追加した LINQ コードを理解していることを確認してください。 LINQ の詳細については、[技術概念ガイド](developer-home-page.md)で説明されているため、以下では基本のみを説明します。

-   最初に、*プロバイダー* を作成します。 すべてのテーブルへのアクセスを提供します。
-   次に、すべての顧客の *コレクション* が作成されます。 利息のある顧客はこのコレクションから取得されます。
-   次に、**RecId** によって要求された顧客を指定する where 句で *クエリ* が作成されます。
-   FirstOrDefault メソッドを呼び出すと、クエリが強制的に実行されます。
-   このメソッドは、一致する単一の顧客を顧客変数に割り当てます。 (RecId 値が顧客と一致しない場合は、Null が割り当てられます。)
-   最後に、関連付けられている運転免許証が有効かどうかを確認するため、顧客データをテストします。 (ライセンスに「89」は含まれていますか。)

## <a name="handle-the-event-when-a-record-is-added"></a>レコードが追加されると、イベントが処理されます。
次のサブセクションでは、次の項目について説明します。

-   次のコード品目および総合関係について説明します。
-   イベント ハンドラーのコードを表示します。
-   ハンドラーをイベントの発生に関連付けます。

### <a name="preparatory-overview"></a>準備の概要

テーブルにレコードを追加しようとすると、そのレコードがデータベースに書き込まれる前に、OnValidateWrite イベントが発生します。 FMRental テーブルに対して OnValidateWrite イベントが発生するたびに、CheckDriversLicense メソッドが呼び出されることを必要とします。 これを行うには、イベントによって呼び出され、checkDriversLicense メソッドを呼び出す C\# メソッドを記述する必要があります。 つまり、CheckDriversLicense メソッドを呼び出すイベント ハンドラーを記述する必要があります。 イベント ハンドラー メソッドは、型のパラメーター、DataEventArgsを受け取ります。 イベント ハンドラーは、レコードを承認または拒否するかを DataEventArgs 構造の値に設定できます。 イベント ハンドラー メソッドを書き込んだ後は、イベントに割り当てて接続するか、または FMRental テーブルのメンバーである OnValidatedWrite をデリゲートして追加します。 FMRental フォームのデータ ソースの init メソッドにこの割り当てを記述します。 デリゲートへのこの割り当ては奇妙に思える場合があります。 結局のところ、既存のコード (FMRental) を変更して、ハンドラーを追加します。これはイベントが提供する予定の疎結合の主な価値提案と矛盾しています。 この割り当てステップは一時的です。 最終的に、X++ の場合と同じストーリーが C\# でも発生します。属性は、デリゲートとハンドアラーを結合するメカニズムとして、C\# イベント ハンドラーに適用されます。 

> [!NOTE]
> データ ソース init メソッドは、フォームを開いたときに呼び出されます。 技術的には、init メソッドは FormDataSource クラスから継承されます。

### <a name="write-an-event-handler-method"></a>イベント ハンドラー メソッドの記述

C\# では、次のイベント ハンドラー メソッドを記述して DriversLicenseChecker クラスに追加します。

```csharp
public static void OnValidatedWriteHandler(Common table, DataEventArgs args)
{
    var validateEventArgs = args as ValidateEventArgs;

    // Do not check if already rejected.
    if (validateEventArgs.parmValidateResult())
    {
        var rentalTable = table as FMRental;
        if (rentalTable == null)
        {
            throw new ArgumentNullException("table");
        }

        var result = CheckDriversLicense(rentalTable.Customer);
        validateEventArgs.parmValidateResult(result);
    }
}
```

プロジェクト ノードを右クリックしてから **ビルド** をクリックし、DriversLicenseEvaluator プロジェクトをビルドします。

### <a name="add-a-reference-pointing-to-the-driverslicenseevaluator-project"></a>DriversLIcenseEvaluator プロジェクトを指定する参照の追加

次の手順を実行し、**移行されたフリート管理** という名前の X++ プロジェクトから **DriversLicenseEvaluator** という名前の C\# プロジェクトへの参照を作成します。

1.  FleetManagement Migrated プロジェクトを右クリックし、**追加** をクリックして **参照** をクリックします。 **プロジェクト** 参照タブで DriversLicenseEvaluator プロジェクトの行を選択し、**OK** をクリックします。 

    ![AddReference\_LinqC.](./media/addreference_linqc1.png)

2.  FleetManagement Migrated プロジェクトで、**References** ノードを展開すると、**DriversLicenseEvaluator** プロジェクトへの新しい参照が表示されます。

    ![SolutionExplorerReferences\_LinqC.](./media/solutionexplorerreferences_linqc2.png)

#### <a name="build-sequence"></a>ビルド順序

C\# DriversLicenseEvaluator プロジェクトは、 FleetManagement Migrated プロジェクトのビルド前にビルドされます。 これは、追加された参照によって、フリート プロジェクトがプロジェクトに依存するためです。 ビルド シーケンスを簡単に確認するには、FleetManagement ソリューションを右クリックし、 **プロジェクト ビルド順序** をクリックして、 **相互関係** をクリックします。

![ProjectDependencies1\_LinqC.](./media/projectdependencies1_linqc2.png)

![ProjectDependencies2\_LinqC.](./media/projectdependencies2_linqc1.png)

### <a name="add-your-event-handler-to-a-delegate"></a>委任へのイベント ハンドラーの追加

1.  **ソリューション エクスプローラー** で、**移行された FleetManagement &gt; ユーザー インターフェイス &gt; フォーム &gt; FMRental** に進みます。
2.  **FMRental** フォームをダブルクリックします。 Visual Studio デザイナーは、このフォームを開きます。
3.  フォームで使われるデータ ソースを表示するには、**データ ソース** ノードを展開します。
4.  **FMRental** データ ソースおよび **メソッド** ノードを展開し、データ ソースで定義されたメソッドを一覧表示します。
5.  **メソッド** を右クリックし、**オーバーライド &gt; メソッド** をクリックします。 リストには、まだ上書きされていないデータ ソース上のすべてのメソッドが表示されます。 **init** を選択すると、**FMRental.xpp** ファイルが X++ コード エディタ内に開き、カーソルが init メソッドのテンプレートの近くに表示されます。
6.  **初期化** メソッド本体の最後に、+= 演算子を使用してデリゲートに 1 つの割り当てを追加します。

    ```xpp
    FMRental.onValidatedWrite += eventhandler
        (DriversLicenseEvaluator.DriversLicenseChecker::OnValidatedWriteHandler);
    ```

7.  クリックして保存し、ソリューション全体を構築します。

## <a name="final-test"></a>最終テスト
このセクションでは、ブレークポイントを設定し、Visual Studio デバッガーでフリート アプリケーションを実行します。 これにより、次のことを証明できます。

-   LINQ クエリは、OnValidateWrite イベントが発生したときに実行されます。
-   LINQ クエリが、顧客のデータの取得に成功します。

### <a name="prepare-the-test"></a>テストの準備

1.  **ソリューション エクスプローラー** で、**移行された FleetManagement &gt; ユーザー インターフェイス &gt; フォーム** に進みます。
2.  **FMRental** を右クリックし、**スタートアップ オブジェクトとして設定** をクリックします。
3.  DriversLicenseChecker.cs のコード エディターで、OnValidateWriteHandler メソッドを検索します。 次のコード行を検索します。

    ```csharp
    var result = CheckDriversLicense(rentalTable.Customer);
    ```
    
4.  このコード行にブレークポイントを設定します。 その線の左余白をクリックすると、これが行なわれます。 ブレークポイントが設定されている場合は、赤いドットが表示されます。
5.  CheckDriversLicense メソッドでは、次の行で別のブレークポイントを設定します。

    ```csharp
    if (string.IsNullOrEmpty(customer.DriverLicense))
    ```
### <a name="run-the-test"></a>テストの実行

このテストでは、書き込んだ C\# コードをデバッグします。 これを行うには、Visual Studio に C\# コードを含むアセンブリのシンボルを読み込むように通知する必要があります。 **Dynamics 365 &gt; オプション &gt; デバッグ** の順に移動し、 **ソリューション内の項目に対してのみシンボルを読み込む** チェック ボックスが選択されていないことを確認します。 

![Options\_LinqC.](./media/options_linqc2.png)

> [!TIP] 
> C\# コードでブレークポイントに到達できない場合、**モジュール** ウィンドウ (**デバッグ&gt;ウィンドウ&gt;モジュール**) で開けて、C\# モジュールを検索し、明示的に読み込みます。

1.  **デバッグ &gt; デバッグを開始** とクリックします。 これにより、フリート アプリケーションが開始され、**FMRental** フォームのブラウザー ウィンドウが表示されます。
2.  **車両レンタル ID** をクリックすると詳細が表示されます。
3.  フォームの左上隅にある **編集** アイコンをクリックします。 アイコンは鉛筆のように見えます。
4.  **レンタル** セクションの **終了** フィールドで、1 日ごとに日付を増加させます。
5.  **保存** ボタンをクリックします。 これにより、強調表示されたブレークポイントで Visual Studio にフォーカスが移動します。 この行は、OnValidatedWrite イベントが発生し、ハンドラー メソッド が呼び出されたことを示しています。
6.  **F5** キーを押して実行を続行します。 すぐに、その他のブレークポイントが強調表示されます。
7.  ブレークポイントの数行上で、変数の顧客を検索します。
8.  顧客変数を右クリックし、**QuickWatch** をクリックします。 長整数値は、LINQ クエリが機能していることを証明します。 

    ![QuickWatch\_LinqC.](./media/quickwatch_linqc2.png)

9.  **F5** キーを押して **保存** 操作を完了します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]