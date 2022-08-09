---
title: robots.txt ファイルの追加または更新
description: この記事では、Microsoft Dynamics 365 Commerce でホストされた各ドメインの robots.txt ファイルを作成、編集、アップロード、および検証する方法について説明します。
author: mssle
ms.date: 07/08/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: sheaton
ms.search.validFrom: 2021-09-20
ms.openlocfilehash: 6d1bad567cc70d259e15a27683ef58cf31624a08
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130276"
---
# <a name="add-or-update-a-robotstxt-file"></a>robots.txt ファイルの追加または更新

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce でホストされた各ドメインの robots.txt ファイルを作成、編集、アップロード、および検証する方法について説明します。

検索リンクによるサイトの予期しない、または方向性のないクロールにより、「404 ページが見つかりません」というエラーが多く引き起こす可能性があります。 これらのエラーは、サイトが存在しないページに関する多くの要求に応答する際、パフォーマンス上に影響を与える可能性があります。 この問題を解決するには、ドメインに常に最新の情報と有効な robots.txt ファイルを使用して、サイト上の関連するページのみを検索するように Web クローラに指示する必要があります。

## <a name="applies-to"></a>適用先

この記事は、次の構成に適用されます。

- **バージョン:** Commerce 10.0.16 またはそれ以降
- **コンポーネント:** 企業とコンシューマー (B2C) または企業間 (B2B)
- **機能領域:** Commerce Web サイト パフォーマンス

## <a name="prerequisites"></a>必要条件

- Commerce インスタンスの[システムの管理者](../manage-ecommerce-users-roles.md#system-administrator-role) です。
- 状況に応じて、コンピュータに robots.txt ファイルを作成、またはコピーをダウンロードしました。

    - 使用しているドメインの robots.txt ファイルをまだアップロードしていない場合は、[ロボット除外標準](https://www.robotstxt.org/orig.html) に従って、コンピュータに新しいファイルを作成してください。 出発点として、この記事の[サンプル robots.txt サンプル](#sample-robotstxt-file-contents) を後で使用します。
    - 使用しているドメインの robots.txt ファイルをまだアップロードしていない場合は、既存ファイルの[ダウンロード](../manage-robots-txt-files.md#download-a-robotstxt-file) を実行します。

## <a name="steps-to-complete"></a>完了までのステップ

robots.txt ファイルを編集およびアップロードするには、次のステップを実行します。

1. robots.txt ファイルのローカル コピーを開きます。
1. すべての **不許可** エントリを次の[サンプル robots.txt ファイル](#sample-robotstxt-file-contents) に含めるよう、ファイルを編集します。
1. ファイルが正しく[ロボット除外標準](https://www.robotstxt.org/orig.html) に従って書式設定されているか確認します。
1. [robots.txt ファイルをアップロード](../manage-robots-txt-files.md#upload-a-robotstxt-file) の手順に従い、ファイルをサイトにアップロードします。

### <a name="sample-robotstxt-file-contents"></a>サンプル robots.txt ファイルの内容

```Plaintext
User-agent: *
Disallow: /signin
Disallow: /cart
Disallow: /*refiners=
Disallow: /*sorting=
Disallow: /*search?
Disallow: /*search=
Disallow: /*.woff
Disallow: /*.woff2
Disallow: /*skip=
```

## <a name="validate"></a>検証

ファイルが追加されているか、次の方法を使用して検証します:

- **説明または目的:** ドメインで robots.txt ファイルが使用できるか検証します。
- **実行するためのステップ:** Web ブラウザで、**\<your\_domain\>/robots.txt** のページを開きます。
- **合格結果:** robots.txt ファイルを正常に表示できます。

## <a name="additional-resources"></a>追加リソース

[robots.txt ファイルの管理](../manage-robots-txt-files.md)

[システム管理者ロール](../manage-ecommerce-users-roles.md#system-administrator-role)
