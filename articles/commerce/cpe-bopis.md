---
title: Dynamics 365 Commerce の評価環境で BOPIS を構成する
description: このトピックでは、プロビジョニング後の Microsoft Dynamics 365 Commerce の評価環境における オンライン購入、店舗での受け取り (BOPIS) の構成方法について説明します。
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ec1c556a70ed92a40d3cb2bf45fb6156b7dbf7fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993478"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce の評価環境で BOPIS を構成する

[!include [banner](includes/banner.md)]

このトピックでは、プロビジョニング後の、 Microsoft Dynamics 365 Commerce の評価環境におけるオンライン購入、店頭受取 (BOPIS) を構成する方法について説明します。

## <a name="prerequisite"></a>前提条件

このトピックに記載の手順は、Commerce の評価環境のプロビジョニングと構成が完了した後にのみ実行してください。 環境のプロビジョニングと構成方法については、 [Dynamics 365 Commerce の評価環境をプロビジョニングする](provisioning-guide.md) と [ Dynamics 365 Commerce の評価環境を構成する](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning) を参照してください。

Commerce 環境のプロビジョニングとエンドツーエンドの構成完了後に、このトピックを使用して BOPIS のシナリオを有効化することができます。

## <a name="configure-the-pos"></a>POS の構成

### <a name="configure-modern-pos"></a>Modern POS の構成

クレジット カードの支払を含む BOPIS シナリオには、ハードウェア ステーションが必要です。 ハードウェア ステーションは、Windows 用および、 Android 用 Modern POS プログラムに組み込まれています。 iOS 用の Cloud POS または Modern POS を使用している場合、販売時点管理（POS）クライアントは、共有ハードウェア ステーションとペアリングする必要があります。 このトピックでは、Windows 用 BOPIS と Android クライアントの設定方法について説明します。 共有ハードウェア ステーションを設定する方法の詳細については、[小売りハードウェア ステーションの設定とインストール](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation) を参照してください。

1. **小売りとコマース\> チャンネル設定 \> POS 設定 \> レジスター の順に移動します**。
2. **SANFRAN-5** の登録を選択し、 **編集** を選択します。
3. **ハードウェア プロファイル** フィールドの値を **HW002** から **HW001** に変更し、**保存** をクリックします。
4. 変更を同期するには、、**小売りと Commerce \> 小売りとCommerce IT \> 配送スケジュール** の順に移動します。
5. 配送スケジュールに **1090** を選択し、アクション ウィンドウで **今すぐ実行** を選択します。
6. **はい** を選択し、続いて **OK** をクリックしてデータの同期を開始します。 

### <a name="install-modern-pos"></a>Modern POS のインストール

1. **小売りとコマース\> チャンネル設定 \> POS 設定 \> デバイス の順に移動します**。
2. デバイスに **SANFRANCIS-5** を選択します。
3. アクション ウィンドウで **ダウンロード** を選択し、続いて **構成ファイル** を選択します。
4. **ダウンロード** を選択し、**Retail Modern POS** を選択します。 
5. **ModernPOSSetup** ファイルのダウンロードが完了したら、**ファイルを開く** を選択します。

    ![ファイルを開きます](./dev-itpro/media/PAYMENTS/openfile.png)

6. インストール プロセスを開始するには、**次へ** を選択します。 インストールが完了したら、**閉じる** を選択します。

### <a name="activate-modern-pos"></a>Modern POS の有効化

