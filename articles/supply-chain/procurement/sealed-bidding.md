---
title: RFQ の封緘入札
description: このトピックでは、購入担当者が開封するまで仕入先の入札応答を秘密にしておくために、封緘された入札を設定する方法について説明します。
author: Henrikan
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 96549b6053ba75f2d5b9a85bcd5b7feb006f0f1b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578083"
---
# <a name="sealed-bidding-for-rfqs"></a>RFQ の封緘入札

[!include [banner](../includes/banner.md)]

封緘された入札は、購入担当者が開封するまで、仕入先の入札応答を秘密にします。 見積依頼 (RFQ) に関連するすべての入札は、入札期限が切れるてはじめてアンシールドすることができます。 入札を開封する前に、専用のユーザー ロールを持ち、仕入先を表すユーザーのみがアクセスできます。

> [!IMPORTANT]
> フォームを修正、拡張したり、新しいフォームやビジネス ロジックを作成したりすると、マイクロソフトが提供するシールド入札の保護が破られる可能性があります。 改造、拡張、新規フォーム、ビジネスロジックを使用するリスク、またはそのような改造、拡張、新規フォーム、ビジネス ロジックに起因するシールド入札機能の使用不能のリスクは、ユーザーが負うものとします。  マイクロソフトは、ユーザーが作成した、または第三者がユーザーに向けて作成した、フォームの修正や拡張、新しいフォームやビジネス ロジックに起因するいかなる損害に対しても責任を負いません。 マイクロソフトは、ユーザーまたはユーザーに代わって第三者が行った変更、拡張、新規フォーム、またはビジネス ロジックについて、技術的またはその他のサポートを提供しません。 ユーザーは、シールド入札に関するすべての適用法または規制を遵守することに単独で責任を負います。

## <a name="how-bids-are-kept-secure"></a>入札のセキュリティ保護方法

封緘された入札では、非対称暗号化を使用して入札暗号化キー (KEK) を暗号化し、対称暗号化を使用して実際の入札を暗号化します。 システムは Microsoft Azure Key Vault に統合されて、封緘された入札を暗号化するために使用される暗号化キーを生成および管理します。 各入札には独自の暗号化キーが設定されています。 この暗号化は、Dynamics 365 Supply Chain Management が実行される組織が所有するキー コンテナーに保管されます 。 システムが暗号化と復号化が必要な場合は、必要に応じてにキー コンテナーにアクセスします。

## <a name="setup-and-configuration"></a>設定およびコンフィギュレーション

このセクションでは、封緘された入札を必要とする RFQ を送信する前に実行する必要がある前提条件について説明します。

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>手順 1: 封緘された入札に対するユーザー アクセスを設定する

封緘された入札を使用する場合、その仕入先の連絡担当者として設定されているユーザーのみが、仕入先の期間が終わるまでその仕入先の入札を表示、編集、および送信できます。 これらのユーザーは **仕入先 (外部)** ロールを持ち、仕入先勘定の連絡担当者として設定されている必要があります。 連絡担当者は、[仕入先コラボレーションの設定と管理](set-up-maintain-vendor-collaboration.md) の説明に従って、仕入先コラボレーションを行うアクセス許可も持っている必要があります。

適切なアクセス許可を持ち、仕入先の連絡先として設定されているユーザーは、仕入先の封緘された入札にアクセスすることができるので、それらのユーザーを追跡することが重要です。 ユーザーとセキュリティ ロールを設定するシステム管理者は、封緘された入札へのアクセスを、実際に表示できるユーザーに制限する責任があります。

### <a name="step-2-enable-the-sealed-bidding-feature"></a>手順 2: 封緘された入札機能を有効にする

