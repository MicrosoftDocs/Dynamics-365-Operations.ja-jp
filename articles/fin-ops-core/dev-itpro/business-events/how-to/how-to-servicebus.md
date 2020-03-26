---
title: ビジネス イベントおよび Azure Service Bus
description: このトピックでは、Microsoft Azure Service Bus エンドポイントを構成する方法と、Service Bus からビジネス イベントを消費する方法を説明します。
author: ibenbouzid
manager: AnnBe
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: imbenbou
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: 022740fdb1dfe19497bc56c03a2c41d38d2ee3b2
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091737"
---
# <a name="business-events-and-azure-service-bus"></a>ビジネス イベントおよび Azure Service Bus
[!include[banner](../../includes/banner.md)]

このトピックでは、Microsoft Azure Service Bus エンドポイントを構成する方法と、Service Bus からビジネス イベントを消費する方法を説明します。

## <a name="scenario-overview"></a>シナリオの概要

セキュリティのベスト プラクティスでは、接続文字列をアプリケーション外の Azure Key Vault ドライブに保存し、アプリケーションに対して Key Vault キー、シークレット、証明書の適切なアクセス権を付与することをお勧めします。

このアプローチの多くの利点のうち 2 つを次に示します。

- アプリケーション データベースにアクセスできるユーザーは、サードパーティの接続文字列を取得できません。
- 特に複数のアプリケーションが同じリソースにアクセスする場合、更新する必要がある接続文字列が 1 か所だけなのでメンテナンスが簡単です。

完了する必要がある手順の概要を次に示します。

1. 新しい Service Bus の名前空間を作成します。
2. 新しい Service Bus のトピックとサブスクリプションを作成します。
3. Service Bus キーを格納する新しい Key Vault を作成します。
4. Key Vault にアクセスするためのアクセス許可が与えられている Azure アプリを登録します。
5. ビジネス イベント エンドポイントをコンフィギュレーションします。
6. ビジネス イベントを消費します。

## <a name="create-a-new-service-bus-namespace"></a>新しい Service Bus の名前空間を作成する

1. Azure ポータルにサインインします。
2. **すべてのサービス \> 統合 \> Service Bus** を順に選択します。
3. **追加** を選択して新しい Service Bus の名前空間を作成し、パラメーターを設定します。 **標準** の価格レベルを選択します。 ラボのコンテナーとして新しいリソース グループを作成するか、または既存のリソース グループを使用できます。

    > [!NOTE]
    > **基本** 価格レベルを選択した場合、作成できるのはキューのみです。 トピックを作成するには **標準** 価格帯を選択する必要があります。

4. すべてのパラメーターの設定が終了したら **作成** を選択します。

## <a name="create-a-new-service-bus-topic-and-subscription"></a>新しい Service Bus のトピックとサブスクリプションを作成

1. Azure ポータルで、作成した Service Bus を選択して新しいトピックを作成します。

   <img alt="Service Bus Topic" src="../../media/BEF-Howto-servicebus-03.png" width="70%">

2. 新しいトピックを選択して **BE-USMF** という名前の新しいサブスクリプションを作成します。

    <img alt="Service Bus subscription" src="../../media/BEF-Howto-servicebus-04.png" width="70%">

3. Service Bus のブレードに戻り、イベントを送信する新しい共有アクセス ポリシーを作成します。 Service Bus のトピックにイベントを送信するには **送信** ポリシーのみが必要です。

    <img alt="Service Bus Shared access policy" src="../../media/BEF-Howto-servicebus-05.png" width="70%">

4. 新しい **送信** ポリシーを選択して **プライマリ接続文字列** 値をコピーして保存します。 この値は後で使用します。

    <img alt="Service Bus connection string" src="../../media/BEF-Howto-servicebus-06.png" width="70%">

  > [!NOTE]
  > 共有アクセス ポリシーは、トピック レベルではなく、名前空間レベルにある必要があります。 トピック レベルの共有アクセスポリシーを使用する場合は、ビジネス イベント用のエンドポイントをコンフィギュレーションするときに、末尾にセミコロン EntityPath = を付加した文字列を含めることはできません。

## <a name="create-a-new-key-vault"></a>新しい Key Vault の作成

この手順では、前の手順でコピーしたキーを保存する Key Vault を作成します。 Key Vault は、キー、シークレット、証明書を保存するために使用する安全なドライブです。 接続文字列を保存する代わりに、より一般的で安全なアプローチは Key Vault に保存することです。 その後、新しいアプリケーションを Azure Active Directory (Azure AD) に登録し、Key Vault からシークレットを取得する権限を付与できます。

1. Azure ポータルで **すべてのサービス \> セキュリティ \> Key Vaults** を選択します。
2. リソース グループに新しい Key Vault を作成し、デフォルトのパラメーターを設定します。

    <img alt="New Key Vault" src="../../media/BEF-Howto-Keyvault-02.png" width="50%">

