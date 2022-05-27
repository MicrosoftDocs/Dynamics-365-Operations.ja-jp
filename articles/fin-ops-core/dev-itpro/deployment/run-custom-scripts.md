---
title: ダウンタイムなしでカスタム X++ スクリプトの実行
description: このトピックでは、システムを中断せずにカスタム X++ スクリプトを含む配置可能パッケージをアップロードおよび実行する方法について説明します。
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: fcd0a472fa5116ca0b3a59561b6eeb72181a9113
ms.sourcegitcommit: 44e6875e974a3a1b3e1d7a24c1a3cff3d3697cdc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2022
ms.locfileid: "8088347"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>ダウンタイムなしでカスタム X++ スクリプトの実行

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

この機能を使用すると、Microsoft Dynamics Lifecycle Services (LCS) を経由したり、システムを中断したりせずに、カスタム X ++ スクリプトを含む配置可能パッケージをアップロードして実行できます。 したがって、ダウンタイムが中断することなく、マイナー データの不整合性を修正できます。

X++ スクリプトを使用してマイナー データの不整合を修正する利点は、スクリプトの実行時に必要に応じてすべての関連テーブルがシステムによって自動的に調整される点です。 この方法は、修正の整合性を保証し、新しい不整合が発生するリスクを最小限にするのに役立ちます。

> [!IMPORTANT]
> この機能は、マイナー データの不整合を修正することを目的にしています。 次の目的または他の目的で使用できません。
>
> - データ収集
> - スキーマの変更
> - データ移行または他の実行時間の長いプロセス
> - 通常の業務プロセス、データ整合性ツール、その他のセルフサービス ツールなど、他の方法で修正できるデータの修正
>
> この機能を使用すると、権限のあるユーザーは、エンティティに関連付けられているビジネス ロジックを実行することなく、エンティティとそのレコードを直接変更できます。 このような変更が、データの整合性の問題の原因となる可能性があります。 したがって、スクリプトの実行前または実行後に、内部および外部の監査者 (または他の同等の利害関係者) からの承認と承認承認を得る必要が生じ、組織で必要になる場合があります。 コンプライアンス上の理由から、いくつかの特性に影響を与える変更は、外部レポート (財務諸表など) で変更したり、政府機関に報告したりする必要がある場合があります。 この機能を通じてデータに加えた変更、変更の承認と承認、承認、開示、および適用される法令への準拠については、組織が責任を負います。 この機能を使用する場合のリスクはすべてユーザーが負います。

システムにアップロードされる配置可能なすべてのパッケージは、必須のワークフローを通過します。 安全上の対策として、また職務の分離を確保するために、配置可能なパッケージ をアップロードするユーザーは、ワークフローの次のステップでパッケージを承認できません。 別のユーザーが承認する必要があります。 ただし、パッケージが承認された後で、パッケージをアップロードしたユーザーは、残りの手順を完了できます。

配置可能なすべてのパッケージでテストの実行を行う必要があります。 ユーザーは、生産データでのスクリプトの実行を許可される前に、**テスト ログの承認** を選択して、出力が正しい検証を行う必要があります。 出力を変更できない場合は、**破棄** を選択してパッケージをマークする必要 があります。 この場合、スクリプトは生産データ上で実行されません。

アップロード済みパッケージはシステムに保存され、定義されているイベント ワークフローを実行します。 タイムスタンプとイベントの実行者の ID を含むログが、イベントごとに保持されます。 これにより、システムは監査証跡が確実に作成されます。

次の図に示すように、システムは、各配置可能パッケージがX++ で実行された方法、およびどのエンティティにアクセスしたのかについての詳細を提供します。

![スクリプトの詳細ページ](media/script-details.png "スクリプトの詳細ページ")

## <a name="assign-duties-to-users-to-control-access"></a>アクセスを制御するユーザーへの職務の割り当て

この機能は、次の職務を提供します。 管理者は、これらの職務を使用して機能へのアクセスを制御することができます。

