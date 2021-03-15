---
title: 顧客ポータルをカスタマイズして使用する
description: このトピックでは、顧客ポータルをシステムに追加した後でカスタマイズする方法について説明します。
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 1e491100bc24718b8e5bc0f62de241835787f7ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980859"
---
# <a name="customize-and-use-the-customer-portal"></a>顧客ポータルをカスタマイズして使用する

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、顧客ポータルで使用できるさまざまなページについて説明します。 ここでは、ページの機能とカスタマイズ方法について説明します。

顧客 ポータルでは、既成 の Web ページとアクションが用意されています。 次のサイトマップは、これら Web ページとアクションの概要と、アクションを実行できるロールを示しています。

![顧客ポータルのサイトマップ](media/customer-portal-site-map.png "顧客ポータルのサイトマップ")

## <a name="typical-customizations"></a>一般的なカスタマイズ

次のトピックでは、Power Apps ポータルの基本とポータルのカスタマイズ方法について説明し ます。

- [テンプレートで作業する](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) - このトピックでは、Power Apps ポータルの機能概要と、ポータルを簡単にカスタマイズする方法を示します。
- [ポータル コンテンツの管理](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) - このトピックでは、ポータルに表示されるコンテンツの管理方法とカスタマイズする方法について説明します。
- [編集 CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) - このトピックでは、ポータルのユーザー インターフェイス (UI) に対してさらに複雑なカスタマイズを行うことができます。
- [ポータルのテーマを作成する](https://docs.microsoft.com/dynamics365/portals/create-theme) - このトピックは、ポータルの UI のテーマを作成する際に役立ちます。
- [ポータルのコンテンツを簡単に作成して公開する](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) - このトピックでは、ポータルで使用する基となるデータとテーブルの管理について説明します。
- [ポータルで使用する連絡先の構成](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) - このトピックでは、ユーザー ロールの作成とカスタマイズの方法、および Power Apps ポータルにおけるセキュリティと認証機能について説明します。
- [ポータルでのテーブル フォームと Web フォームのメモの構成](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) - このトピックでは、ドキュメントと追加のストレージをポータルに追加する方法について説明します。
- [ポータル Web サイトのエラー処理 ](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) - このトピックでは、ポータルのエラーログを表示して Microsoft Azure Blob ストレージ アカウントに保管する方法について説明し ます。

## <a name="customize-the-order-creation-process"></a>注文作成プロセスのカスタマイズ

ユーザーが顧客ポータルを使用して注文を送信すると、対応する Dynamics 365 Supply Chain Management 環境に注文が自動的に同期されます。 ユーザーは外部の顧客であるため、必要な情報の一部は、意図的に非表示となっています。 この情報は、フォームの送信時に自動的に入力されます。

ここでは、連絡先を設定してエラーを回避する方法について説明します。 自動的に設定されるフィールドと、必要に応じてこれらフィールドの値を変更する方法について説明します。

### <a name="the-out-of-box-order-creation-process"></a>既成の注文作成プロセス

ここでは、顧客ポータルから注文を送信する標準的な手順について説明します。

1. ホーム ページの **注文の作成** タイルを選択して、**注文の作成** ウィザードを開きます。
1. **注文情報** ページで、次のフィールドを設定します :

    - **入荷希望日** - 配送日を指定します。
    - **配送先住所** - 注文の配送先の住所を入力します。
    - **会社** - 顧客の会社名を選択します。 このフィールドは、管理者以外のユーザーには自動的に設定されます。
    - **要求番号** - 注文の要求番号を入力します。 このフィールドは必須ではありません。
    - **配送先の国/地域** - 品目が配送される国または地域を入力します。 このフィールドは、管理者以外のユーザーには自動的に設定されます。

    ![注文情報のページ](media/customer-portal-order-information.png "注文情報のページ")

1. **次へ** を選択します。
1. **品目** ページで、**品目の追加** を選択します。

    ![品目ページ](media/customer-portal-items.png "品目ページ")

1. **品目情報** のダイアログ ボックスで、次のフィールドを設定します :

    - **製品名** - 注文に追加する製品を検索して選択します。
    - **数量** - 選択した製品のの数量を入力します。
    - **単位** - 測定単位を指定します ( **個**、**kg**、**箱** など )。
    - **見積正味金額** - この値は、選択された単位の品目の見積価格 × 数量で計算されます。

    ![品目情報のダイアログ ボックスの追加](media/customer-portal-item-information.png "品目情報のダイアログ ボックスの追加")

1. **送信** を選択して、品目を注文に追加します。
1. 手順 4 から 6 を繰り返して、注文するすべての品目を追加します。
1. 品目の追加の完了後は、**品目** ページで **次へ** を選択します。
1. **注文情報** ページに注文の概要が表示されます。 注文内容と配送の詳細を確認します。 すべてが正しい場合は、**送信** を選択して注文を送信します。

    ![注文情報のページ](media/customer-portal-order-submit.png "注文情報のページ")

### <a name="standard-data-setup"></a>標準データの設定

円滑なユーザーエクスペリエンスを実現する目的でに、顧客ポータルでは、いくつかの必須フィールドの値が自動的に入力されます。 これらの値は、注文を送信する顧客の連絡先レコードの情報に基づいています。

顧客ポータルを使用して注文を送信する顧客の [連絡先行](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) には、以下の必須フィールドに値を指定する必要があります。 それ以外の場合は、エラーが発生します。

- **会社** - 注文が属するエンティティを選択します
- **見込み顧客** - 選択した注文に関連付けられている顧客 ID
- **価格リスト** - 顧客のカスタム価格リスト
- **通貨** - 価格に適用する通貨
- **配送先の国/地域** - 品目を配送する国または地域

販売注文テーブルには、次のフィールドが自動的に設定されます:

- **言語** - 注文の言語 (既定では、この値は連絡先レコードから取得されます)
- **配送先の国/地域** : 品目の配送先の国または地域 (既定では、この値は連絡先レコードから取得されます)
- **連絡担当者** - 注文に関する情報の問い合わせの担当ユーザー (既定では、この値は連絡先レコードから取得されます)
- **会社** - 注文が属するエンティティ (既定では、この値は連絡先レコードから取得されます)
- **見込み顧客** – 注文に関連付けられている顧客 ID (既定では、この値は連絡先レコードから取得されます)
- **請求書顧客** - 注文に関連付けられている顧客 ID (既定では、この値は連絡先レコードから取得されます)
- **販売注文の名前**- 販売注文の名前 (既定値は **販売注文** です)
- **通貨** - 注文の通貨 (既定では、この値は連絡先レコードから取得されます)
- **価格表** - 顧客向けのカスタム価格リスト (既定では、連絡先レコードから取得されます)
- **配送先住所の説明** - 販売注文の配送先住所 (既定値は **配送先住所の説明** です)

### <a name="modify-the-order-creation-process"></a>注文作成プロセスの修正

基本の注文作成プロセスを変更していない場合は、顧客ポータルの外観と UI を自由に変更できます。 注文の作成プロセスを変更する場合は、いくつかの点に注意する必要があります。

デュアル書き込みにて販売注文を作成する必要があるため、Microsoft Dataverse の販売注文テーブルでは以下の列を削除しないでください:

- **会社** - 注文が属するエンティティを選択します
- **名前** - 販売注文の名前
- **通貨** - 価格に適用する通貨
- **価格リスト** - 顧客のカスタム価格リスト
- **配送先の国/地域** - 品目を配送する国または地域
- **見込み顧客** - 選択した注文に関連付けられている顧客 ID
- **言語** - 注文で使用する言語 (通常は、潜在顧客の使用する言語です)
- **配送先住所の説明** - 販売注文の配送先住所です

品目には、以下の列が必須です:

- **製品** - 注文する製品
- **数量** - 選択した製品のの数量
- **単位** - 測定単位 ( **個**、**kg**、**箱** など )
- **出荷先の国/地域** 出荷先の国または地域
- **配送先住所の説明** - 注文の配送先住所

顧客ポータルでは、これらのすべての列の値が必ず送信されるようにする必要があります。

ページに列を追加あるいは削除するには、[データ入力を効率化するための簡易作成フォームを作成または編集する](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms) を参照してください。

列のプリセット方法とページ保存時に値の設定方法を変更する場合は、Power Apps ポータル ドキュメントで次の情報を参照してください:

- [フィールドの事前入力](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [保存時に値を設定する](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>ホームページのカスタマイズ

顧客ポータルのすべてのコントロールには、Power Apps ポータル コントロールが実装されています。 これらをカスタマイズするには、Power Apps ポータル ドキュメントで[ページを作成する](https://docs.microsoft.com/powerapps/maker/portals/compose-page) に記載の手順に従ってください。

ホームページのタイル作成には、顧客ポータルのテンプレートに含まれるカスタム コントロールのみが使用されます。

![ホームページのタイル](media/customer-portal-home-page-tiles.png "ホームページのタイル")

タイルを変更するには、次の手順を実行します。

1. [ポータル管理アプリ](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal)を開きます。
1. 左のナビゲーション ウィンドウで、**ページ テンプレート** を選択します。

    ![ポータル管理ナビゲーション ウィンドウ](media/customer-portal-nav.png "ポータル管理ナビゲーション ウィンドウ")

1. **ホーム** という名前のページ テンプレートを選択します。
1. **Web テンプレート** フィールドで、**ホーム** リンクを選択して、そのページのソース コードを開きます。

    ![Web テンプレートのフィールド](media/customer-portal-web-template.png "Web テンプレートのフィールド")

1. ホーム ページのすべてのソース コードが表示され、必要に応じて変更できるようになります。

## <a name="resources"></a>リソース

顧客ポータルを設定、カスタマイズする方法の詳細については、次のリソースを参照してください :

- [Power Apps ポータル ドキュメント](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [デュアル書き込みのドキュメント](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [ポータルのライフ サイクルについて](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [ポータルのアップグレード](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [ポータルの構成の移行](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [ソリューションのライフサイクル管理 : Dynamics 365 for Customer Engagement アプリ](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]