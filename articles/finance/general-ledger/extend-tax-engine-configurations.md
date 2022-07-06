---
title: 税エンジン コンフィギュレーションの拡張
description: この記事では、税エンジンのコンフィギュレーションの拡張について説明します。
author: kailiang
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable
audience: IT Pro
ms.reviewer: kfend
ms.search.region: India
ms.author: kailiang
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 6e72c5e728ba9d352963db1680636e6f20756064
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865757"
---
# <a name="extend-tax-engine-configurations"></a>税エンジン コンフィギュレーションの拡張 

[!include [banner](../includes/banner.md)]

[税エンジン](tax-engine.md) (GTE とも呼ばれます) では、法的要件および業務要件に基づいて、税の適用、計算、転記、および決済を決定する税ルールを設定できます。 この記事では、インドに適用される次のシナリオを使用して、税エンジン コンフィギュレーション拡張プロセスについて説明します。

-   連邦直轄領商品およびサービス税 (UTGST) の税エンジンのコンフィギュレーションを拡張します。
-   参照モデルを使用すると、さまざまな国/地域からの商品輸入の注文の税率の基本的な関税 (BCD) を適用できます。

> [!NOTE]
> 税エンジン機能は、インドに基本住所がある法人に対してのみ使用可能です。

次の税用語がこの記事で使用されます。

|税用語 | 姓名|
|-----|-----------|
|GST | 商品およびサービス税|
|UTGST | 連邦直轄領商品及びサービス税|
|CGST | 中央商品及びサービス税|
|IGST | 統合商品及びサービス税 |
|BCD| 基本関税|

## <a name="prerequisites"></a>必要条件
シナリオ例の作成に取りかかる前に、次の作業を完了させてください。 [税エンジン インポート コンフィギュレーション](tax-engine-import-configuration.md)

### <a name="add-a-configuration-provider-and-make-it-the-active-provider"></a>コンフィギュレーション プロバイダーを追加し、アクティブなプロバイダーとする。
1. **組織管理** > **ワークスペース** > **電子申告** の順に移動します。
2. **コンフィギュレーション プロバイダー** をクリックします。
3. 新しいコンフィギュレーション プロバイダーを作成し、ページを閉じます。
4. 作成したコンフィギュレーション プロバイダーで、**...** > **有効な設定** をクリックします。

![有効なソリューション。](media/gte-extension-active-solution.png)

## <a name="scenario-1-extend-the-tax-engine-configuration-for-utgst"></a>シナリオ 1 : UTGST 用税コンフィギュレーションを拡張する

議会を持たない連邦直轄領のため、GST 評議会は SGST に相当する、UTGST を導入しました。 インドの次の連邦直轄領に UTGST が適用されます。

-   Chandigarh
-   Lakshadweep
-   Daman および Diu
-   Dadra および Nagar Haveli
-   Andaman および Nicobar Islands

SGST は、独自の議会を持ち、販売税プロセスにおいて「州」と見なされるニューデリーや Puducherry などの連邦直轄領にも適用できます。

UTGSTでは、任意の取引で税金の次の組み合わせを適用することができます。

-   州内での商品やサービス (イントラスタット) の供給: CGST + SGST
-   連邦直轄領内での商品やサービスの供給 (イントラ -UT) : CGST + UTGST
-   州または連邦直轄領にまたがる商品やサービスの供給 (イントラスタット/イントラ -UT) : IGST

UTGST のインプット タックス クレジット の使用率の順序は、SGST の インプット タックス クレジットの場合と同じです。 そのため、SGST または UTGST のインプット タックス クレジットは、ず SGST または UTGST、に対してそれぞれ設定されます。 出力税負債、および、残高は IGST 出力税負債に対して設定できます。