1. Windows デスクトップで、 **スタート** ボタンを選択し、**Retail Modern POS** と入力します。
2. **Retail Modern POS** アプリケーションを選択して、有効化を開始します。
3. **次へ** を選択します。 **サーバー URL**、 **デバイスID**、 **登録番号** の各フィールドには、前述の手順でダウンロードした構成ファイルの情報を使用して事前設定を行う必要があります。
4. **有効化** を選択します。
5. 認証ダイアログ ボックスが表示されます。 既に作業者 **000713-Andrew Collette** に関連付けられている電子メール アドレスを使用するアカウントを選択します。

    > [!NOTE]
    > 作業者に ID が関連付けられていない場合、有効化は失敗します。 この場合は、トピック [Dynamics 365 Commerce 評価環境の構成](cpe-post-provisioning.md#associate-a-worker-with-your-identity) 配下の「作業者とあなたの ID を関連付ける」 に記載の手順に従ってください。
    
6. 組織によるデバイス管理を許可するかどうかを確認するメッセージが表示された場合は、**このアプリのみ** を選択します。
7. 有効化が完了したら、**開始する** を選択します。

### <a name="enable-bopis-in-modern-pos"></a>Modern POS の BOPIS を有効化する

1. オペレーター ID に **000713**、パスワードに **123** を使用して Modern POS にサインインします。
2. 入門者向けチュートリアルビデオの再生中に、ダイアログボックスの左下隅にある 2 つのチェック ボックスをオンにして、ダイアログ ボックスを閉じます。
3. シフトの終了を確認するメッセージが表示されない場合は、**ようこそ** ページを右方向に にスクロールし、 **シフトを閉じる** を選択してから、POS に再度サインインします。
4. サイン イン後、メッセージが表示されたら **ドロワー以外の操作の実行** を選択します。
5. **ようこそ**  ページで右にスクロールし、**ハードウェア ステーションの選択** 操作を選択します。
6. **管理** を選択し、**ハードウェア ステーションを使用する** オプションを **オン** に設定して **OK** を選択します。
7. POS からサインアウトし、再度サインインします。
8. ログイン後、**新規シフトを開く** を選択し、 **ドロワー** を選択します。

## <a name="complete-a-bopis-scenario"></a>BOPIS シナリオを完了する

### <a name="create-a-storefront-order-for-in-store-pickup"></a>店舗内集配用のウェブストア注文を作成する

1. 環境の構成をする過程の [e コマースの初期化](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) ステップで指定したURLに移動します。
2. 品目を選択し、**カートに追加する** を選択します。
3. [ショッピングバッグ] ページで、追加した注文明細行に対して **これを選択する** を選択します。
4. **店舗の選択** ダイアログ ボックスで、**サンフランシスコ** と入力し、**検索** ボタンを選択します。
5. 結果の一覧で、サンフランシスコの店舗を見つけ、**ここで集荷する** を選択します。
6. [ショッピングバッグ] ページで、**ゲストとしてチェックアウト** を選択します。 

    > [!NOTE]
    > チェックアウトを続行するには、Cookie の通知に同意する必要があります。 この通知は、チェック アウトページの上部にバナーとして表示されます。

7. クレジット カードの支払方法については、次の情報を入力します。

    - **カード名義人名:** 名前を入力します。
    - **カード番号:** **4111-1111-1111-1111** を入力します。
    - **有効期限:** **10/20** を入力します。
    - **カードのセキュリティー コード (CVV) :** **737** を入力します。

    > [!IMPORTANT]
    > どのような状況でも、テスト サイトで実際のクレジット カード情報は絶対に使用しないでください。

8. 請求先住所の詳細を入力し、**保存して続行** を選択し、チェック アウトを続行します。
9. 注文の準備ができたら、**チェックアウト** を選択します。

### <a name="synchronize-online-orders-to-the-back-office"></a>オンライン注文をバック オフィスに同期します

オンライン注文を同期する方法の詳細については、[オンライン販売と支払の転記](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments) を参照してください。

### <a name="pick-up-an-order-in-the-store"></a>店頭で注文を集荷する

1. POS へのサインイン
2. **ようこそ** 画面で、**注文の履行** を選択します
3. 集荷対象商品の一覧では、オンラインで注文した商品の中から明細行を選択します。
4. 注文明細行が選択されている間、**集荷** を選択します。

    [トランザクション] 画面に明細行品目が追加され、**$0.00** が期日の残高として表示されます。

5. **$0.00** の未払の残高を選択するか、取引を完了する支払方法を選択します。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>POS で取得したオンライン注文の残高がゼロではない場合

店舗内集配の注文が取得されたときに、[未払残高] が0ではない場合は、Modern POSが使用されていること、およびハードウェア ステーションが有効になっていることを確認してください。 IOS 用 クラウド POS または Modern POS を使用している場合は、共有ハードウェア ステーションが有効になっていることを確認してください。 オンラインで行われた支払を取得するには、何らかの形式の有効なハードウェア ステーションが必要です。

### <a name="general-issues-with-payment-capture"></a>決済のキャプチャに関する一般的な問題

すべての一般的な問題については、Modern POS またはインターネット インフォメーション サービス（IIS）ハードウェア ステーション イベント ログを常に参照してください。 これらのログは、Windows イベント ログの以下のノードにあります：

- アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-ModernPOS
- アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-Hardware Station

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 評価環境の概要](cpe-overview.md)

[Dynamics 365 Commerce 評価環境をプロビジョニングする](provisioning-guide.md)

[Dynamics 365 Commerce 評価環境のオプション機能を構成する](cpe-optional-features.md)

[Dynamics 365 Commerce 評価環境に関するよく寄せられる質問](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure ポータル](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce Web サイト](https://aka.ms/Dynamics365CommerceWebsite)

[Adyen 支払コネクタ](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[オンライン支払手段を Adyen コネクタで保存](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[オムニ チャネル支払の概要](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
