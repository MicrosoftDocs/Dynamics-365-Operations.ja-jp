---
title: カスタマイズされた Modern POS のデバイスの有効化
description: このトピックでは、カスタマイズした Modern POS アプリケーションを使用する場合に、デバイスの有効化が正常に動作するように、Microsoft Dynamics 365 Commerce Headquarters を構成する方法について説明します。
author: jashanno
manager: AnnBe
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Application update 3
ms.openlocfilehash: bbb3cf24211f8bdd70eaf1a246782947ce3f8316
ms.sourcegitcommit: ca05440ee503bf15fe98fe138d317c1cdf21ad16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141864"
---
# <a name="device-activation-of-a-customized-modern-pos"></a>カスタマイズされた Modern POS のデバイスの有効化

[!INCLUDE [banner](../includes/banner.md)]

このトピックでは、カスタマイズした Modern POS アプリケーションを使用する場合に、デバイスの有効化が正常に動作するように、Microsoft Dynamics 365 Commerce Headquarters を構成する方法について説明します。 カスタマイズされた返信アドレスを取得し、Headquarters でその値を入力するために必要な手順を説明します。

Modern POS は、Microsoft Dynamics 365 Commerce のクライアント側コンポーネントです。 POS を使用するには、デバイスの有効化を実行する必要があります。 デバイスの有効化は、ユーザーを認証する Azure Active Directory (Azure AD) を使用します。 この領域の拡張機能は、Web アカウント マネージャー サービスを活用するためにデバイスの有効化のフローを変更しました。 この拡張の一部として、認証承認プロセスのセキュリティが強化されました。 このセキュリティ強化では、コールバック URI に特定の一意の値が必要になるため、POS のカスタマイズ時に Headquarters で追加設定が必要です。 (コールバック URI は、リダイレクト URI とも呼ばれます。)

既定では、Modern POS はこのコールバック URI に既に登録されています。 ただし、カスタマイズするとき、コールバック URI が変更されます。 したがって、再度動作するように正しく構成する必要があります。 このトピックでは、この構成を完了するために従う必要がある手順について説明します。 この構成が完了していない場合、カスタマイズされた POS アプリケーションでデバイスの有効化を実行しようとすると、エラー メッセージが表示されます。 このエラー メッセージは次のようになります。

> AADSTS50011: 返信アドレス「ms-appx-web://Microsoft.AAD.BrokerPlugin/[...]」はアプリケーションで構成された返信アドレスと一致しません。

返信アドレスは、上記のエラー メッセージの最後に表示される Modern POS パッケージ SID に依存します。 これは Package Family Name (PFN) の機能なので、名前と公開キーに依存します。 つまり、Modern POS をカスタマイズし、会社の証明書で署名すると、SID は変更されます。 変更はパッケージのバージョンではなく証明書に基づいているので、パッケージ全体が変わらず、証明書が同じである限り、SID は同じままです。

> [!NOTE]
> Dynamics 365 Headquarters を構成する前に、カスタマイズされた Modern POS アプリケーションを 1 回使用することをお勧めします。 これにより、エラー メッセージがどのようなものかを確認し、カスタマイズされた返信アドレスをより簡単に取得できます。

## <a name="setup"></a>段取り
次の手順は、カスタマイズされた Modern POS アプリケーションを使用する場合に、デバイスの有効化が正常に動作できるようにするために必要です。 2 つの Azure AD アプリケーションを作成します。1 つは Modern POS 用、1 つは Commerce Scale Unit 用です。 POS は Commerce Scale Unit を通じてリソースを使用するため、Commerce Scale Unit Azure AD アプリケーションが必要です。 したがって、POS が使用される場合は両方の Azure AD アプリケーションが使用されます。 このシナリオでは、Commerce Scale Unit は、POS が要求する保護されているリソースのエンドポイントとして機能します。

### <a name="create-the-commerce-scale-unit-azure-ad-application"></a>Commerce Scale Unit Azure AD アプリケーションの作成
1. Web ブラウザーで、<https://portal.azure.com/>に移動します。
2. Azure AD アプリケーションを作成するための十分なアクセス許可を持つ Azure AD 資格情報を使用してログインします。
3. Azure サービスの一覧から **Azure Active Directory** を選択し、表示される左端のメニューから **アプリの登録** を選択します。
4. **新しい登録** を選択して、次の値を入力することにより、Commerce Scale Unit Azure AD アプリケーションを作成します。

    - **名前:** **カスタマイズされた Commerce Scale Unit** を入力します。 他の固有の値を入力できますが、入力された名前を記録しておいてください。
    - **サポートされる勘定タイプ:** このアプリケーションの登録が **すべての組織のディレクトリの勘定** の値を要求する複数のテナント間で使用される場合を除き、**この組織のディレクトリの勘定のみ** の値を選択します。 この選択は一般的ではないことに注意してください。
    - **リダイレクト URI:** この値は空白のままにすることができますが、ドロップダウンの初期の選択が **Web** に設定されていることを確認する必要があります。

