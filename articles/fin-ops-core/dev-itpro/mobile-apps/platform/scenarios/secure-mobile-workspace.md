---
title: モバイル ワークスペースのセキュリティを強化する
description: この記事では、ワークスペースへのユーザー アクセスを制限する方法について説明します。
author: jasongre
ms.date: 05/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.custom: 255544
ms.assetid: ''
ms.openlocfilehash: df12dc63daa332a1dee6d5afef4dd3a78b46c53e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275359"
---
# <a name="help-secure-mobile-workspaces"></a>モバイル ワークスペースのセキュリティを強化する

[!include [banner](../../../includes/banner.md)]
[!include [mobile app deprecated](../../../includes/mobile-app-deprecation-banner.md)]

この記事では、ワークスペースへのユーザー アクセスを制限する方法について説明します。

## <a name="assign-a-menu-item-to-workspace"></a>メニュー項目をワークスペースに割り当てる
ワークスペースはメニュー項目に関係させることができます。 ワークスペースはメニュー項目への権限を持つユーザーにのみ表示されるため、メニュー項目へのアクセス権がないユーザーは、ワークスペースを使用できません。

メニュー項目がワークスペースに割り当てられていない場合、ワークスペースは常にユーザーに表示されます。

メニュー項目を割り当てることによってワークスペースのセキュリティを確保するには、これらの手順に従います。

1. **SysAppWorkspaceSecurityAttribute** 属性をワークスペース クラスに追加して、ワークスペースに割り当てるメニュー項目を指定します。

    ![メニュー項目をワークスペースに割り当てます。](media/workspace-api/SecureWorkspaceOption1.png)

2. メニュー項目とワークスペースを構築します。 変更をテストするには、メニュー項目にアクセスできないユーザー アカウントを使用してモバイル アプリにサインインします。

## <a name="override-the-workspacehidden-method"></a>WorkspaceHidden メソッドのオーバーライド
パラメーターに基づき、ワークスペースを非表示または表示するか指定することもできます。 **workspaceHidden** メソッドを上書きすることにより、次のコード例に示すように、コードでワークスペースの可視性を制御できます。

![workspaceHidden メソッドをオーバーライドします。](media/workspace-api/SecureWorkspaceOption2.png)

## <a name="add-a-menu-item-and-override-the-workspacehidden-method"></a>メニュー項目を追加して、workspaceHidden メソッドを上書きする
アプリで両方の先行メソッドを使用することができます。 メニュー項目はセキュリティ チェックを提供し、**workspaceHidden** メソッドには、ワークスペースの可視性に関連する追加ロジックが含まれています。


[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
