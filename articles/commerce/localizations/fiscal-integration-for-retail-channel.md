---
title: コマース チャネルの会計統合の概要
description: このトピックでは、Dynamics 365 Commerce で使用できる会計統合の機能の概要を提供します。
author: josaw
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 155056eb3a2acd0d66e0ace8d5558929678cb8e3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798784"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>コマース チャネルの会計統合の概要

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>はじめに

このトピックは、Dynamics 365 Commerce で使用できる会計統合の機能についての概要です。 会計統合には、小売業界での税金の詐欺防止を目的とした地方の会計法に従って、販売の会計登録を可能にするさまざまな会計デバイスおよびサービスとの統合が含まれます。 会計統合を使用してカバーすることができる典型的なシナリオを以下に示します:

- 会計プリンターのような、POS (販売時点管理) に接続している会計デバイスに販売を登録してから、顧客に会計レシートを印刷します。
- Retail POS で完了した販売と返品に関する情報を、税務当局が運営する外部の Web サービスに安全に送信します。
- デジタル署名での販売トランザクション データの改ざん防止を保証するのに役立ちます。

会計統合機能は、Retail POS と会計デバイスおよび会計サービスとの統合のさらなる開発とカスタマイズのための共通のソリューションを提供するフレームワークです。 この機能には、特定の国または地域の基本的なシナリオをサポートし、特定の会計デバイスまたはサービスと連携する会計統合サンプルも含まれています。 会計統合サンプルは、コマース コンポーネントのいくつかの拡張機能で構成され、ソフトウェア開発キット (SDK) が含まれます。 会計統合のサンプルの詳細については、「[Retail SDK の会計統合のサンプル](#fiscal-integration-samples-in-the-retail-sdk)」を参照してください。 小売 SDK のダウンロードと使用方法については、[小売 ソフトウェアの開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

他の会計デバイスまたはサービスと Retail POS を統合する、または他の国や地域の要件をカバーするために、会計統合サンプルでサポートされていない他のシナリオをサポートするには、既存の会計統合サンプルを拡張するか、例として既存のサンプルを使用することによって新しいサンプルを作成する必要があります。

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>会計デバイスの会計登録プロセスおよび会計統合サンプル

Retail POS の会計登録プロセスは、1 つまたは複数のステップで構成できます。 各ステップには、1 つの会計デバイスまたはサービスでの特定の取引またはイベントの会計登録が含まれます。 次のソリューション コンポーネントは、ハードウェア ステーションに接続されている会計デバイスの会計登録に参加します:

- **Commerce runtime (CRT) 拡張機能** - このコンポーネントは、会計デバイスとのやり取りにも使用される形式でトランザクション/イベント データをシリアル化し、会計デバイスからの応答を解析し、その応答をチャネル データベースに格納します。 拡張機能は、登録する必要がある特定のトランザクションおよびイベントも定義します。 このコンポーネントは多くの場合、*会計ドキュメント プロバイダー* と呼ばれます。
- **ハードウェア ステーション拡張機能**- このコンポーネントは、会計デバイスとの通信を初期化し、会計ドキュメントから抽出されたトランザクション/イベント データに基づいて会計デバイスに要求とダイレクト コマンドを送信し、会計デバイスからの応答を受信します。 このコンポーネントは多くの場合、*会計コネクタ* と呼ばれます。

会計デバイスの会計統合サンプルには、会計ドキュメント プロバイダーおよび会計コネクター用の、CRT およびハードウェア ステーション拡張機能がそれぞれ含まれています。 次のコンポーネントの構成も含まれます:

- **会計ドキュメント プロバイダー構成** - この構成は、出力メソッドおよび会計ドキュメントの形式を定義します。 また、Retail POS からのデータと、会計デバイス ファームウェアで事前定義されている値との互換性を維持するための、税金と支払い方法のデータ マッピングも含まれています。
- **会計コネクタ構成** - この構成は、特定の会計デバイスとの物理的な通信を定義します。

特定の POS レジスターの会計登録プロセスは、POS 機能プロファイルの対応する設定によって定義されます。 会計登録プロセスの構成、会計ドキュメント プロバイダーおよび会計コネクタ構成のアップロード、およびそれらのパラメーターを変更する方法の詳細については、[会計登録プロセスの設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) を参照してください。

次の例では、会計デバイスの一般的な会計登録実行フローを示します。 フローは、POS でのイベント (たとえば、販売トランザクションの終了処理など) で始まり、次のステップのシーケンスを実装します。

1. POSは、CRT から会計ドキュメントを要求します。
2. CRT は、現在のイベントが会計登録を必要とするかどうかを決定します。
3. 会計登録プロセスの設定に基づいて、CRT は、会計登録に使用する会計コネクタおよび対応する会計ドキュメント プロバイダーを識別します。
4. CRT は、トランザクションまたはイベントを表す会計ドキュメント (たとえば、XML ドキュメント) を生成する会計ドキュメント プロバイダーを実行します。
5. POS は、CRT が準備する会計ドキュメントをハードウェア ステーションに送信します。
6. ハードウェア ステーションは、会計ドキュメントを処理し、会計デバイスまたはサービスに通信する会計コネクタを実行します。
7. POS は、会計デバイスまたはサービスからの応答を分析して、会計登録が正常に完了したかどうかを決定します。
8. CRT は応答をチャネル データベースに保存します。

![ソリューション スキーマ](media/emea-fiscal-integration-solution.png "ソリューション スキーマ")

## <a name="error-handling"></a>エラー処理

会計統合フレームワークは、会計登録中のエラーを処理するための次のオプションを提供します:

- **再試行** – オペレーターは、エラーが迅速に解決され、会計登録が再実行される場合にこのオプションを使用することができます。 たとえば、会計デバイスが接続されていないときや、会計プリンターが用紙切れ、または会計プリンターで紙詰まりがあるときに、このオプションを使用することができます。
- **キャンセル** – このオプションを使用すると、オペレーターは現在のトランザクションまたはイベントの会計登録が失敗した場合に延期することができます。 登録が延期された後も、オペレーターは POS の作業を続けることができ、会計登録に必要のない操作を完了することができます。 会計登録を必要とするイベントが POS で発生すると (たとえば、新しいトランザクションが開かれると)、エラー処理ダイアログ ボックスが自動的に表示され、前のトランザクションが正しく登録されなかったことをオペレーターに通知し、エラー処理オプションを提供します。
- **スキップ** – 特定の条件下で会計登録を省略でき、POS で通常の操作を続行できる場合、オペレーターはこのオプションを使用できます。 たとえば、このオプションは、会計登録が失敗した販売トランザクションを特別な紙の仕訳帳に登録できる場合に使用できます。
- **登録済としてマーク** – オペレーターは、トランザクションが会計デバイスに実際に登録されている (たとえば、会計レシートが印刷された) ときにこのオプションを使用できますが、会計応答がチャネル データベースに保存されているときにはエラーが発生しました。

> [!NOTE]
> **スキップ** および **登録済としてマーク** オプションは、使用する前に、会計登録プロセスで有効化する必要があります。 さらに、対応するアクセス許可をオペレーターに付与する必要があります。

**スキップ** および **登録済としてマーク** オプションを使用すると、エラーの理由や会計登録をスキップしたりトランザクションを登録済としてマークすることの妥当性など、エラーに関する特定の情報を取得できます。 エラー処理のパラメーターを設定する方法の詳細については、[エラー処理の設定](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) を参照してください。

### <a name="optional-fiscal-registration"></a>任意の会計登録

会計登録は、いくつかの操作では必須ですが、他の操作ではオプションの場合があります。 たとえば、通常の販売および返品の会計登録は必須かもしれませんが、顧客預金に関連する操作の会計登録はオプションの場合があります。 この場合、販売の会計登録を完了していないとそれ以降の販売はブロックされますが、顧客預金の会計登録が完了していなくても、販売はブロックされません。 必須操作とオプション操作を区別するために、さまざまなドキュメント プロバイダーを介してそれらを処理し、それらのプロバイダーの会計登録プロセスに別々のステップを設定することをお勧めします。 オプションの会計登録に関連するすべてのステップで、**エラーでも続行** パラメーターを有効にする必要があります。 エラー処理のパラメーターを設定する方法の詳細については、[エラー処理の設定](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) を参照してください。

### <a name="manually-running-fiscal-registration"></a>会計登録を手動で実行

トランザクションまたはイベントの会計登録が失敗後に延期された場合 (たとえば、オペレーターがエラー処理ダイアログ ボックスで **キャンセル** を選択した場合)、 対応する操作を呼び出して手動で会計登録を再実行できます。 詳細については、[延期された会計登録の手動実行を有効にする](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)を参照してください。

### <a name="fiscal-registration-health-check"></a>会計登録の正常性チェック

会計登録の正常性チェック手順では、特定のイベントが発生したときに会計デバイスまたはサービスの使用可能性を確認します。 会計登録を現在完了することができない場合は、オペレーターに事前に通知されます。

次のイベントが発生すると、POS は正常性チェックを実行します。

- 新しいトランザクションが開く。
- 一時停止したトランザクションが呼び出される。
- 販売または返品トランザクションが確定する。

正常性チェックが失敗すると、POS は正常性チェック ダイアログ ボックスを表示します。 このダイアログ ボックスには、次のボタンが表示されます。

- **OK**: このボタンをクリックすると、オペレーターは正常性チェックのエラーを無視して操作の処理を続行できます。 **正常性チェック エラーのスキップを許可** が有効になっている場合にのみ、オペレーターはこのボタンを選択することができます。
- **キャンセル** : オペレーターがこのボタンを選択すると、POS は最後のアクションをキャンセルします (たとえば、アイテムは新しいトランザクションに追加されません)。

> [!NOTE]
> 正常性チェックは、現在の操作で会計登録が必要な場合、および会計登録プロセスの現在のステップで **エラーでも続行** パラメーターが無効になっている場合のみ実行されます。 詳細については、[エラー処理の設定](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)を参照してください。

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>会計トランザクションの会計応答を保存しています。

トランザクションまたはイベントの会計登録が成功すると、チャネル データベースに会計トランザクションが作成され、元のトランザクションまたはイベントにリンクされます。 同様に、**スキップ** または **登録済としてマーク** オプションが、失敗した会計登録に対して選択されている場合、この情報は会計トランザクションに格納されます。 会計トランザクションには、会計デバイスまたはサービスの会計応答が保持されます。 会計登録プロセスがいくつかのステップで構成されている場合は、登録の成功または失敗をもたらしたプロセスの各ステップに対して会計トランザクションが作成されます。

会計トランザクションは、トランザクションと共に *P ジョブ* によって本社に転送されます。 **店舗のトランザクション** ページの **トランザクション** クイック タブで、小売トランザクションにリンクされている会計トランザクションを表示することができます。

会計トランザクションには、次の詳細が格納されます:

- 会計登録プロセスの詳細 (プロセス、コネクタ グループ、コネクタなど)。 この情報が会計応答に含まれている場合は、**登録番号** フィールドに、会計デバイスのシリアル番号も格納します。
- 会計登録のステータス: 登録が成功した場合は **完了**、オペレーターが失敗した登録に **スキップ** オプションを選択した場合は **スキップ済**、オペレーターが **登録済としてマーク** オプションを選択した場合は **登録済としてマーク済**。
- 選択した会計トランザクションに関連する情報コード トランザクション。 情報コード トランザクションを表示するには、**会計トランザクション** クイック タブで、ステータスが **スキップ済** または **登録済としてマーク済** になっている会計トランザクションを選択してから、**情報コード トランザクション** を選択します。

## <a name="fiscal-texts-for-discounts"></a>割引用の会計テキスト

国や地域によっては、さまざまな種類の割引が適用される場合に、会計レシートに印刷する必要がある追加のテキストについての特別な要件があります。 会計統合機能を使用すると、会計レシートの割引明細行の後に印刷される割引用の特別なテキストを設定できます。 手動割引の場合は、POS 機能プロファイルで **製品割引** 情報コードとして指定されている情報コードの会計テキストを構成できます。 割引用の会計テキストを設定する方法の詳細については、[割引用の会計のテキストの設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts) を参照してください。

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>会計 X および会計 Z レポートの印刷

会計統合機能は、統合された会計デバイスまたはサービスに固有の、営業終了時の明細書の生成をサポートします:

- POS 画面レイアウトには、対応する操作を実行する新しいボタンを追加する必要があります。 詳細については、[会計 X/Z レポートを POS から設定する](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos) を参照してください。
- 会計統合サンプルでは、これらの操作は会計デバイスの対応する操作に一致する必要があります。

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Retail SDK の会計統合サンプル

次の会計統合サンプルは、Retail SDK で現在使用できます:

- [イタリア向け会計プリンター統合サンプル](emea-ita-fpi-sample.md)
- [ポーランド向け会計プリンター統合サンプル](emea-pol-fpi-sample.md)
- [オーストリア向け会計登録サービス統合サンプル](emea-aut-fi-sample.md)
- [チェコ共和国向け会計登録サービス統合サンプル](emea-cze-fi-sample.md)
- [スウェーデン向け制御ユニットの統合サンプル](./emea-swe-fi-sample.md)
- [ドイツ向け会計登録サービス統合サンプル](./emea-deu-fi-sample.md)

次の会計統合機能は、Retail SDK でも利用可能ですが、現在は会計統合フレームワークを利用していません。 この機能の会計統合フレームワークへの移行は、今後の更新で予定されています。


- [フランス向けデジタル署名](emea-fra-cash-registers.md)
- [ノルウェー向けデジタル署名](emea-nor-cash-registers.md)

Retail SDK で使用可能な次のレガシ会計統合機能は、会計統合フレームワークを使用せず、それ以降の更新では推奨されません。

- [スウェーデン向け制御ユニットの統合サンプル (レガシ)](./retail-sdk-control-unit-sample.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]