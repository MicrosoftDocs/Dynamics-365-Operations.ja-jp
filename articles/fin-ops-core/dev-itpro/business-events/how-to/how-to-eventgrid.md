---
title: ビジネス イベントおよび Azure Event Grid
description: この記事では、Microsoft Azure イベント グリッド エンドポイントを構成する方法と、イベント グリッドからビジネス イベントを消費する方法について説明します。
author: Sunil-Garg
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: 85f58bc3b0f17f0917ba7ba983bbf62f168e84a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889267"
---
# <a name="business-events-and-azure-event-grid"></a>ビジネス イベントおよび Azure Event Grid
[!include[banner](../../includes/banner.md)]

この記事では、Microsoft Azure イベント グリッド エンドポイントを構成する方法と、イベント グリッドからビジネス イベントを消費する方法について説明します。

## <a name="scenario-overview"></a>シナリオの概要

セキュリティのベスト プラクティスでは、接続文字列をアプリケーション外の Azure Key Vault ドライブに保存し、アプリケーションに対して Key Vault キー、シークレット、証明書の適切なアクセス権を付与することをお勧めします。

このアプローチの多くの利点のうち 2 つを次に示します。

- アプリケーション データベースにアクセスできるユーザーは、サードパーティの接続文字列を取得できません。
- 特に複数のアプリケーションが同じリソースにアクセスする場合、更新する必要がある接続文字列が 1 か所だけなのでメンテナンスが簡単です。

完了する必要がある手順の概要を次に示します。

1. 新しいイベント グリッド記事を作成します。
2. イベント グリッド記事のキーを格納する新しいキー コンテナーを作成します。
3. Key Vault にアクセスするためのアクセス許可が与えられている Azure アプリを登録します。
4. エンドポイントのパラメーターをコンフィギュレーションします。
5. ビジネス イベントを消費します。

## <a name="procedure-1-create-a-new-event-grid-article"></a>手順 1: 新しいイベント グリッド記事を作成する

1. Azure ポータルにサインインします。
2. **すべてのサービス \> 統合 \> イベント グリッド トピック** を選択します。
3. **追加** を選択して新しいイベント グリッド記事を作成します。 パラメーターを設定してから **作成** を選択します。 ラボのコンテナーとして新しいリソース グループを作成するか、または既存のリソース グループを使用できます。
4. 配置が完了したら、新しいイベント グリッドを選択します。 プロパティ ブレードで **概要** を選択し、**トピック エンドポイント** 値をメモしておきます。 後に、この値を使用します。

    <img alt="Event grid article" src="../../media/BEF-Howto-EventGrid-03.png" width="70%">

5. プロパティ ブレードに戻って **アクセス キー** を選択して **キー 1** の値をコピーします。 次の手順でキー コンテナーを構成するときに、この値が必要になります。

    <img alt="Event grid access key" src="../../media/BEF-Howto-EventGrid-04.png" width="70%">

## <a name="procedure-2-create-a-key-vault"></a>手順 2: 新しいキー コンテナーの作成

この手順では、前の手順でコピーしたキーを保存する Key Vault を作成します。 Key Vault は、キー、シークレット、証明書を保存するために使用する安全なドライブです。 接続文字列を保存する代わりに、より一般的で安全なアプローチは Key Vault に保存することです。 その後、新しいアプリケーションを Azure Active Directory (Azure AD) に登録し、Key Vault からシークレットを取得する権限を付与できます。

1. Azure ポータルで **すべてのサービス \> セキュリティ \> Key Vaults** を選択します。
2. リソース グループに新しい Key Vault を作成し、デフォルトのパラメーターを設定します。

    <img alt="New Key Vault" src="../../media/BEF-Howto-Keyvault-02.png" width="50%">

3. **概要** を選択し、Key Vault の **DNS 名** 値をコピーして保存します。 この値は後で使用します。

    <img alt="Key vault DNS name" src="../../media/BEF-Howto-Keyvault-03.png" width="70%">

4. **BE-Key Vault \> シークレット \> 生成/インポート** を選択します。 シークレットの名前を入力し、先に保存したイベント グリッド接続文字列を貼り付けます。

    <img alt="Key vault secret " src="../../media/BEF-Howto-Keyvault-04.png" width="70%">

5. **作成** を選択します。

## <a name="procedure-3-register-a-new-application"></a>手順 3: 新しいアプリケーションの登録

この手順では、新しいアプリケーションを Azure AD に登録して、Key Vault のシークレットの読み取りと取得アクセスを許可します。 アプリケーションを使用してイベント グリッドのシークレットを取得します。

1. Azure ポータルで **すべてのサービス \> セキュリティ \> Azure Active Directory** を選択します。
2. **アプリ登録 (プレビュー) \> 新しい登録** を選択し、次にアプリケーションの名前を入力します。
3. **登録** を選択します。
4. 新しいアプリケーションを選択して **証明書とシークレット \> 新しいクライアント シークレット** を選択します。 シークレットの名前を入力し、有効期限が切れないようにシークレットを設定します。 その後 **追加** を選択します。

    <img alt="Azure App secret " src="../../media/BEF-Howto-Keyvault-07.png" width="50%">

5. 新しいシークレットをコピーして保存します。 これは後で使用します。

    > [!IMPORTANT]
    > シークレットは一度だけ表示されます。 シークレットをコピーし忘れた場合は、削除してから新しいシークレットを作成する必要があります。

    <img alt="Copy App secret " src="../../media/BEF-Howto-Keyvault-08.png" width="70%">

