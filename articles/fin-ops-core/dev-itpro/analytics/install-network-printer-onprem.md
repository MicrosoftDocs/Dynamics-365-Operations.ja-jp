---
title: オンプレミス環境でのネットワーク プリンター デバイスのインストール
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) のオンプレミス展開を既存のネットワーク プリンター デバイスに接続する方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCorpNetPrinterList
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 76cc7dc6b5edd001ee6c88a2dbedab7df83521fd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183405"
---
# <a name="install-network-printer-devices-in-on-premises-environments"></a>オンプレミス環境でのネットワーク プリンター デバイスのインストール

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) のオンプレミス展開を既存のネットワーク プリンター デバイスに接続する方法について説明します。 オンプレミス アプリケーションでのネットワーク印刷は、Microsoft Windows Server 2016 の「[印刷およびドキュメント サービス](https://technet.microsoft.com/library/hh831468(v=ws.11).aspx)」機能でサポートされます。 この機能を使用すると、プリンター管理に関連するタスクを集中管理できます。 印刷およびドキュメント サービスをインストールして構成するには、Application Object Server (AOS) のプライマリー インスタンスをホストするサーバーへの管理アクセス権が必要です。

ネットワーク印刷サービスの構成には、次の 2 つの役割があります。

- **サービス管理者** – この役割を持つ担当者は、インストールやプラットフォーム インフラストラクチャのコンポーネントのコンフィギュレーションを担当します。 従来、この役割は昇格したドメイン権限を持った Active Directory アカウントです。 Microsoft Windows Server のコンポーネントのインストールに必要な権限があります。
- **組織の管理者** – このロールを持つユーザーはアプリケーション セキュリティ権限を管理します。 この Active Directory アカウントは、**システム管理者** ロールに割り当てられています。

組織の管理者がネットワーク プリンターの追加を開始する前に、サービス管理者はプライマリ AOS インスタンスをホストするサーバーに印刷およびドキュメント サービスをインストールして構成する必要があります。 組織の管理者は、組み込みツールを使用してネットワーク プリンター デバイスの設定を開始できます。

## <a name="install-and-configure-print-and-document-services"></a>印刷およびドキュメント サービスのインストールと構成

環境管理者は、このセクションの情報を使用してネットワーク印刷サービスを有効にします。

1. [印刷およびドキュメント サービスのインストール](https://technet.microsoft.com/library/jj134159(v=ws.11).aspx)の手順に従って印刷およびドキュメント サービスをインストールします。
2. 次の手順に従って印刷およびドキュメント サービスをコンフィギュレーションします [印刷およびドキュメント サービスのコンフィギュレーション](https://technet.microsoft.com/library/jj134163(v=ws.11).aspx)。
3. AXService アプリケーションをホストするために使用する各サーバーに対して、これらの手順に従います。

    1. ローカル サーバーで、**ローカル ユーザーとグループ**マネージャーを開始します。
    2. **グループ** ノードを選択します。
    3. **出力演算子** を右クリックし、**グループへの追加** を選択します。
    4. グループに AXService アプリケーションを実行するために使用されるネットワーク Active Directory アカウントを追加します。
    5. AXService ユーザー アカウントを使用してネットワーク プリンターをインストールします。 このステップにより、プリンター ドライバーが AXService ユーザー アカウントで使用できることが保証されます。
    6. すべての接続が正しく構成されていることを確認するため、インストールされているプリンターのテスト ページを印刷します。
    7. ユーザーのプロファイルが正しく読み込まれることを保証し、プリンターを参照できるようにするために、AXService アプリケーションを再起動します。

## <a name="manage-network-printers"></a>ネットワーク プリンターの管理

システム管理者は、このセクションの情報を使用してネットワーク プリンターを定義します。

1. **組織管理** \> **設定** \> **ネットワーク プリンター** の順に移動します。
2. **ネットワーク プリンター**ページで、新しいプリンターを追加します。 各プリンターで、名前、説明、パス、およびステータスを指定します。 プリンター パスがインストールされているプリンターのネットワーク パスと一致していることを確認します。

**有効**とマークされている項目は、すぐにアプリケーションのユーザーによって利用できるようになるので、ネットワーク プリンター デバイスで文書スタイル レポートの印刷を開始できます。
