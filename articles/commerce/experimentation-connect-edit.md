---
title: 実験に接続しバリエーションを編集する
description: この記事では、サードパーティ サービスの実験を Dynamics 365 Commerce に接続する方法と実験のバリエーションを編集する方法について説明します。
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942825"
---
# <a name="connect-an-experiment-and-edit-variations"></a>実験に接続しバリエーションを編集する

この記事では、Commerce の実験に接続して、仮説にに沿うようにバリエーションを変化させる方法について説明します。 

次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。 追加の手順については、個別の記事で説明します。

[![実験ユーザー体験 - 接続と編集。](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

サードパーティ サービスで[実験を設定](experimentation-setup.md) した後、Dynamics 365 Commerce で実験を接続し、実験バリエーションを編集します。

## <a name="connect-your-experiment"></a>実験の接続
実験を接続するには、**実験の接続** ウィザードを起動します。 ウィザードでは、実験に接続するために必要な手順を実行できます。 ウィザードを完了すると、実験が関連付けられ、バリエーションを作成および編集する準備ができます。

Commerce サイト ビルダーでの実験の接続を開始するには、以下の手順に従ってください。

1. **実験の接続** ウィザードを起動するには、左側のナビゲーションウィンドウで **実験** を選択し、**接続** を選択します。 別の方法として、ページやフラグメント エディターからウィザードにアクセスするには、このウィザードを編集し、コマンドバーの **実験に接続する** を選択します。

    > [!NOTE]
    > - ページは、一度に 1 つの実験にのみ関連付けることができます。 ページを異なる実験に関連付けるには、最初にページが現在接続されている実験を削除します。
    > - カスタム レイアウトを使用してのみページで実験ができます。 ページにプリセット レイアウトがある場合は、先にカスタム レイアウトに変換します。 この操作を実行するには、ページに移動し、コマンド バーで **カスタム レイアウトに変換** を選択します。 レイアウトの詳細については、[プリセットとカスタムのレイアウト](templates-layouts-overview.md#preset-and-custom-layouts) を参照してください。 

1. 左ナビゲーション ウィンドウの **実験** タブから実験に接続する場合は、表示される一覧から実験名を選択します。
1. 実験を実行するページまたはフラグメントを選択します。
1. ウィザードの最終手順で、**バリエーションの生成およびウィザードの終了** を選択します。 実験に対してバリエーションが作成されます。 

> [!NOTE]
> 実験をライブ サイトに発行する際のスケジュールを設定する場合は、実験に接続する *前* に、実験に関連付けるコンテンツを発行グループで使用できることを確認してください。 公開グループの更なる詳細については、[公開グループの使用](publish-groups.md) を参照してください。

## <a name="edit-your-variations"></a>バリエーションの編集

**実験の接続** ウィザードを終了すると、バリエーションが作成されます。 次の手順に従って、実験仮説で検証する必要がある選択を反映するようにバリエーションを編集します。

1. 編集ビューでは、コマンド バーの下にあるバリエーション ドロップダウン メニューを使用して、元の仮説に基づき各バリエーションを編集します。 バリエーションのいずれかを変更しないで、コントロールまたは基本バリエーションを設定することもできます。
1. 実験したモジュールを選び、省略記号 (...) から **実験に追加** の順に選択します。

> [!NOTE]
> バリエーションのいずれかを変更しないで、コントロールまたは基本バリエーションを確立することを検討してください。

## <a name="previous-step"></a>前のステップ
[実験の設定](experimentation-setup.md) 


## <a name="next-step"></a>次のステップ
[実験のプレビューと公開](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
