---
title: ブラジル向け Dynamics 365 Commerce ローカライズの設定と展開
description: このトピックでは、ブラジル向け Microsoft Dynamics 365 Commerce ローカライズの設定と展開の方法について説明します。
author: akviklis
ms.date: 12/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.region: Brazil
ms.search.industry: Retail
ms.author: akviklis
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d86d7549b8aae3dd1565e90a4c3e69fbc6e09e28
ms.sourcegitcommit: 013196e9737acfc9a3d1f842f351e95f79f64d36
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/01/2021
ms.locfileid: "7878881"
---
# <a name="set-up-and-deploy-the-dynamics-365-commerce-localization-for-brazil"></a>ブラジル向け Dynamics 365 Commerce ローカライズの設定と展開

[!include[banner](../includes/banner.md)]

このトピックでは、ブラジル向け Microsoft Dynamics 365 Commerce ローカライズの設定と展開の方法について説明します。

ブラジル向け Dynamics 365 Commerce ローカライズには、次の Commerce コンポーネントが含まれます: Commerce Runtime (CRT)、Retail Server、および販売時点管理 (POS)。 これらの拡張機能を使用すると、電子会計書類の登録が延期される場合、ブラジル固有の税金の計算、小売販売用の電子会計ドキュメントの生成、カスタムフィールドを持つ DANFE (Documento Auxiliar de Nota Fiscal Eletrônica) の会計レシートの印刷、ブラジル固有の顧客情報の管理、オフライン代替モードでの販売の発行が可能になります。 ブラジル向け Commerce ローカライズの詳細については、[ブラジルのローカライズ スコープ](../../finance/localizations/latam-bra-scope.md) および[ブラジル向け Commerce ローカライズ](latam-bra-commerce-localization.md) を参照してください。

このトピックで説明する拡張機能は、会計統合のフレームワークに基づいて開発されました。 会計統合機能の詳細については、[Commerce チャネルの会計統合の概要](fiscal-integration-for-retail-channel.md) を参照してください。 [電子申告 (ER) は ](../../dev-itpro/analytics/general-electronic-reporting.md)、電子会計ドキュメントの電子化の形式を実装するために使用されます。

## <a name="enable-brazil-specific-commerce-functionality"></a>ブラジル固有の Commerce 機能の有効化

このセクションでは、ブラジルに固有で推奨される Commerce 本社の設定を構成する方法について説明します。 詳細については、[Commerce のホーム ページ](../index.md) を参照してください。

ブラジル固有の機能を有効にして使用するには、Commerce 本社で次の設定を構成する必要があります。

1. 法人の基本住所で、**国/地域** フィールドを **BRA** (ブラジル) に設定します。
1. ブラジルにあるすべての店舗の POS 機能プロファイルで、 **ISO コード フィールド** を **BR** (ブラジル) に設定します。
1. **システム管理 \> ワークスペースs \> 機能の管理** に移動し、**すべて** タブで、次の機能キーを有効にします。

    - (ブラジル) ブラジルに固有の Commerce 機能
    - 小売明細書 - トリクル フィード
    - 会計統合フレームワークの内部および外部コネクタのサポート
    - ドキュメントの登録の延期
    - 小売店舗のユーザー定義の証明書プロファイル

## <a name="set-up-electronic-reporting"></a>電子申告の設定

Microsoft Dynamics Lifecycle Services (LCS) から電子会計ドキュメント用の ER コンフィギュレーションをダウンロードできます。 詳細については、[電子申告 (ER) コンフィギュレーションのインポート](../../dev-itpro/analytics/electronic-reporting-import-ger-configurations.md) を参照してください。 次の手順に示すコンフィギュレーションの最新バージョンをダウンロードする必要があります。

Commerce 本社で電子申告を設定するには、次の手順を実行します。

