---
title: トランザクション イベント用の電子メール テンプレートの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce のトランザクション イベントにおける電子メールテンプレートの作成、アップロード、構成する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 245ca998ef3e6d172df3525f06d7901f3f41b650
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000788"
---
# <a name="create-email-templates-for-transactional-events"></a>トランザクション イベント用の電子メール テンプレートの作成

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のトランザクション イベントにおける電子メールテンプレートの作成、アップロード、構成する方法について説明します。

## <a name="overview"></a>概要

Dynamics 365 Commerce では、トランザクション イベントについて顧客に通知する電子メールを送信する既成のソリューションが用意されています (たとえば、注文が行われたり、注文が集配できる状態になったり、注文が出荷されたりした場合など)。 このトピックでは、トランザクション電子メールの送信に使用される電子メール テンプレートの作成、アップロード、構成をする手順について説明します。

## <a name="create-an-email-template"></a>電子メール テンプレートを作成する

特定のトランザクション イベントを電子メールのテンプレートにマッピングするには、事前にテンプレートを作成しておく必要があります。

電子メール テンプレートを作成するには、次の手順に従います。

1. Commerce 本部で **Retail と Commerce \> 本社の設定 \> 組織の電子メール テンプレート** または、**組織管理 \> 設定 \> 組織の電子メール テンプレート** にある **組織の電子メールテンプレート** に移動します。
1. **新規** を選択します。
1. **全般** 配下で、次のフィールドを設定します:

    - **電子メール ID** – 電子メール ID はテンプレートに固有の ID であり、イベントにマッピングするテンプレートを選択した際に表示される値です。
    - **電子メールの説明** – このオプション フィールドを使用して、テンプレートの説明を入力できます。 入力した値は、Commerce 本部でのみ表示されます。
    - **送信者名** – ここに入力した名前が、ほとんどの電子メール クライアントの [差出人] フィールドに表示されます。
    - **送信者の電子メール** – このテンプレートを使用して送信する電子メールが使用する電子メールのアドレスを入力します。
    - **既定の言語コード** – このテンプレートを呼び出すチャネルで言語が提供されていない場合、送信される電子メールのローカライズされたバージョンを指定します。

1. **電子メール メッセージ コンテンツ** 配下で、**新規** を選択します。
1. **言語** フィールドに、電子メール テンプレートの言語を入力します。 言語とローカライズされたテンプレートは後で追加することもできます。
1. **件名** フィールドには、電子メールの件名フィールドに表示される件名を入力します。
1. 電子メールのテンプレートをアップロードするには、**編集** を選択します。

## <a name="create-an-email-message-body-by-using-html"></a>HTML を使用して電子メール メッセージの本文を作成する

電子メール メッセージの本文はHTMLで構成されています。 HTML およびインライン カスケードスタイルシート (CSS) で使用できる任意のレイアウト、スタイル、ブランディングを使用できます。 一般に公開されている web のエンドポイントに画像をホストする場合は、画像を使用することもできます。 画像を追加するには、HTML **&lt;img&gt;** タグの **src** 属性に画像のURLを入力します。

> [!NOTE]
> 電子メール クライアントにはレイアウトやスタイルの制限があり、メッセージ本文に使用するHTMLや CSS の調整が必要となる場合があります。 人気の高い電子メール クライアントで対応しているHTMLを作成するためのベストプラクティスについて理解しておくことを推奨します。

## <a name="add-placeholders-to-the-email-message-body"></a>電子メール メッセージの本文にプレースホルダーを追加する

電子メールにはプレースホルダーを含めることができます。これは電子メールが生成された際に顧客固有の値やトランザクション固有の値に置き換えられます。 プレースホルダは常にパーセント記号 (%) で囲まれており、HTML 文書の中に直接挿入されます。

次に例を示します。

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>注文のプレースホルダー (販売注文レベル)

