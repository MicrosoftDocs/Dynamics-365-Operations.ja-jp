---
title: アプリケーション スイート レポート データ セットを展開する
description: この記事では、レポート データ プロバイダー (RDP) クラスで X++ ビジネス ロジックを使用して作成された既存のレポート データ セットを拡張する方法について説明します。
author: RichdiMSFT
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.custom: 266594
ms.assetid: 7810ee2c-e012-4a0f-992c-840e626bf437
ms.openlocfilehash: 7d7d663de0ae0e5d57e213f7ace6d4d4cec6b0cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280079"
---
# <a name="expand-application-suite-report-data-sets"></a>アプリケーション スイート レポート データ セットを展開する

[!include [banner](../includes/banner.md)]

この記事では、レポート データ プロバイダー (RDP) クラスで X++ ビジネス ロジックを使用して作成された既存のレポート データ セットを拡張する方法について説明します。

この記事では、レポート データ プロバイダー (RDP) クラスで X++ ビジネス ロジックを使用して作成された既存のレポート データ セットの拡張について説明します。 カスタムのデリゲート ハンドラーおよびテーブル拡張機能を使用して、追加のフィールド データと計算の両方またはいずれかを含めます。 アプリケーション スイートを重層化する必要はありません。 次に、標準のアプリケーション ソリューションを置き換えてデータをユーザーに提供する、カスタムのデザインを作成します。 次の図は、この記事で説明されている一般的なアプリケーションのカスタマイズを示しています。

[![extendingdatasets。](./media/extendingdatasets.png)](./media/extendingdatasets.png)

## <a name="whats-important-to-know"></a>知っている必要がある重要なこと
このソリューションを適用する前に知っておくべき基本的な前提がいくつかあります。

- **RDP クラスを直接拡張することはできません。** ただし、プラットフォームは、標準のアプリケーションのビジネス ロジックを複製せずにデータ セットの拡張を有効にする拡張ポイントを提供します。
- **レポート データ セットを展開するために使用できる 2 つの方法があります。** ソリューションに適した戦略を使用します。

    - **データ処理ポストハンドラー** - このメソッドは、**ProcessReport** メソッドが完了して、データ セットがレポート サーバーに返される前に、1 回だけ呼び出されます。 このポスト ハンドラーを登録し、標準アプリケーション ソリューションによって生成される一時的なデータ セットに対して一括更新を実行します。
    - **イベントを挿入する一時テーブル** – このメソッドは、一時テーブルに追加される各行に対して呼び出されます。 これは計算およびインラインの評価により適しています。 ジョイン操作やルックアップ操作が多い負担のかかるクエリは避けてください。

- **イベントハンドラーを使用して、メニュー項目を新しいレポート デザインにリダイレクトします。** イベント ハンドラーを使用して、アプリケーション レポート ソリューションのすべての側面をカスタマイズすることができます。 コントローラー クラスの **PostHandler** イベントを追加して、ユーザー ナビゲーションをカスタム レポート デザインに再ルーティングします。

## <a name="expand-a-report-data-set"></a>レポート データ セットを展開
次のチュートリアルでは、「純粋な」拡張機能ベースのソリューションを使用して既存のアプリケーション データ セットを拡張するプロセスについて説明します。 このソリューションには、Fleet Management アプリケーション用のカスタム **レンタル リスト** レポートが含まれています。 新しいレポートには、レンタルの詳細に追加のレンタル料金データが含まれています。 アプリケーションのカスタマイズ内容は、拡張モデルで定義されます。 次の図は、標準デザインとカスタム ソリューションを示しています。

### <a name="before-standard-design"></a>(標準デザイン) の前に

[![標準デザイン (カスタマイズ前)。](./media/fleet-extension-rentals-list-before-1024x673.png)](./media/fleet-extension-rentals-list-before.png)

### <a name="after-custom-solution"></a>変更後 (カスタム ソリューション)

[![カスタム ソリューション (カスタマイズ後)。](./media/fleet-extension-rentals-list-after-1024x672.png)](./media/fleet-extension-rentals-list-after.png)

1. **アプリケーション カスタマイズの新しいモデルを作成します。** 拡張モデルに関する詳細については、 [拡張機能およびオーバーレイによるカスタマイズ](../extensibility/customization-overlayering-extensions.md) を参照してください。 この例では、**フリート管理拡張** モデルにカスタム レポートを追加します。
2. **Microsoft Visual Studio で、新しいプロジェクトを作成します。** プロジェクトが拡張モデルに関連付けられていることを確認します。 次の図はプロジェクト設定を示します。

    [![Visual Studio でのプロジェクト設定。](./media/fleet-extension-vs-project-settings.png)](./media/fleet-extension-vs-project-settings.png)

3. **カスタム レポート データを格納するテーブル拡張機能を追加します。** RDP クラスによって設定される **TmpFMRentalsByCust** データ セットの一時的キャッシュを検索し、モデルで拡張を作成します。 レポート サーバーのデータの格納に使用するフィールドを定義し、**保存** をクリックして変更を保存します。 次の図は、この例で必要なテーブル拡張機能を示しています。

    [![この例の拡張テーブル。](./media/fleet-extension-table-extension.png)](./media/fleet-extension-table-extension.png)

