---
title: "モバイル プラットフォームのホーム ページ"
description: "モバイル プラットフォームを使用して、ワークスペースのモバイル アプリを作成できます。"
author: RobinARH
manager: AnnBe
ms.date: 03/07/2018
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
ms.author: robinr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 9a6a792e07c827104667643241d7ec5c2efdb22b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="mobile-platform"></a>モバイル プラットフォーム

[!include [banner](../../includes/banner.md)]

モバイル アプリケーションを使用することにより、Microsoft Dynamics 365 for Finance and Operations からビジネス ロジックおよびモデリングを再利用することができます。 モバイル アプリで、豊富なオフラインおよびモバイルの相互関係と、扱いやすいデザイナー体験を可能にします。 開発者は、Microsoft Visual Studio で簡単なフォームを作成し、この機能を公開するモバイル アプリを設計することができます。 モバイル プラットフォームを使用すると、フォームやモバイル アプリの定義を簡単に変更して、Finance and Operations に加えられたカスタマイズを組み込むことができます。 

## <a name="get-started"></a>使用開始

+ [はじめに](mobile-platform-getting-started.md) 
+ [アーキテクチャ](mobile-platform-architecture.md) 
+ [ページ デザインのガイドライン](page-design-guidelines.md)
+ [アクション デザインのガイドライン](action-design-guidelines.md)
+ [フォーム デザインの要件](form-design-requirements.md)

モバイル アプリの作成方法を示す次のハウツー ビデオ シリーズをチェック アウトしてください。

