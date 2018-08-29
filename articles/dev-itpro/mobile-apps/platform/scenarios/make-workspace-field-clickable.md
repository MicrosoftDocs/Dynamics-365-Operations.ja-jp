---
title: "モバイル アプリ ページのフィールドをクリック可能にする"
description: "このトピックでは、モバイル アプリ ページのフィールドをカスタマイズして、メール アドレス、電話番号、または URL として表示する方法について説明します。"
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: 
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: c34c6217146c416237c1ca866dd5a5498abed5bb
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="make-fields-on-mobile-app-pages-clickable"></a>モバイル アプリ ページのフィールドをクリック可能にする

[!include [banner](../../../includes/banner.md)]

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
> IOS では、URL の完了 (つまり、<strong>http</strong> などのプロトコルで始まる URL) を指定する必要があります。 それ以外の場合、URL はブラウザーで開かれません。 www.microsoft.com などの URL は機能しません。 代わりに、URL は `http://www.microsoft.com` で指定される必要があります。

## <a name="example"></a>例
この例では、顧客の電子メール アドレスと電話番号フィールドを、適切な iOS アプリケーションでクリックして開くことができるように設定する方法を示します。

フィールドをカスタマイズする前に、次のイメージに示すように、フィールドをクリックすることはできません。

![変更される前の、顧客の詳細ページ](media/workspace-api/FieldAsURLOriginal.png)

フィールドがリンクであることを指定するには、これらの手順に従います。

1. **appInit** メソッドに次の明細行を追加します。 **configureControl** メソッドを呼び出して、ページ名とコントロール名を渡します。 次に、コントロールの **LinkType** 値を指定します。 次の値がサポートされています: **電話**、**電子メール**、および **URL**。

    ```
    metadataService.configureControl('PageName', 'ControlName', { LinkType: 'Telephone' });
    metadataService.configureControl('PageName', ' ControlName ', { LinkType: 'Email' });
    metadataService.configureControl('PageName', ' ControlName ', { LinkType: 'Url' });
    ```

2. モバイル アプリ デザイナーを使用して、更新されたビジネス ロジック ファイルをアップロードします。
3. モバイル クライアントでワークスペース メタデータを更新します。

フィールドはリンクとして表示されるようになりました。

![変更後の顧客詳細ページ](media/workspace-api/FieldAsURLFinal.png)

