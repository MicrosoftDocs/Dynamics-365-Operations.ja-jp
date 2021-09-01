---
title: 販売時点管理 (POS) デバイスのライセンス認証
description: この記事では、Cloud POS および Modern POS の新しいガイド付きデバイスの有効化について説明します。
author: athinesh99
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSharedParameters, RetailDevice
audience: IT Pro
ms.reviewer: rhaertle
ms.custom: 18341
ms.assetid: 3dc4c413-e341-4d01-bc49-dc24e35dd8a7
ms.search.region: Global
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 253690ce9bcc358f94e23133c7ab3f182c59306d3b26c0e67276f072ed14e05f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758352"
---
# <a name="point-of-sale-pos-device-activation"></a>販売時点管理 (POS) デバイスのライセンス認証

[!include [banner](../includes/banner.md)]

この記事では、Cloud POS および Modern POS の新しいガイド付きデバイスの有効化について説明し、ユーザーが手動で登録およびデバイス ID 情報を入力しなくても簡単にデバイスをアクティブ化できるクライアントの簡略化について説明します。 

## <a name="checklist-to-follow-before-activation"></a>起動前のチェックリスト

1. 本部 (HQ) で **有効化のためにデバイスを検証** チェックを完了し、デバイスが検証をパスしたことを確認します。
2. デバイスを有効化しているクライアント マシンで、Commerce Scale Unit URL 正常性チェックにアクセスし、正常性チェックが承認されていることを確認します。 次の形式を使用します: `https://clxtestax404ret.cloud.test.dynamics.com/en/healthcheck?testname=ping`。
3. 作業者は、Microsoft Azure Active Directory (AAD) アカウント (**外部 ID 下**) にマップする必要があります。
4. マッピングする AAD アカウントは、同じテナントに属している必要があります。
5. 作業者を AAD アカウントにマップするには、Microsoft Dynamics Lifecycle Services (LCS) の管理者アカウントを使用して HQ に サインインします。
6. 作業者がマネージャー ロール内のユーザーとして設定されていることを確認します (検証でチェックされます)。
7. チャネルが公開されていることを確認します (検証でチェックされます)。
8. チャネル データベースに本社から同期したデータが含まれており、ダウンロード ジョブが実行されていることを確認します。 これを確認するには、ストアのチャネル データベースで次のコマンドを実行します。

    ```sql
    select * from crt.STORAGELOOKUPVIEW
    ```

    データが返され、結果が空ではないことを確認します。

9. **登録** (検証によって確認) でハードウェア プロファイルを設定します。
10. レジスターおよび店舗に画面レイアウトがあることを確認します (検証でチェックされます)。
11. 基本住所が法人に対して設定されていることを確認します。
12. 言語が Commerce Data Exchange: Real-time Service ユーザー プロファイル (デモ データでの JBB) に設定されていることを確認します。
13. リアルタイム サービス プロファイルに適切なアクセス許可があることを確認します。
14. 電子決済 (EFT) のコンフィギュレーションの値があることを確認します。

## <a name="activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation"></a>ガイド付きの有効化を使用して、Modern POS または Cloud POS デバイスを有効化

1. Modern POS またはクラウド POS 用の初期デバイスの有効化ページを開きます。 サインインするように求められます。
2. **始める前に** ページで、指示に従い、**次へ** をクリックします。

    ![POS ウィザード (ページを開始する前に)。](media/p24.png)

3. Cloud POS または Modern POS を起動します。
4. AAD 資格情報を使用してサインインします。 AAD アカウントが既にマッピングされている必要があります。 手順については、[Modern POS (MPOS) のコンフィギュレーション、インストール、および有効化](../retail-modern-pos-device-activation.md) を参照してください。 クラウド POS で、サーバー URL は、アドレス バーに自動的に入力されます。 Modern POS で、サーバー URL をコピーし貼り付ける必要があります。

    [![POS ウィザード、サーバー URL ページの追加。](./media/p18.png)](./media/p18.png)

5. 店舗のリストを入力するには、**次へ** をクリックします。
6. 一覧で適切な店舗を選択します。

    [![POS ウィザード、店舗ページの選択。](./media/p20.png)](./media/p20.png)

