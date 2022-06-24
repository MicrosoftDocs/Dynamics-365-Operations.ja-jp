---
title: レべル 1 Retail Server 仮想マシンに対してデバッグする eコマースの開発環境の設定
description: この記事では、レべル 1 Retail Server 仮想マシン (VM) に対してデバッグする eコマースの開発環境を設定する方法について説明します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7cc6c936c67bc82da1a237341ac07fb69d4ac233
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855705"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>レべル 1 Retail Server 仮想マシンに対してデバッグする eコマースの開発環境の設定

[!include [banner](../../includes/banner.md)]

この記事では、レべル 1 Retail Server 仮想マシン (VM) に対してデバッグする eコマースの開発環境を設定する方法について説明します。

## <a name="description"></a>説明

Microsoft Dynamics 365 Commerce レベル 1 環境は、通常 Commerce Runtime (CRT) と販売時点管理 (POS) 拡張機能開発用に配置されます。 これらはスタンドアロンの環境です。 アーキテクチャにおけるサービスとしてのソフトウェア (SaaS) の性質のため、eコマース コンポーネントは含まれていません。

一部のシナリオでは、レベル 1 環境の拡張機能への呼び出しをテストして、eコマース コンポーネントから拡張機能をデバッグすることができます。 一般的は手順については、[レベル 1 の Commerce 開発環境に対するデバッグ](../e-commerce-extensibility/debug-tier-1.md) を参照してください。

レベル 1 環境に対してデバッグする場合、サイトが別の Retail Server を呼び出しているため、サーバー間の呼び出しによって、コンテンツ セキュリティ ポリシーに関連するさまざまなエラーが発生する可能性があります。

次の図は、製品の詳細ページでバリアントが選択されたときに発生する可能性があるエラーの例を示しています。

![製品の詳細ページでバリアントが選択されたときのエラー。](media/unhandled-rejection-error.jpg)

次の図では、ブラウザーのデバッガー ツール (F12 開発者ツール) における同様のエラーの例を示しています。 このエラー メッセージには、コンテンツ セキュリティ ポリシー ディレクティブの違反を示しています。

![デバッガー ツールのエラー。](media/debugger-tools-error.JPG)

## <a name="resolution"></a>解決策

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Commerce サイト ビルダーでサイトのコンテンツ セキュリティ ポリシーを無効にする

1. 作業しているサイトを選択します。
1. **設定** を選択し、**拡張機能** を選択します。
1. **コンテンツ セキュリティ ポリシー** タブで、**コンテンツ セキュリティ ポリシーを無効にする** を選択します。
1. **保存と公開** を選択します。

> [!NOTE]
> 企業と顧客間 (B2C) サインインは、ローカルの開発環境では機能しません。 ただし、必要に応じてゲスト チェックアウトを使用するか、ページ モックを作成して、ユーザーのサインインをシミュレートできます。

## <a name="additional-resources"></a>追加リソース

[eコマース オンライン拡張機能の開発を開始する](../e-commerce-extensibility/sdk-getting-started.md)

[eコマース サイトでのコンテンツ セキュリティ ポリシー (CSP) の管理](../manage-csp.md)