- **カスタム スクリプトの管理** - この職務は、環境内でのカスタムX++ スクリプト ( ユーザー受入テスト \[UAT\] および生産) のアップロード、テスト、検証、実行を行う機能を提供します。
- **カスタム スクリプトの承認** - この関税により、アップロード済みカスタム X++ スクリプトを承認する機能が付与されます。 承認は、すべてのスクリプトをテスト、検証、および実行する前に必須の手順です。

悪意のあるアクションのリスクを最小限に抑えるために、各スクリプトは、アップロードしたユーザー以外のユーザーによって明示的に承認される必要があります。 この機能を組織で使用するには、管理者が前の職務を 2 つ以上の関連する高信頼ユーザーに割り当てる必要があります。 1 人のユーザーに両方の職務を割り当て可能ですが、そのユーザーは独自のスクリプトを承認できません。

## <a name="create-a-deployable-package"></a>配置可能パッケージの作成

この機能には、Visual Studio で作成できる定期的な配置可能なパッケージが必要です。 指示については、[配置可能パッケージの作成](../deployment/create-apply-deployable-package.md) を参照してください。

配置可能パッケージには、実行できる X++ クラスが 1 つ必要です。 つまり、次の署名を持つメソッドを含むクラスが 1 つ必要です。

```xpp
public static void main(Args _args)
```

> [!NOTE]
> メイン メソッドの名前は小文字である必要があります。

## <a name="code-example"></a>コードの例

次のコード例は、配置可能パッケージの構成方法を示しています。

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>ベスト プラクティス

次の一覧は、スクリプトを正しく作成、実装、実行するためのいくつかのベスト プラクティスを示しています。 リストは完全ではありません。また、ガイダンスのみを考慮する必要があります。

- スクリプトの最後に成功メッセージの記述を **おこなうこと**。 これにより、スクリプトが例外なしで実行されたのを確認できます。
- トランザクション スコープの明示的な処理の追加を **おこなうこと**。
- `update()` メソッドなどの既存のビジネス ロジックを使用 **すること**、しかし `doUpdate()`、`doInsert()`、`doDelete()` メソッドを使用してビジネス ロジックをバイパス **しないこと**。 この方法は、依存データが正しく処理されるようにするために役立ちます。 データの不整合が生じるリスクも大幅に減少します。
- 会社コンテキストをアサート **すること**。 この方法では、スクリプトの実行として一般的な誤りが公開されます。 たとえば、間違った会社でスクリプトが実行されたかどうかが明らかにされます。
- 影響を受けるレコードの数が期待と合うようにアサート **すること**。 この方法により、スクリプトの準備中にシステムでデータが予期せず移動したかどうかが明らかされます。
- 各スクリプトには一意のクラス名を使用 **すること** (たとえば、名前で作業項目への参照を含めることによって)。 この方法により、スクリプトをアップロードするときに名前の変更に関する問題を回避できます。 スクリプトの新しい繰り返しが必要な場合は、新しい名前を付してください。
- 実稼働環境以外の環境で各スクリプトを最初にテスト **すること**。 関連データに対する意図された影響や意図しない悪影響をテストします。 影響を受ける可能性があるすべての業務プロセスを、後で正常に完全に完了する必要があります。

## <a name="upload-and-run-a-deployable-package"></a>展開可能なパッケージのアップロードと実行

以下の手順でスクリプトをアプロードして実行します。

1. 財務と運用アプリで、**システム管理 \> 定期処理 タスク \> データベース \> カスタム スクリプト** に移動します。
1. **アップロード** を選択します。
1. このトピックの前半で説明した通り、作成した展開可能パッケージを選択します。 スクリプトの目的を指定するように求めるメッセージが表示されます。
1. これで、スクリプトをアップロードしたユーザー以外のユーザーが承認する必要があります。 承認者は次の手順に従う必要があります。

    1. **システム管理 \> 定期処理 \> データベース \> カスタム スクリプト** に移動します。
    1. 承認するスクリプトを選択し、**詳細** を選択します。
    1. アクション ペインの、**プロセス ワークフロー** タブの、**開始** グループで、**承認** または **否認** を選択します。 **承認** を選択すると、スクリプトは承認済としてマークされ、テストのロックは解除されます。 **否認** を選択すると、スクリプトはロックされます。 どちらの場合もイベントが記録され、システムにスクリプトのコピーが保持されます。