5. ページの下部にある **登録** を選択します。 ページは、新しく作成された Azure AD アプリケーションに変更されます。
6. **アプリケーション ID URI の追加** と表示されているリンクのある **アプリケーション ID URI** を選択します。 このページは、**API の公開** を選択することによって左のメニューからアクセスすることもできます。
7. 開かれたタイルで、**設定** と表示されている **アプリケーション ID URI** の値を選択します。 **保存** ボタンを選択する前に表示された値をコピーします。 この値は、次のセクションで POS の DLLHost.exe.config ファイルに貼り付けます。
8. **保存** を選択し、この URI を設定します。
9. **スコープの追加** ボタンを選択します。
10. 表示されるスライダーで、次の値を入力します。

    - **スコープ名:** **AccessRetailServer** を入力します。 他の固有の値を入力できますが、入力された名前を記録しておいてください。
    - **同意できるユーザー**: **管理者とユーザー** オプションを選択します。
    - **管理者の同意の表示名:** **AccessRetailServer** を入力します。 単純化のために、この値は上記の **スコープ名** と一致させます。
    - **管理者の同意の説明:** **AccessRetailServer** を入力します。 ここにはどの値も入力することができます。 これはスコープの理由を記録するために使用されます。
    - **ユーザーの同意の表示名** および **ユーザーの同意の説明** は使用されません。
    - **状態:** **有効** が選択されているか確認します。

11. **スコープの追加** ボタンを選択します。
12. 左端のメニューの **概要** タブを選択します。 **アプリケーション ID URI** の値が手順 7 でコピーされたものと一致していることを確認します。

> [!NOTE]
> このトピックの後半で再び使用するため、Web ブラウザー ウィンドウを閉じないでください。

### <a name="update-the-modern-pos-configuration"></a>Modern POS 構成の更新
1. ファイル エクスプローラーで、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker** に移動します。 (このパスは、コンピューターの Microsoft Windows オペレーティング システムが、x64 アーキテクチャ ベースであることを前提としています)。
2. エクスプローラーで、**ファイル** \> **Windows PowerShell を開く** \> **管理者として Windows PowerShell を開く** を選択します。
3. 表示された Microsoft Windows PowerShell ウィンドウで、**notepad DLLHost.exe.config** と入力して Enter キーを押します。 (Windows PowerShell ウィンドウは、現在のファイル ディレクトリを既にポイントしています。)
4. 表示されたメモ帳ウィンドウで、**AADRetailServerResourceId** キーに対応する値を見つけます。 (この値は、既定では `https://commerce.dynamics.com` です)。次に、前のセクションの手順 7 でコピーしたアプリケーション ID URI 値を貼り付けます。
5. **ファイル** \> **保存** を選択します。

> [!NOTE]
> 次にセクションで再び使用するため、メモ帳ウィンドウを閉じないでください。
> 上記の手順を実行する別の方法は、スクリプトまたはインストール後の手順のカスタマイズを使用することです。

### <a name="create-the-customized-modern-pos-azure-ad-application"></a>カスタマイズされた Modern POS Azure AD アプリケーションを作成する
1. <https://portal.azure.com/> が開いている Web ブラウザー ウィンドウに戻り、「Commerce Scale Unit Azure AD アプリケーションを作成する」セクションの手順 3 から 5 を繰り返して、Retail Modern POS Azure AD アプリケーションを作成します。 ただし、今回は次の値を入力します。

    - **名前:** **カスタマイズされた Retail Modern POS** を入力します。 (他の固有の値を入力できますが、入力された名前を記録しておいてください。)
    - **サポートされる勘定タイプ:** このアプリケーションの登録が **すべての組織のディレクトリの勘定** の値を要求する複数のテナント間で使用される場合を除き、**この組織のディレクトリの勘定のみ** の値を選択します。 この選択は一般的ではないことに注意してください。
    - **リダイレクト URI:** 初期のドロップダウン 値は、**パブリック クライアント/ネイティブ (モバイル & デスクトップ)** に変更する必要があります。 このタイプのリダイレクト URI に入力する値は、受信した Modern POS エラー メッセージのこのトピックの冒頭に表示される値です。 そのエラー メッセージに対応する返信アドレス (リダイレクト URI) を入力します。 値の先頭は **ms-appx-web://Microsoft.AAD.BrokerPlugin/[...]** です。

        > [!NOTE]
        > - Windows のイベント ビューアーの **Microsoft-Dynamics-Commerce-ModernPos/Operational** で返信アドレス (リダイレクト URI) を表示することもできます。 イベント ID は 40619 です。 エラー メッセージの先頭は "This UWP application was assigned the following callback URI to be used while interacting with Azure AD: ms-appx-web://Microsoft.AAD.BrokerPlugIn/S-1-15-2-[...]" です。
        > - Azure AD アプリケーションが作成されたら、必要に応じて追加リダイレクト URI を指定できます。 異なるコールバック URI のある複数のパッケージが何らかの理由で生成された場合、この 1 つの Azure AD アプリケーションを保持し、その中にすべてのリダイレクト URI を保持してください。

