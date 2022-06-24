---
title: Lifecycle Services でのマイクロサービス向けアドインのインストール
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) に、電子請求アドインをインストールする手順を説明します。
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 26f92262eff07ded3e894ee5513dd8dbaa6f94a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849808"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Lifecycle Services にマイクロサービス向けのアドインをインストールします

[!include [banner](../includes/banner.md)]

電子請求サービスで認証を行うには、ご使用の環境用のアドインを Microsoft Dynamics Lifecycle Services (LCS) にインストールして、Microsoft Dynamics 365 Finance または Dynamics 365 Supply Chain Management 環境をサービス プラットフォームに登録する必要があります。

環境を登録するには、次の手順に従います。

1. LCS アカウントにサインインします。
2. プロジェクト ダッシュボードで、LCS プロジェクトを選択します。
2. プロジェクトの **環境** ダッシュボードで、配置された環境を選択します。 選択する環境は実行中である必要があります。
3. **Power Platform 統合** タブの **環境アドイン** セクションで、**新しいアドインをインストールする** を選択します。
4. **電子請求** を選択します。
5. **AAD アプリケーション ID** フィールドに、**091c98b0-a1c9-4b02-b62c-7753395ccabe** を入力します。 この値は固定値です。 グローバル一意識別子 (GUID) だけを入力してください。 スペース、コンマ、ピリオド、引用符など、他の記号を含めないでください。
6. **AAD のテナント ID** フィールドに、Azure のサブスクリプション アカウントのテナント ID を入力します。 指定する Azure Active Directory (Azure AD) テナントは、Regulatory Configuration Service (RCS) に使用されるテナントと同じである必要があります。
7. 使用条件を確認して、チェックボックスを選択します。
8. **インストール** を選択します。 数分後、状態が **インストール中** から **インストール済** に変わります。 この変更を表示するには、ページの更新が必要となる場合があります。

電子請求を使用する準備が整いました。

> [!NOTE]
> 通常、会社には複数の Finance または Supply Chain Management 環境があります。 これらの環境には、運用環境、ユーザー受入テスト (UAT) 環境、および開発 (サンドボックス) 環境があります。 電子請求に接続する環境すべてについて、前述の手順を完了する必要があります。
