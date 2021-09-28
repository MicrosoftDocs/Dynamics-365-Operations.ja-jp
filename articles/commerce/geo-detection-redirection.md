---
title: 地域の検出とリダイレクトを設定する
description: このトピックでは、Microsoft Dynamics 365 Commerce での eコマース サイトの地域検出とリダイレクトの設定方法について説明します。
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: ''
ms.openlocfilehash: 3510eb446cb9e6170605d51ff7df0db562fba7b8
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472521"
---
# <a name="set-up-geo-detection-and-redirection"></a>地域の検出とリダイレクトを設定する

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce での eコマース サイトの地域検出とリダイレクトの設定方法について説明します。

Dynamics 365 Commerce の地域検出およびリダイレクト機能を使用すると、顧客の地理的位置を検出し、その情報を使用して、各顧客に最も適したマーケティングおよびローカライズされたサイトを推奨できます。 または、顧客を最も適切なサイトに自動的にリダイレクトすることもできます。

現住所の国または地域に関連付けされていないサイト URL を要求する顧客向けに、2 つのエクスペリエンスのいずれかを選択できます。

- 顧客に、現在の場所に関連付けられているサイトを選択するか、最初に要求したサイトに進むかを選択するよう求めます。
- 顧客は、その国または地域に関連付けられているサイトに自動的にリダイレクトされます。

たとえば、カナダの顧客が、カナダに関連付けされていないサイトを要求したとします。 この場合、国/地域の選択モジュールには、カナダ向けに設定されているサイトをリストしたダイアログ ボックスが表示されます。 次の図の例では、カナダ向けの英語およびフランス語のサイトのオプションがダイアログ ボックスに含まれています。

![カナダ向けの英語およびフランス語のサイトについてのオプションを示す地域/言語選択ダイアログ ボックスの例。](./media/Geo_Country-region-picker.png)

顧客がオプションを選択すると、そのサイトにリダイレクトされます。 顧客のサイト基本設定は、Cookie にもキャプチャされます。 したがって、顧客が次にアクセスした時には、サイトを再度選択するように求められることはありません。

## <a name="enable-geo-redirection-features-in-commerce-site-builder"></a>Commerce サイト ビルダーの地域リダイレクト機能の有効化

Commerce サイト ビルダーのサイトで地域リダイレクトを有効にするには、**サイト設定 \> 一般** に移動し、**地域リダイレクト機能の有効化** 設定をオンにします。

> [!IMPORTANT]
> **地域リダイレクト機能の有効化** 設定をオンにする前に、**場所に基づく店舗検出の有効化** 設定をオンにします。 詳細については、[場所に基づく店舗検出の有効化](enable-store-detection.md)を参照してください。

## <a name="associate-countries-and-regions-with-online-stores-in-commerce-headquarters"></a>Commerce 本社でのオンライン ストアへの国と地域の関連付け

国と地域は、Commerce 本社のオンライン ストア (オンライン チャネルとも呼ばれる) に関連付けられています。 国または地域をオンライン ストアに関連付ける場合は、その国または地域に居住する顧客が、そのオンライン ストアにマップされているサイトを表示する必要があることを示します。 必要に応じて、複数の国や地域をオンライン ストアに関連付けることができます。

国または地域をオンライン ストアに関連付けるには、次の手順を実行します。

1. **Retail と Commerce \> チャネル \> オンライン ストア** に移動するか、検索ボックスで "オンライン ストア" を検索します。
1. 国または地域と関連付けるオンライン チャネルを開きます。
1. **国/地域** クイック タブで **追加** を選択し、**国/地域** フィールドで、国または地域を選択します。
1. オンライン チャネルに関連付ける他の国または地域に対して、上の手順を繰り返します。

![Commerce 本社でオンライン ストアにマップされている国や地域を示す例。](./media/Geo_HQ-Country-Mapping.png)

国や地域のオンライン ストアへの関連付けが完了したら、**Retail および Commerce \> Retail および Commerce IT** に移動し、**配送スケジュール** ビューで、ジョブ 1070 (**チャネル コンフィギュレーション**) を実行してください。 そのジョブが完了すると、オンライン ストアに関連付けた国と地域が、Commerce サイト ビルダーの **サイト設定** にある **チャネル** ページで利用できるようになります。

## <a name="configure-geo-redirection-rules-in-commerce-site-builder"></a>Commerce サイト ビルダーの地域リダイレクト ルールのコンフィギュレーション

