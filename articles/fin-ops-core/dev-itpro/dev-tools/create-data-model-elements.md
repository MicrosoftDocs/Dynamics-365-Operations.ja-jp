---
title: モデルの作成、およびデータモデル要素の作成についての概要
description: このチュートリアルでは、Visual Studio の Dynamics 365 メニューを使用して、フリート管理チュートリアルという名前の新しいモデルを作成します。 また、新しいモデルの要素を作成および編集します。
author: RobinARH
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 23421
ms.assetid: 1b7789f4-12c1-480b-bb39-c354b5b03276
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58a07b4a35db236bbe1a90126bf1fc19a4c532e5
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983665"
---
# <a name="create-models-and-data-model-elements-overview"></a>モデルの作成、およびデータモデル要素の作成についての概要

[!include [banner](../includes/banner.md)]

このチュートリアルでは、Visual Studio の Dynamics 365 メニューを使用して、**フリート管理チュートリアル**という名前の新しいモデルを作成します。 また、新しいモデルの要素を作成および編集します。

## <a name="prerequisites"></a>必要条件

このチュートリアルでは、プロビジョニングする環境に管理者としてアクセスする必要があります。

## <a name="keywords"></a>キーワード
- **モデル** - 他の 2 つのモデルを参照するモデルをコンフィギュレーションします。 これにより、モデルは他のパッケージにあるメタデータとコード要素を参照できます。
- **プロジェクト** - プロジェクトを作成し、次に新しいモデルにプロジェクトを関連付けます。 要素をプロジェクトに追加します。これはモデルにも追加されます。 具体的には、拡張データ型 (EDT) を追加します。 また、フィールドおよびメソッドで入力するテーブルを追加します。
- **デザイナー** - プロジェクトに品目を追加するたびに、選択した品目タイプに合わせたデザイナーが表示されます。 **プロパティ** ウィンドウは、デザイナーの異なるノードが強調表示されるたびに調整されます。 デザイナーおよび **プロパティ** ウィンドウで更新を行います。
- **EDT** - 拡張データ型。

## <a name="create-the-fleet-management-tutorial-model"></a>フリート管理チュートリアル モデルを作成する
1.  **管理者として実行** を使用して Visual Studio を起動します。
2.  **Dynamics 365** ウィンドウから、**モデル管理 &gt; モデルの作成**を選択して、**モデルの作成**ウィザードを開きます。
3.  モデル パラメーターの以下の値を入力します。

    | **プロパティ**           | **値**                                                                                                                |
    |------------------------|--------------------------------------------------------------------------------------------------------------------------|
    | **モデル名**         | FleetMgmntTutorial                                                                                                       |
    | **モデル発行元**    | Microsoft Corp                                                                                                           |
    | **レイヤー**              | isv                                                                                                                      |
    | **モデルの説明**  | このチュートリアルでは、Microsoft Dynamics AX の開発ツールを使用して、フリート管理 アプリケーションを構築する方法を示します。 |
    | **モデルの表示名** | フリート管理のチュートリアル                                                                                                |

    > [!NOTE]
    > モデルの名前は **FleetMgmntTutorial** である必要があります。 他の名前は使用しないでください。 その他のチュートリアルでは、プロジェクトをインポートすることでこのモデル内のモデル要素を上書きします。 このチュートリアルで作成したモデルに **FleetMgmntTutorial** という名前が付けられていない場合、その他のチュートリアルでプロジェクトが正しくインポートできない可能性があります。
 
4.  **次へ**をクリックして次のページに移動し、次に**新しいパッケージの作成**を選択します。 作成しているモデルは独自のパッケージを持ち、独自の .NET アセンブリを構築します。 

    [![Package\_DataModel](./media/package_datamodel.png)](./media/package_datamodel.png)

5.  **次へ**をクリックし、**参照モデルを選択**ステップに進みます。
6.  参照されるモデルとして **アプリケーション プラットフォーム** および **アプリケーション基盤** を選択します。

    [![ReferenceModels\_DataModel](./media/referencemodels_datamodel.png)](./media/referencemodels_datamodel.png) 

    > [!IMPORTANT]
    > 正しい参照モデルを選択していることを確認します。
    
7.  **次へ**をクリックし、**概要**ステップに進みます。
8.  概要ページの情報を確認してから、**新規プロジェクトの作成** および **これを新規プロジェクトの自分の既定のモデルにする** チェック ボックスを選択します。 

    [![Summary\_DataModel](./media/summary_datamodel.png)](./media/summary_datamodel.png)

