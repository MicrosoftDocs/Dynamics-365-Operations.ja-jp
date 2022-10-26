---
title: Invoice Capture ソリューションをインストールする
description: この記事では、Invoice Capture をインストールして、Microsoft Dynamics 365 Finance と統合する方法についての情報を提供します。
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691231"
---
# <a name="install-the-invoice-capture-solution"></a>Invoice Capture ソリューションをインストールする

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> プライベート プレビューにこのソリューションをインストールした場合は、続行する前に古いソリューションをアンインストールする必要があります。

## <a name="prerequisites"></a>必要条件

Invoice Capture ソリューションをインストールできる前に、以下の前提条件を完了する必要があります。

1. アプリケーションを登録して、Azure サブスクリプション下の Microsoft Azure Active Directory (Azure AD) にクライアント シークレットを追加します。 詳細については、[ウェブ アプリケーションを AAD と登録する](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad) をご覧ください。

    > [!NOTE]
    > **アプリケーション (クライアント) ID**、**クライアント シークレット**、**テナント ID** の値は後で必要になるので、メモしておいてください。

2. Azure アプリケーションを Dynamics 365 Finance 環境に登録します。 詳細については、[外部アプリケーションを登録する](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application) をご覧ください。

## <a name="install-and-set-up-the-solution"></a>ソリューションのインストールと設定

Invoice Capture ソリューションをインストールするには、AppSource に移動して、[Dynamics 365 Invoice Capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture) のプレビュー バージョンのリンクを選択します。 インストールが完了した後、Power Apps で選択した環境でソリューションがインストールされたことがわかります。

このセットアップを完了するには、以下の手順に従ってください。

1. [アシスタント ソリューション](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) をダウンロードして、次の詳細を設定します。

    - Microsoft Power Platform と Finance 環境との間のコミュニケーション
    - チャンネルで使用する Dataverse と Office 365 Outlook の接続参照

2. Power Apps で、自分の環境に移動して、**ソリューションのインポート** を選択します。
3. **ブラウザー** を選択して、ダウンロードしたアシスタント ソリューションを選択して、**次へ** を選択します。
4. **次へ** を選択します。
5. 既存の接続を割り当てるか、**新規接続** を選択して新しい接続を作成します。
6. パッケージのインポートが完了した後、**Dynamics 365 Invoice Capture – インストレーション ツール** を開きます。
7. クラウド フローを実行して、Microsoft Power Platform と Finance の Invoice Capture 感での接続を設定します。
8. **実行** を選択し、次のパラメータを指定します。

    - **Dynamics 365 Finance URL** - 統合する Finance 環境の URL。
    - **テナント ID** – Finance 環境のテナント ID。
    - **クライアント ID** - 登録された Azure アプリケーション ID。
    - **クライアント シークレット** – Azure アプリケーションのために生成されたクライアント シークレット。
