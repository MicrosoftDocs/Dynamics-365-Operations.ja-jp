---
title: 共有可能かつセキュリティで保護された、URL (ディープ リンク ) を作成
description: フォームおよびレコードへの共有可能かつセキュリティで保護された URL を作成する方法について説明します。
author: josaw1
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 24321
ms.assetid: 3e49f8eb-d9a8-418c-a73d-687da4ca0c96
ms.openlocfilehash: ae3e861ca64c8b245d255865f8035e64df83517f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275325"
---
# <a name="create-shareable-secured-urls-deep-links"></a>共有可能かつセキュリティで保護された、URL (ディープ リンク ) を作成

[!include [banner](../includes/banner.md)]

フォームおよびレコードへの共有可能かつセキュリティで保護された URL を作成する方法について説明します。

## <a name="overview"></a>概要

URL ジェネレータにより、開発者はルート移動可能な特定のフォームへの共有可能およびセキュリティ保護される URL (ディープ リンクとも呼ばれる) を作成できます。 オプションのデータ コンテキストをフォームに渡すと、フォームを開いた場合にフィルターや固有のデータを表示することができます。 URL ジェネレーターにより、レポート、電子メール、および外部アプリケーションへのリンクの埋め込みなどのシナリオが可能になるため、生成されたリンクを使用して移動するだけで、指定されたフォームやデータを迅速かつ容易に見つけることができます。

### <a name="purpose"></a>目的

-   指定されたインスタンスでのルート移動可能なフォームに移動するために使用できる URL を生成する開発者を支援します。
-   必要に応じて、指定されたフォームに移動した際に表示されるデータ コンテキストを指定する開発者を支援します。
-   ユーザーが、インターネットにアクセスできる任意のブラウザーから生成された URL を共有、保存、およびアクセスできるよう支援します。
-   システム、フォーム、またはデータへの不正アクセスを防ぐために URL を保護します。
-   機密性の高いデータまたは改ざんの影響を防ぐために URL を保護します。

## <a name="security"></a>セキュリティ
### <a name="site-access"></a>サイト アクセス

ドメイン/クライアントへのアクセスは、既存のログインおよびSSL メカニズムを通じて制御されます。

### <a name="form-access"></a>フォーム アクセス
メニュー項目はセキュリティが施工されているエントリ ポイントなので、フォームへのアクセスはメニュー項目によって制御されます。 ユーザーがアクセス権を持たないメニュー項目を含む URL を使用して移動する場合、メニュー項目のセキュリティにより、フォームが開かれなくなります。 ユーザーは、フォームを開くために必要な権限を持っていないことを示すメッセージを受け取ります。 ディープ リンクは、ルート ナビゲーションを許可するメニュー項目に対してのみ機能することに注意してください。

### <a name="data-access"></a>データ アクセス

データへのアクセスは、既存のフォーム レベルのクエリによって制御されます。 生成された URL を使用してフォームが開かれているとき、そのフォームは既存のフォーム レベルのクエリを実行します。これにより、データへのユーザーのアクセスが制限されます。 生成された URL で指定されたデータ コンテキストは、これらのフォーム レベルのクエリが適用された後に消費され、ユーザーに表示されるデータをさらにフィルタリングする場合にのみ発生します。 つまり、生成された URL は多くても 1 つのフォームを開いて、フォーム レベルのクエリに基づいてフォームがユーザーに表示するデータすべてを表示できます。 生成された URL には、生成された URL を使用していない場合にフォームでアクセスできないデータへのアクセスをユーザーに与えることはできません。

## <a name="usage"></a>用途
URL ジェネレーターは、次の名前空間の下の X++ からアクセス可能な .NET ライブラリです。

```xpp
Microsoft.Dynamics.AX.Framework.Utilities.UrlHelper.UrlGenerator
```

#### <a name="requirements"></a>必要量

URL ジェネレーターは、アクティブなユーザー セッションまたはバッチ処理で、AOS 上で実行されているコードから使用する必要があります。 この要件は、URL を生成するインスタンスに固有の暗号化によるセキュリティで保護することができます。 少なくとも、作業 URL を生成するために次の情報を指定して URL ジェネレータに渡す必要があります。

-   **ホスト URL**
    -   インスタンスの Web ルートの URL。 例: `https://ax.dynamics.contoso.com/`
-   **メニュー項目の表示** の AOT 名
    -   フォームを開くために使用するメニュー項目の表示。
-   **パーティション**
    -   要求に使用するパーティション。
-   **会社**
    -   要求に使用する会社。

#### <a name="example"></a>例

```xpp
// gets the generator instance
var generator     = new Microsoft.Dynamics.AX.Framework.Utilities.UrlHelper.UrlGenerator();
var currentHost   = new System.Uri(UrlUtility::getUrl());
generator.HostUrl = currentHost.GetLeftPart(System.UriPartial::Authority);
generator.Company = curext();
generator.MenuItemName = <menu item name>;
generator.Partition = getCurrentPartition(); 

// repeat this segment for each datasource to filter
var requestQueryParameterCollection = generator.RequestQueryParameterCollection;
requestQueryParameterCollection.AddRequestQueryParameter(
    <datasource name>,
    <field1>, <value1>,
    <field2>, <value2>,
    <field3>, <value3>,
    <field4>, <value4>,
    <field5>, <value5>
);

System.Uri fullURI = generator.GenerateFullUrl();

// to get the encoded URI, use the following code
fullURI.AbsoluteUri
```





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