2. **リダイレクト URI** フィールドのこの値を確認することは重要です。 次に、**作成** を選択し、処理が正常に完了するまで待機します。 (エラーが発生する場合は、解決してもう一度やり直します。)

    タイルに、新しいカスタマイズされた Retail Modern POS Azure AD アプリケーションの詳細が表示されます。

3. ページの下部にある **登録** を選択します。 ページは、新しく作成された Azure AD アプリケーションに変更されます。
4. **アプリケーション (クライアント) ID** フィールドを検索し、値をコピーします。 前のセクションで開いたメモ帳に切り替え (または、上のセクション **Modern POS コンフィギュレーションの更新** に従って、**DLLHost.exe.config** ファイルを開く)、**AADClientId** に対応する値に移動します。 このフィールドにこの手順の最初でコピーした値を貼り付け、(同じセクションの手順 5 に示されているように) ファイルを保存します。
5. Web ブラウザーに戻り、左端のメニューで、**API アクセス許可** オプションを選択します。
6. **API アクセス許可** タイルで、**+ アクセス許可の追加** を選択します。
7. 表示されるスライダーで、最初に **自分の API** ヘッダーを選択します。 **カスタマイズされた Commerce Scale Unit** というタイトルの API、またはこのドキュメントの最初の手順 4 で名前として入力された値を選択します。
8. **アクセス許可の選択** の下位ヘッダーの下で、**AccessRetailServer** またはこのドキュメントの手順 10 でスコープ名として入力された値を選択します。
9. スライダーの下部にある **アクセス許可の追加** を選択します。
10. **\<your AAD name\> に対して管理者の同意の付与** を選択します。 **はい** を選択します。 これにより同意を付与することになり、**AccessRetailServer** 行の **状態** 列に表示される **許可済** によって確認することができます。

        > [!NOTE]
        > Granting consent is not required, but simplifies the process by consenting in advance for all users in your tenant (and you as the Admin). If this step is not completed, then each user will be asked for consent the first time that they try to activate Modern POS.

### <a name="configure-dynamics-365-headquarters"></a>Dynamics 365 Headquarters の構成
前の手順は、Modern POS アプリケーションを認証できるようにするために必要でした。 ここでは、要求を承認できるように、次の手順を実行し、新しい Azure AD アプリケーションを Headquarters の安全なプログラムの一覧に追加する必要があります。 (安全なプログラムの一覧はセーフ リストと呼ばれることもあります)

1. Web ブラウザーで、Headquarters URL に移動し、Azure AD 資格情報を使用してログインします。
2. **Retail と Commerce** &gt; **Headquarters の設定** &gt; **パラメーター** &gt; **Commerce 共有パラメーター** の順に移動します。
3. **ID プロバイダー** タブの **ID プロバイダー** セクションで、`HTTPS://sts.windows.net/` から始まるプロバイダーを選択します。 選択したプロバイダーに基づいて、**依存する関係者** セクションの値が更新されます。
5. **依存する関係者** セクションで、**+ 追加** を選択し、次の値を入力します。

    - **ClientId:** 前のセクションの手順 3 でコピーし、手順 13 で DLLHost.exe.config に貼り付けた値を入力します。
    - **タイプ:** **パブリック** を選択します。
    - **UserType:** **作業者** を選択します。
    - **名前:** このエントリが参照する、ユーザーがわかりやすい説明を入力します。

6. アクション ウィンドウで、**保存** を選択します。 作成した依存する関係者は選択したままにしてください。
7. **サーバー リソース ID** セクションで、**+ 追加** を選択し、次の値を入力します。

    - **サーバー リソース ID:** 「Modern POS 構成の更新」セクションの手順 4 でコピーした URL を入力します。 (最初は、「Commerce Scale Unit Azure AD アプリケーションを作成する」セクションの手順 4 でこの値を作成しました。)
    - **名前:** このエントリが参照する、ユーザーがわかりやすい説明を入力します。

8. アクション ウィンドウで、**保存** を選択します。
9. **Retail と Commerce** &gt; **Retail と CommerceIT** \> **配送スケジュール** の順に移動します。
10. ジョブ **1110** (**グローバル構成**) を選択し、アクション ペインで **今すぐ実行** を選択します。 このジョブは、新しいデータを同期させます。 ただし、Commerce Scale Unit にはキャッシュがあり、数分は更新されません。 したがって、迅速な更新が必要な場合、Commerce Scale Unit アプリケーション プールを再利用する必要があります。

    > [!NOTE]
    > 最適な結果を得るため、Modern POS が終了していることと、DLLHost.exe のインスタンスがタスク マネージャーに存在しないことを確認します。

### <a name="perform-modern-pos-device-activation"></a>Modern POS のデバイスの有効化の実行
Modern POS デバイスを有効化してください。 依然として問題が発生する場合は、Windowsでイベント ビューアーを開き、Modern POS に対応するログを表示します。 前のセクションで見逃したステップを判断する際に役立つを警告やエラーを探します。
