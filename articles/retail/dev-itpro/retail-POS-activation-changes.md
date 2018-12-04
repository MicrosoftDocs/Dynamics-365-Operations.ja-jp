---
title: "カスタマイズされた Retail Modern POS のデバイスの有効化"
description: "このトピックでは、カスタマイズした Retail Modern POS アプリケーションを使用する場合に、デバイスの有効化が正常に動作するように、Microsoft Dynamics 365 バックオフィスを設定する方法について説明します。"
author: jashanno
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2017-09-31
ms.dyn365.ops.version: Application update 3
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: 8b092d2b9d3c3f5a728881cdc968eb95a57f7995
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2018

---

# <a name="device-activation-of-a-customized-retail-modern-pos"></a>カスタマイズされた Retail Modern POS のデバイスの有効化

[!INCLUDE [banner](../includes/banner.md)]

このトピックでは、カスタマイズした Retail Modern POS アプリケーションを使用する場合に、デバイスの有効化が正常に動作するように、Microsoft Dynamics 365 バックオフィスを設定する方法について説明します。 カスタマイズされた返信アドレスを取得し、バックオフィスでその値を入力するために必要な手順を説明します。

> [!NOTE]
> このセキュリティおよび機能拡張がは、2017 年 7 月 (7.2) リリースで導入され、その前の 1611 (7.1) リリースに追加されました。

Retail Modern POS は、Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Retail のクライアント側コンポーネントです。 Retail Modern POS を使用するには、デバイスの有効化を実行する必要があります。 デバイスの有効化は、ユーザーを認証する Microsoft Azure Active Directory (Azure AD) を使用します。 この領域の拡張機能は、Web アカウント マネージャー サービスを活用するためにデバイスの有効化のフローを変更しました。 この拡張の一部として、認証承認プロセスのセキュリティが強化されました。 このセキュリティ強化では、コールバック URI に特定の一意の値が必要になるため、Retail Modern POS のカスタマイズ時に、Dynamics 365 バックオフィスで追加設定が必要です。 (コールバック URI は、返信 URI とも呼ばれます。)

既定では、Retail Modern POS はこのコールバック URI に既に登録されています。 ただし、Retail Modern POS をカスタマイズするとき、コールバック URI が変更されます。 したがって、再度動作するように正しく構成する必要があります。 このトピックでは、この構成を完了するために従う必要がある手順について説明します。 この構成が完了しない場合、カスタマイズされた Retail Modern POS アプリケーションでデバイスの有効化を実行しようとすると、エラー メッセージが表示されます。 このエラー メッセージは次のようになります。

> AADSTS50011: The reply address 'ms-appx-web://Microsoft.AAD.BrokerPlugin/[...]' does not match the reply addresses configured for the application

> [!NOTE]
> - Dynamics 365 バックオフィスを構成する前に、カスタマイズされた Retail Modern POS アプリケーションを 1 回使用することをお勧めします。 これにより、エラー メッセージがどのようなものかを確認し、カスタマイズされた返信アドレスをより簡単に取得できます。
> - エラーは、Retail Modern POS アプリケーションに対応するアプリケーション ID に使用される返信アドレスを指定します。

## <a name="setup"></a>段取り
次の手順は、カスタマイズされた Retail Modern POS アプリケーションを使用する場合に、デバイスの有効化が正常に動作できるようにするために必要です。 2 つの Azure AD アプリケーションを作成します。1 つは Retail Modern POS 用、1 つは Retail Server 用です。 Retail Server Azure AD アプリケーションは、Retail Modern POS が Retail Server を通じてリソースを使用するために必要です。 したがって、Retail Modern POS が使用される場合は両方の Azure AD アプリケーションが使用されます。 このシナリオでは、Retail Server は、Retail Modern POS が要求する保護されているリソースのエンドポイントとして機能します。

### <a name="create-the-retail-server-azure-ad-application"></a>Retail サーバーの Azure AD アプリケーションを作成する
1. Web ブラウザーで、<https://portal.azure.com/>に移動します。
2. Azure AD アプリケーションを作成するための十分なアクセス許可を持つ Azure AD 資格情報を使用してログインします。
3. **Azure Active Directory** \> **アプリケーション登録**を選択します。
4. **新しいアプリケーション登録**を選択して、次の値を入力することで、Retail サーバー Azure AD アプリケーションを作成します。

    - **名前:** **カスタマイズされた Retail Server** を入力します。 (他の固有の値を入力できますが、記録しておいてください。)
    - **アプリケーション タイプ:** **Web アプリ/API** を選択します。
    - **サインオン URL:** 実際の物理的な場所をポイントしない固有 URL を入力します。 たとえば、「`https://MyNotRealURL`」を入力します。

