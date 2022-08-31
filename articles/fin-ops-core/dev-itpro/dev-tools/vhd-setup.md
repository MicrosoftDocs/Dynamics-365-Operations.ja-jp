---
title: 最初に使用する際にダウンロードできる VHD を設定する
description: この記事では、Application Object Server を最初に使用するためにダウンロード可能な VHD を設定する方法について説明します。
author: gianugo
ms.date: 02/17/2022
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.openlocfilehash: f6136cda0ca89ad722e558f3726c09d66097f4c0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271011"
---
# <a name="set-up-the-downloadable-vhd-for-first-use"></a>最初に使用する際にダウンロードできる VHD を設定する

[!include [banner](../includes/banner.md)]

> [!NOTE]
> この記事は、バージョン 10.0.24 以降にリリースされた仮想ハード ドライブ (VHD) に適用されます。

仮想マシンに最初にサインインしたとき、**Application Object Server** を使用することはできません。 仮想マシンで使用する自己署名証明書と顧客が指定した認証用のアプリケーション登録 ID を作成するスクリプトを実行する必要があります。 スクリプトが正常に実行されると、環境は使用できるようになります。

## <a name="register-a-new-application-in-azure-active-directory"></a>Azure Active Directory で新しいアプリケーションを登録する

Microsoft Azure Active Directory (Azure AD) で新しいアプリケーションを登録する場合、[アプリまたは Web API を登録する](/azure/active-directory/develop/quickstart-register-app)で説明している手順に従います。 新しいアプリの登録は Web アプリケーションに対して行う必要があり、次のリダイレクト URI を追加する必要があります。

- `https://usnconeboxax1aos.cloud.onebox.dynamics.com/`
- `https://usnconeboxax1aos.cloud.onebox.dynamics.com/oauth/`

作成されると、**アプリケーション (クライアント) ID** をメモします。

## <a name="run-the-setup-script"></a>設定スクリプトを実行する

**管理者** アカウントでサインインした後、デスクトップ ショートカットの **自己署名証明書生成** を右クリックし、**管理者として実行** を選択します。 スクリプトがアプリケーション ID にプロンプトを表示する場合、Azure Active Directory で作成された **アプリケーション (クライアント) ID** を提供します。

スクリプトが完了すると、環境を使用することができます。 現時点では、管理者プロビジョニング ツールを実行して、管理者アカウント、アクセス許可、およびテナントを設定することができます。 電子メールがアプリケーションの登録が作成された Azure Active Directory テナントに対するものであることを確認します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