以下のプレースホルダーは、販売注文レベルで定義されたデータを取得して表示します (販売明細行レベルとは異なります)。

| プレースホルダー名    | プレースホルダー値                                                |
|---------------------|------------------------------------------------------------------|
| customername        | 注文を行った顧客の名称です。                   |
| salesid             | 注文の販売 ID です。                                       |
| deliveryaddress     | 出荷注文の配送先住所です。                         |
| customeraddress     | 顧客の住所です。                                     |
| deliverydate        | 配送日です。                                               |
| shipdate            | 出荷日です。                                                   |
| modeofdelivery      | 注文の出荷モードです。                                  |
| 請求             | 注文に対する金額の合計です。                                 |
| 税                 | 注文の税の合計です。                                     |
| 合計               | 注文に対する金額の総計です。                                  |
| ordernetamount      | 注文の合計金額から税の合計を差し引いた金額です。             |
| 割引            | 注文に対する割引の合計です。                                |
| storename           | 注文を行った店舗の名称です。                |
| storeaddress        | 注文を行った顧客の住所です。                  |
| storeopenfrom       | 注文を行った店舗の開店時間です。             |
| storeopento         | 注文を行った店舗の閉店時間です。             |
| pickupstorename     | 注文が受け取られる店舗の名称です。         |
| pickupstoreaddress  | 注文がピッキングされる店舗の住所です。      |
| pickupopenstorefrom | 注文がピッキングされる店舗の開店時間です。 |
| pickupopenstoreto   | 注文がピッキングされる店舗の閉店時間です。 |

### <a name="order-line-placeholders-sales-line-level"></a>注文ラインのプレースホルダー (販売ライン レベル)

以下のプレースホルダーは、販売注文の個々の製品 (明細行) のデータを取得して表示します。

| プレースホルダー名               | プレースホルダー値 |
|--------------------------------|-------------------|
| productid                      | 明細行の製品 ID です。 |
| lineproductname                | 生産の名前。 |
| lineproductdescription         | 製品の説明。 |
| linequantity                   | ラインに発注された単位数と測定単位 (**ea**、**pair** など) です。 |
| lineunit                       | ラインの測定単位です。 |
| linequantity_withoutunit       | ラインに発注された単位数で、測定単位を含まないもの。 |
| linequantitypicked             | 注文の **PickOrder** イベントが使用された場合の、ピッキングされた単位の数です。 これに該当しない場合は **0** (ゼロ) になります。 |
| linequantitypicked_withoutunit | **PickOrder** イベントが使用された場合の、測定単位を含まない、ピッキングされた単位の数です。 これに該当しない場合は **0** (ゼロ) になります。 |
| linequantitypacked             | **PackOrder** および **ピックアップ可能な注文** イベントが使用された場合の、梱包された単位数です。 これに該当しない場合は **0** (ゼロ) になります。 |
| linequantitypacked_withoutuom  | **PackOrder** および **ピックアップ可能な注文** イベントが使用された場合の、測定単位を含まない、梱包された単位数です。 これに該当しない場合は **0** (ゼロ) になります。 |
| linequantityshipped            | 以下に説明するように、特定のイベントが使用されている場合を除き、常に **0** となります。 |
| linequantityshipped_withoutuom | **ShipOrder** イベントが使用された場合の、測定単位を含まない、ピッキングされた単位の数です。 これに該当しない場合は **0** (ゼロ) になります。 |
| lineprice                      | 一単位の価格です。 |
| linenetamount                  | 単位および適用後のラインの価格です。 |
| linediscount                   | 個々の単位の割引です。 |
| lineshipdate                   | 当該ラインの出荷日です。 |
| linedeliverydate               | 当該ラインの配達日です。 |
| linedeliverymode               | 当該ラインの配送モードです。 |
| linedeliveryaddress            | 当該ラインの配達先住所です。 |
| giftcardnumber                 | ギフト カード タイプの製品の場合の、ギフトカード番号です。 |
| giftcardbalance                | ギフト カード タイプの製品の場合の、ギフトカード残高です。 |
| giftcardmessage                | ギフト カード タイプの製品の場合の、ギフトカードのメッセージです。 |
| giftcardpin                    | ギフト カード タイプの製品の場合の、ギフトカードの識別番号 (PIN) です。 (このプレースホルダーは、外部のギフトカードに固有のものです) |
| giftcardexpiration             | ギフト カード タイプの製品の場合の、ギフトカードの有効期限です。 (このプレースホルダーは、外部のギフトカードに固有のものです) |
| giftcardrecipientname          | ギフト カード タイプの製品の場合の、ギフトカードの受取人の名前です。 |
| giftcardbuyername              | ギフト カード タイプの製品の場合の、ギフトカードの購入者の名前です。 |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>電子メール メッセージ本文における注文明細行のプレースホルダーの形式