5. Azure が **サインオン URL** フィールドの値を検証するように、Tab キーを押します。 次に、**作成** を選択し、処理が正常に完了するまで待機します。 (エラーが発生する場合は、解決してもう一度やり直します。)

    タイルに、新しい Retail Server Azure AD アプリケーションの詳細が表示されます。

6. タイルの上部の **設定** を選択し、アプリケーションの **設定** タイルを開きます。 次に、**プロパティ** を選択します。
7. **プロパティ** タイルで、**アプリケーション ID URI** フィールドの値をコピーします。 この値は、次のセクションで Retail Modern POS の DLLHost.exe.config ファイルに貼り付けます。

> [!NOTE]
> このトピックの後半で再び使用するため、Web ブラウザー ウィンドウを閉じないでください。

### <a name="update-the-retail-modern-pos-configuration"></a>Retail Modern POS 設定の更新
1. ファイル エクスプローラーで、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker** に移動します。 (このパスは、コンピューターの Microsoft Windows オペレーティング システムが、x64 アーキテクチャ ベースであることを前提としています)。
2. エクスプローラーで、**ファイル** \> **Windows PowerShell を開く** \> **管理者として Windows PowerShell を開く** を選択します。
3. 表示された Microsoft Windows PowerShell ウィンドウで、**notepad DLLHost.exe.config**と入力して Enter キーを押します。 (Windows PowerShell ウィンドウは、現在のファイル ディレクトリを既にポイントしています。)
4. 表示されたメモ帳ウィンドウで、**AADRetailServerResourceId** キーに対応する値を見つけます。 (この値は、既定では `https://commerce.dynamics.com` です)。次に、前のセクションの手順 7 でコピーしたアプリケーション ID URI 値を貼り付けます。
5. **ファイル** \> **保存** を選択します。

> [!NOTE]
> 次にセクションで再び使用するため、メモ帳ウィンドウを閉じないでください。

### <a name="create-the-customized-retail-modern-pos-azure-ad-application"></a>カスタマイズされた Retail Modern POS Azure AD アプリケーションを作成する
1. <https://portal.azure.com/> が開いている Web ブラウザー ウィンドウに戻り、「Retail サーバーの Azure AD アプリケーションを作成する」セクションの手順 3 と 4 を繰り返して、Retail Modern POS Azure AD アプリケーションを作成します。 ただし、今回は次の値を入力します。

    - **名前:** **カスタマイズされた Retail Modern POS** を入力します。 (他の固有の値を入力できますが、記録しておいてください。)
    - **アプリケーション タイプ:** **ネイティブ**を選択します。
    - **リダイレクト URI:** このトピックの先頭でお勧めしたように、Dynamics 365 バックオフィスを構成することなく、カスタマイズされた Retail Modern POS アプリケーションを使用するしようとすると、エラー メッセージが表示されます。 そのエラー メッセージに対応する返信アドレス (リダイレクト URI) を入力します。 値の先頭は **ms-appx-web://Microsoft.AAD.BrokerPlugin/[...]** です。

        > [!NOTE]
        > - Windows のイベント ビューアーの **Microsoft-Dynamics-Commerce-ModernPos/Operational** で返信アドレス (リダイレクト URI) を表示することもできます。 イベント ID は 40619 です。 エラー メッセージの先頭は "This UWP application was assigned the following callback URI to be used while interacting with Azure AD: ms-appx-web://Microsoft.AAD.BrokerPlugIn/S-1-15-2-[...]" です。
        > - Azure AD アプリケーションが作成されたら、必要に応じて追加リダイレクト URI を指定できます。 異なるコールバック URI のある複数のパッケージが何らかの理由で生成された場合、この 1 つの Azure AD アプリケーションを保持し、その中にすべてのリダイレクト URI を保持してください。

2. Azure が **リダイレクト URI** フィールドの値を検証するように、Tab キーを押します。 次に、**作成** を選択し、処理が正常に完了するまで待機します。 (エラーが発生する場合は、解決してもう一度やり直します。)

    タイルに、新しいカスタマイズされた Retail Modern POS Azure AD アプリケーションの詳細が表示されます。

