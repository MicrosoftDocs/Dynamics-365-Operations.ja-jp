---
title: モバイル アプリ ページのフィールドをクリック可能にする
description: この記事では、モバイル アプリ ページのフィールドをカスタマイズして、メール アドレス、電話番号、または URL として表示する方法について説明します。
author: jasongre
ms.date: 05/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.custom: 255544
ms.assetid: ''
ms.openlocfilehash: 63822e153d654189e11648d1ab48e3580fe048b2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288669"
---
# <a name="make-fields-on-mobile-app-pages-clickable"></a>モバイル アプリ ページのフィールドをクリック可能にする

[!include [banner](../../../includes/banner.md)]
[!include [mobile app deprecated](../../../includes/mobile-app-deprecation-banner.md)]

モバイル アプリ ページのフィールドは、電子メール アドレス、電話番号、または URL として表示されるようにカスタマイズできます。

## <a name="email-field"></a>電子メール フィールド
ビジネス ロジックを使用することにより、フィールドを電子メール アドレス フィールドとしてマークすることができます。 ユーザーがフィールドをクリックすると、規定のモバイル メール アプリが起動し、フィールド値がアプリにメール アドレスとして表示されます。

## <a name="phone-field"></a>電話番号フィールド
ビジネス ロジックを使用することにより、フィールドを電話番号フィールドとしてマークすることができます。 ユーザーがフィールドをクリックすると、モバイル ダイヤラー アプリが起動し、フィールド値がアプリに電話番号として表示されます。

> [!NOTE]
> IOS では、電話番号が無効な場合、携帯電話のダイヤラー アプリが発生しない可能性があります。

## <a name="url-field"></a>URL フィールド
ビジネス ロジックを使用することにより、フィールドを URL フィールドとしてマークすることができます。 ユーザーがフィールドをクリックすると、規定のモバイル ブラウザーに URL が開き、アドレス バーにフィールド値が表示されます。

> [!NOTE]
> iOS では完全な URL (つまり、<strong>https</strong> などのプロトコルで始まる URL) を指定する必要があります。 それ以外の場合、URL はブラウザーで開かれません。 `www.microsoft.com` などの URL は機能しません。 代わりに、URL は `https://www.microsoft.com` で指定される必要があります。

## <a name="example"></a>例
この例では、顧客の電子メール アドレスと電話番号フィールドを、適切な iOS アプリケーションでクリックして開くことができるように設定する方法を示します。

フィールドをカスタマイズする前に、次のイメージに示すように、フィールドをクリックすることはできません。

![変更される前の、顧客の詳細ページ。](media/workspace-api/FieldAsURLOriginal.png)

フィールドがリンクであることを指定するには、これらの手順に従います。

1. **appInit** メソッドに次の明細行を追加します。 **configureControl** メソッドを呼び出して、ページ名とコントロール名を渡します。 次に、コントロールの **LinkType** 値を指定します。 次の値がサポートされています: **電話**、**電子メール**、および **URL**。

    ```xpp
    metadataService.configureControl('PageName', 'ControlName', { LinkType: 'Telephone' });
    metadataService.configureControl('PageName', ' ControlName ', { LinkType: 'Email' });
    metadataService.configureControl('PageName', ' ControlName ', { LinkType: 'Url' });
    ```

2. モバイル アプリ デザイナーを使用して、更新されたビジネス ロジック ファイルをアップロードします。
3. モバイル クライアントでワークスペース メタデータを更新します。

フィールドはリンクとして表示されるようになりました。

![変更後の顧客詳細ページ。](media/workspace-api/FieldAsURLFinal.png)


[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