9.  **完了** をクリックします。 **新しいプロジェクト** ダイアログ ボックスが開きます。
10. **テンプレート**で、**Dynamics 365** を選択します。
11. **Unified Operations** テンプレートを選択します。
12. ダイアログ ボックスのフィールドに次の値を入力します。

    | **プロパティ** | **値**       |
    |--------------|-----------------|
    | **名前**     | FMTDataModel    |
    | **保管場所** | C:\\FMLab       |
    | **ソリューション** | ソリューションへの追加 |

    [![NewProject\_DataModel](./media/newproject_datamodel.png)](./media/newproject_datamodel.png)

13. プロジェクトを作成するには、**OK** をクリックします。

## <a name="create-the-fmtaddress-extended-data-type"></a>FMTAddress の拡張データ型を作成します。
1.  **ソリューション エクスプローラー**で、**FMTDataModel** を右クリックして**追加**をポイントしてから**新しい項目**をクリックします。
2.  **Dynamics 365 品目**で、**データ型**を選択します。
3.  **EDT 文字列**をクリックし、を新しい項目の種類を選択します。
4.  **名前**フィールドに、**FMTAddress** と入力してから**追加**をクリックします。 

    [![NewItem\_DataModel](./media/newitem_datamodel.png)](./media/newitem_datamodel.png) 

    これにより、新しい EDT モデル要素をプロジェクトに追加され、次の図に示すように、新しい要素の EDT デザイナーを開きます。 

    [![EDTelement\_DataModel](./media/edtelement_datamodel.png)](./media/edtelement_datamodel.png)

5.  デザイナーで **FMTAddress** ルート ノードを選択します。
6.  **プロパティ** ウィンドウの**外観セクション**で、次のプロパティを設定します。

    | **プロパティ**    | **値**          |
    |-----------------|--------------------|
    | **ヘルプ テキスト**   | オンライン ヘルプをチェックしてください。 |
    | **ラベル**       | アドレス            |
    | **文字列サイズ** | 75                 |

    [![EDTProperty\_DataModel](./media/edtproperty_datamodel.png)](./media/edtproperty_datamodel.png)

7.  **Ctrl+S** キーを押して EDT を保存します。

## <a name="add-existing-model"></a>既存のモデルの追加
現在のモデルとプロジェクトに他の必要なモデル要素ファイルを追加します。 **既存の品目を追加** フィーチャーを使用することにより、これを素早く実行することができます。

1.  **ソリューション エクスプローラー**で、**FMTDataModel** を右クリックして**追加**をポイントしてから**既存の項目**をクリックします。
2.  C:\\FMLab\\EDT\\ を参照します。 

    [![ExistingItem\_DataModel](./media/existingitem_datamodel.png)](./media/existingitem_datamodel.png)

3.  **Ctrl+A** を押してすべてのファイルを選択し、**追加** をクリックします。

## <a name="create-the-fmtcustomer-table"></a>FMTCustomer テーブルを作成します。
1. **ソリューション エクスプローラー**で、**FMTDataModel** を右クリックしてから**追加 &gt; 新しい項目**をクリックします。
2. 左ウィンドウで、**インストール済み**を展開し、**Dynamics 365 品目**を展開してから、**データ モデル**をクリックします。
3. アーティファクトの一覧で**テーブル**を選択します。
4. **名前**フィールドに、**FMTCustomer** と入力してから**追加**をクリックします。 テーブル デザイナーが開きます。 

   [![Add\_DataModel](./media/add_datamodel.png)](./media/add_datamodel.png)

### <a name="add-fields-to-the-fmtcustomer-table"></a>FMTCustomer テーブルへのフィールドの追加

FMTCustomer のテーブル デザイナーで、テーブルに複数のフィールドを追加します。 

[![AddFields\_DataModel](./media/addfields_datamodel.png)](./media/addfields_datamodel.png)

