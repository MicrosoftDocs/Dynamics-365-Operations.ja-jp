---
title: ソーシャル共有モジュール
description: このトピックでは、ソーシャル共有モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0fd81aa1f4b1358528f0135c1334dc7b4ac4461f
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761404"
---
# <a name="social-share-module"></a>ソーシャル共有モジュール

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、ソーシャル共有モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。

## <a name="overview"></a>概要

ソーシャル共有モジュールを使用すると、ユーザーは E コマース サイト ページの URL を Facebook、Twitter、Pinterest、LinkedIn などのソーシャルメディアで共有することができます。 サイトページの URL は、メールを使用して共有することもできます。 ソーシャル共有モジュールは、製品の情報共有でユーザーを支援するために、製品の詳細ページ (PDF) 上で一般に使用されます。

各ソーシャル共有モジュールは、ソーシャル共有項目モジュールのコンテナーです。 個々のソーシャル共有項目モジュールは、特定のソーシャル メディア サイトを参照するようにコンフィギュレーションできます。 Facebook、Twitter、LinkedIn、メールとの統合は、標準ではサポートされていません。 サイト ユーザーがソーシャルメディア シンボルを選択すると、それぞれのソーシャルメディア サイトに対して HTML iFrame が起動されます。 iFrame 内では、ユーザーは自分が表示していたページコンテンツにサインインして投稿することができます。

各ソーシャルメディア プラットフォームで cookie が追跡される可能性があるため、このモジュールでは、サイトユーザーに対して cookie の同意を通知するメッセージを受け入れるように要求します。 Cookie の同意が受け入れられない場合、このモジュールはページで非表示になります。 詳細については、[Cookie に関するコンプライアンス](cookie-compliance.md) を参照してください。

次の図は、製品の詳細ページで使用されるソーシャル共有モジュールの例を示しています。

![ソーシャル共有モジュールの例](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>ソーシャル共有モジュールのプロパティ

| プロパティ名             | 先頭値                 | 説明 |
|---------------------------|-----------------------|-------------|
| キャプション                  | テキスト | このプロパティは、モジュールのキャプションを指定します。 |
| 方向 | **水平** または **垂直**  | このプロパティは、ソーシャルメディア項目のレイアウトの方向を定義します。 |

## <a name="social-share-item-module-properties"></a>ソーシャル共有項目モジュールのプロパティ
| プロパティ名             | 先頭値                 | 説明 |
|---------------------------|-----------------------|-------------|
| ソーシャル メディア              | **Facebook**、**Twitter** 、**Pinterest**、**LinkedIn** 、**メール** | ソーシャルメディア プラットフォームの一覧を含むドロップダウン メニュー。 |
| アイコン |画像    | この画像は、それぞれのソーシャルメディアに対して表示されます。 ベスト プラクティスとして、各プラットフォームに使用される推奨されるイメージについては、ソーシャルメディア プラットフォームの SDK を参照してください。 |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>ソーシャル共有モジュールを購入ボックス モジュールに追加する

ソーシャル共有モジュールを購入ボックス モジュールに追加するには、次の手順に従います。

1. Fabrikam サイトで、**ページ** を選択し、**DefaultPDP** ページを選択すると、製品の詳細ページが表示されます。 
1. **Buybox (必須)** スロットで、省略ボタン (**...**) を選択し、続いて **モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**ソーシャル共有** モジュールを選択して、**OK** を選択します。
1. **ソーシャル共有** スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**SocialShare** モジュールを選択して、**OK** を選択します。
1. **SocialShare** モジュールのプロパティ ウィンドウで、**方向** で **水平方向** を選択します。 必要に応じてキャプションを追加します。
1. **SocialShare** スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**SocialShareItem** モジュールを選択して、**OK** を選択します。
1. **SocialShareItem** モジュールのプロパティ ペインで、**ソーシャルメディア** から **Facebook** を選択します。
1. **SocialShareItem** モジュールのプロパティ ペインで、**アイコン** から **+ イメージの追加** を選択します。
1. **メディア ピッカー** ダイアログ ボックスで、Facebook のロゴ イメージを選択して、**OK** を選択します。 Facebook のロゴ イメージが表示されない場合は、**新しいメディア項目をアップロード** を選択してアップロードします。
1. 必要に応じて、追加の **SocialShareItem** モジュールを追加およびコンフィギュレーションし ます。
1. **保存** を選択し、 続いて**プレビュー** を選択してページをプレビューします。 このページには、ソーシャル共有モジュールが表示されます。
1. **編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。

## <a name="additional-resources"></a>追加リソース

[スタート キットの概要](starter-kit-overview.md)

[購入ボックス モジュール](add-buy-box.md)

[Cookie のコンプライアンス](cookie-compliance.md)
