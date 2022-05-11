---
title: 顧客 CDX パッケージを拡張してカスタム データを追加する
description: このトピックでは、Microsoft Dynamics 365 Commerce の顧客の Commerce Data Exchange (CDX) パッケージにカスタム データを追加する方法について説明します。
author: mugunthanm
ms.date: 04/21/2022
ms.topic: article
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 03-30-2022
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: d21f6f342a8a1bc07ec373ef7be5486f98b963a1
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629723"
---
# <a name="extend-the-customer-cdx-package-to-add-custom-data"></a>顧客 CDX パッケージを拡張してカスタム データを追加する

[!include [banner](../includes/banner.md)]

このトピックでは、顧客の Commerce Data Exchange (CDX) パッケージを拡張して、Microsoft Dynamics 365 Commerce にカスタム データを追加する方法について説明します。

販売時点管理 (POS) またはクライアント アプリケーションが Commerce 顧客検索アプリケーション プログラミング インターフェイス (API) を呼び出す場合、API はチャネル データベースで顧客を検索します。 チャネル データベースで顧客が見つからず、コマースの本部でリモート検索が有効になっている場合、API はコマースの本部にリアルタイムで呼び出しを行いデータを取得します。 コマース本部で顧客データが見つかった場合は、コマース本部は顧客データ CDX パッケージを生成し、それをチャネル データベースに同期します。

顧客データ (たとえば、**ロイヤルティ**、**所属**、**拡張** テーブル データ) を CDX パッケージの一部にとして含め、それをチャネル データベースに同期する場合は、X++ を使用してコマース本部の **RetailTransactionServiceCustomerExtensions** クラスを拡張する必要があります。

パッケージのカスタム データ部分を追加するには、**RetailTransactionServiceCustomerExtensions** クラスから **addAdditionalCustomerDataToPackage** メソッドを上書きし、カスタム クエリを追加して必要なテーブルからデータを読み込んでから、**RetailCdxDataPackageSerializationHelper** オブジェクトにデータ部分を書き込みます。

## <a name="prerequisites-for-adding-the-x-extension"></a>X++ 拡張子を追加するための前提条件

- カスタム テーブルとフィールドを同期するには、CDX を拡張する必要があります。 拡張テーブルを同期している場合、拡張テーブル データを読み取るには、Commerce Runtime (CRT) の拡張が必要です。 既成の CRT コードがデータを取り込むため、もし既存のエンティティ (たとえば、**ロイヤルティ**、**所属**、**顧客**) を使用している場合、CRT の拡張は必要ありません。 詳細情報については、[拡張を介してカスタムCommerce Data Exchange 同期を有効する](cdx-extensibility.md)を参照してください。
- **顧客** テーブルと取り込まれる追加データの間のデータ整合性を維持します。 この追加のデータには、拡張テーブルが含まれます。
- すべての拡張テーブルおよび同期テーブルには、CDX フレームワークがテーブルにデータを書き込むための書き込みアクセス許可が必要です。

Customer CDX データ パッケージのデータ部分を追加するカスタム メソッドを作成するには、次の手順に従います。

1. Microsoft Visual Studio を開く。
1. **Dynamics 365** メニューで、**モデル管理 \> モデルの作成** をクリックします。
1. **モデルの作成** ダイアログ ボックスに、次の情報を入力します。

    - **モデル名:** Contoso
    - **モデル発行元:** Contoso
    - **バージョン:** 1.0.0.0
    - **モデルの表示名:** Contoso