3. **アプリケーション ID** フィールドを見つけ、値をコピーします。 (この値は、**AADClientId** キーに対応する値として DLLHost.exe.config ファイルに貼り付けます。)
4. タイルの上部の **設定** を選択し、アプリケーションの **設定** タイルを開きます。 次に、**必要なアクセス許可** を選択します。
5. **必要なアクセス許可** タイルで **+ 追加** を選択します。
6. **API アクセスの追加** タイルで、**1 API を選択する** を選択します。
7. **API を選択** タイルの検索フィールで、「Retail サーバーの Azure AD アプリケーションを作成する」のセクションで作成した Retail Server Azure AD アプリケーションの名前を入力します。 (このトピックでは、アプリケーションの名前は**カスタマイズされた Retail サーバー**です)。そのアプリケーションに対応する品目を選択し、**選択** を選択します。

    **API アクセスを追加する** タイルで、**2 アクセス許可を選択** が自動的に選択され、**アクセスを有効にする** という名前の新しいタイルが表示されます。

8. **アクセスを有効にする** タイルで、**カスタマイズされた Retail サーバーにアクセスする** 行の上にマウス ポインターを置き、左側に表示されるチェック ボックスを選択します。 (Retail Server Azure AD アプリケーションに別の名前を入力し、**カスタマイズされた Retail サーバー** の代わりに、その名前が行で使用される場合)。タイルの下部にある **選択** ボタンが使用できるようになります。
9. **選択** を選択して **API アクセスを追加する** タイルに戻ります。
10. **完了** を選択し、**必要なアクセス許可** タイルに戻ります。
11. **アクセス許可の付与** を選択します。 アクセス許可を付与することを確認するメッセージが表示されたら、**はい** を選択します。
12. DLLHost.exe.config ファイルの内容が表示されているメモ帳ウィンドウに切り替えます。 (前のセクションの手順を完了した後にこのウィンドウから離れます。)
13. **AADClientId** キーに対応する値を見つけます。 (既定では、この値はバックオフィス環境に対応するグローバル一意識別子 [GUID] です)。手順 3 でコピーした値を貼り付けます。
14. **ファイル** \> **保存** を選択します。

### <a name="configure-dynamics-365-headquarters"></a>Dynamics 365 バックオフィスの構成
前の手順は、Retail Modern POS アプリケーションを認証できるようにするために必要でした。 ここでは、要求を承認できるように、次の手順を実行し、新しい Azure AD アプリケーションを Dynamics 365 バックオフィスの安全なプログラムの一覧に追加する必要があります。 (安全なプログラムの一覧はホワイトリストと呼ばれることもあります)。

1. Web ブラウザーで、Dynamics 365 バック オフィス URL に移動し、Azure AD 資格情報を使用してログインします。
2. **小売** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売共有パラメーター**の順にを移動します。
3. **ID プロバイダー** タブの **ID プロバイダー** セクションで、`HTTPS://sts.windows.net/` から始まるプロバイダーを選択します。 選択したプロバイダーに基づいて、**依存する関係者** セクションの値が更新されます。
5. **依存する関係者** セクションで、**+ 追加**を選択し、次の値を入力します。

    - **ClientId:** 前のセクションの手順 3 でコピーし、手順 13 で DLLHost.exe.config に貼り付けた値を入力します。
    - **タイプ:** **パブリック** を選択します。
    - **UserType:** **作業者** を選択します。
    - **名前:** このエントリが参照する、ユーザーがわかりやすい説明を入力します。

6. アクション ウィンドウで、**保存**を選択します。 作成した依存する関係者は選択したままにしてください。
7. **サーバー リソース ID** セクションで、**+ 追加**を選択し、次の値を入力します。

    - **サーバー リソース ID:** 「Retail Modern POS 設定の更新」の手順 4 でコピーした URL を入力します。 (最初は、「Retail サーバーの Azure AD アプリケーションを作成する」の手順 4 でこの値を作成しました)。
    - **名前:** このエントリが参照する、ユーザーがわかりやすい説明を入力します。

8. アクション ウィンドウで、**保存**を選択します。
9. **小売** &gt; **小売 IT** \> **配送スケジュール** の順に移動します。
10. ジョブ **1110** (**グローバル構成**) を選択し、アクション ペインで **今すぐ実行** を選択します。 このジョブは、新しいデータを同期させます。 ただし、Retail サーバーにはキャッシュがあり、数分は更新されません。 したがって、迅速な更新が必要な場合、Retail サーバー アプリケーション プールを再利用する必要があります。

    > [!NOTE]
    > 最適な結果を得るため、Retail Modern POS が終了していることと、DLLHost.exe のインスタンスがタスク マネージャーに存在しないことを確認します。

### <a name="perform-retail-modern-pos-device-activation"></a>Retail Modern POS のデバイスの有効化の実行
Retail Modern POS デバイスを有効化しようとしてください。 依然として問題が発生する場合は、Windowsでイベント ビューアーを開き、Retail Modern POS に対応するログを表示します。 前のセクションで見逃したステップを判断する際に役立つを警告やエラーを探します。

