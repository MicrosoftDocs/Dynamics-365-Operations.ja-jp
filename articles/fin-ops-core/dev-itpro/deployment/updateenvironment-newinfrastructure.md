---
title: 環境の更新
description: この記事では、セルフ サービス配置エクスペリエンスを使用して配置された環境を、更新する方法について説明します。
author: laneswenka
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: f9b76cf47ffde9160e5dce8799a3410e853bf8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867296"
---
# <a name="update-an-environment"></a>環境の更新

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

この記事では、[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用して配置した環境に、更新を適用するプロセスについて説明します。

> [!IMPORTANT]
> 次世代のインフラストラクチャでは、現在のフローで適用されるものとは異なる方法で更新が適用されます。 *パッケージに含まれているものはすべて環境に適用され、既に環境に存在するものはすべて **上書き** されます。* つまり、ビルド環境からのすべてのカスタマイズおよび独立系ソフトウェア ベンダー (ISV) ソリューションを含む 1 つの配置可能パッケージを作成する **必要があります**。 環境内のモデルの一覧がパッケージ内のモデルの一覧と異なる場合は、更新が適用される前に警告が表示されます。 単一のパッケージを作成する方法については、[ソース コントロールを使用することでサード パーティ モデルとランタイム パッケージを管理する](../dev-tools/manage-runtime-packages.md)を参照してください。


## <a name="applying-updates-to-self-service-environments"></a>セルフサービス環境への更新を適用する

セルフサービス環境では、コンテナー ベースの画像プロセスを使用して環境のランタイムが構築されるので、更新は特別な方法で実行されます。 これらの画像をサンドボックス環境に適用すると、顧客から **更新名** の値が与えられ、環境履歴に表示されます。 更新画像は、次の 3 つの部分で構成されます:

- **Microsoft バイナリ** は、Microsoft が定期的にリリースするもので、新しいプラットフォームおよびアプリケーション ソフトウェアの更新が含まれます。 これらのバイナリは、Microsoft Dynamics Lifecycle Services (LCS) の環境の環境詳細ページから利用可能です。 すべてのアプリケーションとプラットフォーム修正の累積的なバイナリ更新を示す **1 つのタイル** が表示されます。 この更新プログラムを適用するには、パッケージを選択して、**パッケージの保存** を選択し、プロジェクト アセット ライブラリに Microsoft の更新プログラムを保存します。
- **AOT 配置可能パッケージ** は、顧客が環境に適用するすべてのカスタム コードの合計である、オールインワン パッケージです。
- 顧客が LCS で提供する **更新名** の値。 
 
![セルフサービス更新イメージの概念モデル。](media/SelfServiceUpdate.png)
 
これらのバイナリの組み合わせが、Application Object Server (AOS) のインスタンスを作成するのに使用する画像のベースになります。 **更新名** の値を使用すると、顧客は何が更新に含まれるかを示すわかりやすい名前を指定できます。

### <a name="update-by-using-packages-on-tier-1-sandboxdevelopment-and-testdemobuild-environments"></a>レベル 1 サンドボックス/開発およびテスト/デモ/ビルド環境でパッケージを使用して更新する

LCS を通じて配置されたレベル 1 サンドボックス/開発およびテスト/デモ/ビルド環境に更新を適用するには、[クラウド環境に更新を適用する](apply-deployable-package-system.md)の手順に従います。

### <a name="update-by-using-packages-on-tier-2-and-above-standard-acceptance-testsandbox-environments"></a>レベル 2 以上の標準承認テスト/サンドボックス環境でパッケージを使用して更新する

> [!IMPORTANT]
> パッケージ アプリケーションは、システムのダウンタイムを引き起こします。 すべて関連するサービスを停止、およびパッケージを適用中のときには環境を使用できなくなります。

サンドボックス レベルでは、セルフサービスの前に Microsoft 管理環境で使用していたパッケージと同じパッケージを使用して、更新は LCS 経由で引き続き適用されます。 顧客がパッケージを適用すると、Microsoft バイナリまたは AOT 配置可能パッケージのいずれかになります。 どちらの場合も、Microsoft は環境の最新画像を取得し、バイナリまたは AOT コンポーネントを上書きし、環境のランタイムを再作成するために使用される新しい画像を生成します。

開始する前に、配置可能パッケージが LCS のプロジェクト アセット ライブラリにアップロードされており、検証が成功したことを確認してください。

パッケージが、プロジェクト アセット ライブラリに入ったら、以下の手順に従って、環境を更新します。

1. パッケージを適用する環境の環境の詳細ページを開きます。
2. **管理 \> 更新プログラムの適用** を選択し、更新プログラムを適用します。
3. 更新プログラムに対して **一意の名前** を入力します。 この名前を使用して、画像 (Microsoft バイナリと顧客 AOT パッケージの両方) を運用環境に推奨する更新を識別します。
4. パッケージを選択して適用します。 上部にあるフィルターを使用してパッケージを探します。 このリストには、アセット ライブラリから検証に合格したアプリケーションおよびプラットフォーム バイナリ パッケージと、アプリケーション配置可能パッケージが含まれます。
5. **適用** を選択します。

    環境詳細ページの右上隅にあるステータスが、 **キュー** から **サービス** に、それから **事後サービス** に変わります。 パッケージ アプリケーションが完了すると、ステータスが **配置済み** に変更されます。

6. パッケージ アプリケーションが完了すると、環境履歴が更新されます。 環境履歴を表示するには、環境の詳細ページで **履歴 \> 環境の変更** を選択します。
7. 環境履歴ページからログをダウンロードすることもできます。
8. 検証が完了すると、 **サインオフ** または **払出サイン オフ** のいずれかを選択して、環境の履歴ページから更新プログラムをサインオフできます。

## <a name="servicing-changes"></a>サービスの変更
Microsoft は、オンライン モードでインデックス作成を行いサービスの全体的なダウンタイムを削減できる、新しい事後サービス ステップを導入しました。 後処理のステップが行われている間、オフライン サービスの完了後に LCS ダッシュボードに **事後サービス** と表示されます。 この間、インデックス作成と変更はオンライン モードで行われます。 環境はユーザーが通常の活動を実行できるようアクセス可能ですが、関連するパッケージ変更のパフォーマンスが低下する可能性があります。 事後サービスの間、ユーザーは新しいサービス要求をキャンセルしたりトリガーしたりできません。

![進行中の後処理のステップを示す LCS ダッシュボード。](https://user-images.githubusercontent.com/90061039/164792400-d8ca418c-6a5e-468c-a965-eae597bfb737.png)

後処理のステップでエラーが発生した場合、LCS ダッシュボートに **事後サービスに失敗しました** と表示されます。 環境はユーザーが通常の活動を実行できるよう引き続きアクセス可能ですが、パフォーマンスが低下する可能性があります。 24 時間以内に問題が解決されない場合は、Microsoft サポートに問い合わせてください。

#### <a name="uninstalling-a-module"></a>モジュールをアンインストールする

AOT 配置可能パッケージは、1 つまたは複数の顧客モジュールで構成されます。 これらは、ISV モジュール、パートナー モジュール、または顧客独自のカスタマイズ モジュールの組み合わせである可能性があります。 AOT 配置可能パッケージを完全にアンインストールする場合、サンドボックス環境には 2 つのオプションがあります:

- **推奨オプション:** [パッケージのアンインストール](uninstall-deployable-package.md)で概説した ModuleToRemove.txt プロセスを使用します。 このオプションでは、前のオプションで実行したことをすべてを実行しますが、結果として得られる画像を運用環境に導入することができます。

- **製品版ではサポートされていないオプション:** 削除するモジュールが不要になった新しい AOT 配置可能パッケージを作成します。 このパッケージをサンドボックス環境に直接適用すると、LCS のメッセージに、環境の現在の画像に含まれているモジュールにパッケージが含まれていないという警告が表示されます。

    - LCS に進みます。 Microsoft は、前回の更新プログラムからの Microsoft バイナリと、削除するモジュールが含まない現在の AOT パッケージとを組み合わせた新しい画像を作成します。 実際には、モジュールがアンインストールされます。
    - このオプションは、まだ運用環境を使用していない場合、または出来上がった環境をすばやくテストする必要があるが、この AOT パッケージを運用に導入する予定がない場合にのみお勧めします。
    - 結果として得られるサンドボックス環境の画像の運用環境への導入がブロックされます。

#### <a name="microsoft-automatic-updates-in-sandbox-environments"></a>サンドボックス環境での Microsoft の自動更新

Microsoft は定期的に、新しい Microsoft バイナリの自動更新をサンドボックス環境にプッシュします。 この自動更新は、サンドボックス環境のバージョンが遅れていて、サポートされている一般に利用可能なバージョンよりも古い場合にのみ行われます。

この自動更新では、最新のサンドボックス画像から Microsoft バイナリを上書きします。 実際には、新しい Microsoft バイナリや以前のカスタマイズを含む新しい更新が作成されます。

### <a name="promote-an-update-to-production-environments"></a>運用環境への更新の導入

パッケージは、運用環境には直接適用されなくなりました。 これまで、Microsoft が管理する環境では、顧客はサンドボックス環境に正常に適用され、*リリース候補* としてマークされたどのパッケージでも適用できました。 しかし、パッケージ A をパッケージ B の前に適用すると正常な環境が得られるが、異なる順序で適用すると機能が退行してしまうという操作順序があるため、この方法には多くの課題がありました。

こうした課題に対処するために、Microsoft は画像ベースの更新プロセスを導入しました。 この記事で前述のとおり、パッケージはサンドボックス環境に適用されるので、Microsoft は **更新名** の値が指定された画像を作成します。 この値は、Microsoft コードとすべてのカスタム コードを一単位として含め、ランタイム全体を表します。 顧客が変更を運用環境に対して導入すると、サンドボックス環境の履歴から更新を選択します。 その後、ランタイム全体がそのまま実稼働インフラストラクチャに移行され、回帰に対するより安全性が向上します。

> [!IMPORTANT]
> パッケージ アプリケーションは、システムのダウンタイムを引き起こします。 すべて関連するサービスを停止、およびパッケージを適用中のときには環境を使用できなくなります。

サンドボックス環境での更新プログラムの適用が成功し、更新プログラムを運用環境に移行する準備ができたら、次の手順に従って、更新をリリース候補としてマークします。

1. 環境履歴ページを開くには、環境の詳細ページで **履歴 \> 環境の変更** を選択します。
2. 運用環境に移動するため更新プログラムを選択します。
3. 更新プログラムの詳細で、 **リリース候補としてマーク** を選択します。

    **リリース候補** オプションが **はい** に設定されています。

更新プログラムをリリース候補としてマークしたら、次の手順に従って環境を更新します。

1. 運用環境の環境の詳細ページを開きます。
2. **管理 \> 更新プログラムの環境** を選択し、更新プログラムを適用します。
3. **使用可能なサンドボックス** の一覧で、更新プログラムが適用され、検証されて、リリース候補としてマークされているソースサンドボックス環境を選択します。
4. グリッドで、運用環境に適用する更新プログラムを選択します。 このグリッドには、リリース候補としてマークされている更新プログラムのみが表示されます。
5. **ダウンタイム開始** フィールドで、日付と時刻を入力します。 環境は、指定された日の指定された時間に停止されます。 **ダウンタイム終了** は、予定された期間に基づいて自動的に計算されます。

    この更新プログラムにはリードタイムは必要ありません。

6. **スケジュール** を選択します。 LCSは、選択された更新プログラムが環境に適用可能であることを確認する検証を実行します。 環境のダウングレードを回避するために、更新プログラムは、そのアプリケーションのバージョンが現在の環境のバージョンよりも低い場合は許可されません。 また、更新プログラムを続行するかどうかを確認するメッセージが表示されます。

    更新プログラムが **正常に** スケジュールされると、すべてのプロジェクト関係者に電子メール通知が送信されます。

    環境詳細ページの右上隅にあるステータスが、 **キュー** から **サービス** に変わります。 その後、更新プログラムが完了すると、ステータスが **配置済み** に変更されます。

    すべての関係者に、工程の進捗状況が通知されます。

7. 更新プログラムが完了すると、環境履歴が更新されます。 環境履歴を表示するには、環境の詳細ページで **履歴 \> 環境の変更** を選択します。
8. 環境履歴ページからログをダウンロードすることもできます。
9. 検証が完了すると、 **サインオフ** または **払出サイン オフ** のいずれかを選択して、環境の履歴ページから更新プログラムをサインオフできます。

> [!NOTE]
> 環境内で進行中の操作がある場合、または環境が同じバージョンまたはそれ以降のバージョンで既に実行されている場合、スケジュールされた更新は取り消されます。 予定された更新プログラムがキャンセルされると、すべてのプロジェクト関係者に電子メール通知が送信されます。 また、環境の詳細 ページで **キャンセル** を選択することにより、更新プログラムを取り消すこともできます。 顧客が更新を再スケジューリングしたり変更したりする場合は、現在の工程をキャンセルして、新しい更新をスケジュールすることができます。

#### <a name="things-to-consider-about-production-updates"></a>実稼働更新について考慮する点

サンドボックス環境から運用環境への更新を導入している場合は、**Microsoft バイナリおよび顧客 AOT パッケージの両方** が含まれます。 顧客は、Microsoft バイナリおよび顧客 AOT パッケージを個別に導入することはできません。 

Microsoft バイナリ更新をサンドボックス環境から導入する場合は、サンドボックスから同じ時点で適用されている最新の顧客パッケージが含まれるのことに注意してください。

顧客の AOT パッケージをサンドボックス環境から導入する場合は、直近で適用された Microsoft バイナリ更新プログラムも含まれることに注意してください。

#### <a name="microsoft-automatic-updates-in-production-environments"></a>運用環境での Microsoft の自動更新

Microsoft は定期的に、新しい Microsoft バイナリの自動更新を運用環境にプッシュします。 この自動更新は、常にサンドボックス環境への更新が成功してから 1 週間後に行われます。

この自動更新では、Microsoft は顧客の AOT パッケージを導入しません。 代わりに、新しいバイナリ バージョンを取得し、対象となる運用環境で最新の顧客 AOT パッケージと組み合わせて、運用ランタイムの新しい画像を作成します。

### <a name="rollback"></a>ロールバック
最新のインフラストラクチャ スタックに配置されている環境では、サービスが失敗した場合、その環境はほとんどの場合に自動的にロールバックされます。 工程が失敗した理由については、環境履歴ページからログをダウンロードできます。

> [!NOTE]
> データベース サイズが大きいときなど、ロールバックによってダウンタイムが延長する環境の小さなサブセットの場合、環境は失敗した状態で、ロールバックを実行しないようにアクションを実行できるかどうかを判断できます。 失敗した工程から先に進めない場合は、通常のロールバック プロセスが開始されます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
