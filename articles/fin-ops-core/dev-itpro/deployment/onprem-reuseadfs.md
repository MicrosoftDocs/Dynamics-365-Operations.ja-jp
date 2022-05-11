---
title: 複数の環境への同じ AD FS インスタンスの再利用
description: このトピックでは、複数の Microsoft Dynamics 365 Finance + Operations (on-premises) 環境で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。
author: faix
ms.date: 03/03/2020
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 496b782a24efe3968b643ed199ab38fef36b61fa
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565527"
---
# <a name="reuse-the-same-ad-fs-instance-for-multiple-environments"></a>複数の環境への同じ AD FS インスタンスの再利用

[!include [banner](../includes/banner.md)]

このトピックでは、複数の Microsoft Dynamics 365 Finance + Operations (on-premises) 環境で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。

## <a name="setup"></a>設定

> [!IMPORTANT]
> この手順では、[オンプレミス環境コンテンツの設定および展開](./setup-deploy-on-premises-environments.md) コンテンツの手順に従って 1 つの環境に対して以前に AD FS が既に構成されていることを前提にしています。 また、環境が問題なく実行されていることも前提としています。

1. AD FS マネージャーで、**AD FS** \> **アプリケーション グループ** に移動し、**Microsoft Dynamics 365 for Operations オンプレミス** を開きます。
2. **ネイティブ アプリケーション** セクションで、次の手順を実行します。

    1. **Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/namespaces/AXSF`) を追加します。
    2. **Microsoft Dynamics 365 for Operations オンプレミス - Financial Reporting - ネイティブ アプリケーション** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/FinancialReporting/ApplicationService/soap/`) を追加します。

3. **Web API** セクションで、次の手順を実行します。

    1. **Microsoft Dynamics 365 for Operations オンプレミス-Web API** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/namespaces/AXSF` および `https://ax.contoso.com`) のエントリを 2 つ追加します。
    2. **Microsoft Dynamics 365 for Operations オンプレミス - Financial Reporting Web API** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/FinancialReporting`) のエントリを 2 つ追加します。

4. オプション : **サーバー** セクションで、**Microsoft Dynamics 365 for Operations オンプレミス - Retail** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/namespaces/AXSF/`) を追加します。
5. オプション: 新しい環境向けの Warehouse Mobile App を、[オンプレミスでの Warehousing アプリのコンフィグレーション](./warehousing-for-on-premise-deployments.md) で次の手順に従って構成します。 新しい環境 (`https://ax.contoso.com`) の URI を **リソース URL** 値として使用することに注意してください。

    > [!NOTE]
    > ワークフローおよびリテール デザイナー アプリケーションには、追加の構成は必要ありません。

6. 新しい環境で、OpenID メタデータ エンドポイント (`https://<adfs-dns-name>/adfs/.well-known/openid-configuration`) に **AOS** ノードおよび **MR** ノードからアクセスできることを確認します。 自己署名付き証明書を使用している場合は、AD FS Secure Sockets Layer (SSL) 証明書を各ノードの信頼済みルート証明機関ストアにインポートする必要があります。
7. Microsoft Dynamics Lifecycle Services (LCS) から新しい環境を配置し、配置構成を指定する場合は、以前の環境に対して指定したのと同じ AD FS OpenID メタデータ エンドポイントと AD FS OpenID 接続クライアント ID を使用していることを確認してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