7. 適切なレジスターとデバイスを選択します。 

    > [!NOTE]
    > このデバイスは **保留中**、**非有効化**、または **有効化** とすることができます。 または、HQ で **デバイスをストアからレジスターに関連付ける** 設定を有効にする場合と、関連付けられているデバイスを持たないレジスターの一覧を表示する可能性があります。 

    [![POS ウィザード、レジスターおよびデバイス ページの選択。](./media/p22.png)](./media/p22.png)

8. **有効化** をクリックします。 デバイスを有効化する必要があります。 

    [![POS ウィザード、有効化されたデバイスのページ。](./media/p23.png)](./media/p23.png)

## <a name="create-a-device-id-from-modern-pos-and-cloud-pos"></a>モダン POS とクラウド POS からデバイス ID を作成する

Modern POS または Cloud POS からデバイスを作成する (すなわち、自動的にデバイス ID を生成する) 機能を追加しました。これにより、デバイスがまだマップされていないレジスターにデバイスを関連付けることができます。 この機能は、HQ の設定を次のように設定した場合にのみ Modern POS で使用できます。

1. **Retail とコマース** &gt; **バックオフィスの設定** &gt; **パラメーター** &gt; **コマース共有パラメーター** &gt; **全般** の順に移動します。
2. **デバイス** で **デバイスからの登録を許可する** を **はい** に設定します。
3. Modern POS クライアントで、ガイド付きの有効化フローの **関連付けられているデバイスがありません** とリストされているレジスターを選択するときにデバイスを追加できるようになりました。
4. レジスターを選択した後に、レジスター マッピングを持たないデバイスを選択するか、**またはデバイスを追加** リンクを使用するかのいずれかを使用することができます。
5. **またはデバイスを追加** リンクをクリックし、新しいデバイス ID を入力するか、または **新しいデバイス ID を自動的に作成する** を選択します。
6. **有効化** をクリックして新しいデバイス ID を作成し、選択したレジスタへの関連付け、および有効化が完了します。

## <a name="activate-the-device-for-modern-pos-by-using-a-configuration-file"></a>コンフィギュレーション ファイルを使用して Modern POS のデバイスを有効化

IT プロフェッショナルは、Modern POS と一緒にダウンロードできるコンフィギュレーション ファイルを使用して、Modern POS のデバイス アクティベーションを簡単に設定できるようになりました。 このファイルは、適切な Modern POS デバイス (**Retail とコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **デバイス**) の **デバイス** ページで利用できます。 

[![構成ファイルのダウンロード。](./media/p16_11_16-1024x481.png)](./media/p16_11_16.png) 

コンフィギュレーション ファイルは、Commerce Scale Unit URL、デバイス ID、およびデバイスの有効化のためのレジスター番号を入力するために使用されます。 インストール時に、インストーラーはファイルを選択し、デバイスのライセンチ値を設定します。

> [!IMPORTANT]
> ユーザーは Modern POS セルフサービス パッケージと同じフォルダにファイルを置いて、.exe ファイルを実行する必要があります。

[![コンフィギュレーション ファイル。](./media/p17_11_16-1024x532.png)](./media/p17_11_16.png) 

Modern POS は手動入力モードで起動し、Commerce Scale Unit URL、デバイス ID、およびレジスター ID は、有効化のために事前設定されています。

## <a name="activate-the-device-for-cloud-pos-by-using-syntactic-sugar"></a>糖衣構文を使用して Cloud POS のデバイスを有効化します。

IT プロフェッショナルは、Cloud POS URL の一部として、デバイス ID とレジスター ID を提供することで、Cloud POS のデバイス アクティベーションを設定できるようになりました。 **デバイス** ページの **クラウド POS URL** フィールドにリンクがあります。 (**Retail とコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **デバイス**)。 

Cloud POS は手動入力モードで起動し、Commerce Scale Unit URL、デバイス ID、およびレジスター ID は、有効化のために事前設定されています。

[![クラウド POS URL フィールド。](./media/p15_11_16.png)](./media/p15_11_16.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]