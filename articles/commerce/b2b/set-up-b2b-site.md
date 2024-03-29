---
title: B2B eコマース サイトの設定
description: この記事では、Microsoft Dynamics 365 Commerce の企業間 (B2B) eコマース サイトを設定する方法について説明します。
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: 162a8d4b51f10f409b77e1ced4c63c1a69a3b1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281127"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>B2B eコマース サイトの設定

[!include [banner](../../includes/banner.md)]

企業間 (B2B) eコマース サイトは、B2B ユーザーのワークフローを最適化するいくつかの重要な機能を提供します。 この記事では、Microsoft Dynamics 365 Commerce の B2B の eコマース サイトを設定する方法について説明します。 B2B に特化したシナリオを有効にするにあたり、構成する必要があるモジュールとサイト設定が示されています。

## <a name="prerequisites"></a>必要条件

- B2B の eコマース サイトを設定するには、この記事で説明するように、Commerce headquarters の特定の機能を有効にして構成する必要があります。
- 製品を見つける、製品の詳細ページ、カート、チェックアウトなどのコア エクスペリエンスには、企業間 (B2C) の eコマース サイトに使用されているものと同じモジュールが使用されます。 サイト作成者は、Dynamics 365 Commerce が対応するすべてのモジュールについてよく理解している必要があります。 詳細については、[モジュール ライブラリの概要](../starter-kit-overview.md)を参照してください。
- この記事では、サイト作成者が eコマース サイトの B2B 機能を有効にできるように、Commerce のサイト ビルダー、テンプレート、フラグメント、ページの基本を理解していることを前提としています。

## <a name="site-level-settings"></a>サイト レベルの設定

サイト ビルダーのサイト レベルの設定には、**サイト設定 \> 拡張機能** でアクセスできます。 次の 2 つのサイト レベル設定は、B2B のシナリオに適用されます。

- **顧客勘定での支払いを有効にする** - このプロパティでは、ユーザーが顧客勘定を使用して注文に対する支払を行います。 使用可能な値は、**B2B 顧客に有効化**、**B2C 顧客に有効化**、**すべての顧客に有効化**、**べての顧客に無効化** です。 B2B サイトが顧客勘定に対応している場合は、**B2B 顧客に有効化** を選択する必要があります。
- **注文数量制限を有効化** - このプロパティを使用すると、製品またはカテゴリごとに注文できる品目の数を制限できます。 使用可能な値は、**B2B 顧客に有効化**、**B2C 顧客に有効化**、**すべての顧客に有効化**、**べての顧客に無効化** です。