3. **概要** を選択し、Key Vault の **DNS 名** 値をコピーして保存します。 この値は後で使用します。

    <img alt="Key vault DNS name" src="../../media/BEF-Howto-Keyvault-03.png" width="70%">

4. **BE-Key Vault \> シークレット \> 生成/インポート** を選択します。 シークレットの名前を入力し、先に保存した Service Bus 接続文字列を貼り付けます。

    <img alt="Key vault secret " src="../../media/BEF-Howto-Keyvault-04.png" width="70%">

5. **作成**を選択します。

## <a name="register-a-new-application"></a>新しいアプリケーションの登録

この手順では、新しいアプリケーションを Azure AD に登録して、Key Vault のシークレットの読み取りと取得アクセスを許可します。 Finance and Operations はこのアプリケーションを使用して、Service Bus のシークレットを取得します。

1. Azure ポータルで **すべてのサービス \> セキュリティ \> Azure Active Directory** を選択します。
2. **アプリ登録 (プレビュー) \> 新しい登録** を選択し、アプリケーションの名前を入力します。
3. **登録** を選択します。
4. 新しいアプリケーションを選択してから **証明書とシークレット \> 新しいクライアント シークレット** を選択します。 シークレットの名前を入力し、有効期限が切れないようにシークレットを設定します。 その後 **追加** を選択します。

    <img alt="Azure App secret " src="../../media/BEF-Howto-Keyvault-07.png" width="50%">

5. 新しいシークレットをコピーして保存します。 これは後で使用します。

    > [!IMPORTANT]
    > シークレットは一度だけ表示されます。 シークレットをコピーし忘れた場合は、削除してから新しいシークレットを作成する必要があります。

    <img alt="Copy App secret " src="../../media/BEF-Howto-Keyvault-08.png" width="70%">

6. **概要** を選択し、アプリケーション ID をコピーして保存します。 この値は後で使用します。

    <img alt="Copy App ID " src="../../media/BEF-Howto-Keyvault-09.png" width="70%">

7. **すべてのサービス \> セキュリティ \> Key Vaults** を選択します。
8. 前に作成した Key Vault を選択してから **アクセスポリシー \> 新規追加** を選択します。
9. **プリンシパル** ブレードで、新しい登録済みアプリケーションを選択します。 Key Vault のシークレットを取得するには、**Get** と **List** シークレット アクセス許可のチェック ボックスを選択します。

    <img alt="Key Vault access policy " src="../../media/BEF-Howto-Keyvault-12.png" width="50%">

10. 新しいアクセス ポリシーを保存します。

## <a name="configure-a-business-events-endpoint"></a>ビジネス イベント エンドポイントのをコンフィギュレーション 

1. アプリケーションにサイン インし、**システム管理** \> **設定** \> **ビジネス イベント**の順に移動します。
2. **エンドポイント** を選択します。
3. **新規** を選択します。
4. **Azure Service Bus のトピック** を選択します。
5. **次へ** を選択します。
6. 必要なパラメーター値を設定します。

    <img alt="Service Bus endpoint" src="../../media/BEF-Howto-servicebus-08.png" width="70%">

7. **OK** を選択します。

## <a name="consume-a-business-event"></a>ビジネス イベントの消費

