---
title: 開発マシンでの新しいユーザーの作成
description: 環境が最初に配置されるとき、1 つのユーザー アカウントのみが仮想マシン (VM)上で開発者として有効になります。 この記事では、開発者が開発 VM に別のユーザー アカウントを有効にする方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 07/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 31621
ms.assetid: c56d5cdf-3c01-4730-bda5-bb5f8f79e375
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6e6d3e5cc7029dea16847d90bf051215cc6bca4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191688"
---
# <a name="create-new-users-on-development-machines"></a>開発マシンでの新しいユーザーの作成

[!include [banner](../includes/banner.md)]

この記事では、開発者が開発 VM に別のユーザー アカウントを有効にする方法について説明します。

> [!NOTE]
> このトピックは、ダウンロードされたローカル仮想マシン (VM) か、顧客のサブスクリプションでホストされている VM にのみ適用されます。 開発者が VM への管理者アクセスを持たない Microsoft が管理する開発およびビルド マシン (プラットフォーム更新 12 以降) において、新しいユーザーを作成することはできません。

環境が最初に配置されるとき、1 つのユーザー アカウントのみが仮想マシン (VM)上で開発者として有効になります。 このユーザーは、Microsoft Dynamics Lifecycle Services (LCS) によって事前設定するか、ダウンロードした仮想ハードディスク (VHD) のローカル管理者のアカウントです。 ただし、新しいユーザー アカウントを VM で開発できます。 新しいアカウントを有効にした後でも、同じ VM/アプリケーションで一度に開発できる開発者は 1 人だけです。


## <a name="prerequisites"></a>前提条件
新しいユーザー アカウントが VM で開発できるようにするには、ユーザー アカウントが VM の管理者である必要があります。 また、既定の開発者アカウントの資格情報を使用して VM にログオンする必要があります。 VM が Microsoft Azure VM である場合は、この勘定の情報は LCS の環境のページで使用できます。 VM がダウンロードした VHD 上で実行されるローカル VM である場合は、ローカル管理者アカウントを使用します。 詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。

## <a name="steps"></a>ステップ
1.  スクリプト ProvisionAxDeveloper.ps1 をダウンロードしてください。スクリプトは、<https://github.com/Microsoft/Dynamics-AX-Scripts> で利用可能です。
2.  Microsoft Windows PowerShell **コマンド プロンプト** ウィンドウを管理者として開きます。
3.  ProvisionAxDeveloper.ps1 スクリプトを実行します。 次のパラメーターを指定します。

    -   **DatabaseServerName** - 通常、これは、コンピューター名です。
    -   **ユーザー** – 次の形式を使用します: &lt;ドメインまたはコンピューター名&gt;\\ユーザー 1、… &lt;ドメインまたはコンピューター名&gt;\\ユーザー n

    **例**

        > ProvisionAxDeveloper.ps1 RDXP00DB20RAINM RDXP00DB20RAINM\username1

        > ProvisionAxDeveloper.ps1 -databaseservername RDXP00DB20RAINM -users RDXP00DB20RAINM\username1,RDXP00DB20RAINM\username2

4.  1 つ以上のユーザー アカウントが同じバージョン管理ワークスペース上で開発されている場合、ワークスペースをパブリックにする必要があります。
    1.  Visual Studio で、**ソース管理エクスプローラー**を開き、ワークスペース ドロップダウンを選択し、**ワークスペースの管理**を選択します。
    2.  アプリケーション ワークスペースを選択して、**編集** をクリックし、**詳細** をクリックしてワークスペースを **パブリック ワークスペース**.[![publicworkspace](./media/publicworkspace.png)](./media/publicworkspace.png) にせっていします