4. **プロジェクトに、カスタム レポートを追加します。** カスタム デザインは、標準的なソリューションによく似ています。 したがって、**フリート管理拡張** モデルで既存のアプリケーション レポートを複製してから、レンタル料金コンテナーにカスタム タイトルと追加テキスト ボックスが含まれるようにレポート デザインを更新することができます。
5. **レポートの名前を変更して、わかりやすい名前にします。** この例では、カスタム レポートの **FERentalsByCustomer** の名前を変更し、標準のソリューションと区別します。
6. **レポート データ セットの参照を復元します。** レポート デザイナーを開いて、**データセット** コレクションを展開し、**FMRentalsByCustDS** と名付けられたデータ セットを右クリックし、それから **復元** をクリックします。 データ セットは、新しく導入された列を含むように拡張されます。 したがって、これらの列は、レポート デザイナーで使用できるようになりました。
7. **レポート デザインのカスタマイズ** デザイナーは、カスタム ソリューションを作成するために使用できる自由形式のデザイン サーフェスを提供します。 次の図は、この例で使用されるカスタム デザインを示しています。

    [![この例のカスタム デザイン。](./media/fleet-extension-custom-design.png)](./media/fleet-extension-custom-design.png)

8. **新しいレポート ハンドラー (X++) クラスをプロジェクトに追加します。** クラスに、それが既存のアプリケーション レポートのハンドラーであることを適切に表す名前を付けます。 この例では、クラスの **FERentalsByCustomerHandler** の名前を変更し、他のレポート ハンドラーと区別します。
9. **PostHandler メソッドを追加して、カスタム レポートの使用を開始します。** この例では、次のコードを使用して標準ソリューション **FMRentalsByCustController** のコントローラー クラスを展開します。

    ```xpp
    class FERentalsByCustomerHandler
    {
        [PostHandlerFor(classStr(FMRentalsByCustController), staticMethodStr(FMRentalsByCustController, construct))]
        public static void ReportNamePostHandler(XppPrePostArgs arguments)
        {
            FMRentalsByCustController controller = arguments.getReturnValue();
            controller.parmReportName(ssrsreportstr(FERentalsByCustomer, Report));
        }
    }
    ```

    アプリケーションのユーザー ナビゲーションは、カスタム レポート ソリューションに再ルーティングされるようになります。 レポート サーバーにカスタム レポートを配置し、アプリケーションがそれを使用していることを確認するには少し時間がかかります。 この時点では、ステップ 3 で導入したカスタム フィールドを作成するために使用されるビジネス ロジックを追加する必要があります。 次の手順では、ソリューションに該当するデータ セット拡張のメソッドを選択する必要があります。

10. **X++ ビジネス ロジックを追加して、カスタム フィールド データを設定します。** ソリューションを必要とする変換のタイプに適したデータの処理方法を選択します。

    - **オプション 1: データ処理ポストハンドラーを追加します。** 標準ソリューションの結果セットに対して 1 つのパスを使用する一括挿入操作にはこの手法を適用します。 テーブル ルックアップを使用してデータ セットを展開するコードを次に示します。

        ```xpp
        class FERentalsByCustomerHandler
        {
            [PostHandlerFor(classStr(FMRentalsByCustDP), methodstr(FMRentalsByCustDP, processReport))]
            public static void TmpTablePostHandler(XppPrePostArgs arguments)
            {
                FMRentalsByCustDP dpInstance = arguments.getThis() as FMRentalsByCustDP;
                TmpFMRentalsByCust tmpTable = dpInstance.getTmpFMRentalsByCust();
                FMRentalCharge chargeTable;
                ttsbegin;
                while select forUpdate tmpTable
                {
                    select * from chargeTable where chargeTable.RentalId == tmpTable.RentalId;
                    tmpTable.ChargeDesc = chargeTable.Description;
                    tmpTable.update();
                }
                ttscommit;
            }
        }
        ```

    - **オプション 2: イベントを挿入する一時テーブルを追加します。** この手法を行ごとの計算に適用します。 テーブル ルックアップを使用してデータ セットを展開するコードを次に示します。

        ```xpp
        class FERentalsByCustomerHandler
        {
            [DataEventHandlerAttribute(tableStr(TmpFMRentalsByCust), DataEventType::Inserting)]
            public static void TmpFMRentalsByCustInsertEvent(Common c, DataEventArgs e)
            {
                TmpFMRentalsByCust tempTable = c;
                FMRentalCharge chargeTable;
                // update the value of the 'ChargeDesc' column during 'insert' operation
                select * from chargeTable where chargeTable.RentalId == tempTable.RentalId
                && chargeTable.ChargeType == tempTable.ChargeType;
                tempTable.ChargeDesc = chargeTable.Description;
            }
        }
        ```

これで、レポート データ セットの拡張が完了しました。 アプリケーションをコンパイルした後、拡張モデルで定義されているレポート クラス ハンドラーで定義したカスタム X++ ビジネス ロジックを使用して、新しいレポート デザインにユーザー ナビゲーションを再ルーティングし始めます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