+ [チュートリアル 1: 販売注文のページを構築する](https://youtu.be/PdegfBxifl8)
+ [チュートリアル 2: 販売注文詳細ページを構築する](https://youtu.be/mF-vlbnRte0)
+ [チュートリアル 3: 新しい販売注文アクション作成を構築する](https://youtu.be/VYw9oTv9t3o)
+ [チュートリアル 4: 新しい販売注文アクション作成にルックアップを追加する](https://youtu.be/eNJKd0IYmZk)
+ [チュートリアル 5: ルックアップの追加し、モバイル ビジネス ロジックを使用してページを非表示にする](https://youtu.be/kIJKk9J8FvI)

## <a name="common-configurations"></a>一般的な構成
これらのトピックでは、モバイル アプリに追加できる一般的なカスタマイズについて説明します。

+ [モバイル ワークスペースのローカライズ](scenarios/localize-workspaces-on-server.md)
+ [モバイル ワークスペースのセキュリティを強化する](scenarios/secure-mobile-workspace.md)
+ [クリック可能なフィールドを設定する](scenarios/make-workspace-field-clickable.md)
+ [ワークスペース クラスを使用して必須フィールドを設定する](scenarios/make-field-mandatory.md)
+ [フィールドに品目数を表示する](scenarios/display-count-workspace.md)

## <a name="client-side-development"></a>クライアント側の開発

クライアント側の API はビジネス ロジック ファイルで使用されます。この API は、カスタマイズ可能なモバイルワーク スペースに拡張レイヤーを提供します。 クライアント側の API を通じてアクセスしたり操作したりできるものは次のとおりです。
+ メタデータ
+ ランタイム コントロール/ページ インスタンス
+ 業務データ
+ オフライン-最初の業務動作
+ レイアウトおよびスタイル

クライアント側の開発のプロセスは次のトピックで説明します。
+ [クライアント側の設計 API の概要](scenarios/client-api-design-overview.md)
+ [ビジネス ロジック イベントの概要](business-logic-events-overview.md)
+ [クライアント API](client-apis/client-apis-reference.md)

引当管理ワークスペースのためにサンプルのビジネス ロジック ファイル (.js ファイル名拡張子付き) をダウンロードすることができます。 [Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) に移動し、**business_logic フォルダ**を開き、FM.js ファイルを指定します。

## <a name="server-side-development"></a>サーバー側の開発

ワークスペースの属性とクラスは、サーバー上でワークスペースを作成、構成、および公開するために使用されます。 タスク レコーダー ベースのメカニズムを使用してワークスペースを構築する代わりに、これらのサーバー側 X++ API を使用できます。 いずれかのメカニズムを使用して作成されたワークスペースは、クライアント側 API を使用してスタイルを設定して強化することができます。

サーバー側開発は、次のトピックで説明します。
+ [ワークスペース クラスの概要](scenarios/mobile-workspace-configuration.md)
+ [サーバー APIs (X++)](mobile-workspace-server-apis.md)

フリート管理モバイル アプリのサンプル プロジェクト (.axpp ファイル名拡張子付き) をダウンロードすることができます。 [Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) に移動し、**FMMobileApp.axpp** ファイルをダウンロードします。

## <a name="debugging-during-development"></a>開発時のデバッグ

展開中に、バックグラウンドで何が起きているのかをより詳細な情報と洞察を得るために、デバッガーを添付すると便利です。 Web デバッガーは、クライアント側の JavaScript ロジックとスタイルで使用することができ、Visual Studio デバッガーは、サーバー側の X++ ビジネス ロジックで使用できます。

### <a name="debugging-the-client-side"></a>クライアント側のデバッグ 

#### <a name="prerequisites"></a>前提条件
- Android デバイスに加えて PC (推奨) または iOS デバイスと Mac
- Azure でホストされた開発マシン (モバイル デバイスで指定できます)

#### <a name="steps-to-debug-the-client-side"></a>クライアント側をデバッグする手順
1. Azure でホストされた開発マシンで公開されている Web クライアントで、Unified Operations アプリ用に公開されたモバイル ワークスペースがあることを確認します。 モバイル ワークスペースを公開する方法については、[モバイル ワークスペースの公開](../publish-mobile-workspace.md) を参照してください。

2. Unified Operations アプリをデバイスで開いて、Azure でホストされた開発マシンを参照し、サインインします。

3. デバッグ マシンからデバイスに接続します。

    - Android デバイスで、Azure でホストされた開発マシンまたは別の PC で、[リモート デバッグ Android デバイスで開始](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/) する Android 開発者指示に従います。 また、[Android 用 Chrome のリモート デバッグ](https://www.youtube.com/results?search_query=chrome+for+android+remote+debugging) を検索することにより、YouTube 上で多様な説明ビデオを見つけることができます。 
    
    - iOS デバイスについては、Mac で実行されている Safari 使用して iOS デバイスに接続します。
    
4. デバッガーに接続した後は、デバイスの有効タブを見つけます。 Android で **その他のタブを表示** をクリックすることが必要な場合があります。 タブのいずれかは、`/www.index.html#/app/appList`または`/www.index.html#/app/app_landing`のようになります。 

    **ファイル** > (ドメインなし) > **ExpenseMobile.js** などのワークスペース JavaScript を表示するには、ノードを展開します。 JavaScript ファイルをクリックして表示し、ブレークポイントを追加します。
    
    ![経費管理モバイル ワークスペース](./media/expense-management-mobile-workspace.png)
    
5. デスクトップ画面に操作できるように、デスクトップにモバイル デバイスを反映します。 

6. 目的のワークスペースとフォームを通して移動します。

7. ブレークポイントが発生した場合、ブラウザーの開発者ツールにより実行フローの管理が可能となり、値と渡されるパラメーターが参照できるようになります。 

8. 実行時にスタイル設定を変更するのにには、要素タブを使用してスタイル設定を変更します。 これは、JavaScript がどの要素を対象にすべきかを決定し、要素のスタイルを設定する方法を決定するのに役立ちます。

9. 必要な変更が指定された場合は、JavaScript では、それらの変更がなされ、環境にこれらの変更をプッシュします。

10. 詳細の変更や検証が必要な場合は、プロセスを繰り返します。

### <a name="debugging-the-server-side"></a>サーバー側のデバッグ

#### <a name="prerequisites"></a>前提条件
- Azure でホストされた開発マシン (モバイル デバイスで指定できます)

#### <a name="steps-to-debug-the-serverside"></a>サーバー側をデバッグする手順
1. Azure でホストされた開発マシンで公開されている Web クライアントで、Unified Operations アプリ用に公開されたモバイル ワークスペースがあることを確認します。 モバイル ワークスペースを公開する方法については、[モバイル ワークスペースの公開](../publish-mobile-workspace.md) を参照してください。

2. Unified Operations アプリをデバイスで開いて、Azure でホストされた開発マシンを参照し、サインインします。

3. 開発マシンでホストされる Azure で Visual Studio を開き、w3wp プロセスにデバッガーを追加します。

4. デバッガーに接続した後、目的のビジネス ロジックを見つけ、必要に応じてブレークポイントを挿入します。

5. 通常どおりデバイスでアプリを使用するか、またはデスクトップにモバイル デバイスを反映させて、デスクトップ画面でモバイル デバイスとやりとりすることが可能です。

6. 目的のワークスペースとフォームを通して移動します。

7. ブレークポイントが発生した場合、Visual Studio により実行フローの管理が可能となり、値と渡されるパラメーターが参照できるようになります。 

8. 必要な変更が指定された場合は、X++ では、それらの変更がなされ、環境にこれらの変更をプッシュします。

9. 詳細の変更や検証が必要な場合は、プロセスを繰り返します。

## <a name="additional-resources"></a>その他のリソース
### <a name="whats-new-and-in-development"></a>新機能および開発中の機能
リリースされた新機能と開発中の新機能については、[Microsoft Dynamics 365 ロードマップ](https://roadmap.dynamics.com/)を参照してください。

### <a name="blogs"></a>ブログ
Retail およびその他のソリューションに関する意見、ニュース、その他の情報については、[Microsoft Dynamics 365 blog (Microsoft Dynamics 365 ブログ)](https://community.dynamics.com/b/msftdynamicsblog) を参照してください。


