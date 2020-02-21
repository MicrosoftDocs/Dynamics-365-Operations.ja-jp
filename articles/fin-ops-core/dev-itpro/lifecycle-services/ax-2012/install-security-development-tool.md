---
title: セキュリティ開発ツールをインストールする
description: このトピックでは、セキュリティ開発ツールのインストール方法について説明します。
author: kfend
manager: AnnBe
ms.date: 07/26/2018
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 18391
ms.assetid: f62f5636-4d63-473e-b326-277ea500c540
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 1e8f6d2f8ef112cdc2100707998c15dc965248a4
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983746"
---
# <a name="install-the-security-development-tool"></a>セキュリティ開発ツールをインストールする

[!include [banner](../../includes/banner.md)]

> [!NOTE] 

> これは、予備的なプレリリース ドキュメントで、予告なしに変更される場合があります。 ここで提供されている情報の正確さは保障されていません。 セキュリティ開発ツールをインストールする前に、次の前提条件を満たしていることを仮定します。

-   Microsoft Dynamics AX 2012 の開発環境を使い慣れています。
-   Microsoft Dynamics AX 2012 のセキュリティ モデルを使い慣れています。
-   Microsoft Dynamics AX の開発者権限を持っている場合、アプリケーション オブジェクト ツリー (AOT) からツールを実行できるようにします。

> [!IMPORTANT] 
> セキュリティ開発ツールの一部のオプション機能では、フレームワーク クラスを変更したり、その追跡を有効にする必要があります。 これらの変更は、Microsoft Dynamics AX システムの全体的なパフォーマンスに影響する可能性があります。 したがって、このツールは開発環境またはテスト環境でのみ使用することをお勧めします。

## <a name="procedures"></a>手順
このセクションでは、セキュリティ開発ツールのインストールと設定に必要なステップを示します。

### <a name="install-the-tool"></a>ツールのインストール

1.  SecurityDevelopmentTool.msi フォームを「[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com)」の Downloadable ツールからダウンロードします (Microsoft のアカウントでログインする場合のみ Downloadable ツールはアクセス可能です。組織アカウントでサインインすると表示されませんので注意してください)
2.  **SecurityDevelopmentTool.msi** を実行して**インストール ウィザード**を開きます。
3.  Microsoft ソフトウェア ライセンス条件に同意し、**インストール**をクリックします。
4.  ツールが正常にインストールされたことを示すメッセージが表示されたら、**完了** をクリックします。 **インストール** **ウィザード**の実行が完了すると、ファイルは次の場所で使用できます。
    -   64 ビット システム用: %ProgramFiles (x86)%Microsoft%Security 開発ツール
    -   32 ビット システム用: %ProgramFiles%Microsoft%Security 開発ツール

### <a name="import-and-compile-the-tool"></a>ツールのインポートおよびコンパイル

1.  使用している Application Object Server (AOS) のインスタンスからクライアント接続を排除します。 詳細については、[AOS からユーザーを排除](https://technet.microsoft.com/library/hh433538.aspx) を参照してください。
2.  **管理ツール**に移動し、**サービス**をクリックし、**Microsoft Dynamics AX Object Server 6.0** サービスを停止します。
3.  Windows PowerShell または AXUtil を使用して、**SecurityDevelopmentTool.axmodel** モデルを Microsoft Dynamics AX AOT にインポートします。
    1.  スタートメニューで、**すべてのプログラム**をポイントし、**管理ツール**をポイントして、**Microsoft Dynamics AX 管理シェル**をクリックします。
    2.  Windows PowerShell コマンド プロンプト PS C:&gt; で、次のコマンドを入力して Enter キーを押します。

            Install-AXModel -File “C:\Program Files (x86)\Microsoft\Security Development Tool\SecurityDevelopmentTool.axmodel”

        詳細については、「[方法: モデルのエクスポートとインポート](https://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx)」を参照してください。

4.  Microsoft Dynamics AX Object Server 6.0 サービスを開始します。
5.  Microsoft Dynamics AX クライアントを起動します。 モデル ストアが変更されました。ダイアログ ボックスが開きます。
6.  **コンパイルして同期**をクリックします。
7.  同期が完了したときに、**Ctrl+Shift+W** を押して、開発ワークスペースを開きます。
8.  **SysSecEntryPointManagerSetup** クラスを実行して以下のメニュー項目を標準  Microsoft Dynamics AX メニューに追加します。

    | メニュー項目                     | メニュー                               |
    |-------------------------------|------------------------------------|
    | SysSecRoleEntryPointDeveloper | SysContextMenu (AOT アドイン)       |
    | SysSecRoleEntryPoint          | システム管理設定セキュリティ |