ビジネス シナリオは USMF 企業の顧客の支払いが転記されるたびに、電子メールやメッセージをチーム チャネルに送信します。 顧客アカウント番号、顧客名、支払い額などの詳細がメッセージ`に含まれる必要があります。

1. ビジネス イベント カタログを選択し、**顧客の支払が転記されました**ビジネス イベントを探します
2. USMF 会社のビジネス イベントを有効化します。

    <img alt="Activate business event " src="../../media/BEF-Howto-servicebus-09.png" width="30%">

    新しい Service Bus エンドポイントを使用するビジネス イベントを有効化した後、アプリケーションはテスト メッセージを送信してコンフィギュレーションが正確であることを確認し、接続をキャッシュします。

3. テスト メッセージが受信されたことを確認するには Azure ポータルで **BE-Topic** Service Bus トピックを選択して、そして以前に作成した **BE-USMF** Service Bus サブスクリプションに入ります。 サブスクリプションのメッセージ数が少なくとも **1** の値を示していることを確認します。 そうでない場合は、バッチジョブがメッセージを受信するまで待ちます。

    <img alt="Service Bus message count" src="../../media/BEF-Howto-servicebus-10.png" width="70%">

3. **すべてのサービス \> 統合 \> ロジック アプリ** を順に選択します。

    <img alt="Logic apps" src="../../media/BEF-Howto-servicebus-11.png" width="70%">

4. リソース グループに新しいロジック アプリを作成します。
5. ロジック アプリ リソースを作成したら、空のロジック アプリを作成するオプションを選択します。
6. **サービス バス** を検索して選択します。
7. **トピック サブスクリプションでメッセージを受信した場合 (オート コンプリート)** という名前のトリガーを選択します。

    > [!NOTE] 
    > オート コンプリートとは、メッセージが取得された後にサブスクリプション キューから削除されることを意味します。 ピーク ロックは同時実行消費者を許可します。 メッセージを削除するには、Service Bus アプリケーション プログラミング インターフェイス (API) の **完了** コマンドを呼び出す必要があります。

    ロジック アプリは初めて Service Bus にアクセスするために新しい接続を要求します。 この接続は、接続の詳細を Service Bus 名前空間の URL と資格情報としてキャッシュします。

8. Service Bus 名前空間を選択して新しい接続の名前を入力します。
9. ロジック アプリの **RootManageSharedAccessKey** ポリシーを選択して **作成** を選択します。

    > [!NOTE]
    > メッセージを送信するのではなく*取得* する必要があるため **送信** ポリシーをここで使用できません。 ベスト プラクティスとして、このユース ケースに新しいポリシーを作成して **リッスン** アクセス許可のみを付与できます。

    <img alt="Service bus listen policy " src="../../media/BEF-Howto-servicebus-16.png" width="70%">

10. トリガー パラメーターを選択します。 作成したトピックとサブスクリプションに必ず正しい名前を使用します。

    この API はコンフィギュレーション可能な頻度で、新しいメッセージの Service Bus をポーリングします (既定は 3 分ごと)。 ロジック アプリはトリガーの呼び出しとアクションの実行ごとに課金されるため、メッセージの量が少ない場合に API は不要なトリガーのコストに影響を与えます。 ただし、途中で Azure Event Grid を使用するプッシュ アーキテクチャを実装できます。 キューやサブスクリプションにメッセージがある場合、Service Bus はイベントをイベント グリッドにプッシュできます。 詳細については [Azure Service Bus からイベント グリッドへの統合の概要](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-to-event-grid-integration-concept) を参照してください。

    <img alt="Logic apps trigger " src="../../media/BEF-Howto-servicebus-17.png" width="70%">

11. **新規ステップ** を選択して新しいアクションを追加します。
12. **JSON の解析** データ処理を検索します。 このステップは、データ コントラクトのスキーマを使用してメッセージを解析するために必要です。

    Service Bus から受信した本文コンテンツは base64 形式にエンコードされます。 したがって、JavaScript Object Notation (JSON) ペイロードを解析する前に文字列形式に変換する必要があります。 

13. **コンテンツ** フィールドをクリックし、表示されたウィンドウの **式** タブに次の式を入力します: **Base64ToString()**

    <img alt="base64ToString " src="../../media/BEF-Howto-servicebus-19.png" width="70%">

14. 式の括弧の間にカーソルを置き、**動的コンテンツ** タブで前の Service Bus トリガーから **メッセージのコンテンツ** コンテンツを見つけて選択します。 その後、**OK** を選択します。

    <img alt="Service Bus message body " src="../../media/BEF-Howto-servicebus-20.png" width="50%">

    次に、アプリケーションから受け取った契約のスキーマを入力する必要があります。 アプリケーションでは、サンプル ペイロードのみ提供します。 ただし、Azure ロジック アプリの機能を使用してペイロードからスキーマを生成できます。

15. ビジネス イベント カタログのイベントを選択し、**スキーマのダウンロード**リンクを選択します。 ダウンロードしたテキスト ファイルを開いて内容をコピーします。
16. ロジック アプリに戻って **サンプル ペイロードを使用してスキーマを生成** リンクを選択します。 テキスト ファイルの内容を貼り付けて **完了** を選択します。

    <img alt="Message schema " src="../../media/BEF-Howto-servicebus-22.png" width="70%">

17. サンプル ペイロードの品質により、特に実値がサンプル ペイロードで整数として与えられた場合、ジェネレーターは整数と実値を区別しません。 生成されたスキーマを確認して **整数** データ型のフィールドを **数値** データ型に変更する必要があるか判断します。 (JSON で **数値** データ型は実値を表します。)

    <img alt="JSON data types " src="../../media/BEF-Howto-servicebus-23.png" width="70%">

    次に、顧客の支払いの詳細を含む通知電子メールの送信など、最終的なアクションを選択します。

18. **電子メールの送信** アクションを検索し、自分の Microsoft Office 365 アカウントにサインインします。
19. メッセージの本文および、必須項目を入力します。

    <img alt="Logic apps action send email " src="../../media/BEF-Howto-servicebus-25.png" width="70%">

20. ロジック アプリを保存します。
21. 顧客の支払いを転記して、ビジネス イベントをトリガーします。 そして、ロジック アプリが実行されていること、顧客の支払いの詳細が記載された電子メールを受信することを確認します。
