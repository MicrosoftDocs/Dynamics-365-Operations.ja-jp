---
title: 実験に接続しバリエーションを編集する
description: このトピックでは、サードパーティ サービスの実験を Dynamics 365 Commerce に接続する方法と実験のバリエーションを編集する方法について説明します。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2a33897d01dd98d446c2fb49e417abd9db9f403a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010027"
---
# <a name="connect-an-experiment-and-edit-variations"></a>実験に接続しバリエーションを編集する

このトピックでは、Commerce の実験に接続して、仮説にに沿うようにバリエーションを変化させる方法について説明します。 

次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。 追加の手順については、個別のトピックで説明します。

[![実験ユーザー体験 - 接続と編集](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

サードパーティ サービスで[実験を設定](experimentation-setup.md) した後、Dynamics 365 Commerce で実験を接続し、実験バリエーションを編集します。

## <a name="planning-considerations"></a>計画の考慮事項

コマースの実験を接続する前に、コンテンツのコマース管理方法に影響を与えるいくつかの決定を行う必要があります。

### <a name="determine-the-scope-of-your-experiment"></a>実験のスコープの決定
実験を接続すると、実験のスコープを定義するように求めるメッセージが表示されます。 実験は、**部分** スコープまたは **全体** スコープとして定義されます。
- ページの特定の部分で実験を実行する場合は、**部分** を選択します。 このオプションを選択した場合、実験に含まれるモジュールを識別する必要があります。 実験に関連していない既定のページまたはフラグメントの一部に加えられた変更は、バリエーション間で自動的に同期されます。
- ページ全体またはフラグメント全体で実験を実行する場合は、**全体** を選択します。 既定ページまたはフラグメントの個別のコピーが作成されます。 編集領域全体を変更できるので、実験に含まれるモジュールを選択する必要はありません。 必要に応じて、モジュールの追加、削除、並び順の変更を行うことができます。 ただし、実験が関連付けられている既定のページまたはフラグメントに変更を加えた場合は、それらの変更をすべてのバリエーションに対して手動で同期する必要があります。

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> レイアウトを使用するページに実験を関連付ける場合は、実験の範囲を **全体** として限定できます。

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>実験の発行時にスケジュール設定を行うかどうかの決定
実験をライブ サイトに発行する際のスケジュールを設定する場合は、実験に接続する *前* に、実験に関連付けるコンテンツを発行グループで使用できることを確認してください。 

公開グループの更なる詳細については、[公開グループの使用](publish-groups.md) を参照してください。


## <a name="connect-your-experiment"></a>実験の接続
実験を接続するには、**実験の接続** ウィザードを起動します。 ウィザードでは、実験に接続するために必要な手順を実行できます。 ウィザードを完了すると、実験が関連付けられ、バリエーションを作成および編集する準備ができます。

Commerce サイト ビルダーでの実験の接続を開始するには、以下の手順に従ってください。

1. **実験の接続** ウィザードを起動するには、左側のナビゲーションウィンドウで **実験** を選択し、**接続** を選択します。 別の方法として、ページやフラグメント エディターからウィザードにアクセスするには、このウィザードを編集し、コマンドバーの **実験に接続する** を選択します。

    > [!NOTE]
    > ページは、一度に 1 つの実験にのみ関連付けることができます。 ページを異なる実験に関連付けるには、最初にページが現在接続されている実験を削除します。

1. 実験を実行するページまたはフラグメントを選択します。
1. 上記の [実験のスコープを決定](#determine-the-scope-of-your-experiment) セクションで行った選択に基づき、実験スコープを **部分** または **全体** に設定します。
    > [!NOTE]
    > 全ページまたはフラグメントで実験する場合、**ページまたはフラグメントの実験** 機能フラグを有効にする必要があります。 詳細については、[Dynamics 365 Commerce の実験](experimentation-overview.md) トピックを参照してください。
    
1. ウィザードの最終手順で、**バリエーションの生成およびウィザードの終了** を選択します。 実験に対してバリエーションが作成されます。 

## <a name="edit-your-variations"></a>バリエーションの編集
ウィザードを終了すると、バリエーションが作成されます。 

次に、実験仮説で検証の必要がある選択を反映するようにバリエーションを編集します。 上記[実験スコープを決定](#determine-the-scope-of-your-experiment) セクションで、実験に対して選択したスコープに対応する次の手順のいずれかを選択します。

### <a name="edit-variations-for-experiments-with-partial-scope"></a>部分的スコープの実験バリエーションの編集
**実験を接続** ウィザードの **部分** として実験のスコープを決定する場合は、次の手順に従います。

1. 編集ビューでは、コマンド バーの下にあるバリエーション ドロップダウン メニューを使用して、元の仮説に基づき各バリエーションを編集します。 バリエーションのいずれかを変更しないで、コントロールまたは基本バリエーションを設定することもできます。
1. 実験したモジュールを選び、省略記号 (...) から **実験に追加** の順に選択します。

### <a name="edit-variations-for-experiments-with-entire-scope"></a>全体スコープの実験バリエーションの編集
編集ビューで、**実験の接続** の **全体** となる実験のスコープを決定したら、コマンドバーの下にあるバリエーション ドロップダウン メニューを使用して、元の仮説に基づき各バリエーションを編集します。 

> [!NOTE]
> どちらの場合でも、バリエーションのいずれかを変更しないで、コントロールまたは基本バリエーションを設定することもできます。

## <a name="previous-step"></a>前のステップ
[実験の設定](experimentation-setup.md) 


## <a name="next-step"></a>次のステップ
[実験のプレビューと公開](experimentation-preview-publish.md)
