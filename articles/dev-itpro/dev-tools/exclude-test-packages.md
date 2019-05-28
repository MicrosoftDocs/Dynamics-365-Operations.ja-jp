---
title: ビルド出力からテスト パッケージを除外
description: このトピックでは、自動ビルドプロセスが生成するビルド出力で、特定のパッケージが展開可能パッケージに含まれないようにする方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 05/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 26731
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3452f9a8fb317ce9948d56153515c6f2d3572f1c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536990"
---
# <a name="exclude-test-packages-from-build-output"></a>ビルド出力からテスト パッケージを除外

[!include [banner](../includes/banner.md)]

プラットフォーム更新プログラム 4 では、自動ビルド プロセスにより、ビルド出力で特定のパッケージが配置可能パッケージに含まれないようにできます。 この機能は、自動化されたテストを使用する顧客にとって重要なことです。 これらの顧客は、テストをビルドして実行したいが、ビルドが出力として生成する配置可能なパッケージにテストが追加したくないと考えている場合があります。

プラットフォーム更新プログラム 3 またはそれ以前の既存のビルド定義を持っている顧客がアップグレードするとき、ビルド定義が自動的に更新されることが表示されません。 新しい機能を使用するには、これらの顧客はビルド定義を手動で編集する必要があります (詳細は下記参照)。 

この新機能は、ビルド プロセスにおけるパッケージ作成ステップの新しいオプション パラメーターを公開します。 このパラメーターはビルド変数で管理されるため、簡単に調整できます。

1. Microsoft Azure DevOps で、**ビルドおよびリリース** ページの**ビルド**にある**すべての定義タブ**でビルド定義を検索します。 省略記号 (...)、**編集**の順にクリックします。

    ![ビルド定義を編集](media/builddef_edit.png)

1. **変数**タブで、新しいビルド定義が **PackagingExclusions** という名前の変数を持つこと通知します。

    ![PackagingExclusions 変数](media/builddef_packexclvariable.png)

1. **PackagingExclusions** 変数で、配置可能パッケージにパッケージする必要がないパッケージの名前をコンマで区切ったリストで指定します。

    > [!NOTE]
    > パッケージの名前は必ずしもモデルの名前ではありません。 代わりに、パッケージ名は通常、モデルがあるフォルダーの名前です。 または、パッケージ モデルのいずれかの記述子ファイルからパッケージ名をコピーして貼り付けることができます。 (XML では、**ModelModule** フィールドでパッケージ名を検索できます。)

    たとえば、MyCompanysAwesomeTests という名前の 1 つのパッケージおよび ContosoTaskRecordingTests という名前の別のパッケージがあり、配置可能なパッケージからこれら両方のパッケージを除外します。 この場合、**PackagingExclusions** 変数の値はこのようになります。

    ![PackagingExclusions の例](media/builddef_packexclexample.png)

    この設定を完了すると、ビルド プロセスはコードをビルドしながらパッケージに含まれているすべてのテストを実行します。 ただし、ビルドが作成する配置可能なパッケージには、それらのパッケージは含まれません。

## <a name="update-an-existing-build-definition-after-upgrade-to-platform-update-4-or-later"></a>プラットフォーム更新プログラム 4 以降へのアップグレード後に既存のビルド定義を更新する

新しい機能を使用するには、Platform update 4 より前に展開した既存のビルド定義を手動で更新する必要があります。

> [!NOTE]
> この機能は、ビルド仮想マシン (VM) をプラットフォーム更新プログラム 4 以降に更新した後でのみ、ビルド定義に追加できます。

1. **変数**タブで、ページの下部にある **+ 追加**をクリックします。
1. **名前**列に、**PackagingExclusions** と入力します。 最後の列で、**キュー時に設定可能**チェック ボックスをオンにします。
1. **タスク**タブで、**生成パッケージ**タスクを検索します。 クリックして選択します。
1. ページの右側で、**引数**パラメーターを見つけます。 テキスト ボックスをクリックし、End キーを押すか、テキスト ボックスの最後までスクロールします。 新しいビルド定義には、前に定義した **PackagingExclusions** 変数を渡す新しい引数があります。 ただし、既存のビルド定義については、スペースを追加し、さらにパラメーターの末尾に次のテキストを追加します: **-ExclusionList "$(PackagingExclusions)"**

    **引数** テキスト ボックスは次のようになります。

    ![パッケージ タスクを生成します](media/builddef_generatepack.png)

1. **保存** をクリックします。

説明の通りに、新しいフィーチャーを使用することができるようになりました。
