---
title: モバイル ワークスペースのセキュリティを強化する
description: このトピックでは、ワークスペースへのユーザー アクセスを制限する方法について説明します。
author: tonyafehr
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 627494055dda16f703fd25c83a0ca58a2aa118f8
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782005"
---
# <a name="help-secure-mobile-workspaces"></a>モバイル ワークスペースのセキュリティを強化する

[!include [banner](../../../includes/banner.md)]

このトピックでは、ワークスペースへのユーザー アクセスを制限する方法について説明します。

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