> [!NOTE]
> モジュール ライブラリの最新バージョンにアップグレードする場合は、先に説明したサイト設定がご利用の環境で利用できるようにするために、追加のステップを踏む必要があります。 詳細については、 [app.settings.json ファイルを更新する](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください 。

## <a name="create-business-partner-sign-up-pages"></a>ビジネス パートナーの新規登録ページを作成する

ビジネスパートナーになるためには、まずビジネス パートナーのリクエストを提出する必要があります。 B2B のホームページには、ビジネス パートナーのリクエスト ページへのリンクが掲載されており、ユーザーがプロセスを開始できるようになっています。 ユーザーがビジネス パートナーの要求を送信すると、要求が送信された旨の確認がユーザーに送信されます。 

### <a name="create-a-business-partner-request-page"></a>ビジネス パートナーのリクエストページを作成する

ビジネス パートナーのリクエスト ページ上の **パートナーの新規登録** モジュールは、ユーザーのリクエストを開始してビジネス パートナー になる際に使用されます。 このモジュールを使用すると、新規登録のプロセスに必要なユーザー情報を収集できます。 また、**ビジネス アカウント のアドレス** モジュールを使用してユーザーの住所を取得します。

サイト ビルダーのビジネス パートナー要求ページを設定、構成するには次の手順に従います。

1. **新規登録** という名前のテンプレート を作成します。 このテンプレートには、次のモジュールが含まれている必要があります :

    - パートナーの新規登録
    - 階層リンク
    - 表題
    - フッター
    - コンテンツ ブロック
    - テキスト ブロック
    - 製品コレクション

1. **新規登録** のテンプレート を使用して、 **ビジネス パートナーのリクエスト要求** という名前のページを作成します。
1. **ヘッダー** スロット で、サイトのヘッダーで構成されたヘッダーフラグメントを追加します。
1. **フッター** スロット で、サイトのフッターで構成されたフッター フラグメントを追加します。
1. **メイン** スロットに **コンテナ** モジュールを追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。
1. **コンテナー** スロットで、**パンくず** モジュールを追加します。 モジュール プロパティ ウィンドウの **リンク** で、ホーム ページへのリンクを構成し、リンク テキストに **ホーム** と入力します。
1. **コンテナー** スロットで、**パンくず** モジュールの下に **パートナー新規登録** モジュールを追加します。 モジュール プロパティ ウィンドウの **ヘッダー** で 、**ビジネス パートナー になる** と入力します。
1. **パートナーの新規登録** スロットで、**ビジネス アカウント アドレス** モジュールを追加します。
1. **コンテナー** スロットで、**パートナーの新規登録** モジュールの下に **テキスト ブロック** モジュールを追加します。 ここでは、新規登録のプロセスに対していくつかの条件を定義できます。
1. **保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。
1. ページの URL を公開します。

### <a name="create-a-business-partner-request-confirmation-page"></a>ビジネス パートナーのリクエスト確認を作成する

ビジネス パートナーのリクエストが送信された後、送信を承認する確認ページがユーザーに表示されます。 

サイト ビルダーのビジネス パートナーの確認ページを設定、構成するには次の手順に従います。

1. 上記で作成した **新規登録** のテンプレート を使用して、 **ビジネス パートナーのリクエスト確認** という名前のページを作成します。
1. **ヘッダー** スロット で、サイトのヘッダーで構成されたヘッダーフラグメントを追加します。
1. **フッター** スロット で、サイトのフッターで構成されたフッター フラグメントを追加します。
1. **メイン** スロットに **コンテナ** モジュールを追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。
1. **コンテナー** スロットで、**コンテンツ ブロック** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**送信済みの要求** を入力します。 **リッチ テキスト** フィールドに、**リクエストが送信されました** と入力します。 **リンク** 配下に、ホーム ページへのリンクを構成し、リンク テキストに **買い物に戻る** と入力します。
1. さらに **コンテナー** モジュールを追加し、これに **製品コレクション** モジュールを追加します。
1. ページに表示したいレコメンデーション、またはカテゴリーのリストを使用して、**製品コレクション** のモジュールを設定します。
1. **保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。
1. ページの URL を公開します。

サイト ビルダーでリクエスト確認ページへのリンクを追加するには次の手順に従います。

1. 上記で作成した **ビジネス パートナーのリクエスト** ページに移動し、**編集** を選択します。 
1. **パートナーの新規登録** モジュール スロットを選択します。 **新規登録確認ページへのリンク** 配下のプロパティ ペインで、上記で作成したビジネス パートナーのリクエスト ページへのリンクを構成します。 
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>ビジネス パートナーのリクエストののリンクをホーム ページに追加する

ビジネス パートナーから新規登リクエスト、および確認ページが作成された後は、ホーム ページのリンクを通じて登録ページにアクセスできる必要があります。 このタスクを実行するには、ホーム ページの任意の **コンテンツ ブロック** モジュールにリンクを追加します。

ホームページにビジネス パートナーのリクエストのリンクを追加するには、次の手順に従います。

1. ご利用のサイトのホームページに移動し、**編集** を選択します。
1. **コンテンツ ブロック** モジュール スロットを選択します。 **リンク** 配下の、モジュール プロパティ ペインで、上記で作成したビジネス パートナーのリクエスト ページへのリンクを構成し、リンク テキストに **ビジネスパートナーに新規登録する**、あるいは類似するテキストを入力します。 必要に応じて画像を追加します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。

## <a name="account-management-landing-page"></a>アカウント管理ランディング ページ

アカウント管理のランディング ページには、B2B と B2C の両方の eコマース サイトに必要なすべてのアカウント管理情報が含まれます。 このページは、サインインしたユーザーだけに表示されます。

サイト ビルダーの B2B アカウント管理のランディング ページを作成・構成するには、次の手順に従います。

1. **アカウント管理** という名前のテンプレート を作成します。 このテンプレートには、次のモジュールが含まれている必要があります :

    - 表題
    - フッター
    - 階層リンク
    - アカウントのようこそタイル
    - アカウント汎用タイル
    - アカウント アドレス タイル
    - アカウント ウィッシュリスト タイトル
    - アカウント アドレス タイル
    - アカウント ロイヤルティ タイル
    - アカウント顧客残高タイル
    - アカウント注文テンプレート タイル
    - 組織ユーザー
    - ビジネス組織リスト
    - 顧客アカウント残高
    - 注文テンプレートの明細
    - 注文テンプレートのリスト
    - アカウント請求書タイル
    - 請求書リスト
    - 請求書の詳細

1. **アカウント管理** のテンプレートを使用して、**自分のアカウント** という名前のページを作成します。
1. **ヘッダー** スロット で、サイトのヘッダーで構成されたヘッダーフラグメントを追加します。
1. **フッター** スロット で、サイトのフッターで構成されたフッター フラグメントを追加します。
1. **メイン** スロットに **コンテナ** モジュールを追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。 
1. **コンテナー** スロットで、**パンくず** モジュールを追加します。 モジュール プロパティ ウィンドウの **リンク** で、ホーム ページへのリンクを構成し、リンク テキストに **ホーム** と入力します。
1. **コンテナー** スロットで、**ウェルカム タイル** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**ようこそ** を入力します。
1. 新しいページの **メイン** スロットで、さらに **コンテナ―** モジュール (**コンテナ―2**)を追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。 **表示される子** の値を **2** に設定します。 
1. **コンテナー2** スロットで、**アカウントの汎用タイル** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**プロファイル** を入力します。 **リンク** で、**プロファイル** ページへのリンクを構成します。 
1. **コンテナー2** スロットで、さらに **アカウントの汎用タイル** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**注文履歴** を入力します。 **リンク** で、注文履歴ページへのリンクを構成します。
1. **メイン** スロットで、さらに **コンテナ―** モジュール (**コンテナ―3**)を追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。 **表示される子** の値を **2** に設定します。 
1. **コンテナー3** スロットで、**アカウントのアドレス タイル** モジュールを追加します。 モジュール プロパティ ペインの **見出し** で、**マイ アドレス** を入力します。 **リンク** で、**マイ アドレス** ページへのリンクを構成します。 
1. **コンテナー3** スロットで、**アカウントのウィッシュ タイル** モジュールを追加します。 モジュール プロパティ ペインの **見出し** で、**マイ ウィッシュリスト** を入力します。 **リンク** で、**マイ ウィッシュリスト** ページへのリンクを構成します。
1. **メイン** スロットで、さらに **コンテナ―** モジュール (**コンテナ―4**)を追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。 **表示される子** の値を **2** に設定します。 
1. **コンテナー4** スロットで、**組織のユーザー** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**組織のユーザー** を入力します。 
1. **コンテナー4** スロットで、**アカウントの顧客残高タイル** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**アカウント クレジット** を入力します。 
1. **メイン** スロットで、さらに **コンテナ―** モジュール (**コンテナ―5**)を追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。 **表示される子** の値を **2** に設定します。 
1. **コンテナー5** モジュールで、**アカウントの注文テンプレート タイル** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**注文テンプレート** を入力します。 
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。

> [!NOTE] 
> 手順13 から 18 で追加したセクションは、B2B アカウントへのサインインが必要となるため、サイト ビルダーの 「見たとおりのものが結果に反映される」 (WYSIWIG) キャンバスには表示されません。

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>顧客残高ページとモジュールの作成・構成 

顧客アカウントは、注文への支払に使用できます。 顧客アカウントの利用可能残高は、ユーザーのアカウント管理ページから確認することができます。

### <a name="create-a-customer-balance-page"></a>顧客残高ページを作成する 

B2B にサインインしたユーザーが顧客残高を表示するには、顧客残高ページを作成する必要があります。 

サイト ビルダーで顧客残高ページを作成するには、次の手順を実行します。

1. 上記で作成した **アカウント管理** テンプレートを使用して **顧客の残高** という名前でページを作成します。
1. **ヘッダー** スロット で、サイトのヘッダーで構成されたヘッダーフラグメントを追加します。
1. **フッター** スロット で、サイトのフッターで構成されたフッター フラグメントを追加します。
1. **メイン** スロットで、さらに **コンテナ―** モジュール (**コンテナ―3**)を追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。 **表示される子** の値を **2** に設定します。
1. **コンテナー** スロットで、**パンくず** モジュールを追加します。 モジュール プロパティ ペインの **リンク** 配下で、アカウント管理ランディングページへのリンクを構成し、リンク テキストに **マイ アカウント** と入力します。
1. **コンテナー** スロットで、**顧客アカウントの残高** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**アカウントの残高** を入力します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。
1. ページの URL を公開します。
1. 上記で作成したアカウント管理ランディング ページ ( **マイ アカウント**) に移動します。
1. **アカウントの顧客残高タイル** モジュール のプロパティ ペインで 、顧客残高ページへのリンクを追加します。 
1. ページを保存してプ公開します。

以上で顧客の残高ページが作成されたため、ユーザーはアカウント管理のランディング ページからアクセスできるようになります。

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>顧客の残高を支払いに使用できるように精算ページを構成します

顧客残高を決済手段として利用できるようにするには、**顧客アカウント決済** モジュールが必要となります。 このモジュールを、支払い方法として精算ページに追加する必要があります。 精算ページの設定方法や、すべての支払い詳細を含む精算に必要となるモジュールについては、[精算モジュール](../add-checkout-module.md)を参照してください。

精算ページの構成後は、支払セクションに **顧客アカウントの支払** モジュールを追加し、ページを保存して公開する必要があります。 その後、B2Bユーザーは eコマース サイトにログインし、精算中に顧客が利用可能な残高を注文に適用できます。

さらに、**サイト ビルダー \> 拡張機能** で、**顧客勘定支払を有効にする** プロパティが **B2B 顧客に対して有効化** に設定されている必要があります。

## <a name="create-order-template-pages"></a>注文テンプレート ページを作成する

B2B の eコマースサイトには、注文テンプレート リストのページと注文テンプレート明細行ページの 2 つの注文テンプレート ページを設定できます。

注文テンプレートの一覧ページには、使用可能なすべての注文テンプレートの一覧が表示されます。 **注文テンプレート リスト** モジュールを使用して設定します。 注文テンプレートリスト ページでは、テンプレートを作成または削除し、テンプレートの品目をカートに追加できます。

注文テンプレート明細行ページには、注文テンプレートリスト ページで選択された注文テンプレートの詳細が表示されます。 **注文テンプレート明細行** モジュールを使用して設定します。 ユーザーが注文テンプレートの一覧ページでテンプレート名を選択すると、注文テンプレートの明細行ページが表示され、テンプレートの詳細が表示されます。 テンプレートの項目を表示、編集できます。

### <a name="create-an-order-templates-list-page"></a>注文テンプレート リストのページを作成する

サイト ビルダーで注文テンプレート リストのページを作成するには、次の手順を実行します。

1. 上記で作成した **アカウント管理** テンプレートを使用して **注文のテンプレート** という名前でページを作成します。
1. **ヘッダー** スロット で、サイトのヘッダーで構成されたヘッダーフラグメントを追加します。
1. **フッター** スロット で、サイトのフッターで構成されたフッター フラグメントを追加します。
1. **メイン** スロットに **コンテナ** モジュールを追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。
1. **コンテナー** スロットで、**パンくず** モジュールを追加します。 モジュール プロパティ ペインの **リンク** 配下で、アカウント管理ランディングページへのリンクを構成し、リンク テキストに **マイ アカウント** と入力します。
1. **コンテナー** スロットで、**注文テンプレート リスト** モジュールを追加します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。
1. ページの URL を公開します。
1. 上記で作成したアカウント管理ランディング ページ ( **マイ アカウント**) に移動します。
1. **リンク** の下にある、**アカウント注文テンプレート タイル** モジュールのプロパティ ペインで、上記で作成した注文テンプレート一覧ページへのリンクを設定します。
1. ページを保存してプ公開します。

以上で注文のテンプレートページが作成されたため、ユーザーはアカウント管理のランディング ページからアクセスできるようになります。

### <a name="create-an-order-template-lines-page"></a>注文テンプレート 明細行ページを作成する

サイト ビルダーで注文テンプレート明細行のページを作成するには、次の手順を実行します。

1. 上記で作成した **アカウント管理** テンプレートを使用して **注文のテンプレート明細行** という名前でページを作成します。
1. **ヘッダー** スロット で、サイトのヘッダーで構成されたヘッダーフラグメントを追加します。
1. **フッター** スロット で、サイトのフッターで構成されたフッター フラグメントを追加します。
1. **メイン** スロットに **コンテナ** モジュールを追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。
1. **コンテナー** スロットで、**パンくず** モジュールを追加します。 モジュール プロパティ ペインの **リンク** 配下で、アカウント管理ランディングページへのリンクを構成し、リンク テキストに **マイ アカウント** と入力します。
1. **コンテナー** スロットで、**注文テンプレート明細行** モジュールを追加します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。
1. ページの URL を公開します。

## <a name="onboard-business-partner-users"></a>ビジネス パートナーのユーザーをオンボードする

組織ユーザーページでは、ビジネスパートナー組織の管理者は、その組織から B2B eコマース サイトに追加のユーザーをオンボードすることができます。 **ビジネス組織のリスト** モジュールを使用して設定します。 管理者は組織ユーザーのページから、ユーザーの追加や削除、アカウント残高の定義、ユーザーのステートメントを要求することができます。

サイト ビルダーで組織ユーザーのページを作成するには、次の手順を実行します。

1. 上記で作成した **アカウント管理** テンプレートを使用して **組織ユーザー** という名前でページを作成します。
1. **ヘッダー** スロット で、サイトのヘッダーで構成されたヘッダーフラグメントを追加します。
1. **フッター** スロット で、サイトのフッターで構成されたフッター フラグメントを追加します。
1. **メイン** スロットに **コンテナ** モジュールを追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。
1. **コンテナー** スロットで、**パンくず** モジュールを追加します。 モジュール プロパティ ペインの **リンク** 配下で、アカウント管理ランディングページへのリンクを構成し、リンク テキストに **マイ アカウント** と入力します。
1. **コンテナー** スロットで、**組織のユーザー** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**組織のユーザー** を入力します。
1. **業務組織 リスト** モジュールのプロパティ ペインで、**テーブルの並べ替え** と **テーブルのページ設定** のプロパティを有効にします。 改ページ位置の自動修正のカウントを **5** に設定します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。
1. ページの URL を公開します。
1. 上記で作成したアカウント管理ランディング ページ ( **マイ アカウント**) に移動します。
1. **リンク** の下にある、**組織ユーザーのタイル** モジュールのプロパティ ペインで、上記で作成した組織ユーザー ページへのリンクを設定します。 
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。

## <a name="create-invoice-pages"></a>請求書ページの作成

請求書一覧のページには、使用可能なすべての請求書が表示されます。 **InvoicesList** モジュールを使用して設定します。 請求書リスト ページで、ユーザーは請求書の支払や要求を実行可能です。 

請求書の詳細ページには、請求書リスト ページで選択された請求書の詳細が表示されます。 **請求書の詳細** モジュールを使用して設定します。 ユーザーが請求書リスト ページで請求書 ID を選択すると、請求書の詳細ページが表示され、請求書の詳細が表示されます。

### <a name="create-an-invoices-list-page"></a>請求書リスト ページを作成する

サイト ビルダーで請求書リストのページを作成するには、次の手順を実行します。

1. 上記で作成した **アカウント管理** テンプレートを使用して **請求書リスト** という名前でページを作成します。
1. **ヘッダー** スロット で、サイトのヘッダーで構成されたヘッダーフラグメントを追加します。
1. **フッター** スロット で、サイトのフッターで構成されたフッター フラグメントを追加します。
1. **メイン** スロットに **コンテナ** モジュールを追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。
1. **コンテナー** スロットで、**パンくず** モジュールを追加します。 モジュール プロパティ ペインの **リンク** 配下で、アカウント管理ランディングページへのリンクを構成し、リンク テキストに **マイ アカウント** と入力します。
1. **コンテナー** スロットで、**InvoicesList** モジュールを追加します。 モジュール プロパティ ウィンドウの **見出し** で、**請求書** と入力します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。
1. ページの URL を公開します。
1. 上記で作成したアカウント管理ランディング ページ ( **マイ アカウント**) に移動します。
1. **リンク** の下にある、**アカウント請求書タイル** モジュールのプロパティ ペインで、上記で作成した請求書のリスト ページへのリンクを設定します。 
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。

### <a name="create-an-invoice-details-page"></a>請求書の詳細ページを作成する

サイト ビルダーで請求書の詳細ページを作成するには、次の手順を実行します。

1. 上記で作成した **アカウント管理** テンプレートを使用して **請求書の詳細** という名前でページを作成します。
1. **ヘッダー** スロット で、サイトのヘッダーで構成されたヘッダーフラグメントを追加します。
1. **フッター** スロット で、サイトのフッターで構成されたフッター フラグメントを追加します。
1. **メイン** スロットに **コンテナ** モジュールを追加します。 モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。
1. **コンテナー** スロットで、**パンくず** モジュールを追加します。 モジュール プロパティ ペインの **リンク** 配下で、アカウント管理ランディングページへのリンクを構成し、リンク テキストに **マイ アカウント** と入力します。 続いて、請求書リスト ページへのリンクを構成し、リンク テキストに **請求書リスト** と入力します。
1. **コンテナー** スロットで、**請求書の詳細** モジュールを追加します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。
1. ページの URL を公開します。

## <a name="add-a-quick-add-module-to-the-cart-page"></a>買い物カゴ ページへのクイック追加モジュールの追加

クイック追加モジュールは、品目 ID (最小在庫管理単位 \[SKU\] ID とも呼ばれる) を使用して、買い物カゴに複数の品目を簡単に追加する方法を提供します。 クイック追加モジュールがサイトの買い物カゴ ページに追加されます。

Commerce サイト ビルダーの買い物カゴ ページにクイック追加モジュールを追加するには、以下の手順に従います。

1. **テンプレート** に移動し、サイトの買い物カゴ ページ テンプレートを選択します。
1. **編集** を選択します。
1. **既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。
1. **コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**クイック追加** モジュールを選択して、**OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。
1. **ページ** に移動し、サイトの買い物カゴ ページを選択します。
1. **既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。
1. **コンテナー** モジュールのプロパティ ウィンドウの **幅** で、**全コンテナー** を選択します。
1. **コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**クイック追加** モジュールを選択して、**OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。

> [!NOTE] 
> クイック追加モジュールは、Commerce バージョン 10.0.17 リリース時点で使用できます。 古いバージョンの Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。 手順については、[SDK およびモジュール ライブラリの更新](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) を参照してください。

## <a name="add-a-bulk-purchase-module-to-a-product-details-page"></a>製品詳細ページに一括購入モジュールを追加する

商品詳細ページ (PDP) の一括購入モジュールは、購入者が複数のバリエーションの商品を素早くカートに入れることができるマトリック スベースのエクスペリエンスを提供します。 サイト ユーザーが同じ製品の複数のバリアントを注文する必要がある場合、これにより、商品の寸法の組み合わせを選択し、数量を定義し、そのバリアントをカートに入れ、さらに他の寸法の組み合わせでも同じ作業を繰り返す必要がなくなります。

Commerce サイト ビルダーの PDP に一括購入モジュールを追加するには、以下の手順で行います。

1. **テンプレート** に移動し、サイトの PDP テンプレートを選択します。
1. **編集** を選択します。
1. **既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。
1. **コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**一括購入** モジュールを選択し、続いて **OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。
1. **ページ** に移動し、サイトの PDP を選択します。
1. **既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。
1. **コンテナー** モジュールのプロパティ ウィンドウの **幅** で、**すべてのコンテナー** を選択します。
1. **コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**一括購入** モジュールを選択し、続いて **OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。

> [!NOTE] 
> 一括購入モジュールは、Commerce バージョン 10.0.24 リリース時点で使用できます。 古いバージョンの Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。 手順については、[SDK およびモジュール ライブラリの更新](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) を参照してください。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](../starter-kit-overview.md)

[SDK およびモジュール ライブラリの更新](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)

[作成ページの概要](../authoring-home-overview.md)

[テンプレートとレイアウトの概要](../templates-layouts-overview.md)

[フラグメントで動作](../work-with-fragments.md)

[新しいサイト ページの追加](../add-new-page.md)

[チェックアウト モジュール](../add-checkout-module.md)

[コンテンツ ブロック モジュール](../add-hero-module.md)

[製品収集モジュール](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