1. **組織管理 \> ワークスペース \> 電子申告** の順に移動します。
1. **Microsoft** コンフィギュレーション プロバイダーのタイルで、省略記号 (**...**)を選択し、**有効に設定** を選択します。
1. タイルで **リポジトリ** を選択します。
1. **グローバル** コンフィギュレーション リポジトリを選択し、アクション ペインで **開く** を選択します。
1. **Regulatory Configuration Service に接続する** ダイアログ ボックスで、**Regulatory Configuration Service に接続するには、ここをクリックしてください** を選択し、ダイアログ ボックスに戻って **OK** を選択します。
1. 次のデータ モデル、データ モデル マッピング、および形式コンフィギュレーションの最新の共有バージョンをインポートします。

    - 会計ドキュメントのマッピング
    - NF-e キャンセル エクスポートの形式 (BR)
    - NF-e 状態要求エクスポートの形式 (BR)
    - NF-e 送信エクスポートの形式 (BR)
    - NFC-e 送信エクスポートの形式 (BR)
    - NFC-e コンティンジェンシー エクスポートの形式 (BR)
    - NFC-e 会計ドキュメントのマッピング
    - NFC-e 会計ドキュメントの検証形式 (BR)

1. **組織管理 \> ワークスペース \> 電子申告** の順に移動し、**コンフィギュレーションをレポートする** を選択します。
1. **会計ドキュメントのマッピング** を選択し、**既定のモデル マッピング** オプションを **いいえ** に設定します。
1. **NFC-e 会計ドキュメントのマッピング** を選択し、**既定のモデル マッピング** オプションを **はい** に設定します。
1. **組織管理 \> 設定 \> ブラジル パラメーター** の順に移動します。
1. **小売タブ** の **形式マッピング** フィールドで、**NFC-e 会計ドキュメント検証形式 (BR)** を選択します。

## <a name="set-up-a-fiscal-establishment-and-nf-e-federal-parameters"></a>会計施設および NF-e パラメーターの設定

Commerce 本社に会計施設および NF-e (Nota Fiscal Eletrônica) の連邦パラメータを設定するには、次の手順に従います。