1. **次へ** を選択します。
1. **既存のパッケージを選択** を選択してから、ドロップダウン リストで **アプリケーション スイート** を選択します。
1. **次へ** を選択します。
1. **完了** を選択します。
1. **新しいプロジェクト** ダイアログ ボックスに、**RetailTransactionServiceCustomerExtensions** というプロジェクト名を入力します。
1.  **OK** を選択します。
1. プロジェクトを選択したままにして (または右クリック)、**追加 \> 新しい項目** を選択します。
1. **新しい項目の追加** ダイアログ ボックスで、**クラス** を選択し、**RetailTransactionServiceCustomerExtensions_Sample_Extension** をクラス名として入力します。
1. 次の例に示すように、**ExtensionOf** 属性をクラスに追加してから、**RetailTransactionServiceCustomerExtensions** クラスを属性値として指定します。

    ```X++
    [ExtensionOf(classStr(RetailTransactionServiceCustomerExtensions))]
    public final class RetailTransactionServiceCustomerExtensions_Sample_Extension
    {
    }
    ```

1. **addAdditionalCustomerDataToPackage** メソッドを上書きし、必要なテーブルからデータを取り込みます。

## <a name="example"></a>例

この例では、データは次のテーブルから取り込まれ、パッケージに含まれています。

- RetailLoyaltyCard
- RetailLoyaltyCardTier
- CustTable
- ContosoRetailCustPreferredContactHours

```X++
/// <summary>
/// Extension method to add additional data to customer data package.
/// </summary>
/// <param name = "serializer">The CDX data package serializer.</param>
/// <param name = "customerRecord">The <see cref="CustTable" /> record for which related information needs to be added.</param>
public static void addAdditionalCustomerDataToPackage(RetailCdxDataPackageSerializationHelper serializer, CustTable customerRecord)
{
    RetailLoyaltyCard loyaltyCard;
    RetailLoyaltyCardTier loyaltyCardTier;
    CustTable extensionCustTable;
    ContosoRetailCustPreferredContactHours contactHoursTable;

    while select loyaltyCard
        where loyaltyCard.Party == customerRecord.Party
    {
        serializer.writeRecord(loyaltyCard);
        loyaltyCardTableAddedToPackage = true;

        while select loyaltyCardTier
            where loyaltyCardTier.LoyaltyCard == loyaltyCard.RecId
        {
            serializer.writeRecord(loyaltyCardTier);
            loyaltyCardTierTableAddedToPackage = true;
        }
    }

    while select contactHoursTable
    {
        serializer.writeRecord(contactHoursTable);
        extensionTableAddedToPackage = true;
    }
}
```

## <a name="full-sample-code"></a>完全なサンプル コード

```X++
/// <summary>
/// Extension sample for RetailTransactionServiceCustomerExtensions::addAdditionalCustomerDataToPackage() method.
/// </summary>
[ExtensionOf(classStr(RetailTransactionServiceCustomerExtensions))]
public final class RetailTransactionServiceCustomerExtensions_Sample_Extension
{
    // These fields are added for unit testing only and are not needed for extension functionality.
    public static boolean loyaltyCardTableAddedToPackage;
    public static boolean loyaltyCardTierTableAddedToPackage;
    public static boolean extensionTableAddedToPackage;

    /// <summary>
    /// Extension method to add additional data to customer data package.
    /// </summary>
    /// <param name = "serializer">The CDX data package serializer.</param>
    /// <param name = "customerRecord">The <see cref="CustTable" /> record for which related information needs to be added.</param>
    public static void addAdditionalCustomerDataToPackage(RetailCdxDataPackageSerializationHelper serializer, CustTable customerRecord)
    {
        RetailLoyaltyCard loyaltyCard;
        RetailLoyaltyCardTier loyaltyCardTier;
        CustTable extensionCustTable;
        ContosoRetailCustPreferredContactHours contactHoursTable;

        while select loyaltyCard
            where loyaltyCard.Party == customerRecord.Party
        {
            serializer.writeRecord(loyaltyCard);
            loyaltyCardTableAddedToPackage = true;

            while select loyaltyCardTier
                where loyaltyCardTier.LoyaltyCard == loyaltyCard.RecId
            {
                serializer.writeRecord(loyaltyCardTier);
                loyaltyCardTierTableAddedToPackage = true;
            }
        }

        while select contactHoursTable
        {
            serializer.writeRecord(contactHoursTable);
            extensionTableAddedToPackage = true;
        }
    }
}
```