Commerce サイト ビルダーのオンライン ストアで利用できるようにする国と地域は、**チャネル** ページで定義されている URL にマッピングできます。 次に、顧客が URL を要求すると、地域リダイレクトは、要求された URL が顧客が居住する国または地域に適していることを確認できます。 または、顧客の所在地に対して指定した 1 つ以上の URL を推奨することもできます。

国および地域をサイト URL に関連付けるには、次の手順を実行します。

1. Commerce サイト ビルダーで、**サイト設定 \> チャネル** に移動します。
1. チャネル名を選択し、ロケールを選択します。
1. URL に関連付ける 1 つ以上の国または地域を選択します。
1. **OK** を選択します。
1. **保存して公開** を選択して変更を保存し、公開します。

### <a name="geo-detection-and-redirection-logic"></a>地域検出およびリダイレクトのロジック

Dynamics 365 Commerce の地域検出およびリダイレクトは、顧客の国または地域を Commerce サイト ビルダーの **チャネル** ページの URL にマップされている国および地域のリストと比較することによって機能します。

顧客がサイトの URL を要求すると、システム リダイレクト ロジックは、顧客の国または地域が要求された URL にマップされているかどうかを判断します。 マップされている場合は、顧客は引き続きその URL を使用します。 そうでない場合は、リダイレクト ロジックは顧客の国や地域にマップされている URL を検索して、その URL を推奨 URL として顧客に示します。 顧客の国または地域に対して自動リダイレクトが有効になっている場合、顧客は自動的に、その国または地域の最適な URL にリダイレクトされます。 自動リダイレクトにどの URL を使用するかを定義する方法の詳細については、このトピックの後半にある[自動リダイレクトのコンフィギュレーション](#configure-automatic-redirection)を参照してください。

次のワークフロー図は、リダイレクト ロジックの手順と決定事項を示しています。

![リダイレクト ロジックの手順と決定事項を示すワークフロー図。](./media/Geo_Redirection-Logic.png)

## <a name="configure-the-countryregion-picker-module"></a>国/地域の選択モジュールのコンフィギュレーション

Commerce モジュール ライブラリに含まれている国/地域の選択モジュールは、国または地域に関連付けられていない URL を要求する顧客に推奨 URL を表示します。 国/地域の選択モジュールのコンフィギュレーションの詳細については、[国/地域の選択モジュール](country-region-picker-module.md)を参照してください。

## <a name="configure-automatic-redirection"></a>自動リダイレクトのコンフィギュレーション

国/地域の選択ダイアログ ボックスから URL を選択するように顧客に求める代わりに、特定の国または地域の顧客を指定した URL に自動的にリダイレクトすることができます。 たとえば、日本に住んでいる顧客を、日本のチャネルと言語にマップされたサイトに自動的に送るとします。 この場合、その URL がコンフィギュレーションされているチャネルで **自動リダイレクト** 設定をオンにします。 変更を保存して公開すると、日本の顧客はその URL に自動的に送られ、国/地域の選択ダイアログ ボックスは表示されません。

国または地域に複数の URL を関連付けることができます。 この場合、自動リダイレクトはチャネルの既定ロケールとして指定されたロケールの URL を使用します。

## <a name="save-customer-site-preferences"></a>顧客サイトの基本設定の保存

Commerce サイト ビルダーで **地域リダイレクト機能の有効化** 設定がオンになっている場合、地域リダイレクトは顧客のサイト基本設定を保存します。 国/地域の選択ダイアログ ボックスで推奨 URL を選択した顧客がそのサイトに移動する前に、選択した URL は、顧客が現在いるドメインの **\_msdyn365\_\_\_site\_** Cookie に書き込まれます。 次に、顧客が以前に国/地域の選択ダイアログ ボックスを表示する元となった URL を要求すると、顧客は自動的に優先サイトにリダイレクトされます。

また、[サイト セレクター モジュール](site-selector.md)も、顧客のサイト選択を **\_msdyn365\_\_\_site\_** Cookie に書き込みます。 顧客が優先サイトを変更できるよう、サイト セレクター モジュールをコンフィギュレーションすることをお勧めします。 地域リダイレクト ロジックは、顧客がサイト セレクター モジュールで選択するサイトを考慮します。

## <a name="additional-resources"></a>追加リソース

[サイト セレクター モジュール](site-selector.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]