---
title: 拡張機能を使用して、フォーム コントロールのプロパティを変更する
description: このトピックでは、拡張機能を使用してコントロールのプロパティを変更する方法について説明します。
author: ivanv-microsoft
ms.date: 07/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 01e2de54acb418b44d01f7a3e345ee5081aa31a3
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866256"
---
# <a name="modify-the-properties-of-form-controls-through-extension"></a>拡張機能を使用して、フォーム コントロールのプロパティを変更する

[!include [banner](../includes/banner.md)]

多くの場合、ユーザーがアプリとやりとりするには、変更が必要です。 通常、ページ上のコントロールを非表示または無効にしたり、標準ラベルをより適切なラベルに置き換えたり、ユーザーが必要とする新しいコントロールを追加したりします。 また、フォーム拡張子を作成することもできます。 

> [!TIP]
> フォーム コントロール イベント上のイベント サブスクリプションを使用して、より高い柔軟性を実現することができます。 この方法については、他のトピックで説明します。 このトピックでは、メタデータの変更に焦点を当てます。

## <a name="example"></a>例

顧客は **リリース済製品の詳細** ページの **在庫の管理** クイック タブへの変更が必要です。 クイック タブのラベルを変更、CW 構成を表示するフィールド グループを無効化、および新しいコントロールを追加する必要があります。 (この例では、新しいコントロールはデータ ソース内の既存のフィールドにバインドされません)。

必要な変更を行うには、これらの手順に従います。

1. 拡張モデルでは、**EcoResProductDetailsExtended** フォームの拡張機能を作成します。
2. フォーム デザイン ツリーを通じて、**TabPageInventory** タブ ページ (**デザイン** &gt; **タブ** &gt; **詳細** &gt; **GroupDetails** &gt; **TabHeader** &gt; **TabPageInventory**) に移動し、デザイナーでそれを選択して、**プロパティ** シートを開きます。
3. **キャプション** プロパティを目的の値に更新します。

    ![キャプション プロパティ](media/ModifyControlProperties01.jpg)

4. タブ ページを右クリックし、**新規** を選択します。 新しいコントロールで必要なプロパティを設定します。 また、すぐそばのコンテナでコントロールを上下に移動して、適切に配置することができます。

    > [!NOTE]
    > または、新しいコントロールに表示するサブノードを右クリックし、**Insert sibling** を選択し、追加するコントロールのタイプを選択します。

    ![兄弟コマンドの挿入](media/ModifyControlProperties02.jpg)

    もちろん、対応するデータ ソースからバインドされたコントロールをドラッグすることもできます。

5. **PdsCatchWeight** グループ コントロールをオンにし、**有効** プロパティを **いいえ** に変更します。

    ![PdsCatchWeight グループ コントロールのプロパティを有効化](media/ModifyControlProperties03.jpg)

    > [!NOTE]
    > **有効** および **表示** のようにメタデータのプロパティを変更した場合、実行時にその状態のままでコントロールの保証はありません。 フォームが読み込まれた後、そのフォームのビジネス ロジックは、コードを使用してコントロールの状態を変更できます。

完了したら、ページには追加のフィールドが含まれ、CW 情報を編集することはできず、クイック タブ全体のキャプションが異なります。 

![変更されたクイック タブ](media/ModifyControlProperties04.jpg)

> [!NOTE]
> コントロールで **AutoDeclaration** プロパティを変更することはできません。 ただし、コードから名前でコントロールにアクセスすることはできます。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]