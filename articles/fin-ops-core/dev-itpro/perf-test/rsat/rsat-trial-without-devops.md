---
title: Azure DevOps を使用しない試用版モード
description: この記事では、Microsoft Azure DevOps を使用しない試用版モードでの Regression Suite Automation Tool (RSAT) の使用方法について説明します。
author: FrankDahl
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2021-03-03
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 21631
ms.openlocfilehash: 5f61d62d1b6b01622a8f692d5d90402a6cff0e50
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277422"
---
# <a name="trial-mode-without-azure-devops"></a>Azure DevOps を使用しない試用版モード

[!include [banner](../../includes/banner.md)]

Regression Suite Automation Tool (RSAT) は試用版モードで使用できます。 試用版モードの利点は、Microsoft Azure DevOps への接続を必要としないことです。

RSAT を初めて使用する組織は、Azure DevOps にサブスクライブすることをコミットしなくても、ツールを探索できます。 この方法で、テスト自動化の価値を確認し、RSAT が適切なツールであるかどうかを判断し、このアプローチが組織にとって意味がある場合は、Azure DevOps とテスト計画のサブスクリプションをユーザーに追加できます。

試用版モードは時間制限がないことに注意することが重要です。 試用版モードの長期に使用がある場合は、インストールを維持します。 一部の組織は、試用版モードが提供するものに完全に満足している場合もあるため、Azure DevOps にサブスクライブしたり、RSAT を統合したりすることなく、試用版モードを引き続き使用できます。

試用版モードの RSAT は、以前のバージョンで知られている標準モードの RSAT に基づいています。 実際、バイナリ アプリケーションは同じですが、新しい試用版モードで実行される場合は名前が異なります。 試用版モードは、Azure DevOps の実行を必要としない簡略化されたアプリケーションを作成するために、標準モードで使用できる機能の縮小版と考えることができます。