1.  各フィールドを追加するには、**フィールド** を右クリックし、**新規** をクリックして、タイプを選択します。 各フィールドを追加すると、次の表に示すように、**プロパティ** ウィンドウでフィールド名とその他の特定の値を指定する必要があります。

    | **タイプ**   | **フィールド名** | **プロパティ値**                                                         |
    |------------|----------------|-----------------------------------------------------------------------------|
    | **日付**   | CCExpiryDate   | 拡張データ型 = FMTCCExpiryDate                                        |
    | **文字列** | アドレス        | 拡張データ型 = FMTAddressHelp テキスト = アドレス フィールドのヘルプ テキスト。 |
    | **文字列** | CellPhone      | 拡張データ型 = 電話                                                  |
    | **文字列** | CreditCardNum  | 拡張データ型 = FMTCreditCardNum                                       |
    | **文字列** | DriversLicense | 拡張データ型 = FMTDriversLicense                                      |
    | **文字列** | 電子メール          | 文字列サイズ = 80Label = 電子メール                                               |
    | **文字列** | 名      | 拡張データ型 = FirstName                                              |
    | **文字列** | 姓       | 拡張データ型 = LastName                                               |
    | **文字列** | ライセンス        | 文字列サイズ = 100Label = ライセンス                                            |
    | **文字列** | 縮小版      | 文字列サイズ = 100Label = サムネイル                                          |


    > [!TIP]
    > EDT を参照するテーブル内のすべての新しいフィールドでは、**ソリューション エクスプローラー**または**アプリケーション エクスプローラー**から EDT エレメントをドラッグし、デザイナーの **FMTCustomer** テーブルの**フィールド**ノードをドロップするだけで、フィールドを作成できます。 

    [![AdministratorArrow\_DataModel](./media/administratorarrow_datamodel.png)](./media/administratorarrow_datamodel.png)

2.  **Ctrl+S** キーを押して、テーブルに新しいフィールドを保存します。

### <a name="add-fields-to-field-groups"></a>フィールド グループへのフィールドの追加

1.  次の一覧のフィールドを選択して、一部の不フィールドを **AutoSummary** フィールド グループに追加する準備をします。 複数のフィールドを選択するには、Ctrl キーを押しながら各フィールドをクリックします。
    -   **住所**
    -   **CCExpiryDate**
    -   **CellPhone**
    -   **CreditCardNum**
    -   **DriversLicense**
    -   **電子メール**
    -   **名**
    -   **姓**

2.  **フィールド グループ**ノードを展開します。
3.  選択したフィールドを **AutoSummary** ノードにドラッグします。
4.  同じ方法を使用して、**氏名**、**姓**、および**携帯**フィールドを**自動レポート**フィールド グループに追加します。
5.  テーブルを保存します。

### <a name="add-a-method"></a>メソッドの追加

1.  **Methods** ノードを右クリックし、**New Method** をクリックして、**FMTCustomer** テーブルに **fullName** という名前の X++ メソッドを 追加します。
2.  コード エディターで、既定のメソッドのコードを次のコードに置き換えます。 
 
    > [!TIP]
    > 「this.」を入力するとき、IntelliSense リストからフィールドを選択します。

```
        public display FMTName fullName()
        {
            return this.FirstName + ' ' + this.LastName;
        }
```

3.  コードを保存します。

## <a name="update-the-fmtaddress-edt"></a>FMTAddress EDT の更新
1.  **ソリューション エクスプローラー**で **FMTDataModel** プロジェクトを展開します。
2.  **FMTAddress** を右クリックしてから、**開く** をクリックします。 **EDT デザイナー**が開きます。
3.  **EDT デザイナー**で、**FMTAddress** を選択します。
4.  **プロパティ** ウィンドウの**参照テーブル** フィールドで、**FMTCustomer** を選択します。 **ヒント:** ドロップダウン リストをクリックし、検索ボックスに、接頭語「FMT」を入力します。 これにより、名前に「FMT」が含まれている表のみが表示されるように、ドロップダウン リストがフィルター処理されます。 フィルター処理されたエントリの一覧から **FMTCustomer** テーブルを選択します。 [![SearchFMT\_DataModel](./media/searchfmt_datamodel.png)](./media/searchfmt_datamodel.png)
5.  EDT を保存します。

## <a name="build-the-fmtdatamodel-project-and-the-fleet-management-tutorial-model"></a>FMTDataModel プロジェクトと フリート管理チュートリアル モデルの構築
1. **ソリューション エクスプローラー**で、**FMTDataModel** を右クリックしてから**リビルド**をクリックします。
2. モデル全体の完全なビルドを行うには、**Dynamics 365** メニューで、**モデルをビルド**をクリックします。
3. **フリート管理チュートリアル**以外のすべてのモデルのチェック ボックスをオフにします。
4. **オプション**タブで、**推奨チェックの実行**チェック ボックスを選択します。 使用可能なその他のオプションに注意してください。
5. **モデル**タブで、**ビルド**をクリックします。
6. ダイアログ ボックスで **閉じる**をクリックします。
7. **ウィンドウ**メニューで、**すべてのドキュメントを閉じる**をクリックして、開いているすべてのドキュメントを閉じます。




