---
title: 電子商取引のメンテナンス モードの有効化とアクティブ化
description: このトピックでは、Microsoft Dynamics 365 Commerce において eコマースのメンテナンス モードを有効化およびアクティブ化し、オプションのカスタム メンテナンス モード ページを構築する方法について説明します。
author: samjarawan
ms.date: 03/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ec995cfbf19eb5e39fccfa4ee4d23cfc0e92c256
ms.sourcegitcommit: 293df12697166556b1da0c9a34d2d8679dc8c0a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2022
ms.locfileid: "8397928"
---
# <a name="enable-and-activate-e-commerce-maintenance-mode"></a>電子商取引のメンテナンス モードの有効化とアクティブ化

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce において eコマースのメンテナンス モードを有効化およびアクティブ化し、オプションのカスタム メンテナンス モード ページを構築する方法について説明します。

メンテナンス モードは、通常、サイト開発などのためにサイトを一時的に停止する必要がある場合に、eコマース サイト全体へのアクセスをブロックするために使用されます。 メンテナンス モードが有効な場合、既定の静的メンテナンス モード ページが表示されます。 カスタム メンテナンス モード ページを作成することもできます。

## <a name="enable-and-activate-maintenance-mode"></a>メンテナンス モードの有効化とアクティブ化

Commerce サイト ビルダーでメンテナンス モードを有効化およびアクティブ化するには、次の手順に従います。

1. サイト ビルダーで、サイトに移動します。 
1. 左のナビゲーション ウィンドウで、 **サイト設定** の下で、**拡張機能** を選択します。
1. **メンテナンス モード** チェック ボックスを選択して、メンテナンス モードを有効にします。
1. アクション ウィンドウで、**保存して公開** を選択して、メンテナンス モードをアクティブ化します。

メンテナンス モードを有効化およびアクティブ化されると、次の図に示すように、eコマース サイトを参照するユーザーに対して既定のメンテナンス モード ページが表示されます。

![eコマース サイトの既定のメンテナンス モード ページ。](media/maintenance-mode_1.png)

## <a name="create-a-custom-maintenance-mode-page"></a>カスタム メンテナンス モード ページを作成する

サイト ビルダーでカスタム メンテナンス モード ページを作成するには、次の手順を実行します。

1. サイト ビルダーで、新しいカスタム メンテナンス モード ページを作成します。 サイト ページの作成方法については、[新しいサイト ページの追加](add-new-page.md)を参照してください。 次の図は、例を示します。

    ![サイト ビルダーでカスタム ページを作成しています。](media/maintenance-mode_2.png)

1. 左ナビゲーションで、**URL** を選択してから、アクション ウィンドウで、**新規 \> 新しいエイリアス** を選択して新しいエイリアスを作成します。
1. **新しいエイリアス** ダイアログ ボックスで、新しいメンテナンス モード ページを選択してから、**エイリアス** フィールドに **既定のメンテナンス** をエイリアス名として入力します。
1. カスタム メンテナンス モード ページを公開します。

これらの手順が完了し、メンテナンス モードを有効化されると、次の例に示すように、サイト ユーザーに対してカスタム メンテナンス モード ページが表示されます。

![カスタム メンテナンス ページの例。](media/maintenance-mode_3.png)