電子メールのメッセージ本文内の個々の注文明細行の HTML を作成する際には、HTML の繰り返しブロックとその行のプレースホルダーを、HTML のコメントタグの中に入れた以下のプレースホルダーで囲みます。

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

次に例を示します。

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>メールで送信される領収書のテンプレートを作成する

領収書は、販売時点管理 (POS) で購入した顧客に電子メールで送信することができます。 一般的には、メールで送信する領収書のテンプレートの作成手順は、その他のトランザクション イベントのテンプレートの作成手順と同じです。 この場合、以下の変更が必要となります:

- 電子メールのテンプレートで使用するメール ID には **emailRecpt** を指定する必要があります。
- 領収書のテキストは、**%message%** のプレースホルダーを使用して電子メールに挿入されます。 領収書の本文が正しく表示されるように、 **%message%** プレースホルダーを HTML タグの **&lt;pre&gt;** **&lt;/pre&gt;** で囲みます。
- 電子メールのヘッダーとフッターにおける HTML の改行は、領収書の本文が正しく表示されるように HTML の **&lt;br /&gt;** タグに変換されます。 領収書メールの不要な縦のスペースを削除するには、HTML 内の縦のスペースが不要な場所で改行を削除します。

電子メールで送信する領収書の構成方法については、[電子メールで送信する領収書の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts) を参照してください。

## <a name="upload-the-email-html"></a>電子メールの HTML をアップロードする

HTML を作成し、テストした後は、メッセージの本文を Commerce 本部にアップロードする必要があります。 現時点では、電子メールの HTML はエクスポートできません。 そのため、HTML のマスターコピーは Commerce 本部以外で管理する必要があります。

新規、または編集した電子メールのテンプレート HTML をアップロードするには、次の手順に従います。

1. Commerce 本部で、**小売りとコマース \> 本部の設定 \> 組織の電子メールのテンプレート** に移動します。
1. HTML を追加または置換する言語の行を選択します。 または、**新規** を選択して新しい言語の行を作成します。
1. **編集** を選択します。
1. 表示されたダイアログ ボックスで、**参照** を選択します。 アップロードする HTMLドキュメントを参照して選択し、**開く** を選択し ます。
1. **アップロード** を選択します。
1. プレビュー ウィンドウに電子メールの HTML が表示されたら、**OK** を選択します。
1. 行に対して、 **本文** のチェック ボックスが選択されていることを確認します。

Commerce 本部が電子メールを送信するように設定済みの場合は、テンプレートにマッピングされたイベントを呼び出すトランザクションを実行するすべての顧客に、新規または更新された電子メールが送信されます。

Dynamics 365 Commerce で電子メールを構成する方法の詳細については、[電子メールの構成と送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md)を参照してください。

## <a name="additional-resources"></a>追加リソース 

[電子メール通知プロファイルの設定](email-notification-profiles.md)

[電子メールのコンフィギュレーションと送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[電子メールのレシートを設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Modern POS (MPOS) からの領収書メールを送信する](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]