1. スクリプトは、意図した動作を実行することを確認するためにテストする必要があります。 テスト担当者は、アップロード者または承認者と同じ場合と同じか、必要なアクセス許可を持つ 3 番目のユーザーである場合があります。 テスト担当者は次の手順に従う必要があります。

    1. **システム管理 \> 定期処理 \> データベース \> カスタム スクリプト** に移動します。
    1. テストするスクリプトを選択し、**詳細** を選択します。
    1. アクション ウィンドウの、**製造ワークフロー** タブの、**テスト** グループで、**テストを実行する** を選択します。 スクリプトは一時的なトランザクション内で実行され、さまざまなログや SQL ステートメントを収集する間はシステムによって自動的に中止されます。
    1. スクリプトの実行が終了したら、ログを確認し、結果が期待に応える結果を確認します。 次の手順のいずれかを実行します。

        - テスト結果に問題がなければ、アクション ウィンドウの **プロセス ワークフロー** タブの **テスト** グループで **テスト ログを受け入れる** を選択してスクリプトを実行できます。 イベント ログには、スクリプトがテストされたという情報が反映され、誰がいつ、そのスクリプトをテストしたのかが示されます。
        - テスト結果に満足いかない場合は、アクション ウィンドウの **プロセス ワークフロー** タブの **終了** グループで **放棄** を選択して、スクリプトの実行を防止します。 システムでは、スクリプトのコピーを履歴のログと共に保持します。

1. スクリプトが期待に応える必要がある場合は、アクション ウィンドウの **プロセス ワークフロー** タブの **実行** グループで **実行** を選択して実行します。 このコマンドは前のテスト実行と同じことを行いますが、トランザクションは最後にコミットされます。
1. スクリプトの実行が終了したら、結果を確認し、意図した通りスクリプトが機能することを確認します。 次の手順のいずれかを実行します。

    - 結果に問題がなければ 、アクション ウィンドウの **プロセス ワークフロー** タブの **終了** グループで **解決された目的** を選択します。 イベント ログには、スクリプトのが正常に実行された事実が反映され、誰がいつ、そのスクリプトをテストしたのかが示されます。 スクリプトは保存されますが、ロックされ、再度実行できません。
    - 結果に満足いかなければ、アクション ウィンドウの **プロセス ワークフロー** タブの **終了** グループで **解決されていない目的** を選択します。 イベント ログには、スクリプトがその目的を満たすことができなかった事実が反映され、誰がいつ、そのスクリプトを実行したのかが示されます。 スクリプトは保存されますが、ロックされ、再度実行できません。 ただし、スクリプト アクションはシステムによって自動的に元に戻されません。 失敗したスクリプトがシステムに与えた影響を取り消すには、新しいスクリプトの記述、インポート、および実行が必要になる場合があります。

最後の手順で選択した内容によって、スクリプトの最終状態が定義されます。 必要に応じてこのプロセスを繰り返すことができます。

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>LCS を通じた展開可能なパッケージのアップロードと実行

前のセクションで説明するように、財務と運用アプリのユーザー インターフェイスを通じて配置可能なパッケージを配置する代わりに、LCS にアップロードし、通常の手順に従って配置することができます。 詳細な情報については、[コマンド ラインからの配置可能なパッケージのインストール](../deployment/install-deployable-package.md) を参照してください。

この方法では制限が少なく、エラーからの保護を少なくすることができます。 また、すべてのサーバーの再起動が必要なので、ある程度のダウンタイムが発生します。