1. **組織管理 \> 組織 \> 会計機関 \> 会計機関** の順に移動します。
1. **税務登録番号 - CNPJ, IE & CCM** フィールドで、税登録番号を入力します。 (CNPJ は *Cadastro Nacional da Pessoa Jurídica*、IE は *Inscrição Estadual*、CCM は *Cadastro de Contribuinte Mobiliário* を意味します。)
1. **施設の住所フィールド** で、住所を入力します。
1. CSC トークンと CS C英数字のコードを入力して、CSC (Código de Segurança do Contribuinte) 暗号化を設定します。
1. 税務当局サービスによる認証と会計ドキュメントのデジタル署名に適切なデジタル証明書を選択します。

    > [!NOTE]
    > **会計施設** ページで構成された証明書は、オフライン代替モードで POS で発行され、Commerce 本社を通じて承認のために送信される NFC-e (Nota Fiscal de Consumidor Eletrônica) ドキュメントに使用されます。 会計ドキュメントをオフライン代替モードで署名できるようにするには、POS のオフライン証明書ストレージに証明書をインストールする必要があります。 詳細については、[オフライン代替モードでの商品の現金店頭払い売上の作成](latam-bra-nfce.md#scenario-3-make-a-cash-and-carry-sale-of-goods-in-offline-contingency-mode) および[代替モードで発行された NFC-e の登録の延期](latam-bra-nfce-contingency-mode.md) を参照してください。

1. **NF-E WEB SERVICE** の、**環境** フィールドで、**テスト** または **生産** を選択します。
1. **NFC-E WEB SERVICE** の、**環境** フィールドで、**テスト** または **生産** を選択します。
1. NF-e および NFC-e 機能のバージョンを指定します。
1. **NF-E WEB SERVICE** の、**所轄官庁** フィールドで、**NF-e 連邦パラメーター \> Web サービス \> 所轄官庁** で使用される値を入力します。
1. **NFC-E WEB SERVICE** の、**所轄官庁** フィールドで、**NF-e 連邦パラメーター \> Web サービス \> 所轄官庁** で使用される値を入力します。
1. **組織の管理 \> 組織 \> 会計施設 \> 電子会計ドキュメント \> NF-e 連邦パラメーター** の順に移動します。
1. 必要な状態に対して新しい所轄官庁を作成するか、既存の所轄官庁を使用します。
1. 各状態について、**NFC-e の照会のインターネット アドレス** フィールドに、QR コード URL を入力します。
1. 各状態について、適切な環境のすべての Web サービスのエンドポイントを指定します。

## <a name="set-up-address-books"></a>アドレス帳を設定します

Commerce 本社のブラジルの顧客、店舗、および作業者に同じアドレス帳を追加するには、次の手順に従います。

1. **Retail とコマース \> 顧客 \> 顧客サービス** の順に移動します。
1. **一般** タブの **アドレス帳** フィールドで、必要に応じて顧客の小売アドレス帳を追加します。
1. **Retail と Commerce \> チャンネル \> 店舗 \> すべての店舗** の順に移動します。
1. **一般** タブの **顧客アドレス帳** フィールドおよび **従業員アドレス帳** フィールドで、店舗のアドレス帳を追加します。
1. **Retail と Commerce \> 従業員 \> 作業者** の順に移動します。
1. **作業者集計** タブの **アドレス帳** フィールドで、作業者のアドレス帳を追加します。

## <a name="set-up-sales-tax-for-pos"></a>POS の消費税を設定します

Commerce 本社で POS の消費税を設定するには、次の手順を実行します。

1. **税 \> 間接税 \> 売上税 \> 売上税コード** の順に移動します。
1. さまざまな税タイプと税コードに対して必要な消費税コードを作成します。 返品による消費税コードを含めます。
1. **税 \> 間接税 \> 売上税 \> 消費税グループ** の順に移動します。
1. 小売販売および返品用の消費税グループを作成し、作成した消費税コードを追加します。
1. **Retail と Commerce \> チャンネル \> 店舗 \> すべての店舗** の順に移動します。
1. **消費税グループ** および **返品用の消費税グループ** フィールドで、作成した消費税グループを選択します。
1. **税 \> 間接税 \> 消費税 \> 品目消費税グループ** の順に移動します。
1. 小売用の品目消費税グループを作成し、作成した消費税コードを追加します。
1. **組織管理 \> セットアップ \> 会計ドキュメント ソース テキスト** へ移動します。
1. 小売税の負担に対する会計ドキュメント ソース テキストを作成します。 **制限** フィールドを **外部** に設定し、**会計情報** オプションを **いいえ** に設定します。
1. **組織管理 \> 設定 \> ブラジル パラメーター** の順に移動します。
1. **小売** タブの **テキスト ID** フィールドで、小売税の負担のソース テキストを指定します。
1. **Retail と Commerce \> 製品とカテゴリ \> カテゴリ別リリース済製品** の順に移動します。
1. 必要な製品を選択し、次のフィールドを設定します。

    - **販売** タブで、次の操作を行います。

        - 品目消費税グループ

    - **会計情報** タブで、次の操作を行います。

        - 課税元
        - 製品タイプ
        - 会計分類コード
        - 概算連邦税率
        - 概算状態税率
        - 概算市税率

1. **税 \> 設定 \> 売上税 \> CFOP コード** の順に移動します。
1. 小売返品に使用する CFOP (Código Fiscal de Operações e de Prestações) コードの **会計参照必須** オプションを **いいえ** に設定します。

## <a name="set-up-a-retail-store"></a>小売店舗の設定

Commerce 本社で小売店舗を設定するには、次の手順を実行します。

1. **在庫管理 \> 設定 \> 在庫詳細 \> 倉庫** の順に移動します。
1. 店舗の倉庫を作成し、住所を指定します。
1. **Retail と Commerce \> チャンネル \> 店舗 \> すべての店舗** の順に移動します。
1. 店舗を作成し、次のフィールドを設定します。

    - 税込価格
    - 売上税グループ
    - 返品用の消費税グループ
    - 既定の顧客

        > [!NOTE]
        > 既定の顧客は、店舗と同じアドレス帳に含める必要があります。

1. 前の手順で作成した店舗の支払方法を設定します。
1. **Retail と Commerce \> 本社の設定 \> コマース スケジューラ** の順にクリックします。
1. 使用するチャネル データベースに、既に作成した店舗を追加します。
1. **小売りとコマース\> チャンネル設定 \> POS 設定 \> レジスター の順に移動します**。
1. POS レジスターを選択し、ブラジル固有の次のフィールドを設定します。

    - NFC-e シリーズ
    - NFC-e 代替シリーズ
    - NF-e シリーズ

1. **小売りとコマース\> チャンネル設定 \> POS 設定 \> デバイス の順に移動します**。
1. 作成した POS レジスター用のデバイスを作成および構成します。
1. **組織管理 \> 組織 \> 組織階層** の順に移動します。
1. **事業単位別小売店舗** 組織階層を選択し、**表示** を選択し、**編集 \> 小売チャネルの挿入** を選択し、既にに作成した店舗を階層内の適切な事業単位に追加します。 次に、変更を公開します。
1. **Retail POS の転記** の目的を、**事業単位別小売店舗** 組織階層に割り当てます。
1. **Retail と Commerce \> チャネル設定 \> チャネル カテゴリと製品属性** に移動します。
1. チャネル更新を公開します。
1. **Retail と Commerce \> チャネル設定 \> POS プロファイル \> レシート プロファイル** の順に移動します。
1. DANFEの レシート レイアウトを作成し、そのレイアウトをレシート プロファイルに追加します。

> [!NOTE]
> レシート設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。 または、ユーザーの既定の会社、およびレシート設定の作成対象の店舗の法人の両方で、同じ言語テキスト設定を作成する必要があります。

レシート形式デザイナーで、必要なレシート形式ごとに、適切なレシート セクションにブラジルのカスタム フィールドを追加します。 レシート形式の使用方法の詳細については、[レシート テンプレートと印刷](../receipt-templates-printing.md) を参照してください。

## <a name="set-up-the-fiscal-registration-process"></a>会計登録プロセスの設定

Commerce 本社で会計登録プロセスを設定するには、次の手順を実行します。 詳細情報については、[コマース チャネルの会計統合の設定](./setting-up-fiscal-integration-for-retail-channel.md) を参照してください。

1. Commerce SDK から会計ドキュメント プロバイダーと会計コネクタのコンフィギュレーション ファイルをダウンロードします。
    1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリ を開きます。
    1. 使用可能な最後のリリース ブランチ (例えば、[リリース/9.31](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.31) を開きます)。
    1. **src \> FiscalIntegration \> ElectronicFiscalDocumentsBrazil** を開きます。
    1. **構成 \> コネクタ** (例えば、[リリース/9.31 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.31/src/FiscalIntegration/ElectronicFiscalDocumentsBrazil/Configurations/Connectors)): で会計コネクタ コンフィギュレーション ファイルをダウンロードします。
        - SubmitConnector.xml
        - SatConnector.xml
        - ContingencyConnector.xml
    1. **構成 \> DocumentProviders** (例えば、[リリース/9.31 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.31/src/FiscalIntegration/ElectronicFiscalDocumentsBrazil/Configurations/DocumentProviders)): で会計ドキュメント プロバイダー コンフィギュレーション ファイルをダウンロードします。
        - SubmitProvider.xml
        - SatProvider.xml
        - ContingencyProvider.xml
1. **Retail とコマース \> 本社の設定 \> パラメーター \> コマース共有パラメーター** の順に移動します。
1. **一般** タブで、**会計統合の有効化** オプションを **はい** に設定します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計コネクタ** に移動し、先ほどダウンロードした会計コネクタ コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** に移動し、先ほどダウンロードした会計ドキュメント プロバイダー コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル** の順に移動します。
1. コンフィギュレーションを読み込んだばかりのドキュメント プロバイダーごとに、コネクタ機能プロファイルを作成し、既にコンフィギュレーションを読み込んだ会計コネクタを選択します。 必要に応じて、データ マッピング設定を更新します。
1. **Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル** の順に移動します。
1. コネクタ技術プロファイルを作成し、既にコンフィギュレーションを読み込んだ会計コネクタを選択します。 必要に応じて、接続設定を更新します。
1. **Retail と Commerc \> チャネル設定 \> 会計統合 \> 会計コネクタ グループ** の順に移動します。
1. 既に作成した各コネクタ機能プロファイル用に、会計コネクタ グループを作成します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 登録プロセス** の順に移動します。
1. 登録プロセスを作成します。 登録手順として、作成した会計コネクタ グループを選択します。
1. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** の順に移動します。
1. 登録プロセスを有効化する店舗にリンクされている機能プロファイルを選択し、**会計登録プロセス** のクイック タブで、作成した登録プロセス番号を選択します。
1. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。
1. 会計プリンターの接続先のハードウェア ステーションにリンクされているハードウェア プロファイルを選択します。
1. **会計周辺機器** クイック タブで、コネクタの技術的なプロファイルを選択します。
1. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。
1. プリンターのハードウェア プロファイルを設定します。
1. **店舗** ページの **ハードウェア ステーション** クイック タブで、ハードウェア ステーションの設定を追加します。 必要に応じて、既に構成したネットワーク プリンターの IP アドレスを構成します。

## <a name="customer-information-management"></a>顧客情報管理

**顧客情報の追加** 操作を使用して、CNPJ または CPF (Cadastro de Pessoas Físicas) などのブラジル固有の顧客税登録番号、および住所を販売トランザクションに追加できます。 顧客情報は、トランザクションに対して指定された顧客レコードから引き出す場合も、手動で入力することもできます。 顧客情報を DANFE の会計レシートに印刷して、請求に使用できます。

Commerce 本社で **顧客住所の追加** を構成するには、次の手順を実行します。

1. **Retail と Commerce \> チャネル設定 \> POS 設定 \> POS \> ボタン グリッド** の順に移動します。
1. 操作を表示するボタン グリッドを選択し、**ボタン グリッド デザイナー** を開きます。
1. ボタンを追加し、**アクション** フィールドで **顧客情報の追加** を選択します。

画面のレイアウトとボタン グリッドの操作方法の詳細については、[販売時点管理 (POS) の画面レイアウト](../pos-screen-layouts.md) を参照してください。

## <a name="enable-customer-searches-based-on-tax-registration-numbers-in-pos"></a>POS での税務登録番号による顧客検索を有効にする

POS で CNPJ/CPF および CCM の税登録番号で顧客を検索できるようにするには、次の手順に従います。

1. Commerce 本部の **コマース パラメーター** ページ、**POS 検索基準** タブ、**顧客検索基準** クイック タブで、レコードを追加します。 
1. 新しいレコードの **顧客検索基準** フィールドで、**税登録番号** を選択します。
1. **絞り込み可能** チェック ボックスはオフにし、**ショートカットとして表示** チェック ボックスを選択します。
1. **配送スケジュール** ページで、1110 のジョブを実行します。

## <a name="set-up-parameters-for-statements"></a>ステートメントのパラメーターを設定します

1. **組織管理 \> 番号順序** の順に移動します。
1. 各店舗 (作業単位) の小売明細書の番号順序を作成および設定します。
1. **参照** クイック タブで、**小売店舗** 領域に対して 2 つの参照を追加します。1 つは **参照値** が **明細書番号** に設定され、もう 1 つは **伝票** に設定されています。
1. **Retail と Commerce \> カタログと品揃え** の順に移動します。
1. 適切な製品を含む品揃えを作成します。
1. **Commerce チャネル** タブで、既に作成した店舗を追加します。 次に、**公開** を選択します。
1. **Retail と Commerce \> チャネル設定 \> チャネル カテゴリと製品属性** に移動し、チャネル更新を公開します。
1. **販売とマーケティング \> 設定 > 返品 \> 廃棄コード** に移動し、廃棄コードを追加します。
1. **Retail と Commerce \> 製品とカテゴリ \> カテゴリ別リリース済製品** の順に移動します。
1. ギフト カードの製品を選択し、**レジスターでブロック** チェック ボックスを選択します。
1. **Retail と Commerce \> 本社の設定 \> パラメーター \> コマース パラメーター** の順にクリックします。
1. **顧客注文** タブで、既に追加した廃棄コードを入力します。
1. **転記** タブで、ギフト カードのパラメータを設定します。 これらのパラメータには、ギフト **ギフト カード会社** および **ギフト カード製品** フィールドが含まれます。

## <a name="configure-a-production-environment"></a>運用環境のコンフィギュレーション

このセクションは、ブラジル向け Commerce のローカライズの Commerce コンポーネントを有効にするための配置ガイドを提供します。

> [!NOTE]
> これらの手順の一部の手順は、使用している製品バージョンによって異なります。 詳細については、 [Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new-home-page.md) を参照してください。

### <a name="use-certificates-for-authentication-with-the-tax-authority-service-and-digital-signing-of-fiscal-documents"></a>税務当局サービスによる認証と会計ドキュメントのデジタル署名に証明書を使用する

Application Object Server (AOS) のデジタル証明書は、Azure Key Vault に格納する必要があります。

Retail Server のデジタル証明書は、ローカルにインストールするか、Key Vault に格納する必要があります。 Retail Server の両方の場所のタイプを同時に構成し、その優先順位に従って使用することもできます。

Key Vault ストレージを操作する方法の詳細については、[Azure Key Vault の使用を開始](/azure/key-vault/key-vault-get-started) および [Azure Key Vault クライアントの設定](../../finance/localizations/setting-up-azure-key-vault-client.md) を参照してください。

Key Vault または Commerce 本社が使用できない場合に、オフラインにするためのフェールオーバーをサポートする[小売店舗のユーザー定義の証明書プロファイル](./certificate-profiles-for-retail-stores.md) を使用することもできます。 この機能は、[小売チャンネルのシークレットを管理 ](../dev-itpro/manage-secrets.md) 機能を拡張します。

> [!NOTE]
> NFC-e ドキュメントをオフライン代替モードで署名できるようにするには、POS のオフライン証明書ストレージに証明書をインストールする必要があります。 詳細については、[オフライン代替モードでの商品の現金店頭払い売上の作成](latam-bra-nfce.md#scenario-3-make-a-cash-and-carry-sale-of-goods-in-offline-contingency-mode) および[代替モードで発行された NFC-e の登録の延期](latam-bra-nfce-contingency-mode.md) を参照してください。

#### <a name="configure-certificates-so-that-they-can-be-used-in-retail-server"></a>Retail Server で使用できる証明書を構成する

Retail Server のブラジルの税務サービス拡張機能は、税務当局サービスによる認証と会計ドキュメントのデジタル署名に証明書を使用します。 Retail Server 証明書の設定は証明書プロファイルによって制御されます。

Retail Server で使用できる証明書を構成するには、次の手順を実行します。

1. **システム管理 \> 設定 \> 証明書プロファイル** の順に移動します。
1. 適切な法人の証明書プロファイルを作成します。
1. 各法人について、**設定** を選択し、次の手順に従います。

    - ローカル証明書の場合は、**場所タイプ** フィールドが **ローカル証明書** に設定されているレコードを作成します。 次に、**拇印** フィールドに値を入力します。
    - Key Vault 証明書の場合は、**場所のタイプ** フィールドが **Key Vault** に設定されているレコードを作成し、**Key Vault 証明書** を選択します。

証明書は、Retail Server または Key Vault が配置されているマシンのローカルの証明書のストレージにインストールされます。 または、両方の場所タイプにインストールして同時に構成し、優先順位に従って使用することもできます。

#### <a name="configure-a-certificate-in-aos"></a>AOS で証明書の構成

税務当局サービスとの認証用の証明書は、Key Vault に格納されます。 この証明書は AOS で使用され、Commerce 本社を通じて、オフライン代替モードの POS で発行された NFC-e ドキュメントを送信します。 「破棄」要求および「置換によるキャンセル」要求のデジタル署名には、証明書も必要です。 証明書のパラメータは、会計施設の設定で指定する必要があります。

AOS で証明書を構成するには、次の手順に従います。

1. **組織管理 \> 組織 \> 会計機関 \> 会計施設** の順に移動します。
1. 税務当局サービスによる認証と会計ドキュメントのデジタル署名に適切なデジタル証明書を選択します。

> [!NOTE]
> 設定が完了したら、Commerce 本社で適切な配送ジョブを実行する必要があります。

### <a name="configure-crt-extension-components"></a>CRT 拡張コンポーネントを構成

CRT 拡張コンポーネントを構成するには、次の手順に従います。

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイルは **Commerceruntime.ext.config** という名前で、インターネット インフォメーション サービス (IIS) Commerce Scale Unit サイトの下の **bin\\ext** フォルダーにあります。

2. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

```xml
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicFiscalServiceBrazil" />
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicFiscalDocumentBrazil" />
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdBrazil" />
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxServiceBrazil" />
 ```
 
3. CRT の Web.config ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **Web.config** で、**\RetailServer\webroot** フォルダーにあります。

4. extensionComposition セクションに新しい拡張ライブラリ名を追加して、この Web.config ファイルを更新します。
 
```xml
<extensionComposition>
 <add source="assembly" value="Microsoft.Dynamics.Retail.RetailServer.ElectronicFiscalDocumentBrazil" />
</extensionComposition>
```

5. Local CRT on Modern POS の拡張コンフィギュレーション ファイルを検索します。

    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーの場所にあります。

6. 拡張コンフィギュレーション ファイルで Local CRT on Modern POS の変更を登録します。

 ```xml
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicFiscalDocumentBrazil.Offline" />
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicFiscalDocumentBrazil" />
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdBrazil" />
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxServiceBrazil" />
 ```

> [!WARNING]
> **Commerceruntime.config** および **CommerceRuntime.MPOSOffline.config** ファイルを編集してはいけません。 これらのファイルはカスタマイズのためのものではありません。

7. Modern POS の Retail プロキシの拡張コンフィギュレーション ファイルを検索します。

    - **Modern POS の Retail プロキシ:** ファイル名は **RetailProxy.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーの場所にあります。

8. 拡張コンフィギュレーション ファイルで Modern POS の Retail プロキシの変更を登録します。

 ```xml
        <retailProxyExtensions>
          <composition>
            <add source="assembly" value="Microsoft.Dynamics.Commerce.RetailProxy.ElectronicFiscalDocumentBrazil" />
          </composition>
        </retailProxyExtensions>
 ```
 
### <a name="enable-modern-pos-extension-components"></a>Modern POS 拡張コンポーネントの有効化

Modern POS 拡張コンポーネントを有効にするには、次の手順に従います。

1. **RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、**実行** コマンドを使用して、Visual Studio から Modern POS を実行できることを確認します。

    > [!NOTE]
    > Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。

1. **extensions.json** ファイルで、次の明細行を追加することによって拡張機能が読み込まれるようにします。

    ```json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/ElectronicFiscalDocument.BR"
            },
            {
                "baseUrl": "Microsoft/TaxRegistrationId.BR"
            }
        ]
    }
    ```

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

1. ソリューションをリビルドします。
1. デバッガーでModern POS を実行し、機能をテストします。

### <a name="enable-cloud-pos-extension-components"></a>Cloud POS 拡張コンポーネントの有効化

Cloud POS の拡張機能コンポーネントを **extensions.json** ファイルに読み込むには、次の行をファイルの適切な部分に追加します。

```json
{
    "extensionPackages": [
        {
            "baseUrl": "Microsoft/ElectronicFiscalDocument.BR"
        },
        {
            "baseUrl": "Microsoft/TaxRegistrationId.BR"
        }
    ]
}
```

## <a name="additional-resources"></a>追加リソース

[ブラジル向け Commerce ローカライズ](latam-bra-commerce-localization.md) 

[ブラジル向け Commerce POS の NFC-e 電子会計ドキュメント](latam-bra-nfce.md)

[ブラジル向け POS の顧客情報管理](latam-bra-customer-information.md)

[ブラジル向け Commerce POS の NFC-e ドキュメントのキャンセルと返品](latam-bra-nfce-cancel-return.md)

[オフライン代替モードで発行された NFC-e ドキュメントの登録延期](latam-bra-nfce-contingency-mode.md)

[Commerce 本社の小売明細書を介してブラジルの会計ドキュメントを投稿](latam-bra-retail-statements.md)