試用版モデルの RSAT は、いくつかの点で制限されています。 詳細については、この記事で後述する [RSAT を標準モードではなく試用版モードで実行した場合の違い](#differences) セクションを参照してください。

インストール プロセス中に、使用可能などの RSAT モードを選択します。 両方のモードがインストールされ、デスクトップにそれぞれ独自のショートカットが設定されます。 両方のモードも同じマシンにインストールでき、それらを交換して使用できるようにします。

RSAT は、標準モードでの実行時の作業に使用したとおり、引き続き正常に機能します。

試用版モードでは、**ローカル テスト計画** という名前の単一の専用のテスト計画に基づいて、すべてのテスト スイートとケースが分離されます。 現在、試用版モードと標準モードの間でのテスト スイートまたはケースの交換はサポートされていません。 つまり、RSAT を試用版モードで実行すると、標準モードの RSAT との統合がなくても機能します。 ただし、RSAT 2.5 リリースでは、計画されている新機能により、ケースと一緒にテスト スイートのエクスポートとインポートが可能になります。 この機能を実装すると、2 つの RSAT モード間でテスト スイートとケースを転送できるようになります。 それらをある環境から別の環境に転送することもできます。

## <a name="install-rsat-in-trial-mode"></a>試用版モードで RSAT をインストールする

RSAT インストーラー プログラムには、使用可能にする RSAT モードを選択する追加のページが含まれるようになりました。 既定では、このページは、標準モードだけがインストールするように構成されています。 ただし、試用版モードのインストールも選択できます。 必要がない場合は、標準モードの選択をクリアすることもできます。 インストール プログラムは、環境内で選択された各モードのショートカットを作成します。 インストールは完全な環境で行われ、作成されたショートカットはその環境のすべてのユーザーによって共有されることに注意してください。

![インストールする RSAT モードの選択。](media/install-rsat.png)

デスクトップに表示されるアイコンは、選択したモードで RSAT を呼び出すショートカットとして機能します。 実行するモードのショートカットを選択するだけです。 試用版モードのアイコンに「試用版」という語のバンドが含まれています。 次の図は、両方のモードが選択およびインストールされている場合に表示されるアイコンを示しています。 

![RSAT デスクトップ アイコン。](media/rsat-icons.png)

## <a name="differences-when-rsat-is-run-in-trial-mode-instead-of-normal-mode"></a><a name="differences"></a> RSAT を通常モードではなく試用版モードで実行した場合の違い

RSAT を標準モードではなく試用版モードで実行すると、ユーザー エクスペリエンスが低下します。 Azure DevOps に関連するアクションと設定は、ユーザー エクスペリエンスから削除されます。

![試用版モードで RSAT を実行します。](media/rsat-trial.png)

次の表では、試用版モードでは使用 **できない** 機能 (コマンド、設定、およびリンク) を要約します。

| フィーチャー | 使用できない理由 |
|---------|-------------------------------|
| メニューを **読み込む** | 試用版モードには、 Azure DevOps への接続はありません。 |
| **新しい** メニューで、**派生テスト ケース** コマンドを作成する | 試用版モードは、派生したテスト ケースをサポートしていません。 |
| **アップロード** メニュー | 試用版モードには、 Azure DevOps への接続はありません。 |
| メニューを **開く** | 試用版モードには、 Azure DevOps への接続はありません。 |
| **既存のテスト ケースを追加** コマンドを **新しいテスト ケース** メニューに追加 | 試用版モードでは、既存のケース ID を参照してテスト ケースを追加することはできません。 |
| 試用版モード設定での Azure DevOps の段落 | |
| **Azure DevOps へのアップロードを有効にする** オプション設定 | |
| **Azure DevOps** セクションとリンク | |

試用版モードの RSAT は、OneBox 開発者の仮想ハードディスク (VHD) で実行されるテスト環境に対しては実行できません。 この機能が必要な場合は、標準モードで RSAT を実行する必要があります。 ただし、試用版モードの RSAT は、クラウド ホスト開発者ボックスに対して実行できます。 通常、試用版モードの RSAT は、クラウド ホスト サンドボックス (Tier-2) 環境を使用します。

Azure DevOps によって提供される一部の機能は、試用版モードの RSAT で直接使用できるようにする必要がありました。

新しいテスト ケースが作成される場合、割り当てられる ID は、試用版ディレクトリで次に使用可能なフォルダ名に基づいて決定されます。

試用版モードで実行する場合、使用できるテスト計画は 1 つのみです。 このテスト計画は自動的に **ローカル テスト計画** という名前が付きます。 複数のテスト計画は、RSAT が標準モードで実行され、Azure DevOps に接続されている場合にのみサポートされます。

RSAT を試用版モードで実行すると、Azure DevOps でテスト スイートが作成されません。 したがって、RSAT ツールバーには、**新しいテスト スイート** という名前の新しいコマンドが含まれています。 このコマンドによって、作成するスイートの名前を指定できるダイアログ ボックスが開きます。

![作成するテスト スイートの名前を指定するダイアログ ボックス。](media/new-suite.png)

試用版モードでは、**ローカル テスト計画** のテスト計画にのみ直接テスト スイートを追加できます。 さらに、**新しいテスト スイート** コマンドは、次の図に示すように、左側のツリーでそのテスト計画のノードが選択されている場合にのみ使用できます。

![テスト ツリーで選択したローカル テスト計画のノード。](media/trial-plan.png)

**テスト スイートの削除** という名前の別の新しいコマンドを使用すると、テスト スイートを削除できます。 ただし、このコマンドは、テスト ケースを含まないテスト スイートにのみ使用できます。 テスト スイートにテスト ケースが含まれている場合は、スイートを削除する前に、それらのケースを個別に削除する必要があります。

**設定** で使用できる **名前を付けて保存** および **開く** コマンドを使用すると、試用版モードで非表示になっている Azure DevOps 設定も含め、使用可能なすべての RSAT 設定を保存および読み込むことができます。 これらのコマンドを使用すると、標準モードの設定を再利用して、たとえば試用版モードで開くことができる他のユーザーと共有できるため、便利です。

## <a name="using-rsat-in-trial-mode"></a>試用版モードで RSAT を使用する

試用版モードで RSAT を開くには、アイコンに「試用版」バンドがあるデスクトップ ショートカットを選択します。 以前のバージョンの RSAT を使用したことがある場合、アプリケーションは非常に使い慣れているように見えます。 ただし、使用できるコマンドは少なくなります。

試用版モードは Azure DevOps に接続しなくても機能し、テストはローカル ファイルによって排他的に維持されます。 RSAT を試用版モードで実行する場合、単一ユーザーとしてインストールを実行します。 作成したテストは、他のユーザーと交換されません。 ユーザー間で作業ディレクトリを共有することをお勧めします。

RSAT 2.5 リリース計画には、テスト スイートのエクスポートとインポートを可能にする機能の追加が含まれています。 このようにして、テスト スイートとケースを交換できるようになります。

初めて試用版モードで RSAT を開くと、テスト スイートやケースは表示されません。 **ローカル テスト計画** という名前のテスト計画は 1 つだけです。 試用版モードのテスト ケースは、RSAT 設定で指定した作業ディレクトリの下の **試用版** フォルダーにあります。 各テスト ケースには、**試用版** フォルダーに独自のサブフォルダーがあります。 サブフォルダーの名前はケースの ID を示します。

**新しいテスト スイート** コマンドを使用して、**ローカル テスト計画** テスト計画の下に 1 つ以上のテスト スイートを追加できます。 テスト ケースをテスト計画に追加することもできますが、代わりにテスト スイートを作成してから、それらにテスト ケースを追加することを強くお勧めします。 テストは、常に左側のツリーで現在選択されているノードに追加されます。 たとえば、次の図では、テストが **発注書** のテスト スイートに追加されます。

![テスト ツリーで選択した発注書テスト スイートのノード。](media/trial-tree.png)

テスト ケースを追加、編集、および削除するには、標準モードの RSAT のリリース 2.2 で使用可能だったのと同じコマンドを使用します。 詳細については、[Regression Suite Automation Tool (RSAT) でのテスト ケースの管理](rsat-maintain-test-cases.md) を参照してください。

試用版モードでのテスト ケースの管理は、標準モードでの管理とほとんど異なりません。 基本的に、試用版モードには次の 2 つの制限があります。

- 派生テスト ケースは使用できません。
- テスト ケースを既存のテスト ケースにリンクして追加することはできません。

試用版モードでは、ファイル システムに新しいファイルを追加するだけでは新しいテストを追加できないことに注意してください。 実際、RSAT は使用されるすべてのファイルの内部データベースを維持しているため、ファイルを直接操作することはお勧めしません。 したがって、RSAT の外部で、ファイル システム内で直接行われた変更は、正しくカタログ化できません。 代わりに、RSAT で使用可能なコマンドを常に使用して、新しいテスト ケースと添付ファイルを追加する必要があります。 同様に、パラメーター ファイルを開いて対話するには、RSAT で使用可能なコマンドを使用します。

試用版モードでテストを実行するには、RSAT ツールバーの **実行** を選択します。 結果は、テストを実行しているユーザーにのみ表示されます。 それらはテスト ケースを示すリストにのみ表示され、どこにも保存されません。 また、結果は RSAT が開いたままの場合にのみ使用できます。 RSAT を閉じて再度開くと、結果は表示されなくなります。 Azure DevOps を使用すると、ユーザーはテスト実行の結果を保存できるため、それらの結果を他のユーザーと共有できますが、試用版モードの RSAT では結果を共有できません。 テストの実行の結果を共有する必要がある場合は、標準モードで RSAT を使用することを検討します。

試用版モードの RSAT の設定は、標準モードの RSAT と共有されます。 唯一の実際の違いは、Azure DevOps に接続するための特定の設定が試用版モードで非表示になっていることです。 ただし、設定ファイルを保存して開くと、RSAT のすべての設定が含まれます。 設定ファイルを保存または適用するときに、どのモードを実行するかは関係ありません。

試用版モードの RSAT には、RSAT で直接テスト スイートを作成および削除できる 2 つの新しいコマンドが含まれています。 現在のリリースでは、これらのコマンドは試用版モードでのみ使用できます。 ただし、Microsoft は、これらのコマンドを標準モードでも要求するフィードバックを受け取っています。 今後のリリースで、それらを標準に追加することを検討します。

前述の通り、テスト ケースをテスト計画に直接追加することもできますが、推奨される方法は、テスト スイートの下でテストを整理することです。 この方法により、テストをエクスポートして、標準モードの RSAT、他のユーザー、または他の組織と交換できるようになります。