6. **概要** を選択し、アプリケーション ID をコピーして保存します。 この値は後で使用します。

    <img alt="Copy App Id " src="../../media/BEF-Howto-Keyvault-09.png" width="70%">

7. **すべてのサービス \> セキュリティ \> Key Vaults** を選択します。
8. 前に作成した Key Vault を選択してから **アクセスポリシー \> 新規追加** を選択します。
9. **プリンシパル** ブレードで、新しい登録済みアプリケーションを選択します。 Key Vault のシークレットを取得するには、**Get** と **List** シークレット アクセス許可のチェック ボックスを選択します。

    <img alt="Key Vault access policy " src="../../media/BEF-Howto-Keyvault-12.png" width="50%">

10. 新しいアクセス ポリシーを保存します。

## <a name="procedure-4-configure-a-business-events-endpoint"></a>手順 4: ビジネス イベント エンドポイントのコンフィギュレーション

1. アプリケーションにサイン インし、**システム管理 \> 設定 \> ビジネス イベント** の順に移動します。
2. **エンドポイント** を選択します。
3. **新規** を選択します。
4. **Azure Event Grid** を選択します。
5. **次へ** を選択します。
6. 必要なパラメーター値を設定します。

    <img alt="Event grid endpoint" src="../../media/BEF-Howto-EventGrid-06.png" width="50%">

7. **OK** を選択します。

## <a name="procedure-5-consume-a-business-event"></a>手順 5: ビジネス イベントの消費

ビジネス シナリオでは、USMF 会社に自由書式の請求書が転記されるたびに電子メール メッセージを送信します。 顧客アカウント番号、顧客名、請求書の合計金額など、詳細がメッセージ`に含まれる必要があります。

1. ビジネス イベント カタログを選択し、**自由書式の請求書が転記されました** ビジネス イベントを探します
2. 次に USMF 会社のビジネス イベントを有効化します。 一度有効になると、テスト メッセージは送信され、構成を検証し、接続をキャッシュします。
3. テスト メッセージが受信されたことを確認するには、Azure ポータルでイベント グリッド記事を選択して **メトリックス** を選択します。 **公開されたイベント** メトリックと **一致しないイベント** メトリックの両方が少なくとも **1** の値を示していることを確認します。 そうでない場合は、バッチ ジョブがメッセージを受信するまで待ちます。

    <img alt="Event grid metrics" src="../../media/BEF-Howto-EventGrid-08.png" width="70%">

    両方のメトリックの値が少なくとも **1** の場合、イベント グリッド記事をサブスクライブする新しいロジック アプリを作成します。

4. **すべてのサービス \> 統合 \> Logic Apps** を順に選択します。
5. リソース グループに新しいロジック アプリを作成します。

    <img alt="New logic apps" src="../../media/BEF-Howto-EventGrid-10.png" width="50%">

6. ロジック アプリ リソースを作成したら、空のロジック アプリを作成するオプションを選択します。
7. **イベント グリッド** を検索して **リソース イベントが発生した場合 (プレビュー)** トリガーを選択します。

    <img alt="Event grid trigger" src="../../media/BEF-Howto-EventGrid-11.png" width="50%">

8. サブスクリプションを選択し、リソース タイプとして **Microsoft.EventGrid.Topics** を選択し、手順 1 で作成したイベント グリッド記事の名前を選択します。

    <img alt="Event grid trigger parameters" src="../../media/BEF-Howto-EventGrid-12.png" width="50%">

9. **新規ステップ** を選択して新しいアクションを追加します。
10. **JSON の解析** データ処理を検索します。 このステップは、データ コントラクトの指定されたスキーマを使用してメッセージを解析するために必要です。
11. **Json 解析** アクションの **コンテンツ** フィールドをクリックします。 表示されるウィンドウには前のトリガーからのオプションが表示されます。 Finance and Operations で送信されるペイロードを含むイベント グリッド メッセージの **データ オブジェクト** フィールドを選択する必要があります。

    <img alt="Logic appas parse JSON " src="../../media/BEF-Howto-EventGrid-14.png" width="50%">

    次に、契約の指定されたスキーマを入力する必要があります。 これは、ただのサンプル ペイロードです。 ただし、Azure Logic Apps の機能を使用してペイロードからスキーマを生成できます。

12. ビジネス イベント カタログのイベントを選択し、**スキーマのダウンロード** リンクを選択します。 テキスト ファイルがダウンロードされます。 テキストファイルを開いて内容をコピーします。
13. Logic Apps に戻って **サンプル ペイロードを使用してスキーマを生成** リンクを選択します。 テキスト ファイルの内容を貼り付けて **完了** を選択します。

    <img alt="Event schema " src="../../media/BEF-Howto-EventGrid-16.png" width="70%">

14. サンプル ペイロードの品質により、特に実値がサンプル ペイロードで整数として与えられた場合、ジェネレーターは整数と実値を区別しません。 生成されたスキーマを確認して **整数** データ型のフィールドを **数値** データ型に変更する必要があるか判断します。 (JavaScript Object Notation \[JSON\] で **数値** データ型は実数値を表します。)

    <img alt="JSON data types " src="../../media/BEF-Howto-EventGrid-17.png" width="100%">

    次に、顧客の支払いの詳細を含む通知電子メールの送信など、最終的なアクションを選択します。

15. **電子メールの送信** アクションを検索し、自分の Microsoft 365 アカウントにサインインします。
16. メッセージの本文および、必須項目を入力します。
17. ロジック アプリを保存します。
18. 顧客の支払いを転記して、ビジネス イベントをトリガーします。 そして、ロジック アプリが実行されていること、顧客の支払いの詳細が記載された電子メールを受信することを確認します。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]