この機能の設定、または使用を開始する前に、システムで使用可能な状態になっていることを確認する必要があります。 管理者は、**[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ワークスペースを使用して、この機能の状態を確認し、有効にすることができます。 **機能管理** ワークスペースで、この機能は次のようにリストされています。

- **モジュール:** *調達*
- **機能名:** *RFQ の封緘された入札*

### <a name="step-3-set-up-azure-key-vault"></a>手順 3: Azure Key Vault の設定

Supply Chain Management では、暗号化キーを使用して、すべての封緘された入札を保護し、適切な時まで秘密にしておきます。 Key Vault の機能を利用して、必要なキーを生成および管理します。 したがって、システムを有効にするには、Supply Chain Management からキー コンテナーへの接続を設定する必要があります。

> [!IMPORTANT]
> 封緘入札に使用するキー コンテナーは、次の要件を満たす必要があります。
>
> - 開発とテストにサンドボックスを使用する場合は、サンドボックス用に専用のキー コンテナーを 1 つと、実稼働用に別のキー コンテナーを用意する必要があります。
> - 各キー コンテナーは、組織が所有する Azure サブスクリプション で作成する必要があります (Supply Chain Management を実行しているサブスクリプションではありません)。
> - 各キー コンテナーは、封緘入札専用に使用される必要があります。 その他の用途には、封緘入札キー コンテナーを使用することはできません。

すべての入札は、独自の秘密キーを取得します。 このキーは、ユーザーが入札を表示、更新、または封緘を開くたびに使用されます。

Key Vault は、仕入先が仕入先コラボレーション インターフェイスで **入札** を選択した場合に、シークレットを取得するために使用されるキーを生成します。 キーは、調達マネージャーが Supply Chain Management の **調達パラメーター** ページで設定した固定時間後に期限切れになります。 キーの有効期限が切れると、誰も入札を表示、編集、または開封できなくなります。 したがって、入札プロセスが完了するのに十分な時間があるように、キーの有効期限を構成することが重要です。

次の 3 つの手順では、Key Vault への接続を設定します。 最初に、封緘された入札で使用するキー コンテナーを設定します。 次に、Supply Chain Management を構成してキー コンテナーと通信します。 最後に、キーの有効期限を設定します。

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>手順 4: 封緘された入札で使用するキー コンテナーを設定

キー コンテナーを設定するには、次の手順を実行します。 手順の順序は重要です。

1. Supply Chain Management を実行しているサブスクリプションとは別の Azure サブスクリプションをまだ設定していない場合は、このサブスクリプションを設定します。
1. 個別の Azure ストレージにキー コンテナーを設定します。 詳細については、[Azure Key Vault ストレージを管理する](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage) を参照してください。
1. Supply Chain Management アプリを、キー コンテナーのクライアントとして機能する設定を行います。 詳細については、[Azure Key Vault クライアントの設定](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client) を参照してください。

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>手順 5: Supply Chain Management の Key Vault パラメーターを構成する

封緘された入札中にキー コンテナーと通信するように Supply Chain Management を構成するには、次の手順に従います。

1. Supply Chain Management にサインインし、**システム管理 \> 設定 \>  Key Vault パラメーター** に移動します。
1. **新規** を選択してレコードを作成し、そのレコードに次のフィールドを設定します:

    - **名前** – 名前を入力します。
    - **説明** – 説明を入力します。
    - **Key Vault URL** – キー コンテナーの既定 URL を入力します。
    - **Key Vault クライアント** – 認証のためにキー コンテナーに関連付けられている Active Directory アプリケーションのインタラクティブ クライアント ID を入力します。
    - **Key Vault 秘密キー** – 証明書の秘密参照を入力します。
    - **封緘された入札の有効化** – このオプションを *はい* に設定します。

![Key Vault パラメータ ページ](media/sealed-bidding-key-vault-param.png "Key Vault パラメータ ページ")

> [!NOTE]
> 一度に封緘された入札に対して有効にできるキー コンテナー構成は 1 つだけです。 既存のキー コンテナー構成を無効にする前に、それを使用するすべての封緘された入札が開封されていることを確認する必要があります。 *封緘済* タイプのすべての RFQ ケースを検査し、その返信がすべて開封されていることを確認します。

### <a name="step-6-set-the-key-expiration-time"></a>手順 6: キーの有効期限を設定する

新しい入札ごとに生成されたキーに適用される有効期限を設定するには、次の手順に従います。

1. **調達パラメーター \> 設定 \> 調達パラメーター** の順に移動します。
1. **見積依頼** タブの **相殺日数** フィールドに、RFQ 期間の最後の日数を入力します。 RFQ が作成されると、ここに入力した日数がシステム日付に追加され、RFQ の既定の有効期限が定義されます。
1. **暗号化キーの有効期限の相殺** フィールドに、すべての暗号化キーを発行した後に有効になる日数を入力します。 暗号化キーの有効期限が切れると、誰も使用する封緘された入札をを表示、編集、または開封できなくなります。

> [!TIP]
> **暗号化キーの有効期限相殺** フィールドの値は **相殺日数** フィールドの値より小さくしないでください。

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>手順 7: 既定の入札タイプを設定する

すべての RFQ ケースには入札タイプがあります。 入札タイプによって、RFQ ケースで公開入札と封緘入札のどちらを提供するかを定義します。

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>入札タイプがない RFQ ケース

作成時に入札タイプが割り当てられていない新しい RFQ ケースに割り当てられる既定の入札タイプを設定するには、次の手順に従います。

1. **調達パラメーター \> 設定 \> 調達パラメーター** の順に移動します。
1. **見積依頼** タブで、**入札タイプ** フィールドを *封緘済* に設定します。

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>入札タイプがある RFQ ケース

作成時に入札タイプが割り当てられている新しい RFQ ケースに割り当てられる既定の入札タイプを設定するには、次の手順に従います。

1. **調達 \> 設定 \> 見積依頼 \> 入札タイプ** の順に移動します。
1. 新しい入札タイプを作成するか、入札タイプが *封緘済* の入札タイプを使用する既存の入札タイプを選択します。
1. **入札タイプ** フィールドを *封緘済* に設定します。
1. 封緘された入札を実装する追加の入札タイプごとに、上の手順を繰り返します。

> [!TIP]
> 新しい RFQ を作成する場合は、入力タイプを割り当てる必要がありません。 入札タイプが割り当てられている場合は、RFQ の既定の入札タイプで取得できます。 それ以外の場合は、調達パラメータで定義されている既定の入札タイプを使用できます。

## <a name="the-sealed-bidding-process"></a>シールド入札のプロセス

封緘された入札は、[見積依頼 (RFQ) の概要](request-quotations.md) で説明されているのとほぼ同じプロセスに従います。 主な違いは、入札が開封されるまで入札データとその添付ファイルを暗号化して保持することです。

> [!IMPORTANT]
> [アンケート ](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires)は暗号化されていないため、機密情報の収集に使用してはいけません

次にプロセスのアウトラインについて示します:

1. RFQ を 1 つ以上の仕入先に作成して送信できます。
1. 仕入先は、封緘された入札を送信して対応します。
1. 入札エントリの有効期限に入札を開封します。
1. 入札が表示され、評価および比較できます。
1. 入札が承認された後は、発注書の生成、購買契約の生成、または購買要求の更新を行います。

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>封緘された入札を使用する RFQ の作成

封緘された入札の RFQ ケースを作成するプロセスは、封緘されていない入札のプロセスとほぼ同じです。 RFQ ケースの両方のタイプの作成方法の詳細については、[見積依頼の作成](tasks/create-request-quotation.md) を参照してください。 このセクションでは、封緘された入札の RFQ を作成する際に、いくつかの重要な考慮事項を強調します。

封緘された入札の RFQ ケースには、*封緘済* の **入札タイプ** 値がある必要があります。 この値を RFQ ケースに割り当てるには、次の 3 つの方法があります:

- 作成後、RFQ ケースに直接値を設定します。
- 調達パラメータのすべての RFQ ケースに対する既定の入札タイプとして封緘された入札を定義します。 (このトピックの前述の[既定の入札タイプの設定](#set-default-bid-type) セクションを参照してください。)
- 新しい RFQ ケースを作成する場合は、封緘された入札に対して設定された入札タイプを選択します。 ([既定の入札タイプの設定](#set-default-bid-type) セクションを参照してください。)

封緘された入札の場合、RFQ ケースの **有効期限日時** の値は、送信された入札を開封できる時を確立します。 各明細行の **有効期限日時** の値は、ヘッダーの値と一致します。

RFQ ケースの送信後は、入札タイプを変更できません。

### <a name="vendors-respond-to-an-rfq"></a>RFQ に対する仕入先の対応

封緘された入札に応答する仕入先は、[仕入先入札ワークスペースでの RFQ の操作](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace) で説明されているように、公開入札に応答するために使用するのと同じ手順を使用します。 公開入札と封緘された入札の両方を処理する方法の詳細については、[RFQ 入札価格の入力と比較および契約の授与](tasks/enter-compare-rfq-bids-award-contracts.md) を参照してください。 封緘された入札の処理と公開入札の処理の唯一の違いは、入札期間が終了するまで、調達のプロフェッショナルは仕入先の封緘された入札を開くことができないということです。 仕入先の連絡担当者のみが、その仕入先の封緘された入札を開くことができます。

> [!IMPORTANT]
> 封緘された入札の場合、仕入先は添付ファイルを PDF 形式でのみアップロードできます。 他の形式は受け付けられません。

登録仕入先ユーザーは、封緘された入札 RFQ で **入札** を選択すると、入札データを入力でき、そのデータは安全に保たれます。 仕入先は、入札の準備中に作業を保存し、必要な頻度で返品し、準備ができたら送信できます。 仕入先は、送信後に入札を表示することもできます。 仕入先は、送信後に入札を変更する必要がある場合は、入札期間が終了するまでいつでも、入札を取り消し、更新し、再送信することができます。

封緘された入札では、次の条件が適用されます:

- 封緘された入札中に、システムは *見積依頼* 仕訳帳を作成します。
- 仕入先が入札を送信すると、シールド価格を持つ明細行なしの RFQ 仕訳帳が作成されます。
- ケースが開封された後、価格と金額のある RFQ 仕訳帳が作成されます。 この仕訳帳にアクセスするには、**すべての見積依頼** ページで **見積依頼仕訳帳** を選択します。
- システムは、ユーザーが封緘された入札アクションで実行した各アクションのログを保存します。 これらのアクションには、入札の表示、編集、および保存が含まれます。 このログは、仕入先と、入札にアクセスできる調達担当者の両方に表示されます。
- 入札が進行するにつれて、調達担当者は状態を確認できます。 状態が、*仕入先が更新中* または *仕入先によって送信* のいずれかになります。
- 封緘された入札の明細行の状態は、入札が開封されるまで *送信済* のままです。
- 仕入先が入札を拒否することを選択した場合、入札には *仕入先が拒否* の **返信進捗状況** の状態があります。 この状態は調達担当者に対して表示されます。
- アンケートの回答は、暗号化された形式でデータベースに保存され **ません**。 そのため、封緘されていません。 ただし、ケースが開封されるまで、RFQ ユーザー インターフェイスには表示されません。

### <a name="all-sealed-bid-activities-are-logged"></a>封緘された入札活動はすべてログに記録される

詳細ログには、入札に対するすべてのユーザー活動とアクションが記録されます。 活動ログを使用すると、組織は、入札期間中に誰が入札を更新したか、および更新内容を決定できます。 また、組織は、封緘された入札にアクセスした権限のあるユーザーのみが確認できます。 活動ログは、すべての入札の **活動** ページで使用できます。

### <a name="review-rfq-activity"></a>RFQ 活動の確認

入札とのすべてのやり取りは記録され、**活動** ページで表示できます。 次の図は、例を示します。

![活動ページの例](media/sealed-bidding-rfq-activity.png "活動ページの例")

仕入先は、**見積依頼の封緘された** ページで **活動** を選択することで **活動** ページにアクセスできます。 調達担当者は、**見積依頼** ページで **活動** を選択することで、アクセスできます。 活動ログは、仕入先と、入札にアクセスした調達担当者に完全な可視性を提供します。 したがって、不正アクセスが明らかになる可能性があります。

### <a name="unseal-sealed-bids"></a>封緘された入札を開封する

封緘された入札 RFQ ケースに構成された **有効期限日時** の値が経過すると、**開封** ボタンが使用可能になります。 選択した RFQ ケースのすべての入札を開封するには、**開封** を選択します。 その後、すべての入札データと添付ファイルが表示され、ケースへの返信を管理できます。 また、送信された入札データを含む仕訳帳が作成されます。

開封イベントは記録され、**活動** ページで表示できます。

### <a name="process-accepted-bids"></a>承認された入札のプロセス

以前に封緘された入札を比較して承認するプロセスは、公開入札のプロセスと同じです。 封緘された入札をスコア付け、比較、否認、および承認する方法の詳細については、[RFQ 入札価格の入力と比較および契約の授与](tasks/enter-compare-rfq-bids-award-contracts.md) を参照してください。

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>RFQ 活動ログは削除されない

管理者や Microsoft サポートでさえ、RFQ 活動ログを編集または削除できる人は誰もいません。 この制限は、封緘された入札プロセスの公平性を確保するのに役立ちます。 また、正確な監査証跡が維持されるようにするのにも役立ちます。