このシナリオでは、次の作業を完了する必要があります:
1. [拡張コンフィギュレーションを作成します](#create-extension-configurations)  
2. [課税対象のドキュメントを拡張して、IntraStateInUnionTerritory フラグを含むようにします](#extend-the-taxable-document-so-that-it-includes-the-intrastateinunionterritory-flag)
3. [拡張された課税対象のドキュメントのデータ マッピングを完了します](#complete-data-mapping-for-the-extended-taxable-document)
4. [税 (インド販売税 Contoso) のデータ モデルを変更します。](#change-the-data-model-of-tax-india-gst-contoso)
5. [州販売税 (SGST) の適用条件を変更します](#change-the-applicability-of-sgst)
6. [UTGST タスク コンポーネントを構成します](#configure-the-utgst-tax-component)
7. [UTGST を含めるための明細行の式を変更します](#modify-the-formulas-of-lines-to-include-utgst)
8. [税に関する文書のコンフィギュレーションを完了します](#complete-the-tax-document-configuration)
9. [拡張されたコンフィギュレーションをインポートし、特定の会社に配置します](#import-the-configuration-and-deploy-it-to-a-specific-company) 


### <a name="create-extension-configurations"></a>拡張機能のコンフィギュレーションの作成
拡張機能のコンフィギュレーションを作成するには、次の手順が必要です。
-   課税対象のドキュメント (インド) から派生した新しい課税対象ドキュメントを作成します。
-   課税対象のドキュメント (インド販売税) から派生した新しい課税対象ドキュメントを作成します。

1. **ローカライズ コンフィギュレーション** ワークスペース (**組織管理** > **ワークスペース** > **電子申告**)、をクリックして **税のコンフィギュレーション**。
2. ツリーで、**課税対象のドキュメント (インド)** コンフィギュレーションを見つけ、**コンフィギュレーションの作成** をクリックします。
3. **課税対象のドキュメント モデルから派生** オプションを選択し、名前と、派生課税対象ドキュメントの説明を入力します。 たとえば、**課税対象のドキュメント (インド Contoso)** と名前を入力します。
4. **コンフィギュレーションの作成** をクリックします。
5. ツリーで、**税 (インド販売税)** コンフィギュレーションを選択し、**コンフィギュレーションの作成** をクリックします。
6. **税コンフィギュレーションから派生** オプションを選択し、名前と、派生課税対象ドキュメントの説明を入力します。 たとえば、**税 (インドContoso)** と名前を入力します。
7. **コンフィギュレーションの作成** をクリックします。

### <a name="extend-the-taxable-document-so-that-it-includes-the-intrastateinunionterritory-flag"></a>課税対象のドキュメントを拡張して、IntraStateInUnionTerritory フラグを含むようにします。

**IntraStateInUnionTerritory** フラグを **課税対象のドキュメント (インド Contoso)** に追加するため、次の手順を完了します。

 1. ツリーで、[拡張機能コンフィギュレーションの作成](#create-extension-configurations)で作成した **課税対象のドキュメント (インド Contoso)** コンフィギュレーションを見つけ、**デザイナー** をクリックします。
 2. ツリーで、**課税対象のドキュメント** > **ヘッダー** > **明細行** と移動し、**新規** をクリックして新しいノードを作成します。
 3. ノードの名前を入力し、アイテムの種類を選択します。
    -   **名前:** IntraStateInUnionTerritory
    -   **アイテムの種類:** Enum

    ![新しいノードの作成。](media/gte-create-node-tax-document.png)

 4. **追加** をクリックします。
 5. **ノード** クイック タブで、**項目参照を切り替える** をクリックします。
 6. ツリーで **NoYes** を選択し、**OK** をクリックします。
 7. コンフィギュレーションを保存し、デザイナーを閉じます。
 8. ツリーで選択されている **課税対象のドキュメント (インド Contoso)** で、**バージョン** リストにある **ステータスを変更** > **完了** をクリックします。

    ![コンフィギュレーション状態の更新。](media/gte-change-configuration-status.png)

 9. **UTGST** のように説明を入力し、**OK** をクリックします。
 10. エラーがある場合は、デザイナーを開き、**検証** をクリックし、エラーを修正します。
 11. ステータスが **完了** に更新されると、コンフィギュレーションを配置できる状態です。

### <a name="complete-data-mapping-for-the-extended-taxable-document"></a>拡張された課税対象ドキュメントのデータ マッピングを完了します。
発注書または販売注文、および課税対象のドキュメントでの参照モードなどの各課税対象ドキュメントのデータ マッピングがあります。 データ マッピングの目的は、課税対象取引から取得した値を GTE に渡し、税の適用または税の計算に使用することです。 利便性のために、**課税対象ドキュメント ソース** と呼ばれ、課税金額、HSN、SAC などの最も一般的な税に関連するフィールドをカプセル化する特別なデータ ソースがあります。 したがって、拡張課税対象ドキュメントに追加のフィールドの値を取得し、マップするための2つの方法があります。

-   方法 1 : 既存の課税対象ドキュメントのソースで追加のフィールドを有効にします。
-   方法 2 : 電子レポート (ER) データ マッピングを使用します。

#### <a name="method-1-data-mapping-by-taxable-document-source"></a>方法 1 : 課税対象ドキュメントのソースによるデータ マッピング
この方法を使用する前に、[税エンジンの統合](tax-engine-integration.md)を必ず読み、基になる概念を理解するようにします。 税エンジンでは、州か連邦直轄領かを識別する必要があります。 したがってこの方法は、データ プロバイダーを変更し、税エンジンにこの情報を提供するようにします。

1. 州マスターの連邦直轄領の名前を検索します。
    1. **組織管理** > **グローバル アドレス帳** > **アドレス** > **アドレスの設定** の順に移動します。 
    2. **連邦直轄領** 列を右クリックし、**フォーム情報** > **フォーム名: LogisticsAddressSetup** をクリックします。 たとえば、列のシステムの名前が **LogisticsAddressState.UnionTerritory_IN** であることを確認します。

    ![連邦直轄領の GTE 拡張機能。](media/gte-extension-union-territory-form-info.png)

2. 連邦直轄領内のイントラスタット取引の税エンジン モデル フィールドを追加します。

    モデル アプリケーション スイートの新しいプロジェクトを作成し、新しいクラスである TaxableDocRowDPExtLineSubscriberSample を追加します。 取引が連邦直轄領内のイントラスタット取引かどうかを判断し、フラグを GTE に渡すための以下のロジックを実装します。
   
    ```xpp   
    public class TaxableDocRowDPExtLineSubscriberSample
    {
        public static const str IsIntraStateInUnionTerritory = 'IntraStateInUnionTerritory';

        [SubscribesTo(classStr(TaxableDocRowDataProviderExtensionLine),               delegateStr(TaxableDocRowDataProviderExtensionLine, initExtensionFieldsForLine))]
        public static void initExtensionFieldsForLine(TaxableDocumentValidFields _validFields)
        {
        _validFields.add(IsIntraStateInUnionTerritory, Types::Enum, enumNum(NoYes));
        }

        [SubscribesTo(classStr(TaxableDocRowDataProviderExtensionLine), delegateStr(TaxableDocRowDataProviderExtensionLine, fillInExtensionFieldsForLine))]
        public static void fillInExtensionFieldsForLine(TaxableDocumentLineObject _lineObj)
        {
        _lineObj.setFieldValue(IsIntraStateInUnionTerritory, TaxableDocRowDPExtLineSubscriberSample::IsIntraStateWithUnionTerritory(_lineObj), enumNum(NoYes));
        }

        private static NoYes IsIntraStateWithUnionTerritory(TaxableDocumentLineObject _lineObj)
        {
        boolean                     isIntraStateWithUnionTerritory = NoYes::No;
        LogisticsPostalAddress      partyAddress;
        LogisticsPostalAddress      taxAddress;
        LogisticsAddressState       partyState;
        SalesPurchJournalLine       documentLineMap;                TaxModelTaxable_IN          taxModelTaxable;
        documentLineMap = SalesPurchJournalLine::findRecId(_lineObj.getTransactionLineTableId(), _lineObj.getTransactionLineRecordId());
        taxModelTaxable = TaxModelDocLineFactory_IN::newTaxModelDocLine(documentLineMap);
        partyAddress = taxModelTaxable.getPartyLogisticsPostalAddress();
        taxAddress = taxModelTaxable.getTaxLogisticsPostalAddressTable();
        if (partyAddress && taxAddress
            && partyAddress.CountryRegionId == taxAddress.CountryRegionId
            && partyAddress.State != ''
            && taxAddress.State != ''
            && partyAddress.State == taxAddress.State)
        {
            partyState = LogisticsAddressState::find(partyAddress.CountryRegionId, partyAddress.State);
                isIntraStateWithUnionTerritory = partyState.UnionTerritory_IN;
        }
        return isIntraStateWithUnionTerritory;
        }

    }
    ```

3. デザイナーでのデータ連結を実行します。
   1. **課税対象ドキュメント (インド Contoso)** コンフィギュレーションに移動し、**デザイナー** をクリックします。

      ![税コンフィギュレーション デザイナー。](media/gte-extension-tax-configuration-designer.png)

   2. **データ ソースへのマップ モデル** をクリックします。
   3. 発注書または販売注文など、それぞれの課税対象ドキュメントと参照モデルのためのたくさんのデータ マッピングがあります。 ビジネスの要求に応じて、データ マッピングを行う必要があります。 例:
      1. 販売注文明細行を選択します。
      2. **デザイナー** をクリックします。

         ![データ マッピング。](media/gte-extension-data-mapping.png)

   4. 1 ~ 5 の手順を実行した後、データ ソースの、**販売注文** > **ヘッダー** > **明細行** の下に、**IntraStateInUnionTerritory** を見つけることができます。 このフィールドを、課税対象のドキュメントの **IntraStateInUnionTerritory:Enumeration** 値に連結することができます。

      ![データ バインディング。](media/gte-extension-data-binding.png)

   5. コンフィギュレーションを保存し、デザイナーを閉じます。
   6. **コンフィギュレーション** ワークスペースで、**ステータスを変更** > **完了** をクリックします。

      ![コンフィギュレーション状態の変更。](media/gte-change-configuration-status.png)

   7. **UTGST** のように説明を入力し、**OK** をクリックします。
   8. エラーがある場合は、デザイナーを開き、**検証** をクリックし、エラーを修正します。

#### <a name="method-2-data-mapping-using-the-er-model-mapping-designer"></a>方法 2 : ER モデル マッピング デザイナーを使用してデータ マッピングします。
この方法を使用する前に、ER およびテーブルの関係、クラス、および発注書に関するメソッドに精通するようにしてください。 
1. 発注書に対してモデル マッピング デザイナーを開き、**PurchLine** をルート データ ソースとしてテーブル レコードに追加します。

   ![Purchline 拡張機能。](media/gte-extension-purchline.png)

2. Data model\Enumeration **YesNo Global** および Dynamics 365 for Operations \Enumeration **NoYes** を追加します。

   ![列挙型の追加。](media/gte-extension-add-enumerations.png)

3. **データ ソース** ツリーで、**発注書** > **明細行** の下に計算済フィールドとして **$PurchLine** を追加し、既存の課税対象ドキュメントである **発注書** と **PurchLine** テーブル レコードの関係を構築します。 **式の編集** をクリックします。

   ![式の編集。](media/gte-extension-edit-formula.png)

4. **PurchLine** および **発注書** 間の関係を記述する式を入力します: 

   ```FIRST(FILTER(PurchLine, PurchLine.RecId='purchase order'.Header.Lines.RecId))```

   ![式の追加。](media/gte-extension-add-formula.png)

5. **保存** をクリックし、ページを閉じます。
6. **$PurchLine** で、計算済フィールド **\$IsIntraStateInUnionTerritory** を追加し、次の式を使用します。 
   
   ```xpp
   AND('purchase order'.'$PurchLine'.'initTaxModelDocLine_IN()'.getPartyLogisticsPostalAddress.'>Relations'.State.StateId = 'purchase order'.'$PurchLine'.'initTaxModelDocLine_IN()'.getTaxLogisticsPostalAddress.'>Relations'.State.StateId, 'purchase order'.'$PurchLine'.'initTaxModelDocLine_IN()'.getPartyLogisticsPostalAddress.'>Relations'.State.UnionTerritory_IN = NoYesAx.Yes, 'purchase order'.'$PurchLine'.'initTaxModelDocLine_IN()'.getTaxLogisticsPostalAddress.'>Relations'.State.UnionTerritory_IN = NoYesAx.Yes)
   ```

7. **モデル マッピング デザイナー** でマッピングを完了します。
   1. **Data Sources** ツリーで、**$IntraStateInUnionTerritory** を選択します。
   2. **Data Model** ツリーで、**IntraStateInUnionTerritory** を選択します。
   3. **編集** をクリックします。

      ![データ マッピングの編集。](media/gte-extension-data-binding2.png)

   4. ブール値を、拡張課税対象ドキュメントの **IntraStateInUnionTerritory** フィールドで使用される列挙値に変換するために次の式を入力します。

      ```xpp
      CASE('purchase order'.'$PurchLine'.'$IsIntraStateInUnionTerritory', true, NoYesModel.Yes, false, NoYesModel.No)
      ```

   5. **保存** をクリックし、ページを閉じます。

8. コンフィギュレーションを保存し、デザイナーを閉じます。
9. **コンフィギュレーション** ワークスペースで、**ステータスを変更** > **完了** をクリックします。

    ![コンフィギュレーション状態の変更。](media/gte-change-configuration-status.png)

10. **UTGST** のように説明を入力し、**OK** をクリックします。
11. エラーがある場合は、デザイナーを開き、**検証** をクリックし、エラーを修正します。

### <a name="change-the-data-model-of-tax-india-gst-contoso"></a>税 (インド販売税 Contoso) のデータ モデルを変更します。

1. **税 (インド販売税 Contoso)** コンフィギュレーションに移動し、**デザイナー** をクリックします。
2. **税務書類** をクリックして、データ モデルとして **課税対象ドキュメント (インド Contoso)** を選択し、データ モデル バージョンとして **1** を選択します。

    ![税務書類。](media/gte-tax-document-designer.png)

3. **保存** をクリックしてコンフィギュレーションを保存します。

### <a name="change-the-applicability-of-sgst"></a>SGST の適用条件を変更

1. **税 (インド販売税 Contoso)** コンフィギュレーションに移動し、**ドラフト** の状態になっているバージョンを選択し、**デザイナー** をクリックします。
2. **税務書類** > **ヘッダー** > **明細行** > **販売税** > **SGST** と移動し、**ルックアップ** タブをクリックします。
3. **列** をクリックします。
4. **利用可能な列** 一覧から、**IntraStateInUnionTerritory** を選択し、右矢印ボタンをクリックして列を **選択した列** リストに移動させます。
5. **OK** をクリックします。
6. **IntraStateInUnionTerritory** 列で、**いいえ** を選択します。
7. **保存** をクリックしてコンフィギュレーションを保存します。

### <a name="configure-the-utgst-tax-component"></a>UTGST 税コンポーネントを構成します。

1. **税 (インド販売税 Contoso)** コンフィギュレーションに移動し、**ドラフト** の状態になっているバージョンを選択し、**デザイナー** をクリックします。
2. UTGST 税コンポーネントを追加します。
    1. **税務書類** > **ヘッダー** > **明細行** > **販売税** と移動します。 **追加** をクリックし、**税コンポーネント** を選択します。
    2. UTGST 税コンポーネントに名前と説明を入力し、**OK** をクリックします。
3. UTGST 税コンポーネントの税措置を構成します。
   1. 税務書類ツリーを展開し、UTGST 税コンポーネントをクリックして、措置を作成します。
   2. **追加** をクリックし、**税措置** を選択します。
   3. UTGST の適用可能性以外、プロパティ、検索、式、転記の場合、および会計など、すべてのロジックは SGST の場合と同じです。 したがって、SGST で使用するすべての税基準を **名前** 一覧で選択し、**OK** をクリックします。 

      ![一覧表示されている措置。](media/gte-utgst-list.png)

4. ルックアップの率/パーセンテージを構成します。
    1. **UTGST** 税コンポーネント ノードを展開します。
    2. **率/パーセンテージ** 型の基準を選択する。
    3. **ルックアップ** > **列** をクリックして、税率/パーセンテージの値に関連する属性の一覧を表示します。
    4. SGST が使用するのと同じ属性を選択します。
        > [!Note]
        > **追加** をクリックしないでください。 ここで入力した値は、実際の単価表に影響を与えません。 そのテーブルは、**税** > **税コンフィギュレーション** > **税の設定** で構成される必要があります。

    5. 税務書類を保存します。

5. プロパティを構成する。
   1. **Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。 **プロパティ** タブをクリックします。
   2. **条件** の横にある **編集** (鉛筆アイコン) クリックします。
   3. SGST が使用するのと同じ条件を入力します。

      ![SGST 条件。](media/gte-sgst-condition.png)

   4. 税務書類を保存します。

6. 税の適用可能性のルックアップを構成します。
    1. **Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。 **ルックアップ** タブをクリックします。
    2. **列** をクリックします。
    3. **インポート オーダー** および **IntraStateInUnionTerritory** を参照列として選択します。
    4. **コンフィギュレーション** をソース タイプとして選択します。
    5. **追加** をクリックします。 **インポート オーダー** 列には **いいえ** を選択し、**IntraStateInUnionTerritory** 列には **はい** を選択します。   
    6. 税務書類を保存します。

7. コンフィギュレーション形式 式は、グループ ノードのレベル (行、税コンポーネントまたは税タイプ) または基準ノード レベルで構成できます。 ただし、常にグループ ノード レベルで税の計算式を設定することをお勧めします。 税額の配分式は、グループ ノード レベル (行、税コンポーネントまたは税タイプ) または基準ノード レベルで構成できます。
    1. **Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。 **式** タブをクリックします。
    2. **税式の追加** をクリックします。
    3. **詳細** クイック タブで、カテゴリとして **計算** を選択し、式と条件を編集します。
    4. UTGST 税コンポーネントが SGST とすべて同じ式になるまで手順 2 ~ 3 を繰り返します。
    5. 税務書類を保存します。

8. 転記プロファイルを構成します。 **税コンポーネント** タイプのノードのみ、転記プロファイルの定義をサポートします。
    1. **Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。 **転記** タブをクリックします。
    2. **転記プロファイルの追加** をクリックして新しい転記プロファイルの定義を作成します。
    3. **詳細** クイック タブで、前のタスクで定義されている税基準の会計処理を入力し、借方と貸方の会計補助元帳の名前を提供します。
    4. **編集** をクリックして、転記プロファイルの条件を入力します。
    5. 必要に応じて、転記プロファイルの説明を入力します。
    6. UTGST 税コンポーネントが SGST とすべて同じ転記プロファイルとなるまで手順 2 ~ 3 を繰り返します。
    7. 税務書類を保存します。

9. 会計のルックアップを構成します。 **税タイプ** および **税コンポーネント** タイプのノードのみ会計ルックアップの定義をサポートします。
    1. **Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。 **会計** タブをクリックします。
    2. **列** をクリックして、税金の計算に使用される主勘定を決定するために使用できる属性の一覧を表示します。
    3. SGST が使用するのと同じ属性を選択します。
        > [!NOTE]
        > **追加** をクリックしないでください。 ここで入力した値は、実際の税主勘定決定テーブルに影響を与えません。 そのテーブルは、**税** > **税コンフィギュレーション** > **税の設定** で構成される必要があります。

    4. 税務書類を保存します。

10. クレジット プールを構成します。 **税コンポーネント** タイプのノードのみクレジット プールの定義をサポートします。
    1. **Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。 **クレジット プール** タブをクリックします。
    2. **列** をクリックして、このコンポーネントの税決済に関連する属性の一覧を表示します。 通常、選択された列は、**販売税登録番号** のように適切な税登録番号です。
    3. SGST が使用するのと同じ属性を選択します。
        > [!NOTE]
        > **追加** をクリックしないでください。 ここで入力した値は、実際の単価表に影響を与えません。 そのテーブルは、**税** > **税コンフィギュレーション** > **税の設定** で構成される必要があります。

    4. 税務書類を保存します。

### <a name="modify-the-formulas-of-lines-to-include-utgst"></a>UTGST を含めるために明細行の式を変更します。

1. **税務書類** > **ヘッダー** > **明細行** と移動します。 **式** タブをクリックします。
2. **基準金額**、**明細行の税額**、および **価格に含まれる税額** 基準を含むすべての数式を変更し、数式が UTGST を反映するようにします。 たとえば、**内税額** 式を次のように変更します。

   ![内税額の式。](media/gte-tax-amount-inclusive.png)
    
3. 税務書類を保存します。
4. デザイナーを閉じます。

### <a name="complete-the-tax-document-configuration"></a>税務書類のコンフィギュレーションを完了します。
1. **ローカライズ コンフィギュレーション** ワークスペース (**組織管理** > **ワークスペース** > **電子申告**)、をクリックして **税のコンフィギュレーション**。
2. **コンフィギュレーション** ワークスペースで、**状態の変更** をクリックし、**完了** を選択します。
3. **UTGST** のように説明を入力し、**OK** をクリックします。
4. エラーがある場合は、デザイナーを開き、**検証** をクリックし、エラーを修正します。
5. ステータスが **完了** に更新されると、コンフィギュレーションを配置できる状態です。

### <a name="import-the-configuration-and-deploy-it-to-a-specific-company"></a>コンフィギュレーションをインポートし、特定の会社に配置します。
1. **税** > **設定** > **税コンフィギュレーション** > **税の設定** と移動します。
2. 新しいレコードを作成し、税の設定を定義します。

    ![新しい税の設定。](media/gte-extension-new-tax-setup.png)

3. **コンフィギュレーション** をクリックします。

4. **税コンフィギュレーション** タブをクリックします。
5. **利用可能な構成** セクションで、**新規** をクリックして税コンフィギュレーションを作成します。

    > [!NOTE]
    > 税に追加されるコンフィギュレーションは、**使用可能なコンフィギュレーション** タブに一覧表示されます。
    
    ![新しいコンフィギュレーション。](media/gte-extension-new-configuration2.png)

6. **税 (インド販売税)** のように、必要なコンフィギュレーションを選択します。 **保存** をクリックします。
7. **同期化** をクリックします。

    ![コンフィギュレーションの同期。](media/gte-extension-synchronize-configuration.png)

8. **有効化** をクリックします。

    ![コンフィギュレーションの有効化。](media/gte-extension-activate-configuration.png)

    ![有効なコンフィギュレーション。](media/gte-extension-active-configuration.png)

9. **閉じる** をクリックします。
10. **会社** クイック タブをクリックします。
11. **新規** をクリックし、**会社** フィールドで、**INMF** を選択します。
12. **保存** をクリックします。
13. **有効化** をクリックして、会社のコンフィギュレーションを有効にします。

    ![会社のコンフィギュレーションの有効化。](media/gte-extension-activate-configuration-to-company.png)

14. **設定** をクリックして、新しいバージョンのデータを設定します。

## <a name="scenario-2-using-a-reference-model"></a>シナリオ 2 : 参照モデルを使用します。

Microsoft 製のコンフィギュレーションごとに、BCD の税率は、優先的関係者/インポート オーダー/カスタム輸入税率コード/エクスポート オーダー/エクスポート カスタム輸出税率コードによって決定されます。 このシナリオを使って、さまざまな国/地域からの商品のインポート オーダーに BCD の異なる税率を適用することをサポートするために参照モデルを使用する方法について説明します。

このシナリオでは、次の作業を完了する必要があります:
1. [拡張コンフィギュレーションの作成](#create-extension-configurations)
2. [原産国/地域の参照モデルを追加します](#add-a-reference-model-for-countryregion-of-origin)
3. [参照モデルのデータ マッピングを完了します](#complete-data-mapping-for-the-reference-model)
4. [課税対象ドキュメントのフィールドに参照モデルをリンクします](#link-the-reference-model-to-a-field-in-the-taxable-document)
5. [BCD税率のルックアップを変更します](#change-the-lookup-of-the-bcd-tax-rate)
6. [税に関する文書のコンフィギュレーションを完了します](#complete-the-tax-document-configuration)
7. [コンフィギュレーションをインポートし、特定の会社に配置します](#import-the-configuration-and-deploy-it-to-a-specific-company)

### <a name="add-a-reference-model-for-countryregion-of-origin"></a>原産国/地域の参照モデルを追加します。

1. **ローカライズ コンフィギュレーション** ワークスペース (**組織管理** > **ワークスペース** > **電子申告**)、をクリックして **税のコンフィギュレーション**。
2. **課税対象ドキュメント (インド Contoso)** コンフィギュレーションを検索、選択し、**デザイナー** をクリックします。
3. **...** > **参照モデル** をクリックして、すべての使用可能な参照モデルを表示できるように、ビューを変更します。
4. **新規** をクリックして、新しい参照モデルを追加します。
    -   **名前** - 原産国
    -   **ノード タイプ**- モデル ルート
5. **追加** をクリックします。
6. **原産国** を強調表示して、**新規** をクリックし、新しい参照モデルを追加します。
    -   **名前** - 原産国
    -   **ノード タイプ** - 有効な子ノード
    -   **品目タイプ** - レコードの一覧
7. **追加** をクリックします。
8. **原産国** を強調表示して、**新規** をクリックし、新しい参照モデルを追加します。
    -   **名前** - 原産国
    -   **ノード タイプ** - 有効な子ノード
    -   **品目タイプ** 文字列
9. **追加** をクリックします。
10. **原産国** を強調表示して、**ナチュラル キー** をクリックします。
11. **原産国\\原産国\\原産国** を、**ナチュラル キー** として選択します。
12. エラーがある場合は、デザイナーを開き、**検証** をクリックし、エラーを修正します。

状態を **完了** に更新すると、コンフィギュレーションを配置できる状態になります。

### <a name="complete-data-mapping-for-the-reference-model"></a>参照モデルのデータ マッピングを完了します。
1. **ローカライズ コンフィギュレーション** ワークスペース (**組織管理** > **ワークスペース** > **電子申告**)、をクリックして **税のコンフィギュレーション**。
2. **課税対象ドキュメント (インド Contoso)** コンフィギュレーションを検索、選択し、**デザイナー** をクリックします。
3. **モデルからデータ ソースへのマップ** をクリックします。
4. **原産国** を選択し、**追加** をクリックします。
5. 一覧で **原産国** を選択して、**デザイナー** をクリックし、モデル マッピングのデザイナーを開きます。
6. ルートとして **LogisticsAddressCountryRegion** テーブル レコードを追加します。
    1. **データ ソース タイプ** で、**テーブル レコード** を選択します。
    2. **ルートの追加** をクリックします。
    3. **名前** フィールドに、**LogisticsAddressCountryRegion** という名前を入力します。
    4. テーブルを選択します。
    5. **OK** をクリックします。
    
    ![テーブル レコードの追加。](media/gte-extension-add-table-records.png)

7. テーブルをバインドします。

    1. **データ ソース** ツリーで、手順 5 で作成した **LogisticsAddressCountryRegion** テーブル レコードを選択します。
    2. **日付モデル** ツリーで、**原産国: レコードの一覧** を選択します。
    3. **バインド** をクリックします。
    
    ![テーブルのバインド。](media/gte-extension-bind-table.png)

8. フィールドをバインドします。

    1. **データ ソース** ツリーで、**国/地域 (CountryRegionID): 文字列** を選択します。
    2. **データ モデル** ツリーで、**原産国: 文字列** を選択します。
    3. **バインド** をクリックします。

    ![フィールドのバインド。](media/gte-extension-bind-field.png)

9. **保存** をクリックします。

### <a name="link-the-reference-model-to-a-field-in-the-taxable-document"></a>課税対象ドキュメントで、参照モデルをフィールドにリンクします。

1. **...** > **課税対象ドキュメント** をクリックし、**課税対象ドキュメント** に対するビューを変更します。
2. **課税対象ドキュメント** > **ヘッダー** > **明細行** > **販売税** > **原産国/地域** と移動します。
3. **ノード** クイック タブで、**参照モデルを選択** をクリックします。 
4. 参照モデルに **原産国** を選択します。
5. **OK** をクリックします。
6. コンフィギュレーションを保存し、デザイナーを閉じます。
7. **コンフィギュレーション** ワークスペースで、**状態の変更** をクリックし、**完了** を選択します。
8. **原産国の参照モデルの追加** のように説明を入力し、**OK** をクリックします。
9. エラーがある場合は、デザイナーを開き、**検証** をクリックし、エラーを修正します。

ステータスが **完了** に更新されると、コンフィギュレーションを配置できる状態です。

### <a name="change-the-lookup-of-the-bcd-tax-rate"></a>BCD 税率のルックアップを変更します

1.  **税 (インド販売税 Contoso)** コンフィギュレーションに移動し、**デザイナー** をクリックします。
2.  **税 (インド販売税 Contoso)** のデータ モデルを、拡張された課税対象ドキュメントの更新されたバージョンに変更します。 これを行うには、[シナリオ 1、タスク 3 : 拡張された課税対象ドキュメントのデータ マッピングを完了](#complete-data-mapping-for-the-extended-taxable-document) にある手順を完了します。
3.  **税務書類** > **ヘッダー** > **明細行** > **カスタム関税** > **BCD** > **レート** と移動します。 **ルックアップ** タブをクリックします。
4.  **列** をクリックします。
5.  ルックアップ列として **原産国/地域** を選択し、右矢印ボタンをクリックします。
6.  **保存** をクリックします。

### <a name="rebase-the-extension-configuration-to-the-latest-microsoft-configuration"></a>拡張機能コンフィギュレーションを最新の Microsoft コンフィギュレーションにリベースする

1. **拡張機能コンフィギュレーション** に移動し、**リベース** を選択します。 
2. **リベース** ダイアログ ボックスの **ターゲット バージョン** フィールドで、ターゲットバージョンを最新の Microsoft バージョンに変更します。

    [![リベース手順 1。](./media/extend-tax-engine-configurations-rebase1.png)](./media/extend-tax-engine-configurations-rebase1.png)

    競合がある場合は、警告メッセージが表示されます。
    
    [![リベース手順 2。](./media/extend-tax-engine-configurations-rebase2.png)](./media/extend-tax-engine-configurations-rebase2.png)

3. 競合を解決するには、**デザイナー** を選択してリベースされた拡張機能コンフィギュレーションを開きます。

    [![リベース手順 3。](./media/extend-tax-engine-configurations-rebase3.png)](./media/extend-tax-engine-configurations-rebase3.png)

4. 次の 3 つの方法のいずれかを選択して、競合を解決します。

    - **前の基準値を適用する**: コンフィギュレーションを初めて作成するときに、基本コンフィギュレーションから元の値を適用します。
    - **基準値を適用する**: ターゲット基本コンフィギュレーションから現在の値を適用します。
    - **独自の値を保持する**: 拡張機能コンフィギュレーションから値を適用します。

5. 競合を解決すると、**解決済** のチェック ボックスがマークされます。

    [![リベース手順 4。](./media/extend-tax-engine-configurations-rebase4.png)](./media/extend-tax-engine-configurations-rebase4.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
